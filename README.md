# Resumo das Aulas de Azure - DIO

- [Azure](#azure)
- [Criando uma VM](#como-criar-uma-vm)
- [Criando um banco de dados](#criando-uma-instância-sql)

Computação em nuvem é a entrega de serviços pela internet. Esses serviços podem incluir infraestrutura de TI tradicional, como VM, armazenamento, banco de dados e redes. Também se expandem para IoT, ML e IA.

## Azure

O Azure é uma plataforma de serviços em nuvem que oferece diversos recursos computacionais. Esses serviços incluem:

- PaaS (Plataforma como Serviço)
- SaaS (Software como Serviço)
- IaaS (Infraestrutura como Serviço)

O Azure disponibiliza uma ampla gama de soluções, como serviços para bancos de dados, APIs web, containers com Docker e máquinas virtuais — cada um com seu serviço dedicado. Uma grande vantagem é o modelo de cobrança baseado no consumo: você paga apenas pelo que utiliza. Isso torna o Azure uma excelente opção para empresas e desenvolvedores que buscam escalabilidade e flexibilidade.

---

## Como Criar uma VM

VM ou Máquina Virtual (_Virtual Machine_) em poucas palavras é um software que simula um ambiente de hardware completo. Ela usa as configurações do host para espelhar um SO (_Operating System_ ou, em português, Sistema Operacional).

Na plataforma do Azure, depois que criamos a nossa conta, veremos este painel:

![Painel Home](/Images/1.png)

Devemos ir em `Criar Recurso`. Um recurso é qualquer coisa que você pode criar, provisionar ou implantar, como:

- VMs
- Redes Virtuais
- Banco de dados
- Serviços cognitivos

Feito isso, a janela para criar recurso é aberta:

![Criar Recursos](/Images/2.png)

Devemos procurar por `Máquina Virtual` e clicar nela.

Para criar uma VM no Azure, devemos seguir algumas etapas dadas pela própria plataforma. Não abordarei todas as etapas, vamos criar uma VM simples.

![Etapa 1](/Images/3.png)

Explicando de forma rápida as opções:

- Assinatura: É o tipo de assinatura que você possui. No Azure, as assinaturas são uma unidade de gerenciamento, cobrança e escala.
- Grupo de Recursos: Definir grupos de recursos é uma boa prática, pois assim conseguimos organizar nosso trabalho. Em um uso mais avançado, podemos definir assinaturas por grupos de recursos, separando ainda mais os custos e deixando a plataforma mais organizada.
- Nome da máquina virtual: Aqui é onde colocamos o nome da VM.
- Região: Região é um tópico importante. Uma região é uma área geográfica do planeta que contém pelo menos um data center, mas possivelmente vários, nas proximidades e conectados a uma rede de baixa latência. Devemos nos atentar para escolher uma que se adeque ao nosso plano de assinatura.
- Opções de Zona e Zona de disponibilidade: Podemos deixar como está. Zonas de disponibilidade são datacenters separados fisicamente dentro de uma região do Azure. Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. Uma zona de disponibilidade é configurada para ser um limite de isolamento. Se uma zona ficar inativa, as outras continuarão funcionando.
- Tipo de segurança: Também podemos deixar o padrão.
- Imagem: Aqui é onde escolhemos nossa imagem, deixarei o Ubuntu Server mesmo.

No geral, é isso que precisamos para criar uma primeira máquina virtual. Podemos ir em `Revisar + Criar`, mas o Azure possui outras etapas para configurarmos, sendo elas:

- Discos
- Rede
- Gerenciamento
- Monitoramento
- Avançado
- Marcas

## Criando uma Instância SQL

Voltando ao painel principal, podemos ir em `Banco de dados SQL` e clicar em `criar`.

![Criar DB](/Images/4.png)

A nova janela é:

![Etapa 1](/Images/5.png)

Aqui, algumas etapas se assemelham às da criação da [Máquina Virtual](#como-criar-uma-vm), então vou explicar o que difere.

Devemos clicar no link `criar novo` para criar nosso servidor. O servidor é importante para rodar nosso banco de dados.

Com a janela aberta:
![Criar servidor](/Images/6.png)

Devemos seguir as etapas para a criação:

- Nome do servidor: Devemos colocar um nome para nosso servidor, que será acessado pela URL `nome.database.windows.net`.
- Localização: É onde o nosso servidor estará hospedado.
- Autenticação: O Microsoft Entra ID é a solução de gerenciamento de identidade e acesso baseada em nuvem da Microsoft. Vamos deixar como está.
- Definir administrador do Microsoft Entra: Devemos definir um administrador para o recurso. Ao clicar, isso aparecerá ao lado, escolha um usuário para ser o administrador.

![Azure AD](/Images/7.png)

Depois, clique em `selecionar` e em `ok`.

Depois disso, podemos ir em `Revisar + Criar` e criaremos um banco de dados básico para os estudos.

Para uma implementação mais correta, devemos nos atentar aos outros passos, como:

- Rede
- Segurança
- Configurações adicionais
- Rótulos

Um banco de dados é um IaaS, ou seja, devemos tomar cuidado com a infraestrutura que estamos criando para não extrapolar os recursos. Esse é um dos serviços em que temos mais liberdade, então devemos ter cuidado

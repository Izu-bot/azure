# Resumo das Aulas de Azure - DIO

- [Azure](#azure)
- [Criando uma VM](#como-criar-uma-vm)

Computação em nuvem é a entrega de serviços pela internet. Esses serviços podem incluir infraestrutura de TI tradicional como VM, Armazenamento, Banco de dados e redes. Também expandem para IoT, ML e AI

## Azure

O Azure é uma plataforma de serviços em nuvem que oferece diversos recursos computacionais. Esses serviços incluem:

- PaaS (Plataforma como Serviço)
- SaaS (Software como Serviço)
- IaaS (Infraestrutura como Serviço)

O Azure disponibiliza uma ampla gama de soluções, como serviços para bancos de dados, APIs web, containers com Docker e máquinas virtuais — cada um com seu serviço dedicado. Uma grande vantagem é o modelo de cobrança baseado no consumo: você paga apenas pelo que utiliza. Isso torna o Azure uma excelente opção para empresas e desenvolvedores que buscam escalabilidade e flexibilidade

---

## Como Criar uma VM

VM ou Máquina Virtual (_Virtual Machine_) em poucas palavras é um software que simula um ambiente de hardware completo, ele usa as configurações do host para espelhar um OS (_Operating System_ ou em português Sistema Operacional)

Na plataforma do Azure depois que criamos a nossa conta veremos esse painel

![Painel Home](/Images/1.png)

Devemos ir em `Criar Recurso`. Um recurso é qualquer coisa que você pode criar, provisionar, implantar, como:

- VMs.
- Redes Virtuais.
- Banco de dados.
- Serviços cognitivos

Feito isso, a janela pra criar recurso é aberta
![Criar Recursos](/Images/2.png)

Devemos procurar por `Máquina Virtual` e clicar nela

Para criar uma MV no Azure devemos seguir algumas etapas dadas pela propria plataforma. Não abordarei todos as etapas, vamos criar uma VM simples

![Etapa 1](/Images/3.png)

Explicando de forma rápida as opções:

- Assinatura = É o tipo de assinatura que você possui, no Azure as assinaturas são uma unidade de gerenciamento, cobrança e escala.
- Grupo de Recursos = Definir grupos de recursos é uma boa prática pois assim conseguimos organizar nosso trabalho com grupo de recursos. Em um uso mais avançado, podemos definir assinaturas por grupos de recursos, separando ainda mais os custos e deixando a plataforma mais organizada.
- Nome da máquina virtual = Aqui é onde colocamos o nome da vm
- Região = Região é um tópico importante, uma região é uma área geográfica do planeta que contém pelo menos um data center, mas possivelmente vários, nas proximidades e conectado a uma rede de baixa latência. Devemos nos atentar para escolhermos uma que se adeque ao nosso plano de assinatura
- Opções de Zona e Zona de disponibilidade = Podemos deixar como está. Zonas de disponibilidade são datacenters separados fisicamente dentro de uma região do Azure. Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. Uma zona de disponibilidade é configurada para ser um limite de isolamento. Se uma zona ficar inativa, as outras continuarão funcionando.
- Tipo de segurança = Também podemos deixar o padrão
- Imagem = Aqui é onde escolhemos nossa imagem, deixarei o Ubuntu server mesmo

No geral é isso que precisamos para criar uma primeira máquina virtual, podemos ir em `Revisar + Criar`, mas o Azure possui outras etapas para configurarmos, sendo elas:

- Discos
- Rede
- Gerenciamento
- Monitoramento
- Avançado
- Marcas

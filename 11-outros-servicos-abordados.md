# Outros Serviços abordados

- O **Amazon Elastic Compute Cloud (Amazon EC2)** oferece a
  **plataforma de computação** mais ampla e aprofundada, com opções de
  processadores, armazenamentos, redes, sistemas operacionais e modelos de
  compras para ajudar você a atender melhor às necessidades da sua carga de
  trabalho(_workload_);

- **Amazon EC2 Autoscaling** permite que você
  **adicione ou remova automaticamente instâncias** do Amazon EC2 em resposta à
  alteração da demanda da aplicação;

- **Elastic Load Balancing (ELB)** é o serviço que
  **distribui automaticamente o tráfego** de entrada de aplicação entre vários
  recursos, como instâncias do Amazon EC2;

- **AWS Simple Notification Service (SNS)** é um serviço de **_publish/subscribe_**
  (pub/sub), ele envia **notificações** de duas maneiras: A2A e A2P. A maneira
  A2A fornece um sistema de mensagens com alto throughput e baseado em _push_ para
  mensagens entre diversos sistemas distribuídos, microsserviços e aplicações
  sem servidor orientadas à eventos. Essas aplicações incluem o Amazon SQS, o
  Amazon Kinesis Data Firehose, o AWS Lambda e outros endpoints HTTPS. A
  funcionalidade A2P, por sua vez, permite o envio de mensagens para seus
  clientes utilizando textos SMS, notificações por push e e-mail;

- **AWS Simple Queue Service (SQS)** é um serviço de **enfileiramento de mensagens**,
  permitindo que você envie, armazene e receba mensagens entre componentes de
  software em qualquer volume, sem perder mensagens ou precisar que outros
  serviços estejam disponíveis;

- **AWS Lambda** é um serviço que se pode fazer **upload de códigos** na função
  do Lambda **sem se preocupar com servidores**, configurando-se um gatilho
  (_trigger_) pelo qual o serviço aguarda, quando detectado, o código é executado
  pelo ambiente que não precisa se preocupar, pois ele é altamente dimensionável
  e disponível. Você paga apenas pelo tempo de computação consumido, isso se
  aplica ao tempo em que o código fica em execução;

- **Elastic Container Service (ECS)** e o **Elastic Kubernetes Service (EKS)**
  são serviços de **orquestração de contêineres do docker**. Quando utilizamos
  contêineres na AWS é preciso que haja processos para iniciar, parar, reiniciar
  e monitorar, não apenas um, mas vários deles juntos, o que é chamado de
  cluster. O processo de realização dessas tarefas é chamado de orquestração de
  contêiner;

- **AWS Fargate** é uma plataforma de **computação serveless para ECS ou EKS**;

  > Caso precise ter acesso total ao sistema operacional, o ideal é utilizar o EC2.
  > Caso sejam funções curtas, aplicações orientadas à serviço ou à eventos, sem
  > provisionamento ou gerenciamento de servidores, melhor utilizar o AWS Lambda.

- O **AWS Quick Starts** serve para automatizar a implantação de _workloads_ no
  ambiente AWS;

- **AWS CodeArtifact** é um serviço gerenciado de **repositório de artefatos**
  que armazena e compartilha software pronto para implantação. O CodeArtifact
  **não é um serviço de gerenciamento de código-fonte**;

- **AWS CodeBuild** é um serviço que ajuda os usuários a **compilar**
  automaticamente o código-fonte, **executar testes de unidade** e
  **produzir pacotes de software prontos** para implantação;

- **AWS CodePipeline** é um serviço que **gerencia a movimentação do código**
  entre os serviços individuais;

- O **AWS CodeCommit** é um serviço de **controle de versão do código-fonte**.
  O CodeCommit ajuda os usuários a armazenar e gerenciar o código-fonte dos
  desenvolvedores na AWS;

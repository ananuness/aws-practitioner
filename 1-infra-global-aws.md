# Infraestrutura global da AWS

### Conceitos

- **Região:** é um local físico no mundo em que temos várias zonas de
  disponibilidade;
- **Zona de Disponibilidade:** é uma parte totalmente isolada da infraestrutura
  global da AWS, em que consiste em um ou mais data centers, cada um com energia,
  rede e conectividade redundantes;

### Amazon CloudFront

O armazenamento de cópia de dados em cache mais perto dos clientes em todo o
mundo, usa o conceito de rede de entregas de conteúdo ou CDNs, na AWS tem-se o
Amazon CloudFront.

Ele é um
**serviço que entrega dados, vídeos, aplicações e APIs a clientes em todo o mundo com baixa latência e alta velocidade de transferência**.
Ele utiliza os locais de borda em todo o mundo para acelerar a comunicação com usuários independente de onde estejam.

O CloudFront usa os locais de borda para armazenar cópias em cache do conteúdo
mais próximo dos clientes para uma entrega mais rápida. Além de executar o
CloudFront, esses locais também executam um **serviço de nome de domínio ou DNS**,
conhecido como **Amazon Route 53**, que direciona os clientes para os locais
corretos da web com baixa latência constante.

### AWS Outposts

O Outposts é um serviço utilizado quando uma empresa quer
**utilizar serviços da AWS dentro do próprio prédio**, na qual a AWS instala uma
região reduzida totalmente operacional dentro do datacenter da empresa. Essa
região pertence e é operada pela AWS, usando 100% das funcionalidades, mas
isolada na empresa.

### AWS Elastic Beanstalk

O Beanstalk é um serviço de **provisionamento de ambientes baseados no Amazon EC2**,
em vez de clicar no console ou escrever diversos comandos para criar algo, é
possível informar o código da aplicação e configurações desejadas e o Beanstalk
criará o ambiente para você, com ele, fica fácil salvar essas configurações e
reimplantá-las sem dificuldade.

Aqui você se concentra na aplicação corporativa e não na infraestrutura para
executar tarefas, como ajustar capacidade, balancear carga, _autoscaling_ e
monitorar a saúde da aplicação.

### AWS CloudFormation

O CloudFormation é outro
**serviço para criação de implantações automatizadas e repetíveis**. Ele é uma
ferramenta de infraestrutura como código (IaaS), que possibilita a definição de
diversos recursos da AWS de forma declarativa, por meio de documentos baseados
em JSON ou YML, chamados de modelos do CloudFormation. Com esse modelo, você
especifica o que quer desenvolver, sem precisar explicar como desenvolver,
havendo menos espaço para erros humanos.

### Observações

**Fatores para escolher uma região:**

- Conformidade com governança de dados e requisitos legais;
- Proximidade com os clientes;
- Serviços disponíveis em uma região;
- Preços.

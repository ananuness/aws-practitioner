# Armazenamento e banco de dados

### Amazon Elastic Block Stores (Amazon EBS)

Com o EBS é possível criar discos virtuais, chamados de volumes do EBS, que
**podem ser anexados à instâncias do EC2**. Com ele, é possível fazer os backups
incrementais de dados, os snapshots.

### Amazon Simple Storage Service (AWS S3)

O S3 é um serviço que facilita o armazenamento de arquivos por servir para
armazenamento e recuperação de uma quantidade praticamente ilimitada de dados em
qualquer escala. Estes são armazenados como **objetos**, que por sua vez, são
armazenados em buckets. O tamanho máximo do objeto que pode ser carregado é de 5
terabytes. Você também pode fazer versões de objeto para protegê-los contra
exclusão acidental, ou seja, é sempre possível reter as versões anteriores de um
objeto como um registro físico.

Outra maneira útil de usar o Amazon S3 é para **hospedagem estática de site**,
como é um grupo de arquivos HTML e cada arquivo é semelhante a uma página física
do site real. Você pode simplesmente carregar todo o HTML, os arquivos web
estáticos em um bucket e marcar uma caixa para hospedá-lo como um site estático.
Depois, insira a URL do bucket e estará pronto.

Há também outras classes de armazenamento:

<details>
  <summary><b>S3 Standard</b></summary>
  <p>
    Foi projetado para <b>dados acessados com frequência</b> e armazenar dados 
    em um <b>mínimo de três Zonas de Disponibilidade</b>. Ele fornece alta 
    disponibilidade para objetos. Isso o torna uma boa escolha para diversos
    casos de uso, como sites, distribuição de conteúdo e <i>data analytics</i>. 
    O Amazon S3 Standard tem um <b>custo mais alto</b> do que outras storage 
    classes destinadas aos dados acessados com pouca frequência e armazenamento 
    de arquivamento.
  </p>
</details>

<details>
  <summary><b>S3 Infrequent Acess (S3 Standard-IA)</b></summary>
  <p>
    É ideal para
    <b>
    dados com pouca frequência de acesso, mas que precisam ter alta 
    disponibilidade quando necessário
    </b>. O S3 Standard-IA tem o mesmo nível de disponibilidade do Amazon S3 
    Standard, mas com um <b>preço de armazenamento mais baixo</b> e um 
    <b>preço de recuperação mais alto</b>.
  </p>
</details>

<details>
  <summary><b>S3 One Zone Infrequent Access (S3 One Zone-IA)</b></summary>
  <p>
    Ele armazena dados em <b>uma única Zona de Disponibilidade</b>, tem um preço 
    de armazenamento menor do que o Amazon S3 Standard-IA. Isso o torna uma boa 
    storage class nas seguintes condições: 
    <ul>
      <li>Economizar custos com armazenamento;</li>
      <li>
        Reproduzir facilmente seus dados em caso de falha na Zona de 
        Disponibilidade;
      </li>
    </ul>
  </p>
</details>

<details>
  <summary><b>S3 Intelligent-Tiering</b></summary>
  <p>
    Nesse o S3 <b>monitora os padrões de acesso dos objetos</b>.
    Se você não acessou um objeto por 30 dias consecutivos, o S3 o move
    automaticamente para o nível de acesso pouco frequente S3 Standard–IA. Se 
    você acessar um objeto no nível de acesso pouco frequente, o S3 o move
    automaticamente para o nível de acesso frequente S3 Standard.
  </p>
</details>

<details>
  <summary><b>S3 Outposts</b></summary>
  <p>
    Ele oferece armazenamento de objetos 
    <b>para o ambiente on-premises do AWS Outposts</b>.
  </p>
</details>

<details>
  <summary><b>S3 Glacier Instant Retrieval</b></summary>
  <p>
    Este funciona bem para <b>dados arquivados que requerem acesso imediato</b> 
    e pode recuperar objetos em alguns <b>milissegundos</b>. É a classe de 
    armazenamento de arquivos que oferece o <b>terceiro menor custo</b> de 
    armazenamento para dados de longa duração.
  </p>
</details>

<details>
  <summary><b>S3 Glacier Flexible Retrieval</b></summary>
  <p>
    Oferecendo o <b>segundo menor custo</b> de armazenamento, ele é projetado 
    para <b>arquivamento de dados</b> e é capaz de recuperar objetos em poucos 
    <b>minutos a horas</b>.
  </p>
</details>

<details>
  <summary><b>S3 Glacier Deep Archive</b></summary>
  <p>
    Ele dá suporte a <b>retenção de longo prazo</b> e preservação digital de 
    <b>dados acessados uma ou duas vezes por ano</b>. Essa storage class é
    o armazenamento de <b>menor custo na nuvem AWS</b>. Com recuperação de dados 
    de <b>12 a 48 horas</b>. Todos os objetos dessa storage class são replicados 
    e armazenados em pelo menos <b>três Zonas de Disponibilidade</b> 
    geograficamente dispersas.
  </p>
</details>

> _As classes do S3 Glacier são projetadas para serem as de menor custo do AWS S3._

### Amazon Elastic File System (Amazon EFS)

O EFS é um **sistema de arquivos dimensionável** usado com os AWS Cloud Services
(como instâncias do EC2) e recursos on-premises **para Linux**. À medida que você
adiciona e remove arquivos, o Amazon EFS expande e retrai automaticamente. Ele
pode dimensionar sob demanda para petabytes sem interromper os aplicativos, ou
seja, possui **armazenamento elástico**.

Como o AWS EFS não pode ser utilizado com o Windows, a AWS criou o **AWS FSx**
que é uma unidade de compartilhamento de sistema de arquivos do **Windows**
totalmente gerenciada que oferece suporte ao protocolo de bloco de mensagens do
servidor e ao sistema de arquivos da tecnologia de rede do Windows;

Comparação entre o Amazon EBS e o Amazon EFS:

|               | Amazon EBS                  | Amazon EFS                                            |
| ------------- | --------------------------- | ----------------------------------------------------- |
| Armazenamento | Uma Zona de Disponibilidade | Várias Zonas de Disponibilidade e entre elas          |
| Acesso        | Na mesma ZD apenas          | Qualquer ZD simultaneamente e usando o Direct Connect |

### AWS Storage Gateway

O Storage Gateway é um serviço que nos permite
**conectar o armazenamento de data center on-premises da AWS a um serviço de**
**armazenamento da AWS** e ajuda a migrar parte ou toda sua plataforma de
armazenamento para a AWS ou oferece suporte à extensão da plataforma para a AWS.

### Amazon Relational Database Service (Amazon RDS)

O RDS é um serviço que permite executar **bancos de dados relacionais** na nuvem
AWS. Esse serviço tem benefícios como aplicativo de patches automatizado,
backups, alta disponibiliade, _failover_ e recuperação de desastres automatizados.

É possível usar os produtos de banco de dados que já conhece com: Db2, MariaDB,
Microsoft SQL Server, MySQL, Oracle e PostgreSQL.

Além disso, tem-se o **Amazon Aurora** que permite trabalhar
**até cinco vezes mais rápido do que os bancos de dados MySQL comuns** e
**até três vezes mais rápido do que os bancos de dados PostgreSQL comuns**.
Também oferece até 6 cópias dos dados em zonas de disponibilidade diferentes, e
é possível adicionar até 15 réplicas de leitura para escalar a performance, além
de ter **backups contínuos para o S3**.

### Amazon DynamoDB

O DynamoDB é um **banco de dados NoSQL e serveless**, ou seja, você não precisa
gerenciar as instâncias que são utilizadas pelo serviço e nem criar a estrutura.
Os dados são armazenados em formato de **chave-valor** e armazena documentos do
tipo JSON. Além de não precisar se preocupar em escalar o armazenamento
manualmente, ele é feito de forma redundante em zonas diferentes e a replicação
dos dados ocorre de forma automática, além de oferecer **alto desempenho** com
respostas de milissegundos.

### Amazon Redshift

O Redshift é um **serviço de data warehouse** que você pode usar para análise de
**Big Data**. Ele oferece a capacidade de coletar dados de muitas fontes além de
ajudar a entender relações e tendências em todos os seus dados. Além disso, ele
é capaz de desempenhar 10 vezes mais que bancos de dados comuns quando se trata
desses tipos de carga de trabalho voltados à inteligência do negócio;

Quando é necessária uma solução para extrair insights usando quantidades massivas
de dados para ajudar na tomada de decisão, ou seja, lidar com inteligência de
negócio, você pode contar com o Redshift;

### Outros serviços

- **Amazon Kinesis** processa e analisa _dados de streaming_ em tempo real;
- **AWS Glue** é um serviço de integração de _dados servless_ para descobrir,
  preparar, mover e integrar dados;
- **Amazon QuickSight** é um serviço de _business intelligence_;
- **Amazon EMR** é um serviço que ajuda a executar frameworks de _Big data_ para
  processar vastas quantidades de dados;
- **Amazon DocumentDB** _compatível com o MongoDB_;
- **Amazon Neptune**, _banco de grafos_, projetado para redes sociais, mecanismos
  de recomendação e detecção de fraude;
- **Amazon Quantum Ledger Database (Amazon QLDB)**, contando com
  _sistema imutável de registro_;
- **Amazon Managed Blockchain** para _criar e gerenciar redes de blockchain_ com
  frameworks de código aberto ou quando se tem registros bancários ou financeiros
  que exigem 100% de imutabilidade;

Tem-se ainda os **aceleradores de bancos de dados**, como:

- **DynamoDB Accelerator (DAX)** como opção para utilizar na
  _camada de cache em conjunto com DynamoDB_;
- **Amazon ElastiCache**, que adiciona uma camada de cache para melhorar o tempo
  de leituras e retorno de dados, _compatível com Memcached e Redis_;

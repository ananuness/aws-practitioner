# Migração

## Migração

### AWS Cloud Adoption Framework (CAF)

O AWS CAF existe para **orientar a empresa** e para que a migração para a AWS
seja rápida e tranquila. O framework orienta sobre seis áreas com foco nas
diferentes pessoas que precisam ser envolvidas durante a migração. Cada
perspectiva abrange responsabilidades distintas:

<details>
  <summary><b>Perspectiva de negócio</b></summary>
  <p>
    Use para criar um <b>caso de negócio sólido</b> para adoção da nuvem e 
    <b>priorizar as iniciativas de adoção da nuvem</b>. Garanta que suas 
    estratégias e metas de negócios estejam alinhadas com suas estratégias e
    metas de TI. Os perfis comuns na perspectiva de negócio são:
  </p>
  <ul>
    <li>Gerentes de negócios;</li>
    <li>Gerentes financeiros;</li>
    <li>Proprietários de orçamento;</li>
    <li>Stakeholders de estratégia;</li>
  </ul>
</details>

<details>
  <summary><b>Perspectiva de pessoas</b></summary>
  <p>
    Use para <b>avaliar estruturas</b> e <b>perfis organizacionais</b>, 
    <b>novos requisitos de habilidades</b>, <b>processos</b> e identificar 
    lacunas. Isso ajuda a <b>priorizar treinamento</b>, pessoal e 
    <b>mudanças organizacionais</b>. Os perfis comuns da perspectiva de pessoas 
    são:
  </p>
  <ul>
    <li>RH;</li>
    <li>Equipe e Gerentes de pessoas;</li>
  </ul>
</details>

<details>
  <summary><b>Perspectiva de governança</b></summary>
  <p>
    Esta se concentra nas
    <b>habilidades e processos para alinhar a estratégia de TI à estratégia de negócios</b>.
    Isso garante que você maximize o valor comercial e minimize os riscos. Os
    perfis comuns na perspectiva de governança são:
  </p>
  <ul>
    <li>Chief Information Officer (CIO);</li>
    <li>Gerentes do programa;</li>
    <li>Enterprise architect;</li>
    <li>Analistas de negócios;</li>
    <li>Gerentes de portfólio;</li>
  </ul>
</details>

<details>
  <summary><b>Perspectiva de plataforma</b></summary>
  <p>
    Esta inclui <b>princípios e padrões para implementação</b> de novas soluções 
    na nuvem e <b>migração de cargas de trabalho on-premises para a nuvem</b>. 
    Os perfis comuns da perspectiva de plataforma são:
  </p>
  <ul>
    <li>Chief Technology Officer (CTO);</li>
    <li>Gerentes de TI;</li>
    <li>Arquitetos de soluções;</li>
  </ul>
</details>

<details>
  <summary><b>Perspectiva de segurança</b></summary>
  <p>
    Esta garante que a organização
    <b>
    atenda aos objetivos de segurança de visibilidade, auditoria, controle e 
    agilidade
    </b>. Os perfis comuns da perspectiva de segurança são:
  </p>
  <ul>
    <li>Chief information security officer (CISO);</li>
    <li>Gerentes de segurança de TI;</li>
    <li>Analistas de segurança de TI;</li>
  </ul>
</details>

<details>
  <summary><b>Perspectiva de operações</b></summary>
  <p>
    Esta ajuda você a
    <b>ativar, executar, usar, operar e recuperar cargas de trabalho de TI</b> 
    para o nível definido com os stakeholders da empresa. Os perfis comuns da 
    perspectiva de operações são:
  </p>
  <ul>
    <li>Gerentes de operações de TI;</li>
    <li>Gerentes de suporte de TI;</li>
  </ul>
</details>

Essas informações são usadas como base para a criação do plano de ação dentro do
AWS Cloud Adoption Framework que é usado para orientar o gerenciamento de mudança
da organização durante a jornada para a nuvem.

> _Em geral, as perspectivas de negócio, pessoas e governança se concentram nos_ > _recursos comerciais, enquanto as perspectivas de plataforma, segurança e_ > _operações se concentram em capacidades técnicas._

### As Sete Estratégias de Migração (Os sete Rs)

- **Retirar** é para aplicações a serem **desativadas** ou **retiradas**;

- **Realocar** é para um **grande número de servidores** que são compostos de
  **uma ou mais aplicações**;

- **Reter** é para aplicações que você quer **manter no ambiente de origem** ou
  aplicações que **não estão prontas para migrar**;

- **Redefinir hospedagem** (também conhecido como _“lift and shift”_) serve para
  **migrar aplicações sem fazer alterações nelas**;

- **Refatoração** (também conhecida como _rearquitetura_) é para aplicações que
  você quer **migrar para a AWS e aproveitar ao máximo os recursos** nativos da
  nuvem para **melhorar a agilidade, o desempenho e o dimensionamento**;

- **Redefinir plataforma** (também conhecido como _“lift, tinker and shift”_) é
  para aplicações que **precisam de algum nível de otimização** para operar com
  eficiência ou aproveitar as vantagens dos recursos da AWS. A otimização é
  alcançada **sem alterar a arquitetura central** do aplicativo;

- **Recomprar** (também conhecido por _“drop and shop”_) é para aplicações com
  uma versão ou produto diferente e oferece mais valor do que a infraestrutura
  existente, ou seja, envolve
  **a substituição de uma aplicação por uma versão baseada na nuvem**, como
  software encontrado no AWS Marketplace. Por exemplo, uma empresa pode optar por
  implementar a estratégia de recomprar migrando de um sistema de gerenciamento
  de relacionamento com o cliente (CRM) para o salesforce.com;

### AWS Snow Family

A Snow Family é uma coleção de **dispositivos físicos para transporte físico**
de **até exabytes de dados** para dentro e para fora da AWS. Eles são projetados
para serem seguros e invioláveis enquanto no local ou em trânsito. Os
dispositivos consistem em:

<details>
  <summary><b>AWS Snowcone</b></summary>
  <p>
    É um dispositivo <b>pequeno, robusto e seguro</b> para transferência de 
    dados e computação de borda. Ele tem 2 CPUs, 4 GB de memória e
    <b>até 14 TB de armazenamento</b> utilizável.
  </p>
</details>

<details>
  <summary><b>AWS Snowball</b></summary>
  <p>Oferece dois tipos de dispositivos:</p>
  <ul>
    <li>
      <b>Snowball Edge Storage Optimized</b> são ideais para
      <b>migrações de dados de grande escala</b> e fluxos de trabalho de 
      transferência recorrentes, em além da computação local com 
      <b>necessidades maiores de capacidade</b>.
      <ul>
        <li>
          <b>Armazenamento: 80 TB de disco rígido</b> (HDD) para volumes de 
          blocos e armazenamento de objeto <b>compatível com o Amazon S3</b>, 
          além de unidade de estado sólido (SSD) do SATA de 
          <b>1 TB para volumes de blocos</b>;
        </li>
        <li>
          <b>Computação: 40 vCPUs e 80 GiB de memória</b> para dar suporte a    
          instâncias sbe1 do Amazon EC2 (equivalente a C5);
        </li>
      </ul>
    </li>
    <br>
    <li>
      <b>Snowball Edge Compute Optimized</b> são ideais para casos de uso que
      precisam de <b>recursos de computação poderosos</b>, como machine learning,
      análise de vídeo em movimento completo, análise e pilhas de computação 
      locais.
      <ul>
        <li>
          <b>Armazenamento:</b> capacidade de <b>HDD utilizável de 80 TB</b> 
          para armazenamento de objeto <b>compatível com o Amazon S3</b> ou 
          volumes de blocos <b>compatíveis com o Amazon EBS</b> e também
          <b>28 TB de SSD NVMe</b> utilizável para volumes de blocos compatíveis 
          com o Amazon EBS;
        </li>
        <li>
          <b>Computação: 104 vCPUs, 416 GiB de memória</b> e uma
          <b>GPU NVIDIA Tesla V100 opcional</b>. Os dispositivos executam as 
          instâncias sbe-c e sbe-g do Amazon EC2, que são equivalentes às 
          instâncias C5, M5a, G3 e P3;
        </li>
      </ul>
    </li>
  </ul>
</details>

<details>
  <summary><b>AWS Snowmobile</b></summary>
  <p>
    É um serviço de <b>transferência dados na escala de exabytes</b> usado para 
    mover grandes quantidades de dados para a nuvem AWS. Você pode transferir 
    <b>até 100 petabytes de dados por Snowmobile</b>, um contêiner de transporte 
    reforçado com 13,71 metros de comprimento puxado por um caminhão semirreboque.
  </p>
</details>

### AWS Database Migration Service (DMS)

O DMS é um serviço gerenciado de **migração de dados e conversão de schema**. O
bacana é que o banco de dados de origem permanece totalmente
**operacional durante a migração**, o que reduz o tempo de inatividade das
aplicações que dependem desses dados e os
**bancos de origem e destino, não precisam ser do mesmo tipo**.

Quando queremos migrar um banco de dados para um mesmo tipo na nuvem, chamamos
isso de **migrações homogêneas**. E podem ser como do MySQL para o Amazon RDS My
SQL, do Oracle para o RDS Oracle e assim por diante.

Quando o banco de origem é diferente do de destino, chamamos de
**migração heterogêneas**. Este é um processo de duas etapas. Como a estrutura
de schema, tipo de dados e código do banco de dados são diferentes, ele precisa
passar por uma conversão primeiro, através do **AWS Schema Conversion Tool**,
ele **converte a estrutura e o código do banco** para corresponder ao do destino.
A próxima etapa é usar o DMS para migrar os dados.

O DMS também inclui migrações de banco de dados de desenvolvimento e teste,
consolidação de bancos de dados e até **replicação contínua** de banco de dados.
Ela pode servir para recuperação de desastres, por exemplo.

### AWS DataSync

Outro serviço de migração de banco de dados é o AWS DataSync, ele
**facilita e agiliza a movimentação de grande quantidade de dados** online entre
o armazenamento on-premises e o Amazon S3, Amazon EFS ou Amazon FSx para Windows
File Server.

Tarefas manuais relacionadas à transferência de dados pode retardar as migrações
e sobrecarregar as operações de TI. O DataSync lida automaticamente com muitas
dessas tarefas, incluindo:

- Scripts de tarefas de cópia;
- Agendamento e monitoramento de transferências;
- Validação de dados e otimização da utilização da rede;
- Transferência de centenas de terabytes e milhões de arquivos em velocidades
  até 10x maiores do que ferramentas _open source_ ou por links do AWS Direct
  Connect;

### Outros serviços para migrações

- O **AWS Application Migration Service (MGN)** é uma solução _“lift-and-shift”_
  automatizada. Essa solução
  **pode migrar servidores físicos e quaisquer bancos de dados** ou aplicativos
  executados neles **para instâncias do EC2 na AWS**;

- O **AWS Migration Hub** é um serviço que ajuda a
  **planejar e rastrear migrações de aplicativos**;

- O **AWS Application Discovery Service** **coleta informações sobre o uso** e a
  **configuração de servidores on-premises** para ajudar a planejar uma migração
  para a AWS;

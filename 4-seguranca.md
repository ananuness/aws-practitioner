# Segurança

**Responsabilidade da AWS:**

- Software: computação, armazenamento, banco de dados, rede;
- Hardware: Regiões, Zonas de Disponibilidade, locais de borda;

**Responsabilidade do cliente:**

- Seus dados
- Plataforma, aplicações, Identity and Access Management (IAM)
- Configuração de sistemas operacionais, rede e firewall
- Criptografia de dados no lado do cliente, criptografia de dados no lado do
  servidor e proteção de tráfego de rede;

Em resumo, a **AWS cuida da segurança da nuvem e você cuida da segurança na nuvem**,
da forma como você utiliza os recursos mantidos pela AWS.

### AWS Identity and Access Management (AWS IAM)

O IAM permite que você **gerencie o acesso aos serviços** e recursos da AWS com
segurança. E todas as ações são negadas por padrão, para mudar isso, é
necessário permitir acesso, mas apenas ao que precisam. Para facilitar o
gerenciamento de usuários e permissões, podemos organizá-los em um grupo do IAM.

Um perfil ou role do IAM é uma identidade que você pode assumir para obter acesso
temporário a permissões.

### AWS Organizations

O AWS Organizations serve para **consolidar e gerenciar múltiplas contas AWS**
em um local central. Você pode controlar de maneira centralizada as permissões
para as contas em sua organização usando as políticas de controle de serviço
(SCPs). As SCPs permitem que você coloque restrições nos serviços AWS, recursos
e ações individuais de API que os usuários e funções em cada conta podem acessar.

Uma SCP afeta todos os usuários, grupos e perfis do IAM em uma conta, incluindo
o usuário-raiz da conta AWS. Além de permitirem que você controle de maneira
centralizada as permissões para as contas em sua organização.

### AWS Artifact

O Artifact é um serviço que concede
**acesso sob demanda a relatórios de segurança e conformidade da AWS** e a
**contratos on-line selecionados**. Ele consiste em duas seções principais: AWS
Artifact Agreements e o AWS Artifact Reports.

No **AWS Artifact Agreements**, você pode ver, **aceitar e gerenciar contratos**
para uma conta individual e para todas as suas contas no AWS Organizations. Já o
**AWS Artifact Reports** oferece **relatórios de conformidade** por auditores
terceirizados.

### AWS Shield

O AWS Shield é um serviço que
**protege aplicações contra ataques distribuído de negação de serviço (DDoS)**,
na qual várias origens são usadas para iniciar um ataque que visa tornar um site
ou aplicação indisponível. O AWS Shield oferece dois níveis de proteção: Standard
e Advanced;

O **AWS Shield Standard protege automaticamente todos os clientes AWS** sem
nenhum custo. Ele protege seus recursos AWS contra os
**tipos de ataques DDoS mais comuns e frequentes**.

Já o **AWS Shield Advanced** é um serviço pago que fornece **diagnósticos**
detalhados de ataques e a capacidade de detectar e mitigar
**ataques elaborados de DDoS**. Ele também se integra a outros serviços, como o
Amazon CloudFront, o Amazon Route 53 e o Elastic Load Balancing. Além disso, você
pode integrar o AWS Shield ao AWS WAF escrevendo regras personalizadas para
mitigar **ataques complexos de DDoS**.

### AWS WAF

Este serviço ajuda a controlar o tráfego com regras definidas por você que
**bloqueiam padrões de ataque comuns**, como injeções SQL ou vulnerabilidade XSS.

### Amazon GuardDuty

O GuardDuty é um serviço de **detecção de ameaças** que **monitora continuamente**
suas contas e _workloads_ da AWS para detectar atividades mal-intencionadas e
entrega descobertas de segurança detalhadas, permitindo visibilidade e correção.
Analisa fluxos contínuos de metadados gerados pela sua conta e atividade de rede
encontrada em eventos do AWS CloudTrail, logs de fluxo da Amazon VPC e logs de
DNS.

O serviço detecta anomalias envolvendo as chaves de acesso do AWS Identity and
Access Management (IAM) e o Amazon Elastic Compute Cloud (Amazon EC2), além de
**utilizar machine learning para identificar ameaças com maior precisão**.

Você também pode ativar os planos de proteção do GuardDuty para analisar dados
adicionais de outros serviços da AWS em seu ambiente da AWS para proteger
_workloads_ usando Amazon S3, Amazon EKS, Amazon RDS e AWS Lambda.

### Outros serviços

- O **AWS Key Management Service (AWS KMS)** permite que você execute operações
  de criptografia usando chaves de criptografia;
- O **AWS Secrets Manager** ajuda você a proteger os segredos necessários para
  acessar aplicativos, serviços e recursos de TI;
- O **Amazon Inspector** melhora a segurança e a conformidade das aplicações na
  AWS, por meio de avaliações de segurança automatizadas e contínuas da sua
  infraestrutura. Ele verifica:
  - desvios de boas práticas de segurança;
  - exposição de instâncias EC2;
  - vulnerabilidades, entre outros;

### Soluções para alguns ataques

- Para **ataques de inundação UDP** (falsificação de um endereço IP de origem,
  gerar pacotes UDP e deixar os recursos indisponíveis), a solução são os
  **grupos de segurança**;
- Para **ataques Slowloris** (fingimento de conexão extremamente lenta), a
  solução é o **Elastic Load balacing**, pois o ELB lida com a solicitação de
  tráfego HTTP antes que chegue às instâncias. E como o ELB é dimensionável,
  seria necessário sobrecarregar uma região inteira da AWS para prejudicá-lo;
- Para **ataques mais sofisticados**, tem-se o **AWS Shield** e o **AWS WAF**,
  este, usa um firewall de aplicação web para filtrar assinaturas de agentes mal
  intencionados no tráfego de entrada. Ele tem ampla capacidade de machine
  learning e pode reconhecer novas ameaças à medida que elas evoluem e podem
  ajudar a defender o sistema de forma próativa contra uma lista cada vez maior
  de vetores destrutivos;

### Extra

- O acesso programático requer uma **ID de chave de acesso** e uma
  **chave de acesso secreta** que pode ser atribuída a um usuário da AWS;
- Uma **chave primária e secundária** é um recurso usado no gerenciamento de
  banco de dados. Ele não concede acesso à conta da AWS;
- Você deve garantir que os dados das suas aplicações estejam protegidos durante
  o armazenamento (criptografia em repouso) e durante a transmissão (criptografia
  em trânsito);

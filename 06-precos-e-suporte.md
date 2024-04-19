# Preços e suporte

### Cobrança consolidada do AWS Organizations

Este recurso permite que você receba uma
**única fatura para todas as contas AWS na sua organização**. Ao consolidar,
você pode rastrear facilmente os custos combinados de todas as contas vinculadas
em sua organização. O número máximo de contas-padrão permitido para uma
organização é quatro, mas você pode entrar em contato com o AWS Support para
aumentar sua cota, se necessário.

### AWS Budgets

No Budgets, você pode
**criar orçamentos para planejar o uso do serviço, os custos de serviço e as reservas de instâncias**.
As informações do AWS Budgets são atualizadas três vezes por dia. Isso ajuda você
a definir com precisão a proximidade entre seu uso e os valores orçados ou
limites de nível gratuito da AWS. Você também pode definir alertas personalizados
para quando seu uso exceder (ou estiver prestes a exceder) o valor orçado.

### AWS Cost Explorer

O Cost Explorer é uma ferramenta que permite
**visualizar, interpretar e gerenciar seus custos e uso da AWS ao longo do tempo**.
Ele inclui um relatório-padrão dos custos e do uso dos cinco principais serviços
da AWS de acúmulo de custos.

### AWS Marketplace

O Marketplace é um **catálogo digital** com milhares de ofertas de software de
provedores independentes de software. Você pode usar o AWS Marketplace para
encontrar, testar e comprar software que pode ser executado na AWS.

### AWS Support Plans

A AWS oferece quatro planos de suporte diferentes para ajudar você a solucionar problemas, reduzir custos e usar os serviços da AWS de maneira eficiente, como:

- **Basic:** é gratuito e oferece suporte para dúvidas sobre contas, faturamento
  e aumentos de cotas de serviços. Todos os AWS clientes têm acesso automático 24 horas por dia, 7 dias por semana, a esses recursos do _Basic Support_:

  - Respostas às perguntas sobre contas e faturamento;
  - Fóruns de suporte;
  - Verificações de integridade de serviços;
  - Documentação, _whitepapers_ e guias sobre práticas recomendadas;

- **Developer:** clientes deste plano têm acesso aos adicionais:

  - Orientação sobre as melhores práticas;
  - Ferramentas de diagnóstico do lado do cliente;
  - Suporte de arquitetura básica: orientação sobre como usar AWS produtos,
    recursos e serviços juntos;
  - Oferece suporte a um número ilimitado de casos de suporte que podem ser
    abertos por qualquer usuário com permissões;

Além disso, os clientes com um plano de suporte **Business**,
**Enterprise On-Ramp** ou **Enterprise** têm acesso à:

- **Orientação de caso de uso:** quais AWS produtos, recursos e serviços usar
  para melhor atender às suas necessidades específicas;
- **AWS Trusted Advisor:** Um recurso do AWS Support, que inspeciona os ambientes
  dos clientes e identifica oportunidades de economizar dinheiro, fechar lacunas de
  segurança e melhorar a confiabilidade e o desempenho do sistema. Você pode
  acessar todos os checks do Trusted Advisor;
- **AWS Support API para interagir com o Support Center e o Trusted Advisor:** é
  possível usar a API do AWS Support para automatizar o gerenciamento do caso de
  suporte e as operações do Trusted Advisor;
- **Suporte a um número ilimitado de usuários AWS Identity and Access Management (IAM)**
  que podem abrir casos de suporte técnico;
- **Suporte a software de terceiros:** ajuda com os sistemas operacionais e a
  configuração de instâncias do Amazon Elastic Compute Cloud (Amazon EC2). Além
  disso, ajuda com o desempenho dos componentes de software de terceiros mais populares da AWS;

Por fim, os clientes com um plano de suporte **Enterprise On-Ramp** ou
**Enterprise** têm acesso à:

- **Orientação sobre arquitetura de aplicação:** orientações consultivas sobre
  como os serviços operam em conjunto para atender a casos de uso, workloads ou
  aplicações específicos;
- **Gerenciamento de eventos de infraestrutura:** engajamento de curto prazo com
  o AWS Support para obter uma compreensão profunda do caso de uso. Após a análise,
  forneça orientações sobre arquitetura e escalabilidade para um evento;
- **Gerente de conta técnico:** trabalhe com um gerente de conta técnico (TAM)
  para seus casos de uso e aplicações específicas. Responsável por educar, capacitar e desenvolver sua jornada para a nuvem;
- **Roteamento de casos "white-glove"**;
- **Análises empresariais de gerenciamento**;

### Modelo de preços

<details>
  <summary><b>Instâncias sob demanda</b></summary>
  <p>
    Você usa quando necessário. São ótimas para quando os 
    <b>recursos são incertos</b>, <b>início e fim flexíveis</b>, cargas de 
    trabalho de <b>curto prazo</b> e aplicações que 
    <b>não toleram interrupções</b>.
  </p>
</details>

<details>
  <summary><b>Savings Plans</b></summary>
  <p>
    Savings Plans da instância do EC2 reduzem os custos de computação,
    <b>comprometendo-se</b> com um gasto consistente por hora
    <b>por um período de 1 ou 3 anos</b>. Isso resulta em 
    <b>economia de até 72% em relação aos custos de instâncias sob demanda.</b>
    Qualquer uso do EC2 até o compromisso é cobrado de acordo com o preço de 
    Savings Plans com desconto. E qualquer uso do EC2 além do compromisso é 
    cobrado de acordo com os preços normais de instâncias sob demanda.
  </p>
</details>

<details>
  <summary><b>Instâncias reservadas</b></summary>
  <p>
    Elas são um desconto aplicado ao uso de instâncias sob demanda na conta AWS. 
    Além disso, você paga mesmo que as instâncias não estejam em execução. Elas 
    são ótimas <b>para aplicações com uso estável, de longo prazo</b>. Geralmente 
    <b>a AWS recomenda as Saving plans por serem mais em conta</b>.
  </p>
</details>

<details>
  <summary><b>Instâncias Spot</b></summary>
  <p>
    Elas são ideais para cargas de trabalho com horários de início
    e término flexíveis ou que <b>podem suportar interrupções</b>. As instâncias 
    spot aproveitam a capacidade de computação do EC2 não utilizada e oferecem
    <b>
      economia de custos de até 90%** sobre os preços das instâncias sob demanda
    </b>.
  </p>
</details>

<details>
  <summary><b>Hosts dedicados</b></summary>
  <p>
    Eles são <b>servidores físicos reservados</b> apenas para o cliente e é pago 
    para que esse host continue dedicado e não seja compartilhado com outros 
    clintes da AWS, ou seja, você <b>paga pelo host e não pelas instâncias</b>
    individuais em execução no host, tornando-se o <b>mais caro</b>. Além disso, 
    uma empresa pode usar as licenças já adquiridas de software por soquete, por
    núcleo ou por VM para manter a conformidade da licença.
  </p>
</details>

<details>
  <summary><b>Instâncias dedicadas</b></summary>
  <p>
    Elas são instâncias do Amazon EC2 que são executadas em uma VPC em 
    <b>hardware dedicado a um único cliente</b>. Suas instâncias dedicadas são 
    <b>isoladas fisicamente no nível de hardware de hospedagem de instâncias</b>
    que pertencem a outras contas da AWS.
  </p>
</details>

### Extra

- **Sempre gratuito:** por exemplo, AWS Lambda permite 1 milhão de solicitações
  gratuitas e até 3,2 milhões de segundos de tempo de computação por mês, o
  Amazon DynamoDB libera 25 GB de armazenamento gratuito por mês;

- **12 meses gratuitos:** Quantidades específicas de armazenamento do Amazon S3
  Standard, limites para horas mensais de tempo de computação do Amazon EC2 e
  quantidades de transferência de dados do Amazon CloudFront para fora são
  alguns exemplos;

- **Versão de teste:** por exemplo, o Amazon Inspector oferece uma versão
  gratuita de 90 dias, o Amazon Lightsail (um serviço que permite que você
  execute servidores virtuais privados) oferece 750 horas de uso gratuitas em um
  período de 30 dias;

- **Definições de preço:** pague pelo que usar, pague menos ao fazer reserva e
  pague menos com descontos baseados em volume, quando usar mais;

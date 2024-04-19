# Monitoramento e análise

### Amazon CloudWatch

O CloudWatch é um serviço da web que permite
**monitorar e gerenciar várias métricas e configurar ações de alarme** de acordo
com os dados dessas métricas. Estas, são usadas para representar os pontos de
dados para seus recursos.

Os serviços AWS enviam as métricas ao CloudWatch, em seguida, ele usa essas
métricas para criar automaticamente **gráficos** que mostram como o desempenho
mudou ao longo do tempo. Com o CloudWatch, você pode criar **alarmes** que vão
executar ações automaticamente se o valor da métrica ultrapassar ou for inferior
a um limite predefinido.

Além disso, você pode usar o CloudWatch com o _AWS CloudTrail_ para monitorar e
receber alertas sobre eventos de login do console que envolvem o usuário-raiz da
conta da AWS.

### AWS CloudTrail

O CloudTrail **registra as chamadas de API realizadas na sua conta,**
**rastreia atividades de usuário** e **filtra logs** para auxiliar na análise
operacional e na solução de problemas.

### AWS Trusted Advisor

O Trust Advisor é um serviço da web que **inspeciona seu ambiente AWS** e faz
**recomendações** em tempo real de acordo com as **práticas recomendadas da AWS**
e em cinco categorias:

<details>
  <summary><b>Desempenho</b></summary>
  <p>
    Recomendações para aproveitar o <i>throughput</i> provisionado e melhorar o 
    desempenho dos serviços, como incluir verificações para alta utilização de 
    instâncias do EC2.
  </p>
</details>

<details>
  <summary><b>Segurança</b></summary>
  <p>
    Verificações que revisam as permissões e identificam quais recursos de 
    segurança da AWS devem ser ativados.
  </p>
</details>

<details>
  <summary><b>Otimização de Custos</b></summary>
  <p>
    Verificações de recursos não utilizados ou ociosos que podem ser eliminados 
    e proporcionar economia de custos.
  </p>
</details>

<details>
  <summary><b>Tolerância à falhas</b></summary>
  <p>
    Verificações para ajudar a melhorar a disponibilidade e a redundância das 
    aplicações.
  </p>
</details>

<details>
  <summary><b>Limites de serviços</b></summary>
  <p>
    Verificações do uso da conta e recebimento de notificações quando ela se 
    aproximar ou exceder os limites de serviços.
  </p>
</details>

O Trust também verifica em grupos de segurança
**regras que permitam acesso irrestrito a um recurso**. O acesso irrestrito
aumenta as oportunidades para atividades maliciosas, como _hacking_,
_ataques de negação de serviço_, _perda de dados_ etc.

### AWS Config

O AWS Config serve para
**avaliar, auditar e verificar as configurações dos recursos da AWS**.

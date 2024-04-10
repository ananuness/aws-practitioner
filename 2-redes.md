# Redes

### Amazon Virtual Private Cloud (Amazon VPC)

A VPC permite com que você crie sua própria rede virtual dentro da nuvem AWS,
isolando seus recursos dos demais na nuvem, podendos ser públicos ou não, e para
isso, criamos as subredes, um subconjunto de IPs na VPC.

Uma VPC pode ter diferentes tipos de gateways anexados para se conectar com
diversos recursos na mesma VPC, porém, em subredes diferentes. Para permitir que
o tráfego público da internet acesse sua VPC, é preciso anexá-la a um gateway de
internet. Já para acessar recursos privados em uma VPC, é necessário utilizar um gateway privado virtual, a VPN.

A VPN é uma conexão criptografada para que uma rede específica consiga chegar
aos recursos privados de uma VPC. Para estabelecer essa conexão, anexa-se o
Gateway privado virtual à VPC.

Alguns conceitos importantes:

- **Lista de Controle de Acesso (ACL) de rede:** é um firewall virtual que
  controla o tráfego de entrada e saída no nível de sub-rede, é stateless e por
  padrão permite todo tráfego de entrada e saída. Uma ACL só consegue avaliar um pacote quando entra ou sai de uma subrede, ou seja, não consegue definir quais pacotes são permitidos ou bloqueados em uma determinada instância do EC2 dentro
  da subrede, por exemplo;
- **Grupos de segurança:** servem para proteger à nível de instância;

> _A principal diferença entre uma ACL e um grupo de segurança é que o grupo é_
> _stateful, ou seja, lembra-se das decisões tomadas para pacotes recebidos e a_
> _ACL verifica sempre quem entra e sai (stateless)._

- A tradução de endereços de rede conhecida como **NAT**, é o processo de
  conceder acesso de saída de um recurso privado à internet. Um exemplo é o
  Internet Gateway;
- O **Internet Gateway (IG)** executa um tipo de NAT denominado NAT estático,
  ele aloca um recurso com um IPv4 público, de modo que quando os dados ou
  pacotes saem desse recurso e passam pelo IG, ele muda o IP de origem do IP
  privado para o IP público e envia o pacote. Quando este volta, ele muda o
  endereço de destino do IP público de volta para o IP privado. Assim o NAT
  fornece acesso privado à internet de saída;

### AWS Direct Connect

O Direct Connect é um serviço que permite estabelecer uma conexão privada
dedicada entre seu data center e uma VPC, para garantir confiabilidade e baixa
latência nessas conexões privadas.

### AWS Site-to-Site VPN

Este serviço cria um caminho de rede criptografado entre sua rede on-premises e
sua rede na nuvem AWS. Essa conexão entre sua rede on-premises e sua rede na
nuvem AWS usa a internet.

### AWS Route 53

O Route 53 é um serviço altamente disponível e dimensionável de nome de domínio
(DNS), que faz a conversão do nome para endereços IPs que os computadores usam
para se comunicar. Indo além, o 53 pode direcionar o tráfego para diferentes
endpoints, por meio de políticas de roteamento diferentes como o baseado em
latência, DNS de geolocalização, geoproximidade e por pesos. Além disso, você
pode usar o Route para registrar, comprar e gerenciar seus DNS.

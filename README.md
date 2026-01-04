# Basic Network Lab – Cisco Packet Tracer

> **Note:** This README is available in **English and Portuguese**.  
> **Aviso:** Este README está disponível em **inglês e português**.

---

## 🇺🇸 English Description

I built this lab to move beyond theory and understand, in practice, how data flows inside a local network. The main goal was to learn how IP addressing works, the role of the default gateway, and how devices discover and communicate with each other within the same network.

## Topology
The structure is simple but functional, simulating a basic corporate network:

- 1 PC (end host)
- 1 Server (simulating a network resource)
- 1 Switch (Layer 2 connectivity)
- 1 Router (default gateway and network exit point)

## Configuration
I intentionally used static IP addresses to better understand subnet behavior and the importance of the gateway. DHCP was not used in this lab on purpose.

**IP Addressing:**

- Router  
  IP: 192.168.1.1  
  Subnet Mask: 255.255.255.0  

- PC  
  IP: 192.168.1.10  
  Subnet Mask: 255.255.255.0  
  Default Gateway: 192.168.1.1  

- Server  
  IP: 192.168.1.20  
  Subnet Mask: 255.255.255.0  
  Default Gateway: 192.168.1.1  

## Connectivity Tests
To validate the network, I performed connectivity tests using the `ping` command:

- PC → Router (gateway responding correctly)
- PC → Server (internal communication working)
- Server → Router (server outbound connectivity verified)

All tests were successful, confirming proper traffic flow across the network.

## Key Learnings
This lab provided insights beyond basic IP configuration:

- The gateway is not optional: without a configured gateway, hosts can communicate locally but cannot reach external networks.
- Basic troubleshooting: when a ping fails, the issue may lie in logical configuration (IP, subnet mask, gateway) or at the physical/logical connection level.
- SOC foundation: observing ICMP traffic in practice builds the foundation for future packet analysis and log investigation using tools like Wireshark.

---

## 🇧🇷 Descrição em Português

Montei este laboratório com o objetivo de sair da teoria e observar, na prática, como os dados trafegam dentro de uma rede local. O foco foi compreender o endereçamento IP, o papel do gateway padrão e como os dispositivos se comunicam entre si dentro da mesma rede.

## Topologia
A estrutura é simples, porém funcional, simulando uma rede corporativa básica:

- 1 PC (host final)
- 1 Server (simulando um recurso de rede)
- 1 Switch (conectividade na Camada 2)
- 1 Router (gateway padrão e saída da rede)

## Configuração
Optei por utilizar endereços IP estáticos para reforçar o entendimento de como a sub-rede se comporta e como o gateway é essencial para a comunicação. Neste laboratório, não utilizei DHCP propositalmente.

**Endereçamento:**

- Router  
  IP: 192.168.1.1  
  Máscara: 255.255.255.0  

- PC  
  IP: 192.168.1.10  
  Máscara: 255.255.255.0  
  Gateway: 192.168.1.1  

- Server  
  IP: 192.168.1.20  
  Máscara: 255.255.255.0  
  Gateway: 192.168.1.1  

## Testes de Conectividade
Para validar o funcionamento da rede, realizei testes de conectividade utilizando o comando `ping`:

- PC → Router (gateway respondendo corretamente)
- PC → Server (comunicação interna funcional)
- Server → Router (saída do servidor validada)

Todos os testes retornaram resposta, confirmando que o tráfego estava fluindo corretamente pela rede.

## Aprendizados
Este laboratório trouxe aprendizados importantes além da simples configuração de IPs:

- Gateway não é opcional: sem o gateway configurado, o host consegue se comunicar dentro da rede local, mas não consegue alcançar outros destinos.
- Troubleshooting básico: quando um ping falha, o problema pode estar tanto na configuração lógica quanto na camada física.
- Base para SOC: visualizar o tráfego ICMP na prática ajuda a construir a base necessária para análises futuras de pacotes e logs em ferramentas como o Wireshark.

 🧠 Cisco SD-WAN Lab — Configuração e Políticas Avançadas

Este repositório contém o progresso e as configurações realizadas durante minha jornada de aprendizado em Cisco SD-WAN, focando na implementação prática de políticas de controle, roteamento dinâmico, e manipulação de OMP.



 🔧 Objetivo do Laboratório

Simular um ambiente corporativo com múltiplas filiais (branches) conectadas a dois datacenters (DC10 e DC20), utilizando Cisco SD-WAN para:

- Criar uma malha de comunicação escalável e segura
- Definir regras de tráfego dinâmico com OMP
- Aplicar políticas de alta disponibilidade (Active/Standby)
- Controlar preferências de caminho usando TE e TLOCs
- Garantir redundância via controle de exportação e importação de prefixos



 🔄 Etapas realizadas

 ✅ OSPF nas VPNs de Serviço  
- Configuração do OSPF para roteamento dinâmico nas VPN10, VPN20 e VPN50  
- Validação da propagação de rotas internas

 ✅ Política DC Active/Standby  
- Manipulação de OMP para garantir que todo tráfego dos branches utilize preferencialmente o DC10  
- DC20 permanece como standby, garantindo continuidade em caso de falha

 ✅ (Em preparação) TE – OMP Preference  
- Direcionar o tráfego da rede `10.10.10.0/24` para o roteador DC10R2  
- Todo o restante do tráfego deve sair exclusivamente pelo DC10R1  
- Redistribuição dos TLOCs pelo DC20 como fallback

 ✅ (Planejada) Inbound vs Outbound Control Policy  
- Garantir que a rede `10.20.50.0/24` (DMZ no DC20) seja anunciada também via DC10  
- Aumentar a redundância e os caminhos alternativos no overlay



 🖼️ Capturas de Tela (Screenshots)

As imagens a seguir mostram os templates criados, a aplicação das políticas e a configuração da infraestrutura:

- `config.template.1.png`
- `config.template.2.png`
- `omp.routes.validation.png`
- `policy.dc.active.standby.png`
- (Outros arquivos serão adicionados à medida que o laboratório avança)



 📚 Sobre este projeto

Este laboratório é parte da minha formação avançada em Cisco SD-WAN.  

Todos os testes foram realizados em ambiente simulado controlado com uso de Cisco vManage, vSmart, vBond e CSR1000v.




 🧠 Autor

Danilo Conceição 
Especialista em Infraestrutura e Segurança de Redes  
Certificado CCNA | CCNP ENCOR | Em formação CCNP ENARSI  

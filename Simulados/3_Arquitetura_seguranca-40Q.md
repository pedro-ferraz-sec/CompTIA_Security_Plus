# 📝 Simulado Específico - Domínio 3.0: Arquitetura de Segurança (18%)

**Exame:** CompTIA Security+ SY0-701  
**Quantidade:** 40 Questões Situacionais  
**Instruções:** Responda às 40 questões abaixo. Todas as opções (A, B, C, D) estão desmarcadas. O **Gabarito Oficial e Justificativas Técnicas** encontra-se exclusivamente na seção final deste documento.

---

### Questão 1
Uma organização financeira está migrando sua aplicação legada para um provedor de nuvem pública. A equipe de segurança exige que a infraestrutura subjacente, o sistema operacional e o servidor de aplicação sejam mantidos e atualizados exclusivamente pelo provedor, enquanto a equipe de desenvolvimento da empresa deve manter controle total sobre o código da aplicação e suas tabelas de banco de dados. Qual modelo de serviço de nuvem atende estritamente a essas especificações?

A) Infrastructure as Service (IaaS)  
B) Platform as a Service (PaaS)  
C) Software as a Service (SaaS)  
D) Function as a Service (FaaS)  

---

### Questão 2
Um arquiteto de segurança projeta a infraestrutura de rede de um datacenter corporativo. Para impedir que o comprometimento de um servidor web na zona desmilitarizada (DMZ) permita o movimento lateral direto para os servidores de banco de dados internos, ele implementa regras rígidas de firewall que isolam o tráfego que flui horizontalmente entre servidores do mesmo segmento. Qual conceito de arquitetura de rede está sendo aplicado?

A) Roteamento Norte-Sul  
B) Microsegmentação (Tráfego Leste-Oeste)  
C) Proxy Reverso  
D) Gerenciamento Fora de Banda (OOB)  

---

### Questão 3
Durante um projeto de modernização de infraestrutura, uma empresa substitui o provisionamento manual de servidores por arquivos de configuração declarativos armazenados em um repositório Git. Isso permite implantar ambientes idênticos de desenvolvimento e produção de forma automatizada e auditável. Qual benefício de segurança primário essa abordagem de Infrastructure as Code (IaC) proporciona?

A) Eliminação de custos com licenças de software de terceiros  
B) Prevenção do desvio de configuração (*configuration drift*) e garantia de conformidade contínua  
C) Substituição completa de firewalls de rede por regras de sistema operacional  
D) Proteção automática contra ataques de negação de serviço distribuído (DDoS)  

---

### Questão 4
Uma empresa de e-commerce precisa proteger seu site contra ataques direcionados à camada de aplicação, tais como SQL Injection, Cross-Site Scripting (XSS) e falsificação de requisições entre sites (CSRF). Qual dispositivo de segurança deve ser posicionado à frente dos servidores web para inspecionar o tráfego HTTP/HTTPS em nível de aplicação?

A) Firewall de Próxima Geração (NGFW)  
B) Web Application Firewall (WAF)  
C) Sistema de Detecção de Intrusão em Rede (NIDS)  
D) Forward Proxy  

---

### Questão 5
Uma equipe de segurança precisa garantir acesso administrativo remoto altamente seguro a servidores Linux hospedados em uma sub-rede privada sem conectividade direta com a Internet. Para isso, eles configuram um servidor dedicado e endurecido (*hardened*) na rede periférica, onde todos os administradores devem se autenticar e registrar suas sessões antes de acessar os recursos internos. Qual elemento de arquitetura está sendo utilizado?

A) Jump Server (Bastion Host)  
B) Reverse Proxy  
C) Load Balancer  
D) Honeypot  

---

### Questão 6
Para atender aos requisitos da Lei Geral de Proteção de Dados (LGPD) e garantir que a chave de criptografia de um banco de dados de alta sensibilidade nunca seja exposta na memória RAM do servidor de aplicação ou acessada por administradores do sistema operacional, a empresa instala um equipamento físico dedicado acoplado à rede interna especializado no ciclo de vida de chaves criptográficas. Qual dispositivo é esse?

A) Trusted Platform Module (TPM)  
B) Hardware Security Module (HSM)  
C) Cloud Access Security Broker (CASB)  
D) Secure Enclave  

---

### Questão 7
Uma corporação multinacional deseja migrar suas filiais regionais de conexões MPLS caras para conexões diretas de Internet. Para manter o controle de segurança, filtragem de conteúdo, firewall em nuvem e proteção Zero Trust unificados de forma centralizada para todos os usuários remotos e escritórios, a empresa decide adotar a arquitetura SASE. Quais tecnologias formam a base da solução SASE?

A) SD-WAN combinada com Serviços de Segurança em Nuvem (SSE / CASB / SWG / ZTNA)  
B) MPLS dedicada combinada com IPS físico em cada filial  
C) VPN IPsec ponto-a-ponto combinada com WAF local  
D) VDI (Virtual Desktop Infrastructure) combinada com redes locais legadas  

---

### Questão 8
Uma equipe de engenharia de segurança implementa uma solução de rede definida por software (SDN). Um analista precisa alterar a política de segurança global para impedir que determinado tráfego atravesse a rede corporativa. Em qual plano da arquitetura SDN o analista deve aplicar a alteração de configuração?

A) Plano de Dados (*Data Plane*)  
B) Plano de Encaminhamento (*Forwarding Plane*)  
C) Plano de Controle (*Control Plane*)  
D) Plano de Gerenciamento de Aplicação Local  

---

### Questão 9
Um analista de cibersegurança está projetando uma política para mitigar riscos associados ao uso não autorizado de serviços de nuvem pelos funcionários (Shadow IT). A solução deve interceptar o tráfego de saída da empresa para a Internet e impor políticas de prevenção de perda de dados (DLP) e controle de acesso a aplicações SaaS corporativas. Qual tecnologia é a mais indicada?

A) Cloud Access Security Broker (CASB)  
B) Firewall de Rede Tradicional (Stateful)  
C) Network Access Control (NAC)  
D) Servidor DNS Interno  

---

### Questão 10
Durante a auditoria de um sistema crítico de automação industrial (SCADA/ICS) localizado em uma usina de energia, o auditor observa que a rede de controle operacional está totalmente separada fisicamente de qualquer outra rede corporativa ou acesso à Internet, sem nenhum cabo ou conexão sem fio que as interligue. Qual técnica de isolamento de segurança está implementada?

A) Air Gap  
B) VLAN Privada  
C) Sub-rede Filtrada (DMZ)  
D) Tunelamento GRE  

---

### Questão 11
Uma organização de saúde precisa processar prontuários médicos enquanto os dados estão sendo analisados e manipulados na memória RAM por um algoritmo de inteligência artificial. Qual estado do dado está sendo protegido e qual tecnologia moderna de hardware é usada para garantir o processamento seguro isolado?

A) Dado em Repouso (*At Rest*) protegidos por criptografia de disco total (FDE)  
B) Dado em Trânsito (*In Transit*) protegidos por TLS 1.3  
C) Dado em Uso (*In Use*) protegidos por Computação Confidencial / Enclaves Seguros  
D) Dado em Backup (*In Archive*) protegidos por fitas magnéticas offline  

---

### Questão 12
Um arquiteto de segurança precisa selecionar um local alternativo de recuperação de desastres para uma aplicação de missão crítica. O requisito de negócio estabelece um RTO (Recovery Time Objective) de poucas horas. O site secundário deve possuir infraestrutura física, energia e servidores já montados e com conectividade de rede, porém com backups e dados necessitando ser restaurados na ocorrência do evento. Qual tipo de site de recuperação atende a esses requisitos?

A) Cold Site  
B) Warm Site  
C) Hot Site  
D) Mirrored Site  

---

### Questão 13
Um administrador de rede deseja isolar completamente o tráfego de administração de roteadores, switches e firewalls do tráfego comum de dados gerado pelos usuários internos, evitando que ataques de interceptação ou cheiragem (*sniffing*) na LAN corporativa capturem sessões administrativas. Qual arquitetura de rede atende a essa necessidade?

A) Gerenciamento Fora de Banda (*Out-of-band / OOB Management*)  
B) Gerenciamento Dentro de Banda (*In-band Management*)  
C) Espelhamento de Porta (SPAN Port)  
D) Sub-rede Filtrada (DMZ)  

---

### Questão 14
Uma empresa decide implementar microsserviços empacotados com todas as suas dependências e bibliotecas necessárias para rodar sobre um sistema operacional hospedeiro compartilhado, permitindo rápida inicialização e alta densidade de implantação. Qual tecnologia de arquitetura está sendo descrita?

A) Máquinas Virtuais (Hipervisor Tipo 1)  
B) Conteinerização (ex: Docker)  
C) Servidores Bare-Metal  
D) Emulação de Hardware  

---

### Questão 15
Para proteger as comunicações de e-mail corporativo contra alteração de conteúdo e garantir o não-repúdio da autoria das mensagens enviadas pelos executivos, o departamento de TI decide implementar um padrão que assina digitalmente e criptografa o conteúdo das mensagens utilizando certificados da PKI corporativa. Qual protocolo/padrão deve ser adotado?

A) S/MIME  
B) DKIM  
C) STARTTLS  
D) HTTPS  

---

### Questão 16
Um engenheiro de segurança configura um conjunto de servidores web sob um balanceador de carga (*Load Balancer*). Para garantir alta disponibilidade caso um dos servidores apresente falhas físicas, o balanceador realiza checagens periódicas no estado dos servidores e redireciona o tráfego automaticamente longe de qualquer nó indisponível. Qual funcionalidade do balanceador garante essa ação?

A) Health Checks (Verificações de Saúde)  
B) SSL Offloading  
C) Persistência de Sessão (*Sticky Sessions*)  
D) Round-Robin Dinâmico  

---

### Questão 17
Um desenvolvedor está projetando um sistema onde falhas elétricas ou travamentos do software em uma catraca eletrônica de emergência predial nunca devem prender as pessoas dentro do edifício. Em caso de perda total de energia ou erro do sistema, as portas devem destravar automaticamente. Qual princípio de design de segurança está sendo aplicado?

A) Fail-Closed (Falha Segura / Bloqueada)  
B) Fail-Safe / Fail-Open (Falha Aberta)  
C) Negação Implícita  
D) Princípio do Menor Privilégio  

---

### Questão 18
Uma empresa de serviços em nuvem quer implantar um ambiente onde o código do cliente seja executado apenas em resposta a eventos específicos (como um upload de arquivo) e a infraestrutura subjacente seja provisionada, dimensionada e desativada automaticamente sem que o cliente precise gerenciar servidores ou sistemas operacionais. Qual paradigma de computação é esse?

A) IaaS (Infraestrutura como Serviço)  
B) Computação Serverless / FaaS  
C) Contêineres Monolíticos  
D) Hospedagem Dedicada Bare-Metal  

---

### Questão 19
Durante a configuração de um firewall de borda, o analista adiciona uma regra ao final de todas as políticas explícitas com a seguinte instrução: "Bloquear qualquer tráfego que não coincida com as regras anteriores". Qual princípio fundamental de firewall é esse?

A) Regra Compensatória  
B) Negação Implícita (*Implicit Deny*)  
C) Permissão Explícita  
D) Inspeção Stateful  

---

### Questão 20
Para evitar que a perda de conectividade com a Internet em um datacenter principal interrompa as operações da empresa, a equipe de infraestrutura contrata dois provedores de Internet (ISPs) distintos, utilizando rotas físicas de fibra ótica totalmente separadas que entram no edifício por pontos geográficos opostos. Qual conceito de resiliência está sendo aplicado?

A) Redundância de Caminho / Diversidade de Meio  
B) Balanceamento de Carga de Aplicação  
C) Espelhamento de Porta  
D) Agregação de Link (LACP)  

---

### Questão 21
Uma instituição financeira precisa proteger as consultas que seus clientes fazem aos nomes de domínio de seus servidores de Internet contra ataques de envenenamento de cache DNS (*DNS Cache Poisoning*). Qual tecnologia garante a autenticidade e integridade das respostas DNS por meio de assinaturas digitais criptográficas?

A) DoH (DNS over HTTPS)  
B) DoT (DNS over TLS)  
C) DNSSEC  
D) Registros MX Criptografados  

---

### Questão 22
Uma organização precisa garantir que a chave privada de seu certificado raiz da PKI interna seja mantida sob o mais alto nível de proteção física e lógica, permanecendo totalmente desconectada de qualquer rede e alimentada apenas quando for necessário assinar uma Autoridade Certificadora Intermediária. Qual conceito se aplica?

A) CA Offline  
B) Sub-rede Filtrada  
C) Servidor OCSP  
D) Repositório CRL  

---

### Questão 23
Um analista de segurança precisa configurar um túnel VPN seguro entre duas filiais corporativas através da Internet pública. A solução deve oferecer criptografia forte na camada de rede (Camada 3 do modelo OSI), garantindo autenticação e confidencialidade de todo o tráfego IP entre os roteadores de borda das duas pontas. Qual protocolo é o padrão da indústria para esse cenário?

A) IPsec no modo Túnel  
B) IPsec no modo Transporte  
C) TLS no modo Gateway  
D) SSH Port Forwarding  

---

### Questão 24
Para evitar que a falha súbita em um único módulo de memória RAM ou na fonte de alimentação de um servidor de banco de dados cause a parada total das transações financeiras, a empresa instala dois servidores idênticos operando em conjunto, onde ambos processam requisições simultaneamente e compartilham o estado do sistema. Qual conceito de disponibilidade descreve esse arranjo?

A) Cluster Ativo-Passivo  
B) Cluster Ativo-Ativo  
C) Cold Standby  
D) Réplica Assíncrona  

---

### Questão 25
Em uma arquitetura de segurança moderna, qual dispositivo atua interceptando as conexões iniciadas por clientes internos, inspeciona o conteúdo das requisições web, filtra URLs maliciosas e aplica controle de acesso a sites antes de encaminhar a requisição para a Internet?

A) Reverse Proxy  
B) Forward Proxy  
C) Web Application Firewall (WAF)  
D) Network Address Translation (NAT)  

---

### Questão 26
Uma empresa de tecnologia armazena dados de seus clientes europeus em um datacenter localizado nos Estados Unidos. Durante uma auditoria de conformidade, a equipe jurídica alerta que essa transferência fere requisitos regulatórios sobre a localização física onde os dados de cidadãos podem ser armazenados e processados. Qual conceito de segurança e privacidade está em discussão?

A) Soberania dos Dados (*Data Sovereignty*)  
B) Sanitização de Dados  
C) Criptografia de Trânsito  
D) Mascaramento Dinâmico de Dados  

---

### Questão 27
Qual protocolo de gerenciamento de rede deve ser utilizado para monitorar a saúde de roteadores e switches corporativos garantindo que as mensagens de gerenciamento sejam criptografadas e autenticadas para evitar a interceptação de informações de desempenho ou alteração de configurações por atacantes?

A) SNMPv1  
B) SNMPv2c  
C) SNMPv3  
D) ICMPv6  

---

### Questão 28
Um administrador de TI precisa criar uma armadilha em um segmento isolado da rede corporativa contendo arquivos falsos e serviços deliberadamente vulneráveis para atrair atacantes, observar suas táticas e coletar inteligência sobre ameaças sem colocar os ativos reais em risco. Qual solução de arquitetura deve ser implantada?

A) Honeypot / Honeynet  
B) Sub-rede Filtrada (DMZ)  
C) Sandbox de Desenvolvimento  
D) Sistema de Detecção de Intrusão (IDS)  

---

### Questão 29
Para proteger os dados em repouso armazenados nos notebooks corporativos dos funcionários contra acesso não autorizado no caso de perda ou roubo do dispositivo físico, qual controle de segurança técnico deve ser ativado?

A) Criptografia Total de Disco (FDE / BitLocker)  
B) Criptografia de Camada de Transporte (TLS)  
C) Assinatura Digital de Arquivo  
D) Mascaramento de Dados (*Data Masking*)  

---

### Questão 30
Uma equipe de resposta a incidentes precisa realizar uma simulação baseada em cenários hipotéticos de ataque de ransomware, onde os executivos e líderes técnicos discutem suas responsabilidades, decisões e fluxos de comunicação em uma sala de reunião sem afetar nenhum ambiente de produção. Qual tipo de teste de resiliência está sendo conduzido?

A) Teste de Failover em Produção  
B) Exercício de Mesa (*Tabletop Exercise*)  
C) Teste de Intrusão (*Pen Test*) Red Team  
D) Análise de Vulnerabilidade Autenticada  

---

### Questão 31
Em uma infraestrutura de chaves públicas (PKI), qual funcionalidade é responsável por permitir que o próprio servidor web consulte o status de revogação de seu certificado na Autoridade Certificadora (CA) e anexe uma prova assinada com carimbo de data/hora diretamente durante o *handshake* TLS com o cliente, reduzindo a carga sobre a CA e aumentando a privacidade do usuário?

A) Lista de Revogação de Certificados (CRL)  
B) OCSP Stapling  
C) Solicitação de Assinatura de Certificado (CSR)  
D) Criptografia Assimétrica de Tráfego  

---

### Questão 32
Um hospital utiliza dispositivos médicos conectados à rede (IoT médico) que executam um sistema operacional de tempo real (RTOS) com recursos computacionais limitados e sem capacidade de receber atualizações de patch frequentes. Qual controle compensatório de arquitetura de rede deve ser adotado para proteger esses dispositivos contra ameaças cibernéticas?

A) Instalar um agente EDR em cada dispositivo médico  
B) Isolar os dispositivos em uma VLAN dedicada protegida por um firewall com inspeção profunda de pacotes  
C) Habilitar autenticação multifator (MFA) no firmware de cada sensor  
D) Conectar todos os dispositivos diretamente à Internet pública para facilitar o suporte do fabricante  

---

### Questão 33
Uma organização deseja garantir que, caso a chave privada de seu servidor web seja comprometida no futuro por um atacante, esse atacante não consiga descriptografar as sessões de comunicação passadas que foram gravadas anteriormente na rede. Qual propriedade criptográfica deve ser habilitada nas negociações do TLS?

A) Perfect Forward Secrecy (PFS)  
B) Hashing Criptográfico (SHA-256)  
C) Criptografia Simétrica AES-256  
D) Assinatura Digital RSA  

---

### Questão 34
Para garantir a continuidade das operações em caso de interrupção abrupta e total do fornecimento de energia elétrica da concessionária pública em um datacenter corporativo, qual sequência de componentes de energia de emergência deve ser projetada?

A) Gerador a Diesel acionado imediatamente sem suporte de UPS  
B) Nobreak (UPS) para suprimento imediato de curto prazo seguido pela partida automatizada do Gerador a Diesel  
C) Protetores de surto individuais conectados a baterias de notebooks  
D) Redundância de fontes ATX internas nos servidores sem baterias externas  

---

### Questão 35
Durante o desenvolvimento de um aplicativo mobile corporativo, os engenheiros substituem números de cartão de crédito e dados de identificação pessoal (PII) por valores aleatórios não correlacionados de formato equivalente gerados por um sistema central, onde o dado original é armazenado em um cofre seguro fora da aplicação. Qual técnica de proteção de dados foi aplicada?

A) Criptografia Homomórfica  
B) Tokenização  
C) Esteganografia  
D) Sanitização Criptográfica  

---

### Questão 36
Qual modelo de arquitetura de segurança exige que cada tentativa de acesso a um recurso interno ou em nuvem seja verificada e autorizada com base na identidade do usuário, estado de conformidade do dispositivo e contexto do acesso, assumindo que a rede interna é tão hostil quanto a Internet pública?

A) Defesa Perimetral Tradicional  
B) Arquitetura Confiança Zero (*Zero Trust Architecture*)  
C) Rede de Longa Distância Definida por Software (SD-WAN)  
D) Modelo de Federação de Identidade Legado  

---

### Questão 37
Uma equipe de infraestrutura precisa restaurar rapidamente o estado operacional de um servidor virtual de aplicação exatamente como ele estava antes da aplicação de uma atualização mal-sucedida de software realizada há 30 minutos. Qual mecanismo de recuperação é o mais ágil para essa situação?

A) Restauração de Backup Completo Fita-a-Disco  
B) Reversão para um Snapshot do Volume Virtual  
C) Reconstrução do Servidor a partir da Imagem Base  
D) Sincronização de Banco de Dados Assíncrona  

---

### Questão 38
Qual o papel de um Sistema de Prevenção de Intrusão baseado em Host (HIPS) instalado em um servidor crítico?

A) Monitorar e bloquear ativamente comportamentos maliciosos e chamadas de sistema suspeitas diretamente no sistema operacional do dispositivo  
B) Inspecionar pacotes de rede que atravessam a sub-rede e redefinir conexões TCP no roteador de borda  
C) Gerar relatórios de conformidade regulatória para auditorias externas  
D) Armazenar cópias de segurança criptografadas do registro do sistema  

---

### Questão 39
Uma empresa deseja implementar controle de acesso à rede local (NAC) com base no padrão IEEE 802.1X. Quando um computador é conectado a uma porta física do switch de acesso, qual entidade atua como o autenticador (*Authenticater*) solicitando credenciais e repassando-as ao servidor RADIUS?

A) O dispositivo do usuário (*Supplicant*)  
B) O switch de rede ou ponto de acesso Wi-Fi  
C) O servidor de Banco de Dados de Identidades (Active Directory)  
D) O Firewall de Borda  

---

### Questão 40
Uma organização armazena backups críticos em discos rígidos externos que são transportados semanalmente para um cofre de segurança em uma instalação física distinta. Para garantir que os backups estejam imunes a modificações ou deleções por ataques de ransomware que infectem a rede corporativa, o que essa estratégia garante?

A) Imutabilidade via Air Gap físico para backups offline  
B) Alta disponibilidade via replicação síncrona  
C) Balanceamento de carga de dados em tempo real  
D) Despoluição magnética dinâmica  

---

## 🏆 Gabarito Oficial e Justificativas Técnicas

#### 1. Resposta Correta: B (Platform as a Service - PaaS)
* **Justificativa:** No modelo PaaS, o provedor de nuvem é responsável pelo gerenciamento da infraestrutura física, rede, camada de virtualização, sistema operacional e servidor de aplicação/middleware. O cliente é responsável apenas pelo desenvolvimento, implantação e manutenção do código da aplicação e dos dados. No IaaS (A), o cliente gerencia o SO. No SaaS (C), o cliente usa a aplicação pronta.

#### 2. Resposta Correta: B (Microsegmentação / Tráfego Leste-Oeste)
* **Justificativa:** O tráfego Leste-Oeste (*East-West Traffic*) refere-se ao tráfego que flui lateralmente entre servidores dentro do mesmo datacenter ou segmento. A microsegmentação cria zonas de segurança granular para bloquear movimentos laterais em caso de comprometimento. O tráfego Norte-Sul (A) é o tráfego que entra ou sai do datacenter para a Internet.

#### 3. Resposta Correta: B (Prevenção do desvio de configuração e garantia de conformidade)
* **Justificativa:** A Infraestrutura como Código (IaC) utiliza arquivos declarativos para provisionar ambientes de forma padronizada, automatizada e auditável, eliminando o *configuration drift* (desvio de configuração causado por alterações manuais não registradas).

#### 4. Resposta Correta: B (Web Application Firewall - WAF)
* **Justificativa:** O WAF inspeciona o tráfego em nível de aplicação (Camada 7 do modelo OSI), identificando e bloqueando ataques específicos de aplicações web como SQL Injection, XSS e CSRF. O NGFW (A) inspeciona camadas de rede e transporte com inspeção profunda, mas o WAF é especializado na camada HTTP/HTTPS de aplicações web.

#### 5. Resposta Correta: A (Jump Server / Bastion Host)
* **Justificativa:** Um *Jump Server* (ou *Bastion Host*) é um servidor altamente protegido e auditado que serve como ponto único de entrada para administradores acessarem sub-redes privadas e sistemas internos de alta sensibilidade sem expor esses sistemas diretamente.

#### 6. Resposta Correta: B (Hardware Security Module - HSM)
* **Justificativa:** O HSM é um dispositivo de hardware dedicado (appliance de rede ou placa PCI) projetado especificamente para a geração, armazenamento e gerenciamento seguro de chaves criptográficas em escala corporativa. O TPM (A) é um chip soldado em placas-mãe de dispositivos individuais (endpoints).

#### 7. Resposta Correta: A (SD-WAN combinada com Serviços de Segurança em Nuvem)
* **Justificativa:** A arquitetura SASE (*Secure Access Service Edge*) converge tecnologias de rede de longa distância (SD-WAN) com serviços de segurança prestados diretamente na nuvem (Security Service Edge - SSE, incluindo CASB, SWG, FWaaS e ZTNA).

#### 8. Resposta Correta: C (Plano de Controle - Control Plane)
* **Justificativa:** Em redes definidas por software (SDN), o **Plano de Controle** é a camada lógica responsável pela tomada de decisões de roteamento, políticas e regras de segurança. O **Plano de Dados** (A) apenas executa o encaminhamento físico dos pacotes com base nas instruções do Plano de Controle.

#### 9. Resposta Correta: A (Cloud Access Security Broker - CASB)
* **Justificativa:** O CASB é uma solução de software/serviço posicionada entre os usuários da empresa e os provedores de nuvem para aplicar políticas de segurança, DLP, controle de acesso e visibilidade sobre o uso de aplicações SaaS (combatendo o Shadow IT).

#### 10. Resposta Correta: A (Air Gap)
* **Justificativa:** O *Air Gap* é uma medida de segurança física e de rede na qual um sistema ou rede é totalmente isolado e desconectado de qualquer outra rede, especialmente da Internet ou da rede corporativa comum.

#### 11. Resposta Correta: C (Dado em Uso / Computação Confidencial)
* **Justificativa:** Dados na memória RAM sendo processados pela CPU estão no estado "Em Uso" (*Data in Use*). A Computação Confidencial protege os dados em uso executando o processamento dentro de um enclave seguro baseado em hardware (TEE).

#### 12. Resposta Correta: B (Warm Site)
* **Justificativa:** Um *Warm Site* possui a infraestrutura de hardware, energia, climatização e conectividade de rede montadas, mas não mantém os dados em tempo real (exigindo a restauração de backups para entrar em produção). O *Hot Site* (C) mantém os dados sincronizados em tempo real (RTO próximo de zero). O *Cold Site* (A) possui apenas o espaço físico e infraestrutura básica sem servidores pré-configurados.

#### 13. Resposta Correta: A (Gerenciamento Fora de Banda - OOB Management)
* **Justificativa:** O gerenciamento OOB (*Out-of-band*) utiliza uma rede física ou lógica totalmente separada para administrar dispositivos de rede, garantindo que o tráfego administrativo não possa ser capturado ou atacado na rede de produção de dados dos usuários.

#### 14. Resposta Correta: B (Conteinerização - ex: Docker)
* **Justificativa:** A conteinerização permite empacotar uma aplicação e suas dependências em um contêiner leve que compartilha o kernel do sistema operacional do hospedeiro (*host*), garantindo alta densidade e rápida inicialização em comparação com máquinas virtuais completas (A).

#### 15. Resposta Correta: A (S/MIME)
* **Justificativa:** O S/MIME (*Secure/Multipurpose Internet Mail Extensions*) é o padrão da indústria para assinatura digital e criptografia de e-mails ponta-a-ponta utilizando certificados digitais baseados em PKI (garantindo autenticidade, integridade e não-repúdio).

#### 16. Resposta Correta: A (Health Checks / Verificações de Saúde)
* **Justificativa:** Os *Health Checks* realizam testes periódicos (ex: requisições HTTP ping no servidor) para validar se o nó está saudável. Caso detectem falhas, o balanceador de carga para de enviar tráfego para o servidor com defeito.

#### 17. Resposta Correta: B (Fail-Safe / Fail-Open)
* **Justificativa:** O princípio *Fail-Safe / Fail-Open* garante que, em caso de falha de energia ou erro do sistema, o dispositivo falhe liberando o acesso para proteger a vida humana e a segurança física das pessoas. O *Fail-Closed* (A) bloqueia o acesso em caso de falha (usado para proteger dados e ativos de alta confidencialidade).

#### 18. Resposta Correta: B (Computação Serverless / FaaS)
* **Justificativa:** Na computação *Serverless* (ou *Function as a Service* - FaaS), a infraestrutura é totalmente abstraída do desenvolvedor. O código é executado sob demanda provocado por eventos, e os recursos são escalados e encerrados automaticamente.

#### 19. Resposta Correta: B (Negação Implícita - Implicit Deny)
* **Justificativa:** O princípio de *Implicit Deny* estabelece que tudo o que não for explicitamente permitido por uma regra de firewall deve ser automaticamente bloqueado/negado ao final da lista de regras.

#### 20. Resposta Correta: A (Redundância de Caminho / Diversidade de Meio)
* **Justificativa:** A diversidade de meio e a redundância de rotas físicas de fibra ótica garantem que a falha física em uma tubulação ou escavação de rua que corte uma das fibras não interrompa a conectividade da empresa, mantendo o segundo link ativo.

#### 21. Resposta Correta: C (DNSSEC)
* **Justificativa:** O DNSSEC (*DNS Security Extensions*) adiciona assinaturas criptográficas aos registros DNS para que os resolvedores possam verificar a autenticidade e a integridade dos dados, prevenindo o envenenamento de cache DNS.

#### 22. Resposta Correta: A (CA Offline)
* **Justificativa:** Uma Autoridade Certificadora Raiz (*Root CA*) mantida *offline* é desconectada de qualquer rede e mantida desligada para evitar seu comprometimento. Ela é ligada apenas para assinar certificados de CAs Intermediárias.

#### 23. Resposta Correta: A (IPsec no modo Túnel)
* **Justificativa:** O IPsec no modo Túnel criptografa todo o pacote IP original (cabeçalho + carga útil) e adiciona um novo cabeçalho IP, sendo o padrão ideal para VPNs Site-to-Site entre roteadores de borda. O modo Transporte (B) criptografa apenas a carga útil e é usado principalmente em conexões Host-to-Host.

#### 24. Resposta Correta: B (Cluster Ativo-Ativo)
* **Justificativa:** Em um arranjo *Ativo-Ativo*, todos os nós do cluster processam requisições de forma simultânea e compartilham a carga de trabalho, oferecendo alta disponibilidade e desempenho otimizado. No *Ativo-Passivo* (A), o nó secundário fica ocioso aguardando a falha do primário.

#### 25. Resposta Correta: B (Forward Proxy)
* **Justificativa:** O *Forward Proxy* situa-se à frente dos clientes internos e gerencia/inspeciona as requisições de **saída** direcionadas à Internet. O *Reverse Proxy* (A) situa-se à frente dos servidores internos e gerencia o tráfego de **entrada**.

#### 26. Resposta Correta: A (Soberania dos Dados - Data Sovereignty)
* **Justificativa:** Soberania dos dados refere-se ao princípio de que os dados estão sujeitos às leis e estruturas regulatórias do país em que são fisicamente coletados ou armazenados (ex: restrições de transferência transfronteiriça sob a GDPR).

#### 27. Resposta Correta: C (SNMPv3)
* **Justificativa:** O SNMPv3 traz suporte nativo a criptografia de dados e autenticação forte. As versões v1 e v2c enviavam credenciais (*community strings*) e dados de gerenciamento em texto claro na rede.

#### 28. Resposta Correta: A (Honeypot / Honeynet)
* **Justificativa:** Um *Honeypot* é um recurso de engodo projetado para atuar como armadilha para atração de invasores, permitindo monitorar suas ferramentas, técnicas e procedimentos (TTPs) de forma isolada e segura.

#### 29. Resposta Correta: A (Criptografia Total de Disco - FDE)
* **Justificativa:** A Criptografia Total de Disco (*Full Disk Encryption* - FDE, como o BitLocker) criptografa todo o volume do armazenamento em repouso, impedindo a leitura dos dados caso o disco rígido ou o notebook físico sejam roubados.

#### 30. Resposta Correta: B (Exercício de Mesa - Tabletop Exercise)
* **Justificativa:** O *Tabletop Exercise* é uma simulação teórica conduzida em sala de reunião onde os participantes revisam o plano de resposta a incidentes e discutem suas papéis diante de um cenário hipotético sem gerar qualquer impacto nos sistemas reais.

#### 31. Resposta Correta: B (OCSP Stapling)
* **Justificativa:** No *OCSP Stapling*, o próprio servidor web obtém uma resposta assinada e com carimbo de data/hora do servidor OCSP da CA e a anexa ao *handshake* TLS enviado ao cliente, otimizando o desempenho e preservando a privacidade do usuário.

#### 32. Resposta Correta: B (Isolar os dispositivos em uma VLAN dedicada protegida por firewall)
* **Justificativa:** Dispositivos legados ou embarcados (RTOS/IoT) que não suportam agentes modernos ou patches frequentes devem ser protegidos por controles compensatórios de arquitetura, como a segmentação estrita em uma VLAN dedicada isolada por firewall.

#### 33. Resposta Correta: A (Perfect Forward Secrecy - PFS)
* **Justificativa:** O PFS utiliza algoritmos de troca de chaves efêmeras (como Diffie-Hellman Efêmero - DHE/ECDHE) para gerar chaves de sessão exclusivas para cada comunicação. Assim, mesmo que a chave privada de longo prazo do servidor seja roubada no futuro, o tráfego passado gravado não poderá ser descriptografado.

#### 34. Resposta Correta: B (Nobreak/UPS para suporte imediato + Gerador a Diesel)
* **Justificativa:** Em uma falta de energia pública, os nobreaks (UPS) fornecem energia contínua imediata via baterias para cobrir os segundos/minutos necessários até que os geradores a diesel sejam acionados e estabilizem a alimentação elétrica de longo prazo.

#### 35. Resposta Correta: B (Tokenização)
* **Justificativa:** A tokenização substitui um dado sensível (como o número do cartão de crédito) por um valor substituto aleatório não sensível (token) de mesmo formato, mantendo a correspondência original mapeada em um cofre de tokens (*token vault*) isolado e seguro.

#### 36. Resposta Correta: B (Arquitetura Confiança Zero - Zero Trust Architecture)
* **Justificativa:** O modelo *Zero Trust* baseia-se no princípio de "nunca confiar, sempre verificar", exigindo validação e autorização contínuas para cada requisição de acesso, independentemente da localização física ou lógica do dispositivo na rede.

#### 37. Resposta Correta: B (Reversão para um Snapshot do Volume Virtual)
* **Justificativa:** O *Snapshot* é um registro instantâneo do estado e dos dados de uma máquina virtual em determinado momento, permitindo reverter alterações ou atualizações mal-sucedidas em poucos segundos ou minutos.

#### 38. Resposta Correta: A (Monitorar e bloquear ativamente comportamentos maliciosos diretamente no SO)
* **Justificativa:** O HIPS (*Host-based Intrusion Prevention System*) é instalado diretamente no endpoint/servidor para inspecionar chamadas de sistema, integridade de arquivos e tráfego local, agindo preventivamente para bloquear ataques no próprio host.

#### 39. Resposta Correta: B (O switch de rede ou ponto de acesso Wi-Fi)
* **Justificativa:** Na arquitetura IEEE 802.1X, o dispositivo do usuário é o *Supplicant*, o switch de rede/AP é o **Autenticador** (*Authenticator* - que bloqueia a porta até a validação) e o servidor RADIUS/TACACS+ é o **Servidor de Autenticação** (*Authentication Server*).

#### 40. Resposta Correta: A (Imutabilidade via Air Gap físico para backups offline)
* **Justificativa:** Backups mantidos em mídias físicas desconectadas da rede (*offline*) criam um *Air Gap* físico que impede que malwares em execução na rede corporativa (como ransomware) alcancem, criptografem ou deletem as cópias de segurança.

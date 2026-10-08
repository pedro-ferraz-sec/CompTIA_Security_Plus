# 📝 Simulado Específico - Domínio 4.0: Operações de Segurança (28%)
**Certificação CompTIA Security+ SY0-701**
**Total de Questões:** 40
**Formato:** Questões situacionais sem respostas marcadas. Gabarito Oficial e Justificativas Técnicas consolidados ao final do documento.

---

### QUESTÃO 1
Uma equipe de SOC detectou que um servidor crítico de banco de dados foi infectado por um ransomware ativado recentemente. O malware está criptografando arquivos de forma ativa e tentando se espalhar lateralmente para outros hosts da sub-rede. De acordo com o ciclo de resposta a incidentes (NIST SP 800-61 / CompTIA), qual deve ser a PRIMEIRA ação do analista de resposta a incidentes?

A) Desligar o servidor imediatamente da tomada elétrica para interromper a criptografia.
B) Isolar logicamente o servidor da rede, desconectando o cabo de rede ou alterando a VLAN/regras de firewall.
C) Executar o antivírus para remover o executável do ransomware e limpar o registro.
D) Restaurar imediatamente o backup mais recente do banco de dados para evitar perda de dados.

---

### QUESTÃO 2
Durante uma investigação de segurança cibernética em um servidor comprometido, o analista forense precisa coletar evidências digitais do sistema em execução. Para respeitar estritamente a Ordem de Volatilidade de dados, qual dos seguintes artefatos deve ser capturado em PRIMEIRO lugar?

A) Arquivo de paginação (Swap / Pagefile) gravado no disco rígido.
B) Conteúdo da memória RAM dinâmica.
C) Tabela de arquivos mestre (MFT) do sistema de arquivos NTFS.
D) Registros de logs do sistema de eventos do Windows (Event Logs).

---

### QUESTÃO 3
Uma organização deseja implementar um controle de autenticação em sua rede Wi-Fi corporativa que exija que cada usuário se autentique com suas credenciais individuais do Active Directory. Além disso, a rede deve utilizar o protocolo IEEE 802.1X com um servidor AAA dedicado na porta TCP 49. Qual protocolo AAA é mais indicado para esse cenário específico?

A) RADIUS
B) TACACS+
C) Kerberos
D) LDAP

---

### QUESTÃO 4
Um analista de SOC monitora um alerta do sistema SIEM indicando que um executável desconhecido tentou modificar arquivos do sistema na pasta `C:\Windows\System32`. A ferramenta responsável por gerar esse alerta específico monitora hashes de arquivos do sistema contra alterações não autorizadas. Qual controle de monitoramento gerou este alerta?

A) Data Loss Prevention (DLP)
B) File Integrity Monitoring (FIM)
C) Network Flow Analysis (NetFlow)
D) User and Entity Behavior Analytics (UEBA)

---

### QUESTÃO 5
Uma empresa de e-commerce implementa uma solução para impedir que atacantes enviem e-mails falsificados se passando pelo domínio corporativo `@empresa.com`. A solução utiliza uma chave criptográfica pública publicada no DNS do domínio para permitir que o servidor destinatário valide a assinatura digital presente no cabeçalho do e-mail. Qual tecnologia atende a esse requisito específico?

A) SPF (Sender Policy Framework)
B) DKIM (DomainKeys Identified Mail)
C) DMARC (Domain-based Message Authentication, Reporting, and Conformance)
D) STARTTLS

---

### QUESTÃO 6
Durante uma auditoria de segurança interna em um ambiente Linux, o auditor verifica que alguns usuários possuem permissão para executar comandos como root sem digitar a senha, e que contas administrativas compartilhadas estão sendo utilizadas diretamente. O auditor recomenda implementar uma solução que centralize, monitore, grave sessões e controle o acesso a credenciais de alto privilégio. Qual solução deve ser implementada?

A) Identity and Access Management (IAM)
B) Privileged Access Management (PAM)
C) Single Sign-On (SSO)
D) Security Information and Event Management (SIEM)

---

### QUESTÃO 7
Um administrador de rede precisa realizar um escaneamento de vulnerabilidades em 500 estações de trabalho corporativas. O objetivo é obter um relatório detalhado sobre atualizações de segurança pendentes, softwares não autorizados instalados e configurações incorretas de registro local sem gerar consumo excessivo de banda de rede ou falso-positivos na detecção de portas. Qual tipo de escaneamento deve ser executado?

A) Escaneamento Não Credenciado (Uncredentialed Scan)
B) Escaneamento Credenciado (Credentialed Scan)
C) Escaneamento Passivo de Tráfego (Passive Banner Grabbing)
D) Teste de Penetração Cego (Blind Penetration Test)

---

### QUESTÃO 8
Uma organização implementa um servidor proxy de e-mail e deseja garantir que mensagens recebidas contendo links maliciosos sejam analisadas em tempo real. O sistema deve abrir o link em uma máquina virtual isolada antes de entregar a mensagem ao destinatário para observar se ocorrem downloads maliciosos ou desvios de execução. Qual técnica de proteção está sendo aplicada?

A) Filtro de Conteúdo estático por palavras-chave
B) Sandbox / Análise Dinâmica em Ambiente Isolado
C) Lista de Bloqueio de IP (IP Blocklist)
D) Análise de Reputação de Domínio (DNS Sinkhole)

---

### QUESTÃO 9
Em uma investigação forense digital, o perito copia a imagem de um disco rígido utilizando uma ferramenta dedicada. Para garantir a integridade da evidência e provar em juízo que os dados não sofreram qualquer alteração durante o processo de coleta e transporte, qual procedimento é indispensável?

A) Criptografar a imagem do disco com uma chave simétrica AES-256.
B) Gerar o hash criptográfico (ex: SHA-256) da mídia original e da imagem gerada e registrar na Cadeia de Custódia.
C) Formatar o disco original após a conclusão da cópia para evitar vazamentos de dados.
D) Armazenar a imagem coletada exclusivamente em um servidor de nuvem pública sem controle de acesso físico.

---

### QUESTÃO 10
Uma equipe de resposta a incidentes precisa realizar a extração da imagem de disco de um laptop apreendido que contém dados sigilosos e é evidência de uma fraude corporativa. Qual dispositivo de hardware deve ser inserido entre o drive original e a estação de trabalho forense para impedir que o sistema operacional de análise grave ou altere metadados no drive investigado?

A) Hardware Security Module (HSM)
B) Write Blocker (Bloqueador de Escrita)
C) Trusted Platform Module (TPM)
D) Network Access Control (NAC)

---

### QUESTÃO 11
Uma aplicação Web corporativa utiliza o protocolo SAML 2.0 para permitir que funcionários acessem múltiplos serviços em nuvem usando uma única credencial. Durante a autenticação, o servidor interno valida o usuário e emite uma afirmação XML assinada para o serviço de nuvem. No modelo SAML, qual papel é desempenhado pelo servidor interno da organização?

A) Service Provider (SP)
B) Identity Provider (IdP)
C) Relying Party (RP)
D) Certificate Authority (CA)

---

### QUESTÃO 12
Durante um incidente de segurança, o analista identificou a presença de um malware que se instalou na máquina de um executivo. Após isolar o sistema e identificar a causa-raiz (uma vulnerabilidade em um software de PDF desatualizado), o analista removeu o malware, limpou os registros corrompidos e aplicou a atualização de segurança no software afetado. De acordo com o ciclo de resposta a incidentes, em qual fase o analista concluiu essas ações?

A) Preparação
B) Contenção
C) Erradicação
D) Lições Aprendidas

---

### QUESTÃO 13
Um administrador de sistemas configura uma política de controle de acesso para um repositório de documentos confidenciais. A política determina que a concessão de acesso depende da combinação da função do usuário (Engenharia), do local de acesso (Rede Interna) e do horário (08:00 às 18:00). Se o usuário tentar acessar fora desse horário, o acesso é bloqueado automaticamente. Qual modelo de controle de acesso está em uso?

A) Discretionary Access Control (DAC)
B) Mandatory Access Control (MAC)
C) Role-Based Access Control (RBAC)
D) Attribute-Based Access Control (ABAC)

---

### QUESTÃO 14
Uma equipe de SOC precisa correlacionar alertas provenientes de antimalware de endpoints, logs de firewalls e acessos a servidores Web. A ferramenta utilizada armazena os logs centralizadamente, analisa eventos em tempo real usando regras de correlação e gera alertas unificados para os analistas. Qual plataforma realiza essa função?

A) SIEM (Security Information and Event Management)
B) EDR (Endpoint Detection and Response)
C) CASB (Cloud Access Security Broker)
D) DLP (Data Loss Prevention)

---

### QUESTÃO 15
Um analista de segurança cibernética recebe um alerta de que um servidor web Linux apresentou comportamento anômalo. Ao analisar os logs do sistema, o analista observa que um comando malicioso foi injetado através de uma aplicação Web e executou com privilégios de `root` porque o processo da aplicação estava rodando sob a conta de superusuário. Qual medida de hardening deveria ter sido aplicada para mitigar essa vulnerabilidade?

A) Desabilitar a interface de rede secundária do servidor.
B) Aplicar o princípio do Menor Privilégio, executando o serviço da aplicação sob uma conta dedicada de baixo privilégio.
C) Habilitar criptografia de disco completo (FDE) no volume raiz.
D) Alterar a porta padrão do serviço SSH de 22 para 2222.

---

### QUESTÃO 16
Uma organização financeira quer garantir que conexões remota de administradores via SSH para servidores críticos exijam a presença de duas pessoas para aprovação prévia, além de gravar em vídeo todas as sessões executadas. Qual solução é especificamente projetada para fornecer essa capacidade de auditoria e controle?

A) Bastion Host simples com autenticação de chave pública
B) Privileged Access Management (PAM) com gravação de sessão e controle de aprovação
C) Multi-Factor Authentication (MFA) baseado em SMS
D) Network Access Control (NAC) baseado em postura de dispositivo

---

### QUESTÃO 17
Um analista de forense digital está examinando o tráfego de rede capturado durante uma invasão e deseja identificar os fluxos de comunicação (IP de origem, IP de destino, porta de origem, porta de destino e quantidade de bytes) entre os hosts sem precisar inspecionar o conteúdo dos pacotes. Qual tipo de dado de rede deve ser analisado?

A) Registros de Logs do Servidor Web (Nginx/Apache)
B) Registros NetFlow / IPFIX
C) Transcrições de Sessão TLS
D) Captura completa de pacotes com carga útil (Full Packet Capture com Payload)

---

### QUESTÃO 18
Uma empresa decide adotar o protocolo WPA3 em sua rede sem fio corporativa. Durante a migração, o administrador configura o WPA3-Enterprise. Qual protocolo subjacente de rede é exigido no servidor backend para realizar a autenticação centralizada dos dispositivos dos funcionários?

A) WEP
B) RADIUS / 802.1X
C) Pre-Shared Key (PSK)
D) WPS (Wi-Fi Protected Setup)

---

### QUESTÃO 19
Durante a análise de uma vulnerabilidade recém-divulgada (CVE), o analista de segurança consulta a pontuação CVSS v3.1 da ameaça. A métrica aponta que a exploração requer acesso físico local ao dispositivo e privilégios elevados de administrador. Como essas características impactam a avaliação de risco do servidor exposto diretamente na Internet?

A) Aumentam a criticidade do risco para Máxima, pois todo servidor na Internet está vulnerável a acessos físicos.
B) Reduzem a probabilidade de exploração remota direta pela Internet, pois a vulnerabilidade exige acesso local físico e credenciais administrativas.
C) Tornam a vulnerabilidade impossível de ser mitigada por qualquer controle compensatório.
D) Anulam a necessidade de aplicar qualquer patch de segurança no sistema operacional.

---

### QUESTÃO 20
Um analista de SOC nota que múltiplos e-mails de phishing foram entregues aos usuários porque os atacantes enviaram as mensagens utilizando um servidor de e-mail não autorizado que clonou o nome de domínio da empresa no campo "De:" (From). O analista verifica que o domínio possui um registro SPF no DNS, mas a política estava configurada como `v=spf1 ip4:192.168.1.0/24 ?all`. O que deve ser alterado no registro SPF para instruir os servidores de destino a rejeitar e-mails não autorizados?

A) Alterar a tag final `?all` (Neutral) para `-all` (Fail / Hard Fail).
B) Remover o endereço IP da rede interna do registro SPF.
C) Alterar o registro SPF de DNS para um registro CNAME apontando para o servidor Web.
D) Adicionar a tag `mx:all` no início do registro.

---

### QUESTÃO 21
Para evitar que funcionários conectem dispositivos USB pessoais (pendrives, HDs externos) nas estações de trabalho corporativas e vazem arquivos confidenciais ou introduzam malwares, qual controle de segurança de endpoint deve ser aplicado via política de grupo (GPO / MDM)?

A) Bloqueio / Desativação de Armazenamento Removível via Endpoint DLP ou GPO
B) Habilitação de Antivírus Baseado em Assinaturas
C) Instalação de Filtro de Conteúdo Web
D) Configuração de IP estático em todas as máquinas

---

### QUESTÃO 22
Uma empresa de desenvolvimento de software implementa uma ferramenta na esteira CI/CD que analisa o código-fonte em busca de falhas de segurança, chaves de API expostas em texto claro e bibliotecas desatualizadas sem precisar compilar ou executar a aplicação. Qual técnica de análise está sendo utilizada?

A) DAST (Dynamic Application Security Testing)
B) SAST (Static Application Security Testing)
C) Fuzzing / Teste de Ofuscação
D) Escaneamento de Penetração Ativo (Active Pentest)

---

### QUESTÃO 23
Uma equipe de resposta a incidentes concluiu a fase de contenção e erradicação de um ataque de malware que comprometeu três servidores de aplicação. Antes de colocar os servidores de volta ao ambiente de produção e reabrir o tráfego de usuários, qual etapa da resposta a incidentes deve ser executada?

A) Lições Aprendidas (Lessons Learned)
B) Recuperação / Restauração (Recovery)
C) Análise de Impacto no Negócio (BIA)
D) Preparação para Novos Ataques

---

### QUESTÃO 24
Um analista de segurança precisa configurar um gateway de e-mail seguro (SEG) para verificar se o e-mail recebido é autêntico. A política configurada exige validar o SPF e o DKIM, e definir a ação (como rejeitar ou colocar em quarentena) caso a validação falhe, além de enviar relatórios diários de agregação de falhas para a equipe de segurança. Qual registro DNS controla essa política global?

A) DMARC
B) PTR / Reverse DNS
C) MX (Mail Exchange)
D) CAA (Certification Authority Authorization)

---

### QUESTÃO 25
Durante a investigação de um incidente em um ambiente corporativo Windows, a equipe de SOC precisa determinar qual processo abriu uma conexão de rede suspeita enviando dados para um IP externo desconhecido. Qual comando de linha de comando nativo do Windows fornece a lista de conexões ativas associadas aos IDs dos processos executáveis (PID)?

A) `ping -a`
B) `netstat -ano`
C) `tracert -d`
D) `ipconfig /all`

---

### QUESTÃO 26
Uma empresa implementa um controle de acesso à rede (NAC) que avalia os computadores dos funcionários assim que eles se conectam à rede corporativa. Se a máquina não possuir o agente de antivírus atualizado ou se o patch do SO estiver pendente, o NAC redireciona a máquina para uma VLAN de quarentena isolada. Qual funcionalidade do NAC está sendo executada?

A) Análise de Postura / Checagem de Saúde (Posture Assessment / Health Check)
B) Autenticação Kerberos
C) Descriptografia SSL/TLS
D) Filtro de Pacotes Estateless

---

### QUESTÃO 27
Uma organização quer proteger seus dispositivos móveis corporativos (smartphones e tablets) fornecidos aos funcionários. A solução deve permitir limpar os dados corporativos remotamente em caso de perda ou roubo, impor senha forte de bloqueio e restringir a instalação de aplicativos não autorizados. Qual tecnologia atende a esses requisitos?

A) MDM (Mobile Device Management)
B) SIEM (Security Information and Event Management)
C) HSM (Hardware Security Module)
D) CASB (Cloud Access Security Broker)

---

### QUESTÃO 28
Um atacante envia uma grande quantidade de pacotes modificados para uma aplicação web, inserindo strings de caracteres aleatórios e malformados nos campos de entrada de formulários para forçar o travamento do sistema ou descobrir estouros de pilha (buffer overflow). Qual técnica de teste automatizado o atacante está simulando?

A) Fuzzing (Teste de Fuzz)
B) Análise Estática de Código (SAST)
C) Fingerprinting de Sistema Operacional
D) Captura de Banner (Banner Grabbing)

---

### QUESTÃO 29
Em uma arquitetura de segurança moderna, uma solução SOAR é implementada para automatizar o fluxo de resposta a incidentes. Quando o SIEM detecta uma tentativa comprovada de força bruta contra uma conta, o SOAR executa automaticamente um script predefinido que bloqueia a conta no Active Directory e isola o IP no firewall sem intervenção humana manual. Qual elemento do SOAR representa esse conjunto de ações automatizadas?

A) Playbook / Runbook
B) Regra de Correlação
C) Conector JDBC
D) Feed de Threat Intelligence

---

### QUESTÃO 30
Um perito forense é chamado para investigar um vazamento de informações sigilosas. Ao chegar ao local, ele identifica o computador do suspeito ligado e desbloqueado na mesa. Sabendo que dados voláteis armazenados na RAM e chaves de criptografia em uso podem ser perdidos se o sistema for desligado, qual deve ser a PRIMEIRA ação do perito?

A) Desconectar o cabo de energia da máquina para preservar o estado do disco.
B) Executar uma ferramenta de captura de memória RAM em tempo real (*live RAM capture*).
C) Reiniciar o computador em modo de segurança a partir de um pendrive bootável.
D) Formatar a partição de sistema para evitar que o malware se destrua.

---

### QUESTÃO 31
Uma organização deseja restringir o acesso a um portal financeiro crítico. O sistema exige que os usuários informem um nome de usuário, uma senha de conhecimento individual e um código temporário gerado por um aplicativo autenticador no smartphone (TOTP). Quais fatores de autenticação estão sendo combinados?

A) Dois fatores do tipo "Algo que você sabe" (Something you know).
B) "Algo que você sabe" (Senha) e "Algo que você possui" (Smartphone/Gerador TOTP).
C) "Algo que você sabe" e "Algo que você é" (Biometria).
D) "Algo que você possui" e "Onde você está" (Geolocalização).

---

### QUESTÃO 32
Um analista de SOC identifica um aumento anormal de tráfego de saída criptografado na porta TCP 443 vindo de uma estação de trabalho interna durante a madrugada. A máquina está enviando dados continuamente para um endereço IP sem reputação conhecida. Qual tipo de ameaça operacional esse comportamento sugere?

A) Ataque de Negação de Serviço Distribuído (DDoS) refletido
B) Exfiltração de Dados / Comunicação com Comando e Controle (C2)
C) Varredura de Portas SYN (SYN Flood)
D) Envenenamento de Cache ARP

---

### QUESTÃO 33
Para atender a requisitos regulatórios de privacidade, uma empresa precisa garantir que todos os dados de clientes armazenados em um banco de dados relacional em nuvem sejam legíveis apenas para a aplicação autorizada. Caso um atacante obtenha acesso direto aos arquivos de dados brutos (`.mdf`/`.db`) no disco rígido subjacente, os dados devem estar inacessíveis. Qual controle atende a essa necessidade?

A) Criptografia no Nível de Armazenamento / Transparent Data Encryption (TDE) ou FDE
B) Criptografia de Transporte TLS 1.3
C) Hashing de Senhas com Bcrypt
D) Mascaramento Dinâmico de Exibição de Tela

---

### QUESTÃO 34
Uma equipe de segurança realiza o descarte seguro de 50 servidores antigos que continham dados confidenciais de clientes. O gerente de segurança exige um método que garanta a destruição irrecuperável dos dados nos drives SSD sem danificar fisicamente os equipamentos, permitindo que os servidores sejam reaproveitados em ambientes de teste não críticos. Qual procedimento é recomendado?

A) Desmagnetização (Degaussing)
B) Apagamento Criptográfico (Cryptographic Erasure / Sanitização por Sobregravação Padrão NVMe/SATA)
C) Formatação Rápida (Quick Format) via Windows Explorer
D) Perfuração Física do Chassi (Drilling)

---

### QUESTÃO 35
Uma organização adota uma arquitetura de acesso remoto baseada em SSL-VPN. Antes de estabelecer o túnel criptografado, o gateway VPN verifica se o sistema operacional da máquina do usuário remoto está atualizado e se o firewall local está habilitado. Como é chamada essa verificação de pré-conexão realizada pelo cliente VPN?

A) Posture Assessment / Host Health Check
B) Network Mapping / Nmap Scan
C) Reverse DNS Lookup
D) Penetration Testing

---

### QUESTÃO 36
Após a identificação de uma intrusão em um servidor web, a equipe de forense precisa provar a custódia das evidências coletadas (logs de tráfego e imagem de disco). Qual documento deve conter o registro cronológico detalhado de quem coletou a evidência, quem a manuseou, a data/hora exata do manuseio e o motivo do acesso?

A) Documento de Resolução de Incidente (IRR)
B) Formulário de Cadeia de Custódia (Chain of Custody)
C) Acordo de Nível de Serviço (SLA)
D) Declaração de Aplicabilidade (SoA)

---

### QUESTÃO 37
Uma equipe de desenvolvimento Web deseja proteger sua aplicação contra ataques de Cross-Site Scripting (XSS) armazenado. Qual prática de codificação segura e controle de cabeçalho HTTP é mais eficaz para impedir a execução de scripts maliciosos injetados nos navegadores dos clientes?

A) Sanitização/Validação de Entrada e Cabeçalho Content Security Policy (CSP)
B) Desabilitar a porta 443 e utilizar HTTP na porta 80
C) Usar hashing MD5 nas URLs de navegação
D) Aumentar o tempo de expiração do cookie de sessão para 30 dias

---

### QUESTÃO 38
Um administrador de segurança configura um sistema EDR em todas as máquinas da empresa. O EDR detectou que o processo `powershell.exe` foi invocado por um documento do Word malicioso e tentou baixar um executável de um servidor externo. O EDR encerrou imediatamente o processo do PowerShell e isolou a máquina da rede. Esse tipo de ação automatizada no endpoint é classificado como:

A) Detecção e Resposta Automatizada de Endpoint (Active Response / Automated Isolation)
B) Varredura Passiva de Vulnerabilidades de Rede
C) Auditoria Manual de Logs de Sistema
D) Controle de Acesso Físico por Biometria

---

### QUESTÃO 39
Uma empresa deseja implementar autenticação de dois fatores (2FA) para acesso às suas aplicações SaaS em nuvem. No entanto, para mitigar o risco de ataques de interceptação do tipo Man-in-the-Middle (MitM) e Phishing em tempo real, a equipe decide banir o envio de códigos por SMS e senhas TOTP de 6 dígitos. Qual método de autenticação resistente a phishing (*Phishing-Resistant MFA*) deve ser adotado?

A) Envio de código via e-mail secundário
B) Chaves de Segurança Físicas baseadas no padrão FIDO2 / WebAuthn (ex: YubiKey)
C) Pergunta de segurança pessoal (ex: "Nome do seu primeiro pet")
D) Senhas estáticas de 16 caracteres armazenadas em bloco de notas

---

### QUESTÃO 40
Durante uma auditoria operacional de segurança, identifica-se que o arquivo de log de eventos de um firewall foi modificado e linhas de registros de log de determinado horário foram apagadas. Qual propriedade fundamental do sistema de gerenciamento de logs foi violada e qual controle deveria ter sido configurado para evitar isso?

A) A propriedade violada foi a Integridade; o controle correto é enviar os logs em tempo real para um servidor SIEM centralizado com permissões de gravação contínua e leitura restrita (WORM / Write Once Read Many).
B) A propriedade violada foi a Disponibilidade; o controle correto é aumentar o tamanho da memória RAM do firewall.
C) A propriedade violada foi a Confidencialidade; o controle correto é utilizar criptografia de disco FDE no firewall.
D) A propriedade violada foi o Não-Repúdio; o controle correto é reiniciar o firewall diariamente.

---
---

# 🎯 GABARITO OFICIAL E JUSTIFICATIVAS TÉCNICAS

---

#### QUESTÃO 1 — RESPOSTA CORRETA: B
* **Justificativa:** A PRIMEIRA ação ao confirmar uma infecção ativa por ransomware é a **Contenção / Isolamento do Host** da rede (desconectando o cabo ou alterando a VLAN). Isso impede que o malware se espalhe lateralmente e continue se comunicando com o servidor de Comando e Controle (C2).
* **Por que as outras estão incorretas?** 
  * A (Desligar a tomada) faz perder dados altamente voláteis armazenados na memória RAM (chaves de criptografia em memória, processos em execução) e viola a ordem de volatilidade.
  * C (Executar antivírus) e D (Restaurar backup) são etapas das fases de **Erradicação** e **Recuperação**, que só devem ocorrer após a contenção do incidente.

---

#### QUESTÃO 2 — RESPOSTA CORRETA: B
* **Justificativa:** De acordo com a **Ordem de Volatilidade** (RFC 3227 / CompTIA), a memória RAM dinâmica é extremamente volátil e seus dados são perdidos se o sistema for desligado ou reiniciado. Portanto, deve ser capturada antes de qualquer artefato armazenado em disco rígido.
* **Por que as outras estão incorretas?** Arquivos de paginação, MFT e Logs do Event Viewer estão gravados em mídia não volátil (disco) e possuem maior durabilidade em comparação à memória RAM.

---

#### QUESTÃO 3 — RESPOSTA CORRETA: A
* **Justificativa:** O protocolo **RADIUS** (Remote Authentication Dial-In User Service) é o padrão da indústria utilizado como servidor AAA backend para autenticação IEEE 802.1X em redes sem fio e cabeadas corporativas.
* **Por que as outras estão incorretas?** 
  * TACACS+ é um protocolo proprietário/amplamente usado para administração e controle de equipamentos de rede (roteadores/switches), utilizando TCP 49. No entanto, para autenticação 802.1X Wi-Fi de clientes, o RADIUS é o protocolo padrão exigido.
  * Kerberos e LDAP são protocolos de diretório e autenticação de domínio, mas não funcionam diretamente como o serviço AAA para o handshake 802.1X Wi-Fi.

---

#### QUESTÃO 4 — RESPOSTA CORRETA: B
* **Justificativa:** O **FIM (File Integrity Monitoring)** é a ferramenta específica para monitorar e alertar sobre alterações não autorizadas em arquivos críticos do sistema operacional, comparando seus hashes criptográficos atuais contra uma linha de base (*baseline*) conhecida.
* **Por que as outras estão incorretas?** 
  * DLP foca na prevenção de vazamento de dados sensíveis (ex: CPF, cartão de crédito).
  * NetFlow analisa métricas de tráfego de rede (IPs, portas, bytes).
  * UEBA analisa comportamentos anômalos de usuários e entidades.

---

#### QUESTÃO 5 — RESPOSTA CORRETA: B
* **Justificativa:** O **DKIM (DomainKeys Identified Mail)** adiciona uma assinatura digital aos cabeçalhos de e-mails enviados. O servidor receptor consulta a chave pública no DNS do domínio remetente para verificar a autenticidade e integridade da mensagem.
* **Por que as outras estão incorretas?** 
  * SPF apenas lista os endereços IP autorizados a enviar e-mails em nome do domínio.
  * DMARC utiliza o resultado do SPF e do DKIM para aplicar políticas (none, quarantine, reject).
  * STARTTLS é o comando de negociação para criptografar o canal SMTP.

---

#### QUESTÃO 6 — RESPOSTA CORRETA: B
* **Justificativa:** O **PAM (Privileged Access Management)** é a solução focada no gerenciamento, cofre de senhas, gravação de sessões, rotação automatizada de credenciais e auditoria de contas de alto privilégio (root, administrator, contas de serviço).
* **Por que as outras estão incorretas?** 
  * IAM gerencia o ciclo de vida e acesso de usuários comuns.
  * SSO permite autenticar uma única vez para acessar múltiplos sistemas.
  * SIEM centraliza logs para correlação de eventos de segurança.

---

#### QUESTÃO 7 — RESPOSTA CORRETA: B
* **Justificativa:** O **Escaneamento Credenciado (Credentialed Scan)** utiliza credenciais de acesso fornecidas ao scanner para se conectar diretamente ao sistema operacional do host. Isso permite inspecionar o registro local, atualizações instaladas e softwares sem gerar tráfego invasivo e eliminando falsos-positivos de portas.
* **Por que as outras estão incorretas?** Escaneamentos não credenciados tentam identificar vulnerabilidades apenas através da rede (portas abertas e banners visíveis externos), resultando em menor visibilidade interna e mais falsos-positivos.

---

#### QUESTÃO 8 — RESPOSTA CORRETA: B
* **Justificativa:** O uso de **Sandbox / Ambiente Isolado** permite a execução detonada e análise dinâmica de arquivos, anexos e URLs maliciosos em um sistema virtual descartável para observar seu comportamento real sem arriscar a rede de produção.
* **Por que as outras estão incorretas?** Filtros estáticos, listas de bloqueio e reputação de DNS não conseguem detectar ameaças inéditas (Zero-Day) ou links dinâmicos e camuflados.

---

#### QUESTÃO 9 — RESPOSTA CORRETA: B
* **Justificativa:** O cálculo e comparação do **Hash Criptográfico (ex: SHA-256)** entre a mídia original e a cópia gerada, devidamente registrado na **Cadeia de Custódia**, prova matematicamente a integridade da evidência digital para admissibilidade jurídica.
* **Por que as outras estão incorretas?** Criptografar a cópia não prova que ela é idêntica ao original; formatar a mídia original destrói a evidência primária.

---

#### QUESTÃO 10 — RESPOSTA CORRETA: B
* **Justificativa:** O **Write Blocker (Bloqueador de Escrita)** é um dispositivo de hardware ou driver especializado que intercepta e bloqueia fisicamente/logicamente qualquer comando de escrita enviado ao disco investigado, garantindo que nenhum metadado ou arquivo seja alterado durante a análise.
* **Por que as outras estão incorretas?** HSM é para gerenciamento de chaves; TPM é o chip de criptografia de plataforma local; NAC é para controle de acesso à rede.

---

#### QUESTÃO 11 — RESPOSTA CORRETA: B
* **Justificativa:** No protocolo SAML, o servidor da organização que autentica o usuário e emite a afirmação XML de identidade (*SAML Assertion*) é o **Identity Provider (IdP)**. O serviço em nuvem que confia no IdP é o *Service Provider (SP)*.
* **Por que as outras estão incorretas?** Service Provider é a aplicação final (SaaS); Relying Party é a nomenclatura equivalente no ecossistema OAuth/OIDC.

---

#### QUESTÃO 12 — RESPOSTA CORRETA: C
* **Justificativa:** A fase de **Erradicação (Eradication)** envolve a remoção definitiva do malware do ambiente, a limpeza de artefatos maliciosos (registros, tarefas agendadas) e a aplicação de patches e correções para fechar a vulnerabilidade explorada.
* **Por que as outras estão incorretas?** Contenção visa isolar e conter a disseminação da ameaça; Recuperação (Recovery) envolve restaurar os sistemas de volta para o ambiente de produção; Lições Aprendidas analisa o evento pós-incidente.

---

#### QUESTÃO 13 — RESPOSTA CORRETA: D
* **Justificativa:** O **ABAC (Attribute-Based Access Control)** avalia atributos dinâmicos do sujeito (função), do recurso (nível de sensibilidade) e do ambiente (horário, localização geográfica, IP) para tomar decisões de acesso granulares.
* **Por que as outras estão incorretas?** 
  * DAC baseia-se na discrição do proprietário do recurso.
  * MAC baseia-se em rótulos de segurança (Top Secret).
  * RBAC baseia-se estritamente na função/papel do usuário, sem avaliar contexto ambiental dinâmico como horário.

---

#### QUESTÃO 14 — RESPOSTA CORRETA: A
* **Justificativa:** O **SIEM (Security Information and Event Management)** é a plataforma responsável pela agregação centralizada de logs, análise e correlação em tempo real de eventos de segurança de múltiplas fontes e geração de alertas.
* **Por que as outras estão incorretas?** EDR atua apenas nos endpoints; CASB monitora tráfego para a nuvem; DLP previne vazamento de dados confidenciais.

---

#### QUESTÃO 15 — RESPOSTA CORRETA: B
* **Justificativa:** Pelo princípio do **Menor Privilégio**, serviços e aplicações Web NUNCA devem ser executados sob a conta `root` ou `Administrator`. Devem utilizar contas de serviço dedicadas com permissões restritas apenas ao diretório da aplicação.
* **Por que as outras estão incorretas?** Desabilitar interfaces secundárias, usar FDE ou alterar porta SSH não impedem a execução de comandos remotos de uma aplicação mal configurada executando como root.

---

#### QUESTÃO 16 — RESPOSTA CORRETA: B
* **Justificativa:** As soluções de **PAM (Privileged Access Management)** oferecem recursos avançados de "Dual Control" / aprovação de acesso por terceiros e **gravação completa em vídeo das sessões administrativas** para auditoria de compliance.
* **Por que as outras estão incorretas?** Bastion hosts simples e MFA não fornecem workflow de aprovação por duas pessoas ou gravação em vídeo das ações do usuário.

---

#### QUESTÃO 17 — RESPOSTA CORRETA: B
* **Justificativa:** O **NetFlow / IPFIX** fornece metadados de tráfego de rede (5-tuple: IP de origem, IP de destino, porta de origem, porta de destino e protocolo), além da quantidade de pacotes e bytes transferidos, sem armazenar o conteúdo do payload.
* **Por que as outras estão incorretas?** Captura completa de pacotes armazena o payload inteiro (muito mais pesado); logs de servidor web cobrem apenas conexões HTTP/HTTPS direcionadas àquele servidor.

---

#### QUESTÃO 18 — RESPOSTA CORRETA: B
* **Justificativa:** O **WPA3-Enterprise** exige a infraestrutura de autenticação **IEEE 802.1X**, utilizando um servidor **RADIUS** backend acoplado a um repositório de identidades (como Active Directory).
* **Por que as outras estão incorretas?** PSK (Pre-Shared Key) é utilizado no modo WPA3-Personal (que utiliza SAE); WEP é obsoleto e inseguro; WPS é vulnerável a ataques de força bruta e desativado em redes corporativas.

---

#### QUESTÃO 19 — RESPOSTA CORRETA: B
* **Justificativa:** As métricas do CVSS v3.1 *Attack Vector: Local* e *Privileges Required: High* indicam que um atacante precisa de acesso físico ao host e credenciais de administrador já comprometidas para explorar a falha. Isso reduz a probabilidade de um ataque remoto direto vindo da Internet.
* **Por que as outras estão incorretas?** Ter um servidor na Internet não dá acesso físico local ao equipamento; vulnerabilidades locais podem ser mitigadas por controles de acesso físico e IAM.

---

#### QUESTÃO 20 — RESPOSTA CORRETA: A
* **Justificativa:** A tag `?all` indica um resultado "Neutral" (o servidor de destino não toma ação agressiva). Para instruir os servidores de e-mail destinatários a rejeitar (Hard Fail) mensagens enviadas por IPs fora do bloco especificado, a tag deve ser alterada para **`-all`**.
* **Por que as outras estão incorretas?** Remover os IPs torna o registro inútil; alterar para CNAME invalida a sintaxe SPF; `mx:all` não é a instrução de bloqueio da política.

---

#### QUESTÃO 21 — RESPOSTA CORRETA: A
* **Justificativa:** O **bloqueio de portas/dispositivos de armazenamento removível** via Endpoint DLP, soluções de gerenciamento MDM ou diretivas de grupo (GPO) impede fisicamente/logicamente a montagem de pendrives e mídias USB não autorizadas.
* **Por que as outras estão incorretas?** Antivírus e filtros Web não impedem a cópia direta de arquivos corporativos para um pendrive.

---

#### QUESTÃO 22 — RESPOSTA CORRETA: B
* **Justificativa:** O **SAST (Static Application Security Testing)** analisa o código-fonte em repouso ("white-box") sem a necessidade de compilar ou executar o programa, identificando padrões de código inseguros e credenciais expostas.
* **Por que as outras estão incorretas?** DAST exige a aplicação rodando em execução; Fuzzing injeta dados aleatórios na aplicação em tempo de execução.

---

#### QUESTÃO 23 — RESPOSTA CORRETA: B
* **Justificativa:** A fase de **Recuperação (Recovery)** ocorre logo após a erradicação. Nela, os sistemas são restaurados a partir de backups limpos, validados, testados e reconectados gradualmente ao ambiente de produção sob monitoramento ostensivo.
* **Por que as outras estão incorretas?** Lições aprendidas é a fase FINAL do ciclo de resposta a incidentes, realizada após a restauração completa da operação.

---

#### QUESTÃO 24 — RESPOSTA CORRETA: A
* **Justificativa:** O **DMARC (Domain-based Message Authentication, Reporting, and Conformance)** utiliza as validações do SPF e DKIM para definir a política de alinhamento e ação (none, quarantine, reject) e solicitar o envio de relatórios de agregações (rua/ruf).
* **Por que as outras estão incorretas?** MX aponta para os servidores de correio; PTR faz a resolução reversa de IP; CAA define quais CAs podem emitir certificados TLS para o domínio.

---

#### QUESTÃO 25 — RESPOSTA CORRETA: B
* **Justificativa:** O comando `netstat -ano` exibe todas as conexões TCP/UDP ativas, portas de escuta, endereços IP remotos e a coluna **PID (Process Identifier)** que identifica qual processo gerou a conexão no Windows.
* **Por que as outras estão incorretas?** `ping` testa conectividade ICMP; `tracert` mapeia rota de rede; `ipconfig` exibe dados das interfaces de rede locais.

---

#### QUESTÃO 26 — RESPOSTA CORRETA: A
* **Justificativa:** A **Análise de Postura (Posture Assessment / Health Check)** do NAC é o processo que verifica a conformidade da estação (versão do SO, presença de patches, status do antivírus e firewall) antes de autorizar o acesso à rede principal.
* **Por que as outras estão incorretas?** Kerberos é para autenticação de domínio; SSL/TLS é criptografia de transporte; Stateless é filtragem simples de pacote.

---

#### QUESTÃO 27 — RESPOSTA CORRETA: A
* **Justificativa:** As soluções de **MDM (Mobile Device Management)** oferecem gerenciamento centralizado de smartphones e tablets, permitindo aplicar políticas de segurança, criptografia, restrição de aplicativos e **wipe remoto** de dados.
* **Por que as outras estão incorretas?** SIEM é para logs; HSM é para chaves criptográficas; CASB é para visibilidade e controle de aplicações em nuvem.

---

#### QUESTÃO 28 — RESPOSTA CORRETA: A
* **Justificativa:** O **Fuzzing (ou Fuzz Testing)** é uma técnica automatizada de teste de software que envia dados aleatórios, malformados ou inválidos para as entradas da aplicação para provocar falhas, travamentos ou estouros de memória.
* **Por que as outras estão incorretas?** SAST analisa código estático sem executar o software; Fingerprinting identifica o SO; Banner Grabbing identifica versões de serviços através da rede.

---

#### QUESTÃO 29 — RESPOSTA CORRETA: A
* **Justificativa:** Um **Playbook (ou Runbook)** no contexto de SOAR é a codificação automatizada de um fluxo de resposta a incidentes que define a sequência de ações a serem tomadas pelas ferramentas sem necessidade de ação humana manual.
* **Por que as outras estão incorretas?** Regras de correlação ficam no SIEM para gerar alertas; Conectores JDBC fazem integração com bancos de dados.

---

#### QUESTÃO 30 — RESPOSTA CORRETA: B
* **Justificativa:** Se a máquina investigada estiver **ligada e desbloqueada**, a PRIMEIRA ação do perito forense deve ser a captura **ao vivo da memória RAM (Live RAM Capture)** para preservar conteúdos voláteis (chaves de criptografia de disco, conexões de rede ativas e malware rodando exclusivamente na memória).
* **Por que as outras estão incorretas?** Desconectar a tomada apaga todo o conteúdo da RAM; reiniciar o computador limpa a memória e pode alterar metadados nos discos.

---

#### QUESTÃO 31 — RESPOSTA CORRETA: B
* **Justificativa:** Senha é "Algo que você sabe" (Knowledge Factor); o smartphone/aplicativo autenticador gerador do código TOTP é "Algo que você possui" (Possession Factor). A combinação de fatores de categorias diferentes caracteriza a autenticação de múltiplos fatores (MFA).
* **Por que as outras estão incorretas?** Senha e código TOTP não pertencem à mesma categoria; não há biometria ("algo que você é") nem geolocalização envolvidas.

---

#### QUESTÃO 32 — RESPOSTA CORRETA: B
* **Justificativa:** Tráfego de saída constante, criptografado e fora do horário comercial enviado para um IP externo atípico indica forte suspeita de **Exfiltração de Dados** ou comunicação do host infectado com um servidor de **Comando e Controle (C2)** do atacante.
* **Por que as outras estão incorretas?** DDoS refletido ataca a vítima recebendo tráfego massivo de terceiros; SYN Flood é um ataque de negação de serviço de entrada no handshake TCP.

---

#### QUESTÃO 33 — RESPOSTA CORRETA: A
* **Justificativa:** A **Criptografia Transparente de Dados (TDE)** ou a Criptografia de Disco Completo (FDE) garante que os arquivos de dados brutos e backups do banco de dados no nível de armazenamento estejam totalmente criptografados em repouso (*Data at Rest*).
* **Por que as outras estão incorretas?** TLS protege dados em trânsito pela rede; Bcrypt é para hashing de senhas; Mascaramento apenas oculta dados na interface do usuário.

---

#### QUESTÃO 34 — RESPOSTA CORRETA: B
* **Justificativa:** Discos SSD e unidades flash NVMe utilizam memórias semicondutoras e não aceitam desmagnetização (degaussing). Para sanitizar SSDs com segurança mantendo o hardware funcional, utiliza-se o **Apagamento Criptográfico (Cryptographic Erasure / Sobregravação Padrão NVMe/SATA)**.
* **Por que as outras estão incorretas?** Degaussing só funciona em mídias magnéticas (HDDs/fitas); Formatação rápida apenas remove os ponteiros do sistema de arquivos, deixando os dados intactos e recuperáveis; Perfuração física destrói o chassi e impede o reuso.

---

#### QUESTÃO 35 — RESPOSTA CORRETA: A
* **Justificativa:** A verificação de **Posture Assessment / Host Health Check** realizada pelo cliente VPN checa a saúde e conformidade da máquina remota antes de autorizar o estabelecimento do túnel na rede corporativa.
* **Por que as outras estão incorretas?** Nmap scan é uma varredura de portas; Reverse DNS resolve IP para nome; Pentest é uma simulação de ataque.

---

#### QUESTÃO 36 — RESPOSTA CORRETA: B
* **Justificativa:** O formulário de **Cadeia de Custódia (Chain of Custody)** é o documento legal e pericial obrigatório que rastreia a posse, custódia, controle, transferência e análise de evidências digitais do início da coleta até o julgamento.
* **Por que as outras estão incorretas?** IRR é o relatório interno pós-incidente; SLA é contrato de nível de serviço; SoA é a declaração de aplicabilidade da ISO 27001.

---

#### QUESTÃO 37 — RESPOSTA CORRETA: A
* **Justificativa:** Para mitigar XSS, a prática recomendada de desenvolvimento é a **sanitização/validação rigorosa de entradas e saídas**, aliada ao uso do cabeçalho de resposta HTTP **Content Security Policy (CSP)**, que restringe quais scripts o navegador pode executar.
* **Por que as outras estão incorretas?** Usar HTTP desprotegido expõe os dados em texto claro; MD5 nas URLs não impede injeção de scripts; aumentar a expiração de cookies agrava o risco de sequestro de sessão.

---

#### QUESTÃO 38 — RESPOSTA CORRETA: A
* **Justificativa:** As soluções de EDR (Endpoint Detection and Response) com recurso de **Resposta Ativa / Isolamento Automatizado** conseguem identificar o encadeamento de processos maliciosos e encerrar os processos envolvidos e isolar o host da rede de forma imediata.
* **Por que as outras estão incorretas?** Varreduras passivas de rede e auditorias manuais não conseguem bloquear o ataque de forma ativa e automatizada no endpoint em tempo real.

---

#### QUESTÃO 39 — RESPOSTA CORRETA: B
* **Justificativa:** O padrão **FIDO2 / WebAuthn** utilizando chaves de segurança físicas de hardware (como YubiKeys) utiliza criptografia de chave pública alinhada ao domínio específico da aplicação, tornando-a **imune e resistente a Phishing e interceptação de proxies MitM**.
* **Por que as outras estão incorretas?** SMS, e-mails secundários e códigos TOTP de 6 dígitos são vulneráveis a ataques de engenharia social, interceptação de SIM Swap e proxies reversos de phishing (como Evilginx).

---

#### QUESTÃO 40 — RESPOSTA CORRETA: A
* **Justificativa:** A alteração ou exclusão não autorizada de registros de log viola a **Integridade**. O controle adequado para mitigar esse risco é o envio imediato e centralizado dos eventos para um **SIEM / Repositório WORM (Write Once, Read Many)**, impedindo que administradores locais apaguem seus vestígios no host.
* **Por que as outras estão incorretas?** Apagar registros de log não é falha de disponibilidade ou confidencialidade; reiniciar o firewall ou aumentar a memória RAM não impede a edição não autorizada dos logs locais.

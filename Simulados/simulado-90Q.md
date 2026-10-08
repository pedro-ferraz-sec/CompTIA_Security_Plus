# 📝 Simulado Impresso Completo - CompTIA Security+ SY0-701 (90 Questões)

> **Instruções:** Responda às 90 questões situacionais abaixo sem consultar o gabarito. As alternativas estão todas desmarcadas. O gabarito oficial com as justificativas técnicas encontra-se consolidado ao final deste documento.

---

## 📋 Questões (1 a 90)

### Questão 1
Durante uma auditoria interna em um banco de dados financeiro, descobriu-se que registros de transações antigas foram modificados sem autorização por uma conta de serviço comprometida. Qual princípio fundamental da tríade CIA foi diretamente violado?
- A) Confidencialidade
- B) Integridade
- C) Disponibilidade
- D) Não Repúdio

### Questão 2
Uma organização de saúde está implementando uma arquitetura Confiança Zero (*Zero Trust* - NIST SP 800-207). Em qual componente dessa arquitetura ocorre a decisão lógica de conceder ou negar o acesso de um usuário a um recurso específico?
- A) Ponto de Aplicação de Políticas (*Policy Enforcement Point* - PEP)
- B) Mecanismo de Política (*Policy Engine*)
- C) Administrador de Políticas (*Policy Administrator*)
- D) Gateway de Fronteira (*Border Gateway*)

### Questão 3
Qual componente da arquitetura Confiança Zero (*Zero Trust*) é responsável por executar e aplicar fisicamente a decisão de permitir ou bloquear o tráfego de conexão em direção ao recurso?
- A) Mecanismo de Política (*Policy Engine*)
- B) Ponto de Aplicação de Políticas (*Policy Enforcement Point* - PEP)
- C) Administrador de Políticas (*Policy Administrator*)
- D) Servidor de Identidade de Domínio

### Questão 4
Um analista de segurança precisa calcular a Expectativa de Perda Anualizada (*ALE*) para um servidor Web de e-commerce avaliado em $ 200.000. Sabendo que o Fator de Exposição (*EF*) para inundações é de 30% e que a Taxa Anual de Ocorrência (*ARO*) é de 0,1 (uma vez a cada 10 anos), qual é a *ALE*?
- A) $ 6.000
- B) $ 20.000
- C) $ 60.000
- D) $ 600.000

### Questão 5
Um analista de segurança analisa alertas e percebe que uma ferramenta maliciosa está escutando passivamente o tráfego de uma rede local para extrair credenciais enviadas em texto claro sem alterar os pacotes. Qual técnica de ataque está sendo executada?
- A) Ataque On-path (*Man-in-the-Middle*)
- B) *Sniffing* de Rede
- C) Envenenamento de Cache ARP
- D) *Password Spraying*

### Questão 6
Um engenheiro de redes configura um firewall de borda para bloquear todo o tráfego de entrada por padrão, liberando apenas portas especificamente autorizadas. Qual princípio de segurança está sendo aplicado nessa regra final?
- A) Menor Privilégio
- B) Negação Implícita (*Implicit Deny*)
- C) Separação de Deveres
- D) Defesa em Profundidade

### Questão 7
Dentro de uma infraestrutura de Rede Definida por Software (*Software-Defined Networking* - SDN), qual camada é responsável por tomar as decisões lógicas de roteamento e aplicar políticas globais de segurança?
- A) Plano de Dados (*Data Plane*)
- B) Plano de Controle (*Control Plane*)
- C) Plano de Aplicação (*Application Plane*)
- D) Plano Físico (*Physical Plane*)

### Questão 8
Um atacante tenta autenticar em uma empresa testando poucas senhas muito comuns (como "Senha123!" e "Mudar2024") contra centenas de contas de usuários diferentes, alternando IPs a cada tentativa. Qual técnica de ataque é essa?
- A) *Credential Stuffing*
- B) Ataque de Força Bruta Direta
- C) *Password Spraying*
- D) *Dictionary Attack* em Hash

### Questão 9
Qual é a vantagem primária da implementação de um sistema de Orquestração, Automação e Resposta de Segurança (*SOAR*) em relação à simples automação de tarefas isoladas em um SOC?
- A) Elimina 100% dos analistas humanos de Nível 1 e Nível 2.
- B) Integra e coordena múltiplos fluxos de trabalho e ferramentas heterogêneas de forma centralizada.
- C) Garante que nenhum falso positivo seja gerado pelo SIEM.
- D) Substitui a necessidade de ter um firewall de aplicação Web (WAF).

### Questão 10
Uma grande corporação contrata uma auditoria externa para obter um relatório que ateste a eficácia operacional contínua dos seus controles de segurança ao longo de um período de 6 meses. Qual relatório deve ser solicitado?
- A) SOC 1 Type I
- B) SOC 2 Type I
- C) SOC 2 Type II
- D) SOC 3 Type I

### Questão 11
Para impedir que respostas falsas de nomes de domínio sejam aceitas pelos clientes e evitar o envenenamento de cache, um administrador ativa o protocolo DNSSEC. Como o DNSSEC garante essa proteção?
- A) Criptografando todo o tráfego de consulta DNS com TLS na porta 853.
- B) Utilizando assinaturas digitais e criptografia assimétrica para autenticar a origem e a integridade das respostas DNS.
- C) Bloqueando consultas DNS vindas de endereços IP externos.
- D) Substituindo registros A por registros CNAME criptografados.

### Questão 12
Qual papel na governança de dados é responsável pela conformidade legal, nível de sensibilidade e regras de classificação de um determinado conjunto de dados de negócios?
- A) Custodiante dos Dados (*Data Custodian*)
- B) Encarregado de Proteção de Dados (*DPO*)
- C) Proprietário dos Dados (*Data Owner*)
- D) Engenheiro de Processamento de Dados

### Questão 13
Qual profissional é responsável por aplicar operacionalmente os controles técnicos de segurança, backups, permissões de arquivo e manutenção do armazenamento definido pelo proprietário do dado?
- A) Proprietário dos Dados (*Data Owner*)
- B) Custodiante dos Dados (*Data Custodian*)
- C) Controlador de Dados (*Data Controller*)
- D) Gestor de Riscos Corporativos

### Questão 14
Durante uma investigação de incidente de *ransomware*, a equipe de SOC decide isolar a máquina infectada da rede local mantendo o computador ligado na tomada. Qual é o motivo primordial para não desligar a máquina imediatamente?
- A) Evitar a perda de arquivos de log salvos no disco rígido.
- B) Preservar a memória RAM e as conexões de rede ativas para análise forense (ordem de volatilidade).
- C) Permitir que o antivírus remova o malware automaticamente.
- D) Garantir que o backup em nuvem continue sendo sincronizado.

### Questão 15
Qual propriedade criptográfica garante que, mesmo que a chave privada de um servidor seja comprometida no futuro, o atacante não conseguirá descriptografar as sessões TLS passadas que capturou na rede?
- A) Confidencialidade Perfeita para Frente (*Perfect Forward Secrecy* - PFS)
- B) Grapeamento OCSP (*OCSP Stapling*)
- C) Assinatura Digital RSA-4096
- D) Hashing com Salting (*Key Stretching*)

### Questão 16
Como o recurso de *OCSP Stapling* melhora a eficiência e a privacidade no processo de validação de certificados digitais TLS?
- A) Faz com que o navegador do cliente consulte a CA diretamente via HTTPS para cada conexão.
- B) O próprio servidor Web consulta periodicamente a CA, obtém o status assinado e o anexa (*staple*) no *handshake* TLS enviado ao cliente.
- C) Exige que a Lista de Certificados Revogados (CRL) seja baixada inteiramente pelo cliente a cada 24 horas.
- D) Substitui a necessidade de autoridade certificadora na árvore de confiança.

### Questão 17
Qual é a diferença fundamental de arquitetura física entre o módulo criptográfico TPM (*Trusted Platform Module*) e o HSM (*Hardware Security Module*)?
- A) O TPM é um equipamento de rede centralizado, enquanto o HSM é um software instalado no SO.
- B) O TPM é um chip criptográfico integrado/soldado à placa-mãe do dispositivo local, enquanto o HSM é um appliance dedicado e centralizado para gerenciamento em alta escala.
- C) O TPM lida apenas com chaves simétricas, enquanto o HSM processa exclusivamente hash MD5.
- D) Não há diferença; ambos são termos sinônimos para cartões inteligentes USB.

### Questão 18
Em um processo de resposta a incidentes de segurança, qual é a etapa oficial que vem imediatamente *após* a Contenção bem-sucedida da ameaça?
- A) Preparação
- B) Erradicação
- C) Recuperação
- D) Lições Aprendidas

### Questão 19
Um atacante consegue alterar a memória RAM de um processo legítimo e confiável do sistema operacional (como `svchost.exe`), esvaziando seu código original e injetando um código malicioso sem criar novos arquivos no disco. Qual é o nome dessa técnica de evasão?
- A) Injeção de SQL (*SQLi*)
- B) *Process Hollowing*
- C) *Cross-Site Scripting* (XSS)
- D) *Buffer Overflow* de Pilha

### Questão 20
Um executivo sênior (*CFO*) de uma empresa recebe um e-mail falso altamente personalizado, aparentando vir do Conselho de Administração, solicitando uma transferência bancária urgente. Como se classifica este tipo específico de engenharia social?
- A) *Phishing* Genérico
- B) *Spear Phishing*
- C) *Whaling*
- D) *Vishing*

### Questão 21
Qual mecanismo de controle de rede é instalado na borda de um ambiente para filtrar requisições de saída dos usuários internos navegando na Internet?
- A) *Reverse Proxy*
- B) *Forward Proxy*
- C) Balanceador de Carga de Aplicação
- D) Firewall de Aplicação Web (WAF)

### Questão 22
Um administrador de sistemas deseja proteger os servidores Web internos da empresa contra ataques externos e balancear a carga de entrada do tráfego vindo da Internet. Qual solução de arquitetura deve ser implementada à frente dos servidores?
- A) *Forward Proxy*
- B) *Reverse Proxy*
- C) Servidor DHCP
- D) Gateway de E-mail Seguro (SEG)

### Questão 23
Uma política de segurança exige que funcionários da equipe financeira alternem periodicamente de funções e tirem licenças/férias de pelo menos uma semana contínua por ano. Qual é a principal finalidade dessa medida de controle de RH?
- A) Reduzir os custos com horas extras de funcionários.
- B) Detectar e expor fraudes ou atividades não autorizadas contínuas que seriam ocultadas pelo operador titular.
- C) Garantir que todos os funcionários aprendam a programar.
- D) Aumentar a velocidade de processamento de dados.

### Questão 24
Antes de enviar a chave pública para uma Autoridade Certificadora (CA) assinar e emitir um certificado TLS, o administrador de rede deve gerar qual arquivo de solicitação padrão?
- A) Lista de Revogação de Certificados (CRL)
- B) Solicitação de Assinatura de Certificado (*Certificate Signing Request* - CSR)
- C) Registro de Par de Chaves (KPR)
- D) Arquivo de Resposta OCSP

### Questão 25
Qual modelo de contratação em nuvem transfere para o provedor a responsabilidade completa sobre a infraestrutura física, virtualização, sistema operacional e aplicação, cabendo ao cliente apenas o controle e a gestão dos dados e acessos?
- A) *Infrastructure as a Service* (IaaS)
- B) *Platform as a Service* (PaaS)
- C) *Software as a Service* (SaaS)
- D) *Function as a Service* (FaaS)

### Questão 26
No modelo de nuvem *Platform as a Service* (PaaS), qual camada da pilha de tecnologia fica sob a responsabilidade de gerenciamento e manutenção do cliente?
- A) Hardware físico e fiação de rede.
- B) Camada de virtualização (*Hypervisor*).
- C) Sistema Operacional e *Middleware*.
- D) Código da Aplicação e Dados do Usuário.

### Questão 27
Qual é a principal vantagem de governança e operação obtida ao adotar a abordagem de Infraestrutura como Código (*Infrastructure as Code* - IaC)?
- A) Eliminação da necessidade de usar firewalls em servidores.
- B) Automação de ambientes padronizados, auditáveis e imutáveis, eliminando o desvio de configuração (*configuration drift*).
- C) Redução do tamanho das senhas de administrador para 4 dígitos.
- D) Permissão para que qualquer usuário instale softwares sem aprovação.

### Questão 28
Uma organização instala um equipamento físico de *Hardware Write Blocker* em seu laboratório de perícia digital antes de conectar o disco rígido apreendido em um incidente. Qual é o objetivo primário desse dispositivo?
- A) Criptografar o disco de origem com algoritmo AES-256.
- B) Impedir fisicamente qualquer gravação, alteração ou escrita de dados no disco original durante a duplicação bit a bit.
- C) Acelerar a velocidade de leitura do disco em até 10 vezes.
- D) Apagar automaticamente os vírus contidos na mídia.

### Questão 29
Em um exame forense digital, qual é a Ordem de Volatilidade correta para coleta de evidências na memória, do item *mais volátil* para o *menos volátil*?
- A) Disco rígido local -> Memória RAM -> Registradores da CPU -> Backups em fita.
- B) Registradores/Cache da CPU -> Memória RAM -> Tabela de Processos/Rede -> Disco rígido -> Mídias de backup.
- C) Backups em fita -> Disco rígido -> Memória RAM -> Registradores da CPU.
- D) Logs do servidor SIEM -> Memória RAM -> Registradores da CPU -> Disco rígido.

### Questão 30
Uma equipe de segurança instala um ponto de acesso sem fio falso nas imediações de uma cafeteria corporativa, configurando o mesmo nome de SSID ("Empresa_Guest") e canal de rede da empresa para capturar o tráfego dos funcionários. Como se classifica esse ataque?
- A) *Rogue AP*
- B) *Evil Twin*
- C) *Bluejacking*
- D) *War Driving*

### Questão 31
O que diferencia tecnicamente um *Rogue AP* de um *Evil Twin*?
- A) O *Rogue AP* utiliza obrigatoriamente criptografia WPA3, enquanto o *Evil Twin* não usa senha.
- B) O *Rogue AP* é um dispositivo físico não autorizado conectado à rede interna sem clonar necessariamente um SSID; o *Evil Twin* clona o SSID e atributos de um AP legítimo para enganar os clientes.
- C) O *Evil Twin* ataca apenas conexões via cabo Ethernet.
- D) Não há diferença técnica; ambos se referem estritamente a ataques de Bluetooth.

### Questão 32
Um analista de segurança executa uma ferramenta automatizada que envia dados aleatórios, malformados e inválidos continuamente para os campos de entrada de uma aplicação Web até provocar seu travamento. Qual técnica de teste de segurança está sendo usada?
- A) Análise Estática de Código (SAST)
- B) Teste de *Fuzzing* (*Fuzz Testing*)
- C) Revisão Manual de Código
- D) Escaneamento de Portas Passivo

### Questão 33
Uma solução de Controle de Acesso à Rede (NAC) verifica se o notebook de um funcionário possui a versão mais recente do antivírus e os patches do sistema operacional aplicados antes de liberar o acesso à rede corporativa. Qual recurso do NAC está sendo utilizado?
- A) *Posture Assessment* (Avaliação de Postura)
- B) Detecção de Intrusão em Redes (NIDS)
- C) Inspeção Profunda de Pacotes (DPI)
- D) Análise de Vulnerabilidade Sem Credenciais

### Questão 34
Qual é a vantagem principal de executar um escaneamento de vulnerabilidades utilizando um *Credentialed Scan* (Escaneamento Credenciado) em comparação com um escaneamento sem credenciais?
- A) Exige menos largura de banda e consome zero memória no scanner.
- B) Reduz falsos positivos e fornece uma visão profunda dos patches, registros e arquivos internos instalados no host.
- C) Garante que a rede fique imune a ataques de *DoS*.
- D) Não exige permissão da equipe de segurança para ser executado.

### Questão 35
Qual norma do NIST estabelece as diretrizes padrão para a Arquitetura Confiança Zero (*Zero Trust Architecture*)?
- A) NIST SP 800-53
- B) NIST SP 800-207
- C) NIST SP 800-37
- D) NIST Cybersecurity Framework (CSF)

### Questão 36
Um ataque cibernético compromete a integridade do arquivo de resolução de nomes local de uma estação de trabalho (`hosts`), fazendo com que o acesso ao site `banco.com` seja direcionado para o IP de um servidor malicioso. Qual ataque ocorreu?
- A) Envenenamento de Cache ARP
- B) *DNS Poisoning* / Alteração de Arquivo *Hosts*
- C) *MAC Flooding*
- D) *SQL Injection*

### Questão 37
Ao tentar ler dados sensíveis emitidos por uma máquina de criptografia, um atacante mede as variações de consumo de energia e as emanações eletromagnéticas do hardware durante o processamento de chaves. Qual tipo de ataque é este?
- A) Ataque de Canal Lateral (*Side-channel Attack*)
- B) Ataque de Análise de Pincelada
- C) *Fault Injection* por Software
- D) Engenharia Reversa de Binário

### Questão 38
Qual termo descreve a prática de diversificar os fornecedores de sistemas operacionais, firewalls e softwares em uma infraestrutura corporativa para evitar que uma única vulnerabilidade de dia zero derrube 100% do ambiente?
- A) Redundância de Hardware
- B) Diversidade de Plataformas (*Platform Diversity*)
- C) Ofuscação de Código
- D) Alta Disponibilidade Ativo-Passivo

### Questão 39
Uma empresa deseja estabelecer uma parceria comercial com um fornecedor e assina um documento formal que descreve as intenções gerais de cooperação e objetivos comuns, mas sem criar obrigações financeiras ou contratuais vinculantes rígidas. Qual documento é esse?
- A) Acordo de Nível de Serviço (*SLA*)
- B) Memorando de Entendimento (*MOU*)
- C) Acordo de Não Divulgação (*NDA*)
- D) Declaração de Trabalho (*SOW*)

### Questão 40
Durante a investigação de um ataque em uma rede Wi-Fi corporativa baseada no padrão 802.1X, o analista confirma que o servidor de autenticação central utilizado para validar os certificados EAP-TLS é o:
- A) Servidor DHCP
- B) Servidor RADIUS
- C) Servidor DNS
- D) Servidor Proxy HTTP

### Questão 41
Em qual situação a autenticação via protocolo *EAP-TLS* se destaca em segurança em relação ao *EAP-TTLS*?
- A) O EAP-TLS exige certificado digital apenas no servidor, dispensando certificados nos clientes.
- B) O EAP-TLS exige autenticação mútua com certificados digitais válidos instalados tanto no servidor quanto em cada dispositivo cliente.
- C) O EAP-TLS não utiliza criptografia na camada de transporte.
- D) O EAP-TLS é projetado exclusivamente para redes cabeadas antigas de 10 Mbps.

### Questão 42
Um analista avalia o sistema CVSSv3 de uma vulnerabilidade e observa a métrica *Privileges Required* (PR) definida como *High*. O que isso significa?
- A) O atacante não precisa de nenhuma conta no sistema para explorar a falha.
- B) O atacante precisa possuir privilégios administrativos ou de alto nível no sistema antes de conseguir explorar a falha.
- C) A vulnerabilidade só pode ser explorada via conexão Bluetooth.
- D) O impacto da falha afetará apenas usuários convidados (*guests*).

### Questão 43
Um invasor caminha logo atrás de um funcionário autorizado e passa pela catraca da empresa aproveitando que a porta física ficou aberta, sem apresentar o crachá. Qual é o nome dessa técnica de invasão física?
- A) *Shoulder Surfing*
- B) *Tailgating* / *Piggybacking*
- C) *Baiting*
- D) *Dumpster Diving*

### Questão 44
Uma empresa adota uma solução que fica posicionada entre os usuários locais e os serviços de nuvem contratados (como Office 365 e Salesforce) para monitorar atividades, aplicar DLP e impor políticas de segurança na nuvem. Qual é essa solução?
- A) *Web Application Firewall* (WAF)
- B) *Cloud Access Security Broker* (CASB)
- C) *Virtual Private Network* (VPN)
- D) *Next-Generation Router*

### Questão 45
Um usuário recebe uma ligação telefônica de um indivíduo que se identifica como técnico do suporte de TI da empresa, solicitando a senha da rede para "atualizar o sistema". Qual ataque de engenharia social ocorreu?
- A) *Phishing*
- B) *Vishing*
- C) *Smishing*
- D) *Whaling*

### Questão 46
Um atacante deixa vários pendrives infectados espalhados pelo estacionamento de uma empresa, contendo etiquetas chamativas como "Folha de Pagamento - Confidencial", esperando que um funcionário o conecte a um computador interno. Como se chama essa técnica?
- A) *Watering Hole*
- B) *Baiting* (Iscagem)
- C) *Pretexting*
- D) *Typosquatting*

### Questão 47
Em um contrato de segurança da informação com um provedor de nuvem, qual cláusula define os tempos máximos aceitáveis para resposta a incidentes e as métricas de disponibilidade (*uptime*) garantidas?
- A) Acordo de Não Divulgação (*NDA*)
- B) Acordo de Nível de Serviço (*SLA*)
- C) Regras de Engajamento (*RoE*)
- D) Memorando de Acordo (*MOA*)

### Questão 48
Antes de contratar um novo fornecedor de SaaS que processará dados financeiros da empresa, a equipe de segurança realiza uma análise minuciosa de seus controles internos, histórico e políticas de segurança. Como é chamado esse processo prévio?
- A) *Due Diligence* (Devida Diligência)
- B) *Due Care* (Devido Cuidado)
- C) Resposta a Incidentes
- D) Teste de Aceitação do Usuário (UAT)

### Questão 49
Qual termo descreve a obrigação contínua e a responsabilidade legal de uma organização em manter os controles de segurança funcionando adequadamente no dia a dia para proteger os dados sob sua guarda?
- A) *Due Diligence*
- B) *Due Care* (Devido Cuidado)
- C) Governança Descentralizada
- D) Isenção de Responsabilidade

### Questão 50
Uma empresa precisa manter uma infraestrutura secundária pronta para disaster recovery, onde os equipamentos e conexões de rede já estão instalados, mas os dados mais recentes precisam ser restaurados a partir de backups antes de iniciar as operações. Qual é o tipo desse local de recuperação?
- A) *Cold Site*
- B) *Warm Site*
- C) *Hot Site*
- D) *Mobile Site*

### Questão 51
O que caracteriza um *Hot Site* no contexto de continuidade de negócios?
- A) Um galpão vazio apenas com energia elétrica e ar condicionado.
- B) Um local totalmente equipado, com hardware operando e dados sincronizados em tempo real, pronto para assumir a operação em minutos.
- C) Um servidor instalado no porão da matriz.
- D) Um contrato exclusivo para aluguel de computadores em caso de crise.

### Questão 52
Um administrador de banco de dados cria uma tabela em que o número de cartão de crédito `4532 1123 8890 1234` é armazenado e exibido na tela como `4532 XXXX XXXX 1234`. Qual técnica de proteção de dados foi aplicada?
- A) Criptografia Homomórfica
- B) Mascaramento de Dados (*Data Masking*)
- C) Esteganografia
- D) Hashing com Salt

### Questão 53
Como a Tokenização protege dados sensíveis (como números de cartão de pagamento) durante o armazenamento?
- A) Aplicando um algoritmo de cifra reversível usando a mesma chave do usuário.
- B) Substituindo o dado sensível por um valor aleatório sem significado matemático (token) mantido em um cofre de tokens isolado e seguro.
- C) Compactando o arquivo em formato `.zip` com senha.
- D) Ocultando os dados dentro de um arquivo de imagem JPEG.

### Questão 54
Para garantir a privacidade dos dados de saúde em um ambiente de pesquisa, o analista remove totalmente qualquer identificador direto ou indireto (nome, CPF, data de nascimento) que possa reidentificar o paciente. Qual técnica é essa?
- A) Anonimização de Dados
- B) Pseudonimização
- C) Codificação Base64
- D) Ofuscação de Código fonte

### Questão 55
A Pseudonimização difere da Anonimização porque:
- A) A Pseudonimização é irreversível em qualquer circunstância.
- B) A Pseudonimização substitui identificadores por pseudônimos, mantendo a capacidade de reidentificar o indivíduo se informações adicionais mantidas separadamente forem utilizadas.
- C) A Pseudonimização só se aplica a arquivos de áudio.
- D) A Anonimização exige o pagamento de licenças de software.

### Questão 56
Em uma arquitetura SASE (*Secure Access Service Edge*), quais dois conceitos primários de TI e segurança são convergidos em uma plataforma unificada entregue via nuvem?
- A) Servidores DNS e Bancos de Dados SQL.
- B) Capacidades de Rede de Longa Distância (*SD-WAN*) e Serviços de Segurança de Rede (*CASB, SWG, ZTNA*).
- C) Antivírus tradicional e Backups em fita.
- D) Processamento Gráfico (GPU) e Armazenamento SAN.

### Questão 57
Qual tipo de firewall inspeciona o tráfego com base nas sessões ativas e no estado das conexões de rede, bloqueando pacotes que não pertencem a uma conexão conhecida?
- A) Firewall Sem Estado (*Stateless Firewall*)
- B) Firewall Com Estado (*Stateful Firewall*)
- C) Filtro de Pacotes Simples de Camada 3
- D) Roteador Não Gerenciável

### Questão 58
Um analista precisa identificar a presença de malware em um endpoint verificando modificações não autorizadas em arquivos críticos do sistema operacional (`C:\Windows\System32`). Qual ferramenta realiza essa verificação contínua?
- A) Monitor de Integridade de Arquivos (*File Integrity Monitoring* - FIM)
- B) Servidor DHCP
- C) Balanceador de Carga
- D) Gerenciador de Senhas

### Questão 59
Para evitar que e-mails falsificados utilizando o domínio da empresa (`@empresa.com`) sejam entregues a clientes, o administrador configura os registros DNS SPF, DKIM e DMARC. Qual é a função do registro DMARC?
- A) Criptografar o corpo das mensagens de e-mail com PGP.
- B) Definir as ações e políticas (rejeitar, quarentena ou aceitar) que os servidores de destino devem tomar caso a autenticação SPF ou DKIM falhe.
- C) Aumentar o limite de tamanho de anexos para 100 MB.
- D) Criar contas de e-mail automaticamente para novos contratados.

### Questão 60
O protocolo WPA3-Enterprise utiliza qual padrão de cifra simétrica e tamanho de chave padrão para garantir segurança robusta nas redes sem fio corporativas?
- A) DES com chaves de 56 bits
- B) AES com GCMP-256 / CCMP-128
- C) RC4 de 128 bits
- D) Blowfish de 64 bits

### Questão 61
Qual método de autenticação sem fio no WPA3-Personal substitui o PSK (*Pre-Shared Key*) tradicional para proteger contra ataques de dicionário offline e garantir troca de chaves segura?
- A) Autenticação Simultânea de Iguais (*Simultaneous Authentication of Equals* - SAE)
- B) WEP de 64 bits
- C) Captive Portal com formulário HTTP
- D) WPS por código PIN

### Questão 62
Um analista de resposta a incidentes precisa garantir a Cadeia de Custódia (*Chain of Custody*) de uma evidência digital extraída de um servidor. Qual procedimento é essencial?
- A) Guardar a mídia na gaveta do analista sem anotações para evitar vazamentos.
- B) Documentar cronologicamente todos os responsáveis pelo manuseio da evidência, datas, locais e hashes de verificação de integridade.
- C) Formatar a mídia antes de apresentá-la em juízo.
- D) Alterar a data de modificação dos arquivos para a data atual.

### Questão 63
Qual métrica de gerenciamento de riscos quantifica o tempo máximo tolerável que uma organização pode suportar com um sistema fora do ar após um desastre antes de sofrer prejuízos inaceitáveis?
- A) Ponto Objetivo de Recuperação (*Recovery Point Objective* - RPO)
- B) Tempo Objetivo de Recuperação (*Recovery Time Objective* - RTO)
- C) Tempo Médio Entre Falhas (*MTBF*)
- D) Fator de Exposição (*EF*)

### Questão 64
A métrica RPO (*Recovery Point Objective*) está diretamente relacionada com qual decisão de infraestrutura corporativa?
- A) O número de monitores na sala de operações do SOC.
- B) A frequência com que os backups de dados devem ser executados e a quantidade de dados que a empresa aceita perder.
- C) A velocidade do processador do servidor.
- D) O tempo de resposta do suporte do fornecedor de hardware.

### Questão 65
Um analista configura o sistema de registro de eventos (logging) para enviar todos os eventos dos servidores para um servidor centralizado usando o protocolo Syslog. Qual é a porta padrão UDP não criptografada e a porta TCP criptografada (TLS) do Syslog?
- A) UDP 53 / TCP 443
- B) UDP 514 / TCP 6514
- C) UDP 80 / TCP 8080
- D) UDP 161 / TCP 162

### Questão 66
Qual modelo de controle de acesso se baseia em rótulos de segurança e níveis de confidencialidade (*Top Secret, Secret, Unclassified*) atribuídos tanto aos sujeitos quanto aos objetos, sendo controlado estritamente pelo sistema?
- A) Controle de Acesso Discricionário (DAC)
- B) Controle de Acesso Mandatório (MAC)
- C) Controle de Acesso Baseado em Funções (RBAC)
- D) Controle de Acesso Baseado em Regras (RBAC-Rules)

### Questão 67
Um administrador concede acesso a um pasta da rede atribuindo usuários a grupos como "Financeiro_Leitura" e "RH_Edicao". Qual modelo de controle de acesso está sendo aplicado?
- A) Controle de Acesso Mandatório (MAC)
- B) Controle de Acesso Baseado em Funções (*Role-Based Access Control* - RBAC)
- C) Controle de Acesso Baseado em Atributos (ABAC)
- D) Controle de Acesso Físico

### Questão 68
Qual modelo de controle de acesso avalia variáveis contextuais como localização do usuário, horário do acesso, tipo de dispositivo e endereço IP antes de conceder permissão?
- A) Controle de Acesso Discricionário (DAC)
- B) Controle de Acesso Baseado em Atributos (*Attribute-Based Access Control* - ABAC)
- C) Controle de Acesso por Lista Rígida
- D) Controle de Acesso por Senha Única

### Questão 69
Um atacante envia uma mensagem de e-mail contendo um link malicioso que aparenta ser do banco da empresa. Ao clicar no link enquanto está autenticado no site real do banco em outra aba, o navegador do usuário executa uma transferência bancária não autorizada sem o seu conhecimento. Qual é o nome desse ataque?
- A) *Cross-Site Scripting* (XSS)
- B) *Cross-Site Request Forgery* (CSRF)
- C) Injeção de Comando de Sistema
- D) *Insecure Direct Object Reference* (IDOR)

### Questão 70
O ataque de *Cross-Site Scripting* (XSS) explora primariamente a falta de validação de entrada de dados para injetar e executar scripts maliciosos (como JavaScript) em qual local?
- A) No banco de dados do servidor backend.
- B) No navegador do cliente/usuário final que visualiza a página.
- C) No firmware do roteador de borda.
- D) Na memória RAM do firewall de rede.

### Questão 71
Qual protocolo de autenticação corporativa é utilizado em ambientes Active Directory para permitir Single Sign-On (SSO) seguro baseado em bilhetes (*tickets*) criptografados e na porta TCP/UDP 88?
- A) NTLMv1
- B) Kerberos
- C) RADIUS
- D) TACACS+

### Questão 72
O protocolo TACACS+ se diferencia do RADIUS principalmente por:
- A) Utilizar UDP e combinar autenticação e autorização no mesmo pacote.
- B) Utilizar TCP (porta 49) e criptografar todo o corpo do pacote de comunicação (autenticação, autorização e contabilização separadamente).
- C) Não suportar criptografia.
- D) Ser um protocolo aberto e exclusivo para redes de sensores IoT.

### Questão 73
Uma empresa adota o padrão SAML 2.0 para permitir que seus funcionários acessem aplicações em nuvem terceirizadas usando suas credenciais corporativas internas. Qual é a função da empresa nesse fluxo de federação?
- A) Provedor de Serviços (*Service Provider* - SP)
- B) Provedor de Identidade (*Identity Provider* - IdP)
- C) Autoridade Certificadora
- D) Servidor Proxy Reverso

### Questão 74
No protocolo OAuth 2.0, qual é o artefato emitido após a autorização do usuário que concede ao aplicativo de terceiros acesso a recursos específicos em seu nome?
- A) Certificado X.509
- B) Token de Acesso (*Access Token* - Bearer/JWT)
- C) Ticket TGT do Kerberos
- D) Senha em texto claro

### Questão 75
Um hacker utiliza um scanner de portas e identifica a porta TCP 22 aberta em um servidor de produção. Qual serviço seguro está em execução nessa porta?
- A) Telnet
- B) Secure Shell (SSH)
- C) FTP Inseguro
- D) RDP (Remote Desktop)

### Questão 76
Qual porta padrão TCP é utilizada pelo protocolo RDP (*Remote Desktop Protocol*) para conexões de área de trabalho remota no Windows?
- A) 22
- B) 3389
- C) 443
- D) 8080

### Questão 77
Qual é o objetivo principal de uma simulação de segurança do tipo *Tabletop Exercise* (Exercício de Mesa)?
- A) Testar o tempo de resposta de um firewall contra um ataque de negação de serviço de 10 Gbps.
- B) Reunir equipes de liderança e resposta a incidentes em uma sala de reunião para discutir e validar cenários teóricos de crise e procedimentos sem interromper as operações reais.
- C) Formatar os servidores de produção para testar a restauração de backups.
- D) Contratar hackers éticos para invadir fisicamente o prédio.

### Questão 78
Uma organização contrata um teste de invasão (*Pentest*) na modalidade *Black Box* (Caixa Preta). O que isso significa para a equipe de pentesters?
- A) Eles recebem o código fonte completo e diagramas de arquitetura detalhados do sistema.
- B) Eles não recebem nenhuma informação prévia ou conhecimento interno sobre a infraestrutura da empresa alvo.
- C) Eles trabalham juntamente com os administradores de rede compartilhando senhas de root.
- D) O teste só pode ser realizado no período noturno.

### Questão 79
Qual é a característica de um Pentest na modalidade *White Box* (Caixa Branca)?
- A) O testador possui conhecimento total e acesso prévio a documentações, código fonte e diagramas do ambiente.
- B) O testador deve invadir o ambiente sem usar computadores.
- C) O cliente não sabe que o teste está acontecendo.
- D) O teste é focado apenas na segurança física do estacionamento.

### Questão 80
Em um exercício de equipe de segurança (*Red Team vs. Blue Team*), qual é o papel desempenhado pela *Purple Team*?
- A) Atuar como a auditoria externa financeira da empresa.
- B) Facilitar a cooperação, integração e compartilhamento contínuo de inteligência entre a equipe de ataque (*Red Team*) e a equipe de defesa (*Blue Team*).
- C) Gerenciar os contratos com fornecedores de hardware.
- D) Desligar os servidores caso um ataque ocorra.

### Questão 81
Durante o gerenciamento de incidentes, o que é uma retenção legal (*Legal Hold*)?
- A) A proibição de contratar novos funcionários durante a investigação.
- B) Uma ordem que exige a preservação e não destruição de todos os dados, logs e documentos relevantes que possam servir como evidência em processos judiciais.
- C) O bloqueio imediato das contas bancárias da empresa.
- D) A obrigação de publicar os detalhes do incidente nos jornais.

### Questão 82
Um administrador precisa garantir que um aplicativo web legado continue funcionando, mas ele utiliza criptografia fraca que não pode ser atualizada diretamente no código. Ele instala um dispositivo que intercepta o tráfego e aplica criptografia forte TLS antes do envio. Qual tipo de controle de segurança foi aplicado?
- A) Controle Deterrente
- B) Controle Compensatório
- C) Controle Corretivo
- D) Controle Físico

### Questão 83
Qual das seguintes opções representa um exemplo clássico de Controle de Segurança do tipo *Deterrente* (*Deterrent*)?
- A) Placa de aviso visível com os dizeres "Sorria, você está sendo filmado - Área Monitorada".
- B) Sistema de Extinção de Incêndio por Gás FM-200.
- C) Backup diário em fita magnética.
- D) Firewall de inspeção profunda de pacotes.

### Questão 84
Um sistema de detecção de intrusões (IDS) gera um alerta indicando que um ataque de injeção de SQL ocorreu, mas após investigação do analista, confirma-se que a requisição tratava-se de uma busca legítima de um usuário válido. Como se classifica esse alerta?
- A) Verdadeiro Positivo
- B) Falso Positivo
- C) Falso Negativo
- D) Verdadeiro Negativo

### Questão 85
Qual é o resultado mais perigoso para a segurança de uma organização em um sistema de detecção de ameaças?
- A) Falso Positivo
- B) Falso Negativo (uma ameaça real ocorre e o sistema não detecta nem emite alertas)
- C) Verdadeiro Positivo
- D) Alerta de Carga Elevada de CPU

### Questão 86
Qual é o objetivo principal da fase de *Hardening* (Endurecimento) em um sistema operacional recém-instalado?
- A) Instalar jogos e aplicativos de entretenimento para os usuários.
- B) Reduzir a superfície de ataque desativando serviços desnecessários, fechar portas não utilizadas, alterar credenciais padrão e aplicar patches.
- C) Aumentar a velocidade do clock do processador (*Overclocking*).
- D) Liberar acesso de administrador para todos os usuários da rede.

### Questão 87
Um atacante consegue explorar uma vulnerabilidade de *Buffer Overflow* em um aplicativo compilado em C. O que causa tecnicamente essa vulnerabilidade?
- A) O programa não valida o tamanho do dado digitado pelo usuário antes de copiá-lo para um buffer de memória de tamanho fixo, sobrescrevendo posições adjacentes na pilha.
- B) O servidor ficou sem espaço em disco rígido.
- C) O cabo de rede foi desconectado durante a transferência.
- D) A senha do banco de dados era muito curta.

### Questão 88
Qual tipo de vulnerabilidade de software ocorre quando duas tarefas concorrentes tentam acessar e modificar o mesmo recurso de memória simultaneamente, e o resultado final depende de qual tarefa é executada primeiro?
- A) *SQL Injection*
- B) Condição de Corrida (*Race Condition* / TOC-TOU)
- C) *Cross-Site Scripting*
- D) Injeção de Formatação de String

### Questão 89
Uma empresa instala uma câmera de segurança com recurso de inteligência artificial que detecta e alerta a central quando uma pessoa não autorizada tenta pular o muro perimetral. Qual categoria e tipo de controle foram aplicados?
- A) Controle Físico e Detectivo
- B) Controle Lógico e Compensatório
- C) Controle Administrativo e Corretivo
- D) Controle Técnico e Diretivo

### Questão 90
Para mitigar o risco de vazamento de dados por exfiltração de arquivos sensíveis via pendrives ou anexos de e-mail não autorizados, a empresa instala um agente de software em todos os endpoints corporativos. Qual tecnologia de segurança foi implementada?
- A) *Prevenção contra Perda de Dados* (DLP - *Data Loss Prevention*)
- B) *Domain Name System* (DNS)
- C) *Network Address Translation* (NAT)
- D) *Network Time Protocol* (NTP)

---

## 🔑 Gabarito Oficial e Justificativas Técnicas

| Questão | Gabarito | Justificativa Técnica Breve |
| :---: | :---: | :--- |
| **1** | **B** | Modificação não autorizada de dados viola a **Integridade** (Confidencialidade refere-se a vazamento/acesso). |
| **2** | **B** | O **Policy Engine** é o cérebro que analisa o contexto e toma a decisão lógica de autorizar ou negar o acesso. |
| **3** | **B** | O **PEP (Policy Enforcement Point)** é quem aplica fisicamente o bloqueio/liberação da conexão no recurso. |
| **4** | **A** | $ALE = SLE 	imes ARO$. Onde $SLE = 200.000 	imes 0,30 = 60.000$. Então $ALE = 60.000 	imes 0,1 = \$ 6.000$. |
| **5** | **B** | Escutar o tráfego da rede passivamente em texto claro sem alterar os pacotes caracteriza o **Sniffing**. |
| **6** | **B** | Bloquear todo o tráfego por padrão e liberar apenas exceções é o princípio da **Negação Implícita (Implicit Deny)**. |
| **7** | **B** | O **Plano de Controle** da SDN centraliza as decisões lógicas de roteamento e aplicação de políticas. |
| **8** | **C** | **Password Spraying** testa poucas senhas comuns contra muitas contas para contornar bloqueios de conta. |
| **9** | **B** | O **SOAR** destaca-se por orquestrar fluxos de trabalho completos integrando ferramentas distintas. |
| **10** | **C** | O relatório **SOC 2 Type II** atesta a eficácia operacional contínua dos controles ao longo de um período. |
| **11** | **B** | **DNSSEC** adiciona assinaturas digitais assimétricas para garantir a autenticidade e integridade da resposta DNS. |
| **12** | **C** | O **Data Owner** possui a responsabilidade executiva/legal pela classificação e autorização do dado. |
| **13** | **B** | O **Data Custodian** é o responsável técnico por aplicar controles, backups e permissões indicadas pelo Owner. |
| **14** | **B** | Manter a máquina ligada isolada preserva a **RAM** (item altamente volátil) para investigação forense. |
| **15** | **A** | **PFS (Perfect Forward Secrecy)** usa chaves efêmeras para impedir a descriptografia de sessões passadas. |
| **16** | **B** | No **OCSP Stapling**, o servidor obtém o status assinado na CA e o anexa diretamente no handshake TLS. |
| **17** | **B** | O **TPM** é um chip soldado no dispositivo local; o **HSM** é um appliance de rede dedicado corporativo. |
| **18** | **B** | No ciclo oficial de incidentes, a **Erradicação** vem imediatamente após a fase de Contenção. |
| **19** | **B** | **Process Hollowing** substitui o código de um processo legítimo na RAM por payload malicioso sem arquivo no disco. |
| **20** | **C** | Ataques altamente direcionados a executivos do alto escalão (C-level) classificam-se como **Whaling**. |
| **21** | **B** | O **Forward Proxy** intercepta e filtra o tráfego de saída dos clientes internos para a Internet. |
| **22** | **B** | O **Reverse Proxy** fica à frente dos servidores internos protegendo e balanceando o tráfego de entrada. |
| **23** | **B** | **Férias Obrigatórias** forçam a saída temporária do operador para que fraudes contínuas venham à tona. |
| **24** | **B** | O arquivo **CSR (Certificate Signing Request)** contém a chave pública e dados para emissão do certificado na CA. |
| **25** | **C** | No **SaaS**, o provedor gerencia toda a infraestrutura e aplicação; o cliente gerencia apenas os dados e acessos. |
| **26** | **D** | No **PaaS**, a plataforma/SO é do provedor, cabendo ao cliente o código da **Aplicação e os Dados**. |
| **27** | **B** | **IaC** permite criar ambientes declarativos, auditáveis e imutáveis, evitando o desvio de configuração. |
| **28** | **B** | O **Write Blocker** impede qualquer gravação de dados na mídia original durante a clonagem bit a bit. |
| **29** | **B** | Ordem de volatilidade: Registradores/Cache -> RAM -> Tabela de Rede/Processos -> Disco -> Fitas de Backup. |
| **30** | **B** | Um AP falso clonando o nome de SSID e canal de uma rede legítima para enganar clientes é um **Evil Twin**. |
| **31** | **B** | **Rogue AP** é um AP físico não autorizado na rede interna; **Evil Twin** clona o SSID legítimo. |
| **32** | **B** | O envio automatizado de dados malformados/inválidos até causar travamento é a técnica de **Fuzzing**. |
| **33** | **A** | **Posture Assessment** no NAC checa antivírus e patches do dispositivo antes de conceder acesso. |
| **34** | **B** | O **Credentialed Scan** acessa registros/arquivos do host, reduzindo falsos positivos e aprofundando o teste. |
| **35** | **B** | O padrão do NIST para Arquitetura Confiança Zero (*Zero Trust Architecture*) é o **NIST SP 800-207**. |
| **36** | **B** | A alteração do arquivo `hosts` ou envenenamento de cache redireciona domínios legítimos para IPs falsos. |
| **37** | **A** | Medir consumo de energia e radiação eletromagnética do hardware é um **Ataque de Canal Lateral (Side-channel)**. |
| **38** | **B** | **Platform Diversity** evita que uma única vulnerabilidade de dia zero afete 100% da infraestrutura. |
| **39** | **B** | O **MOU (Memorandum of Understanding)** formaliza a cooperação geral sem obrigações financeiras vinculantes. |
| **40** | **B** | O servidor **RADIUS** realiza a autenticação centralizada do padrão 802.1X via EAP. |
| **41** | **B** | O **EAP-TLS** exige autenticação mútua com certificados digitais no servidor e também em cada cliente. |
| **42** | **B** | Métrica CVSS *Privileges Required: High* exige que o atacante já possua credenciais administrativas ativas. |
| **43** | **B** | Acolar-se fisicamente a um funcionário para entrar em área restrita sem crachá é **Tailgating / Piggybacking**. |
| **44** | **B** | O **CASB** atua entre a rede corporativa e os serviços em nuvem para impor DLP e políticas de acesso. |
| **45** | **B** | Engenharia social realizada via chamada de voz por telefone é classificada como **Vishing**. |
| **46** | **B** | Deixar pendrives infectados em locais públicos para atrair a curiosidade de funcionários é **Baiting (Iscagem)**. |
| **47** | **B** | O **SLA (Service Level Agreement)** formaliza métricas de disponibilidade e tempos de resposta a chamados. |
| **48** | **A** | **Due Diligence** é a análise e pesquisa prévia minuciosa antes de assinar contrato com um parceiro. |
| **49** | **B** | **Due Care** é a responsabilidade legal e operacional contínua de manter as proteções no dia a dia. |
| **50** | **B** | Um **Warm Site** possui equipamentos e conectividade prontos, mas exige restauração prévia de backups. |
| **51** | **B** | O **Hot Site** mantém hardware funcionando e dados sincronizados em tempo real para rápida alternância. |
| **52** | **B** | Ocultar partes de dados sensíveis para exibição segura é a técnica de **Mascaramento de Dados (Data Masking)**. |
| **53** | **B** | A **Tokenização** substitui o dado por um token sem valor matemático mantido em um cofre seguro. |
| **54** | **A** | A **Anonimização** remove de forma irreversível os identificadores de um indivíduo do conjunto de dados. |
| **55** | **B** | A **Pseudonimização** permite reidentificar o indivíduo se informações adicionais separadas forem usadas. |
| **56** | **B** | **SASE** converge funções de rede de longa distância (**SD-WAN**) e segurança na nuvem (**CASB, SWG, ZTNA**). |
| **57** | **B** | O **Stateful Firewall** monitora e valida o estado e a sessão ativa de cada conexão de rede. |
| **58** | **A** | Ferramentas de **FIM (File Integrity Monitoring)** detectam alterações não autorizadas em arquivos do SO. |
| **59** | **B** | O **DMARC** orienta os servidores de e-mail sobre o que fazer caso o alinhamento SPF ou DKIM falhe. |
| **60** | **B** | O WPA3-Enterprise utiliza cifra **AES** com algoritmos de alto desempenho **GCMP-256 / CCMP-128**. |
| **61** | **A** | O WPA3-Personal substitui o PSK pelo protocolo **SAE (Simultaneous Authentication of Equals)**. |
| **62** | **B** | A **Cadeia de Custódia** exige registro detalhado e cronológico de todos os manuseios e hashes da evidência. |
| **63** | **B** | **RTO (Recovery Time Objective)** representa o tempo máximo tolerável de inatividade do sistema. |
| **64** | **B** | O **RPO (Recovery Point Objective)** determina a tolerância à perda de dados e a frequência dos backups. |
| **65** | **B** | O protocolo Syslog opera na porta **UDP 514** (não criptografada) e **TCP 6514** (criptografada via TLS). |
| **66** | **B** | O **Controle de Acesso Mandatório (MAC)** baseia-se em rótulos do sistema (*Top Secret, Secret*). |
| **67** | **B** | **RBAC (Role-Based Access Control)** atribui permissões com base na função ou grupo do usuário. |
| **68** | **B** | O **ABAC (Attribute-Based Access Control)** avalia múltiplos atributos contextuais (IP, horário, local). |
| **69** | **B** | Forçar o navegador do usuário autenticado a executar uma ação involuntária em outro site é o **CSRF**. |
| **70** | **B** | O ataque de **Cross-Site Scripting (XSS)** executa scripts maliciosos no navegador da vítima (*client-side*). |
| **71** | **B** | O **Kerberos** utiliza bilhetes (*tickets*) criptografados e opera na porta TCP/UDP 88 para SSO em AD. |
| **72** | **B** | O **TACACS+** usa TCP 49 e criptografa 100% do corpo dos pacotes de autenticação e autorização. |
| **73** | **B** | Ao validar suas credenciais internas para liberar a nuvem, a empresa atua como **Provedor de Identidade (IdP)**. |
| **74** | **B** | No OAuth 2.0, o artefato retornado para autorizar a aplicação cliente é o **Access Token** (Bearer/JWT). |
| **75** | **B** | A porta TCP **22** é o padrão para conexões administrativas criptografadas via **SSH**. |
| **76** | **B** | O protocolo **RDP (Remote Desktop)** do Windows utiliza a porta TCP/UDP **3389**. |
| **77** | **B** | O **Tabletop Exercise** consiste em discutir cenários teóricos de crise em mesa sem afetar a produção. |
| **78** | **B** | No Pentest **Black Box**, a equipe de invasão não possui nenhum conhecimento prévio do ambiente alvo. |
| **79** | **A** | No Pentest **White Box**, os testadores possuem total acesso prévio a diagramas e código fonte. |
| **80** | **B** | O **Purple Team** existe para integrar e promover a colaboração entre o Red Team e o Blue Team. |
| **81** | **B** | A **Legal Hold (Retenção Legal)** determina a preservação rigorosa de logs e evidências para litígios. |
| **82** | **B** | O **Controle Compensatório** é uma alternativa implementada para suprir a impossibilidade do controle ideal. |
| **83** | **A** | Avisos e placas de monitoramento funcionam como **Controle Deterrente** para desestimular o atacante. |
| **84** | **B** | Um alerta gerado para uma atividade que na verdade era legítima é classificado como **Falso Positivo**. |
| **85** | **B** | O **Falso Negativo** é o pior cenário, pois uma invasão real ocorre sem que nenhum alarme seja disparado. |
| **86** | **B** | **Hardening** envolve desativar serviços, fechar portas e alterar padrões para reduzir a superfície de ataque. |
| **87** | **A** | O **Buffer Overflow** ocorre ao ultrapassar o limite de memória reservado para uma variável na pilha. |
| **88** | **B** | Falhas resultantes de acesso concorrente não sincronizado à memória são **Race Conditions (TOC-TOU)**. |
| **89** | **A** | Câmeras e sensores em muros perimetrais constituem controles da categoria **Física** e do tipo **Detectivo**. |
| **90** | **A** | Soluções de **DLP (Data Loss Prevention)** evitam o vazamento e exfiltração não autorizada de dados sensíveis. |

---

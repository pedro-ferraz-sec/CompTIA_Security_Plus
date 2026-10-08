# 🛠️ Simulado Prático Especial - 100 PBQs (Performance-Based Questions / Labs) - CompTIA Security+ SY0-701

**Instruções do Simulado:**
* Este documento reúne **100 Questões Baseadas em Desempenho (PBQs / Simulações Práticas / Labs)** no formato oficial exigido no exame CompTIA Security+ SY0-701.
* Todas as questões, logs, configurações e matrizes de associação estão no formato **desmarcado / não preenchido** para você exercitar na prática.
* O **Gabarito Oficial e a Resolução Técnica Detalhada** de todas as 100 questões estão localizados exclusivamente no final deste documento.

---

## 📝 PARTE 1: QUESTÕES E LABS PRÁTICOS (1 A 100)

### PBQ 1: Configuração de Regras de Firewall e ACL de Borda
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Uma empresa precisa liberar acesso externo seguro para sua sub-rede filtrada (DMZ) e impedir tráfego malicioso.
Servidores na DMZ:
- Servidor Web 1: 192.168.10.5 (HTTP/HTTPS)
- Servidor de E-mail: 192.168.10.10 (SMTP/IMAPS)
- Servidor SSH de Gerenciamento: 192.168.10.50 (SSH)
Rede Interna: 10.0.0.0/8 | Internet: Qualquer (0.0.0.0/0)

**Tabela de ACL para Preenchimento:**
| Regra | Origem | Destino | Porta/Protocolo | Ação |
| :---: | :---: | :---: | :---: | :---: |
| 1 | [ SELECIONAR ] | 192.168.10.5 | [ SELECIONAR ] | [ SELECIONAR ] |
| 2 | [ SELECIONAR ] | 192.168.10.10 | [ SELECIONAR ] | [ SELECIONAR ] |
| 3 | [ SELECIONAR ] | 192.168.10.50 | [ SELECIONAR ] | [ SELECIONAR ] |
| 4 | Qualquer | Qualquer | Qualquer | [ SELECIONAR ] |

**Sua Tarefa:**
Preencha a tabela de ACL seguindo o princípio do menor privilégio.

---

### PBQ 2: Componentes da Arquitetura Zero Trust (NIST SP 800-207)
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Mapeie os componentes da arquitetura Zero Trust com suas respectivas funções:
**Componentes:** 1. Policy Engine (PE) | 2. Policy Administrator (PA) | 3. Policy Enforcement Point (PEP) | 4. Control Plane | 5. Data Plane

**Funções:**
- [ A ] Ponto de tráfego onde transitam os dados reais de negócios da aplicação.
- [ B ] Tomador de decisão lógica baseado em regras e avaliação contínua de postura e contexto.
- [ C ] Ponto de aplicação de segurança que intercepta, abre e fecha conexões de rede.
- [ D ] Emissor de credenciais e comandos de sessão para estabelecer conexões autorizadas.
- [ E ] Plano de sinalização e controle onde trafegam as decisões de gerenciamento.

**Sua Tarefa:**
Associe os números às letras correspondentes.

---

### PBQ 3: Configuração de Redes Definidas por Software (SDN)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Um arquiteto de segurança está desenhando uma infraestrutura SDN. Associe os planos e funções aos seus elementos:

**Elementos:** 1. Plano de Controle | 2. Plano de Dados | 3. Controladores SDN | 4. Comutadores / Switches

**Matriz de Mapeamento:**
- [   ] Processa pacotes de acordo com as regras instaladas sem tomar decisões estratégicas.
- [   ] Toma decisões lógicas centrais de roteamento, políticas de firewall e qualidade de serviço.
- [   ] Dispositivo físico/virtual que executa o encaminhamento no Plano de Dados.
- [   ] Software centralizado que gerencia a inteligência da rede no Plano de Controle.

**Sua Tarefa:**
Complete a matriz associando os elementos corretos.

---

### PBQ 4: Implementação de SASE e SD-WAN
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Uma corporação com 50 filiais precisa migrar sua arquitetura legada baseada em MPLS para uma solução moderna de borda de serviço de segurança (SASE).

**Módulos de Arquitetura para Associação:**
A. SD-WAN | B. CASB | C. SWG (Secure Web Gateway) | D. ZTNA (Zero Trust Network Access) | E. FWaaS (Firewall as a Service)

**Cenários de Aplicação:**
1. Substituição de links MPLS caros por conexões de internet direta com roteamento dinâmico otimizado.
2. Inspecção de tráfego web de saída dos colaboradores para bloquear URLs maliciosas e malware.
3. Proteção e visibilidade de arquivos e dados armazenados em serviços SaaS de terceiros (como OneDrive/Google Drive).
4. Substituição da VPN cliente-servidor legada por acesso privado baseado no princípio do menor privilégio a aplicações específicas.
5. Inspecção centralizada de tráfego de rede corporativa na nuvem com prevenção de intrusão e filtragem de pacotes.

**Sua Tarefa:**
Associe a letra do módulo ao número do cenário correspondente.

---

### PBQ 5: Dimensionamento de Servidores Proxy: Forward vs. Reverse
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Determine se a arquitetura exige um **Forward Proxy** ou um **Reverse Proxy** para os seguintes cenários corporativos:

**Cenários:**
1. Filtragem do tráfego de navegação de saída dos funcionários para a Internet para aplicar políticas de uso aceitável (AUP).
2. Balanceamento de carga de requisições de clientes externos na Internet para uma fazenda de servidores Web internos.
3. Mascaramento dos endereços IP internos das estações de trabalho ao acessar sites na Web.
4. Descarregamento de criptografia TLS (SSL Offloading) antes que o tráfego atinja os servidores de aplicação internos.
5. Ocultação da topologia e estrutura interna dos servidores de banco de dados para usuários externos.

**Sua Tarefa:**
Classifique cada cenário como Forward Proxy ou Reverse Proxy.

---

### PBQ 6: Segregação de Rede e Microsegmentação
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Um banco precisa isolar o tráfego da rede para impedir a movimentação lateral (*Lateral Movement*).

**Zonas de Rede:** 1. Zona PCI-DSS | 2. Wi-Fi Visitantes | 3. Rede IoT/Câmeras | 4. Rede TI

**Mecanismo de Segurança Recomendado:**
- [ A ] VLAN isolada com acesso restrito via Jump Server e MFA obrigatório.
- [ B ] Microsegmentação por Software (Host-based Firewalls + SDN) isolando servidores no mesmo rack.
- [ C ] VLAN com Captive Portal e acesso exclusivo à Internet através de Gateway NAT isolado.
- [ D ] VLAN sem roteamento para outras sub-redes corporativas e bloqueio total de tráfego de entrada.

**Sua Tarefa:**
Mapeie cada Zona de Rede ao Mecanismo de Segurança correto.

---

### PBQ 7: Posicionamento de Sensores NIDS e NIPS
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Um analista precisa posicionar um NIDS passivo e um NIPS ativo no diagrama de rede.
- Posição 1: Em linha (*In-line*) entre o Firewall de Borda e o Comutador Principal.
- Posição 2: Conectado a uma porta de espelhamento (*SPAN / TAP*) no Comutador Principal.

**Perguntas:**
1. Qual dispositivo deve ser colocado na Posição 1 e por quê?
2. Qual dispositivo deve ser colocado na Posição 2 e por quê?
3. Qual o impacto de uma falha de hardware na Posição 1 se o equipamento não possuir modo *Bypass*?
4. Qual o impacto de um falso positivo na Posição 1 versus Posição 2?

**Sua Tarefa:**
Responda às 4 perguntas de arquitetura de IDS/IPS.

---

### PBQ 8: Configuração de Bastion Host / Jump Server
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Um administrador precisa aplicar hardening em um Jump Server utilizado para administrar servidores de banco de dados na nuvem.

**Lista de Configurações Recomendadas (Selecione SIM ou NÃO):**
1. [ SIM / NÃO ] Permitir conexões diretas via RDP/SSH da Internet pública para o Jump Server sem VPN.
2. [ SIM / NÃO ] Exigir Autenticação Multi-Fator (MFA) para todas as sessões de login no Jump Server.
3. [ SIM / NÃO ] Permitir o redirecionamento de área de transferência (Ctrl+C/Ctrl+V) e montagem de unidades locais.
4. [ SIM / NÃO ] Habilitar registro detalhado de auditoria de sessão com gravação de vídeo e logs enviados para SIEM imutável.
5. [ SIM / NÃO ] Permitir que usuários naveguem na Internet a partir do Jump Server.

**Sua Tarefa:**
Responda SIM ou NÃO para cada uma das 5 práticas de hardening do Jump Server.

---

### PBQ 9: Sistemas In-Band vs. Out-of-Band (OOB) Management
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Um centro de dados sofreu uma falha na tabela de roteamento dos switches principais, impedindo o acesso remoto pela rede local.

**Cenário de Diagnóstico:**
1. Qual método de gerenciamento teria permitido o acesso mesmo durante o colapso completo da rede corporativa? [ SELECIONAR: In-Band / Out-of-Band (OOB) ]
2. Qual meio físico/tecnologia é característico dessa solução de emergência? [ SELECIONAR: Interface SSH na VLAN 1 / Conexão Serial via Modem Celular 4G/5G / HTTPS no IP principal ]
3. Qual o principal requisito de segurança para proteger a interface OOB? [ SELECIONAR: Isolamento de rede físico ou lógico estrito sem rota para a Internet pública / Acesso livre sem senha ]

**Sua Tarefa:**
Selecione as opções corretas para os 3 itens do diagnóstico OOB.

---

### PBQ 10: Resiliência e Locais de Recuperação (Hot, Warm, Cold Site)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Mapeie o tipo de local de recuperação de desastres (Disaster Recovery Site) mais adequado:

**Opções:** A. Hot Site | B. Warm Site | C. Cold Site | D. Mobile Site

**Requisitos de Negócio:**
1. RTO próximo de zero (minutos/segundos) com dados sincronizados em tempo real e hardware/software idênticos.
2. Orçamento limitado e RTO de semanas, precisando apenas de espaço físico com energia, climatização e cabeamento.
3. RTO equilibrado (horas/dias), com equipamentos pré-configurados que exigem restauração de backup.
4. Infraestrutura temporária montada em um caminhão adaptado para atender uma agência destruída por incêndio.

**Sua Tarefa:**
Associe a letra do tipo de site ao número do requisito correspondente.

---

### PBQ 11: Escolha do Algoritmo Criptográfico e Modo de Operação
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Associe o requisito de segurança ao algoritmo ou conceito criptográfico ideal:
1. Criptografia simétrica de alta performance em hardware para dados em repouso com autenticação de integridade integrada.
2. Troca segura de chaves simétricas sobre um canal inseguro sem segredo pré-compartilhado.
3. Garantia de que o comprometimento futuro da chave privada não permitirá a decifragens de sessões TLS passadas.
4. Assinatura digital que garante autenticidade e não-repúdio.

Opções: (A) RSA/ECDSA (Chave Privada) | (B) AES-GCM | (C) Diffie-Hellman / ECDHE | (D) Perfect Forward Secrecy (PFS)

**Sua Tarefa:**
Associe a opção (A, B, C, D) a cada um dos 4 requisitos.

---

### PBQ 12: Hierarquia de Validação de Certificados: CRL vs. OCSP Stapling
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Identifique a tecnologia para cada cenário de verificação de revogação de certificados:
1. Cliente baixa um arquivo assinado contendo a lista de todos os certificados revogados pela CA. [ CRL / OCSP / OCSP Stapling ]
2. Cliente faz consulta direta em tempo real ao servidor da CA a cada conexão TLS, podendo vazar a navegação. [ CRL / OCSP / OCSP Stapling ]
3. O próprio servidor Web busca o status na CA e anexa a prova assinada diretamente no handshake TLS com o cliente. [ CRL / OCSP / OCSP Stapling ]

**Sua Tarefa:**
Informe a tecnologia para cada item.

---

### PBQ 13: Diferença entre Criptografia no Hardware: TPM vs. HSM
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Mapeie as características entre TPM e HSM:
1. Chip integrado à placa-mãe de laptops para armazenamento de chaves do BitLocker e validação do boot. [ TPM / HSM ]
2. Appliance de rede dedicado com proteção contra violação física para assinar milhares de transações financeiras. [ TPM / HSM ]
3. Utilizado localmente pelo SO para armazenar hashes e credenciais biométricas do usuário. [ TPM / HSM ]
4. Utilizado em bancos de dados corporativos na nuvem para aceleração criptográfica e gestão centralizada de chaves. [ TPM / HSM ]

**Sua Tarefa:**
Classifique cada item como TPM ou HSM.

---

### PBQ 14: Processo de Solicitação e Emissão de Certificado Digital (CSR & PKI)
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Ordene as etapas para obtenção de um certificado digital Web:
[ A ] A CA valida a identidade do solicitante e assina o certificado com sua Chave Privada.
[ B ] O administrador gera um par de chaves (Chave Pública e Chave Privada) no servidor local.
[ C ] O servidor Web instala o certificado e disponibiliza a Chave Pública no handshake TLS.
[ D ] O administrador cria um arquivo CSR contendo a Chave Pública e o envia para a CA.

**Sua Tarefa:**
Ordene as etapas de A a D na ordem cronológica (1ª a 4ª).

---

### PBQ 15: Proteção de Dados: Mascaramento, Tokenização e Salting
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Mapeie a técnica para a necessidade de proteção:
1. Mascaramento | 2. Tokenização | 3. Salting | 4. Esteganografia

- [   ] Adicionar valor aleatório único antes do hashing de uma senha para impedir ataques de tabela rainbow.
- [   ] Substituir o número do cartão de 16 dígitos por um valor aleatório mapeado em um cofre seguro (Vault).
- [   ] Ocultar uma mensagem secreta dentro do código de pixels de uma imagem digital PNG.
- [   ] Ocultar os primeiros 12 dígitos do CPF em telas de atendimento, exibindo apenas ***.***.123-45.

**Sua Tarefa:**
Associe os números das técnicas às descrições.

---

### PBQ 16: Formato e Extensões de Certificados Digitais
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Identifique o formato de arquivo para cada necessidade:
A. .PEM/.CRT | B. .PFX/.P12 (PKCS#12) | C. .DER | D. .P7B (PKCS#7)

1. Exportação do certificado digital junto com sua Chave Privada protegida por senha.
2. Formato codificado em ASCII Base64 delimitado por -----BEGIN CERTIFICATE-----.
3. Formato binário codificado em DER, comum em Java e embarcados.
4. Formato que contém apenas a cadeia de certificados sem conter a Chave Privada.

**Sua Tarefa:**
Associe as letras às descrições.

---

### PBQ 17: Sistemas de Arquivos e Criptografia em Repouso (FDE vs. File Level)
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Classifique as afirmações (FDE ou File-level Encryption):
1. Protege todo o volume, incluindo arquivos do SO e swap quando o laptop está desligado. [ FDE / File-level ]
2. Permite conceder permissões de leitura decifrada apenas para usuários específicos em pasta compartilhada. [ FDE / File-level ]
3. Fica totalmente vulnerável e decifrado quando o SO é inicializado e o usuário realiza o login. [ FDE / File-level ]
4. Exige suporte de hardware como o chip TPM para desbloqueio transparente no boot. [ FDE / File-level ]

**Sua Tarefa:**
Classifique cada afirmação como FDE ou File-level.

---

### PBQ 18: Cálculo de Colisão e Propriedades de Hash
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Avalie as propriedades de funções de hash criptográficas:
- Efeito Avalanche: Pequena alteração na entrada gera alteração [ Mínima / Drástica e Imprevisível ] no hash.
- Resistência à Colisão: Inviável encontrar duas entradas [ Identicas / Diferentes ] que produzam o [ Mesmo / Diferente ] hash.
- Irreversibilidade (One-way): Dado um hash, é impossível computar o [ Algoritmo / Texto Claro de Origem ].

**Sua Tarefa:**
Selecione as opções corretas.

---

### PBQ 19: Infraestrutura PKI: CAs Raiz, Intermediárias e Subordinadas
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Cenário do Lab / Simulação:**
Responda às perguntas de arquitetura de PKI:
1. Qual deve ser o estado operacional da CA Raiz após a emissão dos certificados das CAs Intermediárias? [ Online / Offline ]
2. Por que a CA Raiz deve ser mantida nesse estado? [ Para economizar energia / Para evitar o comprometimento da chave mestra da PKI ]
3. Quem deve emitir os certificados operacionais do dia a dia? [ CA Raiz / CA Intermediária ]

**Sua Tarefa:**
Responda às 3 perguntas de PKI.

---

### PBQ 20: Protocolos Criptográficos de Rede Seguros vs. Legados Inseguros
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Substitua os protocolos inseguros por suas alternativas criptografadas:
1. FTP (Portas 20/21) -> [ SFTP / FTPS / Telnet ]
2. Telnet (Porta 23) -> [ SSH / RDP / HTTP ]
3. HTTP (Porta 80) -> [ HTTPS / SSL / DNS ]
4. LDAP (Porta 389) -> [ LDAPS (Porta 636) / Kerberos ]
5. SNMPv1/v2c -> [ SNMPv3 (Portas 161/162 com Cifra) / Syslog ]

**Sua Tarefa:**
Informe a alternativa segura para cada serviço.

---

### PBQ 21: Modelos de Controle de Acesso (RBAC, ABAC, MAC, DAC)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Mapeie o modelo de controle de acesso adequado:
1. RBAC | 2. ABAC | 3. MAC | 4. DAC

- [   ] O criador do arquivo tem total autonomia para conceder ou revogar permissões de leitura.
- [   ] Permissões atribuídas automaticamente com base no cargo corporativo do funcionário.
- [   ] Acesso a documentos confidenciais exige rótulos de sensibilidade ("Top Secret") e autorização do sistema.
- [   ] Acesso liberado se: Cargo="Médico", Horário="08-18h", Local="Unidade A" e Dispositivo="Compliant".

**Sua Tarefa:**
Associe os modelos aos 4 cenários.

---

### PBQ 22: Arquitetura AAA: RADIUS vs. TACACS+
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Escolha RADIUS ou TACACS+ para cada afirmação:
1. Criptografa todo o pacote (cabeçalho + corpo), garantindo confidencialidade para comandos administrativos. [ RADIUS / TACACS+ ]
2. Criptografa apenas a senha dentro do pacote, deixando usuário e dados visíveis em texto claro. [ RADIUS / TACACS+ ]
3. Utiliza o protocolo de transporte TCP (Porta 49) para maior confiabilidade. [ RADIUS / TACACS+ ]
4. Utiliza UDP (Portas 1812/1813) e é o padrão de mercado para autenticação 802.1X sem fio. [ RADIUS / TACACS+ ]
5. Separa de forma rígida as funções de Autenticação, Autorização e Contabilidade. [ RADIUS / TACACS+ ]

**Sua Tarefa:**
Preencha a matriz escolhendo RADIUS ou TACACS+.

---

### PBQ 23: Federação de Identidades e SSO: SAML vs. OAuth 2.0 vs. OIDC
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Identifique o protocolo de federação correto:
A. SAML 2.0 | B. OAuth 2.0 | C. OpenID Connect (OIDC)

1. Protocolo baseado em XML usado para Autenticação Única (SSO) entre IdP e SP em aplicações corporativas.
2. Protocolo de Autorização baseado em JSON que permite acesso a recursos via tokens de acesso (Bearer Tokens).
3. Camada de Autenticação construída sobre o OAuth 2.0 que fornece um Token de Identidade (ID Token JWT).

**Sua Tarefa:**
Associe a letra do protocolo a cada requisito.

---

### PBQ 24: Análise e Configuração de Fatores de Autenticação (MFA)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Classifique os métodos em seus fatores formais:
1. Conhecimento | 2. Posse | 3. Inerência | 4. Localização | 5. Comportamento

[ A ] Padrão de digitação de teclado (Keystroke Dynamics) e assinatura.
[ B ] Token FIDO2 / Chave de Segurança YubiKey USB.
[ C ] Coordenadas GPS e validação de Sub-rede IP autorizada.
[ D ] Impressão digital, leitura de íris ou reconhecimento facial 3D.
[ E ] Senha complexa ou número de PIN pessoal.

**Sua Tarefa:**
Mapeie a letra do Método ao número do Fator.

---

### PBQ 25: Autenticação Resistente a Phishing: FIDO2 / WebAuthn
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Responda às perguntas sobre autenticação FIDO2:
1. Por que o SMS e o TOTP tradicional não são resistentes a phishing? [ Porque podem ser digitados em site falso AiTM / Porque usam senhas fracas ]
2. Qual tecnologia utiliza criptografia de chave pública e vinculação de origem (Origin Binding)? [ SAML / FIDO2 / WebAuthn / Kerberos ]
3. Qual elemento físico é utilizado como autenticador FIDO2? [ Cartão SD sem senha / Chave de Segurança USB de Hardware ]

**Sua Tarefa:**
Selecione as opções corretas.

---

### PBQ 26: Configuração de Gestão de Contas e Privilégios (PAM)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Selecione a funcionalidade PAM adequada para cada item:
1. Rotação automática de senhas de contas administrativas sem intervenção humana. [ Password Vaulting / Just-In-Time Access / Session Recording ]
2. Elevação temporária de privilégios concedida apenas durante o atendimento de um chamado aprovado. [ Just-In-Time (JIT) / Credential Stuffing / SSO ]
3. Gravação em vídeo e texto de todas as ações executadas em servidores críticos por usuários privilegiados. [ Session Recording / Dual Control / MAC ]

**Sua Tarefa:**
Selecione a funcionalidade PAM.

---

### PBQ 27: Controles de RH e Separação de Funções (Separation of Duties)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe os controles administrativos às suas finalidades:
1. Separação de Deveres | 2. Controle Duplo | 3. Férias Obrigatórias | 4. Rodízio de Funções

- [   ] Força o funcionário a se afastar temporariamente para que um substituto assuma e expor fraudes contínuas.
- [   ] Exige que duas pessoas diferentes aprovem sequencialmente ou atuem simultaneamente para concluir a tarefa.
- [   ] Divide um processo crítico em múltiplas etapas executadas por pessoas diferentes.
- [   ] Alterna periodicamente os funcionários entre diferentes posições de trabalho.

**Sua Tarefa:**
Associe os números dos controles às letras das finalidades.

---

### PBQ 28: Acesso Baseado em Políticas de Condição de Contexto (Conditional Access)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Crie a regra de Acesso Condicional para proteger dados confidenciais na nuvem:
- Grupo: "Diretoria e Finanças"
- Condição de Dispositivo: [ Qualquer Dispositivo / Apenas Dispositivos Gerenciados (Compliant) ]
- Condição de Localização: [ Qualquer País / IPs Autorizados da Sede ]
- Pontuação de Risco do Login: [ Alto / Baixo ]
- Ação Requerida: [ Bloquear Acesso / Exigir MFA + Aceite de Termos de Uso ]

**Sua Tarefa:**
Apresente a combinação de Acesso Condicional mais segura.

---

### PBQ 29: Protocolo Kerberos e Ticket-Granting Ticket (TGT)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Ordene a autenticação do protocolo Kerberos:
[ A ] O usuário apresenta o Ticket de Serviço (ST) ao servidor de recursos.
[ B ] O KDC valida a senha do usuário e emite o Ticket-Granting Ticket (TGT).
[ C ] O usuário envia solicitação de autenticação (AS-REQ) para o KDC.
[ D ] O usuário apresenta o TGT ao TGS e recebe o Ticket de Serviço (ST).

**Sua Tarefa:**
Ordene as etapas de A a D na ordem correta (1ª a 4ª).

---

### PBQ 30: Ataques de Autenticação: Password Spraying vs. Credential Stuffing
**Domínio:** Domínio 2.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Diferencie os dois ataques automatizados de força bruta:
1. Testa uma única senha muito comum (ex: Mudar123!) contra centenas de contas de usuários. [ Password Spraying / Credential Stuffing ]
2. Utiliza dicionários automatizados de pares usuário/senha vazados de outros sites na Internet. [ Password Spraying / Credential Stuffing ]

Mitigações:
- Exigir MFA obrigatório para invalidar senhas vazadas. [ Credential Stuffing / Password Spraying ]
- Implementar detecção de velocidade por senha única e bloqueio de IPs. [ Password Spraying / Credential Stuffing ]

**Sua Tarefa:**
Identifique os ataques e assinale as mitigações.

---

### PBQ 31: Análise de Código Vulnerável e Injeção Web (Cross-Site Scripting - XSS)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Identifique a variante de XSS (Refletido, Armazenado ou Baseado em DOM):
1. Inserção de script malicioso no campo de comentário de fórum lido por todos os usuários. [ Refletido / Armazenado / DOM-Based ]
2. Link malicioso em e-mail que exibe a busca com script imediatamente na tela. [ Refletido / Armazenado / DOM-Based ]
3. Script cliente lê a URL no navegador e executa diretamente via eval() sem passar pelo servidor. [ Refletido / Armazenado / DOM-Based ]
Contramedida no Navegador: [ Ativar atributo HttpOnly nos cookies / Criptografia RSA ]

**Sua Tarefa:**
Preencha a matriz e indique a contramedida.

---

### PBQ 32: Ataques Server-Side Request Forgery (SSRF) vs. CSRF
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Diferencie SSRF e CSRF:
Cenário A: Aplicação na nuvem importa imagem via URL. Atacante envia URL do serviço de metadados da nuvem (169.254.169.254) e recebe credenciais IAM temporárias.
Cenário B: E-mail com imagem invisível induz o navegador do usuário autenticado a fazer transferência bancária usando seus cookies ativos.

1. Qual cenário é SSRF? [ Cenário A / Cenário B ]
2. Qual cenário é CSRF? [ Cenário A / Cenário B ]
3. Contramedida primária para Cenário B? [ Tokens Anti-CSRF Únicos / Validação de IP ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 33: Ataques de Estouro de Buffer (Buffer Overflow) e Proteções de Compilação
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Associe a defesa de compilação ao seu efeito:
1. Stack Canaries | 2. ASLR | 3. DEP/NX

- [   ] Impede a execução direta de instruções maliciosas na memória da pilha.
- [   ] Torna imprevisíveis os endereços de memória dos registradores da aplicação.
- [   ] Detecta a corrupção da pilha antes que a função retorne ao ponteiro manipulado.

**Sua Tarefa:**
Associe as técnicas aos 3 itens.

---

### PBQ 34: Condições de Corrida: Race Conditions (TOC/TOU)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Análise de TOC/TOU:
1. Qual o nome dessa vulnerabilidade? [ TOC/TOU / Buffer Overflow / Integer Overflow ]
2. Como o atacante a explora? [ Enviando requisições concorrentes em milissegundos para sacar o mesmo saldo / Alterando o hash ]
3. Qual a correção adequada? [ Operações Atômicas e Mutex / Aumentar tempo de pausa ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 35: Modelos de Nuvem e Matriz de Responsabilidade Compartilhada
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Mapeie o responsável principal (Cliente ou Provedor):
1. SO convidado em uma Máquina Virtual na nuvem (IaaS). [ Cliente / Provedor ]
2. BD relacional gerenciado (AWS RDS/Azure SQL) e SO subjacente (PaaS). [ Cliente / Provedor ]
3. Infraestrutura física do datacenter, hipervisores e rede (IaaS/PaaS/SaaS). [ Cliente / Provedor ]
4. Dados e permissões no Office 365 / Google Workspace (SaaS). [ Cliente / Provedor ]

**Sua Tarefa:**
Informe o responsável para cada item.

---

### PBQ 36: Ataques XML External Entity (XXE) e Injeção de Comando
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Diagnóstico de payload XML:
1. Qual a vulnerabilidade presente? [ XXE / SQLi / XSS / SSRF ]
2. Qual o impacto imediato? [ Leitura de arquivos confidenciais do SO (/etc/passwd) / Apagamento do BD ]
3. Qual a contramedida técnica? [ Desativar entidades externas DTD no parser XML / Usar HTTPS ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 37: Segurança em Microserviços, Conteinerização e Docker
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Mapeie as práticas de hardening Docker (CORRETO ou INCORRETO):
1. Executar a aplicação dentro do contêiner como usuário root. [ CORRETO / INCORRETO ]
2. Utilizar imagens minimalistas (Alpine/Distroless) oficiais assinadas. [ CORRETO / INCORRETO ]
3. Configurar o sistema de arquivos do contêiner como Somente Leitura (Read-Only). [ CORRETO / INCORRETO ]
4. Mapear o soquete do Docker (/var/run/docker.sock) dentro do contêiner. [ CORRETO / INCORRETO ]

**Sua Tarefa:**
Mapeie cada prática como CORRETO ou INCORRETO.

---

### PBQ 38: Infraestrutura como Código (IaC) e Drift de Configuração
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Perguntas sobre IaC:
1. Qual o termo técnico para a divergência entre a nuvem real e o código Terraform? [ Configuration Drift / Memory Leak / Race Condition ]
2. Como o processo de CI/CD com IaC resolve essa discrepância? [ Sobrescrevendo a alteração manual e re-aplicando o estado declarativo / Deletando a nuvem ]
3. Qual o benefício de segurança primário da IaC? [ Imutabilidade, padronização, auditoria e rastreabilidade via Git ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 39: Injeção de Comando de Sistema Operacional (Command Injection)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Analise a função PHP `system("ping -c 3 " . $_GET['ip']);` com payload `8.8.8.8; cat /etc/shadow`:
1. Qual a vulnerabilidade? [ Command Injection / SQLi / Path Traversal ]
2. O que o operador `;` realiza? [ Executa o segundo comando em sequência no shell do SO ]
3. Qual a correção de código? [ Evitar chamadas diretas de shell e sanitizar rigorosamente a entrada ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 40: Ataques de Travessia de Diretório (Directory / Path Traversal)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Analise a URL `download.php?file=../../../../etc/passwd`:
1. Qual o ataque executado? [ Path Traversal / SSRF / CSRF ]
2. O que a sequência `../` realiza? [ Sobe um nível no diretório até atingir a raiz do sistema ]
3. Qual a contramedida principal? [ Sanitizar sequências de pontos/barras e usar mapeamento numérico indireto no BD ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 41: Taxonomia de Ataques de Phishing e Vetores de Contato
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Associe o ataque à sua descrição:
1. Spear Phishing | 2. Whaling | 3. Vishing | 4. Smishing | 5. Waterhole

- [   ] Compromete site muito frequentado por colaboradores de um setor para infectá-los.
- [   ] Mensagem SMS contendo link falso para confirmação de compra bancária.
- [   ] E-mail altamente customizado enviado ao Diretor Financeiro (CFO).
- [   ] Ligação telefônica se passando pelo suporte de TI.
- [   ] E-mail personalizado enviado aos 5 engenheiros do setor de P&D.

**Sua Tarefa:**
Associe os números às descrições.

---

### PBQ 42: Técnicas de Evasão em Memória: Process Hollowing vs. DLL Injection
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Diferencie as técnicas:
Cenário A: Processo legítimo suspenso (svchost.exe) tem seu código desalocado e substituído por código malicioso.
Cenário B: Processo malicioso força o carregamento de uma DLL maliciosa no espaço de memória de outro processo.

1. Qual técnica é o Cenário A? [ Process Hollowing / DLL Injection ]
2. Qual técnica é o Cenário B? [ Process Hollowing / DLL Injection ]
3. Qual o benefício para o atacante? [ Execução em memória sem arquivo no disco (Fileless) burlando antivírus ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 43: Ameaças Físicas: Tailgating, Piggybacking e Shoulder Surfing
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Identifique o ataque e o controle:
Cenário 1: Entregador segura a porta aberta para funcionário e entra na área restrita sem crachá.
Cenário 2: Invasor observa com binóculo a tela do laptop de um executivo gravando a digitação de senhas.

- Cenário 1: Ataque = [ Tailgating / Shoulder Surfing ] | Controle = [ Catraca Mantrap / Filtro de Privacidade ]
- Cenário 2: Ataque = [ Tailgating / Shoulder Surfing ] | Controle = [ Catraca Mantrap / Filtro de Privacidade ]

**Sua Tarefa:**
Preencha a matriz.

---

### PBQ 44: Tipos de Malware: Ransomware, Rootkit, Logic Bomb e Spyware
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Mapeie a família de malware:
1. Ransomware | 2. Rootkit | 3. Logic Bomb | 4. Spyware

- [   ] Código oculto acionado por data futura para apagar banco de dados.
- [   ] Altera chamadas de sistema para esconder seus próprios processos de ferramentas de segurança.
- [   ] Criptografa arquivos e exige resgate em criptomoedas.
- [   ] Monitora teclas digitadas e envia capturas de tela para C2.

**Sua Tarefa:**
Associe as famílias aos itens.

---

### PBQ 45: Ataques de Engenharia Social com IA e Deepfakes
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Análise de ataque com IA generativa:
1. Qual técnica de manipulação é empregada para clonar áudio/vídeo do CEO? [ Deepfake / Vishing / Typosquatting ]
2. Qual princípio de engenharia social é explorado? [ Autoridade e Urgência / Escassez ]
3. Qual procedimento mitiga o ataque? [ Validação de transferência fora de banda com aprovação dupla ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 46: Análise de Ataques Typosquatting e Combôsquatting
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Classifique o domínio malicioso em relação a `bancobrasil.com.br`:
1. `bancodebrasil.com.br` -> [ Combosquatting / Typosquatting ]
2. `bancobrasll.com.br` -> [ Combosquatting / Typosquatting ]
3. `bancobrasil-login.com.br` -> [ Combosquatting / Typosquatting ]
Contramedida: [ Registrar variações comuns e monitorar DNS via Threat Intelligence / Firewall L4 ]

**Sua Tarefa:**
Classifique os domínios e a contramedida.

---

### PBQ 47: Software Inseguro e Sombra de TI (Shadow IT)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Perguntas sobre Shadow IT:
1. Qual termo descreve o uso de soluções não homologadas pela segurança? [ Shadow IT / Insider Threat ]
2. Qual ferramenta detecta o uso dessas aplicações em nuvem não homologadas? [ CASB / Firewall L3 / Antivírus ]
3. Qual o maior risco da Shadow IT? [ Vazamento não monitorado de dados confidenciais e não conformidade LGPD ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 48: Insiders Maliciosos vs. Insiders Negligentes
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Diagnóstico de Insider Threat:
Cenário 1: DB Admin prestes a ser demitido copia segredos industriais para HD externo para vender a concorrente.
Cenário 2: Colaborador envia planilha com dados de clientes para e-mail pessoal para trabalhar no fim de semana.

- Cenário 1: [ Insider Malicioso / Insider Negligente ] | Controle = [ DLP + PAM / Treinamento ]
- Cenário 2: [ Insider Malicioso / Insider Negligente ] | Controle = [ DLP + Treinamento / Processo Criminal ]

**Sua Tarefa:**
Preencha o diagnóstico.

---

### PBQ 49: Ataques Supply Chain (Cadeia de Suprimentos)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Análise de ataque Supply Chain:
1. Qual a denominação do ataque que compromete o servidor de build do fornecedor? [ Supply Chain / MITM ]
2. Por que é bem-sucedido? [ Porque a atualização vem assinada por fonte de software confiável ]
3. Qual mecanismo de governança reduz este risco? [ Due Diligence, SBOM e verificação de integridade ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 50: Criptojacking e Abuso de Recursos de Computação
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Análise de Criptojacking:
1. Qual a ameaça identificada pelo processo `minerd`? [ Cryptojacking / Ransomware / Spyware ]
2. Qual o impacto direto na nuvem? [ Custo financeiro elevado pela escala automática e degradação de desempenho ]
3. Qual a ação imediata de remediação? [ Interromper o processo, isolar a instância e revogar credenciais ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 51: Análise de Ataques em Redes Wi-Fi: Rogue AP vs. Evil Twin
**Domínio:** Domínio 2.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Diferencie os pontos de acesso:
Cenário A: Colaborador pluga roteador pessoal na tomada de rede para ter Wi-Fi no celular.
Cenário B: Atacante liga AP falso clonando o SSID e BSSID da empresa no ar.

1. Qual é Rogue AP? [ Cenário A / Cenário B ]
2. Qual é Evil Twin? [ Cenário A / Cenário B ]
3. Qual tecnologia detecta e bloqueia? [ WIPS / Filtro MAC / Ocultar SSID ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 52: Ataques de Desautenticação (Deauthentication Attack) e WPA3 SAE
**Domínio:** Domínio 2.0 / 3.0: Arquitetura

**Cenário do Lab / Simulação:**
Perguntas sobre WPA3:
1. Por que o WPA2 é vulnerável a ataques Deauth? [ Porque quadros de gerenciamento são em texto claro e sem autenticação ]
2. Qual recurso obrigatório no WPA3 mitiga ataques Deauth? [ PMF (IEEE 802.11w) / WEP / PSK ]
3. Qual mecanismo substitui o PSK no WPA3 contra ataques de dicionário offline? [ SAE (Dragonfly) / TKIP / MD5 ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 53: Modelos de Implantação Móvel: BYOD, COPE, CYOD e Corporate-Owned
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Associe os modelos móveis:
1. BYOD | 2. COPE | 3. CYOD | 4. Corporate-Owned

- [   ] Empresa compra e é proprietária, permitindo uso pessoal isolado via MDM.
- [   ] Colaborador usa smartphone pessoal com partição MDM corporativa.
- [   ] Colaborador escolhe o modelo a partir de lista homologada pela empresa.
- [   ] Propriedade da empresa estritamente corporativo sem uso pessoal.

**Sua Tarefa:**
Associe os modelos às descrições.

---

### PBQ 54: Recursos de Gerenciamento Móvel (MDM / MAM) e Wipe Remoto
**Domínio:** Domínio 3.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Smartphone corporativo roubado. Ordene a resposta do MDM:
[ A ] Bloqueio de tela remoto (Remote Lock) via MDM.
[ B ] Bloqueio de IMEI na operadora de telefonia.
[ C ] Apagamento remoto (Remote Wipe) dos dados corporativos.
[ D ] Revogação de certificados e tokens de sessão no IdP.

**Sua Tarefa:**
Ordene a sequência correta de prioridade.

---

### PBQ 55: Hardening de Host: Lista de Aplicações Permitidas (Application Allowlisting)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Perguntas sobre Application Allowlisting:
1. Qual abordagem bloqueia por padrão todo executável, liberando apenas o autorizado? [ Application Allowlisting / Blocklisting ]
2. Qual critério de regra é o mais seguro e imune a alterações de nomes? [ Publisher Rule (Assinatura Digital) / Path Rule ]
3. Por que regras de Caminho (Path Rule) são inseguras? [ Porque um atacante com escrita no caminho pode colocar malware com o mesmo nome ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 56: Capacidades de Soluções Endpoint: EDR vs. XDR vs. Antivírus Tradicional
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Associe as soluções (A. Antivírus Assinatura | B. EDR | C. XDR):
1. Analisa comportamentos anômalos em tempo real na estação e isola o host automaticamente. [ A / B / C ]
2. Compara arquivos no disco com banco de dados estático de hashes conhecidos. [ A / B / C ]
3. Correlaciona telemetria de Endpoints, E-mail, Nuvem, Rede e Identidade unificada. [ A / B / C ]

**Sua Tarefa:**
Associe as letras às capacidades.

---

### PBQ 57: Proteção de Navegação e Isolamento de Sessão (Browser Isolation / RBI)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Cenário do Lab / Simulação:**
Perguntas sobre RBI:
1. Qual tecnologia roda a sessão web dentro de contêiner isolado na nuvem enviando apenas pixels? [ RBI / CASB / SWG ]
2. Como elimina o risco de infecção por malware? [ Código malicioso executa na nuvem e é destruído ao fechar a aba sem tocar no PC local ]

**Sua Tarefa:**
Responda às 2 perguntas.

---

### PBQ 58: Proteção de Dispositivos de Armazenamento e Desativação USB
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Bloqueio de USB via GPO:
1. Onde configurar a diretiva de bloqueio de USB no Active Directory? [ Configuração do Computador -> Modelos Administrativos -> Sistema -> Acesso de Armazenamento Removível ]
2. Como liberar um pendrive corporativo específico criptografado mantendo o bloqueio geral? [ Cadastrar o ID do Dispositivo (Hardware ID / VID & PID) na lista de exceções permitidas da GPO ]

**Sua Tarefa:**
Responda às 2 perguntas.

---

### PBQ 59: Ataques Bluetooth: Bluejacking vs. Bluesnarfing
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Cenário do Lab / Simulação:**
Diferencie ataques Bluetooth:
Cenário 1: Envio de mensagens não solicitadas sem extrair dados do aparelho. [ Bluejacking / Bluesnarfing ]
Cenário 2: Roubo não autorizado de contatos, fotos e mensagens do celular via Bluetooth. [ Bluejacking / Bluesnarfing ]
Contramedida: [ Manter Bluetooth em modo Não Descobrível / Usar Antivírus ]

**Sua Tarefa:**
Preencha o mapeamento.

---

### PBQ 60: Sistemas de Arquivos de Segurança e Criptografia em Nuvem (DLP / CASB)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Inspecção e prevenção de vazamento de dados:
1. Qual componente de segurança previne vazamento de PII no e-mail corporativo? [ Email Gateway DLP / WAF ]
2. Qual componente monitora e bloqueia compartilhamento público não autorizado no Google Drive / Office 365 via API? [ CASB / Firewall L3 ]

**Sua Tarefa:**
Responda às 2 perguntas.

---

### PBQ 61: Fases do Ciclo de Vida de Resposta a Incidentes (NIST SP 800-61)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Ordene as fases do NIST SP 800-61:
[ A ] Erradicação e Recuperação
[ B ] Preparação
[ C ] Atividades Pós-Incidente / Lições Aprendidas
[ D ] Detecção e Análise

**Sua Tarefa:**
Ordene na sequência oficial (1ª a 4ª).

---

### PBQ 62: Mapeamento das Ações do Analista de Incidentes (Contenção vs. Erradicação)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Classifique a ação na fase de resposta:
1. Desconectar cabo de rede e isolar porta do switch em VLAN de quarentena. [ Contenção / Erradicação / Recuperação / Lições Aprendidas ]
2. Remover o malware, deletar registros de inicialização e aplicar patch de correção. [ Contenção / Erradicação / Recuperação / Lições Aprendidas ]
3. Restaurar o SO a partir de imagem limpa e recuperar dados dos backups offline. [ Contenção / Erradicação / Recuperação / Lições Aprendidas ]
4. Elaborar relatório final de causa-raiz e atualizar IOCs. [ Contenção / Erradicação / Recuperação / Lições Aprendidas ]

**Sua Tarefa:**
Classifique cada ação.

---

### PBQ 63: Ordem de Volatilidade da Evidência Digital (RFC 3227)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Ordene as evidências do MAIS VOLÁTIL (1º) ao MENOS VOLÁTIL (5º):
[ A ] Disco Rígido Principal (HDD / SSD)
[ B ] Memória RAM do Sistema
[ C ] Registradores do Processador e Cache
[ D ] Backups em Fita
[ E ] Tabela de Roteamento, Cache ARP e Processos

**Sua Tarefa:**
Ordene de 1º a 5º.

---

### PBQ 64: Uso do Write Blocker e Clonagem Forense (Bit-stream Image)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Procedimento forense de aquisição:
1. Qual equipamento deve ser inserido antes de ler o disco original? [ Hardware Write Blocker / Switch ]
2. Qual sua função? [ Impedir qualquer alteração de dados ou metadados no disco original ]
3. Qual o tipo de imagem gerada? [ Imagem Bit-a-Bit setor por setor / Cópia Windows Explorer ]
4. Como é comprovada a integridade no tribunal? [ Comparando o valor de Hash SHA-256 gerado na apreensão com o do exame ]

**Sua Tarefa:**
Responda às 4 perguntas.

---

### PBQ 65: Formulário de Cadeia de Custódia (Chain of Custody)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Campos essenciais da Cadeia de Custódia:
- Coletado Por: [ Nome, Cargo e Assinatura do Perito Responsável ]
- Armazenamento: [ Cofre de Evidências Físicas com Controle de Acesso ]
- Transferência de Custódia: [ Data, Hora, Motivo, Nome do Doador e Assinatura do Recebedor ]

**Sua Tarefa:**
Identifique os requisitos essenciais.

---

### PBQ 66: Coleta e Extração de Memória Volátil (RAM Dump)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Extração de RAM em Fileless Malware:
1. O servidor deve ser desligado antes da coleta da RAM? [ SIM / NÃO ]
2. Por que o desligamento destrói a evidência? [ Porque a RAM é volátil e o corte de energia apaga os dados ]
3. Ferramenta para extrair a RAM: [ FTK Imager / WinPmem / Lime ]
4. Ferramenta para analisar a RAM: [ Volatility Framework / Nmap ]

**Sua Tarefa:**
Responda às 4 perguntas.

---

### PBQ 67: Prevenção de Alteração e Retenção Legal (Legal Hold)
**Domínio:** Domínio 4.0 / 5.0: GRC

**Cenário do Lab / Simulação:**
Ações sob Legal Hold (CORRETO ou INCORRETO):
1. Suspender rotinas de expiração e substituição automatizada de backups dos investigados. [ CORRETO / INCORRETO ]
2. Continuar destruição automática de e-mails antigos após 30 dias. [ CORRETO / INCORRETO ]
3. Preservar caixas de e-mail e logs em armazenamento imutável WORM. [ CORRETO / INCORRETO ]

**Sua Tarefa:**
Mapeie as 3 ações.

---

### PBQ 68: Análise Forense de Cabeçalho de E-mail (Email Header Analysis)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Analise o cabeçalho: `Received: from mail.evil-attacker.com (198.51.100.25)` | `From: suporte@bancodobrasil.com.br` | `Authentication-Results: spf=fail`
1. O e-mail é legítimo? [ SIM / NÃO ]
2. Qual elemento comprova a falsificação? [ IP de origem 198.51.100.25 no Received falhou no SPF ]
3. Qual campo indica para onde a resposta oculta iria? [ Return-Path ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 69: Auditoria e Integridade de Logs de Servidores
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Proteção contra alteração de logs por invasor root:
1. Qual solução exige que logs sejam enviados em tempo real para servidor remoto imutável? [ Syslog Centralizado / SIEM WORM ]
2. Qual recurso garante integridade criptográfica contra alteração de logs locais? [ Forward Secure Logging / Criptografia de Logs em Cadeia ]

**Sua Tarefa:**
Responda às 2 perguntas.

---

### PBQ 70: Indicadores de Comprometimento (IOCs) vs. Indicadores de Ataque (IOA)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Classifique em IOC ou IOA:
1. Hash SHA-256 de um arquivo binário malicioso conhecido. [ IOC / IOA ]
2. Processo desconhecido injetando código na RAM de outro processo e abrindo conexões de madrugada. [ IOC / IOA ]
3. Endereço IP externo de reputação ruim listado como servidor C2. [ IOC / IOA ]

**Sua Tarefa:**
Classifique cada exemplo.

---

### PBQ 71: Análise de Logs do SIEM e Correlação de Eventos de Segurança
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Analise a regra do SIEM:
- EventID 4625 (Falha Logon) > 50 vezes em 1 min do mesmo IP para vários usuários.
- EventID 4624 (Logon Sucesso) no 51º segundo para 'marcos.silva'.
- Processo criado: 'net localgroup Administrators marcos.silva /add'.

1. Qual ataque causou o primeiro evento? [ Password Spraying / Credential Stuffing ]
2. O que indica o evento 2? [ Comprometimento de Conta (Account Takeover) com sucesso ]
3. O que o comando no evento 3 executa? [ Elevação Local de Privilégios ]
4. Ação inicial do SOAR? [ Desativar a conta 'marcos.silva', revogar sessão e isolar o host ]

**Sua Tarefa:**
Responda às 4 perguntas.

---

### PBQ 72: Orquestração de Segurança e Playbooks Automáticos no SOAR
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Ordene o Playbook do SOAR para Phishing:
[ A ] Se confirmado malicioso no Sandbox, bloquear a Hash no EDR e o IP no Firewall.
[ B ] Enviar o anexo .zip automaticamente para o Sandbox de malware.
[ C ] Notificar a equipe do SOC e responder ao usuário que reportou.
[ D ] Purgar o e-mail de Phishing de todas as caixas de entrada da empresa.

**Sua Tarefa:**
Ordene de 1ª a 4ª etapa.

---

### PBQ 73: Monitoramento de Integridade de Arquivos (FIM - File Integrity Monitoring)
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Alerta do FIM: Alteração no Hash SHA-256 do arquivo `/usr/sbin/sshd`.
1. O que indica essa alteração imprevisível sem janela de manutenção? [ Substituição do binário legítimo por versão trojanizada com backdoor ]
2. Qual pilar da Tríade CIA foi violado? [ Integridade ]
3. Ação imediata? [ Isolar o servidor, preservar imagem do disco/RAM e restaurar binário limpo ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 74: Análise de Tráfego de Rede via NetFlow / IPFIX
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Análise de registro NetFlow de madrugada (10.0.5.12 -> IP Estrangeiro:443 | 85 GB | 4 Horas):
1. Qual a anomalia evidenciada? [ Exfiltração Massiva de Dados (Data Exfiltration) ]
2. O NetFlow inspeciona o payload dos pacotes? [ SIM / NÃO ]
3. Diferença entre NetFlow e PCAP? [ NetFlow coleta apenas metadados do fluxo sem salvar o payload ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 75: Framework MITRE ATT&CK e Mapeamento de Táticas
**Domínio:** Domínio 2.0 / 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Mapeie a ação à Tática do MITRE ATT&CK:
1. Initial Access | 2. Persistence | 3. Privilege Escalation | 4. Defense Evasion | 5. Lateral Movement

- [   ] Criar chave no Registro do Windows HKLM\...\Run apontando para script.
- [   ] Conectar via RDP com credencial administrativa de uma máquina para outra.
- [   ] Enviar Spear Phishing com anexo malicioso executável.
- [   ] Executar chmod 777 e desativar agente de antivírus local.
- [   ] Explorar buffer overflow no spoofer local para obter acesso SYSTEM.

**Sua Tarefa:**
Associe as ações às táticas.

---

### PBQ 76: Fontes de Inteligência sobre Ameaças (Threat Intelligence Feeds)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Classifique a fonte de Threat Intelligence (A. OSINT | B. Pago | C. ISAC):
1. Informações estratégicas do setor bancário compartilhadas via FS-ISAC. [ A / B / C ]
2. Feeds públicos, relatórios acadêmicos e blogs abertos. [ A / B / C ]
3. Serviço proprietário assinado que fornece dados validados de honeypots globais. [ A / B / C ]

**Sua Tarefa:**
Associe as letras aos itens.

---

### PBQ 77: Análise de Logs de Firewall de Borda e Bloqueio de Portas
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Log de firewall: `PERMIT TCP 198.51.100.44 -> 10.0.1.50:445`
1. Qual serviço/protocolo está atacado na porta 445? [ SMB / Porta 445 / Compartilhamento Windows ]
2. Qual a ameaça associada à exposição da porta 445 na Internet? [ Propagação de Worms / Ransomware (WannaCry) ]
3. Regra de firewall correta? [ Bloquear tráfego público para as portas TCP 139 e 445 na borda ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 78: Análise de Logs de Antivírus e Ações de Quarentena
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Alerta EDR: `C:\Users\public\invoice.exe` -> Quarentena | Hash: `c4ca4238...`
1. Oferece risco de execução imediata? [ NÃO, pois está isolado em quarentena ]
2. Próxima etapa de investigação? [ Threat Hunting da mesma Hash nas demais estações via SIEM/EDR ]
3. Ação no Gateway de E-mail? [ Bloquear a Hash do anexo e o remetente ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 79: Tabela de Correlação de Eventos de Autenticação
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Correlacione o Event ID do Windows ao significado:
1. Event ID 4624 | 2. Event ID 4625 | 3. Event ID 4672 | 4. Event ID 4720

- [   ] Conta de usuário foi criada.
- [   ] Falha de logon.
- [   ] Logon bem-sucedido.
- [   ] Privilégios administrativos especiais atribuídos a novo logon.

**Sua Tarefa:**
Associe os números dos eventos.

---

### PBQ 80: Varredura e Mapeamento com Nmap e Interpretação de Portas
**Domínio:** Domínio 4.0: Operações de Segurança

**Cenário do Lab / Simulação:**
Resultado Nmap: 21 (FTP), 22 (SSH), 80 (HTTP), 443 (HTTPS), 3389 (RDP)
1. Qual porta oferece maior risco de vazamento de credenciais em texto claro? [ Porta 21 (FTP) / Porta 22 (SSH) ]
2. Qual porta expõe RDP diretamente? [ Porta 3389 / Porta 443 ]
3. Ação de hardening recomendada para 3389? [ Bloquear exposição pública da 3389 e exigir VPN com MFA + NLA ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 81: Cálculo Quantitativo de Risco (SLE, ARO e ALE)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Ativo: R$ 200.000 | EF: 30% (0,30) | ARO: 0,1
1. Calcule o SLE (Valor * EF): [ R$ 60.000 ]
2. Calcule o ALE (SLE * ARO): [ R$ 6.000 ]
3. Custo do controle: R$ 4.000/ano. Justifica-se a contratação? [ SIM / NÃO ]

**Sua Tarefa:**
Apresente os cálculos e a decisão.

---

### PBQ 82: Métricas de Continuidade de Negócio: RTO vs. RPO vs. MTTR vs. MTBF
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe as métricas aos conceitos:
1. RTO | 2. RPO | 3. MTTR | 4. MTBF

- [   ] Volume máximo aceitável de perda de dados medido em tempo (frequência de backup).
- [   ] Tempo máximo tolerável de inatividade de um sistema após um desastre.
- [   ] Tempo médio esperado entre falhas de um sistema reparável.
- [   ] Tempo médio necessário para reparar e restaurar o sistema após falha.

**Sua Tarefa:**
Associe as métricas.

---

### PBQ 83: Estratégias de Resposta ao Risco (Risk Response Strategies)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe as estratégias às ações:
1. Mitigação | 2. Transferência | 3. Aceitação | 4. Evitação

- [   ] Cancelar projeto em país de alto risco eliminando a atividade.
- [   ] Contratar seguro cibernético (Cyber Insurance) para cobrir eventuais custos.
- [   ] Instalar WAF e aplicar patches para reduzir a probabilidade de invasão.
- [   ] Documentar e conviver com o risco devido ao custo-benefício desfavorável do controle.

**Sua Tarefa:**
Associe as estratégias.

---

### PBQ 84: Avaliação de Riscos de Terceiros e Relatórios SOC
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Escolha o relatório SOC correto:
1. Relatório público sumário simplificado sem detalhes técnicos. [ SOC 1 / SOC 2 / SOC 3 ]
2. Relatório focado nos controles internos contábeis e financeiros. [ SOC 1 / SOC 2 / SOC 3 ]
3. Relatório de auditoria que avalia a eficácia operacional contínua ao longo de 6 a 12 meses. [ SOC 1 / SOC 2 Type I / SOC 2 Type II ]

**Sua Tarefa:**
Selecione o relatório SOC.

---

### PBQ 85: Exercícios de Continuidade: Tabletop vs. Functional vs. Full-Scale
**Domínio:** Domínio 3.0 / 5.0: GRC

**Cenário do Lab / Simulação:**
Classifique o teste de BCP:
1. Tabletop Exercise | 2. Functional Test | 3. Full-Scale Test

- [   ] Discussão teórica baseada em cenário em sala de reunião sem mobilizar recursos físicos.
- [   ] Desligamento real do ambiente principal com alternância total para o Hot Site.
- [   ] Teste de failover dos servidores de BD no ambiente secundário no fim de semana.

**Sua Tarefa:**
Associe os testes aos cenários.

---

### PBQ 86: Análise de Impacto no Negócio (BIA - Business Impact Analysis)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Classifique os objetivos do BIA (VERDADEIRO ou FALSO):
1. Identificar funções críticas de negócios e recursos para mantê-las. [ VERDADEIRO / FALSO ]
2. Determinar o impacto financeiro/operacional da indisponibilidade ao longo do tempo. [ VERDADEIRO / FALSO ]
3. Escolher o fabricante do firewall e configurar as regras de ACL. [ VERDADEIRO / FALSO ]
4. Estabelecer métricas de RTO e RPO para cada sistema corporativo. [ VERDADEIRO / FALSO ]

**Sua Tarefa:**
Mapeie cada item.

---

### PBQ 87: Tipos de Backups: Total, Incremental e Diferencial
**Domínio:** Domínio 3.0 / 4.0: Operações

**Cenário do Lab / Simulação:**
Compare os tipos de backup para restauração na quinta-feira (Total no Domingo):
Cenário Incremental:
- Exige: Backup Total de Domingo + [ Apenas o de Quarta / Todos de Segunda, Terça e Quarta em ordem ]
- Velocidade de execução do backup diário: [ RÁPIDO / LENTO ]
- Tempo de restauração total: [ RÁPIDO / MAIS LENTO ]

Cenário Diferencial:
- Exige: Backup Total de Domingo + [ Apenas o último Diferencial de Quarta / Todos ]
- Tempo de restauração total: [ MAIS RÁPIDO QUE O INCREMENTAL / MAIS LENTO ]

**Sua Tarefa:**
Preencha o comparativo.

---

### PBQ 88: Gestão de Riscos de Terceiros e Acordos Contratuais
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe os documentos contratuais às finalidades:
1. SLA | 2. MOU | 3. NDA | 4. BPA

- [   ] Acordo formal de confidencialidade proibindo divulgação de dados sensíveis.
- [   ] Cláusula contratual com metas rígidas de disponibilidade (99,99%) e penalidades.
- [   ] Documento de intenção bilateral sem obrigações financeiras executáveis.
- [   ] Contrato que estabelece termos de parceria, divisão de lucros e riscos.

**Sua Tarefa:**
Associe os documentos.

---

### PBQ 89: Gerenciamento de Mudanças (Change Management) e Plano de Rollback
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Ordene a Gestão de Mudanças:
[ A ] Apresentar a solicitação para aprovação do Comitê de Mudanças (CAB).
[ B ] Testar em homologação e elaborar o Plano de Rollback detalhado.
[ C ] Aplicar a mudança na janela autorizada e realizar testes pós-implantação.
[ D ] Registrar a RFC documentando a justificativa de negócios.

**Sua Tarefa:**
Ordene na sequência correta (1ª a 4ª).

---

### PBQ 90: Modelos de Governança: CobIT, ITIL, NIST CSF e ISO/IEC 27001
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe o framework de governança (A. ISO 27001 | B. NIST CSF | C. ITIL | D. COBIT):
1. Norma internacional auditável para certificação formal de SGSI. [ A / B / C / D ]
2. Estrutura das 6 funções (Govern, Identify, Protect, Detect, Respond, Recover). [ A / B / C / D ]
3. Framework focado na governança corporativa de TI alinhada ao conselho. [ A / B / C / D ]
4. Boas práticas para o gerenciamento de serviços de TI (ITSM). [ A / B / C / D ]

**Sua Tarefa:**
Associe os frameworks.

---

### PBQ 91: Papéis e Responsabilidades sobre Dados (Data Roles)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe os papéis de dados aos cenários:
1. Data Owner | 2. Data Custodian | 3. DPO | 4. Data Processor

- [   ] Provedor de nuvem terceirizado que processa dados sob instruções da empresa.
- [   ] Diretor de RH responsável legal pela classificação dos dados dos funcionários.
- [   ] Administrador de Banco de Dados da TI responsável por backups e acessos técnicos.
- [   ] Encarregado de dados responsável por privacidade e contato com a autoridade (ANPD).

**Sua Tarefa:**
Associe os papéis.

---

### PBQ 92: Conceito de Privacidade por Design (Privacy by Design)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Aplicação do Privacy by Design:
Aplicação móvel de compras exige GPS em tempo real, data de nascimento e título de eleitor apenas para navegar no catálogo.
1. Qual princípio do Privacy by Design foi violado? [ Minimização de Dados / Criptografia ]
2. Qual a correção do fluxo? [ Solicitar estritamente o necessário para a consulta ao catálogo ]

**Sua Tarefa:**
Responda às 2 perguntas.

---

### PBQ 93: Análise de Impacto na Proteção de Dados (DPIA / RIPD)
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Análise de conformidade para Reconhecimento Facial:
1. Qual documento formal deve ser elaborado antes de coletar biometria? [ DPIA / RIPD / Relatório SOC 1 ]
2. Qual o propósito desse relatório? [ Descrever o processamento sensível, avaliar necessidade e mapear riscos/mitigações ]
3. Quem deve ser consultado? [ DPO, equipe de TI/Segurança e representantes dos titulares ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 94: Mapeamento de Leis de Privacidade e Padrões Setoriais
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe as normas às áreas de aplicação:
1. PCI-DSS | 2. HIPAA | 3. GDPR/LGPD | 4. SWIFT CSP

- [   ] Regulamenta privacidade e tratamento de dados pessoais de cidadãos.
- [   ] Padrão obrigatório para entidades que processam dados de Cartões de Crédito.
- [   ] Legislação para proteção de informações de saúde (PHI).
- [   ] Padrão obrigatório para transferências financeiras internacionais.

**Sua Tarefa:**
Associe as normas.

---

### PBQ 95: Classificação de Dados e Rótulos de Sensibilidade
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Associe os rótulos de sensibilidade (A. Público | B. Interno | C. Confidencial | D. Restrito):
1. Receita secreta do produto principal e código-fonte proprietário. [ A / B / C / D ]
2. Manual de integração e lista de ramais do escritório. [ A / B / C / D ]
3. Relatórios de demonstrações financeiras já publicados no site oficial. [ A / B / C / D ]
4. Dados pessoais sensíveis de clientes e demonstrações antes da divulgação. [ A / B / C / D ]

**Sua Tarefa:**
Associe os rótulos aos exemplos.

---

### PBQ 96: Técnicas de Destruição e Sanitização de Mídias
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Escolha o método de sanitização:
1. Degaussing | 2. Cryptographic Erasure | 3. Trituração Física | 4. Sanitização por Software

- [   ] Destruir as chaves de cifragem de um SSD/Volume criptografado para inviabilizar os dados instantaneamente.
- [   ] Destruição física em triturador reduzindo HDDs e fitas a pequenos fragmentos.
- [   ] Destruição magnética do revestimento de um disco rígido tradicional HDD (Não funciona em SSDs).
- [   ] Sobrescrever todos os setores do disco com padrões de bits para reutilização na empresa.

**Sua Tarefa:**
Associe os métodos aos cenários.

---

### PBQ 97: Transferência Internacional de Dados e Soberania dos Dados
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Perguntas sobre Soberania de Dados:
1. O que estabelece a Soberania dos Dados? [ Os dados estão sujeitos às leis do país onde estão fisicamente armazenados ]
2. Como garantir que dados na nuvem não saiam do país? [ Configurando o bloqueio de região (Geo-Locking) ]
3. Servidor nos EUA armazenando dados de europeus está sujeito a intimações dos EUA? [ SIM, a localização física do hardware estabelece a jurisdição local ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 98: Auditoria Interna vs. Auditoria Externa
**Domínio:** Domínio 5.0: GRC

**Cenário do Lab / Simulação:**
Preencha a matriz de auditoria (Interna ou Externa):
1. Realizada por funcionários da própria empresa para avaliar controles antes da verificação oficial. [ Interna / Externa ]
2. Realizada por firma independente credenciada para emitir parecer formal de mercado (SOC 2). [ Interna / Externa ]
3. Fornece o maior grau de independência e credibilidade jurídica perante reguladores. [ Interna / Externa ]

**Sua Tarefa:**
Preencha a matriz.

---

### PBQ 99: Gestão de Vulnerabilidades e Janela de Patching
**Domínio:** Domínio 4.0 / 5.0: GRC

**Cenário do Lab / Simulação:**
Vulnerabilidade RCE de pontuação CVSS 10.0 identificada em servidor Web:
1. Nível de prioridade para correção? [ Crítica - Aplicação Imediata de Patch de Emergência ]
2. Se o patch exige reinicializar o servidor de produção, qual o procedimento formal? [ Criar RFC de Emergência, aprovar pelo e-CAB e notificar a operação ]
3. Se for um ataque Zero-Day sem patch oficial disponível, qual a medida compensatória? [ Criar uma regra de patching virtual no WAF / NIPS ]

**Sua Tarefa:**
Responda às 3 perguntas.

---

### PBQ 100: Plano Integrado de Segurança e Resumo da Prontidão do Candidato
**Domínio:** Domínio 1.0 ao 5.0: Todas as Áreas

**Cenário do Lab / Simulação:**
Mapeie os Domínios do exame aos seus pilares estratégicos:
1. Domínio 1.0 (12%) | 2. Domínio 2.0 (22%) | 3. Domínio 3.0 (18%) | 4. Domínio 4.0 (28%) | 5. Domínio 5.0 (20%)

- [   ] Governança de TI, gestão quantitativa de riscos (ALE/SLE), SOC 2, BCP/DRP e conformidade (LGPD/GDPR).
- [   ] Monitorar e correlacionar eventos via SIEM/SOAR, investigação forense com ordem de volatilidade e IAM/MFA.
- [   ] Projetar redes seguras com Zero Trust (PEP), nuvem (IaaS/PaaS/SaaS), SASE, microsegmentação e TPM/HSM.
- [   ] Conceitos fundamentais de segurança (Tríade CIA), categorias de controle, criptografia e PKI.
- [   ] Identificar vetores de ataque, malwares, engenharia social, vulnerabilidades Web (SQLi/XSS) e hardening.

**Sua Tarefa:**
Associe os domínios aos seus pilares.

---

## 🟢 PARTE 2: GABARITO OFICIAL E RESOLUÇÃO TÉCNICA DETALHADA (1 A 100)

Abaixo está a resolução explicada de cada uma das 100 simulações práticas do simulado:

### 📌 Resolução da PBQ 1: Configuração de Regras de Firewall e ACL de Borda
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
**Regra 1:** Origem: *Qualquer* | Destino: *192.168.10.5* | Porta/Protocolo: *TCP 80, 443 (HTTP/HTTPS)* | Ação: *PERMITIR (ALLOW)*
**Regra 2:** Origem: *Qualquer* | Destino: *192.168.10.10* | Porta/Protocolo: *TCP 25, 993 (SMTP/IMAPS)* | Ação: *PERMITIR (ALLOW)*
**Regra 3:** Origem: *10.0.0.0/8 (Rede Interna)* | Destino: *192.168.10.50* | Porta/Protocolo: *TCP 22 (SSH)* | Ação: *PERMITIR (ALLOW)*
**Regra 4:** Origem: *Qualquer* | Destino: *Qualquer* | Porta/Protocolo: *Qualquer* | Ação: *NEGAR TUDO (IMPLICIT DENY)*
*Explicação:* Acesso Web/Email é público nas portas padrão. O gerenciamento SSH deve ser restrito à rede interna. A regra final implementa a Negação Implícita (Implicit Deny).

---

### 📌 Resolução da PBQ 2: Componentes da Arquitetura Zero Trust (NIST SP 800-207)
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
**1 -> B** (Policy Engine toma a decisão lógica).
**2 -> D** (Policy Administrator gera credenciais/tokens de sessão).
**3 -> C** (PEP executa a liberação/bloqueio físico do tráfego).
**4 -> E** (Control Plane carrega sinalização de controle).
**5 -> A** (Data Plane carrega o tráfego do usuário).

---

### 📌 Resolução da PBQ 3: Configuração de Redes Definidas por Software (SDN)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
- **Plano de Dados (2):** Processa pacotes conforme regras sem decidir.
- **Plano de Controle (1):** Toma decisões lógicas centrais de roteamento e políticas.
- **Comutadores / Switches (4):** Executam o encaminhamento físico no Plano de Dados.
- **Controladores SDN (3):** Software centralizado que implementa a inteligência do Plano de Controle.

---

### 📌 Resolução da PBQ 4: Implementação de SASE e SD-WAN
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
**1 -> A (SD-WAN)**
**2 -> C (SWG)**
**3 -> B (CASB)**
**4 -> D (ZTNA)**
**5 -> E (FWaaS)**

---

### 📌 Resolução da PBQ 5: Dimensionamento de Servidores Proxy: Forward vs. Reverse
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. **Forward Proxy** (Gerencia tráfego de saída dos usuários).
2. **Reverse Proxy** (Gerencia tráfego de entrada para os servidores internos).
3. **Forward Proxy** (Oculta IPs de estações internas ao navegar).
4. **Reverse Proxy** (Faz SSL Offloading à frente dos servidores).
5. **Reverse Proxy** (Esconde a infraestrutura interna de clientes externos).

---

### 📌 Resolução da PBQ 6: Segregação de Rede e Microsegmentação
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
**1 -> B** (PCI-DSS exige microsegmentação rígida até entre servidores no mesmo segmento).
**2 -> C** (Wi-Fi de visitantes com Captive Portal e saída direta pra Internet sem rota interna).
**3 -> D** (IoT/Câmeras em VLAN isolada sem rota para a rede corporativa).
**4 -> A** (Rede de TI com acesso via Jump Server e MFA).

---

### 📌 Resolução da PBQ 7: Posicionamento de Sensores NIDS e NIPS
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. **NIPS na Posição 1:** Deve ser posicionado em linha (*In-line*) para conseguir analisar e **bloquear/descartar** o tráfego malicioso em tempo real.
2. **NIDS na Posição 2:** Deve ser conectado a uma porta SPAN/TAP para receber cópias do tráfego em modo passivo sem impactar a latência.
3. **Impacto de Falha na Posição 1:** Sem o recurso de *Bypass* (Fail-Open), a falha interromperá todo o tráfego de rede (Fail-Closed).
4. **Impacto de Falso Positivo:** Na Posição 1 (NIPS), um falso positivo bloqueia tráfego legítimo. Na Posição 2 (NIDS), gera apenas um alarme sem derrubar a conexão.

---

### 📌 Resolução da PBQ 8: Configuração de Bastion Host / Jump Server
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. **NÃO** (Conexões devem vir de VPN restrita).
2. **SIM** (MFA obrigatório).
3. **NÃO** (Desativar transferência de arquivos e área de transferência para evitar exfiltração).
4. **SIM** (Gravação de sessão e envio de logs para SIEM imutável).
5. **NÃO** (Bloquear acesso à Internet a partir do Jump Server).

---

### 📌 Resolução da PBQ 9: Sistemas In-Band vs. Out-of-Band (OOB) Management
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. **Out-of-Band (OOB)** (Opera de forma independente do plano de dados da rede).
2. **Conexão Serial via Modem Celular 4G/5G ou Linha Análoga** (Acesso direto à porta Console do equipamento).
3. **Isolamento de rede físico ou lógico estrito sem rota para a Internet pública**.

---

### 📌 Resolução da PBQ 10: Resiliência e Locais de Recuperação (Hot, Warm, Cold Site)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
**1 -> A (Hot Site)**
**2 -> C (Cold Site)**
**3 -> B (Warm Site)**
**4 -> D (Mobile Site)**

---

### 📌 Resolução da PBQ 11: Escolha do Algoritmo Criptográfico e Modo de Operação
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
1 -> B (AES-GCM)
2 -> C (Diffie-Hellman / ECDHE)
3 -> D (Perfect Forward Secrecy - PFS)
4 -> A (RSA / ECDSA)

---

### 📌 Resolução da PBQ 12: Hierarquia de Validação de Certificados: CRL vs. OCSP Stapling
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
1. CRL (Certificate Revocation List)
2. OCSP Padrão (Online Certificate Status Protocol)
3. OCSP Stapling (RFC 6066)

---

### 📌 Resolução da PBQ 13: Diferença entre Criptografia no Hardware: TPM vs. HSM
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
1. TPM
2. HSM
3. TPM
4. HSM

---

### 📌 Resolução da PBQ 14: Processo de Solicitação e Emissão de Certificado Digital (CSR & PKI)
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
1ª Etapa: B (Gera o par de chaves)
2ª Etapa: D (Cria e envia o CSR)
3ª Etapa: A (CA valida e assina)
4ª Etapa: C (Instala o certificado)

---

### 📌 Resolução da PBQ 15: Proteção de Dados: Mascaramento, Tokenização e Salting
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
- Salting de Senhas (3)
- Tokenização (2)
- Esteganografia (4)
- Mascaramento (1)

---

### 📌 Resolução da PBQ 16: Formato e Extensões de Certificados Digitais
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
1 -> B (.PFX / .P12)
2 -> A (.PEM / .CRT)
3 -> C (.DER)
4 -> D (.P7B)

---

### 📌 Resolução da PBQ 17: Sistemas de Arquivos e Criptografia em Repouso (FDE vs. File Level)
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
1. FDE
2. File-level
3. FDE
4. FDE

---

### 📌 Resolução da PBQ 18: Cálculo de Colisão e Propriedades de Hash
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
- Efeito Avalanche: Drástica e Imprevisível
- Resistência à Colisão: Entradas Diferentes gerando o Mesmo hash
- Irreversibilidade: Texto Claro de Origem

---

### 📌 Resolução da PBQ 19: Infraestrutura PKI: CAs Raiz, Intermediárias e Subordinadas
**Domínio:** Domínio 1.0: Conceitos Gerais de Segurança

**Gabarito e Solução do Lab:**
1. Offline e isolada da rede.
2. Para evitar o comprometimento da chave mestra da PKI.
3. CA Intermediária ou Subordinada.

---

### 📌 Resolução da PBQ 20: Protocolos Criptográficos de Rede Seguros vs. Legados Inseguros
**Domínio:** Domínio 1.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
1. SFTP (Porta 22) ou FTPS (Portas 989/990)
2. SSH (Porta 22)
3. HTTPS (Porta 443)
4. LDAPS (Porta 636)
5. SNMPv3 (Portas 161/162 com Autenticação e Cifra)

---

### 📌 Resolução da PBQ 21: Modelos de Controle de Acesso (RBAC, ABAC, MAC, DAC)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- DAC (4)
- RBAC (1)
- MAC (3)
- ABAC (2)

---

### 📌 Resolução da PBQ 22: Arquitetura AAA: RADIUS vs. TACACS+
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. TACACS+
2. RADIUS
3. TACACS+
4. RADIUS
5. TACACS+

---

### 📌 Resolução da PBQ 23: Federação de Identidades e SSO: SAML vs. OAuth 2.0 vs. OIDC
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1 -> A (SAML 2.0)
2 -> B (OAuth 2.0)
3 -> C (OpenID Connect - OIDC)

---

### 📌 Resolução da PBQ 24: Análise e Configuração de Fatores de Autenticação (MFA)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- Fator 1 (Conhecimento): E (Senha/PIN)
- Fator 2 (Posse): B (Token FIDO2 / YubiKey)
- Fator 3 (Inerência): D (Digital / Íris / Face)
- Fator 4 (Localização): C (GPS / IP)
- Fator 5 (Comportamento): A (Keystroke Dynamics)

---

### 📌 Resolução da PBQ 25: Autenticação Resistente a Phishing: FIDO2 / WebAuthn
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Porque o usuário pode ser induzido a digitar o código em um site falso (Ataques AiTM).
2. FIDO2 / WebAuthn (A chave privada é vinculada ao domínio real do navegador).
3. Chave de Segurança USB de Hardware (Hardware Security Key / Passkey).

---

### 📌 Resolução da PBQ 26: Configuração de Gestão de Contas e Privilégios (PAM)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Password Vaulting / Rotação Automática
2. Just-In-Time (JIT) Access
3. Session Recording / Monitoramento de Sessão

---

### 📌 Resolução da PBQ 27: Controles de RH e Separação de Funções (Separation of Duties)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- Separação de Deveres (1) -> Divide o processo entre pessoas
- Controle Duplo (2) -> Exige 2 operadores simultâneos
- Férias Obrigatórias (3) -> Afasta para expor fraudes contínuas
- Rodízio de Funções (4) -> Alterna atribuições periodicamente

---

### 📌 Resolução da PBQ 28: Acesso Baseado em Políticas de Condição de Contexto (Conditional Access)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- Condição de Dispositivo: Apenas Dispositivos Corporativos Gerenciados (Compliant)
- Condição de Localização: IPs Autorizados da Sede ou Países Permitidos
- Pontuação de Risco do Login: Baixo
- Ação Requerida: Exigir MFA + Aceite de Termos de Uso

---

### 📌 Resolução da PBQ 29: Protocolo Kerberos e Ticket-Granting Ticket (TGT)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1ª Etapa: C (Inicia solicitação AS-REQ)
2ª Etapa: B (Recebe TGT do KDC)
3ª Etapa: D (Apresenta TGT e recebe ST do TGS)
4ª Etapa: A (Apresenta ST ao servidor de destino)

---

### 📌 Resolução da PBQ 30: Ataques de Autenticação: Password Spraying vs. Credential Stuffing
**Domínio:** Domínio 2.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
1. Password Spraying
2. Credential Stuffing
- Mitigação Credential Stuffing: Exigir MFA obrigatório.
- Mitigação Password Spraying: Monitorar velocidade por senha única e exigir MFA.

---

### 📌 Resolução da PBQ 31: Análise de Código Vulnerável e Injeção Web (Cross-Site Scripting - XSS)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. XSS Armazenado (Stored)
2. XSS Refletido (Reflected)
3. XSS Baseado em DOM (DOM-Based)
Contramedida: Ativar atributo HttpOnly nos cookies de sessão.

---

### 📌 Resolução da PBQ 32: Ataques Server-Side Request Forgery (SSRF) vs. CSRF
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Cenário A (SSRF)
2. Cenário B (CSRF)
3. Tokens Anti-CSRF Únicos e Imprevisíveis.

---

### 📌 Resolução da PBQ 33: Ataques de Estouro de Buffer (Buffer Overflow) e Proteções de Compilação
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- DEP / NX (3)
- ASLR (2)
- Stack Canaries (1)

---

### 📌 Resolução da PBQ 34: Condições de Corrida: Race Conditions (TOC/TOU)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Time-of-Check to Time-of-Use (TOC/TOU)
2. Enviando requisições concorrentes em milissegundos
3. Operações Atômicas e Transações com Bloqueio de Banco de Dados (Mutex)

---

### 📌 Resolução da PBQ 35: Modelos de Nuvem e Matriz de Responsabilidade Compartilhada
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. Cliente (IaaS)
2. Provedor (PaaS)
3. Provedor (Todos)
4. Cliente (SaaS)

---

### 📌 Resolução da PBQ 36: Ataques XML External Entity (XXE) e Injeção de Comando
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. XXE (XML External Entity)
2. Leitura de arquivos confidenciais do sistema operacional (/etc/passwd)
3. Desativar a resolução de entidades externas DTD no parser XML

---

### 📌 Resolução da PBQ 37: Segurança em Microserviços, Conteinerização e Docker
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. INCORRETO
2. CORRETO
3. CORRETO
4. INCORRETO

---

### 📌 Resolução da PBQ 38: Infraestrutura como Código (IaC) e Drift de Configuração
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. Configuration Drift (Desvio de Configuração)
2. Sobrescrevendo a alteração manual e re-aplicando o estado declarativo
3. Imutabilidade, padronização, auditoria e rastreabilidade via Git

---

### 📌 Resolução da PBQ 39: Injeção de Comando de Sistema Operacional (Command Injection)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Command Injection (Injeção de Comando do SO)
2. Executa o segundo comando em sequência no shell do SO
3. Evitar chamadas de shell do SO e sanitizar a entrada com regex

---

### 📌 Resolução da PBQ 40: Ataques de Travessia de Diretório (Directory / Path Traversal)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Directory / Path Traversal
2. Sobe um nível no diretório do sistema de arquivos
3. Sanitizar entradas e usar chaves indiretas de mapeamento

---

### 📌 Resolução da PBQ 41: Taxonomia de Ataques de Phishing e Vetores de Contato
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- Waterhole (5)
- Smishing (4)
- Whaling (2)
- Vishing (3)
- Spear Phishing (1)

---

### 📌 Resolução da PBQ 42: Técnicas de Evasão em Memória: Process Hollowing vs. DLL Injection
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Process Hollowing
2. DLL Injection
3. Execução em memória sem criar arquivo no disco (Fileless Malware)

---

### 📌 Resolução da PBQ 43: Ameaças Físicas: Tailgating, Piggybacking e Shoulder Surfing
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- Cenário 1: Tailgating | Controle: Catraca Mantrap (Eclusa)
- Cenário 2: Shoulder Surfing | Controle: Filtro de Privacidade na Tela

---

### 📌 Resolução da PBQ 44: Tipos de Malware: Ransomware, Rootkit, Logic Bomb e Spyware
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- Logic Bomb (3)
- Rootkit (2)
- Ransomware (1)
- Spyware (4)

---

### 📌 Resolução da PBQ 45: Ataques de Engenharia Social com IA e Deepfakes
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Deepfake
2. Autoridade e Urgência
3. Validação fora de banda (Out-of-band Verification) com aprovação dupla

---

### 📌 Resolução da PBQ 46: Análise de Ataques Typosquatting e Combôsquatting
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Combosquatting
2. Typosquatting
3. Combosquatting
Contramedida: Registrar variações de marca e monitorar DNS via Threat Intelligence

---

### 📌 Resolução da PBQ 47: Software Inseguro e Sombra de TI (Shadow IT)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
1. Shadow IT (TI Fantasma)
2. CASB (Cloud Access Security Broker)
3. Vazamento não monitorado de dados confidenciais e não conformidade regulatória

---

### 📌 Resolução da PBQ 48: Insiders Maliciosos vs. Insiders Negligentes
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- Cenário 1: Insider Malicioso | Controle: DLP + Bloqueio de USB + Revogação de acesso (PAM)
- Cenário 2: Insider Negligente | Controle: DLP + Treinamento de Conscientização

---

### 📌 Resolução da PBQ 49: Ataques Supply Chain (Cadeia de Suprimentos)
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Ataque à Cadeia de Suprimentos (Supply Chain Attack)
2. Porque a atualização vem assinada por uma fonte confiável homologada
3. Avaliação de Due Diligence, exigência de SBOM e análise de integridade

---

### 📌 Resolução da PBQ 50: Criptojacking e Abuso de Recursos de Computação
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
1. Cryptojacking
2. Custo financeiro elevado por auto-scaling e degradação do serviço
3. Interromper o processo, isolar a instância, revogar credenciais e investigar vetor inicial

---

### 📌 Resolução da PBQ 51: Análise de Ataques em Redes Wi-Fi: Rogue AP vs. Evil Twin
**Domínio:** Domínio 2.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
1. Cenário A (Rogue AP)
2. Cenário B (Evil Twin)
3. WIPS (Wireless Intrusion Prevention System)

---

### 📌 Resolução da PBQ 52: Ataques de Desautenticação (Deauthentication Attack) e WPA3 SAE
**Domínio:** Domínio 2.0 / 3.0: Arquitetura

**Gabarito e Solução do Lab:**
1. Quadros de gerenciamento no WPA2 são transmitidos sem criptografia ou autenticação
2. PMF (Protected Management Frames / IEEE 802.11w)
3. SAE (Simultaneous Authentication of Equals / Algoritmo Dragonfly)

---

### 📌 Resolução da PBQ 53: Modelos de Implantação Móvel: BYOD, COPE, CYOD e Corporate-Owned
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
- COPE (2)
- BYOD (1)
- CYOD (3)
- Corporate-Owned (4)

---

### 📌 Resolução da PBQ 54: Recursos de Gerenciamento Móvel (MDM / MAM) e Wipe Remoto
**Domínio:** Domínio 3.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
1ª Ação: C (Remote Wipe imediato)
2ª Ação: D (Revogar tokens de sessão e certificados no IdP)
3ª Ação: A (Bloqueio de tela)
4ª Ação: B (Bloquear IMEI na operadora)

---

### 📌 Resolução da PBQ 55: Hardening de Host: Lista de Aplicações Permitidas (Application Allowlisting)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Lista de Aplicações Permitidas (Application Allowlisting)
2. Assinatura Digital do Fabricante (Publisher Rule) ou Hash de Arquivo (File Hash)
3. Porque atacantes com escrita na pasta podem substituir o binário mantendo o caminho

---

### 📌 Resolução da PBQ 56: Capacidades de Soluções Endpoint: EDR vs. XDR vs. Antivírus Tradicional
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1 -> B (EDR)
2 -> A (Antivírus Tradicional)
3 -> C (XDR)

---

### 📌 Resolução da PBQ 57: Proteção de Navegação e Isolamento de Sessão (Browser Isolation / RBI)
**Domínio:** Domínio 3.0: Arquitetura de Segurança

**Gabarito e Solução do Lab:**
1. RBI (Remote Browser Isolation)
2. O código malicioso executa e é contido no ambiente isolado da nuvem, sendo destruído no encerramento da sessão

---

### 📌 Resolução da PBQ 58: Proteção de Dispositivos de Armazenamento e Desativação USB
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Configuração do Computador -> Modelos Administrativos -> Sistema -> Acesso de Armazenamento Removível
2. Cadastrar o Hardware ID (VID & PID) específico na lista de permissões da GPO

---

### 📌 Resolução da PBQ 59: Ataques Bluetooth: Bluejacking vs. Bluesnarfing
**Domínio:** Domínio 2.0: Ameaças e Vulnerabilidades

**Gabarito e Solução do Lab:**
- Cenário 1: Bluejacking
- Cenário 2: Bluesnarfing
Contramedida: Manter o Bluetooth Não Descobrível e desativado quando não utilizado

---

### 📌 Resolução da PBQ 60: Sistemas de Arquivos de Segurança e Criptografia em Nuvem (DLP / CASB)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Email Gateway DLP (ou Endpoint DLP)
2. CASB (Cloud Access Security Broker)

---

### 📌 Resolução da PBQ 61: Fases do Ciclo de Vida de Resposta a Incidentes (NIST SP 800-61)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1ª Fase: B (Preparação)
2ª Fase: D (Detecção e Análise)
3ª Fase: A (Erradicação e Recuperação / Contenção)
4ª Fase: C (Atividades Pós-Incidente / Lições Aprendidas)

---

### 📌 Resolução da PBQ 62: Mapeamento das Ações do Analista de Incidentes (Contenção vs. Erradicação)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Contenção
2. Erradicação
3. Recuperação
4. Lições Aprendidas

---

### 📌 Resolução da PBQ 63: Ordem de Volatilidade da Evidência Digital (RFC 3227)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1º: C (Registradores e Cache)
2º: B (Memória RAM)
3º: E (Tabela de Roteamento e Cache ARP)
4º: A (Disco Rígido / SSD)
5º: D (Backups em Fita)

---

### 📌 Resolução da PBQ 64: Uso do Write Blocker e Clonagem Forense (Bit-stream Image)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Bloqueador de Escrita em Hardware (Hardware Write Blocker)
2. Impedir qualquer alteração de dados/metadados no disco original
3. Imagem Bit-a-Bit (Bit-stream Image)
4. Comparando os valores de Hash (SHA-256 / MD5)

---

### 📌 Resolução da PBQ 65: Formulário de Cadeia de Custódia (Chain of Custody)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- Coletado Por: Nome, Cargo e Assinatura do Perito
- Armazenamento: Cofre de Evidências com Acesso Restrito e Auditoria
- Transferência: Data, Hora, Motivo e Assinaturas de ambos os envolvidos

---

### 📌 Resolução da PBQ 66: Coleta e Extração de Memória Volátil (RAM Dump)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. NÃO
2. Porque a memória RAM é volátil e o corte de energia apaga o conteúdo
3. FTK Imager / WinPmem / Lime
4. Volatility Framework

---

### 📌 Resolução da PBQ 67: Prevenção de Alteração e Retenção Legal (Legal Hold)
**Domínio:** Domínio 4.0 / 5.0: GRC

**Gabarito e Solução do Lab:**
1. CORRETO
2. INCORRETO
3. CORRETO

---

### 📌 Resolução da PBQ 68: Análise Forense de Cabeçalho de E-mail (Email Header Analysis)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. NÃO
2. O campo Authentication-Results: spf=fail e o IP de origem no primeiro salto Received
3. Return-Path

---

### 📌 Resolução da PBQ 69: Auditoria e Integridade de Logs de Servidores
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Servidor Syslog Centralizado / SIEM com retenção imutável WORM
2. Forward Secure Logging e Assinatura Hashing de Blocos em Cadeia

---

### 📌 Resolução da PBQ 70: Indicadores de Comprometimento (IOCs) vs. Indicadores de Ataque (IOA)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
1. IOC
2. IOA
3. IOC

---

### 📌 Resolução da PBQ 71: Análise de Logs do SIEM e Correlação de Eventos de Segurança
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Password Spraying
2. Comprometimento de Conta (Account Takeover) com sucesso
3. Elevação Local de Privilégios no host
4. Desativar a conta no AD, revogar tokens de sessão e isolar o host

---

### 📌 Resolução da PBQ 72: Orquestração de Segurança e Playbooks Automáticos no SOAR
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1ª Etapa: B (Envia o anexo para o Sandbox)
2ª Etapa: A (Bloqueia Hash no EDR e IP no Firewall)
3ª Etapa: D (Purga o e-mail de todas as outras caixas)
4ª Etapa: C (Notifica o SOC e encerra o chamado)

---

### 📌 Resolução da PBQ 73: Monitoramento de Integridade de Arquivos (FIM - File Integrity Monitoring)
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Substituição do binário legítimo do SSH por versão trojanizada com backdoor
2. Integridade
3. Isolar o servidor da rede, preservar evidências para forense e restaurar fonte limpa

---

### 📌 Resolução da PBQ 74: Análise de Tráfego de Rede via NetFlow / IPFIX
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Exfiltração Massiva de Dados (Data Exfiltration)
2. NÃO
3. O NetFlow coleta metadados estatísticos do fluxo sem salvar o payload de dados

---

### 📌 Resolução da PBQ 75: Framework MITRE ATT&CK e Mapeamento de Táticas
**Domínio:** Domínio 2.0 / 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- Persistence (2)
- Lateral Movement (5)
- Initial Access (1)
- Defense Evasion (4)
- Privilege Escalation (3)

---

### 📌 Resolução da PBQ 76: Fontes de Inteligência sobre Ameaças (Threat Intelligence Feeds)
**Domínio:** Domínio 2.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
1 -> C (ISAC)
2 -> A (OSINT)
3 -> B (Feed Comercial Pago)

---

### 📌 Resolução da PBQ 77: Análise de Logs de Firewall de Borda e Bloqueio de Portas
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. SMB (Server Message Block) / Porta TCP 445
2. Propagação automática de Worms e Ransomware (WannaCry / EternalBlue)
3. Bloquear todo tráfego público vindo da Internet com destino às portas TCP 139 e 445 na borda

---

### 📌 Resolução da PBQ 78: Análise de Logs de Antivírus e Ações de Quarentena
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. NÃO (O arquivo está isolado sem permissão de execução)
2. Threat Hunting da mesma Hash em todas as estações da rede
3. Bloquear a Hash do anexo e o remetente no Gateway de E-mail

---

### 📌 Resolução da PBQ 79: Tabela de Correlação de Eventos de Autenticação
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
- Event ID 4720 (Criação de conta)
- Event ID 4625 (Falha de logon)
- Event ID 4624 (Logon bem-sucedido)
- Event ID 4672 (Logon com privilégios especiais)

---

### 📌 Resolução da PBQ 80: Varredura e Mapeamento com Nmap e Interpretação de Portas
**Domínio:** Domínio 4.0: Operações de Segurança

**Gabarito e Solução do Lab:**
1. Porta 21 (FTP)
2. Porta 3389 (RDP)
3. Bloquear exposição pública da porta 3389 e exigir acesso via VPN com MFA e NLA

---

### 📌 Resolução da PBQ 81: Cálculo Quantitativo de Risco (SLE, ARO e ALE)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. SLE = R$ 200.000 * 0,30 = R$ 60.000
2. ALE = R$ 60.000 * 0,1 = R$ 6.000 por ano
3. SIM (Custo de R$ 4.000/ano é menor que o risco anualizado de R$ 6.000/ano)

---

### 📌 Resolução da PBQ 82: Métricas de Continuidade de Negócio: RTO vs. RPO vs. MTTR vs. MTBF
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- RPO (2)
- RTO (1)
- MTBF (4)
- MTTR (3)

---

### 📌 Resolução da PBQ 83: Estratégias de Resposta ao Risco (Risk Response Strategies)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- Evitação (4)
- Transferência (2)
- Mitigação (1)
- Aceitação (3)

---

### 📌 Resolução da PBQ 84: Avaliação de Riscos de Terceiros e Relatórios SOC
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. SOC 3
2. SOC 1
3. SOC 2 Type II

---

### 📌 Resolução da PBQ 85: Exercícios de Continuidade: Tabletop vs. Functional vs. Full-Scale
**Domínio:** Domínio 3.0 / 5.0: GRC

**Gabarito e Solução do Lab:**
- Tabletop Exercise (1)
- Full-Scale Test (3)
- Functional Test (2)

---

### 📌 Resolução da PBQ 86: Análise de Impacto no Negócio (BIA - Business Impact Analysis)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. VERDADEIRO
2. VERDADEIRO
3. FALSO
4. VERDADEIRO

---

### 📌 Resolução da PBQ 87: Tipos de Backups: Total, Incremental e Diferencial
**Domínio:** Domínio 3.0 / 4.0: Operações

**Gabarito e Solução do Lab:**
- Incremental: Exige Total de Domingo + Todos os Incrementais em ordem | Backup rápido | Restauração mais lenta
- Diferencial: Exige Total de Domingo + Apenas o último Diferencial de Quarta | Restauração mais rápida que o Incremental

---

### 📌 Resolução da PBQ 88: Gestão de Riscos de Terceiros e Acordos Contratuais
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- NDA (3)
- SLA (1)
- MOU (2)
- BPA (4)

---

### 📌 Resolução da PBQ 89: Gerenciamento de Mudanças (Change Management) e Plano de Rollback
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1ª Etapa: D (Registra a RFC)
2ª Etapa: B (Testa em homologação e elabora Plano de Rollback)
3ª Etapa: A (Submete para análise do CAB)
4ª Etapa: C (Aplica na janela e testa pós-implantação)

---

### 📌 Resolução da PBQ 90: Modelos de Governança: CobIT, ITIL, NIST CSF e ISO/IEC 27001
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1 -> A (ISO/IEC 27001)
2 -> B (NIST CSF v2.0)
3 -> D (COBIT)
4 -> C (ITIL v4)

---

### 📌 Resolução da PBQ 91: Papéis e Responsabilidades sobre Dados (Data Roles)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- Data Processor (4)
- Data Owner (1)
- Data Custodian (2)
- DPO / Encarregado (3)

---

### 📌 Resolução da PBQ 92: Conceito de Privacidade por Design (Privacy by Design)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. Minimização de Dados
2. Solicitar estritamente os dados necessários para a finalidade informada

---

### 📌 Resolução da PBQ 93: Análise de Impacto na Proteção de Dados (DPIA / RIPD)
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. Avaliação de Impacto na Proteção de Dados (DPIA / RIPD)
2. Descrever o processamento sensível, avaliar necessidade/proporcionalidade e mapear riscos com mitigações
3. O Encarregado de Dados (DPO), equipe de TI e representantes dos titulares

---

### 📌 Resolução da PBQ 94: Mapeamento de Leis de Privacidade e Padrões Setoriais
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- GDPR / LGPD (3)
- PCI-DSS v4.0 (1)
- HIPAA (2)
- SWIFT CSP (4)

---

### 📌 Resolução da PBQ 95: Classificação de Dados e Rótulos de Sensibilidade
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1 -> D (Restrito / Segredo Comercial)
2 -> B (Interno)
3 -> A (Público)
4 -> C (Confidencial)

---

### 📌 Resolução da PBQ 96: Técnicas de Destruição e Sanitização de Mídias
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
- Cryptographic Erasure (2)
- Trituração Física (3)
- Degaussing (1)
- Sanitização por Software (4)

---

### 📌 Resolução da PBQ 97: Transferência Internacional de Dados e Soberania dos Dados
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. Os dados estão sujeitos às leis e jurisdições do país onde estão fisicamente armazenados
2. Configurando o bloqueio de região (Region / Geo-Locking)
3. SIM, a localização física do servidor estabelece a jurisdição do governo local sobre o equipamento

---

### 📌 Resolução da PBQ 98: Auditoria Interna vs. Auditoria Externa
**Domínio:** Domínio 5.0: GRC

**Gabarito e Solução do Lab:**
1. Auditoria Interna
2. Auditoria Externa
3. Auditoria Externa

---

### 📌 Resolução da PBQ 99: Gestão de Vulnerabilidades e Janela de Patching
**Domínio:** Domínio 4.0 / 5.0: GRC

**Gabarito e Solução do Lab:**
1. Crítica - Aplicação Imediata de Patch de Emergência
2. Elaborar RFC de Emergência, obter aprovação do e-CAB e notificar a operação
3. Criar regra de correção virtual (Virtual Patching) no WAF ou NIPS

---

### 📌 Resolução da PBQ 100: Plano Integrado de Segurança e Resumo da Prontidão do Candidato
**Domínio:** Domínio 1.0 ao 5.0: Todas as Áreas

**Gabarito e Solução do Lab:**
- Domínio 5.0 (5)
- Domínio 4.0 (4)
- Domínio 3.0 (3)
- Domínio 1.0 (1)
- Domínio 2.0 (2)

---


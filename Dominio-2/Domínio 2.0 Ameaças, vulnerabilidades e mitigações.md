# Guia Security+ SY0-701 — Domínio 2.0: Ameaças, vulnerabilidades e mitigações

Oct 7, 2026 · @Pedro Henrique Ferraz

Material de estudo para a certificação CompTIA Security+ (SY0-701). O Domínio 2.0 vale 22% da prova — o maior peso — e cobre quem ataca, por onde ataca, o que explora, como se reconhece o ataque e como se mitiga. Todos os gabaritos ficam na última seção.

## Como usar este guia

Este material cobre todo o Domínio 2.0 da CompTIA Security+ SY0-701 com o mesmo método do Domínio 1.0: cada conceito segue ideia simples, definição técnica, exemplo real, aplicação profissional (SOC, Blue Team, Red Team, redes e infraestrutura), comparação, memorização, pegadinhas, questão no estilo da prova, raciocínio de eliminação e resumo de alta retenção.

**Legenda de origem do conteúdo:**

| Marca | Significado |
| --- | --- |
| \[OFICIAL\] | Item que consta literalmente nos objetivos SY0-701 da CompTIA |
| \[COMPLEMENTAR\] | Conhecimento de apoio para entender o item oficial |
| \[DIDÁTICO\] | Exemplo, analogia ou cenário criado para fixar o conceito |

**Termos em inglês:** formato inglês → tradução → significado → como cai na prova. A CompTIA redige o exame em inglês e muitas questões dependem de reconhecer o termo original.

**Mini-desafios e simulado:** nenhuma resposta aparece junto da pergunta. Todos os gabaritos comentados ficam na última seção.

**Por que o Domínio 2.0 é o mais importante:** com 22% do exame, é o de maior peso. Ele é a espinha dorsal das questões baseadas em cenário (PBQs), porque exige identificar o ataque a partir de sintomas, logs e contexto. Dominar o vocabulário de ataques e indicadores aqui rende pontos em toda a prova.

**Estrutura do Domínio 2.0 (peso 22%):** cinco objetivos oficiais — 2.1 Motivações e atores de ameaças; 2.2 Vetores de ameaça e superfícies de ataque; 2.3 Tipos de vulnerabilidades; 2.4 Indicadores de atividade maliciosa; 2.5 Técnicas de mitigação.

## 2.1 Atores de ameaças e motivações \[OFICIAL\]

A prova cobra reconhecer quem é o atacante (ator), suas características (atributos) e por que ele ataca (motivação). A chave é casar o perfil do ator com a motivação descrita no cenário.

### Atores de ameaças (Threat actors)

- Estado-nação (Nation-state): patrocinado por governo; altíssimo recurso e sofisticação; paciente e furtivo. Associado a APT (Advanced Persistent Threat). Motivações típicas: espionagem, guerra, interrupção.
- Invasor não qualificado (Unskilled attacker / script kiddie): usa ferramentas prontas sem entender a fundo; baixa sofisticação. Motivação: caos, status, diversão.
- Hacktivista (Hacktivist): motivado por causa política/ideológica; quer visibilidade. Motivações: crenças filosóficas/políticas, interrupção.
- Ameaça interna (Insider threat): pessoa de dentro (funcionário, terceiro) com acesso legítimo. Motivações: vingança, ganho financeiro, erro não intencional.
- Crime organizado (Organized crime): grupos profissionais com fins lucrativos; alta capacidade. Motivação: ganho financeiro.
- Shadow IT: uso de TI não autorizada pela organização (apps/serviços fora da governança). Não é malicioso por definição, mas cria risco. Motivação: conveniência/produtividade.

### Atributos dos atores (Threat actor attributes)

- Interno vs externo (internal/external): está dentro ou fora da organização.
- Recursos/financiamento (resources/funding): quanto dinheiro e infraestrutura o ator tem.
- Nível de sofisticação/capacidade (sophistication/capability): quão avançadas são suas técnicas.

### Motivações (Motivations)

Exfiltração de dados, espionagem, interrupção do serviço, chantagem, ganhos financeiros, crenças filosóficas/políticas, ética, vingança, perturbação/caos e guerra. A prova associa cada motivação a um perfil de ator.

### Representação visual sugerida \[DIDÁTICO\]

Mapa 2x2 posicionando os atores por sofisticação (baixa→alta) e recurso/financiamento (baixo→alto): script kiddie no canto baixo-baixo; estado-nação no alto-alto; crime organizado no alto-alto (lucro); hacktivista no meio; insider variável. (Renderizado como imagem após esta seção.)

&#91;embedded content: Atores de ameaça por sofisticação e recurso\]

### Comparação — o que mais confunde

- Estado-nação vs Crime organizado: ambos são sofisticados e bem financiados, mas o estado-nação busca espionagem/guerra e o crime organizado busca lucro. A motivação decide.
- Hacktivista vs Estado-nação: ambos podem ter motivação política, mas o hacktivista é ideológico/visibilidade e geralmente menos recurso; o estado-nação é patrocinado e furtivo.
- Insider vs externo: o insider já tem acesso legítimo — isso o torna especialmente perigoso e difícil de detectar.
- Shadow IT não é um atacante: é um risco criado por uso não autorizado, não um adversário com intenção maliciosa.

### Memorização \[DIDÁTICO\]

- Estado-nação = APT = paciente, furtivo, espionagem/guerra.
- Crime organizado = dinheiro.
- Hacktivista = causa/ideologia.
- Script kiddie = ferramentas prontas, caos/status.
- Insider = acesso de dentro (pode ser vingança ou erro).
- Shadow IT = TI fora das regras (risco, não ataque).

### Pegadinhas típicas da prova

1. Marcar estado-nação quando a motivação é claramente lucro — nesse caso é crime organizado.
2. Tratar shadow IT como um ator malicioso — é um risco de governança.
3. Esquecer que o insider tem acesso legítimo, o que muda a estratégia de detecção.
4. Confundir sofisticação com motivação: um ator muito capaz pode ter qualquer motivação.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve um ataque e seus sinais (recursos, alvo, objetivo) e pede o ator mais provável. Raciocínio: primeiro leia a motivação (lucro? espionagem? ideologia? caos?) e o nível de recurso/sofisticação; depois case com o perfil. Alvo estratégico + furtividade + alto recurso = estado-nação; lucro + profissionalismo = crime organizado; causa pública = hacktivista.

### Mini-desafio 2.1-A

Um grupo altamente financiado e furtivo compromete uma agência governamental e permanece meses sem ser detectado, coletando documentos sigilosos. Qual ator é o mais provável?

1. Script kiddie
2. Hacktivista
3. Estado-nação (APT)
4. Shadow IT

### Mini-desafio 2.1-B

Um funcionário insatisfeito, prestes a ser demitido, copia dados de clientes para prejudicar a empresa. Qual categoria de ator e motivação melhor descreve o caso?

1. Estado-nação motivado por espionagem
2. Ameaça interna motivada por vingança
3. Crime organizado motivado por lucro
4. Hacktivista motivado por ideologia

### Resumo de alta retenção — atores e motivações

- PRECISO SABER: atores (estado-nação/APT, script kiddie, hacktivista, insider, crime organizado, shadow IT); atributos (interno/externo, recurso, sofisticação); motivações (lucro, espionagem, ideologia, vingança, caos, guerra).
- PRECISO RECONHECER: furtivo+alto recurso+governo→estado-nação; lucro+profissional→crime organizado; causa→hacktivista; acesso de dentro→insider.
- NÃO CONFUNDIR: estado-nação (espionagem) ≠ crime organizado (lucro); shadow IT (risco) ≠ atacante.
- PEGADINHAS: lucro não é estado-nação; sofisticação ≠ motivação.
- MEMORIZAÇÃO: APT=paciente/furtivo; crime=dinheiro; hacktivista=causa.
- NA PRÁTICA: o SOC usa threat intelligence para atribuir ataques a perfis (TTPs); insiders exigem controles de UEBA e DLP.

## 2.2 Vetores de ameaça e superfícies de ataque \[OFICIAL\]

Vetor de ameaça (threat vector) é o caminho pelo qual o ataque chega; superfície de ataque (attack surface) é o conjunto de pontos expostos. A prova cobra reconhecer o vetor usado em um cenário, com forte ênfase em engenharia social.

### Vetores baseados em mensagens

- E-mail: principal vetor de phishing e malware.
- SMS (Short Message Service): base do smishing.
- Mensagens instantâneas (IM): apps de chat usados para links e arquivos maliciosos.

### Outros vetores técnicos

- Baseado em imagem (image-based): código malicioso embutido em arquivos de imagem.
- Baseado em arquivo (file-based): documentos com macros, PDFs maliciosos.
- Chamada de voz (voice call): base do vishing.
- Dispositivo removível (removable device): pen drive infectado (ataque do "USB no estacionamento").
- Software vulnerável (vulnerable software): baseado no cliente (client-based, com agente instalado) vs sem agente (agentless).
- Sistemas e aplicativos não suportados (unsupported systems/applications): sem patches, fim de vida útil.
- Redes inseguras (unsecure networks): sem fio, com fio e Bluetooth.
- Portas de serviço abertas (open service ports): serviços expostos desnecessariamente.
- Credenciais padrão (default credentials): senhas de fábrica não trocadas.
- Cadeia de suprimento (supply chain): MSPs, fornecedores (vendors) e provedores (suppliers) comprometidos como porta de entrada.

### Vetores humanos / engenharia social (Social engineering)

O mais cobrado do objetivo. Explora a confiança e o comportamento humano.

- Phishing: e-mail fraudulento em massa para roubar credenciais/dados.
- Vishing (voice phishing): golpe por chamada de voz.
- Smishing (SMS phishing): golpe por SMS.
- Informação errada/desinformação (misinformation/disinformation): espalhar conteúdo falso (erro involuntário vs intencional).
- Personificação (impersonation): fingir ser outra pessoa.
- Comprometimento de e-mail comercial (BEC, Business Email Compromise): fraude via conta de e-mail corporativa comprometida ou falsificada, geralmente mirando pagamentos.
- Pretexting: criar um pretexto/história convincente para obter informação.
- Watering hole: comprometer um site legítimo que o alvo costuma visitar.
- Personificação da marca (brand impersonation): imitar uma marca confiável.
- Typosquatting: registrar domínios com erros de digitação (ex.: gooogle.com) para capturar vítimas.

### Representação visual sugerida \[DIDÁTICO\]

Tabela/painel das três variantes de phishing por canal: Phishing (e-mail), Vishing (voz), Smishing (SMS) — mesma técnica, canal diferente. (Renderizado como imagem após esta seção.)

&#91;embedded content: Phishing, vishing e smishing · mesma técnica, canais diferentes\]

### Comparação — o que mais confunde

- Phishing × Vishing × Smishing: a técnica é a mesma (enganar para roubar), muda o canal — e-mail, voz, SMS.
- Spear phishing × Whaling \[COMPLEMENTAR\]: spear phishing é direcionado a um alvo específico; whaling mira um executivo de alto escalão. (Não listados literalmente, mas úteis.)
- Pretexting × Impersonation: pretexting é a história/pretexto inventado; impersonation é fingir ser alguém específico. Frequentemente aparecem juntos.
- Misinformation × Disinformation: misinformation é falsidade sem intenção de enganar; disinformation é intencional.
- Typosquatting × Watering hole: typosquatting usa um domínio parecido com erro de digitação; watering hole compromete um site legítimo e confiável que o alvo já visita.
- Supply chain: o ataque entra por um terceiro confiável (fornecedor/MSP), não diretamente pelo alvo.

### Memorização \[DIDÁTICO\]

- phISHING = e-mail; vISHING = voz (V de voice); smISHING = SMS. Mesma raiz "ishing", canais diferentes.
- BEC = e-mail corporativo + fraude de pagamento.
- Watering hole = "poço d'água": o predador espera onde a presa bebe (site que ela visita).
- Typosquatting = erro de digitação no domínio.

### Pegadinhas típicas da prova

1. Trocar vishing por smishing (voz vs SMS). Leia o canal com atenção.
2. Chamar de phishing um golpe por voz (é vishing) ou por SMS (é smishing).
3. Confundir watering hole com typosquatting — site legítimo comprometido vs domínio falso parecido.
4. Tratar misinformation como sempre intencional — só disinformation é intencional.
5. Esquecer que o vetor de cadeia de suprimento entra por um terceiro confiável.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve como o ataque chegou (um e-mail, uma ligação, um pen drive, um site) e pede o vetor/técnica. Raciocínio: identifique o canal e a tática. Canal de voz → vishing; SMS → smishing; site confiável comprometido → watering hole; domínio parecido com erro → typosquatting; fraude por e-mail corporativo mirando pagamento → BEC.

### Mini-desafio 2.2-A

Um atacante liga para a recepcionista fingindo ser o técnico de TI e pede a senha dela para "resolver um problema no sistema". Qual técnica de engenharia social está sendo usada?

1. Smishing
2. Vishing
3. Watering hole
4. Typosquatting

### Mini-desafio 2.2-B

Um grupo compromete um site de notícias legítimo muito acessado pelos funcionários de uma empresa-alvo, implantando malware que infecta apenas visitantes daquela empresa. Qual vetor foi usado?

1. Phishing
2. Typosquatting
3. Watering hole
4. BEC

### Resumo de alta retenção — vetores e engenharia social

- PRECISO SABER: vetores (mensagens, imagem/arquivo, voz, USB, software vulnerável, redes inseguras, portas abertas, credenciais padrão, cadeia de suprimento); engenharia social (phishing/vishing/smishing, BEC, pretexting, impersonation, watering hole, typosquatting, brand impersonation, mis/disinformation).
- PRECISO RECONHECER: voz→vishing; SMS→smishing; site confiável comprometido→watering hole; domínio com erro→typosquatting; fraude por e-mail corporativo→BEC.
- NÃO CONFUNDIR: canais do phishing (e-mail/voz/SMS); watering hole ≠ typosquatting; misinformation (sem intenção) ≠ disinformation (intencional).
- PEGADINHAS: trocar o canal; misinformation tratada como intencional; esquecer a cadeia de suprimento.
- MEMORIZAÇÃO: phishing=e-mail, vishing=voz, smishing=SMS; watering hole=poço d'água.
- NA PRÁTICA: o SOC monitora e-mail (gateways, DMARC/SPF/DKIM) e treina usuários; a cadeia de suprimento é risco-chave de terceiros (Domínio 5).

## 2.3 Tipos de vulnerabilidades \[OFICIAL\]

Vulnerabilidade é a fraqueza que pode ser explorada. A prova cobra reconhecer a categoria da fraqueza a partir da descrição técnica.

### Aplicação

- Injeção de memória (memory injection): inserir código na memória de um processo.
- Buffer overflow (estouro de buffer): gravar além do espaço alocado, corrompendo memória e podendo executar código.
- Condições de corrida (race conditions): dois processos competem por um recurso; a janela entre verificar e usar é explorada.
  - TOC (Time-of-check): momento em que a condição é verificada.
  - TOU (Time-of-use): momento em que o recurso é usado. O ataque TOCTOU explora a diferença entre os dois.
- Atualização maliciosa (malicious update): update legítimo em aparência que entrega código malicioso.

### Baseado no sistema operacional (OS-based)

Fraquezas no próprio SO (ex.: falha de kernel, serviço vulnerável).

### Baseado na web (web-based)

- SQLi (SQL injection): injetar comandos SQL em um campo de entrada para manipular o banco.
- XSS (Cross-site scripting): injetar script malicioso que roda no navegador de outros usuários.

### Hardware

- Firmware: código de baixo nível vulnerável.
- Fim da vida útil (end-of-life): sem suporte/atualização do fabricante.
- Legado (legacy): sistemas antigos mantidos em produção.

### Virtualização

- Escape de máquina virtual (VM escape): sair da VM e alcançar o host/hypervisor.
- Reutilização de recursos (resource reuse): dados de uma VM vazando para outra via recurso compartilhado.

### Nuvem e cadeia de suprimento

- Específico para nuvem (cloud-specific): más configurações, APIs expostas, responsabilidade compartilhada mal entendida.
- Cadeia de suprimento (supply chain): provedor de serviços, fornecedor de hardware e de software comprometidos.

### Outros

- Criptográfico (cryptographic): algoritmo fraco, chave curta, implementação ruim.
- Configuração incorreta (misconfiguration): a vulnerabilidade mais comum na prática — padrões inseguros, permissões erradas.
- Dispositivo móvel (mobile device): sideloading (instalar apps fora da loja oficial) e jailbreaking (remover restrições do sistema).
- Dia zero (zero-day): falha desconhecida do fornecedor, sem patch disponível — não há defesa baseada em assinatura.

### Representação visual sugerida \[DIDÁTICO\]

Linha do tempo do dia zero: falha existe → descoberta pelo atacante → exploração ativa (janela de exposição) → fornecedor descobre → patch liberado → sistemas corrigidos. (Renderizado como imagem após esta seção.)

&#91;embedded content: Linha do tempo do dia zero · janela de exposição\]

### Comparação — o que mais confunde

- SQLi × XSS: SQLi ataca o banco de dados (injeta SQL); XSS ataca outros usuários no navegador (injeta script). Pergunte: quem é a vítima — o banco ou o navegador do usuário?
- Buffer overflow × Injeção de memória: ambos mexem com memória; buffer overflow extrapola um buffer específico; injeção de memória insere código no espaço do processo.
- Dia zero × Vulnerabilidade conhecida: dia zero não tem patch nem assinatura; a conhecida já tem CVE e correção.
- VM escape × Resource reuse: escapar da VM para o host vs vazamento entre VMs por recurso compartilhado.
- Sideloading × Jailbreaking: instalar app fora da loja vs remover as restrições do próprio SO do aparelho.
- TOC × TOU: verificar vs usar; o ataque explora a janela entre os dois (TOCTOU).

### Memorização \[DIDÁTICO\]

- SQLi = banco (SQL). XSS = navegador/usuário (script).
- Zero-day = "zero dias para se defender": sem patch.
- Sideload = ao LADO da loja oficial; jailbreak = quebrar a cadeia/restrição.
- TOCTOU = Time-Of-Check to Time-Of-Use.

### Pegadinhas típicas da prova

1. Trocar SQLi por XSS — a vítima é o banco (SQLi) ou o navegador do usuário (XSS).
2. Chamar qualquer falha nova de dia zero — só é zero-day se o fornecedor ainda não a conhece e não há patch.
3. Confundir sideloading com jailbreaking.
4. Esquecer que misconfiguration é das causas mais frequentes de incidentes reais.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve a fraqueza explorada e pede a categoria. Raciocínio: identifique onde está a falha (aplicação, SO, web, hardware, VM, nuvem, cripto, móvel) e o alvo do ataque. Entrada que manipula o banco → SQLi; script que executa no navegador de outros → XSS; falha sem patch conhecido → zero-day; app fora da loja → sideloading.

### Mini-desafio 2.3-A

Um atacante insere `' OR '1'='1` em um campo de login e consegue acessar o sistema sem credenciais válidas, manipulando a consulta ao banco de dados. Qual vulnerabilidade foi explorada?

1. Cross-site scripting (XSS)
2. SQL injection (SQLi)
3. Buffer overflow
4. VM escape

### Mini-desafio 2.3-B

Uma falha crítica está sendo ativamente explorada, mas o fornecedor do software ainda não tem conhecimento dela e nenhum patch existe. Como se classifica essa vulnerabilidade?

1. Configuração incorreta
2. Legado
3. Dia zero (zero-day)
4. Fim da vida útil

### Resumo de alta retenção — vulnerabilidades

- PRECISO SABER: aplicação (buffer overflow, injeção de memória, race/TOCTOU, update malicioso); web (SQLi, XSS); SO; hardware (firmware, EOL, legado); virtualização (VM escape, resource reuse); nuvem; cadeia de suprimento; criptográfica; misconfiguration; móvel (sideloading, jailbreaking); dia zero.
- PRECISO RECONHECER: manipula banco→SQLi; script no navegador→XSS; sem patch conhecido→zero-day; app fora da loja→sideloading; sair da VM→VM escape.
- NÃO CONFUNDIR: SQLi (banco) ≠ XSS (navegador); sideloading ≠ jailbreaking; zero-day ≠ falha conhecida.
- PEGADINHAS: trocar SQLi/XSS; chamar tudo de zero-day; ignorar misconfiguration.
- MEMORIZAÇÃO: SQLi=banco, XSS=navegador; zero-day=sem patch; TOCTOU=check→use.
- NA PRÁTICA: o Blue Team prioriza vulnerabilidades por CVSS e exposição (Domínio 4); zero-days exigem defesa em profundidade e detecção comportamental.

## 2.4 Indicadores de atividade maliciosa — parte 1: malware e ataques físicos \[OFICIAL\]

Este é o objetivo mais denso do domínio e a base das PBQs. A prova dá sintomas/indicadores e pede o ataque. Vamos por categorias: malware e físicos aqui; rede, aplicativos, cripto, senhas e indicadores na parte 2.

### Ataques de malware (Malware attacks)

- Ransomware: cifra os dados da vítima e exige resgate. Indicador: arquivos cifrados, nota de resgate, perda de acesso.
- Trojan (cavalo de Troia): software que parece legítimo mas carrega código malicioso. Variante importante: RAT (Remote Access Trojan), dá controle remoto.
- Worm (verme): se replica e se espalha sozinho pela rede, sem precisar de hospedeiro ou ação do usuário. Indicador: propagação rápida na rede.
- Spyware: coleta informações do usuário sem consentimento.
- Bloatware: software indesejado pré-instalado; não é malicioso por definição, mas aumenta a superfície de ataque.
- Vírus (virus): precisa de um hospedeiro/arquivo e de ação do usuário para executar e se espalhar.
- Keylogger: registra as teclas digitadas (captura senhas).
- Bomba lógica (logic bomb): código que dispara quando uma condição é atendida (ex.: uma data, a demissão de alguém).
- Rootkit: se esconde em nível profundo do sistema (kernel) para manter persistência e evitar detecção.

### Ataques físicos (Physical attacks)

- Força bruta (brute force) físico: arrombar, forçar acesso físico.
- Clonagem de RFID (RFID cloning): copiar um crachá/credencial sem contato.
- Ambiental (environmental): atacar infraestrutura de suporte (energia, refrigeração/HVAC) para causar indisponibilidade.

### Representação visual sugerida \[DIDÁTICO\]

Tabela de malware com a característica que distingue cada um (precisa de hospedeiro? se replica sozinho? se esconde? cifra dados?). (Renderizado como imagem após esta seção.)

&#91;embedded content: Tipos de malware · característica distintiva\]

### Comparação — o que mais confunde

- Vírus × Worm: o vírus precisa de hospedeiro e de ação do usuário; o worm se replica e se espalha sozinho pela rede. Esta é a distinção mais cobrada.
- Trojan × Vírus: o trojan engana (parece legítimo) e não se replica por si; o vírus se anexa a arquivos e se propaga.
- RAT × Trojan: RAT é um trojan especializado em acesso remoto.
- Rootkit × Spyware: rootkit se esconde profundamente para manter controle; spyware coleta dados (podendo ser visível a ferramentas).
- Bomba lógica × outros: dispara por condição/gatilho (tempo, evento), não por propagação.
- Bloatware × malware: bloatware é indesejado mas não necessariamente malicioso.

### Memorização \[DIDÁTICO\]

- Worm = anda sozinho (Wander/Worm): auto-replica pela rede.
- Vírus = precisa de carona (hospedeiro + usuário).
- Trojan = disfarce (parece bom, é mau).
- Rootkit = raiz escondida (kernel, furtivo).
- Bomba lógica = espera o gatilho.
- RAT = Remote Access Trojan (controle remoto).

### Pegadinhas típicas da prova

1. Trocar vírus por worm: se espalha SOZINHO pela rede = worm; precisa de hospedeiro/ação = vírus.
2. Chamar qualquer malware furtivo de rootkit — rootkit é especificamente de nível profundo/kernel.
3. Tratar bloatware como malware confirmado — é indesejado, não necessariamente malicioso.
4. Confundir a condição-gatilho (bomba lógica) com propagação automática (worm).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve o comportamento observado (replicação, cifragem, disfarce, persistência oculta, gatilho) e pede o malware. Raciocínio: foque no verbo-chave. Se espalha sozinho → worm; cifra e cobra resgate → ransomware; parece legítimo → trojan; se esconde no kernel → rootkit; dispara por condição → bomba lógica; registra teclas → keylogger.

### Mini-desafio 2.4-A

Um código malicioso se replica e se espalha automaticamente por toda a rede corporativa, sem precisar que o usuário abra qualquer arquivo. Que tipo de malware é esse?

1. Vírus
2. Worm
3. Trojan
4. Spyware

### Mini-desafio 2.4-B

Um ex-administrador deixou um código que apaga a base de dados automaticamente caso o nome dele seja removido da folha de pagamento. Que tipo de malware descreve esse comportamento?

1. Rootkit
2. Worm
3. Bomba lógica (logic bomb)
4. Ransomware

### Resumo de alta retenção — malware e físicos

- PRECISO SABER: ransomware, trojan/RAT, worm, spyware, bloatware, vírus, keylogger, bomba lógica, rootkit; físicos (força bruta, clonagem RFID, ambiental).
- PRECISO RECONHECER: espalha sozinho→worm; cifra+resgate→ransomware; parece legítimo→trojan; esconde no kernel→rootkit; gatilho→bomba lógica; registra teclas→keylogger.
- NÃO CONFUNDIR: vírus (hospedeiro+usuário) ≠ worm (auto-replica); rootkit (furtivo/kernel) ≠ spyware (coleta dados); bloatware ≠ malware.
- PEGADINHAS: vírus vs worm; chamar tudo furtivo de rootkit.
- MEMORIZAÇÃO: worm anda sozinho; vírus pega carona; trojan se disfarça; rootkit é raiz escondida.
- NA PRÁTICA: EDR/antivírus detectam por assinatura e comportamento; worms exigem segmentação de rede para conter propagação.

## 2.4 Indicadores de atividade maliciosa — parte 2: rede, aplicativos, cripto, senhas e indicadores \[OFICIAL\]

### Ataques de rede (Network attacks)

- DDoS (Distributed Denial of Service): muitos sistemas sobrecarregam o alvo até derrubá-lo.
  - Amplificado (amplified): usa serviços que respondem com muito mais dados do que a requisição (ex.: DNS, NTP).
  - Refletido (reflected): usa a vítima como refletor, forjando o IP de origem.
- Ataques ao DNS (DNS attacks): envenenamento de cache, sequestro de DNS.
- Sem fio (wireless): ataques a redes Wi-Fi.
- On-path (antigo man-in-the-middle): o atacante se posiciona entre as partes para interceptar/alterar o tráfego.
- Repetição de credenciais (credential replay): capturar e reenviar credenciais/tokens válidos.
- Código malicioso (malicious code): execução de código hostil na rede.

### Ataques de aplicativos (Application attacks)

- Injeção (injection): SQLi, comandos, LDAP etc.
- Buffer overflow: estouro de buffer na aplicação.
- Reprodução (replay): reenviar dados capturados.
- Escalação de privilégio (privilege escalation): ganhar permissões acima das concedidas (vertical) ou de outro usuário de mesmo nível (horizontal).
- Falsificação (forgery): CSRF/XSRF (cross-site request forgery) — forçar a ação de um usuário autenticado.
- Travessia de diretórios (directory traversal): acessar arquivos fora do diretório permitido (ex.: ../../etc/passwd).

### Ataques criptográficos (Cryptographic attacks)

- Downgrade: forçar o uso de um protocolo/cifra mais fraco.
- Colisão (collision): duas entradas com o mesmo hash (quebra de integridade de hashes fracos).
- Aniversário (birthday): ataque estatístico que explora a probabilidade de colisões.

### Ataques a senhas (Password attacks)

- Spraying (password spraying): testar poucas senhas comuns em muitas contas, evitando bloqueio.
- Força bruta (brute force): testar muitas combinações contra uma conta.

### Indicadores (Indicators)

Sinais que aparecem nos logs e sistemas e denunciam atividade maliciosa:

- Bloqueio de conta (account lockout): muitas tentativas falhas.
- Uso de sessão simultânea (concurrent session usage): mesma conta ativa em lugares diferentes ao mesmo tempo.
- Conteúdo bloqueado (blocked content): tentativa de acessar algo barrado por política.
- Viagem impossível (impossible travel): logins de locais geograficamente impossíveis no intervalo de tempo.
- Consumo de recursos (resource consumption): uso anormal de CPU/memória/banda.
- Inacessibilidade de recursos (resource inaccessibility): serviços indisponíveis.
- Registro fora do ciclo (out-of-cycle logging): logs em horários incomuns.
- Publicado/documentado (published/documented): o incidente aparece em fontes externas/threat intel.
- Logs ausentes (missing logs): registros apagados ou não gerados — sinal de encobrimento.

### Representação visual sugerida \[DIDÁTICO\]

Comparação lado a lado de brute force vs password spraying: muitas senhas em uma conta vs poucas senhas em muitas contas. (Renderizado como imagem após esta seção.)

&#91;embedded content: Força bruta vs password spraying\]

### Comparação — o que mais confunde

- Brute force × Spraying: força bruta ataca uma conta com muitas senhas (gera bloqueio); spraying usa poucas senhas comuns em muitas contas (evita bloqueio).
- DDoS amplificado × refletido: amplificado explora resposta grande; refletido forja o IP da vítima para que respostas cheguem a ela. Muitos ataques são as duas coisas.
- On-path × replay: on-path intercepta em tempo real no meio da comunicação; replay reenvia dados capturados depois.
- Escalação vertical × horizontal: vertical sobe de nível (usuário→admin); horizontal pega acesso de outro usuário do mesmo nível.
- Colisão × aniversário: colisão é o resultado (mesmo hash); o ataque de aniversário é o método probabilístico para encontrá-la.
- Viagem impossível × sessão simultânea: viagem impossível foca na distância/tempo entre logins; sessão simultânea é a mesma conta ativa em paralelo.

### Memorização \[DIDÁTICO\]

- Brute force = uma conta, muitas senhas. Spraying = uma senha comum, muitas contas (spray = borrifar sobre vários).
- On-path = "no caminho" (no meio). Replay = "reprisa" o que gravou.
- Viagem impossível = login em dois continentes em minutos.
- Logs ausentes = alguém apagou o rastro.

### Pegadinhas típicas da prova

1. Trocar brute force por spraying: o detalhe é quantas senhas × quantas contas e se evita ou gera bloqueio.
2. Confundir on-path (tempo real, no meio) com replay (reenvio posterior).
3. Tratar colisão e aniversário como a mesma coisa — um é o efeito, o outro é o método.
4. Não reconhecer indicadores sutis como viagem impossível e logs ausentes nos cenários de SOC.

### Como a CompTIA transforma isso em questão + raciocínio

PBQ típica: dá um trecho de log ou lista de sintomas e pede o ataque/indicador. Raciocínio: leia o padrão. Muitas falhas em uma conta → brute force/lockout; poucas tentativas em muitas contas → spraying; login de dois países em minutos → viagem impossível; logs sumidos → missing logs/encobrimento; resposta de serviço maior que a requisição → DDoS amplificado.

### Mini-desafio 2.4-C

O SIEM mostra que o mesmo usuário fez login em São Paulo e, oito minutos depois, em Tóquio. Qual indicador de atividade maliciosa é esse?

1. Bloqueio de conta
2. Viagem impossível
3. Uso de sessão simultânea
4. Registro fora do ciclo

### Mini-desafio 2.4-D

Um atacante testa apenas as três senhas mais comuns ("Senha123", "123456", "Qwerty") contra milhares de contas de uma organização, justamente para não acionar o bloqueio por tentativas. Qual ataque é esse?

1. Força bruta
2. Password spraying
3. Credential replay
4. Downgrade

### Resumo de alta retenção — rede, app, cripto, senhas, indicadores

- PRECISO SABER: rede (DDoS amp/refletido, DNS, wireless, on-path, credential replay); app (injeção, buffer overflow, replay, escalação de privilégio, CSRF, directory traversal); cripto (downgrade, colisão, aniversário); senhas (spraying, brute force); indicadores (lockout, sessão simultânea, viagem impossível, consumo/inacessibilidade de recursos, out-of-cycle logging, missing logs).
- PRECISO RECONHECER: muitas senhas/uma conta→brute force; poucas senhas/muitas contas→spraying; no meio em tempo real→on-path; login impossível no tempo→viagem impossível; logs sumidos→missing logs.
- NÃO CONFUNDIR: brute force ≠ spraying; on-path ≠ replay; colisão (efeito) ≠ aniversário (método); escalação vertical ≠ horizontal.
- PEGADINHAS: senhas×contas; on-path vs replay; indicadores sutis.
- MEMORIZAÇÃO: spraying=borrifar senha comum em muitas contas; on-path=no caminho.
- NA PRÁTICA: o SOC detecta esses padrões no SIEM com regras de correlação; viagem impossível e sessão simultânea são alertas clássicos de UEBA.

## 2.5 Técnicas de mitigação \[OFICIAL\]

Mitigações são as medidas que reduzem o risco. A prova cobra escolher a técnica adequada para conter uma ameaça específica.

### Técnicas principais

- Segmentação (segmentation): dividir a rede em zonas isoladas para conter a propagação (ex.: limitar um worm ou um ataque lateral). Muito cobrada contra movimento lateral.
- Controle de acesso (access control): ACL (Access Control List) e permissões que definem quem acessa o quê.
- Lista de aplicações permitidas (application allow list): só executa o que está explicitamente autorizado — mais seguro que a deny list.
- Isolamento (isolation): separar completamente um sistema comprometido ou de risco (ex.: quarentena, air gap).
- Patching: aplicar correções para fechar vulnerabilidades conhecidas.
- Criptografia (encryption): proteger dados em repouso e em trânsito.
- Monitoramento (monitoring): observar continuamente para detectar atividade anômala.
- Privilégio mínimo (least privilege): conceder apenas as permissões estritamente necessárias. Reduz o impacto de contas comprometidas.
- Aplicação de configuração (configuration enforcement): garantir que os sistemas mantenham a configuração segura definida (baseline).
- Descomissionamento (decommissioning): retirar com segurança sistemas que não são mais necessários, reduzindo a superfície de ataque.

### Técnicas de hardening (endurecimento)

Hardening é reduzir a superfície de ataque de um sistema. Técnicas oficiais:

- Criptografia (encryption): cifrar dados do sistema.
- Instalação de proteção de endpoint (endpoint protection): antivírus/EDR nos dispositivos.
- Firewall baseado em host (host-based firewall): filtra tráfego no próprio dispositivo.
- HIPS (Host-based Intrusion Prevention System): previne intrusões no host.
- Desativação de portas/protocolos (disabling ports/protocols): fechar o que não é usado.
- Alterações de senha padrão (default password changes): trocar credenciais de fábrica.
- Remoção de software desnecessário (removal of unnecessary software): menos software, menos risco.

### Representação visual sugerida \[DIDÁTICO\]

Mapa que liga ameaças comuns às suas mitigações principais: worm → segmentação; conta comprometida → privilégio mínimo; vulnerabilidade conhecida → patching; execução de software não autorizado → allow list; sistema comprometido → isolamento. (Renderizado como imagem após esta seção.)

&#91;embedded content: Ameaça → mitigação principal\]

### Comparação — o que mais confunde

- Segmentação × Isolamento: segmentação divide a rede em zonas (ainda há comunicação controlada); isolamento separa completamente (quarentena/air gap).
- Allow list × Deny list: allow list permite só o listado (mais seguro); deny list bloqueia o listado (permite o resto).
- Privilégio mínimo × Controle de acesso: controle de acesso define quem acessa; privilégio mínimo é o princípio de dar o mínimo necessário.
- Patching × Hardening: patching corrige falhas conhecidas; hardening é o conjunto amplo de medidas que reduz a superfície de ataque (inclui patching, mas vai além).
- Descomissionamento × Isolamento: descomissionar é retirar de serviço definitivamente; isolar é separar mantendo (temporariamente) o sistema.

### Memorização \[DIDÁTICO\]

- Segmentação = muros internos (conter propagação).
- Isolamento = quarentena (separar de vez).
- Privilégio mínimo = só o necessário.
- Allow list = só convidados entram.
- Patching = tapar o buraco conhecido.
- Hardening = blindar o sistema (remover o excesso).

### Pegadinhas típicas da prova

1. Trocar segmentação por isolamento — conter a propagação na rede (segmentação) vs separar totalmente (isolamento).
2. Preferir deny list quando a resposta mais segura é allow list.
3. Tratar patching como sinônimo de hardening — hardening é mais amplo.
4. Esquecer o descomissionamento como mitigação de superfície de ataque (sistemas legados/EOL).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve uma ameaça e pede a melhor mitigação. Raciocínio: case a ameaça com o controle. Propagação lateral de malware → segmentação; abuso de permissões → privilégio mínimo; falha conhecida → patching; software não autorizado rodando → application allow list; host infectado → isolamento/quarentena; sistema obsoleto exposto → descomissionamento.

### Mini-desafio 2.5-A

Para impedir que um worm, caso infecte um único setor, se espalhe para toda a rede corporativa, qual técnica de mitigação é a mais adequada?

1. Criptografia
2. Segmentação de rede
3. Patching
4. Alteração de senha padrão

### Mini-desafio 2.5-B

Uma empresa quer garantir que apenas aplicativos previamente aprovados possam ser executados nas estações de trabalho, bloqueando qualquer software não autorizado. Qual técnica atende a esse objetivo?

1. Deny list
2. Application allow list
3. Monitoramento
4. Isolamento

### Resumo de alta retenção — mitigações

- PRECISO SABER: segmentação, controle de acesso (ACL/permissões), application allow list, isolamento, patching, criptografia, monitoramento, privilégio mínimo, configuration enforcement, descomissionamento; hardening (endpoint protection, host firewall, HIPS, desativar portas/protocolos, trocar senha padrão, remover software).
- PRECISO RECONHECER: conter propagação→segmentação; separar de vez→isolamento; só o necessário→privilégio mínimo; só o aprovado→allow list; falha conhecida→patching; obsoleto→descomissionamento.
- NÃO CONFUNDIR: segmentação ≠ isolamento; allow list ≠ deny list; patching ≠ hardening (amplo).
- PEGADINHAS: segmentação vs isolamento; preferir allow list; patching não é hardening inteiro.
- MEMORIZAÇÃO: segmentação=muros internos; isolamento=quarentena; hardening=blindar.
- NA PRÁTICA: defesa em profundidade combina várias dessas camadas; segmentação e privilégio mínimo são pilares de Zero Trust (Domínio 1).

## Revisão do Domínio 2.0

### Revisão 20/80 — os 20% que explicam 80% do domínio

1. Atores pela motivação: estado-nação (espionagem/guerra), crime organizado (lucro), hacktivista (ideologia), insider (acesso de dentro), script kiddie (caos).
2. Phishing muda de nome pelo canal: e-mail (phishing), voz (vishing), SMS (smishing).
3. Vírus precisa de hospedeiro e usuário; worm se espalha sozinho pela rede.
4. SQLi ataca o banco; XSS ataca o navegador do usuário.
5. Zero-day = sem patch e sem assinatura; defesa é comportamental e em profundidade.
6. Força bruta = muitas senhas em uma conta; spraying = poucas senhas em muitas contas.
7. Indicadores de SOC: viagem impossível, logs ausentes, sessão simultânea, consumo anormal de recursos.
8. Mitigações-chave: segmentação (propagação), privilégio mínimo (abuso de acesso), patching (falha conhecida), allow list (software não autorizado), isolamento (host infectado).

### Mapa mental do Domínio 2.0

(Renderizado como imagem após esta seção: o Domínio 2.0 ao centro com cinco ramos — Atores, Vetores/engenharia social, Vulnerabilidades, Indicadores de ataque e Mitigações.)

&#91;embedded content: Mapa mental do Domínio 2.0\]

### Tabela dos conceitos mais confundidos

| Par confundido | Como diferenciar |
| --- | --- |
| Estado-nação × Crime organizado | Espionagem/guerra × lucro |
| Phishing × Vishing × Smishing | E-mail × voz × SMS |
| Watering hole × Typosquatting | Site confiável comprometido × domínio com erro |
| Misinformation × Disinformation | Sem intenção × intencional |
| Vírus × Worm | Hospedeiro+usuário × auto-replica na rede |
| Trojan × Vírus | Disfarce, não replica × anexa e propaga |
| Rootkit × Spyware | Furtivo no kernel × coleta dados |
| SQLi × XSS | Ataca o banco × ataca o navegador |
| Sideloading × Jailbreaking | App fora da loja × remover restrições do SO |
| Zero-day × Falha conhecida | Sem patch/assinatura × tem CVE e correção |
| Força bruta × Spraying | Muitas senhas/1 conta × poucas senhas/muitas contas |
| On-path × Replay | No meio, tempo real × reenvio posterior |
| Escalação vertical × horizontal | Sobe de nível × acesso de outro do mesmo nível |
| DDoS amplificado × refletido | Resposta grande × IP da vítima forjado |
| Segmentação × Isolamento | Zonas na rede × separação total |
| Allow list × Deny list | Só o permitido × bloqueia o listado |

### Flashcards (pergunta → resposta)

| Pergunta | Resposta |
| --- | --- |
| Ator furtivo, bem financiado, mira governo? | Estado-nação (APT) |
| Ator motivado por lucro? | Crime organizado |
| Golpe por SMS? | Smishing |
| Golpe por voz? | Vishing |
| Site legítimo comprometido que o alvo visita? | Watering hole |
| Malware que se espalha sozinho na rede? | Worm |
| Malware que precisa de hospedeiro e usuário? | Vírus |
| Malware que se disfarça de legítimo? | Trojan |
| Malware furtivo no kernel? | Rootkit |
| Código que dispara por condição? | Bomba lógica |
| Injeção que manipula o banco? | SQLi |
| Script que roda no navegador de outros? | XSS |
| Falha sem patch e sem assinatura? | Zero-day |
| Muitas senhas em uma conta? | Força bruta |
| Poucas senhas comuns em muitas contas? | Password spraying |
| Login de dois países em minutos? | Viagem impossível |
| Mitigação contra propagação lateral? | Segmentação |
| Mitigação contra abuso de permissões? | Privilégio mínimo |
| Só executa software aprovado? | Application allow list |

## Mini-simulado do Domínio 2.0

Doze questões no estilo da prova, cobrindo todo o domínio. As respostas comentadas estão na última seção. Responda antes de conferir.

**Q1.** Um grupo criminoso profissional invade uma rede hospitalar, cifra todos os prontuários e exige pagamento em criptomoeda para liberar o acesso. Qual a combinação ator + malware mais provável?

1. Hacktivista + spyware
2. Crime organizado + ransomware
3. Estado-nação + worm
4. Script kiddie + trojan

**Q2.** Um funcionário recebe uma mensagem de texto no celular dizendo que sua conta bancária será bloqueada e pedindo que clique em um link para "revalidar" os dados. Qual técnica foi usada?

1. Vishing
2. Phishing
3. Smishing
4. Watering hole

**Q3.** Um atacante registra o domínio "micorsoft.com" para capturar usuários que erram a digitação de "microsoft.com". Qual técnica é essa?

1. Watering hole
2. Typosquatting
3. Brand impersonation
4. Pretexting

**Q4.** Em um campo de busca de um site, um atacante insere um script que passa a ser executado no navegador de todos os visitantes que carregam a página. Qual vulnerabilidade foi explorada?

1. SQL injection
2. Cross-site scripting (XSS)
3. Directory traversal
4. Buffer overflow

**Q5.** Um malware se espalha automaticamente por toda a rede explorando uma vulnerabilidade de serviço, sem qualquer interação do usuário. Como ele é classificado?

1. Vírus
2. Trojan
3. Worm
4. Keylogger

**Q6.** O analista do SOC nota que a conta de um usuário aparece autenticada simultaneamente em dois endereços IP distantes, nos mesmos minutos. Qual indicador descreve melhor essa situação?

1. Bloqueio de conta
2. Logs ausentes
3. Uso de sessão simultânea
4. Consumo de recursos

**Q7.** Um atacante tenta as senhas "123456" e "Senha@2024" contra 5.000 contas de funcionários, propositalmente limitando as tentativas por conta para não disparar bloqueios. Qual ataque é esse?

1. Força bruta
2. Password spraying
3. Credential replay
4. Birthday attack

**Q8.** Para conter a propagação lateral de um possível malware entre departamentos, qual técnica de mitigação a equipe de rede deve priorizar?

1. Criptografia de disco
2. Segmentação de rede
3. Troca de senha padrão
4. Monitoramento de logs

**Q9.** Uma vulnerabilidade crítica está sendo explorada "na natureza" (in the wild), mas o fornecedor ainda não a reconheceu e não há correção. Qual é a classificação?

1. Legado
2. Fim da vida útil
3. Dia zero
4. Configuração incorreta

**Q10.** Um atacante se posiciona entre o cliente e o servidor para interceptar e, possivelmente, alterar o tráfego em tempo real. Qual ataque de rede é esse?

1. Replay
2. On-path
3. DDoS refletido
4. DNS poisoning

**Q11.** Uma empresa quer impedir que qualquer software não previamente aprovado seja executado nas estações de trabalho. Qual controle é o mais adequado?

1. Deny list
2. Application allow list
3. HIPS
4. Firewall de host

**Q12.** Um ex-funcionário programou um script para apagar bancos de dados automaticamente se seu usuário for desativado. Que tipo de malware é esse?

1. Rootkit
2. Bomba lógica
3. Ransomware
4. Worm

## Gabarito comentado — Domínio 2.0

### Mini-desafios

**2.1-A — Resposta: 3 (Estado-nação/APT).** Alto financiamento, furtividade, permanência longa e alvo governamental com coleta de sigilo são a assinatura de uma APT patrocinada por estado. Script kiddie não tem recurso; hacktivista busca visibilidade; shadow IT não é atacante.

**2.1-B — Resposta: 2 (Ameaça interna motivada por vingança).** Funcionário com acesso legítimo agindo por ressentimento = insider + vingança. As demais trocam ator ou motivação.

**2.2-A — Resposta: 2 (Vishing).** O canal é a chamada de voz (voice), e há personificação do técnico de TI. Smishing seria SMS; watering hole é site comprometido; typosquatting é domínio falso.

**2.2-B — Resposta: 3 (Watering hole).** Comprometer um site legítimo que o alvo costuma visitar para infectá-lo é a definição de watering hole. Phishing usa mensagem; typosquatting usa domínio com erro; BEC é fraude por e-mail corporativo.

**2.3-A — Resposta: 2 (SQL injection).** A entrada manipula a consulta ao banco de dados (`' OR '1'='1`). XSS atacaria o navegador; buffer overflow é memória; VM escape é virtualização.

**2.3-B — Resposta: 3 (Dia zero).** Exploração ativa sem conhecimento do fornecedor e sem patch = zero-day. Misconfiguration, legado e EOL são falhas conhecidas/gerenciáveis.

**2.4-A — Resposta: 2 (Worm).** Auto-replicação e propagação automática pela rede, sem ação do usuário, define o worm. Vírus exigiria hospedeiro e ação; trojan se disfarça; spyware coleta dados.

**2.4-B — Resposta: 3 (Bomba lógica).** Código que dispara ao atender uma condição (remoção do nome da folha) é logic bomb. Rootkit é furtivo; worm se replica; ransomware cifra e cobra.

**2.4-C — Resposta: 2 (Viagem impossível).** Logins em locais geograficamente impossíveis no intervalo (São Paulo → Tóquio em 8 min) é impossible travel. Sessão simultânea foca em paralelismo; lockout é bloqueio; out-of-cycle é horário anômalo.

**2.4-D — Resposta: 2 (Password spraying).** Poucas senhas comuns contra muitas contas, evitando bloqueio por conta, é spraying. Força bruta seria muitas senhas em uma conta; replay reenvia credenciais; downgrade é cripto.

**2.5-A — Resposta: 2 (Segmentação de rede).** Dividir a rede em zonas contém a propagação lateral do worm. Criptografia protege dados; patching fecha a falha específica; troca de senha não limita propagação.

**2.5-B — Resposta: 2 (Application allow list).** Só executa o que está explicitamente aprovado, bloqueando o resto. Deny list permitiria tudo exceto o listado; monitoramento e isolamento não controlam execução.

### Mini-simulado

| Questão | Resposta | Comentário |
| --- | --- | --- |
| Q1 | 2 | Grupo profissional + cifragem com resgate = crime organizado + ransomware |
| Q2 | 3 | Golpe por mensagem de texto = smishing |
| Q3 | 2 | Domínio com erro de digitação = typosquatting |
| Q4 | 2 | Script executado no navegador de visitantes = XSS |
| Q5 | 3 | Propagação automática sem interação = worm |
| Q6 | 3 | Mesma conta ativa em paralelo = uso de sessão simultânea |
| Q7 | 2 | Poucas senhas em muitas contas, evitando bloqueio = password spraying |
| Q8 | 2 | Conter propagação lateral = segmentação de rede |
| Q9 | 3 | Exploração sem conhecimento do fornecedor nem patch = dia zero |
| Q10 | 2 | Interceptar/alterar no meio em tempo real = on-path |
| Q11 | 2 | Só executar software aprovado = application allow list |
| Q12 | 2 | Código que dispara por condição (desativação) = bomba lógica |

### Autodiagnóstico sugerido

| Acertos (de 12) | Classificação | Ação recomendada |
| --- | --- | --- |
| 11–12 | Excelente | Domínio sólido; avançar ao 3.0 |
| 9–10 | Bom | Revisar os pares da tabela de confundidos |
| 6–8 | Atenção | Refazer flashcards e releitura de 2.3 e 2.4 |
| 4–5 | Fraco | Reestudar o domínio com foco em malware, vetores e indicadores |
| 0–3 | Crítico | Reiniciar o domínio do zero, objetivo por objetivo |

**Subtemas que mais derrubam candidatos neste domínio:** vírus × worm (2.4), SQLi × XSS (2.3), força bruta × spraying (2.4) e os indicadores sutis de SOC — viagem impossível, logs ausentes, sessão simultânea (2.4). Como o 2.4 concentra as PBQs, priorize treinar leitura de cenários e logs.

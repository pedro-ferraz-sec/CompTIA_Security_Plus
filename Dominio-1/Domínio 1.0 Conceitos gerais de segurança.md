# Guia Security+ SY0-701 — Domínio 1.0: Conceitos gerais de segurança

Oct 7, 2026 · @Pedro Henrique Ferraz

Material de estudo para a certificação CompTIA Security+ (SY0-701). O Domínio 1.0 vale 12% da prova e reúne os conceitos-base que sustentam todos os outros domínios. Todos os gabaritos ficam na última seção.

## Como usar este guia

Este material cobre todo o Domínio 1.0 da CompTIA Security+ SY0-701 com um método de aprendizado voltado ao reconhecimento de padrões da prova, não à memorização isolada. Cada conceito segue a sequência: ideia simples, definição técnica, exemplo real, aplicação profissional (SOC, Blue Team, Red Team, redes e infraestrutura), comparação com conceitos parecidos, técnica de memorização, pegadinhas típicas, questão no estilo da prova e resumo de alta retenção.

**Legenda de origem do conteúdo** (use para saber o que é cobrado oficialmente):

| Marca | Significado |
| --- | --- |
| \[OFICIAL\] | Item que consta literalmente nos objetivos SY0-701 da CompTIA |
| \[COMPLEMENTAR\] | Conhecimento de apoio que ajuda a entender o item oficial, mas não é um tópico listado |
| \[DIDÁTICO\] | Exemplo, analogia ou cenário criado para fixar o conceito |

**Termos em inglês:** sempre que um termo for relevante para a prova, ele aparece no formato inglês → tradução → significado → como cai na prova. A CompTIA redige o exame em inglês e muitas questões dependem de reconhecer o termo original.

**Mini-desafios e simulado:** ao longo do guia há mini-desafios (perguntas rápidas de fixação) e, ao final, um mini-simulado do domínio. Nenhuma resposta aparece junto da pergunta. Todos os gabaritos comentados ficam reunidos na última seção, para permitir autoavaliação honesta.

**Estrutura do Domínio 1.0 (peso 12%):** quatro objetivos oficiais — 1.1 Comparar tipos de controles de segurança; 1.2 Resumir conceitos fundamentais; 1.3 Importância da gestão de mudanças; 1.4 Importância de soluções criptográficas apropriadas.

## 1.1 Categorias de controles de segurança \[OFICIAL\]

O objetivo 1.1 tem dois eixos que a CompTIA testa separadamente e adora misturar: a categoria (a natureza do controle — quem ou o que o executa) e o tipo (a função do controle — o que ele faz). Esta seção trata das quatro categorias; a próxima trata dos seis tipos.

**As quatro categorias \[OFICIAL\]:** Técnico (Technical), Gerencial (Managerial), Operacional (Operational) e Físico (Physical). A pergunta que define a categoria é sempre: quem ou o que executa o controle?

### Técnico (Technical / Logical)

Controle executado por tecnologia — um sistema faz o trabalho, não uma pessoa. Objetivo: aplicar a segurança automaticamente via hardware, software ou firmware. Exemplos: firewall, antivírus/EDR, criptografia, IDS/IPS, autenticação multifator (MFA), listas de controle de acesso (ACLs), permissões de arquivo, SIEM. Na questão, aparecem tecnologia, configuração, sistema ou software.

- Termo: Technical control → controle técnico → implementado por tecnologia → a CompTIA também chama de logical control (controle lógico). São sinônimos na prova.
- SOC/Blue Team: regra de correlação no SIEM, bloqueio automático no EDR.
- Red Team: é o que eles tentam burlar (ex.: evadir o antivírus, contornar o firewall).

### Gerencial (Managerial / Administrative)

Controle baseado em decisões, políticas e gestão — o papel e a caneta da segurança. Objetivo: governar como a segurança deve ser feita (direção, não execução técnica). Exemplos: políticas de segurança, avaliação de risco (risk assessment), política de contratação, verificação de antecedentes (background check), o programa/política de treinamento, planejamento.

- Termo: Managerial control → controle gerencial → também aparece como administrative control (controle administrativo). São sinônimos na prova.
- SOC/Blue Team: a política que define retenção de logs, o playbook aprovado pela gestão.
- Red Team: as regras de engajamento (rules of engagement) e a autorização formal do pentest.

### Operacional (Operational)

Controle executado por pessoas no dia a dia — não por máquina, não por política no papel, mas pela ação humana recorrente. Exemplos: a execução do treinamento de conscientização, revisão manual de logs por um analista, troca de turno de guarda, gestão operacional de mudanças, resposta a incidente executada pela equipe. Na questão, há uma pessoa executando uma rotina ou processo.

- SOC/Blue Team: o analista fazendo triagem de alertas, a ronda de monitoramento do turno.
- Infraestrutura: o administrador aplicando patches manualmente conforme o procedimento.

### Físico (Physical)

Controle do mundo físico — barreiras e proteções tangíveis que protegem instalações, equipamentos e pessoas. Exemplos: cercas, muros, catracas, fechaduras, guardas (como barreira/presença), crachá, iluminação, câmeras (CCTV), biometria na porta, mantrap (eclusa de segurança).

- Blue Team/infra: controle de acesso ao datacenter, trancamento de racks.
- Red Team: o que uma equipe de pentest físico tenta vencer (tailgating, clonagem de crachá).

### Tabela comparativa das categorias

| Categoria | Quem executa | Pergunta-chave | Exemplo-âncora |
| --- | --- | --- | --- |
| Técnico (Technical/Logical) | A tecnologia/sistema | "Um sistema faz sozinho?" | Firewall, MFA, criptografia |
| Gerencial (Managerial/Admin) | A gestão, no papel | "É decisão ou política?" | Política de risco, background check |
| Operacional (Operational) | Uma pessoa, na rotina | "Alguém executa a rotina?" | Analista revisando logs, ronda |
| Físico (Physical) | Barreira tangível | "Dá para tocar?" | Cerca, fechadura, guarda, CCTV |

### Representação visual sugerida \[DIDÁTICO\]

Diagrama de quatro quadros lado a lado, cada um com cor própria, rotulados Técnico, Gerencial, Operacional e Físico. Abaixo de cada quadro, o exemplo-âncora. Centralizada no rodapé, a pergunta que resolve toda questão de categoria: "QUEM ou O QUÊ executa o controle?" (Este diagrama está renderizado como imagem logo após esta seção.)

&#91;embedded content: As quatro categorias de controle · definidas por quem executa\]

### Comparação — o que mais confunde

- Técnico vs Físico: a biometria na porta de uma sala é física; a biometria para logar no sistema é técnica. CCTV costuma ser física (dissuasão/monitoração do ambiente); o software de análise de vídeo seria técnico. O contexto decide.
- Gerencial vs Operacional: a política de treinamento (documento/decisão) é gerencial; o treinamento sendo aplicado por pessoas é operacional. Decidir e planejar é gerencial; executar a rotina é operacional.
- Guarda de segurança: pode ser classificado como físico (barreira humana) ou operacional (pessoa em processo). A CompTIA geralmente o trata como físico; observe o contexto do enunciado.

### Memorização \[DIDÁTICO\]

Use a pergunta de ouro "QUEM faz?": Máquina → Técnico; Chefia no papel → Gerencial; Funcionário na rotina → Operacional; Parede/barreira → Físico. E guarde os sinônimos que a prova usa: Técnico = Logical; Gerencial = Administrative.

### Pegadinhas típicas da prova

1. Misturar os eixos: o enunciado pergunta categoria, mas oferece tipos (Preventivo, Detectivo) como distratores. Se pergunta categoria, a resposta só pode ser Técnico/Gerencial/Operacional/Físico.
2. Usar o sinônimo para confundir: o enunciado diz logical control e o candidato não reconhece que é técnico, ou administrative e não liga a gerencial.
3. Treinamento ambíguo: dependendo da redação é gerencial (a política) ou operacional (a execução).
4. Criptografia classificada como física — erro clássico. Criptografia é sempre técnica.

### Como a CompTIA transforma isso em questão + raciocínio

O enunciado descreve um controle concreto e pergunta a categoria. O raciocínio de eliminação: identifique o executor. Se for um sistema agindo sozinho, é técnico; se for um documento ou decisão da gestão, é gerencial; se for uma pessoa cumprindo rotina, é operacional; se for barreira física, é físico. Elimine alternativas que pertencem ao outro eixo (tipos de controle) de imediato.

### Mini-desafio 1.1-A

A diretoria aprovou e publicou uma política de classificação de dados que define como as informações devem ser rotuladas e tratadas. Qual categoria de controle essa política representa?

1. Técnico
2. Operacional
3. Gerencial
4. Físico

### Resumo de alta retenção — categorias

- PRECISO SABER: 4 categorias classificadas por quem/o que executa — Técnico, Gerencial, Operacional, Físico.
- PRECISO RECONHECER: Technical = Logical; Managerial = Administrative. Gatilhos: "policy" → Gerencial; "firewall/encryption/MFA" → Técnico; "pessoa executando" → Operacional; "cerca/porta/guarda/CCTV" → Físico.
- NÃO CONFUNDIR: Gerencial (decidir no papel) ≠ Operacional (executar rotina); categoria ≠ tipo.
- PEGADINHAS: eixo trocado; sinônimos; criptografia nunca é física.
- MEMORIZAÇÃO: "QUEM faz?" → Máquina/Chefia/Funcionário/Parede.
- NA PRÁTICA: SIEM/EDR (técnico), playbook aprovado (gerencial), triagem de alertas (operacional), acesso ao datacenter (físico).

## 1.1 Tipos de controles de segurança \[OFICIAL\]

Agora o segundo eixo: o tipo descreve a função do controle — o que ele faz diante de uma ameaça, em relação ao momento do incidente (antes, durante, depois). São seis tipos oficiais: Preventivo, Dissuasor, Detectivo, Corretivo, Compensatório e Diretivo.

### Preventivo (Preventive)

Impede que o incidente aconteça. Age antes do evento, bloqueando a ação. Exemplos: firewall bloqueando tráfego, regra de senha forte, criptografia, treinamento que impede o erro, tranca na porta. Palavra-chave: impedir, bloquear, prevenir.

### Dissuasor (Deterrent)

Desencoraja o atacante, sem necessariamente impedir fisicamente. Age sobre a decisão do adversário. Exemplos: placa de aviso "área monitorada", presença visível de câmera, aviso de sanções legais, cão de guarda à vista. Palavra-chave: desencorajar, intimidar, avisar.

### Detectivo (Detective)

Descobre e registra que um incidente ocorreu ou está ocorrendo. Age durante ou depois do evento. Exemplos: IDS, SIEM gerando alerta, revisão de logs, CCTV gravando, alarme. Palavra-chave: detectar, identificar, alertar, registrar.

### Corretivo (Corrective)

Corrige e restaura após o incidente, reduzindo o impacto. Age depois do evento. Exemplos: restauração de backup, patch aplicado após exploração, isolamento/quarentena de host infectado, procedimento de recuperação. Palavra-chave: corrigir, restaurar, recuperar, remediar.

### Compensatório (Compensating)

Controle alternativo usado quando o controle primário/ideal não é viável. Não é a solução preferida, mas cobre o risco de outra forma. Exemplos: MFA temporário porque um sistema legado não suporta a política padrão; segmentação de rede isolando um sistema que não pode receber patch; monitoramento extra enquanto a correção definitiva não chega. Palavra-chave: alternativa, substituto, quando o ideal não é possível.

### Diretivo (Directive)

Orienta ou obriga um comportamento por meio de instrução. Diz o que deve ser feito. Exemplos: política de uso aceitável (AUP), procedimento operacional padrão, placa "use o crachá", instrução de classificar documentos. Palavra-chave: orientar, instruir, exigir por norma.

### Tabela comparativa dos tipos

| Tipo | Quando age | O que faz | Exemplo-âncora |
| --- | --- | --- | --- |
| Preventivo | Antes | Impede o evento | Firewall, criptografia, tranca |
| Dissuasor | Antes | Desencoraja o atacante | Placa "monitorado", câmera visível |
| Detectivo | Durante/Depois | Descobre e registra | IDS, SIEM, revisão de logs, CCTV |
| Corretivo | Depois | Corrige e restaura | Backup, patch, quarentena |
| Compensatório | Qualquer | Alternativa ao ideal | MFA temporário, segmentação |
| Diretivo | Antes | Orienta por norma | AUP, SOP, placa de instrução |

### Representação visual sugerida \[DIDÁTICO\]

Linha do tempo de um incidente (Antes → Durante → Depois) com os tipos posicionados: Diretivo, Dissuasor e Preventivo antes; Detectivo durante/depois; Corretivo depois; Compensatório atravessando toda a linha como faixa paralela. (Renderizado como imagem após esta seção.)

&#91;embedded content: Tipos de controle na linha do tempo do incidente\]

### Comparação — o que mais confunde

- Preventivo vs Dissuasor: o preventivo impede de fato (a tranca não deixa abrir); o dissuasor só desencoraja (a placa faz o ladrão desistir, mas não tranca nada). A mesma câmera pode ser dissuasora (visível, intimida) e detectiva (grava e permite investigar).
- Detectivo vs Corretivo: detectar é descobrir (IDS avisa); corrigir é consertar (restaurar backup). O IDS detecta; o IPS, que bloqueia, tende a preventivo.
- Diretivo vs Preventivo: o diretivo manda fazer (a política exige senha forte); o preventivo é o mecanismo que impõe (o sistema rejeita senha fraca).
- Compensatório: só é compensatório porque o controle ideal não pôde ser usado. Se a questão disser "a solução padrão não era viável, então adotou-se X", X é compensatório.

### Memorização \[DIDÁTICO\]

Coloque cada tipo na linha do tempo do incidente. Antes: Diretivo (manda), Dissuasor (assusta), Preventivo (bloqueia). Durante/Depois: Detectivo (vê). Depois: Corretivo (conserta). Transversal: Compensatório (substitui o ideal). Frase-gatilho do compensatório: "não deu para usar o certo, então usei outro".

### Pegadinhas típicas da prova

1. CCTV: a mesma câmera é dissuasora (visível) e detectiva (grava). A resposta depende do foco do enunciado — intimidar ou investigar.
2. Preventivo x Dissuasor: trocar impedir por desencorajar. Tranca é preventiva; placa é dissuasora.
3. Compensatório disfarçado: sempre que houver "o controle ideal não era possível", pense compensatório — mesmo que o exemplo pareça técnico.
4. Diretivo x Preventivo: a política (diretivo) não é o mecanismo (preventivo).

### Matriz categoria × tipo \[COMPLEMENTAR\]

A CompTIA pode cruzar os dois eixos: um mesmo controle tem uma categoria e um tipo. Exemplos de cruzamento: criptografia = Técnico + Preventivo; placa de aviso = Físico/Gerencial + Dissuasor; IDS = Técnico + Detectivo; restauração de backup = Operacional/Técnico + Corretivo; AUP = Gerencial + Diretivo; guarda de segurança = Físico + Preventivo/Dissuasor. (Matriz visual renderizada como imagem após esta seção.)

&#91;embedded content: Matriz categoria × tipo · exemplos cruzados\]

### Mini-desafio 1.1-B

Após um ataque de ransomware, a equipe de TI restaurou os sistemas a partir dos backups mais recentes e voltou a operação ao normal. Que tipo de controle foi aplicado?

1. Preventivo
2. Detectivo
3. Corretivo
4. Dissuasor

### Mini-desafio 1.1-C

Um sistema legado crítico não suporta a autenticação multifator exigida pela política. Como mitigação, a empresa isolou esse sistema em uma sub-rede separada e aumentou o monitoramento. Esse controle é melhor classificado como:

1. Preventivo
2. Compensatório
3. Diretivo
4. Detectivo

### Resumo de alta retenção — tipos

- PRECISO SABER: 6 tipos pela função/momento — Preventivo, Dissuasor, Detectivo, Corretivo, Compensatório, Diretivo.
- PRECISO RECONHECER: impedir→Preventivo; desencorajar→Dissuasor; detectar/registrar→Detectivo; restaurar→Corretivo; alternativa ao ideal→Compensatório; instruir/norma→Diretivo.
- NÃO CONFUNDIR: Preventivo (impede) ≠ Dissuasor (desencoraja); Detectivo (vê) ≠ Corretivo (conserta); Diretivo (manda) ≠ Preventivo (impõe).
- PEGADINHAS: CCTV dissuasor vs detectivo; compensatório quando o ideal não é viável.
- MEMORIZAÇÃO: posicione na linha Antes/Durante/Depois; compensatório é transversal.
- NA PRÁTICA: IDS/SIEM (detectivo), IPS/firewall (preventivo), backup/quarentena (corretivo), segmentação por legado (compensatório), AUP/SOP (diretivo).

## 1.2 Conceitos fundamentais de segurança — parte 1 \[OFICIAL\]

Este objetivo reúne os pilares conceituais da segurança. Começamos pela tríade CIA, não repúdio, AAA, análise de lacunas e Zero Trust. Segurança física e tecnologia de engano vêm na parte 2.

### Tríade CIA — Confidentiality, Integrity, Availability

Os três objetivos que toda medida de segurança busca preservar. A prova cobra reconhecer qual pilar foi afetado em um cenário.

- Confidentiality → Confidencialidade → só quem tem autorização acessa a informação. Protegida por criptografia, controle de acesso, MFA. Violação: vazamento de dados.
- Integrity → Integridade → a informação não foi alterada indevidamente; está correta e completa. Protegida por hashing, assinaturas digitais, controle de versões. Violação: adulteração de um registro.
- Availability → Disponibilidade → a informação e os sistemas estão acessíveis quando necessários. Protegida por redundância, backups, proteção contra DDoS. Violação: ataque DDoS, ransomware que trava o acesso.

&#91;COMPLEMENTAR\] A DAD é o oposto da CIA: Disclosure (divulgação indevida), Alteration (alteração), Denial/Destruction (negação/destruição) — útil para lembrar o que cada violação ataca.

### Não repúdio (Non-repudiation)

Garante que quem praticou uma ação não possa negar tê-la praticado. É sustentado por assinaturas digitais e por logs/auditoria confiáveis. Exemplo: um e-mail assinado digitalmente prova que aquele remetente o enviou. Não confunda com integridade: a integridade garante que a mensagem não mudou; o não repúdio garante quem a originou.

### AAA — Authentication, Authorization, Accounting

O modelo que controla identidade e acesso.

- Authentication → Autenticação → provar quem você é (senha, biometria, token). A prova distingue autenticação de pessoas e autenticação de sistemas (ex.: certificados de máquina, 802.1X para dispositivos).
- Authorization → Autorização → definir o que você pode fazer depois de autenticado (permissões, modelos de autorização como RBAC, ABAC).
- Accounting → Auditoria/Contabilização → registrar o que você fez (logs, trilhas de auditoria). Sustenta o não repúdio.

Ordem mnemônica: primeiro provo quem sou (Authentication), depois recebo permissões (Authorization), e tudo que faço é registrado (Accounting).

### Análise de lacunas (Gap analysis)

Comparação entre o estado atual de segurança e o estado desejado (uma norma, uma baseline, um objetivo), identificando as lacunas a fechar. Exemplo: comparar os controles atuais com os exigidos pela ISO 27001 e listar o que falta. Na prova, aparece como o passo que mostra a diferença entre onde você está e onde precisa estar.

### Zero Trust (Confiança zero)

Modelo que parte do princípio nunca confie, sempre verifique: nenhuma entidade é confiável por padrão, nem dentro da rede. Cada acesso é verificado continuamente. A CompTIA divide o Zero Trust em dois planos \[OFICIAL\]:

**Plano de controle (Control Plane)** — decide se o acesso é permitido:

- Identidade adaptativa (adaptive identity): a verificação se ajusta ao risco e ao contexto do pedido.
- Redução do escopo da ameaça (threat scope reduction): limitar o alcance do que um acesso pode atingir.
- Controle de acesso orientado por políticas (policy-driven access control): a política decide o acesso.
- Administrador de políticas (policy administrator): componente que executa a decisão, estabelecendo/encerrando a sessão.
- Mecanismo de política (policy engine): componente que toma a decisão de permitir ou negar.

**Plano de dados (Data Plane)** — executa o acesso aprovado:

- Zonas de confiança implícitas (implicit trust zones): áreas onde, após a verificação, o tráfego flui.
- Assunto/Sistema (subject/system): quem ou o que solicita o acesso.
- Ponto de aplicação de políticas (policy enforcement point, PEP): onde a decisão é efetivamente aplicada.

&#91;COMPLEMENTAR\] Regra de ouro: o Policy Engine decide, o Policy Administrator comunica/executa a decisão, e o Policy Enforcement Point aplica no caminho dos dados.

### Representação visual sugerida \[DIDÁTICO\]

(1) Triângulo CIA com um pilar em cada vértice e a violação correspondente ao lado. (2) Fluxo do Zero Trust: Assunto → PEP → (consulta ao plano de controle: Policy Engine decide, Policy Administrator executa) → acesso liberado no plano de dados. (Ambos renderizados como imagem após esta seção.)

&#91;embedded content: Tríade CIA · pilar e violação correspondente\]

&#91;embedded content: Fluxo Zero Trust · Engine decide, Administrator executa, PEP aplica\]

### Comparação — o que mais confunde

- Integridade vs Não repúdio: integridade = a mensagem não mudou; não repúdio = o autor não pode negar que a enviou.
- Autenticação vs Autorização: autenticar = quem é você; autorizar = o que você pode. Autenticar sempre vem antes.
- Confidencialidade vs Privacidade: confidencialidade é proteger o acesso ao dado; privacidade (visto no Domínio 5) trata do direito do titular sobre seus dados.
- Policy Engine vs Policy Administrator: o Engine decide (sim/não); o Administrator comunica e aplica a decisão abrindo/fechando a sessão.

### Memorização \[DIDÁTICO\]

- CIA = Confidencial, Íntegro, Acessível. DAD é o espelho dos ataques.
- AAA em ordem: Autentico → Autorizo → Audito.
- Zero Trust: Engine decide, Administrator executa, PEP aplica. "Decide, executa, aplica."

### Pegadinhas típicas da prova

1. Trocar integridade por não repúdio (ou vice-versa) em cenários com assinatura digital — a assinatura fornece ambos, mas o enunciado foca em um.
2. Chamar de autorização algo que é autenticação (ex.: "o usuário digitou a senha" é autenticação, não autorização).
3. Atribuir a decisão de acesso ao PEP — quem decide é o Policy Engine; o PEP só aplica.
4. Achar que Zero Trust confia em quem já está na rede interna — justamente o contrário.

### Como a CompTIA transforma isso em questão + raciocínio

Cenário descreve um incidente e pergunta qual pilar da CIA foi violado, ou descreve um componente Zero Trust e pede o nome. Raciocínio: para a CIA, pergunte o que o atacante conseguiu — ver o dado (confidencialidade), mudar o dado (integridade) ou impedir o acesso (disponibilidade). Para Zero Trust, separe quem decide (Engine) de quem aplica (PEP).

### Mini-desafio 1.2-A

Um invasor alterou silenciosamente os valores de um banco de dados financeiro, sem copiá-los nem derrubar o sistema. Qual pilar da tríade CIA foi diretamente violado?

1. Confidencialidade
2. Integridade
3. Disponibilidade
4. Não repúdio

### Mini-desafio 1.2-B

Em uma arquitetura Zero Trust, qual componente é responsável por tomar a decisão de permitir ou negar um pedido de acesso?

1. Policy Enforcement Point (PEP)
2. Policy Administrator
3. Policy Engine
4. Implicit trust zone

### Resumo de alta retenção — conceitos fundamentais (1)

- PRECISO SABER: CIA (Confidencialidade/Integridade/Disponibilidade), não repúdio, AAA (Autenticação/Autorização/Auditoria), gap analysis, Zero Trust (planos de controle e de dados).
- PRECISO RECONHECER: ver dado→confidencialidade; mudar dado→integridade; travar acesso→disponibilidade; "não pode negar"→não repúdio; Engine decide, PEP aplica.
- NÃO CONFUNDIR: integridade ≠ não repúdio; autenticação ≠ autorização; Engine ≠ PEP.
- PEGADINHAS: assinatura cobre integridade e não repúdio; Zero Trust não confia na rede interna.
- MEMORIZAÇÃO: Autentico→Autorizo→Audito; "decide, executa, aplica".
- NA PRÁTICA: SOC investiga violações de CIA nos logs (accounting); Zero Trust rege o acesso em redes modernas e nuvem.

## 1.2 Conceitos fundamentais — parte 2: segurança física e tecnologia de engano \[OFICIAL\]

### Segurança física

Controles tangíveis que protegem instalações e ativos. A prova cobra reconhecer a função de cada um.

- Barreiras (barriers): obstáculos físicos que limitam a passagem.
- Entrada de controle de acesso (access control vestibule), antiga mantrap: eclusa de duas portas que impede tailgating — a segunda porta só abre após a primeira fechar.
- Cercas (fences): perímetro; altura e anti-escalada variam conforme o nível desejado.
- Vigilância de vídeo (video surveillance / CCTV): grava e permite investigar; visível, também dissuade.
- Proteções de segurança (security guards): pessoas que controlam e respondem.
- Crachá de acesso (access badge): credencial física, muitas vezes com RFID/NFC.
- Iluminação (lighting): reduz esconderijos e apoia a vigilância; é dissuasora e de apoio ao detectivo.
- Sensores (sensors): detectam presença ou movimento. Tipos oficiais:
  - Infravermelho (infrared): detecta calor/corpo.
  - Pressão (pressure): detecta peso sobre uma superfície.
  - Microondas (microwave): detecta movimento por reflexão de ondas.
  - Ultrassônico (ultrasonic): detecta movimento por ondas sonoras de alta frequência.

### Tecnologia de engano e interrupção (Deception and disruption technology)

Recursos que atraem, detectam e atrasam o atacante, gerando inteligência. Diferença-chave da prova: o que cada "honey" representa.

- Honeypot → pote de mel → um sistema isca único, feito para ser atacado, para estudar o adversário e desviá-lo de alvos reais.
- Honeynet → rede isca → uma rede inteira de honeypots, simulando um ambiente completo.
- Honeyfile → arquivo isca → um arquivo atraente (ex.: "senhas.xlsx") que, se acessado, dispara alerta.
- Honeytoken → credencial/dado isca → um dado falso (conta, chave de API, registro) plantado para que, se usado, denuncie o acesso indevido.

&#91;COMPLEMENTAR\] Pense em escala e granularidade crescentes: token (um dado) → file (um arquivo) → pot (um host) → net (uma rede).

### Representação visual sugerida \[DIDÁTICO\]

Escada de granularidade da tecnologia de engano: Honeytoken (dado) → Honeyfile (arquivo) → Honeypot (host) → Honeynet (rede), cada degrau maior que o anterior. (Renderizado como imagem após esta seção.)

&#91;embedded content: Tecnologia de engano · granularidade crescente\]

### Comparação — o que mais confunde

- Honeypot vs Honeynet: um host isca (pot) vs uma rede inteira de iscas (net).
- Honeyfile vs Honeytoken: um arquivo isca que dispara ao ser aberto (file) vs um dado/credencial plantado que denuncia ao ser usado (token).
- Sensor de microondas vs ultrassônico: ambos detectam movimento; microondas usa ondas eletromagnéticas, ultrassônico usa som de alta frequência.
- Access control vestibule vs porta comum: o vestíbulo bloqueia tailgating com duas portas intertravadas.

### Memorização \[DIDÁTICO\]

Escala do engano, do menor para o maior: Token → File → Pot → Net ("um dado, um arquivo, uma máquina, uma rede").

### Pegadinhas típicas da prova

1. Trocar honeyfile por honeytoken: arquivo isca é file; credencial/dado isca é token.
2. Chamar uma rede inteira de iscas de honeypot — é honeynet.
3. Esquecer que CCTV e iluminação também têm efeito dissuasor, além do detectivo/apoio.
4. Confundir access control vestibule (duas portas, anti-tailgating) com simples catraca.

### Mini-desafio 1.2-C

A equipe de segurança plantou uma credencial de administrador falsa em um sistema. Qualquer tentativa de uso dessa credencial gera um alerta imediato, revelando acesso indevido. Que tecnologia de engano foi usada?

1. Honeypot
2. Honeynet
3. Honeyfile
4. Honeytoken

### Resumo de alta retenção — segurança física e engano

- PRECISO SABER: barreiras, vestíbulo de acesso, cercas, CCTV, guardas, crachá, iluminação, sensores (infravermelho/pressão/microondas/ultrassônico); honeypot/honeynet/honeyfile/honeytoken.
- PRECISO RECONHECER: duas portas intertravadas→vestíbulo; dado isca→honeytoken; arquivo isca→honeyfile; host isca→honeypot; rede isca→honeynet.
- NÃO CONFUNDIR: file (arquivo) ≠ token (dado/credencial); pot (host) ≠ net (rede).
- PEGADINHAS: CCTV é detectivo e dissuasor; vestíbulo combate tailgating.
- MEMORIZAÇÃO: Token → File → Pot → Net (granularidade crescente).
- NA PRÁTICA: honeytokens e honeyfiles são ótimos sinais de detecção precoce para o SOC; honeynets apoiam threat intelligence.

## 1.3 Gestão de mudanças e seu impacto na segurança \[OFICIAL\]

Mudanças mal controladas abrem brechas. A gestão de mudanças (change management) garante que toda alteração passe por aprovação, análise e documentação. A prova cobra reconhecer cada elemento do processo e por que ele importa para a segurança.

### Processos de negócio que impactam a operação de segurança

- Processo de aprovação (approval process): nenhuma mudança entra em produção sem autorização formal — evita alterações não revisadas.
- Propriedade (ownership): alguém é responsável por conduzir a mudança do início ao fim.
- Partes interessadas (stakeholders): quem é afetado e precisa ser consultado/informado.
- Análise de impacto (impact analysis): avaliar o que a mudança pode quebrar ou expor antes de aplicá-la.
- Resultado dos testes (test results): a mudança foi validada em ambiente controlado antes da produção.
- Plano de remediação / reversão (backout plan): como voltar atrás se a mudança falhar.
- Janelas de manutenção (maintenance windows): horários planejados para minimizar impacto.
- Procedimentos operacionais padrão (SOPs): passos consistentes e repetíveis para executar a mudança.

### Implicações técnicas

- Listas de permissão/negação (allow lists / deny lists): mudanças podem exigir ajustar o que é permitido ou bloqueado.
- Atividades restritas (restricted activities): o escopo autorizado da mudança deve ser respeitado.
- Tempo de inatividade (downtime): algumas mudanças derrubam serviços temporariamente — precisa ser previsto.
- Reinicialização de serviço / de aplicativo (service / application restart): muitas mudanças só fazem efeito após reinício.
- Aplicativos legados (legacy applications): sistemas antigos podem não suportar a mudança e exigir cuidado especial.
- Dependências (dependencies): uma mudança pode afetar outros sistemas conectados.

### Documentação

- Atualização de diagramas (updating diagrams): manter os diagramas de rede/arquitetura refletindo a realidade após a mudança.
- Atualização de políticas/procedimentos (updating policies/procedures): a documentação normativa acompanha a mudança.

### Controle de versões (Version control)

Registrar e rastrear versões de configurações, código e documentos, permitindo comparar, auditar e reverter. É o que torna possível saber o que mudou, quando e por quem.

### Representação visual sugerida \[DIDÁTICO\]

Fluxograma do ciclo de mudança: Solicitação → Aprovação → Análise de impacto → Teste → Janela de manutenção (implantação) → Documentação → (se falhar) Plano de reversão. (Renderizado como imagem após esta seção.)

&#91;embedded content: Ciclo de gestão de mudanças com plano de reversão\]

### Comparação — o que mais confunde

- Análise de impacto vs Resultado dos testes: a análise prevê riscos antes; os testes comprovam o comportamento em ambiente controlado.
- Plano de remediação (backout) vs Plano de remediação de vulnerabilidade: aqui, backout é voltar atrás da mudança; no Domínio 4, remediação é corrigir uma falha de segurança.
- Allow list vs Deny list: a allow list só permite o que está na lista (mais restritiva e segura); a deny list bloqueia o que está na lista (permite o resto).

### Memorização \[DIDÁTICO\]

Ciclo CARTDR: Solicita → Aprova → Analisa impacto → Testa → Implanta na janela → Documenta → (Reverte se falhar). Toda mudança segura tem um caminho de volta (backout).

### Pegadinhas típicas da prova

1. Esquecer o backout plan: a resposta certa frequentemente destaca a necessidade de um plano de reversão antes de aplicar a mudança.
2. Confundir allow list com deny list: allow list é mais segura por negar tudo que não está explicitamente permitido.
3. Aplicar mudança sem análise de impacto nem aprovação — a questão quer que você aponte a falha de processo.
4. Não atualizar diagramas/documentação após a mudança — gera risco por informação desatualizada.

### Mini-desafio 1.3-A

Uma equipe vai aplicar uma atualização crítica em um servidor de produção. Qual elemento da gestão de mudanças garante que, se a atualização causar falha, o sistema possa retornar rapidamente ao estado anterior?

1. Análise de impacto
2. Janela de manutenção
3. Plano de reversão (backout plan)
4. Procedimento operacional padrão

### Resumo de alta retenção — gestão de mudanças

- PRECISO SABER: aprovação, propriedade, stakeholders, análise de impacto, testes, backout plan, janelas de manutenção, SOPs; implicações técnicas (downtime, restart, legado, dependências, allow/deny list); documentação e controle de versões.
- PRECISO RECONHECER: "voltar atrás"→backout plan; "prever riscos antes"→análise de impacto; "só o que está na lista"→allow list.
- NÃO CONFUNDIR: análise de impacto (antes) ≠ testes (validação); allow list (restritiva) ≠ deny list (permissiva).
- PEGADINHAS: faltou backout; faltou aprovação/análise; documentação desatualizada.
- MEMORIZAÇÃO: Solicita→Aprova→Analisa→Testa→Implanta→Documenta→Reverte.
- NA PRÁTICA: change management reduz incidentes causados por alterações; controle de versões sustenta auditoria e rollback.

## 1.4 Soluções criptográficas apropriadas \[OFICIAL\]

Criptografia é a espinha dorsal da confidencialidade, integridade e não repúdio. Este objetivo é extenso e muito cobrado. Vamos por blocos: PKI, tipos e níveis de cifragem, ferramentas, ofuscação, hashing, assinaturas e certificados.

### Infraestrutura de chave pública (PKI)

Sistema que gerencia chaves e certificados digitais.

- Chave pública (public key): compartilhada livremente; cifra o que só a chave privada decifra.
- Chave privada (private key): secreta; decifra o que a pública cifrou e assina digitalmente.
- Key escrow (custódia de chaves): uma cópia da chave privada é guardada por um terceiro confiável, para recuperação em caso de perda. Risco: concentra poder — se comprometido, expõe tudo.

&#91;COMPLEMENTAR\] Regra prática da criptografia assimétrica: para confidencialidade, cifre com a chave pública do destinatário; para autenticidade/não repúdio, assine com a sua chave privada.

### Criptografia: tipos

- Simétrica (symmetric): a mesma chave cifra e decifra. Rápida, boa para grandes volumes. Desafio: distribuir a chave com segurança. Exemplos: AES, 3DES.
- Assimétrica (asymmetric): par de chaves (pública/privada). Mais lenta, resolve a troca de chave e permite assinatura. Exemplos: RSA, ECC.
- Troca de chave (key exchange): como as partes combinam uma chave de sessão com segurança (ex.: Diffie-Hellman).
- Algoritmos e tamanho de chave (algorithms / key length): quanto maior a chave, maior a resistência a força bruta (ex.: AES-256).

### Criptografia: níveis (onde se aplica)

- Disco completo (full-disk, FDE): cifra todo o disco (ex.: BitLocker).
- Partição / Volume: cifra uma divisão específica.
- Arquivo (file): cifra arquivos individuais.
- Banco de dados (database): cifra os dados armazenados no BD.
- Registro (record): cifra registros específicos dentro de uma base.
- Transporte/comunicação (transport/communication): cifra os dados em trânsito (ex.: TLS, IPsec).

### Ferramentas de criptografia

- TPM → Trusted Platform Module → chip na placa-mãe que armazena chaves e mede a integridade do boot. Protege chaves de FDE localmente.
- HSM → Hardware Security Module → dispositivo dedicado (geralmente de rede/servidor) para gerar e guardar chaves em alta escala e com alta segurança.
- Sistema de gerenciamento de chaves (key management system, KMS): centraliza ciclo de vida das chaves (geração, rotação, revogação).
- Enclave seguro (secure enclave): área isolada do processador para operações sensíveis.

Diferença TPM vs HSM \[COMPLEMENTAR\]: TPM é um chip embarcado em um único dispositivo (nível de máquina); HSM é um appliance dedicado para muitas chaves/serviços (nível de organização).

### Ofuscação (Obfuscation)

Tornar os dados menos compreensíveis sem necessariamente cifrá-los.

- Esteganografia (steganography): esconder a informação dentro de outro arquivo (ex.: dados ocultos em uma imagem).
- Tokenização (tokenization): substituir o dado sensível por um token sem valor; o dado real fica em um cofre separado. Muito usado em pagamentos (PCI DSS).
- Mascaramento de dados (data masking): ocultar parte do dado (ex.: mostrar só os 4 últimos dígitos do cartão).

### Hashing e salting

- Hashing: função de mão única que gera um resumo (digest) de tamanho fixo. Garante integridade: se o dado mudar, o hash muda. Exemplos: SHA-256. Não é reversível.
- Salting (sal): valor aleatório adicionado antes do hash da senha, para impedir ataques de rainbow table e tornar hashes idênticos diferentes.
- Key stretching (alongamento de chave): aplicar a função muitas vezes para tornar a quebra mais lenta (ex.: PBKDF2, bcrypt).
- Colisão (collision): quando duas entradas diferentes geram o mesmo hash — falha de um algoritmo fraco (ex.: MD5).

### Assinaturas digitais, blockchain e livro-razão

- Assinatura digital (digital signature): hash da mensagem cifrado com a chave privada do remetente. Fornece integridade, autenticidade e não repúdio.
- Blockchain: registro distribuído e encadeado por hashes, resistente a adulteração.
- Livro-razão público (public ledger): registro aberto e verificável de transações.

### Certificados digitais

- Autoridade certificadora (CA): emite e assina certificados, atestando identidades.
- Lista de revogação de certificados (CRL): lista de certificados revogados antes do vencimento.
- OCSP (Online Certificate Status Protocol): consulta em tempo real se um certificado é válido (alternativa mais ágil à CRL).
- Autoassinado (self-signed): certificado assinado pela própria entidade; não confiável por padrão fora do ambiente interno.
- Terceiros (third-party): certificado emitido por uma CA pública confiável.
- Raiz de confiança (root of trust): a CA raiz na qual toda a cadeia confia.
- CSR (Certificate Signing Request): solicitação enviada à CA para emitir um certificado.
- Wildcard: certificado que cobre todos os subdomínios de um domínio (ex.: \*.exemplo.com).

### Representação visual sugerida \[DIDÁTICO\]

(1) Comparação simétrica vs assimétrica: uma chave única vs par pública/privada. (2) Fluxo de assinatura digital: remetente gera hash → cifra com a privada → destinatário verifica com a pública. (Ambos renderizados como imagem após esta seção.)

&#91;embedded content: Criptografia simétrica vs assimétrica\]

&#91;embedded content: Fluxo de assinatura digital\]

### Comparação — o que mais confunde

- Simétrica vs Assimétrica: uma chave (rápida, mesma chave) vs par de chaves (mais lenta, resolve troca de chave e assina).
- Cifrar vs Assinar: para sigilo, cifre com a pública do destinatário; para provar autoria, assine com sua privada.
- Hashing vs Criptografia: hash é de mão única (não reversível, garante integridade); criptografia é reversível com a chave (garante confidencialidade).
- Tokenização vs Mascaramento: tokenização substitui por um token com cofre reverso; mascaramento apenas oculta parte do dado.
- TPM vs HSM: chip de uma máquina vs appliance para muitas chaves.
- CRL vs OCSP: lista baixada periodicamente vs consulta em tempo real.

### Memorização \[DIDÁTICO\]

- Confidencialidade → cifrar com a chave PÚBLICA do destinatário. Não repúdio → assinar com a SUA chave PRIVADA. ("Público para esconder, privado para provar.")
- Hash = integridade e mão única. Salt = contra rainbow tables. Stretching = deixar lento.
- TPM = um; HSM = muitos. CRL = lista; OCSP = online/tempo real.

### Pegadinhas típicas da prova

1. Inverter cifrar/assinar: cifrar com a privada não dá sigilo (qualquer um tem a pública) — dá assinatura.
2. Tratar hashing como criptografia reversível — hash não se desfaz.
3. Confundir tokenização com mascaramento ou com criptografia.
4. Achar que certificado autoassinado é confiável externamente — não é.
5. Trocar CRL por OCSP: OCSP é a verificação em tempo real.
6. Esquecer o salt ao proteger senhas — hash puro é vulnerável a rainbow table.

### Como a CompTIA transforma isso em questão + raciocínio

Cenário pede escolher a solução criptográfica adequada (ex.: proteger senhas armazenadas, garantir não repúdio de um contrato, proteger cartões em um sistema de pagamento). Raciocínio: identifique o objetivo — sigilo (criptografia), integridade (hash), autoria/não repúdio (assinatura), substituição de dado sensível (tokenização). Depois escolha a ferramenta/nível coerente (FDE para disco, TLS para trânsito, HSM para muitas chaves).

### Mini-desafio 1.4-A

Uma empresa precisa armazenar senhas de usuários de forma segura. Além de aplicar uma função de hash, qual técnica adicional impede que senhas iguais gerem o mesmo hash e protege contra ataques de rainbow table?

1. Key escrow
2. Salting
3. Tokenização
4. Esteganografia

### Mini-desafio 1.4-B

Um executivo precisa enviar um contrato de forma que o destinatário tenha certeza de que foi ele quem o enviou e que o conteúdo não foi alterado. Qual solução atende a integridade, autenticidade e não repúdio simultaneamente?

1. Criptografia simétrica com AES
2. Assinatura digital
3. Mascaramento de dados
4. Full-disk encryption

### Mini-desafio 1.4-C

Qual mecanismo permite verificar, em tempo real, se um certificado digital ainda é válido ou foi revogado?

1. CRL
2. CSR
3. OCSP
4. Wildcard

### Resumo de alta retenção — criptografia

- PRECISO SABER: PKI (pública/privada/key escrow); simétrica vs assimétrica; níveis (FDE, arquivo, BD, transporte); TPM/HSM/KMS/enclave; ofuscação (estegano/tokenização/masking); hashing/salting/key stretching; assinatura digital; certificados (CA, CRL, OCSP, self-signed, CSR, wildcard).
- PRECISO RECONHECER: sigilo→cifrar com pública; não repúdio→assinar com privada; integridade→hash; senha→hash+salt; cartão→tokenização; tempo real→OCSP.
- NÃO CONFUNDIR: hash (mão única) ≠ cifra (reversível); tokenização ≠ masking; TPM (um) ≠ HSM (muitos); CRL (lista) ≠ OCSP (tempo real).
- PEGADINHAS: inverter cifrar/assinar; hash tratado como reversível; self-signed confiável externamente.
- MEMORIZAÇÃO: "público para esconder, privado para provar"; TPM=um, HSM=muitos.
- NA PRÁTICA: TLS/IPsec protegem trânsito; FDE/TPM protegem endpoints; HSM/KMS sustentam PKI corporativa; tokenização atende PCI DSS.

## Revisão do Domínio 1.0

### Revisão 20/80 — os 20% que explicam 80% do domínio

1. Categoria responde quem/o que executa (Técnico, Gerencial, Operacional, Físico); tipo responde o que o controle faz (Preventivo, Dissuasor, Detectivo, Corretivo, Compensatório, Diretivo). Não misture os eixos.
2. CIA: ver o dado (confidencialidade), mudar o dado (integridade), travar o acesso (disponibilidade).
3. AAA em ordem: Autentico (quem sou) → Autorizo (o que posso) → Audito (o que fiz).
4. Zero Trust: nunca confie, sempre verifique; o Engine decide, o PEP aplica.
5. Criptografia: público para esconder, privado para provar; hash é integridade de mão única; senha leva salt.
6. Gestão de mudanças: toda mudança segura tem aprovação, análise de impacto, teste e plano de reversão.
7. Certificados: CRL é lista, OCSP é tempo real; self-signed não é confiável fora do ambiente interno.

### Mapa mental do Domínio 1.0

(Renderizado como imagem após esta seção: o Domínio 1.0 ao centro, com quatro ramos — Controles, Conceitos fundamentais, Gestão de mudanças e Criptografia — e seus subtemas.)

&#91;embedded content: Mapa mental do Domínio 1.0\]

### Tabela dos conceitos mais confundidos

| Par confundido | Como diferenciar |
| --- | --- |
| Categoria × Tipo | Categoria = quem executa; Tipo = o que faz |
| Preventivo × Dissuasor | Impede de fato × apenas desencoraja |
| Detectivo × Corretivo | Descobre × conserta/restaura |
| Integridade × Não repúdio | Dado não mudou × autor não pode negar |
| Autenticação × Autorização | Quem você é × o que você pode |
| Policy Engine × PEP | Decide × aplica |
| Hashing × Criptografia | Mão única (integridade) × reversível (sigilo) |
| Tokenização × Mascaramento | Substitui por token com cofre × oculta parte do dado |
| TPM × HSM | Chip de uma máquina × appliance para muitas chaves |
| CRL × OCSP | Lista periódica × verificação em tempo real |
| Allow list × Deny list | Só o permitido × bloqueia o listado |
| Honeyfile × Honeytoken | Arquivo isca × dado/credencial isca |

### Flashcards (pergunta → resposta)

| Pergunta | Resposta |
| --- | --- |
| Firewall é qual categoria? | Técnico (Technical/Logical) |
| Sinônimo de controle gerencial? | Administrative |
| Backup restaurado após ataque é qual tipo? | Corretivo |
| Placa "área monitorada" é qual tipo? | Dissuasor |
| Controle usado quando o ideal não é viável? | Compensatório |
| Pilar violado ao alterar dados? | Integridade |
| Ordem do AAA? | Autenticação → Autorização → Auditoria |
| Quem decide o acesso no Zero Trust? | Policy Engine |
| Para sigilo, cifra-se com qual chave? | Pública do destinatário |
| Para não repúdio, assina-se com qual chave? | Privada do remetente |
| Hash protege qual pilar? | Integridade |
| O que impede rainbow table em senhas? | Salting |
| Verificação de certificado em tempo real? | OCSP |
| Certificado que cobre subdomínios? | Wildcard |
| Rede inteira de iscas? | Honeynet |
| Elemento que permite voltar atrás de uma mudança? | Plano de reversão (backout) |

## Mini-simulado do Domínio 1.0

Dez questões no estilo da prova, cobrindo todo o domínio. As respostas comentadas estão na última seção. Responda antes de conferir.

**Q1.** Uma empresa instalou catracas com duas portas intertravadas na entrada do datacenter, de modo que a segunda porta só abre após a primeira fechar. Esse controle é melhor classificado, por categoria e tipo, como:

1. Técnico e Detectivo
2. Físico e Preventivo
3. Gerencial e Diretivo
4. Operacional e Corretivo

**Q2.** O time de segurança publicou um documento obrigatório definindo como os funcionários devem tratar dados confidenciais. Qual tipo de controle esse documento representa?

1. Preventivo
2. Compensatório
3. Diretivo
4. Detectivo

**Q3.** Durante uma investigação, o analista do SOC percebe que alertas que deveriam existir não foram gerados e vários registros de log simplesmente não estão presentes. Qual indicador está sendo observado?

1. Viagem impossível
2. Logs ausentes
3. Bloqueio de conta
4. Consumo de recursos

**Q4.** Um atacante conseguiu copiar e divulgar publicamente uma base de clientes. Qual pilar da tríade CIA foi violado?

1. Integridade
2. Disponibilidade
3. Confidencialidade
4. Não repúdio

**Q5.** Em uma arquitetura Zero Trust, o componente que efetivamente aplica a decisão de acesso no caminho dos dados é o:

1. Policy Engine
2. Policy Administrator
3. Policy Enforcement Point
4. Implicit trust zone

**Q6.** A empresa precisa proteger senhas armazenadas contra ataques de rainbow table. Além do hashing, o que deve ser aplicado?

1. Tokenização
2. Salting
3. Key escrow
4. Esteganografia

**Q7.** Um contrato eletrônico precisa garantir que o signatário não possa negar tê-lo assinado e que o conteúdo não foi alterado. Qual solução atende a esses requisitos?

1. Criptografia simétrica
2. Mascaramento de dados
3. Assinatura digital
4. Full-disk encryption

**Q8.** Antes de aplicar uma mudança crítica em produção, a equipe documenta como reverter o sistema ao estado anterior caso algo falhe. Esse elemento é o:

1. Procedimento operacional padrão
2. Plano de reversão (backout plan)
3. Janela de manutenção
4. Análise de impacto

**Q9.** Qual mecanismo permite a uma aplicação verificar, em tempo real, se um certificado digital específico foi revogado?

1. CRL
2. CSR
3. OCSP
4. Root of trust

**Q10.** A equipe de defesa plantou um arquivo atraente chamado "folha\_de\_pagamento.xlsx" em um servidor. Qualquer tentativa de abri-lo dispara um alerta. Qual tecnologia de engano foi usada?

1. Honeypot
2. Honeynet
3. Honeyfile
4. Honeytoken

## Gabarito comentado — Domínio 1.0

### Mini-desafios

**1.1-A — Resposta: 3 (Gerencial).** Uma política aprovada e publicada pela gestão é uma decisão administrativa, não uma tecnologia nem uma barreira física. Palavra-chave: "política". Erradas: Técnico (não há sistema executando), Operacional (não é execução de rotina), Físico (não é barreira).

**1.1-B — Resposta: 3 (Corretivo).** Restaurar sistemas a partir de backup após o ataque corrige e recupera o ambiente — age depois do incidente. Palavra-chave: "restaurou". Erradas: Preventivo (não impediu), Detectivo (não é descoberta), Dissuasor (não desencoraja).

**1.1-C — Resposta: 2 (Compensatório).** O controle ideal (MFA) não era viável no legado, então adotou-se uma alternativa (isolamento + monitoramento). O gatilho é "não suporta... como mitigação". Erradas: Preventivo/Detectivo descrevem só parte do efeito; Diretivo seria uma norma.

**1.2-A — Resposta: 2 (Integridade).** O invasor alterou os dados sem copiá-los (não é confidencialidade) nem derrubar o sistema (não é disponibilidade). Palavra-chave: "alterou os valores".

**1.2-B — Resposta: 3 (Policy Engine).** O Engine toma a decisão de permitir/negar. O PEP apenas aplica; o Administrator executa/estabelece a sessão; a implicit trust zone é área do plano de dados.

**1.2-C — Resposta: 4 (Honeytoken).** Credencial/dado isca plantado que denuncia ao ser usado. Honeyfile seria um arquivo; honeypot um host; honeynet uma rede.

**1.3-A — Resposta: 3 (Plano de reversão / backout plan).** É o elemento que permite voltar ao estado anterior se a mudança falhar. Análise de impacto prevê riscos antes; janela de manutenção é o horário; SOP é o passo a passo.

**1.4-A — Resposta: 2 (Salting).** O sal aleatório torna hashes de senhas iguais diferentes e inutiliza rainbow tables. Key escrow é custódia de chave; tokenização substitui dado por token; esteganografia esconde dado em outro arquivo.

**1.4-B — Resposta: 2 (Assinatura digital).** Fornece integridade, autenticidade e não repúdio ao mesmo tempo. AES (simétrica) dá só confidencialidade; masking oculta dado; FDE protege disco em repouso.

**1.4-C — Resposta: 3 (OCSP).** Verificação de validade/revogação em tempo real. CRL é a lista baixada periodicamente; CSR é a solicitação de emissão; wildcard cobre subdomínios.

### Mini-simulado

| Questão | Resposta | Comentário |
| --- | --- | --- |
| Q1 | 2 | Vestíbulo de acesso = barreira física (categoria Físico) que impede tailgating (tipo Preventivo) |
| Q2 | 3 | Documento obrigatório que orienta comportamento = Diretivo |
| Q3 | 2 | Ausência de registros esperados = indicador "logs ausentes" (missing logs) |
| Q4 | 3 | Dados copiados e divulgados = violação de Confidencialidade |
| Q5 | 3 | Quem aplica a decisão no caminho dos dados é o PEP; o Engine apenas decide |
| Q6 | 2 | Salting protege senhas contra rainbow table |
| Q7 | 3 | Assinatura digital cobre integridade, autenticidade e não repúdio |
| Q8 | 2 | Documentar como voltar atrás = plano de reversão (backout plan) |
| Q9 | 3 | Verificação em tempo real de revogação = OCSP |
| Q10 | 3 | Arquivo isca que dispara ao ser aberto = Honeyfile |

### Autodiagnóstico sugerido

| Acertos (de 10) | Classificação | Ação recomendada |
| --- | --- | --- |
| 9–10 | Excelente | Domínio sólido; avançar ao 2.0 |
| 7–8 | Bom | Revisar os pares da tabela de confundidos |
| 5–6 | Atenção | Refazer flashcards e releitura de 1.2 e 1.4 |
| 3–4 | Fraco | Reestudar o domínio inteiro com foco em controles e criptografia |
| 0–2 | Crítico | Reiniciar o domínio do zero, subtema por subtema |

**Subtemas que mais derrubam candidatos neste domínio:** distinção categoria × tipo (1.1), cifrar × assinar (1.4) e Policy Engine × PEP (1.2). Priorize esses três se errar questões relacionadas.

# Guia Security+ SY0-701 — Domínio 5.0: Gerenciamento e supervisão do programa de segurança

Oct 7, 2026 · @Pedro Henrique Ferraz

Material de estudo para a certificação CompTIA Security+ (SY0-701). O Domínio 5.0 vale 20% da prova e cobre o lado de gestão: governança, risco, terceiros, conformidade, auditorias e conscientização. Encerra a série dos cinco domínios. Todos os gabaritos ficam na última seção.

## Como usar este guia

Mesmo método dos domínios anteriores: cada conceito segue ideia simples, definição técnica, exemplo real, aplicação profissional (SOC, Blue Team, Red Team, redes e infraestrutura), comparação, memorização, pegadinhas, questão no estilo da prova, raciocínio de eliminação e resumo de alta retenção.

**Legenda de origem do conteúdo:**

| Marca | Significado |
| --- | --- |
| \[OFICIAL\] | Item que consta literalmente nos objetivos SY0-701 da CompTIA |
| \[COMPLEMENTAR\] | Conhecimento de apoio para entender o item oficial |
| \[DIDÁTICO\] | Exemplo, analogia ou cenário criado para fixar o conceito |

**Termos em inglês:** formato inglês → tradução → significado → como cai na prova.

**Mini-desafios e simulado:** nenhuma resposta aparece junto da pergunta. Todos os gabaritos comentados ficam na última seção.

**Caráter do Domínio 5.0:** com 20% do exame, é o domínio de gestão (GRC — governança, risco e conformidade). Menos técnico e mais conceitual: a prova testa definições precisas, cálculos de risco (SLE/ALE/ARO), ordem de conceitos e a capacidade de distinguir termos parecidos (papéis de dados, tipos de acordo, estratégias de risco). É muito "decoreba bem entendida" — vocabulário exato rende pontos.

**Estrutura do Domínio 5.0 (peso 20%):** seis objetivos oficiais — 5.1 Governança eficaz; 5.2 Processo de gerenciamento de riscos; 5.3 Gestão de riscos de terceiros; 5.4 Conformidade eficaz; 5.5 Tipos e finalidades de auditorias e avaliações; 5.6 Práticas de conscientização de segurança.

Com este guia, a série dos cinco domínios da Security+ SY0-701 fica completa.

## 5.1 Governança de segurança eficaz \[OFICIAL\]

Governança é o conjunto de diretrizes, políticas, padrões e estruturas que dirigem o programa de segurança. A prova cobra distinguir os tipos de documento e os papéis sobre os dados.

### A hierarquia de documentos (muito cobrada)

Do mais geral e obrigatório ao mais detalhado e prático:

- Diretrizes (guidelines): recomendações, não obrigatórias — orientam, mas não impõem.
- Políticas (policies): declarações obrigatórias de alto nível (o quê e por quê). Exemplos oficiais: AUP (política de uso aceitável), política de segurança da informação, continuidade de negócios, recuperação de desastre, resposta a incidentes, SDLC, gestão de mudanças.
- Padrões (standards): requisitos obrigatórios e específicos (ex.: padrão de senha, de controle de acesso, de segurança física, de criptografia).
- Procedimentos (procedures): passo a passo de como executar (gestão de mudanças, integração/desligamento, playbooks).

&#91;DIDÁTICO\] Pense: a política diz "devemos proteger senhas"; o padrão diz "mínimo 14 caracteres"; o procedimento diz "clique aqui para redefinir"; a diretriz sugere "prefira uma frase-senha".

### Considerações externas

Fatores de fora que moldam a governança: regulatório, jurídico, da indústria, e o alcance local/regional, nacional e global.

### Monitoramento, revisão e estruturas de governança

- Monitoramento e revisão (monitoring and revision): a governança é revisada periodicamente.
- Tipos de estrutura de governança: conselhos (boards), comitês (committees), entidades governamentais, e modelo centralizado vs descentralizado.

### Funções e responsabilidades sobre os dados (muito cobrado)

- Proprietário (owner): responsável final pelo dado; define classificação e quem acessa.
- Controlador (controller): decide por que e como os dados são processados (termo-chave em privacidade/GDPR).
- Processador (processor): processa os dados em nome do controlador (ex.: um provedor de nuvem).
- Custodiante/administrador (custodian/steward): cuida da proteção técnica do dado no dia a dia (backups, controles) — não decide, executa.

### Representação visual sugerida \[DIDÁTICO\]

Pirâmide da hierarquia de governança: Políticas (topo, obrigatório, o quê) → Padrões (requisitos específicos) → Procedimentos (passo a passo) e, ao lado, Diretrizes (recomendação, não obrigatória). (Renderizado como imagem após esta seção.)

&#91;embedded content: Hierarquia de governança · políticas, padrões, procedimentos e diretrizes\]

### Comparação — o que mais confunde

- Política × Padrão × Procedimento × Diretriz: política é o quê/por quê (obrigatória, geral); padrão é o requisito específico (obrigatório); procedimento é o passo a passo (como fazer); diretriz é recomendação (não obrigatória). A palavra-chave "obrigatório vs recomendado" separa diretriz das demais.
- Controlador × Processador: o controlador decide o propósito e os meios; o processador apenas processa por conta do controlador. O provedor de nuvem costuma ser processador.
- Owner × Custodian: o owner é o responsável/decide a classificação; o custodian implementa a proteção técnica. Owner decide, custodian executa.
- Centralizado × Descentralizado: governança concentrada em um ponto vs distribuída pelas unidades.

### Memorização \[DIDÁTICO\]

- Hierarquia: Política (o quê) → Padrão (quanto/qual exatamente) → Procedimento (como, passo a passo). Diretriz = sugestão (opcional).
- Controlador decide (o chefe dos dados); Processador faz o trabalho (o terceirizado).
- Owner decide a classificação; Custodian protege no dia a dia.

### Pegadinhas típicas da prova

1. Tratar diretriz como obrigatória — diretriz é recomendação.
2. Confundir padrão (requisito específico obrigatório) com procedimento (passo a passo).
3. Trocar controlador por processador — o controlador decide o propósito; o provedor de nuvem é processador.
4. Confundir owner (decide/classifica) com custodian (protege/executa).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve um documento ou um papel e pede a classificação. Raciocínio: é obrigatório e geral → política; requisito específico obrigatório → padrão; passo a passo → procedimento; recomendação opcional → diretriz. Para papéis: decide propósito dos dados → controlador; processa por conta de outro → processador; responsável/classifica → owner; protege tecnicamente → custodian.

### Mini-desafio 5.1-A

Um documento define que "toda senha deve ter no mínimo 14 caracteres e incluir caracteres especiais". Como esse documento é melhor classificado?

1. Diretriz
2. Política
3. Padrão
4. Procedimento

### Mini-desafio 5.1-B

Uma empresa contrata um provedor de nuvem que processa os dados de clientes exatamente conforme as instruções da empresa. No contexto de privacidade, o provedor de nuvem é o:

1. Controlador de dados
2. Processador de dados
3. Proprietário (owner)
4. Titular dos dados

### Resumo de alta retenção — governança

- PRECISO SABER: diretrizes, políticas (AUP, BC, DR, IR, SDLC), padrões, procedimentos; considerações externas; estruturas (conselhos, comitês, centralizado/descentralizado); papéis (owner, controller, processor, custodian).
- PRECISO RECONHECER: obrigatório/geral→política; requisito específico→padrão; passo a passo→procedimento; recomendação→diretriz; decide propósito→controlador; processa por outro→processador.
- NÃO CONFUNDIR: política ≠ padrão ≠ procedimento ≠ diretriz; controlador (decide) ≠ processador (executa); owner (classifica) ≠ custodian (protege).
- PEGADINHAS: diretriz não é obrigatória; padrão vs procedimento; controlador vs processador.
- MEMORIZAÇÃO: Política=o quê, Padrão=qual exatamente, Procedimento=como; controlador decide, processador faz.
- NA PRÁTICA: a governança guia todo o programa; os papéis de dados são centrais em privacidade/GDPR (5.4).

## 5.2 Processo de gerenciamento de riscos \[OFICIAL\]

O núcleo do domínio. A prova cobra o vocabulário, os cálculos quantitativos (SLE/ALE/ARO) e as estratégias de tratamento de risco.

### Identificação e avaliação

- Identificação de riscos (risk identification): descobrir quais riscos existem.
- Avaliação de riscos (risk assessment): pode ser ad hoc (pontual, sob demanda), recorrente (periódica), de uso único (one-time) ou contínua (continuous).

### Análise de risco

- Qualitativa (qualitative): usa julgamento/escalas (alto/médio/baixo) — subjetiva.
- Quantitativa (quantitative): usa números e valores monetários — objetiva.
- Fórmulas quantitativas (decore):
  - SLE (Single Loss Expectancy) = valor do ativo × fator de exposição (EF). Perda por um único incidente.
  - ARO (Annualized Rate of Occurrence): quantas vezes o incidente ocorre por ano.
  - ALE (Annualized Loss Expectancy) = SLE × ARO. Perda esperada por ano.
- Probabilidade, possibilidade, fator de exposição e impacto: ajustam a análise.

### Registro e tolerância ao risco

- Registro de risco (risk register): documento que lista os riscos, com indicadores-chave de risco (KRIs), proprietários de risco (risk owners) e o limiar de risco (risk threshold).
- Tolerância ao risco (risk tolerance): o quanto de desvio a organização suporta.
- Apetite ao risco (risk appetite): quanto risco a organização está disposta a assumir — pode ser expansionista (alto apetite), conservador (baixo) ou neutro.

### Estratégias de tratamento de risco (muito cobrado)

- Transferir (transfer): passar o risco a um terceiro (ex.: seguro).
- Aceitar (accept): assumir o risco conscientemente, com isenção (exemption) ou exceção (exception).
- Evitar (avoid): eliminar a atividade que gera o risco.
- Mitigar (mitigate): reduzir o risco com controles.

### Relatório e análise de impacto nos negócios (BIA)

- Relatório de riscos (risk reporting): comunicar os riscos à gestão.
- BIA (Business Impact Analysis): avalia o impacto de interrupções. Métricas-chave (decore):
  - RTO (Recovery Time Objective): tempo máximo aceitável para restaurar um serviço.
  - RPO (Recovery Point Objective): perda máxima aceitável de dados, medida no tempo (até onde voltar no backup).
  - MTTR (Mean Time To Repair): tempo médio para reparar.
  - MTBF (Mean Time Between Failures): tempo médio entre falhas (confiabilidade).

### Representação visual sugerida \[DIDÁTICO\]

(1) Cadeia de cálculo quantitativo: Valor do ativo × EF = SLE; SLE × ARO = ALE. (2) Diferença RTO × RPO numa linha do tempo do incidente: RPO olha para trás (dados perdidos), RTO olha para frente (tempo até voltar). (Ambos renderizados como imagem após esta seção.)

&#91;embedded content: Cálculo quantitativo · SLE e ALE\]

&#91;embedded content: RTO vs RPO na linha do tempo do incidente\]

### Comparação — o que mais confunde

- Qualitativa × Quantitativa: qualitativa usa escalas subjetivas (alto/médio/baixo); quantitativa usa números/dinheiro (SLE, ALE).
- SLE × ALE: SLE é a perda de um único incidente; ALE é a perda anual (SLE × ARO).
- RTO × RPO: RTO é quanto tempo até voltar (foco em tempo de recuperação); RPO é quanto dado você pode perder (foco no ponto de restauração/último backup). RPO olha para o passado; RTO para o futuro.
- MTTR × MTBF: MTTR é o tempo para reparar; MTBF é o tempo entre falhas (quanto maior, mais confiável).
- Apetite × Tolerância: apetite é quanto risco você quer assumir (estratégico); tolerância é o quanto de variação você aguenta na prática.
- Transferir × Aceitar × Evitar × Mitigar: passar a terceiro × assumir × eliminar a atividade × reduzir com controle.

### Memorização \[DIDÁTICO\]

- SLE = um susto. ALE = o susto × quantas vezes no ano (SLE × ARO).
- RPO = Ponto (dados que posso perder, olha para trás). RTO = Tempo (até voltar, olha para frente).
- MTBF = Between (entre falhas, confiabilidade). MTTR = To Repair (consertar).
- Estratégias: TAEM — Transferir, Aceitar, Evitar, Mitigar.

### Pegadinhas típicas da prova

1. Trocar SLE por ALE — ALE é anual (multiplica pelo ARO).
2. Inverter RTO e RPO — RPO é dados (ponto/passado), RTO é tempo (voltar/futuro).
3. Confundir apetite (quanto quer) com tolerância (quanto aguenta).
4. Chamar "contratar seguro" de mitigação — é transferência.
5. Confundir qualitativa (subjetiva) com quantitativa (numérica).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário dá valores e pede um cálculo, ou descreve uma decisão e pede a estratégia/métrica. Raciocínio de cálculo: perda de um incidente = valor × EF (SLE); perda anual = SLE × ARO (ALE). Para estratégias: seguro → transferir; aceitar formalmente → aceitação (isenção/exceção); desligar a atividade → evitar; aplicar controle → mitigar. RTO = tempo para voltar; RPO = dados aceitáveis a perder.

### Mini-desafio 5.2-A

Um ativo vale R$ 100.000. Um incidente específico causa, em média, 20% de perda do valor do ativo (fator de exposição) e ocorre 2 vezes por ano. Qual é a ALE (expectativa de perda anualizada)?

1. R$ 20.000
2. R$ 40.000
3. R$ 100.000
4. R$ 200.000

### Mini-desafio 5.2-B

Uma organização define que, após um desastre, pode tolerar a perda de no máximo 1 hora de dados. Qual métrica da BIA representa esse requisito?

1. RTO
2. RPO
3. MTTR
4. MTBF

### Mini-desafio 5.2-C

Uma empresa decide contratar uma apólice de seguro cibernético para cobrir perdas de um risco que não consegue eliminar. Qual estratégia de tratamento de risco é essa?

1. Mitigar
2. Evitar
3. Transferir
4. Aceitar

### Resumo de alta retenção — gerenciamento de riscos

- PRECISO SABER: identificação; avaliação (ad hoc, recorrente, contínua); análise (qualitativa/quantitativa, SLE=valor×EF, ALE=SLE×ARO); registro (KRI, risk owner, threshold); apetite (expansionista/conservador/neutro) e tolerância; estratégias (transferir, aceitar, evitar, mitigar); BIA (RTO, RPO, MTTR, MTBF).
- PRECISO RECONHECER: perda de um incidente→SLE; perda anual→ALE; tempo até voltar→RTO; dados aceitáveis a perder→RPO; seguro→transferir; eliminar atividade→evitar.
- NÃO CONFUNDIR: qualitativa ≠ quantitativa; SLE ≠ ALE; RTO (tempo) ≠ RPO (dados); apetite (quer) ≠ tolerância (aguenta); seguro é transferir, não mitigar.
- PEGADINHAS: SLE vs ALE; RTO vs RPO; seguro=transferir; apetite vs tolerância.
- MEMORIZAÇÃO: ALE=SLE×ARO; RPO=ponto/dados/passado, RTO=tempo/voltar/futuro; TAEM.
- NA PRÁTICA: o risk register orienta decisões; RTO/RPO guiam a arquitetura de resiliência (Domínio 3); análise quantitativa justifica investimentos em segurança.

## 5.3 Gestão de riscos de terceiros \[OFICIAL\]

Fornecedores e parceiros ampliam a superfície de ataque. A prova cobra principalmente distinguir os tipos de acordo (as siglas).

### Avaliação e seleção de fornecedores

- Avaliação do fornecedor (vendor assessment): teste de intrusão, cláusulas de direito de auditoria (right-to-audit), evidência de auditoria interna, avaliações independentes e análise da cadeia de suprimentos.
- Seleção de fornecedores (vendor selection): devida diligência (due diligence) e checagem de conflito de interesses.
- Monitoramento de fornecedores, questionários e regras de engajamento (rules of engagement): acompanhar o fornecedor ao longo do contrato.

### Tipos de acordo (decore as siglas — muito cobrado)

- SLA (Service Level Agreement): acordo de nível de serviço — define metas mensuráveis (uptime, tempo de resposta).
- MOA (Memorandum of Agreement): memorando de acordo — mais formal que o MOU, define responsabilidades.
- MOU (Memorandum of Understanding): memorando de entendimento — declaração de intenção, geralmente não vinculante.
- MSA (Master Service Agreement): contrato mestre que estabelece os termos gerais para futuros trabalhos.
- WO/SOW (Work Order / Statement of Work): ordem de serviço / declaração de trabalho — detalha o trabalho específico a ser feito (escopo, entregáveis, prazos).
- NDA (Non-Disclosure Agreement): acordo de confidencialidade — protege informações sigilosas.
- BPA (Business Partners Agreement): acordo de parceiros de negócios — define a relação entre parceiros (lucros, responsabilidades).

### Representação visual sugerida \[DIDÁTICO\]

Tabela das siglas de acordo com a função de cada uma: SLA (nível de serviço), MOU (intenção), MOA (responsabilidades formais), MSA (termos gerais), SOW (trabalho específico), NDA (confidencialidade), BPA (parceria). (Renderizado como imagem após esta seção.)

&#91;embedded content: Tipos de acordo · função de cada sigla\]

### Comparação — o que mais confunde

- MOU × MOA: o MOU é uma declaração de intenção, geralmente não vinculante; o MOA é mais formal e define responsabilidades. MOA é mais "sério" que o MOU.
- MSA × SOW: o MSA define os termos gerais de longo prazo; o SOW detalha o trabalho específico de cada projeto (sob o guarda-chuva do MSA). MSA é o contrato-mãe; SOW é o detalhe do serviço.
- SLA × MSA: o SLA define métricas de serviço (uptime, SLA é Service Level); o MSA define os termos gerais.
- NDA × BPA: NDA protege segredos (confidencialidade); BPA define a parceria de negócios.
- Right-to-audit × due diligence: a cláusula de direito de auditoria permite auditar o fornecedor; a due diligence é a investigação prévia antes de contratar.

### Memorização \[DIDÁTICO\]

- SLA = Service Level (métricas/uptime). MOU = entendimento (intenção). MOA = acordo (responsabilidades). MSA = Master (termos gerais). SOW = Statement of Work (o trabalho em si). NDA = segredo. BPA = parceiros.
- MSA é o contrato-mãe; SOW é o filho (o serviço específico).
- MOU = "combinamos a intenção"; MOA = "combinamos quem faz o quê".

### Pegadinhas típicas da prova

1. Trocar MOU por MOA — MOU é intenção (não vinculante); MOA define responsabilidades formais.
2. Confundir MSA (termos gerais) com SOW (trabalho específico).
3. Chamar de SLA um acordo que não define métricas de serviço.
4. Usar NDA para definir parceria — NDA é só confidencialidade; parceria é BPA.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve o propósito do documento e pede a sigla. Raciocínio: métricas de serviço/uptime → SLA; declaração de intenção → MOU; responsabilidades formais → MOA; termos gerais de longo prazo → MSA; detalhe do trabalho/entregáveis → SOW; proteger segredo → NDA; definir parceria → BPA.

### Mini-desafio 5.3-A

Uma empresa fecha um contrato com um provedor que garante 99,9% de disponibilidade e tempo de resposta máximo de 4 horas para chamados críticos, com penalidades se não cumprir. Qual tipo de acordo define essas métricas?

1. NDA
2. SLA
3. MOU
4. BPA

### Mini-desafio 5.3-B

Duas organizações assinam um documento que estabelece os termos gerais e as condições que regerão todos os projetos futuros entre elas, servindo de base para ordens de serviço específicas. Qual é esse acordo?

1. SOW
2. MSA
3. MOU
4. SLA

### Resumo de alta retenção — riscos de terceiros

- PRECISO SABER: avaliação (pentest, right-to-audit, auditoria interna, cadeia de suprimentos); seleção (due diligence, conflito de interesses); monitoramento, questionários, regras de engajamento; acordos (SLA, MOA, MOU, MSA, WO/SOW, NDA, BPA).
- PRECISO RECONHECER: métricas de serviço→SLA; intenção→MOU; responsabilidades formais→MOA; termos gerais→MSA; trabalho específico→SOW; confidencialidade→NDA; parceria→BPA.
- NÃO CONFUNDIR: MOU (intenção) ≠ MOA (responsabilidades); MSA (geral) ≠ SOW (específico); SLA (métricas) ≠ MSA (termos); NDA (segredo) ≠ BPA (parceria).
- PEGADINHAS: MOU vs MOA; MSA vs SOW; SLA precisa de métricas.
- MEMORIZAÇÃO: SLA=Service Level, MSA=Master (mãe), SOW=o trabalho (filho), NDA=segredo, BPA=parceiros.
- NA PRÁTICA: a gestão de terceiros é risco crítico de cadeia de suprimento (Domínio 2); SLAs e right-to-audit sustentam a conformidade (5.4).

## 5.4 Conformidade eficaz \[OFICIAL\]

Conformidade (compliance) é cumprir leis, regulamentos e normas. A prova cobra as consequências da não conformidade e os conceitos de privacidade.

### Relatório e monitoramento de conformidade

- Relatório de conformidade (compliance reporting): interno (para a própria gestão) e externo (para reguladores/auditores).
- Monitoramento de conformidade (compliance monitoring): devida diligência/cuidado (due diligence/due care), atestado e reconhecimento (attestation and acknowledgement), interno e externo, e automação.

&#91;COMPLEMENTAR\] Due diligence × due care: due diligence é investigar/pesquisar antes de agir; due care é agir com o cuidado razoável e contínuo depois. "Diligência é olhar; cuidado é fazer."

### Consequências da não conformidade

Multas, sanções, danos à reputação, perda de licença e impactos contratuais. A prova pode pedir qual consequência se aplica.

### Privacidade (muito cobrado)

- Implicações legais em níveis local/regional, nacional e global.
- Titular dos dados (data subject): a pessoa a quem os dados pertencem.
- Controlador vs processador (controller vs processor): o controlador decide o propósito/meios; o processador processa por conta do controlador (reforço do 5.1).
- Propriedade (ownership): quem é responsável pelos dados.
- Inventário e retenção de dados (data inventory and retention): saber quais dados se tem e por quanto tempo guardá-los.
- Direito ao esquecimento (right to be forgotten): o titular pode exigir a exclusão de seus dados (ex.: GDPR).

### Representação visual sugerida \[DIDÁTICO\]

Lista das consequências de não conformidade em ordem de gravidade crescente: multas → sanções → impactos contratuais → danos à reputação → perda de licença. (Descrição em texto; conteúdo é uma lista de consequências.)

### Comparação — o que mais confunde

- Due diligence × Due care: diligência é a investigação prévia (pesquisar o fornecedor antes de contratar); cuidado é a ação responsável e contínua (manter os controles depois).
- Titular × Controlador × Processador: o titular é a pessoa dona dos dados; o controlador decide o uso; o processador executa o processamento. Três papéis distintos.
- Conformidade interna × externa: interna é reportar à própria gestão; externa é a reguladores/auditores.
- Direito ao esquecimento × retenção: o esquecimento exige apagar os dados do titular; a retenção obriga a guardar por um prazo. Podem entrar em conflito e exigem política clara.

### Memorização \[DIDÁTICO\]

- Due diligence = investigar (diligência de olhar). Due care = cuidar (agir com cuidado).
- Titular = dono dos dados (a pessoa). Controlador = decide. Processador = processa.
- Direito ao esquecimento = "apague-me".
- Consequências: multa, sanção, contrato, reputação, licença.

### Pegadinhas típicas da prova

1. Trocar due diligence (investigar antes) por due care (cuidar depois).
2. Confundir titular (pessoa) com controlador (quem decide) ou processador (quem processa).
3. Esquecer que a não conformidade pode custar a licença de operar, não só multas.
4. Ignorar o conflito entre direito ao esquecimento e obrigações de retenção.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve um conceito de privacidade/conformidade e pede o termo, ou uma falha e pede a consequência. Raciocínio: pessoa dona dos dados → titular; quem decide o uso → controlador; investigar antes → due diligence; agir com cuidado → due care; exigir exclusão → direito ao esquecimento; perder autorização de operar → perda de licença.

### Mini-desafio 5.4-A

Sob o GDPR, um cliente exige que uma empresa apague todos os seus dados pessoais dos sistemas. Qual direito de privacidade está sendo exercido?

1. Soberania de dados
2. Direito ao esquecimento
3. Retenção de dados
4. Due care

### Mini-desafio 5.4-B

Uma empresa realiza uma investigação detalhada sobre a reputação e os controles de segurança de um fornecedor ANTES de assinar o contrato. Esse processo é melhor descrito como:

1. Due care
2. Due diligence
3. Atestado
4. Direito ao esquecimento

### Resumo de alta retenção — conformidade

- PRECISO SABER: relatório (interno/externo); monitoramento (due diligence/due care, atestado, automação); consequências (multas, sanções, reputação, perda de licença, contratuais); privacidade (titular, controlador vs processador, inventário/retenção, direito ao esquecimento, níveis legais).
- PRECISO RECONHECER: investigar antes→due diligence; cuidar depois→due care; dono dos dados→titular; decide o uso→controlador; apagar dados→direito ao esquecimento.
- NÃO CONFUNDIR: due diligence (antes) ≠ due care (depois); titular ≠ controlador ≠ processador; esquecimento ≠ retenção.
- PEGADINHAS: diligência vs cuidado; papéis de privacidade; perda de licença; esquecimento vs retenção.
- MEMORIZAÇÃO: diligência=investigar, cuidado=agir; titular=pessoa, controlador=decide; "apague-me"=esquecimento.
- NA PRÁTICA: compliance rege políticas e auditorias (5.5); privacidade conecta-se à proteção de dados (Domínio 3) e aos papéis de governança (5.1).

## 5.5 Tipos e finalidades de auditorias e avaliações \[OFICIAL\]

Auditorias e avaliações verificam se os controles funcionam. A prova cobra a distinção interno/externo e, principalmente, os tipos de pentest (conhecimento do ambiente e reconhecimento).

### Atestado, auditoria interna e externa

- Atestado (attestation): declaração formal de que algo é verdadeiro/conforme.
- Interno (internal): conformidade, comitê de auditoria e autoavaliações (self-assessments) feitas pela própria organização.
- Externo (external): regulatório, exames, avaliação e auditoria independente de terceiros.

### Teste de intrusão (penetration testing)

- Tipos por abordagem: físico, ofensivo, defensivo e integrado.
- Conhecimento do ambiente (muito cobrado):
  - Ambiente conhecido (known environment): o testador tem conhecimento completo do alvo (antigo white box).
  - Ambiente parcialmente conhecido (partially known): conhecimento parcial (antigo gray box).
  - Ambiente desconhecido (unknown environment): nenhum conhecimento prévio — simula um atacante externo real (antigo black box).
- Reconhecimento (reconnaissance):
  - Passivo (passive): coletar informações sem interagir diretamente com o alvo (OSINT, registros públicos) — não detectável.
  - Ativo (active): interagir com o alvo (varreduras, port scan) — pode ser detectado.

### Representação visual sugerida \[DIDÁTICO\]

Escala dos ambientes de pentest por nível de conhecimento do testador: conhecido (tudo), parcialmente conhecido (parte), desconhecido (nada) — e ao lado, reconhecimento passivo (não interage/não detectável) vs ativo (interage/detectável). (Renderizado como imagem após esta seção.)

&#91;embedded content: Ambientes de pentest e tipos de reconhecimento\]

### Comparação — o que mais confunde

- Conhecido × Parcialmente conhecido × Desconhecido: conhecido = testador sabe tudo (white box, mais rápido/completo); desconhecido = testador não sabe nada (black box, simula atacante real); parcial = meio-termo (gray box). A prova usa a nomenclatura nova (conhecido/parcial/desconhecido).
- Reconhecimento passivo × ativo: passivo não toca no alvo (OSINT, não detectável); ativo interage (scan, detectável). Passivo = observar de longe; ativo = cutucar.
- Interno × Externo: interno é a própria organização (autoavaliação); externo é terceiro/regulador.
- Auditoria × Avaliação: ambas verificam, mas auditoria tende a ser mais formal/independente; avaliação pode ser mais ampla e interna.

### Memorização \[DIDÁTICO\]

- Conhecido = sabe tudo. Parcial = sabe um pouco. Desconhecido = sabe nada (atacante real).
- Passivo = olha sem tocar (não detectável). Ativo = toca/escaneia (detectável).
- Interno = nós mesmos. Externo = terceiro/regulador.

### Pegadinhas típicas da prova

1. Trocar ambiente conhecido por desconhecido — conhecido é white box (sabe tudo); desconhecido é black box (sabe nada).
2. Confundir reconhecimento passivo (não interage/não detectável) com ativo (interage/detectável).
3. Usar a nomenclatura antiga (white/gray/black box) sem reconhecer os equivalentes novos.
4. Tratar autoavaliação como auditoria externa.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve o nível de informação do testador ou o método de coleta e pede o termo. Raciocínio: testador sabe tudo → conhecido; não sabe nada → desconhecido; meio-termo → parcial; coletar sem tocar no alvo → reconhecimento passivo; escanear/interagir → reconhecimento ativo; verificação por terceiro → auditoria externa.

### Mini-desafio 5.5-A

Uma empresa contrata um pentester e não fornece nenhuma informação sobre a infraestrutura, para simular um atacante externo real que começa do zero. Que tipo de ambiente de teste é esse?

1. Ambiente conhecido
2. Ambiente parcialmente conhecido
3. Ambiente desconhecido
4. Reconhecimento passivo

### Mini-desafio 5.5-B

Durante a fase inicial de um pentest, o testador coleta informações apenas de fontes públicas (redes sociais, registros de domínio, sites) sem enviar nenhum pacote ao alvo. Que tipo de reconhecimento é esse?

1. Reconhecimento ativo
2. Reconhecimento passivo
3. Varredura de portas
4. Auditoria interna

### Resumo de alta retenção — auditorias e avaliações

- PRECISO SABER: atestado; interno (conformidade, comitê, autoavaliação); externo (regulatório, exames, terceiros); pentest (físico, ofensivo, defensivo, integrado); ambiente (conhecido, parcial, desconhecido); reconhecimento (passivo, ativo).
- PRECISO RECONHECER: sabe tudo→conhecido; sabe nada→desconhecido; sem tocar no alvo→passivo; escanear/interagir→ativo; terceiro verifica→externo.
- NÃO CONFUNDIR: conhecido ≠ desconhecido; passivo (não detectável) ≠ ativo (detectável); interno ≠ externo; nomenclatura nova vs antiga (white/gray/black).
- PEGADINHAS: conhecido vs desconhecido; passivo vs ativo; autoavaliação não é auditoria externa.
- MEMORIZAÇÃO: conhecido=sabe tudo, desconhecido=sabe nada; passivo=olha, ativo=toca.
- NA PRÁTICA: pentest valida controles (Domínio 4); reconhecimento passivo usa OSINT (Domínio 2); auditorias sustentam a conformidade (5.4).

## 5.6 Práticas de conscientização de segurança \[OFICIAL\]

O usuário é a última linha de defesa (e o elo mais explorado). A conscientização transforma pessoas em um controle ativo. A prova cobra reconhecer os componentes de um programa de awareness.

### Phishing

- Campanhas (campaigns): simulações de phishing para treinar e medir os usuários.
- Reconhecimento de tentativa de phishing: ensinar a identificar sinais (remetente suspeito, urgência, links estranhos).
- Resposta a mensagens suspeitas relatadas: ter um canal para reportar e tratar.

### Reconhecimento de comportamento anômalo

- Arriscado (risky): comportamento que cria risco conscientemente (ex.: usar app não autorizado).
- Inesperado (unexpected): fora do padrão normal do usuário.
- Não intencional (unintentional): erro sem intenção (ex.: clicar num link por engano).

### Orientação e treinamento do usuário

Temas oficiais: política/manuais, percepção situacional (situational awareness), ameaça interna (insider threat), gerenciamento de senha, mídia e cabos removíveis, engenharia social, segurança operacional (OpSec) e ambientes de trabalho híbridos/remotos.

### Relatórios, monitoramento e ciclo do programa

- Relatórios e monitoramento (reporting and monitoring): inicial (baseline) e recorrente (contínuo) — medir a evolução.
- Desenvolvimento (development) e execução (execution): criar e rodar o programa de conscientização.

### Representação visual sugerida \[DIDÁTICO\]

Ciclo do programa de conscientização: Desenvolvimento → Execução → Monitoramento/Relatórios (inicial e recorrente) → (ajustar e) voltar ao desenvolvimento — melhoria contínua. (Renderizado como imagem após esta seção.)

&#91;embedded content: Ciclo do programa de conscientização de segurança\]

### Comparação — o que mais confunde

- Arriscado × Inesperado × Não intencional: arriscado é consciente (sabe que cria risco); inesperado é fora do padrão; não intencional é por engano (sem intenção). A intenção/consciência separa os três.
- Campanha de phishing × ataque real: a campanha é uma simulação interna de treino; o ataque é real. A prova pode descrever uma simulação autorizada.
- Relatório inicial × recorrente: inicial estabelece a linha de base; recorrente mede a evolução ao longo do tempo.
- Percepção situacional × OpSec: percepção situacional é estar atento ao ambiente/ameaças; OpSec é proteger informações que o adversário poderia explorar.

### Memorização \[DIDÁTICO\]

- Comportamentos: Arriscado = de propósito; Inesperado = fora do padrão; Não intencional = sem querer.
- Programa: Desenvolve → Executa → Monitora/Relata (inicial e recorrente) → repete.
- Awareness = transformar o usuário em sensor de segurança.

### Pegadinhas típicas da prova

1. Confundir comportamento arriscado (consciente) com não intencional (por engano).
2. Tratar relatório inicial (baseline) como recorrente (contínuo).
3. Esquecer que campanhas de phishing são simulações de treino, não ataques.
4. Misturar percepção situacional com OpSec.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve um comportamento do usuário ou uma prática do programa e pede o termo. Raciocínio: cria risco de propósito → arriscado; fora do padrão → inesperado; por engano → não intencional; simulação de e-mail falso para treinar → campanha de phishing; medir a evolução no tempo → relatório recorrente.

### Mini-desafio 5.6-A

Um funcionário, por engano e sem perceber o risco, clica em um link de um e-mail que parecia legítimo. Como esse comportamento é melhor classificado?

1. Arriscado
2. Inesperado
3. Não intencional
4. Insider malicioso

### Mini-desafio 5.6-B

A equipe de segurança envia e-mails falsos de teste aos funcionários para medir quantos clicam e, com base nisso, direcionar treinamento. Qual prática de conscientização é essa?

1. Campanha de phishing (simulação)
2. Due diligence
3. Atestado
4. Pentest de ambiente desconhecido

### Resumo de alta retenção — conscientização

- PRECISO SABER: phishing (campanhas, reconhecimento, resposta a reportes); comportamento anômalo (arriscado, inesperado, não intencional); treinamento (política, percepção situacional, insider, senha, mídia removível, engenharia social, OpSec, híbrido/remoto); relatórios (inicial/recorrente); desenvolvimento/execução.
- PRECISO RECONHECER: cria risco de propósito→arriscado; fora do padrão→inesperado; por engano→não intencional; simulação de e-mail→campanha de phishing; medir evolução→relatório recorrente.
- NÃO CONFUNDIR: arriscado (consciente) ≠ não intencional (engano); inicial (baseline) ≠ recorrente; campanha (treino) ≠ ataque real; percepção situacional ≠ OpSec.
- PEGADINHAS: arriscado vs não intencional; inicial vs recorrente; campanha é simulação.
- MEMORIZAÇÃO: arriscado=de propósito, inesperado=fora do padrão, não intencional=sem querer; programa = desenvolve/executa/monitora.
- NA PRÁTICA: awareness reduz o sucesso de engenharia social (Domínio 2); campanhas e métricas sustentam a melhoria contínua do programa de segurança.

## Revisão do Domínio 5.0

### Revisão 20/80 — os 20% que explicam 80% do domínio

1. Hierarquia de documentos: política (o quê, obrigatória) → padrão (requisito específico) → procedimento (passo a passo); diretriz é recomendação.
2. Papéis de dados: owner decide/classifica, custodian protege; controlador decide o uso, processador processa.
3. Cálculo: SLE = valor × EF; ALE = SLE × ARO.
4. RTO é tempo até voltar; RPO é dados aceitáveis a perder (passado).
5. Estratégias de risco: transferir (seguro), aceitar, evitar, mitigar.
6. Acordos: SLA (métricas), MOU (intenção), MOA (responsabilidades), MSA (termos gerais), SOW (trabalho específico), NDA (segredo), BPA (parceria).
7. Privacidade: titular (pessoa), controlador (decide), processador (processa); direito ao esquecimento.
8. Pentest: conhecido (sabe tudo), desconhecido (sabe nada); reconhecimento passivo (não detectável) vs ativo (detectável).
9. Comportamento: arriscado (de propósito), inesperado (fora do padrão), não intencional (por engano).

### Mapa mental do Domínio 5.0

(Renderizado como imagem após esta seção: o Domínio 5.0 ao centro com os seis objetivos — Governança, Risco, Terceiros, Conformidade, Auditorias, Conscientização.)

&#91;embedded content: Mapa mental do Domínio 5.0\]

### Tabela dos conceitos mais confundidos

| Par confundido | Como diferenciar |
| --- | --- |
| Política × Padrão × Procedimento | O quê (geral) × requisito específico × passo a passo |
| Diretriz × Política | Recomendação × obrigatório |
| Owner × Custodian | Decide/classifica × protege no dia a dia |
| Controlador × Processador | Decide o uso × processa por conta de outro |
| SLE × ALE | Perda de um incidente × perda anual (SLE×ARO) |
| RTO × RPO | Tempo até voltar × dados aceitáveis a perder |
| MTTR × MTBF | Tempo de reparo × tempo entre falhas |
| Apetite × Tolerância | Quanto quer assumir × quanto aguenta |
| Transferir × Mitigar | Passar a terceiro (seguro) × reduzir com controle |
| MOU × MOA | Intenção (não vinculante) × responsabilidades formais |
| MSA × SOW | Termos gerais (mãe) × trabalho específico (filho) |
| NDA × BPA | Confidencialidade × parceria |
| Due diligence × Due care | Investigar antes × cuidar depois |
| Conhecido × Desconhecido | Testador sabe tudo × sabe nada |
| Recon passivo × ativo | Não interage/não detectável × interage/detectável |
| Arriscado × Não intencional | De propósito × por engano |

### Flashcards (pergunta → resposta)

| Pergunta | Resposta |
| --- | --- |
| Documento obrigatório e geral (o quê)? | Política |
| Documento com passo a passo? | Procedimento |
| Recomendação não obrigatória? | Diretriz |
| Quem decide o propósito dos dados? | Controlador |
| Quem processa por conta de outro? | Processador |
| Fórmula do ALE? | SLE × ARO |
| Fórmula do SLE? | Valor do ativo × EF |
| Tempo máximo até restaurar? | RTO |
| Dados máximos aceitáveis a perder? | RPO |
| Contratar seguro é qual estratégia? | Transferir |
| Acordo com métricas de serviço/uptime? | SLA |
| Contrato-mãe de termos gerais? | MSA |
| Acordo de confidencialidade? | NDA |
| Investigação prévia do fornecedor? | Due diligence |
| Direito de exigir exclusão dos dados? | Direito ao esquecimento |
| Pentest sem nenhuma informação prévia? | Ambiente desconhecido |
| Coleta de dados sem tocar no alvo? | Reconhecimento passivo |
| Comportamento de risco feito de propósito? | Arriscado |
| E-mail falso de teste para treinar usuários? | Campanha de phishing |

## Mini-simulado do Domínio 5.0

Doze questões no estilo da prova, cobrindo todo o domínio. As respostas comentadas estão na última seção. Responda antes de conferir.

**Q1.** Um documento interno recomenda, sem obrigar, que os funcionários prefiram frases-senha a senhas curtas. Como esse documento é melhor classificado?

1. Política
2. Padrão
3. Diretriz
4. Procedimento

**Q2.** No contexto de privacidade, qual papel decide o propósito e os meios do processamento dos dados pessoais?

1. Processador
2. Controlador
3. Titular
4. Custodiante

**Q3.** Um ativo vale R$ 50.000. Um incidente causa 40% de perda do valor (fator de exposição) e ocorre uma vez por ano. Qual é a ALE?

1. R$ 10.000
2. R$ 20.000
3. R$ 40.000
4. R$ 50.000

**Q4.** Uma organização determina que pode tolerar no máximo 4 horas para restaurar um serviço após uma falha. Qual métrica da BIA representa isso?

1. RPO
2. RTO
3. MTBF
4. SLE

**Q5.** Uma empresa decide descontinuar completamente um serviço legado que representa risco alto, em vez de tentar protegê-lo. Qual estratégia de risco é essa?

1. Mitigar
2. Transferir
3. Evitar
4. Aceitar

**Q6.** Dois fornecedores assinam um documento que apenas declara a intenção de cooperar, sem criar obrigações legalmente vinculantes detalhadas. Qual acordo é esse?

1. SLA
2. MOU
3. MSA
4. NDA

**Q7.** Qual acordo define os termos gerais e as condições que servirão de base para todos os contratos futuros entre duas empresas?

1. SOW
2. MSA
3. SLA
4. BPA

**Q8.** Antes de contratar um fornecedor, uma empresa investiga minuciosamente sua reputação, finanças e controles de segurança. Esse processo é:

1. Due care
2. Due diligence
3. Atestado
4. Direito ao esquecimento

**Q9.** Um cliente exige que uma empresa exclua permanentemente todos os seus dados pessoais. Qual direito de privacidade está sendo exercido?

1. Soberania de dados
2. Direito ao esquecimento
3. Retenção de dados
4. Portabilidade

**Q10.** Uma empresa contrata um pentester e fornece a ele conhecimento completo da arquitetura, diagramas e credenciais, para um teste aprofundado. Que tipo de ambiente é esse?

1. Ambiente desconhecido
2. Ambiente parcialmente conhecido
3. Ambiente conhecido
4. Reconhecimento ativo

**Q11.** Durante um pentest, o testador apenas consulta redes sociais, registros de domínio e sites públicos, sem enviar qualquer pacote ao alvo. Isso é:

1. Reconhecimento ativo
2. Reconhecimento passivo
3. Varredura de vulnerabilidades
4. Ambiente conhecido

**Q12.** Um funcionário, sabendo que é contra a política, instala um aplicativo não autorizado para facilitar seu trabalho. Como esse comportamento é melhor classificado?

1. Não intencional
2. Inesperado
3. Arriscado
4. Insider malicioso

## Gabarito comentado — Domínio 5.0

### Mini-desafios

**5.1-A — Resposta: 3 (Padrão).** Requisito específico e obrigatório (mínimo de 14 caracteres) = padrão. Política é geral (o quê/por quê); procedimento é passo a passo; diretriz é recomendação.

**5.1-B — Resposta: 2 (Processador de dados).** Quem processa por conta e conforme as instruções da empresa = processador. A empresa é o controlador (decide propósito); o titular é a pessoa dona dos dados; owner é responsabilidade interna.

**5.2-A — Resposta: 2 (R$ 40.000).** SLE = 100.000 × 0,20 = R$ 20.000. ALE = SLE × ARO = 20.000 × 2 = R$ 40.000.

**5.2-B — Resposta: 2 (RPO).** Perda máxima aceitável de dados (1 hora) = RPO. RTO é tempo até restaurar; MTTR é tempo de reparo; MTBF é tempo entre falhas.

**5.2-C — Resposta: 3 (Transferir).** Contratar seguro passa o risco financeiro a um terceiro = transferência. Mitigar reduziria com controle; evitar eliminaria a atividade; aceitar assumiria.

**5.3-A — Resposta: 2 (SLA).** Métricas de serviço (disponibilidade, tempo de resposta) com penalidades = Service Level Agreement. NDA é confidencialidade; MOU é intenção; BPA é parceria.

**5.3-B — Resposta: 2 (MSA).** Termos gerais que regem projetos futuros = Master Service Agreement (contrato-mãe). O SOW detalha cada trabalho específico; MOU é intenção; SLA é métricas.

**5.4-A — Resposta: 2 (Direito ao esquecimento).** Exigir a exclusão dos dados pessoais = right to be forgotten (GDPR). Soberania trata de jurisdição; retenção é guardar; due care é cuidado contínuo.

**5.4-B — Resposta: 2 (Due diligence).** Investigação detalhada ANTES de contratar = due diligence. Due care é o cuidado contínuo depois; atestado é declaração formal; esquecimento é direito de exclusão.

**5.5-A — Resposta: 3 (Ambiente desconhecido).** Sem informação prévia, simulando atacante externo real = unknown environment (black box). Conhecido tem tudo; parcial tem parte; reconhecimento passivo é fase de coleta.

**5.5-B — Resposta: 2 (Reconhecimento passivo).** Coleta só de fontes públicas, sem enviar pacotes ao alvo = passivo (não detectável). Ativo interagiria; varredura de portas é ativo; auditoria interna é outra coisa.

**5.6-A — Resposta: 3 (Não intencional).** Clicar por engano, sem perceber o risco = comportamento não intencional. Arriscado seria consciente; inesperado é fora do padrão; insider malicioso teria intenção de causar dano.

**5.6-B — Resposta: 1 (Campanha de phishing / simulação).** Enviar e-mails falsos de teste para medir e treinar = campanha de phishing simulada. As demais são conceitos de conformidade/auditoria.

### Mini-simulado

| Questão | Resposta | Comentário |
| --- | --- | --- |
| Q1 | 3 | Recomendação não obrigatória = diretriz |
| Q2 | 2 | Decide propósito e meios dos dados = controlador |
| Q3 | 2 | SLE = 50.000 × 0,40 = 20.000; ALE = 20.000 × 1 = R$ 20.000 |
| Q4 | 2 | Tempo máximo para restaurar = RTO |
| Q5 | 3 | Descontinuar a atividade de risco = evitar |
| Q6 | 2 | Declaração de intenção não vinculante = MOU |
| Q7 | 2 | Termos gerais para contratos futuros = MSA |
| Q8 | 2 | Investigação prévia do fornecedor = due diligence |
| Q9 | 2 | Exigir exclusão dos dados = direito ao esquecimento |
| Q10 | 3 | Conhecimento completo do alvo = ambiente conhecido |
| Q11 | 2 | Coleta de fontes públicas sem tocar no alvo = reconhecimento passivo |
| Q12 | 3 | Violar a política de propósito = comportamento arriscado |

### Autodiagnóstico sugerido

| Acertos (de 12) | Classificação | Ação recomendada |
| --- | --- | --- |
| 11–12 | Excelente | Domínio sólido; série completa — parta para simulados gerais |
| 9–10 | Bom | Revisar os pares da tabela de confundidos |
| 6–8 | Atenção | Refazer flashcards e releitura de 5.2 e 5.3 |
| 4–5 | Fraco | Reestudar o domínio com foco em risco e acordos |
| 0–3 | Crítico | Reiniciar o domínio do zero, objetivo por objetivo |

**Subtemas que mais derrubam candidatos neste domínio:** cálculos SLE/ALE (5.2), RTO × RPO (5.2), as siglas de acordo SLA/MOU/MOA/MSA/SOW (5.3) e os papéis controlador × processador (5.1/5.4). Como o domínio é de vocabulário preciso, treine as definições exatas e os cálculos.

### Série completa

Com este guia, os cinco domínios da CompTIA Security+ SY0-701 estão cobertos: 1.0 Conceitos gerais (12%), 2.0 Ameaças (22%), 3.0 Arquitetura (18%), 4.0 Operações (28%) e 5.0 Gerenciamento do programa (20%) — 100% dos objetivos oficiais. Próximos passos sugeridos para quem estuda: alternar entre os cinco mini-simulados, refazer os flashcards de todos os domínios e, por fim, resolver simulados completos cronometrados (90 minutos, até 90 questões) para treinar ritmo e resistência.

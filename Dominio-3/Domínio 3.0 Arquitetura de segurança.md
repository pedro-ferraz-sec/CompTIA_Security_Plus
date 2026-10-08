# Guia Security+ SY0-701 — Domínio 3.0: Arquitetura de segurança

Oct 7, 2026 · @Pedro Henrique Ferraz

Material de estudo para a certificação CompTIA Security+ (SY0-701). O Domínio 3.0 vale 18% da prova e cobre como projetar ambientes seguros: modelos de arquitetura, proteção de infraestrutura e de dados, e resiliência. Todos os gabaritos ficam na última seção.

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

**Caráter do Domínio 3.0:** com 18% do exame, é o domínio de projeto. Aqui você decide onde colocar cada peça, como protegê-la e como manter tudo funcionando após uma falha. As questões costumam pedir a escolha de arquitetura ou controle mais adequado a um requisito (disponibilidade, custo, resiliência, conformidade).

**Estrutura do Domínio 3.0 (peso 18%):** quatro objetivos oficiais — 3.1 Implicações de segurança de modelos de arquitetura; 3.2 Aplicar princípios de segurança à infraestrutura; 3.3 Proteger dados; 3.4 Resiliência e recuperação.

## 3.1 Modelos de arquitetura — parte 1 \[OFICIAL\]

Cada modelo de arquitetura traz implicações de segurança próprias. A prova cobra reconhecer o risco e a característica de cada um.

### Nuvem (Cloud)

- Matriz de responsabilidade (responsibility matrix): define o que o provedor protege e o que o cliente protege. Varia por modelo de serviço — em IaaS o cliente cuida de mais camadas; em SaaS, de menos.
- Considerações híbridas (hybrid considerations): combinar nuvem e on-premises traz desafios de integração e visibilidade.
- Fornecedores terceirizados (third-party vendors): dependência de terceiros amplia o risco de cadeia de suprimento.

&#91;COMPLEMENTAR\] Modelos de serviço: IaaS (infraestrutura), PaaS (plataforma), SaaS (software). Quanto mais "as a service", menos o cliente gerencia — e menos ele controla.

### Infraestrutura como código e computação moderna

- Infraestrutura como código (IaC): provisionar infraestrutura via scripts/templates versionáveis. Benefício: consistência e repetibilidade; risco: um erro no código propaga em escala.
- Sem servidor (serverless): o provedor gerencia a execução; o cliente só fornece o código (ex.: funções). Reduz a superfície de SO, mas depende da segurança do provedor.
- Microsserviços (microservices): aplicação dividida em serviços pequenos e independentes. Mais resiliência e escalabilidade; mais pontos de comunicação a proteger (APIs).

### Infraestrutura de rede

- Isolamento físico (physical isolation): separar fisicamente redes/sistemas.
  - Air-gapped: rede totalmente desconectada de outras (sem conexão física com a internet).
- Segmentação lógica (logical segmentation): dividir a rede logicamente (ex.: VLANs).
- Rede definida por software (SDN): separar o plano de controle do plano de dados, gerenciando a rede por software.

### Outros modelos e ambientes

- Local (on-premises): tudo sob controle da organização; mais controle, mais responsabilidade.
- Centralizado vs descentralizado: gestão em um ponto único vs distribuída.
- Conteinerização (containerization): empacotar app e dependências em containers (ex.: Docker); leve e portável, mas compartilha o kernel do host.
- Virtualização (virtualization): várias VMs sobre um hypervisor; isola melhor que containers, mas é mais pesado.
- IoT (Internet of Things): dispositivos conectados com recursos limitados e, muitas vezes, segurança fraca.
- ICS/SCADA: sistemas de controle industrial / supervisão e aquisição de dados; controlam processos físicos (energia, água, fábricas). Prioridade é disponibilidade e segurança operacional; difíceis de corrigir.
- RTOS (Real-time Operating System): sistema operacional de tempo real; usado onde o tempo de resposta é crítico.
- Sistemas embarcados (embedded systems): computadores dedicados dentro de equipamentos.
- Alta disponibilidade (high availability): arquitetura que minimiza o tempo de inatividade.

### Representação visual sugerida \[DIDÁTICO\]

Diagrama comparando a matriz de responsabilidade por modelo de nuvem: em IaaS o cliente gerencia mais camadas (SO, apps, dados); em PaaS, camadas intermediárias; em SaaS, quase só os dados/acesso. On-prem = tudo com o cliente. (Renderizado como imagem após esta seção.)

&#91;embedded content: Matriz de responsabilidade por modelo de nuvem\]

### Comparação — o que mais confunde

- Conteinerização × Virtualização: containers compartilham o kernel do host (leves, isolamento menor); VMs têm SO próprio sobre o hypervisor (mais pesadas, isolamento maior).
- Isolamento físico (air-gap) × Segmentação lógica (VLAN): air-gap é separação física total; VLAN é separação lógica dentro da mesma infraestrutura.
- IaaS × PaaS × SaaS: quanto mais "as a service", menos o cliente gerencia e menos controla. A matriz de responsabilidade muda conforme o modelo.
- Serverless × Microsserviços: serverless é sobre quem gerencia a execução (o provedor); microsserviços é sobre como a aplicação é dividida.
- ICS/SCADA × TI comum: em ICS/SCADA a prioridade é disponibilidade e segurança física do processo; patches são raros e arriscados.

### Memorização \[DIDÁTICO\]

- IaaS/PaaS/SaaS: quanto mais serviço, menos você gerencia (e menos controla).
- Container = compartilha o kernel (leve); VM = SO próprio (isolado).
- Air-gap = sem fio nenhum ligando à rede externa.
- ICS/SCADA = mundo físico, disponibilidade acima de tudo.

### Pegadinhas típicas da prova

1. Trocar container por VM (compartilha kernel vs SO próprio).
2. Confundir air-gap (físico) com VLAN (lógico).
3. Aplicar práticas de patch de TI comum a ICS/SCADA — nesses ambientes, disponibilidade e cautela vêm primeiro.
4. Esquecer que na matriz de responsabilidade o cliente SEMPRE é responsável pelos próprios dados e controle de acesso, em qualquer modelo.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve um requisito (isolamento máximo, portabilidade leve, menor responsabilidade operacional, controle total) e pede o modelo. Raciocínio: case o requisito com a característica. Isolamento máximo entre cargas → VMs ou air-gap; portabilidade leve → containers; mínima gestão de SO → serverless/SaaS; controle total → on-premises.

### Mini-desafio 3.1-A

Uma empresa precisa executar várias aplicações isoladas de forma leve e portável, compartilhando o mesmo sistema operacional do host para economizar recursos. Qual tecnologia atende melhor?

1. Máquinas virtuais (VMs)
2. Conteinerização
3. Air-gap
4. SCADA

### Mini-desafio 3.1-B

Em um ambiente de nuvem IaaS, de quem é a responsabilidade por aplicar patches no sistema operacional das instâncias e proteger os dados armazenados?

1. Totalmente do provedor de nuvem
2. Do cliente
3. De ninguém, é automático
4. Dividida igualmente e fixa em todos os modelos

### Resumo de alta retenção — modelos de arquitetura

- PRECISO SABER: nuvem (matriz de responsabilidade, híbrido, terceiros), IaC, serverless, microsserviços, isolamento físico/air-gap, segmentação lógica, SDN, on-prem, containers, virtualização, IoT, ICS/SCADA, RTOS, embarcados, alta disponibilidade.
- PRECISO RECONHECER: leve/portável→container; isolamento forte→VM; separação total→air-gap; processo físico→ICS/SCADA; menos gestão→serverless/SaaS.
- NÃO CONFUNDIR: container (kernel compartilhado) ≠ VM (SO próprio); air-gap (físico) ≠ VLAN (lógico); IaaS/PaaS/SaaS (grau de responsabilidade).
- PEGADINHAS: container vs VM; air-gap vs VLAN; patch em ICS/SCADA; dados/acesso são sempre do cliente.
- MEMORIZAÇÃO: mais serviço = menos gestão; container compartilha kernel; ICS/SCADA = disponibilidade.
- NA PRÁTICA: arquitetura de nuvem exige entender a matriz de responsabilidade; ICS/SCADA pede segmentação rígida e monitoramento (OT security).

## 3.1 Modelos de arquitetura — parte 2: considerações \[OFICIAL\]

Ao escolher uma arquitetura, pesam-se trade-offs. A prova cobra reconhecer qual consideração está em jogo em um cenário.

### As considerações oficiais

- Disponibilidade (availability): o sistema está acessível quando necessário.
- Resiliência (resilience): capacidade de resistir e se recuperar de falhas.
- Custo (cost): quanto a solução custa para implantar e manter.
- Responsivo (responsiveness): rapidez de resposta do sistema.
- Escalabilidade (scalability): capacidade de crescer conforme a demanda.
- Facilidade de implantação (ease of deployment): quão simples é colocar em produção.
- Transferência de risco (risk transference): passar parte do risco a um terceiro (ex.: seguro, provedor de nuvem).
- Facilidade de recuperação (ease of recovery): quão rápido se restaura após falha.
- Disponibilidade de patches (patch availability): existem correções disponíveis para a solução?
- Impossibilidade de fazer patch (inability to patch): sistemas que não podem ser corrigidos (ex.: muitos ICS, IoT, legados) exigem controles compensatórios.
- Alimentação (power): requisitos de energia.
- Computação (compute): requisitos de processamento.

### Representação visual sugerida \[DIDÁTICO\]

Lista de considerações agrupadas por eixo de decisão: confiabilidade (disponibilidade, resiliência, recuperação), crescimento (escalabilidade, responsivo, computação), operação (custo, implantação, energia) e risco (patch, impossibilidade de patch, transferência de risco). (Descrição em texto; sem diagrama dedicado por ser uma lista de critérios.)

### Comparação — o que mais confunde

- Disponibilidade × Resiliência: disponibilidade é estar acessível agora; resiliência é a capacidade de continuar/recuperar diante de falhas. Resiliência sustenta a disponibilidade.
- Escalabilidade × Responsividade: escalar é crescer para atender mais carga; responsividade é a rapidez de resposta.
- Impossibilidade de patch × Disponibilidade de patch: um sistema pode não ter patch disponível (fornecedor não lançou) ou não poder receber patch (crítico/legado que não pode parar).
- Transferência de risco: não elimina o risco — repassa parte dele a um terceiro (seguro, provedor).

### Memorização \[DIDÁTICO\]

- Disponibilidade = está no ar agora. Resiliência = aguenta o tranco e volta.
- Transferência de risco = passar a bola (seguro, terceiro), não eliminar.
- Inability to patch = "não dá para corrigir" → precisa de controle compensatório.

### Pegadinhas típicas da prova

1. Trocar disponibilidade por resiliência — uma é o estado atual, a outra é a capacidade de aguentar/recuperar.
2. Achar que transferência de risco elimina o risco — só o repassa.
3. Ignorar a impossibilidade de patch em ICS/IoT, que exige compensar com segmentação e monitoramento.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve uma restrição ou objetivo (orçamento apertado, crescimento rápido, sistema que não pode parar, falha frequente) e pede a consideração dominante. Raciocínio: identifique o que o cenário prioriza. Crescer sob demanda → escalabilidade; aguentar falhas → resiliência; repassar a um seguro/terceiro → transferência de risco; sistema que não pode ser corrigido → inability to patch (mitigar por compensação).

### Mini-desafio 3.1-C

Uma empresa contrata um seguro cibernético para cobrir perdas financeiras em caso de violação de dados. Qual estratégia/consideração de risco está sendo aplicada?

1. Mitigação
2. Transferência de risco
3. Aceitação de risco
4. Evitar o risco

### Resumo de alta retenção — considerações

- PRECISO SABER: disponibilidade, resiliência, custo, responsividade, escalabilidade, facilidade de implantação/recuperação, transferência de risco, disponibilidade/impossibilidade de patch, energia, computação.
- PRECISO RECONHECER: crescer→escalabilidade; aguentar/recuperar→resiliência; no ar agora→disponibilidade; passar a terceiro→transferência de risco; não dá patch→inability to patch.
- NÃO CONFUNDIR: disponibilidade (estado) ≠ resiliência (capacidade); escalabilidade ≠ responsividade; sem patch disponível ≠ impossível aplicar patch.
- PEGADINHAS: disponibilidade vs resiliência; transferência não elimina risco; patch em sistemas críticos.
- MEMORIZAÇÃO: disponibilidade=no ar; resiliência=aguenta e volta; transferir=passar a bola.
- NA PRÁTICA: arquitetos equilibram esses trade-offs; sistemas que não podem receber patch são isolados e monitorados (OT/ICS).

## 3.2 Proteger a infraestrutura empresarial \[OFICIAL\]

Aqui entram o posicionamento dos dispositivos, as zonas, os modos de falha, os equipamentos de rede, a segurança de portas, os firewalls e os acessos seguros. É um objetivo muito técnico e muito cobrado.

### Considerações sobre infraestrutura

- Posicionamento do dispositivo (device placement): onde colocar cada equipamento (ex.: firewall na borda).
- Zonas de segurança (security zones): dividir a rede por nível de confiança (ex.: DMZ para serviços expostos).
- Superfície de ataque (attack surface): reduzir pontos expostos.
- Conectividade (connectivity): como os sistemas se conectam.
- Modos de falha (failure modes):
  - Abertura com falha (fail-open): se o dispositivo falha, o tráfego passa (prioriza disponibilidade).
  - Fechado com falha (fail-closed): se o dispositivo falha, o tráfego é bloqueado (prioriza segurança).
- Atributo do dispositivo (device attribute):
  - Ativo vs passivo (active vs passive): o ativo age sobre o tráfego; o passivo só observa.
  - Em linha vs tap/monitor (inline vs tap/monitor): inline está no caminho do tráfego; tap/monitor recebe uma cópia.

### Dispositivos de rede

- Jump server (servidor de salto): host intermediário endurecido para acessar sistemas sensíveis.
- Servidor proxy (proxy server): intermedia requisições, pode filtrar e cachear.
- IPS/IDS: IDS detecta (passivo, alerta); IPS previne (ativo, bloqueia). Esta distinção é muito cobrada.
- Balanceador de carga (load balancer): distribui tráfego entre servidores (disponibilidade e escalabilidade).
- Sensores (sensors): coletam dados para monitoramento.

### Segurança de porta

- 802.1X: controle de acesso à rede baseado em porta; autentica o dispositivo antes de liberar a conexão.
- EAP (Extensible Authentication Protocol): framework de autenticação usado com 802.1X.

### Tipos de firewall

- WAF (Web Application Firewall): protege aplicações web (camada 7); bloqueia SQLi, XSS etc.
- UTM (Unified Threat Management): appliance tudo-em-um (firewall, antivírus, IDS/IPS, filtro).
- NGFW (Next-generation Firewall): firewall moderno com inspeção profunda e reconhecimento de aplicação.
- Camada 4 vs Camada 7: camada 4 filtra por porta/protocolo; camada 7 entende a aplicação (mais granular).

### Comunicação e acesso seguro

- VPN (Virtual Private Network): túnel cifrado para acesso remoto seguro.
- Acesso remoto (remote access): conectar-se de fora à rede.
- Túnel (tunnel):
  - TLS (Transport Layer Security): cifra a comunicação (ex.: HTTPS, VPN SSL/TLS).
  - IPsec (Internet Protocol Security): cifra e autentica no nível de IP (VPN site-to-site).
- SD-WAN (Software-defined WAN): WAN gerenciada por software, otimiza rotas entre sites.
- SASE (Secure Access Service Edge): combina rede (SD-WAN) e segurança (Zero Trust, SWG, CASB) entregues na borda, como serviço de nuvem.
- Seleção de controles eficazes (selection of effective controls): escolher o controle certo para cada necessidade.

### Representação visual sugerida \[DIDÁTICO\]

Diagrama de zonas de rede: internet (não confiável) → firewall de borda → DMZ (servidores públicos) → firewall interno → rede interna (confiável), com jump server para acesso administrativo. (Renderizado como imagem após esta seção.)

&#91;embedded content: Zonas de rede · da internet à rede interna\]

### Comparação — o que mais confunde

- IDS × IPS: IDS detecta e alerta (passivo, fora do caminho); IPS detecta e bloqueia (ativo, em linha). A palavra Prevention revela que o IPS age.
- Fail-open × Fail-closed: fail-open prioriza disponibilidade (deixa passar ao falhar); fail-closed prioriza segurança (bloqueia ao falhar).
- WAF × NGFW × UTM: WAF é específico para apps web (camada 7); NGFW é firewall avançado com inspeção profunda; UTM é o pacote tudo-em-um.
- TLS × IPsec: TLS cifra na camada de transporte/aplicação (comum em VPN SSL e HTTPS); IPsec cifra no nível de IP (comum em VPN site-to-site).
- Inline × Tap/monitor: inline está no caminho e pode bloquear; tap/monitor só recebe cópia e observa.
- Proxy × Jump server: proxy intermedia requisições (geralmente de saída/web); jump server é ponto de acesso administrativo endurecido.

### Memorização \[DIDÁTICO\]

- IDS = Detecta (alerta). IPS = Previne (bloqueia). "P de Prevenção = age."
- Fail-OPEN = deixa aberto (disponibilidade). Fail-CLOSED = fecha (segurança).
- WAF = Web. NGFW = next-gen (inspeção profunda). UTM = tudo-em-um.
- TLS = transporte/HTTPS. IPsec = nível de IP/site-to-site.
- SASE = SD-WAN + segurança na nuvem.

### Pegadinhas típicas da prova

1. Trocar IDS por IPS — só o IPS bloqueia (Prevention).
2. Confundir fail-open (disponibilidade) com fail-closed (segurança): ambientes de alta segurança preferem fail-closed; onde disponibilidade é crítica, fail-open.
3. Escolher firewall de camada 4 quando o cenário pede proteção de aplicação web (precisa de WAF/camada 7).
4. Misturar TLS e IPsec; lembrar o nível em que cada um atua.

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve a necessidade (detectar sem bloquear, proteger uma app web, acesso remoto seguro, comportamento ao falhar) e pede o dispositivo/configuração. Raciocínio: detectar e alertar → IDS; detectar e bloquear → IPS; proteger app web → WAF; falhar bloqueando → fail-closed; VPN site-to-site → IPsec; acesso administrativo centralizado → jump server.

### Mini-desafio 3.2-A

A equipe quer um dispositivo que, ao identificar tráfego malicioso, bloqueie ativamente a conexão em tempo real, estando posicionado no caminho do tráfego. Qual dispositivo atende?

1. IDS
2. IPS
3. Proxy
4. Load balancer

### Mini-desafio 3.2-B

Um ambiente bancário exige que, se o firewall falhar, nenhum tráfego seja permitido, priorizando a segurança sobre a disponibilidade. Qual modo de falha deve ser configurado?

1. Fail-open
2. Fail-closed
3. Active-passive
4. Inline

### Mini-desafio 3.2-C

Uma empresa precisa proteger uma aplicação web contra SQL injection e XSS na camada 7. Qual solução é a mais adequada?

1. Firewall de camada 4
2. WAF (Web Application Firewall)
3. Load balancer
4. VPN IPsec

### Resumo de alta retenção — proteger a infraestrutura

- PRECISO SABER: posicionamento, zonas/DMZ, superfície de ataque, modos de falha (fail-open/closed), ativo/passivo, inline/tap; dispositivos (jump server, proxy, IDS/IPS, load balancer, sensores); 802.1X/EAP; firewalls (WAF, UTM, NGFW, camada 4/7); VPN, TLS, IPsec, SD-WAN, SASE.
- PRECISO RECONHECER: detecta/alerta→IDS; detecta/bloqueia→IPS; falha bloqueando→fail-closed; app web→WAF; VPN site-to-site→IPsec; acesso admin→jump server.
- NÃO CONFUNDIR: IDS (passivo) ≠ IPS (ativo); fail-open (disponibilidade) ≠ fail-closed (segurança); TLS (transporte) ≠ IPsec (IP); WAF ≠ NGFW ≠ UTM.
- PEGADINHAS: IDS vs IPS; fail-open vs fail-closed; camada 4 vs 7 para apps web.
- MEMORIZAÇÃO: IPS previne (age); fail-open=disponibilidade; WAF=web; SASE=SD-WAN+segurança na nuvem.
- NA PRÁTICA: o Blue Team posiciona IDS/IPS e WAF conforme o fluxo; SASE e Zero Trust são o padrão moderno de acesso.

## 3.3 Proteger dados \[OFICIAL\]

Proteger dados começa por saber que dado é, como ele é classificado, em que estado ele está e qual método aplicar. A prova cobra casar o estado/tipo do dado com o método de proteção certo.

### Tipos de dados

- Regulados (regulated): sujeitos a leis/normas (ex.: dados de saúde, financeiros).
- Segredo comercial (trade secret): informação competitiva sigilosa.
- Propriedade intelectual (intellectual property): patentes, código, criações.
- Informações legais (legal information): documentos jurídicos.
- Informações financeiras (financial information): dados financeiros.
- Legível/ilegível por humanos (human/non-human readable): texto comum vs dados que exigem máquina para interpretar.

### Classificação de dados

Níveis que determinam o rigor da proteção: Sensível, Confidencial, Público, Restrito, Privado, Crítico. Quanto mais alto o nível, mais rígidos os controles.

### Considerações gerais sobre dados

- Estados de dados (data states):
  - Dados em repouso (at rest): armazenados (disco, BD). Protegidos por criptografia (FDE, cripto de BD).
  - Dados em trânsito (in transit): trafegando pela rede. Protegidos por TLS, IPsec, VPN.
  - Dados em uso (in use): sendo processados na memória. Mais difíceis de proteger (ex.: enclave seguro, criptografia homomórfica).
- Soberania dos dados (data sovereignty): os dados estão sujeitos às leis do país onde residem.
- Geolocalização (geolocation): onde os dados/usuários estão fisicamente.

### Métodos para proteção de dados

- Restrições geográficas (geographic restrictions): limitar acesso por região.
- Criptografia (encryption): proteger confidencialidade.
- Hashing: garantir integridade.
- Mascaramento (masking): ocultar parte do dado.
- Tokenização (tokenization): substituir o dado por um token.
- Ofuscação (obfuscation): tornar o dado menos compreensível.
- Segmentação (segmentation): isolar os dados em zonas.
- Restrições de permissão (permission restrictions): limitar quem acessa.

### Representação visual sugerida \[DIDÁTICO\]

Diagrama dos três estados de dados com o método de proteção correspondente: em repouso → criptografia de disco/BD; em trânsito → TLS/IPsec/VPN; em uso → enclave seguro/processamento protegido. (Renderizado como imagem após esta seção.)

&#91;embedded content: Estados de dados · método de proteção por estado\]

### Comparação — o que mais confunde

- Em repouso × Em trânsito × Em uso: repouso é armazenado (cripto de disco/BD); trânsito é na rede (TLS/IPsec); uso é na memória/processamento (enclave, mais difícil).
- Criptografia × Hashing × Masking × Tokenização: cripto é reversível com chave (confidencialidade); hash é integridade; masking oculta parte; tokenização substitui por token com cofre.
- Soberania × Geolocalização: soberania é a lei que rege os dados conforme o país; geolocalização é onde eles estão.
- Classificação × Tipo de dado: classificação é o nível de sensibilidade (público/restrito); tipo é a natureza (financeiro, PI, regulado).

### Memorização \[DIDÁTICO\]

- Repouso = parado (cripto de disco). Trânsito = na estrada (TLS/IPsec). Uso = na mão (memória/enclave).
- Confidencialidade → criptografia; integridade → hash; esconder parte → masking; substituir → tokenização.
- Soberania = os dados obedecem à lei do país onde moram.

### Pegadinhas típicas da prova

1. Proteger dados em trânsito com criptografia de disco (FDE) — FDE é para repouso; em trânsito use TLS/IPsec.
2. Confundir masking com tokenização ou com criptografia.
3. Esquecer que dados em uso são os mais difíceis de proteger (memória).
4. Trocar soberania (lei) por geolocalização (lugar).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve onde o dado está ou o que precisa proteger e pede o método. Raciocínio: identifique o estado. Armazenado → criptografia de disco/BD; na rede → TLS/IPsec/VPN; na memória → enclave seguro; proteger cartões → tokenização; esconder parte do CPF → masking; garantir que não mudou → hash.

### Mini-desafio 3.3-A

Uma empresa precisa proteger dados de clientes enquanto eles trafegam entre o navegador do usuário e o servidor web. Qual método é o mais adequado?

1. Full-disk encryption
2. TLS
3. Hashing
4. Mascaramento

### Mini-desafio 3.3-B

Uma organização quer que, em um relatório, os números de cartão de crédito apareçam como "\*\*\*\* \*\*\*\* \*\*\*\* 1234", ocultando parte do dado sem substituí-lo por um token em cofre. Qual técnica é essa?

1. Tokenização
2. Mascaramento (masking)
3. Criptografia
4. Segmentação

### Resumo de alta retenção — proteger dados

- PRECISO SABER: tipos (regulado, segredo comercial, PI, legal, financeiro, legível/ilegível); classificação (sensível, confidencial, público, restrito, privado, crítico); estados (repouso, trânsito, uso); soberania e geolocalização; métodos (restrição geográfica, cripto, hash, masking, tokenização, ofuscação, segmentação, permissões).
- PRECISO RECONHECER: armazenado→cripto de disco/BD; na rede→TLS/IPsec; na memória→enclave; esconder parte→masking; substituir→tokenização; integridade→hash.
- NÃO CONFUNDIR: repouso ≠ trânsito ≠ uso; masking ≠ tokenização ≠ criptografia; soberania (lei) ≠ geolocalização (lugar); classificação ≠ tipo.
- PEGADINHAS: FDE para trânsito; masking vs tokenização; dados em uso são os mais difíceis.
- MEMORIZAÇÃO: repouso=parado/cripto, trânsito=estrada/TLS, uso=memória/enclave.
- NA PRÁTICA: DLP, classificação e criptografia por estado são pilares da proteção de dados corporativa; soberania importa em arquiteturas multinacionais e multinuvem.

## 3.4 Resiliência e recuperação \[OFICIAL\]

Resiliência é projetar para aguentar e se recuperar de falhas. A prova cobra reconhecer a estratégia/recurso certo para manter ou restaurar operação.

### Alta disponibilidade

- Balanceamento de carga vs clusterização (load balancing vs clustering): balanceamento distribui tráfego entre servidores; clusterização agrupa servidores para trabalhar como um só, com failover.

### Considerações sobre o site (sites de recuperação)

Muito cobrado. Quanto mais pronto o site, mais caro e mais rápido o retorno:

- Hot site: totalmente equipado e atualizado, pronto para assumir quase imediatamente. Mais caro, recuperação mais rápida.
- Warm site: parcialmente equipado; precisa de alguma configuração/dados antes de operar. Custo e tempo intermediários.
- Cold site: só a estrutura básica (espaço, energia); precisa de muito trabalho para operar. Mais barato, recuperação mais lenta.
- Dispersão geográfica (geographic dispersion): espalhar recursos por regiões para resistir a desastres locais.

### Diversidade e continuidade

- Diversidade de plataformas (platform diversity): usar tecnologias diferentes para que uma única falha não derrube tudo.
- Sistemas multinuvem (multi-cloud systems): distribuir entre provedores de nuvem.
- Continuidade de operações (COOP, continuity of operations): manter funções essenciais durante interrupções.

### Planejamento de capacidade

Pessoal, tecnologia e infraestrutura — dimensionar recursos para a demanda.

### Testes

- Teste de mesa (tabletop exercise): discussão teórica do plano, sem executar.
- Failover: testar a transição para o sistema reserva.
- Simulação (simulation): exercício prático simulando o incidente.
- Processamento paralelo (parallel processing): rodar o sistema de recuperação em paralelo com o de produção para validar.

### Backups

- No local/externo (onsite/offsite): cópias locais e remotas.
- Frequência (frequency): com que regularidade se faz backup.
- Criptografia (encryption): proteger os backups.
- Snapshots: imagem do estado em um ponto no tempo.
- Recuperação (recovery): restaurar a partir do backup.
- Replicação (replication): copiar dados continuamente para outro local.
- Registro no diário (journaling): registrar mudanças para permitir recuperação precisa.

### Alimentação

- Geradores (generators): energia de longa duração em queda prolongada.
- UPS (Uninterruptible Power Supply): energia imediata e temporária (bateria) para transição até o gerador ou desligamento seguro.

### Representação visual sugerida \[DIDÁTICO\]

Comparação dos sites de recuperação em dois eixos: custo (baixo→alto) e velocidade de recuperação (lenta→rápida): cold (barato/lento), warm (meio), hot (caro/rápido). (Renderizado como imagem após esta seção.)

&#91;embedded content: Sites de recuperação · custo vs velocidade\]

### Comparação — o que mais confunde

- Hot × Warm × Cold site: hot = pronto e caro (retorno quase imediato); cold = barato e lento (só a estrutura); warm = meio-termo. Trade-off custo × tempo de recuperação.
- UPS × Gerador: UPS cobre a queda imediata por minutos (bateria); gerador sustenta por horas/dias (combustível). Trabalham juntos.
- Teste de mesa × Simulação × Failover: mesa é só discussão; simulação é prática simulada; failover testa a real transição para o reserva.
- Balanceamento × Clusterização: balancear distribui carga; cluster trabalha como unidade com failover.
- Replicação × Backup: replicação é cópia contínua (quase em tempo real); backup é cópia periódica para restauração.
- Dispersão geográfica × Multinuvem: dispersar por regiões físicas vs distribuir entre provedores de nuvem.

### Memorização \[DIDÁTICO\]

- Sites: Cold=caixa vazia (barato/lento), Warm=mornas (meio), Hot=ligado (caro/rápido).
- UPS = segura o tranco agora (bateria); gerador = aguenta a longa (combustível).
- Mesa = conversa; simulação = ensaio; failover = troca de verdade.

### Pegadinhas típicas da prova

1. Trocar hot por cold site — o hot é o mais caro e rápido; o cold é o mais barato e lento.
2. Confundir UPS (imediato/curto) com gerador (longo).
3. Chamar tabletop de simulação — o tabletop é só discussão teórica.
4. Misturar replicação (contínua) com backup (periódico).

### Como a CompTIA transforma isso em questão + raciocínio

O cenário descreve o requisito (retorno quase imediato, menor custo, energia imediata, validar o plano sem interromper) e pede a solução. Raciocínio: retorno imediato e orçamento alto → hot site; menor custo, tolera lentidão → cold site; energia instantânea por minutos → UPS; energia prolongada → gerador; validar plano sem executar → tabletop.

### Mini-desafio 3.4-A

Uma empresa exige retomar as operações em poucos minutos após um desastre e tem orçamento para isso. Qual tipo de site de recuperação é o mais adequado?

1. Cold site
2. Warm site
3. Hot site
4. Dispersão geográfica

### Mini-desafio 3.4-B

Durante uma queda de energia, qual equipamento fornece energia imediata por alguns minutos, tempo suficiente para o gerador entrar em operação ou para um desligamento seguro?

1. Gerador
2. UPS
3. PDU
4. Snapshot

### Mini-desafio 3.4-C

A equipe reúne os responsáveis em uma sala para discutir, passo a passo e apenas teoricamente, como reagiriam a um ataque de ransomware, sem executar nenhum sistema. Que tipo de teste é esse?

1. Failover
2. Simulação
3. Teste de mesa (tabletop)
4. Processamento paralelo

### Resumo de alta retenção — resiliência e recuperação

- PRECISO SABER: alta disponibilidade (balanceamento vs cluster); sites hot/warm/cold; dispersão geográfica; diversidade de plataformas; multinuvem; COOP; capacidade; testes (mesa, failover, simulação, paralelo); backups (onsite/offsite, frequência, cripto, snapshots, replicação, journaling); energia (UPS, geradores).
- PRECISO RECONHECER: retorno imediato→hot site; barato/lento→cold site; energia imediata→UPS; energia prolongada→gerador; só discutir→tabletop; cópia contínua→replicação.
- NÃO CONFUNDIR: hot ≠ warm ≠ cold; UPS (curto) ≠ gerador (longo); tabletop (teoria) ≠ simulação (prática); replicação (contínua) ≠ backup (periódico).
- PEGADINHAS: hot vs cold; UPS vs gerador; tabletop vs simulação.
- MEMORIZAÇÃO: cold=caixa vazia, hot=ligado; UPS=agora/bateria, gerador=longa/combustível.
- NA PRÁTICA: resiliência é base de BCP/DRP (Domínio 5); hot sites e replicação atendem RTO/RPO baixos; a escolha equilibra custo × tempo de recuperação.

## Revisão do Domínio 3.0

### Revisão 20/80 — os 20% que explicam 80% do domínio

1. Nuvem: quanto mais "as a service" (IaaS→PaaS→SaaS), menos o cliente gerencia — mas dados e acesso são sempre do cliente.
2. Container compartilha o kernel (leve); VM tem SO próprio (isolamento forte).
3. IDS detecta e alerta (passivo); IPS detecta e bloqueia (ativo).
4. Fail-open prioriza disponibilidade; fail-closed prioriza segurança.
5. Estados de dados: repouso (cripto de disco), trânsito (TLS/IPsec), uso (enclave).
6. Sites: cold (barato/lento), warm (meio), hot (caro/rápido).
7. UPS cobre a queda imediata (bateria); gerador sustenta a longa (combustível).
8. Resiliência é projetar para aguentar e recuperar; sustenta a disponibilidade.

### Mapa mental do Domínio 3.0

(Renderizado como imagem após esta seção: o Domínio 3.0 ao centro com quatro ramos — Modelos de arquitetura, Proteger infraestrutura, Proteger dados e Resiliência/recuperação.)

&#91;embedded content: Mapa mental do Domínio 3.0\]

### Tabela dos conceitos mais confundidos

| Par confundido | Como diferenciar |
| --- | --- |
| Container × VM | Compartilha kernel (leve) × SO próprio (isolado) |
| Air-gap × VLAN | Separação física × separação lógica |
| IaaS × PaaS × SaaS | Mais responsabilidade × menos responsabilidade |
| IDS × IPS | Detecta/alerta (passivo) × bloqueia (ativo) |
| Fail-open × Fail-closed | Disponibilidade × segurança |
| WAF × NGFW × UTM | App web × firewall avançado × tudo-em-um |
| TLS × IPsec | Transporte/HTTPS × nível de IP/site-to-site |
| Dados em repouso × trânsito × uso | Disco × rede × memória |
| Masking × Tokenização × Criptografia | Oculta parte × substitui por token × cifra reversível |
| Soberania × Geolocalização | Lei do país × lugar físico |
| Hot × Warm × Cold site | Pronto/caro × meio × vazio/barato |
| UPS × Gerador | Imediato/bateria × prolongado/combustível |
| Tabletop × Simulação × Failover | Discussão × ensaio prático × troca real |
| Replicação × Backup | Cópia contínua × cópia periódica |
| Disponibilidade × Resiliência | Estado atual × capacidade de aguentar/recuperar |

### Flashcards (pergunta → resposta)

| Pergunta | Resposta |
| --- | --- |
| Tecnologia leve que compartilha o kernel do host? | Conteinerização |
| Rede totalmente desconectada fisicamente? | Air-gap |
| Dispositivo que só detecta e alerta? | IDS |
| Dispositivo que detecta e bloqueia ativamente? | IPS |
| Modo de falha que prioriza segurança? | Fail-closed |
| Firewall específico para apps web (camada 7)? | WAF |
| VPN site-to-site cifra em que nível? | IPsec (nível de IP) |
| Proteção de dados em trânsito? | TLS/IPsec |
| Proteção de dados em repouso? | Criptografia de disco/BD |
| Ocultar parte do dado (\*\*\*\* 1234)? | Mascaramento |
| Lei que rege os dados pelo país? | Soberania de dados |
| Site de retorno quase imediato? | Hot site |
| Site mais barato e lento? | Cold site |
| Energia imediata por minutos (bateria)? | UPS |
| Energia prolongada (combustível)? | Gerador |
| Teste só teórico/discussão? | Tabletop |
| Cópia contínua de dados para outro local? | Replicação |
| Acesso administrativo centralizado e endurecido? | Jump server |

## Mini-simulado do Domínio 3.0

Dez questões no estilo da prova, cobrindo todo o domínio. As respostas comentadas estão na última seção. Responda antes de conferir.

**Q1.** Uma startup quer rodar dezenas de microsserviços isolados de forma leve, compartilhando o mesmo SO do host para economizar recursos. Qual tecnologia é a mais indicada?

1. Máquinas virtuais
2. Conteinerização
3. Air-gap
4. SCADA

**Q2.** Em um ambiente de nuvem SaaS, qual item permanece como responsabilidade do cliente, independentemente do modelo?

1. Patch do sistema operacional dos servidores
2. Manutenção do hardware físico
3. Os dados e o controle de acesso
4. A virtualização

**Q3.** A equipe precisa de um dispositivo que apenas observe uma cópia do tráfego e gere alertas, sem interferir no fluxo. Qual é o mais adequado?

1. IPS inline
2. IDS (tap/monitor)
3. WAF
4. Load balancer

**Q4.** Um data center militar exige que, se o firewall falhar, todo o tráfego seja interrompido para preservar a segurança. Que modo de falha deve ser usado?

1. Fail-open
2. Fail-closed
3. Active-active
4. Tap/monitor

**Q5.** Para estabelecer uma VPN site-to-site cifrada e autenticada no nível de IP entre duas filiais, qual protocolo é o mais apropriado?

1. TLS
2. IPsec
3. HTTP
4. SNMP

**Q6.** Uma empresa precisa proteger informações de clientes enquanto trafegam entre o aplicativo móvel e a API na nuvem. Qual método protege os dados em trânsito?

1. Full-disk encryption
2. TLS
3. Masking
4. Snapshot

**Q7.** Um sistema de pagamento substitui os números de cartão por valores sem significado, mantendo os dados reais em um cofre separado. Qual técnica é essa?

1. Mascaramento
2. Tokenização
3. Hashing
4. Esteganografia

**Q8.** Uma organização com orçamento robusto exige retomar operações em minutos após um desastre. Qual site de recuperação atende a esse RTO baixíssimo?

1. Cold site
2. Warm site
3. Hot site
4. Air-gap

**Q9.** Durante uma queda de energia, qual recurso mantém os sistemas ligados por alguns minutos até o gerador assumir ou o desligamento seguro ocorrer?

1. Gerador
2. UPS
3. PDU
4. Replicação

**Q10.** A equipe reúne os líderes para discutir, apenas verbalmente e passo a passo, a resposta a um cenário de ransomware, sem acionar sistemas. Que tipo de teste é esse?

1. Failover
2. Simulação
3. Processamento paralelo
4. Teste de mesa (tabletop)

## Gabarito comentado — Domínio 3.0

### Mini-desafios

**3.1-A — Resposta: 2 (Conteinerização).** Leve, portável e compartilhando o SO do host = containers. VMs têm SO próprio (mais pesadas); air-gap é isolamento físico; SCADA é controle industrial.

**3.1-B — Resposta: 2 (Do cliente).** Em IaaS o cliente gerencia SO, aplicações e dados; o provedor cuida da infraestrutura física/virtualização. Dados e acesso são sempre do cliente, em qualquer modelo.

**3.1-C — Resposta: 2 (Transferência de risco).** Contratar seguro repassa parte do risco a um terceiro. Mitigação reduz; aceitação assume; evitar elimina a atividade de risco.

**3.2-A — Resposta: 2 (IPS).** Bloqueio ativo em tempo real, no caminho do tráfego, é a função do IPS. IDS só detecta/alerta; proxy intermedia; load balancer distribui carga.

**3.2-B — Resposta: 2 (Fail-closed).** Bloquear todo o tráfego ao falhar prioriza segurança = fail-closed. Fail-open deixaria passar; active-passive e inline são atributos, não modos de falha.

**3.2-C — Resposta: 2 (WAF).** Proteção de aplicação web na camada 7 contra SQLi/XSS é a função do WAF. Firewall de camada 4 não entende a aplicação; load balancer e VPN têm outras funções.

**3.3-A — Resposta: 2 (TLS).** Dados em trânsito (navegador↔servidor) são protegidos por TLS. FDE é para repouso; hashing é integridade; masking oculta exibição.

**3.3-B — Resposta: 2 (Mascaramento).** Ocultar parte do dado na exibição, sem cofre de substituição, é masking. Tokenização substitui por token com cofre; criptografia cifra; segmentação isola.

**3.4-A — Resposta: 3 (Hot site).** Retomada em minutos com orçamento disponível = hot site (pronto e atualizado). Cold é lento/barato; warm é intermediário; dispersão geográfica é estratégia de distribuição.

**3.4-B — Resposta: 2 (UPS).** Energia imediata por minutos (bateria) para transição é o UPS. Gerador cobre a longa duração; PDU distribui energia; snapshot é imagem de dados.

**3.4-C — Resposta: 3 (Teste de mesa / tabletop).** Discussão teórica, passo a passo, sem executar sistemas = tabletop. Failover testa a transição real; simulação é prática simulada; paralelo roda em paralelo à produção.

### Mini-simulado

| Questão | Resposta | Comentário |
| --- | --- | --- |
| Q1 | 2 | Leve, portável, compartilha o SO = conteinerização |
| Q2 | 3 | Dados e controle de acesso são sempre do cliente |
| Q3 | 2 | Observa cópia do tráfego e alerta, sem interferir = IDS (tap/monitor) |
| Q4 | 2 | Interromper tudo ao falhar, priorizando segurança = fail-closed |
| Q5 | 2 | VPN site-to-site no nível de IP = IPsec |
| Q6 | 2 | Dados em trânsito entre app e API = TLS |
| Q7 | 2 | Substituir cartão por valor sem significado com cofre = tokenização |
| Q8 | 3 | RTO em minutos com orçamento = hot site |
| Q9 | 2 | Energia imediata por minutos (bateria) = UPS |
| Q10 | 4 | Discussão teórica sem acionar sistemas = teste de mesa |

### Autodiagnóstico sugerido

| Acertos (de 10) | Classificação | Ação recomendada |
| --- | --- | --- |
| 9–10 | Excelente | Domínio sólido; avançar ao 4.0 |
| 7–8 | Bom | Revisar os pares da tabela de confundidos |
| 5–6 | Atenção | Refazer flashcards e releitura de 3.2 e 3.4 |
| 3–4 | Fraco | Reestudar o domínio com foco em infraestrutura e resiliência |
| 0–2 | Crítico | Reiniciar o domínio do zero, objetivo por objetivo |

**Subtemas que mais derrubam candidatos neste domínio:** IDS × IPS (3.2), fail-open × fail-closed (3.2), estados de dados e seus métodos (3.3) e sites hot/warm/cold (3.4). Priorize esses quatro se errar questões relacionadas.

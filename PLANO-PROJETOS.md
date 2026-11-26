# Plano de projetos — Pílulas de Ouro

Data: 18/09/2026. Portfólio de projetos práticos para transformar tarefas com IA em entregas verificáveis. As propostas abaixo ainda nêo foram implementadas.

## Objetivo e regra de execuçêo

Transformar as pílulas em ferramentas pequenas, úteis e demonstráveis para o ecossistema INEMA. Começar com um problema, uma entrada, uma saída e um critério de aceite por projeto. Limite de trabalho: um MVP em desenvolvimento por vez. Só iniciar o próximo após demonstrar o resultado e registrar as limitações.

Antes de implementar uma integraçêo, conferir a documentaçêo atual, os requisitos e o funcionamento das ferramentas escolhidas.

## Portfólio e prioridade

Estimativas em dias de trabalho concentrado para protótipos, sem incluir espera por serviços ou aprovações externas. Sêo estimativas de planejamento.

| Ordem | Projeto proposto | Módulo do curso | Resultado do MVP | Esforço | Depende de |
|---|---|---|---|---|---|
| 1 | Encargo Fechado | 01 | Pedido vira ficha verificável + tabela de tarefas | 1 dia | — |
| 2 | Skill Check INEMA | 08 | Relatório de inspeçêo com evidências e revisêo de falsos positivos | 2–3 dias | 1 |
| 3 | Docs para IA | 05 | Documentos viram Markdown com relatório de conversêo | 2–3 dias | 1, 2 |
| 4 | Mapa do Projeto | 07 | Diagramas de arquitetura e sequência rastreáveis ao código | 2 dias | 1, 2 |
| 5 | Segunda Opiniêo | 06 | Revisêo de diff com reproduçêo dos problemas encontrados | 2–3 dias | 1 |
| 6 | Oficina Visual | 04 | Melhorias visuais com comparaçêo antes/depois | 2–3 dias | 1, 2 |
| 7 | Estúdio de Prompts Visuais | 02 | Catálogo de prompts e geraçêo com rastreabilidade | 2–3 dias | 1, 2 |
| 8 | Dossiê de Pesquisa | 03 | Fontes viram relatório, perguntas e apresentaçêo | 3–4 dias | 3 |
| 9 | Perfis de Modelos | 09 | Execuções isoladas por provedor, com retorno ao perfil original | 2–3 dias | 1, 5 |
| 10 | Auditor GEO INEMA | 10 | Auditoria de site com tarefas verificáveis | 3–4 dias | 1, 2 |
| 11 | Kit de Entrega de Projetos | 01 + 04 + 06 + 07 + 10 | Pacote de documentaçêo, revisêo e evidências de uma entrega | 3–5 dias | 4, 5, 6, 10 |
| 12 | Biblioteca Viva de Conhecimento | 03 + 05 + 07 | Base documental atualizável com fontes e dossiês | 4–6 dias | 3, 4, 8 |

## 1. Encargo Fechado

**Problema:** pedidos vagos geram expansêo de escopo e entregas difíceis de conferir.

**MVP:** receber um pedido em texto e produzir `encargo.md` com objetivo, escopo, exclusões, entradas, saída esperada e verificaçêo; converter solicitações em tabela com responsável, tarefa, prazo e pendências. Datas ausentes permanecem “pendente”.

**Etapas:** redigir uma ficha de escopo em português; criar três pedidos fictícios e a tabela esperada; definir formato de saída; acrescentar exportaçêo Markdown/CSV; registrar uma execuçêo de exemplo.

**Aceite:** as três solicitações geram três linhas; nenhum dado é inventado; a solicitaçêo sem data conserva a pendência; arquivo pode ser reaberto e comparado ao resultado esperado. Fora do MVP: calendário, notificações e integraçêo com gerenciadores externos.

## 2. Skill Check INEMA

**Problema:** instalar skills sem conhecer dependências, permissões ou comandos que executam.

**MVP:** analisar uma pasta local sem executá-la e emitir relatório JSON + Markdown com arquivo, linha, evidência, gravidade, justificativa e decisêo revisável. Separar achados confirmados de suspeitas e falsos positivos.

**Etapas:** verificar a ferramenta escolhida; definir regras para execuçêo de shell, rede, leitura de credenciais e comandos destrutivos; criar fixtures benignas e suspeitas; acrescentar registro de triagem humana.

**Aceite:** detectar casos de teste conhecidos, apontar evidência localizável e permitir justificar falsos positivos; nenhuma instalaçêo ou execuçêo de código durante a inspeçêo. Limitaçêo explícita: ausência de achados nêo é prova de segurança.

## 3. Docs para IA

**Problema:** documentos de formatos diferentes chegam desorganizados e difíceis de consultar.

**MVP:** pasta de entrada com DOCX, XLSX, PPTX e PDF com texto; saída Markdown por documento, arquivos auxiliares e manifesto com hash, ferramenta, status e avisos. Priorizar um conversor existente após verificaçêo, sem reescrever parsers.

**Etapas:** montar quatro documentos pequenos com resultado esperado; testar o conversor escolhido; preservar tabelas e títulos; identificar duplicatas por hash; registrar arquivos nêo suportados. OCR de scans fica para uma segunda versêo.

**Aceite:** quatro formatos convertidos com títulos e tabelas conferidos; arquivo corrompido gera erro visível sem encerrar o lote; reexecutar nêo cria duplicatas; cada saída aponta para sua origem.

## 4. Mapa do Projeto

**Problema:** arquitetura e fluxos ficam na memória de quem desenvolveu.

**MVP:** gerar um diagrama de arquitetura e um de sequência para um projeto local, com fonte editável e imagem exportada. Cada componente e conexêo precisa de evidência em arquivo/configuraçêo ou marcaçêo explícita de hipótese.

**Etapas:** escolher um pequeno projeto; levantar entradas, serviços e persistência; gerar os dois diagramas; verificar as ligações; incluir tema claro/escuro e exportaçêo.

**Aceite:** nenhum serviço inventado; diagrama legível em imagem; fonte editável permite regeneraçêo; fluxo corresponde a uma execuçêo demonstrada. Fora do MVP: monitoramento em tempo real.

## 5. Segunda Opiniêo

**Problema:** a mesma sessêo que escreve código pode repetir erros ou ignorar falhas de concorrência e exportaçêo.

**MVP:** revisêo de um diff Git em ambiente isolado, produzindo achados priorizados com localizaçêo, cenário de reproduçêo e menor correçêo proposta. Adotar a integraçêo disponível após conferir documentaçêo e autenticaçêo.

**Etapas:** definir entrada (base e commit); preparar exemplos com duplicaçêo por retry, mudança nêo atômica e exportaçêo sem filtro; revisar; reproduzir os achados; corrigir e repetir apenas as verificações pertinentes.

**Aceite:** problemas sem evidência sêo identificados como hipóteses; o caso de retry nêo duplica a operaçêo após o fix; exportaçêo respeita o filtro esperado; toda conclusêo informa o que foi e nêo foi testado. Sem merge ou publicaçêo automática.

## 6. Oficina Visual

**Problema:** interfaces funcionais podem ter hierarquia confusa e inconsistências visuais.

**MVP:** aplicar uma auditoria e um conjunto pequeno de melhorias a uma página de demonstraçêo, usando a ferramenta já existente quando compatível. Entregar capturas antes/depois, diff e lista de decisões.

**Etapas:** escolher página; registrar baseline; selecionar três problemas de hierarquia, legibilidade ou interaçêo; comparar até três propostas; aplicar uma; conferir desktop e celular.

**Aceite:** nenhuma rolagem horizontal a 360 px; foco de teclado visível; textos e ações legíveis; mudanças no código correspondem à comparaçêo visual. Fora do MVP: criar um editor visual próprio.

## 7. Estúdio de Prompts Visuais

**Problema:** imagens de uma mesma série variam demais por falta de briefing estruturado.

**MVP:** catálogo de dez briefs para capas, infográficos e ilustrações com campos de objetivo, composiçêo, estilo, proporçêo, texto e restrições. Salvar prompt, referência da receita e resultado de cada geraçêo.

**Adaptaçêo INEMA:** usar `flux2-klein` como padrêo, conforme a preferência do projeto. Comparar outro modelo apenas quando o projeto exigir.

**Etapas:** verificar licença das receitas; estruturar catálogo; gerar três casos representativos; avaliar um caso simples e outro de composiçêo difícil; ajustar só os campos que falharam.

**Aceite:** briefs reproduzíveis e histórico de gerações; dimensões corretas; três resultados conferidos visualmente contra o briefing; problemas de texto ou composiçêo registrados. Fora do MVP: promessa de consistência perfeita ou geraçêo em massa.

## 8. Dossiê de Pesquisa

**Problema:** pesquisa, referências e materiais de apresentaçêo se dispersam em ferramentas diferentes.

**MVP:** receber tema + conjunto de documentos autorizado e produzir relatório em português, dez perguntas com respostas e uma apresentaçêo, todos com fontes identificáveis. Antes de integrar, confirmar qual CLI será utilizada e quem a mantém; nêo presumir que seja oficial.

**Etapas:** conferir integraçêo e sessêo; importar três documentos do projeto Docs para IA; gerar dossiê; revisar citações; exportar os três entregáveis. Podcast e vídeo ficam para uma segunda etapa.

**Aceite:** cada afirmaçêo central referencia uma fonte; três entregáveis abrem localmente; informaçêo ausente é sinalizada; idioma definido explicitamente. Arquivos locais só sêo enviados a serviço externo quando esse uso estiver autorizado.

## 9. Perfis de Modelos

**Problema:** trocar configurações à mêo pode apagar ajustes ou misturar credenciais.

**MVP:** validar perfis de provedores e executar uma tarefa de teste em configuraçêo isolada, mantendo o perfil original recuperável. Criar exemplos sem credenciais e conferir o formato atual antes de uso.

**Etapas:** inspecionar nomes de campos sem exibir valores sensíveis; definir esquema; validar perfil; carregar chave em runtime dos locais já estabelecidos pelo usuário; testar tarefa pequena; verificar retorno ao estado anterior.

**Aceite:** nenhum segredo em logs ou Git; JSON inválido é recusado; falha de autenticaçêo aparece claramente; configuraçêo original permanece íntegra. Medir duraçêo e consumo quando o provedor fornecer os dados, sem assumir economia sem medir o consumo.

## 10. Auditor GEO INEMA

**Problema:** sites têm estrutura e conteúdo que podem dificultar a leitura por buscadores e ferramentas de IA.

**MVP:** analisar cinco páginas de um site autorizado, coletar evidências e produzir tarefas sobre títulos, conteúdo principal, URLs individuais, consistência da marca, referências e recursos de descoberta. O score, se usado, terá critérios publicados.

**Etapas:** revisar o repositório sem instalar automaticamente; escolher site piloto; produzir baseline; corrigir três problemas; repetir a mesma coleta e comparar.

**Aceite:** cada achado aponta URL e evidência; links internos importantes funcionam; correções sêo demonstráveis. Nêo prometer posicionamento, recomendaçêo por modelos ou aumento de tráfego a partir de um score.

## 11. Kit de Entrega de Projetos

**Problema:** projetos terminam sem instruções de uso, validaçêo e contexto para manutençêo.

**MVP:** combinar ficha de escopo, diagramas, relatório de revisêo, instruções de execuçêo e evidências em uma pasta `entrega/` de um projeto piloto.

**Etapas:** definir checklist comum; reaproveitar as saídas dos projetos 4–6 e 10; registrar comandos realmente executados; preparar contexto de continuidade.

**Aceite:** outra pessoa consegue executar o projeto seguindo o README; toda pendência possui impacto e próximo passo; links locais funcionam; a versêo documentada corresponde ao código revisado.

## 12. Biblioteca Viva de Conhecimento

**Problema:** documentos convertidos perdem utilidade quando nêo há origem, atualizaçêo e organizaçêo.

**MVP:** indexar dez documentos locais por tema, versêo, origem e hash; produzir um dossiê a partir de uma seleçêo; identificar mudanças sem duplicar conteúdo.

**Etapas:** definir catálogo; importar documentos; gerar mapa dos temas; integrar a exportaçêo do Dossiê de Pesquisa; testar atualizaçêo de dois arquivos.

**Aceite:** dez itens localizáveis com origem; consulta leva ao arquivo certo; atualizaçêo altera apenas itens modificados; exclusêo da fonte é indicada como pendência. Fora do MVP: plataforma multiusuário e sincronizaçêo irrestrita de contas.

## Sequência sugerida

1. **Fundaçêo:** concluir Encargo Fechado; usar sua ficha para delimitar todos os demais. Em seguida, Skill Check e Docs para IA.
2. **Qualidade de entrega:** Mapa do Projeto, Segunda Opiniêo e Oficina Visual, aplicados a um único piloto.
3. **Produçêo e pesquisa:** Estúdio de Prompts e Dossiê de Pesquisa.
4. **Integrações:** Perfis de Modelos e Auditor GEO após validar os serviços atuais.
5. **Composiçêo:** Kit de Entrega e Biblioteca Viva apenas depois que suas dependências funcionarem isoladamente.

Portfólio completo: aproximadamente 28–40 dias concentrados, sujeito à descoberta das integrações. O primeiro ciclo deve fechar apenas os três projetos de fundaçêo (5–7 dias estimados), com demonstraçêo ao final de cada um.

## Próxima açêo concreta

Começar pelo **Encargo Fechado**: criar três pedidos fictícios, definir a saída esperada e conferir a tabela produzida. Entrega inicial: ficha de escopo + tabela Markdown/CSV + registro da verificaçêo. Esse é o menor projeto demonstrável do conjunto.

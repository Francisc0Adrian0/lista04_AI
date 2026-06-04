-Relatório - Detecção de Anomalias em Logs de Acesso

-Descrição da Abordagem

Nesta atividade foi utilizado o algoritmo Isolation Forest para identificar acessos potencialmente anômalos em registros de acesso a um sistema.

Inicialmente foi realizada a análise exploratória do conjunto de dados para compreender as variáveis disponíveis. Em seguida, os dados foram normalizados utilizando StandardScaler para reduzir diferenças de escala entre as variáveis.

Após o pré-processamento, o modelo Isolation Forest foi treinado para identificar registros com comportamento diferente do padrão observado na maioria dos acessos.

-Interpretação dos Resultados

O modelo identificou alguns registros como anômalos. Em geral, esses acessos apresentaram características incomuns em relação ao restante do conjunto de dados, como horários de acesso pouco frequentes, duração elevada da sessão, IP diferente do habitual e grande quantidade de páginas acessadas.

Esses registros merecem atenção por representarem comportamentos diferentes do padrão predominante observado nos logs.

-Respostas às Questões

-Quais padrões de acesso foram considerados normais pelo modelo?

O modelo considerou normais os acessos realizados em horários comuns, com duração moderada de sessão, poucas tentativas de login, utilização de IP habitual e quantidade moderada de páginas acessadas.

-Quais características aparecem com maior frequência nos acessos classificados como anômalos?

Entre os acessos classificados como anômalos destacam-se horários incomuns, sessões mais longas, IP diferente do habitual e quantidade elevada de páginas acessadas.

-Todas as anomalias identificadas representam um possível problema de segurança? Justifique.

Não. Uma anomalia indica apenas um comportamento diferente do padrão observado. Em alguns casos, o usuário pode estar realizando uma atividade legítima, mas incomum, sem que isso represente um incidente de segurança.

-Que tipos de falso positivo podem ocorrer nesse cenário?

Podem ocorrer falsos positivos em situações como acesso durante viagens, utilização de uma nova rede de internet, sessões excepcionalmente longas ou atividades que exijam o acesso a muitas páginas em um curto período.

-Como esse tipo de modelo poderia ser usado em um sistema real de monitoramento?

O modelo pode ser utilizado para monitorar continuamente os logs de acesso e gerar alertas quando comportamentos significativamente diferentes do padrão histórico forem detectados, auxiliando equipes de segurança na investigação de possíveis incidentes.

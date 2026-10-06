# **CONTEXTUALIZAÇÃO**

Pra começar falando sobre o assunto, acho necessário destacar a origem e evolução da code review até o atual momento.

Em 1976, na IBM, surgiu a Inspeção de Fagan. Era um processo muito formal, presencial, linha por linha, mas tão lento que 20% do tempo era desperdiçado apenas agendando essas reuniões.

Nos anos 90, as primeiras ferramentas, como o ICICLE da Bellcore, começaram a levar a revisão para a tela do computador. E foi entre os anos 2000 e 2010 que chegamos no modelo de revisão moderna que domina o mercado. Ela é informal, assíncrona, e ocorre em ferramentas que usamos todo dia, como GitHub, GitLab e CodeFlow.

É aqui que nasce a cultura do Pull Request (ou PR). Hoje, o fluxo funciona assim: o desenvolvedor faz uma mudança numa cópia separada (a branch) e abre o PR explicando o que mudou e o porquê. O revisor analisa as diferenças (aquele famoso código verde e vermelho do diff), faz seus comentários e, se estiver tudo certo, aprova e junta ao código oficial.

Porém, essa revisão moderna gerou um gargalo absurdo de tempo. Dados levantados antes da explosão da IA mostram que um desenvolvedor gastava cerca de 6 horas por semana apenas revisando código dos outros. Na Microsoft, a mediana para um PR ser aprovado era de 24 horas, tornando essa a etapa mais lenta de todo o desenvolvimento. Para contornar isso, o Google teve que impor a regra de fazer revisões minúsculas, de apenas 24 linhas por mudança, para conseguir respostas em menos de 4 horas.

É por isso que, de 2024 para cá, o mercado começou a migrar para a "Revisão com IA", onde bots (como o uReview da Uber e o Amazon Q) revisam o PR antes mesmo do humano ler.

Mas já que o Code Review se tornou uma prática diária em quase toda empresa de software, isso nos leva à nossa primeira questão: Por que as equipes revisam o código umas das outras? O motivo que os desenvolvedores declaram para essa prática é o que realmente acontece na prática?

# **POR QUE É FEITA A REVISÃO DE CÓDIGO?**

Se você perguntar para a equipe, o motivo declarado é quase unânime: "nós revisamos para achar bug". Como podemos ver nos dados da pesquisa de Bacchelli & Bird, 44% dos programadores colocam a busca por defeitos como o 1º motivo para revisar um código. E curiosamente, 44% dos gerentes pensam exatamente igual. A expectativa geral é que o revisor seja um "filtro" implacável.

Contudo, os resultados práticos mostram um cenário totalmente diferente: os bugs são achados, sim, mas são poucos e muito simples. Quando os pesquisadores analisaram 570 comentários reais de revisão, a busca por defeitos caiu para um mero segundo plano, representando apenas 14% dos apontamentos. O verdadeiro líder das revisões foi a "Melhoria de código" (como legibilidade e padronização), ocupando 29% do tempo.

E tem um detalhe ainda mais revelador: dentro desses 14% de bugs encontrados, a esmagadora maioria (65 comentários) era sobre lógicas muito simples. Falhas profundas de design (6 comentários) ou de segurança (apenas 5 comentários) quase não foram pegas pela revisão humana.

E isso não é uma exclusividade desse estudo. O artigo complementar da Microsoft corrobora totalmente com isso. Eles constataram que apenas cerca de 15% dos comentários apontavam um possível bug, enquanto 50% ou mais do esforço da revisão era focado apenas em manutenção a longo prazo.

Inclusive, o título do artigo da Microsoft é "Code Reviews Do Not Find Bugs" (Revisões de código não encontram bugs). Nós do grupo consideramos que esse título exagera um pouco, já que os bugs são encontrados sim, mas os dados da Microsoft deixam muito claro que caçar bugs não é, de fato, o foco real que acontece no dia a dia da revisão.

Analisando a afirmação anterior, há de se concordar com o diagnóstico do problema que a Microsoft levanta: **o modelo atual é custoso e ineficiente para encontrar defeitos em código (como bugs)**.

A pesquisa deles revelou dados alarmantes:

    - Um desenvolvedor gasta, em média, 6 horas por semana apenas fazendo revisões.
    - Um Pull Request leva um tempo mediano de 24 horas para ser aprovado, tornando a revisão a etapa mais lenta de toda a integração de código.

Por que demora tanto e acha tão pouco bug estrutural? O próprio artigo da Microsoft responde isso provando que o gargalo é o entendimento humano. Eles notaram que quando um revisor vai analisar um código que não tem familiaridade, apenas 33% dos comentários dele são úteis. Além disso, se a revisão passa de 20 arquivos alterados, a qualidade do feedback simplesmente despenca.

Ou seja, a revisão de código humana exige um esforço cognitivo alto, causa interrupções constantes e é ineficiente para achar falhas complexas se o volume de código for muito grande.

Então, se a revisão de código não serve como a principal barreira contra bugs e custa tão caro para a equipe, quais são as defesas reais que um defeito precisa atravessar antes de chegar em produção?

# **DEFESAS DO CÓDIGO E O PAPEL DA REVISÃO**

Se a revisão de código não é a principal responsável por encontrar bugs, então quais são as barreiras que realmente impedem defeitos de chegar ao usuário?

Na prática, um erro precisa passar por várias camadas de proteção. Primeiro vem o compilador, que detecta erros de sintaxe e tipagem. Depois, ferramentas de análise estática identificam problemas comuns automaticamente. Em seguida ocorre a revisão de código, onde alguém avalia se a mudança faz sentido e segue os padrões do projeto. Por fim, os testes verificam se o sistema está funcionando corretamente.

Segundo Capers Jones, em um estudo com mais de 13 mil projetos, a análise estática remove cerca de 85% dos defeitos detectáveis por esse método, a revisão de código remove aproximadamente 50% e os testes unitários cerca de 40%. Quando utilizadas juntas, essas barreiras podem alcançar taxas próximas de 98% de remoção de defeitos.

Isso mostra que a revisão não é a única nem a principal defesa contra bugs. Ela é apenas uma das camadas de proteção do processo de desenvolvimento.

Outro ponto importante é que revisar todo o código não garante que os erros serão eliminados. Um estudo de McIntosh e colaboradores analisou grandes projetos open source e verificou que aproximadamente 87% dos módulos que apresentaram bugs após o lançamento já haviam passado por revisão completa.

O que realmente fez diferença não foi simplesmente revisar, mas sim discutir o código. Os pesquisadores observaram que mudanças aprovadas rapidamente, sem comentários ou sem troca de ideias entre autor e revisor, apresentavam mais defeitos posteriormente.

Portanto, o principal valor da revisão de código não está apenas em encontrar bugs. Seu papel mais importante é promover discussão técnica, compartilhar conhecimento e ajudar a equipe a compreender melhor o sistema. A revisão funciona como mais uma barreira de qualidade, mas seu diferencial é a colaboração entre os desenvolvedores.

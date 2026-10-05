# **CONTEXTUALIZAÇÃO**

Pra começar falando sobre o assunto, acho necessário destacar a origem e evolução da code review até o atual momento.

Em 1976 na IBM, Michael Fagan formalizou um processo altamente estruturado de revisão de código, baseado em revisões linha a linha feitas em grupos, com reuniões extensas.

Durante anos pesquisadores proveram evidências dos benefícios da inspeção do código, porém a sua adoção é dificultada pela sua forma de abordagem complexa e lenta.

Devido a essa dificuldade, atualmente muitas organizações adotam práticas de code review mais leves, de forma a limitar ineficiências, sendo a principal delas a utilização de ferramentas assíncronas (GitHub, GitLab, CodeFlow e etc).

Essas práticas fazem parte da revisão de código moderna, que pode ser definida como informal, baseada em ferramentas e como prática regular em grandes empresas.

Mas já que o Code Review se tornou uma prática diária em quase toda empresa de software, isso nos leva à nossa primeira questão: Por que as equipes revisam o código umas das outras? O motivo que os desenvolvedores declaram para essa prática é o que realmente acontece na prática?

# **POR QUE É FEITA A REVISÃO DE CÓDIGO?**

Quando perguntados, 44% dos desenvolvedores (e a maioria dos gerentes) nos estudos feitos Bacchelli & Bird dentro da Microsoft afirmam que a motivação primária das revisões de código é encontrar defeitos. A expectativa geral é que o revisor seja um "filtro" final para impedir que bugs cheguem em produção.

Contudo, os resultados práticos mostram um cenário diferente. Nesta mesma pesquisa, é possível ver que, na prática, apenas 14% dos comentários em revisões de código são sobre defeitos, geralmente sendo sobre erros de lógica, dessa forma ficando longe dos 29% dos comentários que mais aparecem, estes sendo sobre melhorias no código, como legibilidade e padronização.

E isso não é uma exclusividade daquele estudo. É exatamente nesse ponto que entra a pesquisa feita dentro da Microsoft, que carrega o título "Code Reviews Do Not Find Bugs" (Revisões de código não encontram bugs).

Apesar do título, que não acreditamos ser verdadeiro, visto que bugs são sim encontrados nessas revisões, como constatado anteriormente, os dados que a Microsoft traz confirmam a mesma quebra de expectativa. Eles constataram que apenas cerca de 15% dos comentários apontam possíveis defeitos. Na verdade, pelo menos 50% do esforço da revisão é focado apenas em manutenção de longo prazo.

Analisando essa afirmação, há de se concordar com o diagnóstico do problema que a Microsoft levanta: **o modelo atual é custoso e ineficiente para encontrar defeitos em código (como bugs)**.

A pesquisa deles revelou dados alarmantes:

    - Um desenvolvedor gasta, em média, 6 horas por semana apenas fazendo revisões.
    - Um Pull Request leva um tempo mediano de 24 horas para ser aprovado, tornando a revisão a etapa mais lenta de toda a integração de código.

Por que demora tanto e acha tão pouco bug estrutural? O próprio artigo da Microsoft responde isso provando que o gargalo é o entendimento humano. Eles notaram que quando um revisor vai analisar um código que não tem familiaridade, apenas 33% dos comentários dele são úteis. Além disso, se a revisão passa de 20 arquivos alterados, a qualidade do feedback simplesmente despenca.

Ou seja, a revisão de código humana exige um esforço cognitivo alto, causa interrupções constantes e é ineficiente para achar falhas complexas se o volume de código for muito grande.

Então, se a revisão de código não serve como a principal barreira contra bugs e custa tão caro para a equipe, quais são as defesas reais que um defeito precisa atravessar antes de chegar em produção?

# **DEFESAS DO CÓDIGO E O PAPEL DA REVISÃO**

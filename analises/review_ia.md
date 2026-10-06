# Revisar código é relevante no contexto atual? Como a IA mudou isso?

Depois de responder as três perguntas norteadoras, chegamos na principal. A IA mexe em praticamente tudo que vimos antes: no volume de código, no limite humano e no papel da revisão.

## Mais código para revisar

O relatório da Faros AI (2025) analisou dados de mais de 10 mil desenvolvedores em 1.255 times. Nos times que mais usavam IA, cada dev concluiu 21% mais tarefas e o número de pull requests aumentou 98%. Só que cada PR ficou 154% maior, o tempo de revisão subiu 91% e os bugs por dev aumentaram 9%.

Ou seja, cada pessoa escreve mais, mas quando se olha para a empresa toda o ganho some, porque o gargalo saiu da escrita e foi para a revisão. E isso bate direto no limite de 200 a 400 linhas que vimos antes.

O relatório DORA (2024) vai no mesmo sentido: para cada 25% a mais de adoção de IA, a estabilidade das entregas caiu 7,2%. A explicação que eles dão é que a IA facilita fazer mudanças maiores, e mudanças maiores são mais difíceis de revisar.

Importante lembrar que a Faros é uma empresa e os dados mostram correlação, não causa.

## O código chega com mais problemas

A CodeRabbit (2025) comparou 470 pull requests de projetos open source, 320 feitos com IA e 150 só por pessoas. Os PRs com IA tinham em média 10,83 problemas contra 6,45 dos humanos, cerca de 1,7 vez mais. O que mais aumentou foram erros de lógica e de legibilidade, que são justamente os que precisam de alguém entendendo o código para achar. A CodeRabbit também vende revisão com IA, então esse dado tem que ser lido com esse cuidado.

## A IA também revisando

A resposta das empresas foi colocar IA para revisar também. A Uber criou o uReview (2025), que comenta os PRs antes do revisor humano. Ele passa por umas 65 mil mudanças por semana, 75% dos comentários foram considerados úteis pelos engenheiros e 65% foram corrigidos. A empresa estima uma economia de 1.500 horas por semana. O que achamos mais interessante foi onde ele não funciona bem: ele é bom em bugs visíveis no código e em boas práticas, mas fraco em questões de design do sistema, porque não tem o contexto do projeto.

A AWS tem algo parecido no Amazon Q, que revisa segurança, senhas no código, configuração de infraestrutura e dependências. E num estudo acadêmico de Cihan et al. (2025), 73,8% dos comentários de um bot de revisão foram aceitos, mas o tempo para fechar um PR subiu de 5h52 para 8h20, porque mais comentários também geram mais trabalho.

No fim, a IA faz bem o que o artigo-âncora já dizia em 2013 que devia ser automatizado: a parte mais repetitiva da revisão.

## O risco: o time parar de entender o próprio código

Se a revisão sempre foi o lugar onde o time aprende o sistema, passar tudo para a IA tem um custo. Um experimento da Anthropic (Shen e Tamkin, 2026) colocou 52 desenvolvedores para aprender uma biblioteca nova de Python, metade com assistente de IA e metade sem. Na prova feita logo depois, sem IA, quem aprendeu sozinho acertou em média 67% e quem usou IA acertou 50%. A maior diferença foi em debugging, que é achar e entender um erro, bem o que um revisor faz. Um detalhe é que quem usou a IA para pedir explicações foi bem, o problema foi quem só delegou. E o estudo mediu só o curto prazo.

A Thoughtworks (2026) descreve a revisão com quatro funções: mentoria, consistência, corretude e confiança. Com a IA gerando código mais rápido do que dá para revisar, eles falam em "dívida cognitiva", que é a distância entre o quanto o sistema é complexo e o quanto o time realmente entende dele. A IBM, num texto sobre o assunto, também diz que a IA ajuda, mas que o elemento humano continua sendo o mais importante.

## Nossa resposta

A gente acha que sim, revisar código continua relevante, mas o trabalho de quem revisa muda. Antes o revisor olhava tudo, de formatação a bug simples. Agora a IA pode cuidar dessa parte, e o humano fica com o que ela não faz bem: ver se a mudança faz o que deveria, se encaixa no sistema e qual o risco se der errado. E o ensino, que antes acontecia meio sem querer na revisão, precisa ser feito de forma mais intencional, com quem conhece o código revisando junto com quem está aprendendo e o autor explicando o porquê, inclusive do código que a IA gerou.

Como a IA aumentou a quantidade de código que alguém precisa entender, esse papel ficou mais importante, não menos.

Fontes: FAROS AI, The AI Productivity Paradox Report, 2025. DORA/Google Cloud, Accelerate State of DevOps Report, 2024. CODERABBIT, State of AI vs Human Code Generation Report, 2025. UBER ENGINEERING, uReview, 2025. AWS, Amazon Q Developer. CIHAN, U. et al. Automated Code Review In Practice, ICSE-SEIP 2025. SHEN, J. H.; TAMKIN, A. How AI Impacts Skill Formation, Anthropic, 2026. THOUGHTWORKS, The Future of Software Engineering, 2026. IBM, AI Code Review.
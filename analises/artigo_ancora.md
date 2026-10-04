## **SEÇÃO 1 - INTRODUÇÃO**

- Revisão de código em pares é reconhecida como uma ferramenta importante para redução de defeitos melhora de qualidade de projetos de software.

- 1976: Fagan formalizou um processo altamente estruturado de revisão de código, baseado em revisões linha a linha feitas em grupos, com reuniões extensas.

- Durante anos pesquisadores proveram evidências dos benefícios da inspeção do código, porém a sua adoção é dificultada pela sua forma de abordagem complexa e lenta.

- Muitas organizações atualmente adotam práticas de code review mais leves, de forma a limitar as ineficiências dessas inspeções, uma dessas é a utilização de ferramentas de code review.

- A revisão de código moderna pode ser definida como informal, baseada em ferramentas e como prática regular em grandes empresas.

- Resultados da investigação mostram que a motivação principal do code review é achar defeitos, porém na prática relatos de defeitos são a menor parte dos comentários, o que mais ocupa a revisão são pequenos problemas de lógica de baixo nível. Por outro lado, a revisão proveem muitos benefícios às equipes, como transferência de conhecimento, conscientização e melhora na solução de problemas.

- De acordo com os resultados esperados, desenvolvedores empregam muitos mecanismos para cumprir as necessidades de entendimento, maioria das quais não são atendidas por ferramentas.

## **SEÇÃO 2 - ESTUDOS ANTERIORES**

- Stein et al. conduziu um estudo focando em inspeção de código distribuida e assíncrona, com inclusão de uma ferramenta que permitia a identificação e compartilhamento de falhas ou defeitos no código.

- Laitenburger conduziu um questionário de métodos de inspeção de código, e apresentou a taxonomia das técnicas de inspeção.

- Johnson conduziu uma investigação de revisão de código em desenvolvimento open source e seus efeitos nas escolhas feitas por gerentes de projetos de software.

- Porter et al. reportaram uma revisão de estudos de revisão de código que examinou efeito de fatores como tamanho de equipe, tipo de review, número de sessões e inspeções de código. Também avaliaram custos e benefícios em vários estudos. Estes foram majoritariamente estudos envolvendo reuniões planejadas de discussão de código, sem uso de ferramentas.

- Pesquisas anteriores mostram também por que das revisões atuais serem informais, e algumas vezes assíncronas, sendo a principal causa o tempo requerido pra inspeções formais. Votta descobriu que 20% do intervalo em uma "inspeção tradicional" é desperdiçada por agendamento.

- A ferramenta ICICLE (Intelligent Code Inspection in a C Language Environment) foi desenvolvida após desenvolvedores da Bellcore observarem quanto tempo e trabalho era usado antes e durante uma inspeção formal. Muitas das ferramentas de review atuais são basedas nas ideias dela.

- Rigby teve extenso trabalho examinando prátivas de revisão em desenvolvimento de softwares open source. Por exemplo, em um estudo de práticas no projeto Apache, mineraram arquivos de email e descobriram que as revisões eram, tipicamente, pequenas e frequentes, e que contribuições para a revisão eram frequentemente breves e independentes umas das outras.

- Sutherland e Venolia levantaram a hipótese que a troca de conhecimento durante as revisões pode ser de grande valor para que engenheiros posteriormente tentassem entender ou modificar o código discutido. De acordo com eles, **"as revisões de código são uma oportunidade atraente para capturar a justificativa do projeto"**.

- Em um estudo de hábitos de trabalho, Latoza et al. descobriram que muitos problemas encontrados por desenvolvedores eram relacionados ao entendimento racional por trás das mudanças de código e à obtenção de conhecimento de outros membros do time.

## **SEÇÃO 3 - METODOLOGIA**

- 4 motivos surgiram dentre os entrevistados para a pergunta "O que você espera alcançar ao enviar uma revisão de código?": encontrar defeitos, manter a equipe informada, melhorar a qualidade de código e avaliar o projeto de alto nível.

- Foram executadas diferentes formas de pesquisa, essas sendo: observações e entrevistas com desenvolvedores, classificação de cartas (técnica de ordenação amplamente utilizada em arquitetura da informação para criar modelos mentais e derivar taxonomias a partir de dados de entrada), diagrama de afinidade e pesquisas com desenvolvedores e gerentes. 

## **SEÇÃO 4 - POR QUE PROGRAMADORES FAZEM CODE REVIEW?**


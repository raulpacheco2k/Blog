# Como um tester deve lidar com bugs em produção?

Acredito que a frase que um testador, no seu início de carreira, mais teme é: “quebrou em produção”, de fato não é nada bom! Porem, ao passar do tempo aprendemos a lidar com a frase e, além disso, aprendemos que isso é inevitável, cedo ou tarde irá quebrar em produção, por isso existimos, para minimizar os impactos dos bugs e diminuir os riscos de lançamentos. *Inclusive a inevitabilidade de ocorrer bugs em produção é um dos fundamentos de teste de software, é simplesmente normal.*

#### Mas como devemos reagir esse problema?

Encarre o bug em produção como uma oportunidade. É compreensível que seja difícil pensar desta forma, ainda mais quando você ocupa um cargo de importante na organização, mas não há outra forma de pensar a não ser essa sem deixar o ambiente tóxico. Encarre os bugs que ocorrem em produção como uma oportunidade de fazer melhor! É maravilhoso quando encontramos os bugs no ambiente de sandbox e podemos reportar-lós no backlog e avisar os stakeholders, no entanto, já sabemos que exceções ocorrem.

Quando bugs ocorrem em produção, muitas vezes a peso cai nas costas dos testadores, mas devemos lembrar que a responsabilidade da qualidade do produto não é de responsabilidade inteira dos testadores e sim do time em sua totalidade; antes de chegar em produção temos algumas fases, como, por exemplo: levantamento de requisitos, análise de requisitos, prototipação, design da arquitetura, desenvolvimento, testes, e implantação, é completamente injusto, para não falar covarde, que a responsabilidade caia por complemento sobre as costas dos testadores para massagear o ego de alguns.

Quando os envolvidos no fluxo de desenvolvimento apontam o dedo ao testador e diz: é culpa sua. Este tipo de situação, além de deixar o ambiente tóxico, é sem dúvida prejudicial à saúde mental, desanimando e fazendo com que o testador duvide de sua própria capacidade. É simplesmente contraproducente, devemos focar no que deve ser feito para solucionar o problema e evitar que se repita no futuro e não quem é responsável pelo que aconteceu, a final estamos vivenciando a transição do modelo cascata para o modelo ágil, onde um dos pilares é que somos um time e não um indivíduo isolado.

O objetivo de encontrar bugs não é culpar ninguém, mas melhorar a qualidade do produto.

Quando estamos trabalhando em uma empresa com uma cultura que não dê o devido valor aos testes, podemos e devemos jogar com os números ao nosso favor para mostrar que adicionar um fluxo de testes robustos não somente irá diminuir o número de bugs críticos que poderiam ser evitados como também vai diminuir a dor de cabeça e o desenvolvedor não irá precisar

ficar fazendo horas extras para apagar incêndio no final de semana. Nesta etapa podemos criar uma apresentação para a equipe de desenvolvimento mostrando alguns números de como a implementação de teste diminui a quantidade de bugs reportados em produção em empresas do mesmo porte e/ou segmento. Se você já trabalha algum tempo na organização mostre um relatório de quantos bugs já foram reportados e qual seria o impacto desses bugs caso ocorressem em produção.

Uma boa estratégia de teste é fundamental para o sucesso de um produto, além da estratégia é vital que os testadores e desenvolvedores tenham uma boa noção em técnicas de testes de software, obvio que o testador deve ter um conhecimento técnico mais aprofundado que o desenvolvedor, há uma lenda que diz que desenvolvedores não sabem e/ou não devem testar, que os testes devem ficar apenas na mão dos testadores, isso é pura balela, desenvolvedor é, querendo ou não, um prestador de serviço e é fundamental que este prestador de serviço saiba garantir a integridade daquilo que entrega. Obvio que por mais que o desenvolvedor teste, quem deve dar o aval sobre a qualidade de tarefa desenvolvida deve ser um testador.

Por mais que pareça que seja um retrabalho, isso se chama em empatia, além do mais quando o time fica maduro o suficiente e temos testes automatizados validando as entradas possíveis os testadores não precisa alocar a grande parte do seu tempo testando entrada com múltiplos 9 para avaliar se a aplicação vai quebrar por coisa que poderia ter sido prevenida antes que a tarefa chegasse até a fila de teste, quando temos o cenário em que o testador não precise alocar muito tempo em smoke testing, este pode estar implementando testes mais complexos e robustos na aplicação, afim de realmente avaliar como a aplicação se comporta com um cenário desenhado especificamente para quebrar a aplicação.

Alguns testadores, incluindo o meu início como testador, ficam frutados quando seus colegas, ou ele próprio vai testar uma parte do sistema que já havia sido validada anteriormente e acabam achando novos bugs que não surgiram por novas implementações, elas estavam simplesmente mascaradas até então. Achar bugs em uma segunda bateria de teste ou no teste de regressão é melhor que em produção! Penso que nem precisaria falar isso, mas infelizmente isso ocorre e devemos tratar do assunto. Ninguém é perfeito, erros são bem-vindos, desde que aprendemos com eles. Cabeças diferentes, já passaram por situações diferentes por consequência pensam diferente, consequentemente testam diferente e acham bugs diferentes.

Quando identificar um bug nunca fique omisso em relação ao bug afim de querer passar uma falsa ideia do produto está seguro, essa atitude demostra imaturidade, reporte-o e o adicione ao seu conjunto de testes para que não volte a aparecer.

É essencial que quando a aplicação for para produção podemos rastrear as falhas ocorridas antes mesmo dos usuários reportar, para isso temos [ferramentas de monitoramento e rastreamento de erros](https://flatlogic.com/blog/10-best-error-monitoring-and-error-tracking-tools/) que nos auxiliam no processo.

#### Então, resumidamente o que devemos fazer lidar com bugs em produção é:
1. Saber que cedo ou tarde irá ocorrer.
2. Conscientizar o time a respeito da importância dos testes.
3. Caso não haja, implementar a cultura de teste.
4. Mostrar os resultados.
5. Erros são bem-vindos, desde que aprendemos com eles.



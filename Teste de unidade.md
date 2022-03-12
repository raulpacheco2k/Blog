# Teste de unidade
Existem muitas definições para o teste de unidade, mas, dentre todas elas existem tópicos em comum:
1. São testes de baixo nível, focado na menor parte possível do código.
2. Deve ser escrito pelo próprio desenvolvedor.
3. São significantes mais rápidos que outros tipos de testes.

## O que é uma unidade?

As maiores diferenças entre as definições é sobre o que é a menor parte possível (a unidade). Bem, vamos ver as definições e expressões conforme os dicionários.

### Definições:
1. Seção independente que, dentro de uma estrutura maior, compõe o todo. [Dicio, 5.](https://www.dicio.com.br/unidade/#:~:text=Se%C3%A7%C3%A3o%20independente%20que%2C%20dentro%20de%20uma%20estrutura%20maior%2C%20comp%C3%B5e%20o%20todo.)
2. Qualidade do que é uno, unido ou único. [Michaelis, 1.](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=Qualidade%20do%20que%20%C3%A9%20uno%2C%20unido%20ou%20%C3%BAnico.)
3. A qualidade ou estado do que constitui um todo, formado de partes ou elementos separados. [Michaelis, 4](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=A%20qualidade%20ou%20estado%20do%20que%20constitui%20um%20todo%2C%20formado%20de%20partes%20ou%20elementos%20separados)
4. O estado do que está em completa concordância. [Michaelis, 6](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=O%20estado%20do%20que%20est%C3%A1%20em%20completa%20concord%C3%A2ncia)
5. Qualidade do que é só; singularidade. [Michaelis, 9](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=Qualidade%20do%20que%20%C3%A9%20s%C3%B3%3B%20singularidade.)
6. Cada parte componente de uma máquina ou de um mecanismo complexo. [Michaelis, 14](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=Cada%20parte%20componente%20de%20uma%20m%C3%A1quina%20ou%20de%20um%20mecanismo%20complexo.)
7. Qualidade do que não pode ser dividido. [Dictionary Cambridge, 2.](https://dictionary.cambridge.org/pt/dicionario/portugues-ingles/unidade?q=Unidade#:~:text=qualidade%20do%20que%20n%C3%A3o%20pode%20ser%20dividido)

### Expressões:
1. Em programação, rotina básica que pode ser usada para criar rotinas mais complexas. [Michaelis, 2a.](https://michaelis.uol.com.br/busca?r=0&f=0&t=0&palavra=unidade#:~:text=%20em%20programa%C3%A7%C3%A3o%2C%20rotina%20b%C3%A1sica%20que%20pode%20ser%20usada%20para%20criar%20rotinas%20mais%20complexas)

Bem, como vimos, tem algumas definições e fica a cargo do time escolher qual a melhor definição para o contexto da solução. A programação orientada a objetos trata a unidade como uma classe, já em abordagens procedurais ou funcionais consideraram uma única função como uma unidade. 

Porém, é algo que adequamos a necessidade do time de desenvolvimento. Não é algo imutável.

## Testes sociáveis ou solitários?
Em um cenário que você tem uma classe para tratar os fretes do uma loja de varejo e um dos métodos desta classe recebe como parâmetro uma classe de usuário, onde será consultado o endereço, sendo essa outra classe, para realizar o cálculo do frete automaticamente quando um usuário acessa a tela de um produto. Para realizar os testes de unidade na classe de frete, devo também instanciar cliente e endereço? E se tiver um bug nessas outras classes? Meu teste do frete vai falhar!

Em outro cenário em que sua aplicação é responsável única e exclusivamente por realizar o cálculo do frete, sendo que os dados do endereço a ser realizado o cálculo do frete chega até você por uma API que é de responsabilidade de uma empresa terceira, faz sentido ficarmos "reféns" do bom funcionamento de outro software? E se tiver um bug no outro software? Meu teste do frete vai falhar!

Para essa situação temos duas possiveis solução:
1. Utilizar testes solitários, usar dublês de teste. (Estilo mockista) 
2. Utilizar testes sociavéis, não usar dublês de teste. (Estilo clássico)

Talvez no início, no pontapé inicial, das escritas dos testes automatizados deixar 100% desacoplado pode ser desvantajoso, pois, com testes sociais alcançaremos um coverage maior. Então, quando se sentirmos confiantes em relação aos códigos já cobertos, alterando as dependências para mocks. Claro, existe a questão do acoplamento e talvez não seja interessante em determinado contexto módulos diferentes acoplados entre si pelos testes. Tudo isso é algo que deve ser negociado com o time, tendo em vista o seu cenário.

Já no caso de quando dependemos da resposta de um outro software devemos utilizar dublês de testes, para que, caso algo falhe na outra ponta, nossos testes não falhem também.

Por isso digo, novamente, isso são coisas que devem ser definidas com o time considerando os planos de curto a longo prazo. 

### Principais diferenças dos testes sociáveis e solitários

| Sociáveis | Solitários |
| :---: | :---: |
| Cobertura mais ampla. | Cobertura menos ampla. |
| Arquivos de testes longos. | Arquivos de testes enxutos. |
| Acoplado. | Desacoplado. |
| Menor necessidade de mocks. | Maior necessidade de mocks. |
| Todas as classes dependentes também precisam ser instanciadas com suas próprias dependências. | Utiliza apenas os mocks da classe que é dependência para teste. |
| Mais lento para executar e escrever, e consequentemente mais caros. | Mais rápido para executar e escrever, e consequentemente mais baratos. |
|É necessário repetir a mesma configuração do ambiente de teste necessário várias vezes dentro da sua classe de teste. | Você terá muito menos repetição e duplicação nos testes, pois é verificado o comportamento desejado diretamente.|

>  Não achamos difícil rastrear a falha real, mesmo que ela tenha causado falhas nos testes vizinhos. Portanto, sentimos que permitir que nossos testes fossem sociáveis ​​não levou a problemas na prática. [...] Hoje eu conheço e respeito testadores de xunit de ambos os estilos (pessoalmente eu fiquei com o estilo clássico). [...] De fato, alguns testadores xunit classicistas também argumentam que qualquer colaboração com recursos externos, como um banco de dados ou sistema de arquivos, deve usar doubles - Martin Fowler

## Vantagens de testes de unidade antecipado

## Quanto de testes de unidade é o sufiente
## Praticas de cobertura de teste de unidade
## Tamanho dos testes de unidade

## Variáveis em JavaScript.

## O que são variáveis:

Em JavaScript assim como em outras linguagens de programação, variáveis são espécie de caixas na memoria do computador que tem a função de armazenar dados que você pode acessar e modificar ao longo do seu programa.

## Tipos de variáveis em javaScript: 

Quando falamos de tipos de variáveis em JavaScript, nós podemos encontrar três tipos de variáveis ou melhor, três formas de declarar variáveis em JavaScript que são: **const, var e let**.

## Funcionamento do **let e const** na declaração,atribuição e retribuição de variáveis.

**let** e **const** são as formas preferidas de declarar variáveis no JavaScript moderno, mas eles diferem em como lidam com a atribuição e retribuição de valores.

O **let** permite que você declare variáveis que podem ser atualizadas ou retribuídas posteriormente. Imagine o **let** como um recipiente flexível, uma vez que você armazenou um valor nela, pode trocar esse valor conforme necessário ao longo do seu código ou programa. Veja um exemplo usando o **let**:

     let moedas = 100;
     console.log(moedas);
     moedas = 200;
     console.log(moedas);

O **const** é usado para declarar variáveis que são constantes. uma vez que você atribui um valor a uma variável declarada com **const**, você não pode reatribuila, ou seja, você não pode passar um novo valor para a variável. Veja um exemplo usando o **const**:

     const moedas = 300;
     console.log(moedas);
     moedas = 540;
     console.log(moedas);

No exemplo acima, nos tentamos passar um novo valor para a variável moedas que por sua vez ela foi declarada usando **const** e isso gerá um erro, então podemos concluir que as variáveis **const** são imutáveis.

## Porquê não usar var

Imagina que tens uma caixa chamada `nome` dentro de um quarto.

Com `let`, essa caixa só existe dentro do quarto.
Quando sais do quarto, a caixa desaparece.
Isso é o comportamento esperado e seguro.

Com `var`, a caixa vaza para fora do quarto.
Mesmo depois de sair, a caixa ainda existe.
Isso causa confusão porque podes aceder a valores
em lugares do código onde não devias.

Outro problema: com `var` podes criar duas caixas
com o mesmo nome sem receber nenhum erro.
O JavaScript simplesmente sobrescreve a primeira.
Isso causa bugs difíceis de encontrar.

O `var` existe porque o JavaScript é antigo (1995).
O `let` e `const` foram criados em 2015
exatamente para corrigir esses problemas.
Hoje não existe nenhuma razão para usar `var`.

## Regras para nomear variáveis

Existem regras que o JavaScript obriga a seguir.
Se as quebrares, o código dá erro.

**Pode começar com:**
- Uma letra: nome, idade, valor
- Underscore: _nome, _total
- Cifrão: $preco, $valor

**Não pode:**
- Começar com número: 1nome, 2valor — dá erro
- Ter espaços: nome completo — dá erro
- Usar palavras reservadas do JavaScript
  como: if, for, let, const, return, function

**É sensível a maiúsculas:**
nome, Nome e NOME são três variáveis diferentes
O JavaScript trata cada uma como coisa separada
então toma cuidado com isso.

**CamelCase — como funciona:**
Quando o nome tem mais de uma palavra,
a primeira palavra fica toda em minúscula
e cada palavra seguinte começa com maiúscula.
Não se usam espaços nem underscores.

Exemplo no dia a dia:
Se fosses escrever "idade do utilizador" como variável:
- Errado:  idade_do_utilizador  (underscore, evitar em JS)
- Correto: idadeDoUtilizador    (camelCase)

É como se cada nova palavra dentro do nome
recebesse uma letra maiúscula como sinal de início.
Daí o nome camelCase — sobe e desce como
a corcova de um camelo.

---

## Boas práticas

Estas não são obrigatórias mas fazem
uma diferença enorme na qualidade do teu código.

**Usa nomes que descrevem o conteúdo:**
O nome da variável deve dizer exatamente
o que ela guarda. Quando leres o código
daqui a semanas, tens de perceber sem pensar.

- Mau:  let x = 25;
- Bom:  let idadeUtilizador = 25;

- Mau:  let c = "vermelho";
- Bom:  let corFavorita = "vermelho";

**Usa const por padrão:**
Sempre que criares uma variável, começa com const.
Se mais tarde precisares de mudar o valor,
aí sim mudas para let.
Isso evita alterar valores por engano.

**Só usa let quando o valor vai mudar:**
Por exemplo, uma pontuação num jogo vai mudando.
Faz sentido ser let porque o valor não é fixo.
```javascript
let pontuacao = 0;
pontuacao = pontuacao + 10; // faz sentido mudar
```

**Nunca uses var:**
Já vimos porquê. Não existe nenhuma situação
hoje em dia onde var seja a melhor escolha.
Esquece que existe.

**Evita abreviações:**
- Mau:  let usr = "John";
- Bom:  let utilizador = "John";

Poupar duas letras não vale a confusão que causa.

**Uma variável, uma responsabilidade:**
Cada variável deve guardar apenas uma coisa.
Não tentes guardar informação misturada
numa só variável, cria outra.

- Mau:  let dadosUtilizador = "John 20 Portugal";
- Bom:  
  const nomeUtilizador = "John";
  const idadeUtilizador = 20;
  const paisUtilizador = "portugal";
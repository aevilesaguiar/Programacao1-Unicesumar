# Programacao 1 Unicesumar(Java)

## Capitulo 1 - apontamentos

- O Java elimina algumas construções de baixo nível, como ponteiros, além
  de possuir um modelo de memória muito simples, em que cada objeto é alocado em uma 
  pilha e todas as variáveis de tipos de objeto são referências. O seu
  gerenciamento de memória é feito por meio da coleta de lixo (Garbage Collector)
  automática realizada pela JVM.

- A plataforma Java consiste de vários programas. Cada programa fornece uma
  parcela de suas capacidades gerais. Por exemplo, o compilador Java, que 
  converte código-fonte Java em bytecode Java (uma linguagem intermediária para a
  JVM), é fornecido como parte do Java Development Kit (JDK). O Java Runtime
  Environment (JRE) complementa a JVM com um compilador just-in-time (JIT),
  que converte bytecodes intermediários no código de máquina nativo da plataforma alvo. 
  Um extenso conjunto de bibliotecas também forma a plataforma Java.

- Assim, os componentes essenciais da plataforma Java são: o compilador
  Java, as bibliotecas e o ambiente de tempo de execução em que o bytecode Java
  intermediário “executa” de acordo com as regras estabelecidas na especificação
  da máquina virtual.
- O coração da plataforma Java é a máquina virtual, que executa programas
  de bytecode Java. Este código é o mesmo, não importa em que sistema operacional 
  ou hardware o programa está sendo executado. O compilador JIT traduz
  o bytecode Java em instruções do processador nativo em tempo de execução e
  armazena o código nativo em memória durante a execução.

- Embora os programas Java sejam multiplataforma ou independente de plataforma, o 
  código da máquina virtual em que estes programas rodam não é. Cada
  plataforma operacional possui a sua própria JVM

- O CLASSPATH: O Path (caminho em inglês) é uma variável de ambiente de um sistema operacional 
  que fornece a uma aplicação uma lista de pastas onde procurar por algum
  recurso específico

- O exemplo mais comum é o caminho para programas executáveis. A variável de ambiente CLASSPATH de
  Java é uma lista de locais que são visitados na
  procura por arquivos de classes. Tanto o interpretador Java como o compilador
  Java usa a CLASSPATH quando procura por pacotes e classes Java. 

- O INTERPRETADOR JAVA A interpretação de arquivos bytecode Java é a base para a criação de aplicações Java.

- A ASSINATURA DO MÉTODO MAIN( ): O método main( ) deve possuir a assinatura de método correta. A assinatura de
  um método é um conjunto de informações que define o método. Ela inclui o
  nome do método, seus argumentos e o tipo de retorno, assim como o modificador de visibilidade e tipo. O método main( ) deve ser público (public), estático
  (static) e receber um array de objetos Strings (textos, nesse caso sem espaço) e
  não deve retornar valor indicando com a palavra reservada void. Assim: public static void main (String[ ] argumentos)
- O fato de main( ) ser público e estático simplesmente significa que ele é acessível globalmente e que ele pode ser 
  chamado diretamente pelo nome. Quem o chama é o inicializador quando interpretamos o bytecode. 
- O único argumento do método main( ) é um array de objetos Strings, que
  serve para armazenar em cada entrada do array os parâmetros digitados pelo
  usuário após o nome da classe a ser interpretada. O nome do parâmetro pode
  ser escolhido pelo usuário (escolhemos “argumentos” no exemplo acima); mas
  o tipo deve ser sempre String[ ], que significa array de objetos String.

## Questões - capitulo 1

1. Por que o Java divulga tanto que os seus programas são “write once, run
   everywhere”? porque uma vez escritos e compilados em bytecodes, só é necessário uma JVM , ficando
    o programa independente de plataforma

            
3. Quais as principais características do Java 5? O que mudou nos programas já
      existentes até o momento do seu lançamento?
4. O que é JCP? Como você pode fazer para submeter uma mudança que você considera importante para futuras versões de Java?
5. Quais plataformas compõem a tecnologia Java? Forneça uma pequena descrição de cada uma delas.
6. Explique o que é bytecode e como ele deve ser “lido” para permitir que um programa Java seja executado.
7. Explique, com as suas palavras, o processo de compilação, interpretação e execução de programas Java. Dica: faça uma ilustração.
8. Por que o classpath é tão importante para o Java?

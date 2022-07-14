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
![esquemaFuncionamentoJvm](img.png)
a JVM além de ser um interpretador de código,  é também responsável pela execução das pilhas, gerenciamento de memória, 
threads e etc., ou seja, é um “computador virtual”. Uma de suas funções que podemos notar aqui é o Garbage Collector. 
Ele é uma thread responsável pela “limpeza” da memória virtual, ou seja, quando existe muito “lixo” na memória virtual, 
o Garbage Collector entra em ação. Porém, é difícil prever quando isso irá acontecer, por ele ser uma thread, como 
comentado anteriormente, e as threads são lançadas de acordo com o escalonador de processos.
   A JVM não entende código Java, e sim um código especifico chamado ByteCode, que é gerado pelo compilador Java (javac). 
 Esse código é o que será traduzido pela Virtual Machine para o código de cada máquina em questão. Os processos de 
execução de um software Java foram aperfeiçoados ao longo dos tempos, pois no início, a Virtual Machine interpretava
apenas um ByteCode por vez. Hoje em dia, a JVM possui sistemas de compilação JIT (Just - In - Time) misturados com a 
interpretação do código. Essa técnica cria os chamados “Hot-Spots”, que nada mais são que áreas de código executadas 
com maior frequência. Isso ocorre com a análise dos ByteCodes à medida que eles são interpretados pela Virtual Machine.
            
2. Quais as principais características do Java 5? O que mudou nos programas já existentes até o momento do seu lançamento?
   As principais características estão relacionadas à sintaxe da linguagem, com as seguintes melhorias: 
   - for enhanced(loop for aprimorado), 
      for(declaration : expression) {
     // Statements
     }
   - generics :trouxe funcionalidades interessantes para o reuso de código. Agora, podemos criar uma classe só e, a 
   partir dessa classe, instanciar objetos de diferentes tipos, de acordo com a nossa escolha
   
   - autoboxing.
     Com a introdução do autoboxing e unboxing em Java, essa conversão primitiva para objeto acontece automaticamente 
     pelo compilador Java, o que torna o código mais legível.


4. O que é JCP? Como você pode fazer para submeter uma mudança que você considera importante para futuras versões de Java?
   JCP é a Java Community Process. Para submeter uma mudança, uma pessoa deve propor uma JSR (Java Specification Release) e enviar à JCP.

5. Quais plataformas compõem a tecnologia Java? Forneça uma pequena descrição de cada uma delas.
  - Java SE para o desenvolvimento de sistemas desktop e distribuídos; 
  - Java EE para aplicações corporativas Web e de componentes de negócio; 
  - Java ME para o desenvolvimento de aplicações para dispositivos móveis.
  - Java Card. Voltada para dispositivos embarcados com limitações de processamento e armazenamento, como smart cards e o Java Ring.
  - JavaFX. Plataforma para desenvolvimento de aplicações multimídia em desktop/web (JavaFX Script) e dispositivos móveis (JavaFX Mobile).

6. Explique o que é bytecode e como ele deve ser “lido” para permitir que um programa Java seja executado.
   Bytecode é o código gerado pelo compilador Java. Ele é interpretado por meio
   das instruções presentes na máquina virtual Java.

7. Explique, com as suas palavras, o processo de compilação, interpretação e execução de programas Java. Dica: faça uma ilustração.
   Após escrito o código .java, ele é compilado por meio do compilador Java gerando o bytecode .class . O bytecode é 
   então carregado e interpretado pela JVM que executa suas instruções.
   ![esquemaFuncionamentoJvm](img.png)

8. Por que o classpath é tão importante para o Java?
   O classpath indica o local exato onde estão disponíveis todas as classes necessárias para que um programa seja 
   compilado e executado.
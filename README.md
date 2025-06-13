COMPILADORES-T4

Quarto trabalho da disciplina de Compiladores (T4) – Segunda parte do Analisador Semântico para Linguagem LA

Aluno:
Yago David Pimenta • RA: 800273

Professor:
Andre Backes

Descrição do Projeto:
Este repositório contém a extensão do analisador semântico para a linguagem LA, desenvolvida com ANTLR4 e Java. O Trabalho 4 (T4) complementa o T3 e implementa:

Tabela de símbolos com escopos aninhados

Suporte a registros e campos internos (por exemplo, r.cliente.nome)

Verificação de declarações duplicadas (variáveis, constantes, tipos, parâmetros)

Checagem de identificadores não declarados em comandos, expressões e atribuições

Detecção de atribuições incompatíveis entre tipos, incluindo misturas inteiro↔real

Validação do comando RETORNE, permitido somente dentro de funções

Ao final da análise, todas as mensagens de erro são gravadas em um arquivo de saída, seguido de "Fim da compilacao".

Pré-requisitos:

Java 8+ (JDK instalado)

Maven

Bash (Linux, Windows ou Mac)

ANTLR4 Maven Plugin (configurado no pom.xml)

Corretor automático (fornecido pelo professor)

Casos de teste (Google Classroom)

Comandos de Instalação em Debian/Ubuntu:
sudo apt update
sudo apt install openjdk-11-jdk maven

Como Clonar:
git clone https://github.com/Yago-Pimenta/CompiladoresT4.git
cd CompiladoresT4

Compilar e Gerar JAR:
mvn clean generate-sources package

Isso gera:

ANTLR4 em target/generated-sources/antlr4

Classes Java compiladas

JAR com dependências em target/CompiladoresT4-1.0-SNAPSHOT-jar-with-dependencies.jar

Como Executar:
java -jar target/CompiladoresT4-1.0-SNAPSHOT-jar-with-dependencies.jar <entrada.la> <saida.txt>

Onde:
<entrada.la> : arquivo de teste em LA
<saida.txt>  : arquivo de saída com mensagens de erro

Usando o Corretor Automático:

Copie o JAR do corretor para a pasta do projeto
mv compiladores-corretor-automatico-1.0-SNAPSHOT-jar-with-dependencies.jar .

Execute:
java -jar compiladores-corretor-automatico-1.0-SNAPSHOT-jar-with-dependencies.jar "java -jar target/CompiladoresT4-1.0-SNAPSHOT-jar-with-dependencies.jar" gcc temp casos-de-teste "800273" t4

Casos de Teste:
As pastas casos-de-teste/entrada e casos-de-teste/saida contêm as entradas e saídas de referência.

Pontuação Esperada:
O analisador semântico T4 deve detectar corretamente todos os erros e alcançar 9/9 nos testes semânticos.


Yago David Pimenta

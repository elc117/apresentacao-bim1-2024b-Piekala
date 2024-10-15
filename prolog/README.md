
# Ambientes de Execução de Prolog

## Introdução
Online ou local, Compilado ou Interpretado, Ferramentas, uma introdução sobre Prolog!

## Interpretado ou Compilado
Prolog é uma linguagem declarativa que pode ser compilado ou interpretado.

## Diferença entre Interpretador e Compilador
- **Interpretador**: Executa o código linha por linha, ideal para testes e desenvolvimento rápido. 
- **Compilador**: Converte o código para binário ou uma forma intermediária antes da execução, o que geralmente melhora o desempenho.

## Ambientes de Execução de Prolog

### 1. SWI-Prolog
- **Tipo**: Interpretador e compilador
- **Disponibilidade**: Local e online ( SWISH )
- **Descrição**: É uma das implementações mais populares de Prolog. Oferece uma gama completa de funcionalidades, como depuração gráfica, análise estática, além de suporte a diversos pacotes e bibliotecas.
- **Link**: https://www.swi-prolog.org
  
### 2. GNU Prolog
- **Tipo**: Compilador ( com suporte a execução interpretada )
- **Disponibilidade**: Local
- **Descrição**: O GNU Prolog é conhecido por gerar código nativo que pode ser executado diretamente, o que resulta em maior eficiência. Também inclui um sistema de depuração e diagnóstico de código.
- **Link**: http://www.gprolog.org

### 3. Ciao Prolog
- **Tipo**: Compilador e interpretador
- **Disponibilidade**: Local e algumas versões online
- **Descrição**: O Ciao é um ambiente modular que permite alternar entre execução interpretada e compilada. Ele inclui recursos avançados como análise estática, verificação de tipos, e pode ser usado tanto em pesquisa quanto no desenvolvimento industrial.
- **Link**: https://ciao-lang.org

### 4. ECLiPSe Prolog
- **Tipo**: Interpretador
- **Disponibilidade**: Local
- **Descrição**: Focado em problemas de programação em restrições e otimização, o ECLiPSe é utilizado em várias áreas acadêmicas e industriais para resolver problemas complexos.
- **Link**: https://eclipseclp.org

## Plataformas Online
### 1. SWISH
- Versão online do SWI-Prolog, acessível via navegador. Oferece uma experiência interativa para escrever e executar código Prolog sem a necessidade de instalação local.
- Link: https://swish.swi-prolog.org/

### 2. Online Prolog Compiler
- Uma ferramenta online simples para execução de código Prolog. Ideal para testes rápidos ou aprendizado básico.
- Link: https://onecompiler.com/prolog

### 3. JDoodle (Prolog Online)
- Plataforma que permite executar código Prolog diretamente no navegador. É fácil de usar e suporta múltiplas linguagens além de Prolog.
- Link: https://www.jdoodle.com/execute-prolog-online

## Uso
- Prolog tem sido muito utilizada em mercado de Inteligência Arificifial, dado que o mesmo utiliza raciocinio baseado em fatos e regras e possui extensões que permitem lidar com incertezas e estatísticas ( ProbLog )

## Exemplos de prolog

### Familia
% Fatos<br/>
pai(joao, maria).<br/>
pai(joao, jose).<br/>
mae(ana, maria).<br/>
mae(ana, jose).<br/>

% Regras<br/>
irmao(X, Y) :- pai(P, X), pai(P, Y), mae(M, X), mae(M, Y), X \= Y.<br/>
filho(X, P) :- pai(P, X); mae(P, X).<br/>
filha(X, P) :- (pai(P, X); mae(P, X)), sexo(X, feminino).<br/>
sexo(maria, feminino).<br/>
sexo(jose, masculino).<br/>

% Consultas<br/>
% ?- irmao(maria, jose). % verdadeiro<br/>
% ?- filho(jose, joao).  % verdadeiro<br/>
% ?- filha(maria, ana).  % verdadeiro<br/>

### Missionários ( Exemplo Teórico e não funcional [ Pedi um exeplo de ia pro GPT, requer um controle de estados maior ] )

% Definição de estados: (Missionários, Canibais, Lado)<br/>
estado(0, 0, esq).  % Estado final: todos do outro lado.<br/>

% Regras de movimentação.
transporte(3, 3, dir, 2, 0, esq).  % Mover dois missionários.<br/>
transporte(3, 3, dir, 0, 2, esq).  % Mover dois canibais.<br/>




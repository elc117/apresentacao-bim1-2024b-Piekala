
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
- **Disponibilidade**: Local e online (SWISH)
- **Descrição**: É uma das implementações mais populares de Prolog. Oferece uma gama completa de funcionalidades, como depuração gráfica, análise estática, além de suporte a diversos pacotes e bibliotecas.
  
### 2. GNU Prolog
- **Tipo**: Compilador (com suporte a execução interpretada)
- **Disponibilidade**: Local
- **Descrição**: O GNU Prolog é conhecido por gerar código nativo que pode ser executado diretamente, o que resulta em maior eficiência. Também inclui um sistema de depuração e diagnóstico de código.

### 3. SICStus Prolog
- **Tipo**: Compilador e interpretador
- **Disponibilidade**: Local
- **Descrição**: Amplamente utilizado em aplicações comerciais devido à sua robustez e suporte a grandes projetos. Oferece recursos avançados de depuração, análise de desempenho e interface gráfica.

### 4. TuProlog
- **Tipo**: Interpretador e embutível
- **Disponibilidade**: Local
- **Descrição**: Implementado em Java, facilita a integração de Prolog com outras linguagens e sistemas. É usado principalmente em ambientes onde é necessário combinar Prolog com outras tecnologias.

### 5. Ciao Prolog
- **Tipo**: Compilador e interpretador
- **Disponibilidade**: Local e algumas versões online
- **Descrição**: O Ciao é um ambiente modular que permite alternar entre execução interpretada e compilada. Ele inclui recursos avançados como análise estática, verificação de tipos, e pode ser usado tanto em pesquisa quanto no desenvolvimento industrial.

### 6. ECLiPSe Prolog
- **Tipo**: Interpretador
- **Disponibilidade**: Local e remoto (conectado a servidores via cliente)
- **Descrição**: Focado em problemas de programação em restrições e otimização, o ECLiPSe é utilizado em várias áreas acadêmicas e industriais para resolver problemas complexos.

## Plataformas Online
### 1. SWISH
- Versão online do SWI-Prolog, acessível via navegador. Oferece uma experiência interativa para escrever e executar código Prolog sem a necessidade de instalação local.

### 2. Online Prolog Compiler
- Uma ferramenta online simples para execução de código Prolog. Ideal para testes rápidos ou aprendizado básico.

### 3. JDoodle (Prolog Online)
- Plataforma que permite executar código Prolog diretamente no navegador. É fácil de usar e suporta múltiplas linguagens além de Prolog.

<details>

<sumary>Exemplos de prolog</sumary>
% Fatos
pai(joao, maria).
pai(joao, jose).
mae(ana, maria).
mae(ana, jose).

% Regras
irmao(X, Y) :- pai(P, X), pai(P, Y), mae(M, X), mae(M, Y), X \= Y.
filho(X, P) :- pai(P, X); mae(P, X).
filha(X, P) :- (pai(P, X); mae(P, X)), sexo(X, feminino).
sexo(maria, feminino).
sexo(jose, masculino).

% Consultas:
% ?- irmao(maria, jose). % verdadeiro
% ?- filho(jose, joao).  % verdadeiro
% ?- filha(maria, ana).  % verdadeiro

</details>


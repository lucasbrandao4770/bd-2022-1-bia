
## Atividade (data limite: **26/08/2022 23h59min59s**)

Crie o diretório **topico-19** no seu repositório https://github.com/contagithub/bd-2022-1-bia, onde **contagithub** é o nome da conta do aluno no Github. Este é o repositório que você criou no início da disciplina.

Neste diretório você deverá depositar um arquivo JPG, contendo a imagem de um DER conforme solicitado na atividade.<br>
**Atenção às diretrizes abaixo**:
- Use a ferramenta que desejar, desde que a especificação do DER tenha **precisamente** a notação apresentada no [Tópico 15a](./topico-15a.md):
  - Sugestão 1: use a ferramenta [Dia](http://dia-installer.de/), que é uma ferramenta de desenho:
    - para especificar o DER, selecione a *Folha* **ER** (em vez da *Folha* **Banco de Dados**);
  - Sugestão 2: use a ferramenta [ERRCASE](https://sites.google.com/a/cin.ufpe.br/eercase/), que é uma ferramenta de 'modelagem' de banco de dados;
  - Independente da ferramenta utilizada, ao final exporte o desenho para um arquivo JPG.
- Ao 'depositar' o arquivo no diretório, checar se as dimensões da imagem do diagrama estão ajustadas à area de apresentação no GitHub (não deve ser muito pequeno a ponto de tornar-se ilegível, nem grande demais a ponto de ser necessário **rolar** (*to scroll*) para visualizar).
- Faça você mesmo, evite olhar respostas prontas.<br> Novamente, convém citar Cora Coralina para esclarecer o objetivo da atividade: "O que vale na vida não é o ponto de partida e sim a caminhada. Caminhando e semeando, no fim terás o que colher".

### BD Passagens Aéreas ...

A atividade considera os requisitos de dados do **BD Passagens Aéreas**, conforme descrito a seguir.

O _Sistema de Informação de Passagens Aéreas_ visa ao acompanhamento e ao controle dos vôos domésticos e seus passageiros.<br>
O conceito primeiro a ser considerado é o _**voo**_:
- Tipicamente, há um conjunto de voos, cada qual é realizado (executado) periodicamente.
- Um voo é tipicamente composto por uma **sequência** de trechos [de voos]:
  - por exemplo, um voo particular de Brasília para Porto Alegre é composto pela sequência de trechos: Brasília-São Paulo, São Paulo-Belo Horizonte e Belo Horizonte-Porto Alegre;
  - sobre _voos realizados periodicamente_, se o voo for executado diariamente, todos os dias há a realização dos três trechos deste voo.

Sobre as execuções de trecho de voo:
- Cada execução de trecho possui uma **data/hora de partida _prevista_** e uma **data/hora de partida _efetivamente realizada_**:
  - o realizado pode diferir do previsto; por exemplo, quando há atraso na execução do trecho de voo.
- Cada execução de trecho possui uma **data/hora de chegada _prevista_** e uma **data/hora de chegada _efetivamente realizada_**.
- Cada execução de trecho possui **aeroporto de partida _previsto_** e **aeroporto de partida _realizado_**.
- Cada execução de trecho possui **aeroporto de chegada _previsto_** e **aeroporto de chegada _realizado_**.
- Cada execução de trecho ocorre por meio de uma **aeronave**.
- Uma aeronave possui um **mapa de assentos**:
  - o mapa de assentos de uma areonave se refere a todos os assentos ocupáveis por passageiros:
    - cada assento de uma aeronave é identificado pela fileira (por exemplo: 1, 2, 3, etc.) e pela posição na fileira (por exemplo: A, B, C, etc.);
    - cada assento está na **_primeira classe_** ou na **_classe executiva_**;
    - na execução de um trecho de voo, tipicamente há **assentos _ocupados_** e **assentos _não ocupados_**;
  - duas aeronaves distintas podem ter mapas de assentos distintos.

Ao adquirir uma passagem aérea, o passageiro (CPF, Nome, Data de Nascimento, etc.) contrata uma **sequência** de trechos de voos (não necessariamente do mesmo voo), cada trecho com execução (realização) prevista para determinada data/hora:
- Por exemplo, se um passageiro pretende ir de Brasília para Macapá com partida em uma data/hora, pode utilizar:
  - a sequência de trechos Brasília-São Paulo e São Paulo-Belo Horizonte de um voo; e
  - a sequência de trechos Belo Horizonte-Belém e Belém-Macapá de outro voo;
  - obviamente, a primeira sequência deve anteceder a segunda no tempo.
- Em cada trecho de voo, o passageiro ocupará um assento da aeronave pertinente à execução do trecho na data/hora prevista.

Algumas demandas informacionais são:
1. Quais os trechos por voo? Qual a cidade que participa (partida ou chegada) de mais trechos de voo?
2. Quantos são os trechos cujo destino é cidade X?
3. Quais as cidades que são origem de pelo menos um trecho, mas não são destino de qualquer trecho, e vice-versa?
4. Qual o grafo diário, em relação ao mês X, dos trechos com execução prevista?
5. Quais os passageiros que mais repetiram assentos, dentre todos os trechos de voo executados?
6. Qual o mapa de assentos da aeronave X?
7. Quais os voos com menor ocupação de passageiros no período X? Considere a média de ocupação de todos os trechos de cada voo executados no período. Em cada trecho de voo executado, a ocupação é a razão entre o número de assentos ocupados e o número de assentos da aeronave em questão.
8. Quais os passageiros com mais trechos voados no último mês?
9. Quais os destinos mais voados no último mês? Se refere ao destino do último trecho de cada passagem aérea.
10. Quais as passagens de maior realização no último mês? Se refere às passagens que compartilham a origem do primeiro trecho e o destino do último trecho.

Desenhe um DER capaz de atender todas as demandas informacionais acima:<br>
&#9786; É necessário 'desenhar' o DER completo.

## Artefatos

1. Diretório **topico-19**, criado no repositório do estudante, contendo um arquivo com a imagem JPG do DER solicitado.

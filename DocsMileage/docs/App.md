# Sistema de Telemetria
<hr> 



##### **Repositório** : <https://github.com/inspermileage/dashboard-pilot>

<br>

##  Sobre o Aplicativo

<p align="justify">  Nosso aplicativo é responsável por mostrar os dados mais importantes que o carro fornece para o piloto  através de uma comunicação serial com o arduino. Além disso, após recebermos esses dados, é necessário realizar requisições HTTP para poder armazená-los e acessá-los no nosso banco de dados. 
</p>

###### ** Organização de Pastas**


- Components: principais elementos que podem ser utilizados em várias páginas, como dropdown.
- Pages: Dividida em duas partes, a de cadastro gerais da corrida e a com a interface do piloto.
- Themes: contém um arquivo com as cores utilizadas no app.
- Functions: possui funções interessantes para o projeto, junto com a conexão do banco de dados (axios).
- assets: imagens importantes.
- Store: possui um gerenciador de states (Redux).


###### ** O Redux**

<p align="justify">  Nosso app contém um gerenciador de states que funciona como um banco de dados local. Ele nos ajuda a guardar os id's do Car e Track, e Round cadastrados para que possamos realizar um post no banco de dados depois. Para isso, ele é composto de 4 principais arquivos. O primeiro, types.js, é onde podemos cadastrar os reducers, e, como temos que guardar informações de três tabelas diferentes, criamos tês reducers. O segundo arquivo,  actions.js, é onde configuramos as funções responsáveis  por "settar" a variável no reducer. Detalhe: o payload é o que você está passando como argumento, o que você quer que fique guardado, e o dispatch é responsável por efetivamente guardar. Por fim, no arquivo Reducer.js, colocamos todas as informações iniciais e o que os reducers vão conter. Além disso, foi feita uma função para registrar os reducers passando todo o estado inicial, mais os payloads recebidos. </p>


###### ** O Design**

Pensando em armazenar os dados de maneira correta, as primeiras páginas do projeto são destinadas para o cadastro do Carro, Pista, e Round: 

<br>
<div style="text-align:center"> 

<img src="/imgs/Car.png"  width=500/>
</div> 

<br> 
<div style="text-align:center" > 

<img src="/imgs/Track.png"  width=500 />
</div> 

<br> 
<div style="text-align:center"> 

<img src="/imgs/Round.png"  width=500 />
</div> 


<br>

Enfim, temos a interface principal com o piloto: 

<br> 
<div style="text-align:center"> 

<img src="/imgs/NavBar.png"  width=500 />
</div> 

<br> 
<div style="text-align:center"> 

<img src="/imgs/Main.png"   width=500/>
</div> 


## Dependências

Para realizar essa parte do projeto é necessário instalar:

- Yarn
- Node.js
- Chocolatey (Windows)
- Homebrew (Mac)
- JDK 8
- Android Studio

<p align="justify">  Para ter todas as dependências instaladas e configurações corretas, sugerimos seguir o link:  <https://react-native.rocketseat.dev/>, que possui um tutorial para os três tipos de sistemas operacionais (Windows, Mac e Linux).</p>


## Executando

    yarn install
    react-native run-android




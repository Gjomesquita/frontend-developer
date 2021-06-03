![UsuCampeão](logo.png)

Para iniciar o projeto, entre na pasta pokedex.
Questionário respondido no readme dentro de pokedex
# USUCAMPEÃO Tecnologia em Regularização Imobiliária

Somos mais que uma Startup de regularização de imóveis, nascemos para resolver um problema social que atinge mais de 50% da população brasileira.

Através da inovação, execução de qualidade e baixo custo realizamos o sonho da propriedade regularizada.

Nosso propósito é gerar segurança jurídica e #prosperidade a todas as pessoas.

*Venha fazer parte deste time CAMPEÃO!!!*

## Desenvolvedor Front-End

Então, quer dizer que você gosta de desafios e quer se tornar um desenvolvedor front-end na UsuCampeão? Está no lugar certo!

Este teste faz parte do nosso processo de seleção e é a sua chance de nos mostrar todo o seu conhecimento como desenvolvedor front-end com angular. Este teste está dividido em duas etapas:

1. Responder um questionário sobre HTML, CSS, JavaScript e Angular
1. Desenvolver uma aplicação simples, demonstrando seu conhecimento na prática

Daremos um feedback a todos os que fizerem o Pull Request.

O questionário e a especificação da aplicação estão logo abaixo.

A sua entrega será feita através de um Pull Request nesse repositório. Faça um fork do repositório, implemente o seu código, responda as questões no README.md e faça um pull request. Sinta-se a vontade para colocar quaisquer outras informações que você considere pertinente no README.

### Instruções:

1. Faça um fork deste repositório;
1. Responda as questões no README.md - caso prefira, podemos conversar sobre elas na entrevista;
1. Construa uma aplicação conforme solicitado, utilizando HTML, CSS e Angular;
1. Adicione quaisquer informações adicionais para executar sua aplicação no README.md;
1. Após terminar, submeta um pull request e aguarde seu feedback.

**PS:** Utilizamos este mesmo testes para os níveis (**júnior**, **pleno** ou **sênior**), apenas adequando o nível de exigência na avaliação de acordo com o perfil da vaga.

### Questionário

1. O que são ``components`` e ``directives`` e quais as difenças entre eles? Dê alguns exemplos de utilização.
Basicamente, uma Directive (Diretiva) é uma função que é executada pelo Angular ao ser encontrada no HTML, seja para adicionar um style dependendo de alguma condição, para remover/adicionar elementos ao DOM ou até para construir uma interface inteira. Diretivas são criadas adicionando a anotação @Directive a uma classe Typescript. 
Components (Componentes) na verdade são um tipo de Diretiva que contêm templates, ou seja, que têm uma estrutura em html que será construída no DOM. Podemos então dividir as Diretivas em três tipos: 
    Componentes: já explicados. São criados com a anotação @Component e que necessita de um template(html) para funcionar.
    Diretivas de atributo: Servem para manipular a aparência, atributo e valor de elementos, além de guardar variaveis que podem ser acessadas por outra Diretiva. Ex: ngHide, ngClass, ngModel.
    Diretivas Estruturais: Alteram a estrutura do DOM, podendo por exemplo adicionar e remover elementos do DOM. Ex: *ngIf, *ngFor, *ngSwitch

2. O que são ``services``? Dê alguns exemplos de utilização.
Services são classes usadas para armazenar valores, funções e funcionalidades, que podem ser usadas por diversas diretivas. São criadas com a anotação @Injectable e podem ser injetadas nas Diretivas pelo constructor.

3. O que são ``pipes``? Dê alguns exemplos de utilização.
Pipes são funções usadas para transformar um valor antes de mostra-lo no DOM. Por exemplo, o pipe 'uppercase', transforma os caracteres de uma string para maiúsculo, o DatePipe formata a data da maneira que quiser, podendo usar formatos pré-definidos como também estipular o formato diretamente {date:"dd/MM/yyyy"}. 
Para usar pipes, basta adicionar ( | ${pipe}) na expressão de modelo {{valor}}. Ex: {{ dataAtual | Date: "dd/MM/yyyy" }}.

4. O que é ``data-binding`` e quais os tipos que o Angular dá suporte?
O data-binding é uma técnica que sincroniza dados/valores entre dois ou mais lugares. No Angular, usamos data-binding constantemente para sincronizar um valor entre o template e o component. 
No Angular podemos usar esses tipos, que diferem no fluxo da sincronização:
Interpolation ou Interpolação (Component -> Template): caso o valor seja atualizado por alguma função, ele é atualizado no template. Há duas maneiras de usa-lo, dependendo do caso, para mostrar o valor é usado {{}}, caso para um atributo é usado []. Ex: [disabled]="${valor}" ou <div>{{ ${valor} }}</div>
Event ou Evento (Template -> Component): Para atualizações feitas no template que são passadas ao component. Ex: (click), (select), (keydown.enter).
Two-way ou Duas-mãos (Component <-> Template): O valor é sincronizado entre o template e o component igualmente, uma alteração em qualquer um dos lados é passada ao outro. Ex: [(ngModel)]

5. Como se adiciona um *listener* de eventos do usuário em um componente? Por exemplo, como adicionar uma função que responde a um clique de usuário?
No angular é possível adicionar um listener de várias maneiras diferentes. 
Pelo template: dentro do elemento você pode declarar um listener de click, por exemplo, declarando dentro do elemento um onclick="console.log("clicado")" ou (click)="funcaoNoComponent()".
    No exemplo, usando onclick é necessário declarar diretamente a ação do click, no caso de (click) é possível chamar uma função que está no Component.
Pelo Javascript: basta pegar o object a qual você quer adicionar o listener (como um <button>) e chamar um addEventListener(), exemplo: object.addEventListener("click", funcaoNaComponent).

6. Quais as diferenças entre ``constructor`` e ``ngOnInit``, e quando devemos usar cada um?
O Constructor serve para injeção de dependências no Component, muito usado para inicializar services e permitir que seja usado suas funções.
Já o ngOnInit é um Lifecycle Hook, uma função que é rodada após o component ter sido criado e suas dependências construídas.
É preferível que se coloque qualquer lógica de inicialização no ngOnInit e deixe o constructor apenas para conectar com services e outras classes.

7. Quais as diferenças entre ``Observables`` e ``Promises``? Como você o utilizaria cada um em um ``template``?
Observables e Promises servem para guardar dados asyncronos, como dados que vêm de chamadas de API. Porem há algumas diferenças entre eles.
Observables podem guardar diversos valores tal qual um array enquanto o Promise guarda apenas um valor. Além disso Observables tem acesso a diversos operadores como map, for, forEach, filter, reduce, retry, retryWhen, entre outos. Os Promises chamam suas requisições assim que são inicializados enquanto observables dependem de uma subscrição (.subscribe()) para fazer as chamadas.
Para poder pegar o valor de Observables e Promises no template, há o pipe 'async' que irá esperar o resultado e assim que tiver, estará disponível no template. 

8. Quais as diferenças entre ``template-driven forms`` e ``reactive forms``? Como fazer validação de dados de formulário em cada caso?
No template-driven form o formulário é assincrono e a maior parte de sua lógica é programada no template enquanto um reactive form é em sua maioria sincrono e sua lógica reside em maior parte no Component. 
Para a validação de dados em um formulário template-drive, será indicado se o item é obrigatório adicionando no <input> o atributo 'required'. Ex: <input ngModel required (...)>. 
Enquanto em um formulário reactive, o required é indicado dentro do FormGroup criado no Component, inicializando o FormControl com um segundo paramêtro, 'Validators.required'. Ex: new FormGroup({ 'item': new FormControl(null, Validators.required)}) 

9.  Como se utiliza o ``angular router``? Quais são as formas de enviar parâmetros para uma rota?
Para a definição das rotas e seus componentes é usado o service angular router, cria-se um array de Route que será importado pela RouterModule.
Cada Route deve ter um atributo 'path' que guarda a URL de caminho para essa rota e um atributo 'component' que indica o component dessa rota.
É possível enviar parâmetros simples pela url, indicando no path o nome do parâmetro após ':'. Ex: path: 'pokemon/:id'.
Também é possível passar parâmetros ao navegar para a rota com Router.navigate('urlRota', {state: {nomeParametro: parametro}})

10.  O que são *guards de rota* e para que são úteis?
Route Guards é uma interface que controla o acesso a rotas. Muito útil para assegurar que nenhum usuario sem acesso poderá acessar uma página restrita.

11. O que é ``NgZone``? Em que momento deve ser utilizada?

12. O que é *injeção de dependências* e por que isso é útil? Como você realiza injeção de dependências entre módulos?
Injeção de dependências é uma técnica em que uma classe requisita dependências de fontes externas e as usa sem que precise cria-las dentro da classe. Muitas vezes, as depêndencias são services que contém diversas funções que podem ser usadas.

Ah, e a mais importante de todas: Bulbassauro, Charmander ou Squirtle? =)
A fluidez do Squirtle

### Projeto: Criando uma Pokédex usando a PokéAPI

Pokémon é uma enorme franquia com jogos, desenhos, filmes, brinquedos e diversos produtos mundialmente conhecidos. Da [Wikipédia](https://pt.wikipedia.org/wiki/Pokémon_(série_de_jogos_eletrônicos)):

> Pokémon é uma série de jogos eletrônicos desenvolvidos pela Game Freak e publicados pela Nintendo como parte da franquia de mídia Pokémon. Lançado pela primeira vez em 1996 no Japão para o console Game Boy, a principal série de jogos de RPGs, que continuou em cada geração em portáteis da Nintendo.
> 
> Os jogos são geralmente lançados em pares - cada um com pequenas variações - com uma recriação aprimorado dos usados jogos lançados em alguns anos depois das versões originais. Enquanto a série principal consiste em RPGs, os spin-off abrangem outros gêneros, como RPG de ação, quebra-cabeça e jogos virtuais para animais de estimação.
> 
> A partir de 24 de novembro de 2017, mais de 300 milhões de jogos de Pokémon foram vendidos em todo o mundo, em 76 títulos. Isso faz de Pokémon a segunda franquia de jogos eletrônicos mais vendidas, atrás da própria franquia da Nintendo Mario.

Em 2016, a Nintendo lançou o jogo Pokémon Go, para Android e iOS, que permitia aos jogadores "caçar" Pokémons no "mundo real" através de realidade aumentada, utilizando o GPS e a câmera dos celulares dos jogadores. Seus monstrinhos capturados ficavam listados na chamada Pokédex, um acervo de Pokémons que já existia desde o primeiro jogo.

Seu objetivo, neste projeto, é criar uma Pokédex em Angular usando a PokéAPI.

A [PokéAPI](https://pokeapi.co/) é uma API aberta, sem necessidade de  disponibiliza uma API REST com, entre outras coisas, informações de todos os Pokémons até a geração 7. Você pode consultar a documentação da API [aqui](https://pokeapi.co/docs/v2).

Você é livre para montar a aplicação como quiser, mas gostaríamos de ver a listagem de todos o Pokémons, com informações básicas, em uma página inicial e detalhes do Pokémon selecionado em outra página. Como referência de layout, recomendamos que utilize as seguintes Pokédex como exemplo:

- [Pokédex oficial](https://www.pokemon.com/br/pokedex/)

(link: [https://www.pokemon.com/br/pokedex/](https://www.pokemon.com/br/pokedex/))

![Pokédex oficial](pokemon.com.png)

- [Pokedex.org](https://pokedex.org/)

(link: [https://pokedex.org/](https://pokedex.org/))

![Podedex.org](pokedex.org.png)

Temos alguns pré-requisitos:
- Utilização de Angular 8+;
- Uso de SASS/SCSS para CSS da aplicação;
- Design responsivo;
- Testes usando JEST serao obrigatorios !!!!
- Ah, e não se esqueça de mostrar os sprites (as imagens) de cada Pokémon!

Além disso, vamos avaliar como você organiza e documenta o projeto, e a estrutura de módulos, componentes, serviços e rotas que você criou.

Ganhe pontos extras por:
- Uso de Angular Material;
- Layout diferenciado e animações;
- Mecanismo de pesquisa;
- Cache e persistência dos dados no ``localStorage`` ou ``IndexedDB``;
- Funcionamento offline com os dados cacheados - melhor ainda se for um PWA!;
- Testes unitários e end to end;
- Scripts de deploy;
- Organização e mensagens dos commits.

E não se esqueça, bugs e exceções são como Pokémons: *Gotta catch 'em all!*

**Boa sorte! =)**

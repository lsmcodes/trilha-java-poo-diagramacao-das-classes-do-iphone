# DIO - Trilha POO Java
<div style="display:inline-block">
        <picture  title="Java">
                <source height="40" width="40" media="(prefers-color-scheme: light)" srcset="https://cdn.simpleicons.org/openjdk/000000">
                <img height="40" width="40" src="https://cdn.simpleicons.org/openjdk/FFFFFF" />
        </picture>
        <picture  title="Apache Maven">
                <source height="40" width="40" media="(prefers-color-scheme: light)" srcset="https://cdn.simpleicons.org/apachemaven/000000">
                <img height="40" width="40" src="https://cdn.simpleicons.org/apachemaven/FFFFFF" />
        </picture>
        <picture  title="Spring Boot">
                <source height="40" width="40" media="(prefers-color-scheme: light)" srcset="https://cdn.simpleicons.org/springboot/000000">
                <img height="40" width="40" src="https://cdn.simpleicons.org/springboot/FFFFFF" />
        </picture>
        <picture  title="UML">
                <source height="40" width="40" media="(prefers-color-scheme: light)" srcset="https://cdn.simpleicons.org/uml/000000">
                <img height="40" width="40" src="https://cdn.simpleicons.org/uml/FFFFFF" />
        </picture>
        <picture  title="Mermaid">
                <source height="40" width="40" media="(prefers-color-scheme: light)" srcset="https://cdn.simpleicons.org/mermaid/000000">
                <img height="40" width="40" src="https://cdn.simpleicons.org/mermaid/FFFFFF" />
        </picture>
</div>

## Autor do Desafio e Repositório Original
- [Gleyson Sampaio](https://github.com/glysns)
- [Desafio Diagramação de Classes do Iphone](https://github.com/digitalinnovationone/trilha-java-basico/tree/main/desafios/poo)

## Contexto
O desafio é diagramar e modelar um Iphone em `UML` e `código` baseado-se no vídeo do [lançamento do primeiro Iphone](https://www.youtube.com/watch?v=9ou608QQRq8), onde Steve Jobs anuncia que o Iphone seria a junção de um reprodutor musical, um aparelho telefônico e um dispositivo de comunicação com a internet (navegador).

Utilize conceitos de POO para diagramar com a ferramenta de sua preferência e criar as interfaces que representam as seguintes funções:

- `Reprodutor Musical`: tocar, pausar, selecionarMusica
- `Aparelho Telefônico`: ligar, atender, iniciarCorreioVoz
- `Navegador`: exibirPagina, adicionarNovaAba, atualizarPagina

Além de diagramar e criar a classe que representa o Iphone em si.

## Diagrama UML
Abaixo temos o diagrama UML que representa o Iphone herdando as características apresentadas:

```mermaid
classDiagram
    class ReprodutorMusical
    <<interface>> ReprodutorMusical
    ReprodutorMusical : +tocar()
    ReprodutorMusical : +pausar()
    ReprodutorMusical : +selecionarMusica()

    class AparelhoTelefonico
    <<interface>> AparelhoTelefonico
    AparelhoTelefonico : +ligar()
    AparelhoTelefonico : +atender()
    AparelhoTelefonico : +iniciarCorreioVoz()

    class Navegador
    <<interface>> Navegador
    Navegador : +exibirPagina()
    Navegador : +adicionarNovaAba()
    Navegador : +atualizarPagina()

    ReprodutorMusical <|-- Iphone
    AparelhoTelefonico <|-- Iphone
    Navegador <|-- Iphone

```
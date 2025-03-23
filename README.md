# Documentação do Sistema

## Sumário

- [Documentação do Sistema](#documentação-do-sistema)
  - [Sumário](#sumário)
  - [Dados do Cliente](#dados-do-cliente)
  - [Equipe de Desenvolvimento](#equipe-de-desenvolvimento)
  - [Introdução](#introdução)
  - [Objetivo](#objetivo)
  - [Escopo](#escopo)
    - [Parte 1 - Teclado](#parte-1---teclado)
      - [Requisitos funcionais (Teclado)](#requisitos-funcionais-teclado)
      - [Requisitos não funcionais (Teclado)](#requisitos-não-funcionais-teclado)
    - [Parte 2 - Software](#parte-2---software)
      - [Requisitos funcionais (Software)](#requisitos-funcionais-software)
      - [Requisitos não funcionais (Software)](#requisitos-não-funcionais-software)
  - [Backlogs do Produto](#backlogs-do-produto)
    - [Teclado](#teclado)
    - [Software](#software)
  - [Cronograma](#cronograma)
  - [Materiais e Métodos](#materiais-e-métodos)
    - [Modelagem do Sistema](#modelagem-do-sistema)
    - [Tecnologias Utilizadas](#tecnologias-utilizadas)
    - [Arquitetura do Sistema](#arquitetura-do-sistema)
  - [Resultados](#resultados)
    - [Protótipo](#protótipo)
    - [Códigos das Principais Funcionalidades](#códigos-das-principais-funcionalidades)
  - [Conclusão](#conclusão)
    - [Impacto do Sistema](#impacto-do-sistema)
    - [Melhorias Futuras](#melhorias-futuras)
  - [Relato Individual do Processo](#relato-individual-do-processo)
    - [Caio Pontes Magalhães](#caio-pontes-magalhães)
    - [David Henrique Queiroz Viotti Fernandes](#david-henrique-queiroz-viotti-fernandes)
    - [Laura  Santos Honório](#laura--santos-honório)
    - [Letícia Tavares Braga](#letícia-tavares-braga)
    - [Lizandra Gomes de Souza](#lizandra-gomes-de-souza)

---

## Dados do Cliente

- **Título do Projeto**: aeon: teclado que se adapta ao seu corpo, não o contrário.
- **Cliente**: BrainX
- **CNPJ/CPF**: 58.450.889/0001-99
- **Contato**: Caio Pontes Magalhães
- **Email do contato**: <caio@brainx.dev>

---

## Equipe de Desenvolvimento

| Nome completo                           | Curso                  | Disciplina                          |
| --------------------------------------- | ---------------------- | ----------------------------------- |
| Caio Pontes Magalhães                   | Ciências da Computação | Programação de Software Básico em C |
| David Henrique Queiroz Viotti Fernandes | Ciências da Computação | Programação de Software Básico em C |
| Laura  Santos Honório                   | Ciências da Computação | Programação de Software Básico em C |
| Letícia Tavares Braga                   | Ciências da Computação | Programação de Software Básico em C |
| Lizandra Gomes de Souza                 | Ciências da Computação | Programação de Software Básico em C |

---

| Professores Orientador      |
| --------------------------- |
| Kesede Rodrigues Julio      |
| *Mauro ...*                 |
| *Professor de Fisioterapia* |

---

## Introdução

O projeto aeon surgiu a partir da necessidade de pessoas que passam longos períodos no computador e sofrem com dores causadas por má postura, ou se preocupam com esse tema. Além disso, existe uma dificuldade relativamente alta em configurar e personalizar teclados split disponíveis hoje no mercado, exigindo conhecimentos técnicos avançados.

Para resolver esses problemas, o aeon será composto por duas frentes: a primeira, que será feita junto ao professor Mauro e o *Professor de Fisioterapia*, será o desenvolvimento de um teclado físico com layout ergonômico personalizado, baseado na estrutura do corpo do usuário final, promovendo a postura correta e o conforto. Em segundo lugar, com o professor Kasede, será criado um software intuitivo que permitirá ao usuário final configurar o teclado sem precisar reprogramá-lo manualmente, com recursos como criação de macros, suporte a múltiplos layouts (como Dvorak e Colemak), e uma plataforma gamificada para treinar digitação de forma divertida e eficaz.

As tecnologias que optamos por utilizar são: microcontroladores (nRF52840), firmware ZMK, API em C para gerar o keymap (layout do teclado) e uma interface web em React para facilitar a personalização do teclado. A gamificação será feita em TypeScript para integrar-se à aplicação web, transformando-a em um hub para entusiastas de teclados, além de um simples configurador.

Impacto: O projeto Aeon vai criar um teclado pensado no corpo humano, e não um teclado ao qual precisamos nos adaptar para utilizar, promovendo saúde postural. Além disso, nossa segunda vertente permitirá uma personalização intuitiva e uma nova experiência de digitação no dia a dia, com treinamentos envolventes que facilitarão o aprendizado.

---

## Objetivo

Criar um teclado split ergonômico e funcional, removendo a necessidade de o usuário final ter conhecimentos técnicos para recompilar o firmware e criando incentivos para que ele melhore sua velocidade de escrita.

---

## Escopo

### Parte 1 - Teclado

#### Requisitos funcionais (Teclado)

- Desenho da PCB
- Protótipo teclado
- Teclado Final

#### Requisitos não funcionais (Teclado)

- Melhores peças
- Case final
- Criação de macros
- Sem fio
- Conexão bluetooth

### Parte 2 - Software

#### Requisitos funcionais (Software)

- Conversor json to keymap
- Interface para criação do layout
- Envio do keymap para o Teclado (Sem fleshar)

#### Requisitos não funcionais (Software)

- Gameficação do treinamento
- Construção de Macros
- layouts comuns
- Customização do RGB

---

## Backlogs do Produto

### Teclado

- Características Fisicas
  - Melhores peças
  - Split
  - Case de Aluminio
  - RGB no topo
  - Gasket mount
  - HotSwap
  - Pintura Anodizada
  - Three mode
  - Ortolinear
  - Potenciômetro
- Característias do Firmware
  - Função sem fio
  - Three mode
  - Rendenização de imagem
  - Interação com digitação
  - Alteração de layout sem Flash
- Documentação
- Apresentação

### Software

- Funcionalidades
  - Criação de Macros
  - Customização do RGB
  - Gameficação para Treino
  - Alteração de layout
- UI/UX
  - Dark and White mode
  - Web
  - Velocidade
  - Simplificação de Uso
- Documentação
- Apresentação

---

## Cronograma

Infelizmente, são dois projetos, e as datas são volátil, e as licenças de visualizações são cobradas no software utilizado (ClickUp). Portanto, apresentarei apenas uma imagem do cronograma feito no projeto do software. Caso tenha interesse em ver com mais detalhes, estarei à disposição.

![Gantt](./assets/Gantt.png)

---

## Materiais e Métodos

### Modelagem do Sistema

*<A modelagem do seu sistema são diagramas (desenhos) da sua estrutura ou comportamento. A UML (Unified Modelling Language) oferece diversos diagramas para que você possa modelar seu sistema. Escolha, pelo menos, dois modelos e insira aqui. Por exemplo, Modelo de Dados (Diagrama de Classe ou MER), Casos de Uso, Diagrama de Sequência, Diagrama de Atividades etc.>*

### Tecnologias Utilizadas

- Obsidian: Modelagem UML
- Typescript: Lógica do front-end
- HTML/CSS: Front-end
- C: Lógica da criação do layout e firmware
- Click-up: Gerenciamento do Projeto
- Jetbrains IDEs: IDEs para programar tudo
- VS-CODE: Editor de texto
- Git: Versionamento
- GitHub: Ospedagem e organização do projeto
- AWS: Hospedagem da aplicação em Produção
- GoDaddy: Compra de Dominio e gerenciador DNS
- Docker: Escalar aplicação
- Nginx: Proxy reverso
- Illustrato/Photoshop: Criação de Logo e Designs
- KiCad: Criação da PCB
- AI: Muita AI para ajudar kkk
- ZMK: Firmware escolhido para controlar o teclado
- Protocol Buffer: Linguagem de comunicação entre porta COM e Firmware

### Arquitetura do Sistema

*<Insira aqui uma imagem contendo a arquitetura do sistema e o fluxo das informações. Se a arquitetura for muito simples, detalhe o fluxo dos processos.>*

---

## Resultados

### Protótipo

*<São as telas do software e suas descrições. Em cada uma delas, descreva as ações possíveis do usuário e reações do sistema. Isto pode ser feito através do print das telas do seu sistema.>*

### Códigos das Principais Funcionalidades

<Copy-cole aqui as seções mais relevantes do seu código. Insira comentários sobre cada seção.>

```<linguagem>
<seção de código com comentários>
```

---

## Conclusão

### Impacto do Sistema

<Como o sistema impactou (alterou positivamente) o processo do cliente>

### Melhorias Futuras

<Elencar, pelo menos, uma melhoria que poderá ser realizada futuramente no sistema.>

---

## Relato Individual do Processo

### Caio Pontes Magalhães

O projeto foi uma quebra de expectativa, honestamente. Inicialmente, parecia que seria algo muito simples, pois nosso projeto seria apenas uma variação de alguns projetos existentes.
Mas, ao longo do desenvolvimento, tomamos muitas decisões técnicas em prol da performance, estética e usabilidade. Isso trouxe experiências incríveis para nós, com a inclusão de features como tela, bateria, alteração de layout simplificada e mudança de layout físico.

Trouxe muitos aprendizados que levarei para a vida. Aprendi como funciona uma PCB de forma real; tive que aprender a usar o KiCad para poder prototipar a minha PCB de acordo com o layout que eu queria, entender como funciona o upload de firmware, listar todos os possíveis microcontroladores e seus prós e contras, escolher um firmware que entregasse tudo o que eu queria, fazer engenharia reversa pegando os pacotes sniffer que eram enviados por uma aplicação para poder desenvolver minha própria API para isso...

Tive excelentes experiências com esse projeto e ainda vou ter. É algo ao qual ainda estou me dedicando e, sem sombra de dúvidas, vou sair melhor desse projeto.

### David Henrique Queiroz Viotti Fernandes

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

### Laura  Santos Honório

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

### Letícia Tavares Braga

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

### Lizandra Gomes de Souza

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

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
      - [Diagrama de Classe](#diagrama-de-classe)
    - [Tecnologias Utilizadas](#tecnologias-utilizadas)
    - [Arquitetura do Sistema](#arquitetura-do-sistema)
  - [Resultados](#resultados)
    - [Protótipo](#protótipo)
      - [Protótipo do Teclado](#protótipo-do-teclado)
      - [Protótipo da aplicação](#protótipo-da-aplicação)
    - [Códigos das Principais Funcionalidades](#códigos-das-principais-funcionalidades)
  - [Conclusão](#conclusão)
    - [Impacto do Sistema](#impacto-do-sistema)
    - [Melhorias Futuras](#melhorias-futuras)
      - [Melhoria no Prótotipo](#melhoria-no-prótotipo)
      - [Melhoria no Software](#melhoria-no-software)
  - [Homologação](#homologação)
  - [Divulgação](#divulgação)
    - [Linkedin do Projeto](#linkedin-do-projeto)
  - [Seminário de Projetos de Software](#seminário-de-projetos-de-software)
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
| Alef *                                  | Ciências da Computação | Programação de Microcontroladores   |
| André *                                 | Ciências da Computação | Programação de Microcontroladores   |
| Caio Pontes Magalhães                   | Ciências da Computação | Programação de Software Básico em C |
| David Henrique Queiroz Viotti Fernandes | Ciências da Computação | Programação de Software Básico em C |
| Jean *                                  | Ciências da Computação | Programação de Microcontroladores   |
| Laura  Santos Honório                   | Ciências da Computação | Programação de Software Básico em C |
| Letícia Tavares Braga                   | Ciências da Computação | Programação de Software Básico em C |
| Lizandra Gomes de Souza                 | Ciências da Computação | Programação de Software Básico em C |
| Reian Reis *                            | Ciências da Computação | Programação de Microcontroladores   |

---

| Professores Orientador      |
| --------------------------- |
| Kesede Rodrigues Julio      |
| *Mauro ...*                 |

---

## Introdução

O projeto aeon surgiu para ajudar pessoas que passam longos períodos no computador e sofrem com dores causadas por má postura ou que se preocupam com ergonomia. Além disso, existe uma dificuldade relativamente alta em configurar e personalizar teclados split disponíveis hoje no mercado, exigindo conhecimentos técnicos avançados em hardware e programação.

Para resolver esses problemas, aeon será composto por duas frentes: a primeira, que será desenvolvida junto ao professor Mauro, será a criação de um teclado com layout ergonômico personalizado, baseado na experiência do usuário final, promovendo a postura correta e o conforto.

Em segundo lugar, com o professor Kasede, será criado um software intuitivo que permitirá ao usuário final configurar o teclado sem precisar reprogramá-lo manualmente, com recursos como criação de macros, suporte a múltiplos layouts (como Dvorak e Colemak), alteração do perfil RGB e uma plataforma gamificada para treinar digitação de forma divertida e eficaz.

As tecnologias que optamos por utilizar estão mais detalhadas no tópico de [Tecnologias Utilizadas](#tecnologias-utilizadas), mas, para uma introdução, é interessante mencionar os microcontroladores (dois nRF52840), firmware ZMK, API construída em C para gerar o keymap (layout do teclado) e uma interface web em React para facilitar a personalização do teclado. A gamificação será feita em TypeScript, uma vez que a aplicação é web. O TypeScript se comunica de forma nativa com JavaScript, linguagem nativa dos navegadores, transformando assim a plataforma em um hub para entusiastas de teclados.

**Impacto:** O projeto aeon vai criar um teclado pensado para o corpo humano, e não um teclado ao qual precisamos nos adaptar para utilizar. No começo, existe uma curva de aprendizado, por termos usado teclados escalonados por anos, mas a mudança de layout físico promove maior saúde postural, já que estamos seguindo o fomato do corpo. Além disso, nossa segunda vertente permitirá uma personalização intuitiva e uma nova experiência de digitação no dia a dia, com treinamentos envolventes que facilitarão o aprendizado.

---

## Objetivo

Criar um teclado split ergonômico e funcional, eliminando a necessidade do usuário final ter conhecimentos técnicos para recompilar o firmware e criar uma plataforma que ofereça incentivos para que ele treine a migração do layout e aumente sua velocidade e produtividade.

---

## Escopo

### Parte 1 - Teclado

#### Requisitos funcionais (Teclado)

- [x] Desenho da PCB
- [x] Protótipo do teclado
- [x] Teclado funcional

#### Requisitos não funcionais (Teclado)

- [x] Melhores peças
- [ ] Case final
- [ ] Criação de macros
- [ ] Sem fio
- [ ] Conexão Bluetooth
- [ ] Teclado Final

### Parte 2 - Software

#### Requisitos funcionais (Software)

- [ ] Conversor JSON para keymap
- [x] Interface para criação do layout
- [ ] Home Page

#### Requisitos não funcionais (Software)

- [ ] Gamificação do treinamento
- [ ] Construção de macros
- [ ] Layouts comuns
- [ ] Customização do RGB
- [ ] Envio do keymap para o teclado (sem flash)

---

## Backlogs do Produto

### Teclado

- Características Físicas
  - Melhores peças
  - Split
  - Case de alumínio
  - RGB no topo
  - Gasket mount
  - HotSwap
  - Pintura anodizada
  - Three mode
  - Ortolinear
  - Potenciômetro
  - Trackball
- Características do Firmware
  - Função sem fio
  - Three mode
  - Renderização de imagem
  - Interação com digitação
  - Alteração de layout sem flash
- Documentação
- Apresentação

### Software

- Funcionalidades
  - Criação de macros
  - Customização do RGB
  - Gamificação para digitação
  - Alteração de layout
- UI/UX
  - Dark e White mode
  - Web
  - Velocidade
  - Simplificação de uso
- Documentação
- Apresentação

O backlog principal está no nosso software de gestão, no qual estamos usando para manter a organização do projeto.

---

## Cronograma

Infelizmente, são dois projetos, e as datas são voláteis. Além disso, as licenças de visualização são cobradas no software utilizado (ClickUp). Portanto, apresentarei apenas uma imagem do cronograma feito no projeto do software. Caso haja interesse em ver com mais detalhes, estarei à disposição.

![Gantt](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/Gantt.png)

---

## Materiais e Métodos

### Modelagem do Sistema

#### Diagrama de Classe

![structure](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/structure.png)

### Tecnologias Utilizadas

- Obsidian: Modelagem UML e documentação
- nRF52840: Microcontrolador com suporte a Bluetooth e bateria
- TypeScript: Lógica do front-end e do Game
- HTML/CSS: Front-end
- C: Lógica da criação do layout e firmware
- ClickUp: Gerenciamento do projeto
- JetBrains IDEs: IDEs para programar tudo
- VS Code: Editor de texto
- Git: Versionamento
- GitHub: Hospedagem e organização do projeto
- AWS: Hospedagem da aplicação em produção
- GoDaddy: Compra de domínio e gerenciador DNS
- Docker: Escalabilidade da aplicação
- Nginx: Proxy reverso
- Illustrator/Photoshop: Criação de logo e designs
- KiCad: Criação da PCB
- AI: Muita AI para ajudar kkk
- ZMK: Firmware escolhido para controlar o teclado
- Protocol Buffer: Linguagem de comunicação entre a porta COM e o firmware

### Arquitetura do Sistema

Temos uma aplicação baseada em TypeScript, com funcionalidades implementadas em C, para uma conversão rápida de JSON para binário. Esse conversor envia o binário para a aplicação, que, antes de permitir a alteração do layout, estabelece uma conexão com a porta COM onde está conectado o teclado do usuário, sendo possível o envio do binário para o firmware.

![System Design](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/system_design.png)

---

## Resultados

### Protótipo

#### Protótipo do Teclado

Sua prototipagem está sendo mantida no repositório referente ao assunto. Para acompanhar, acesse:

- [Prototipagem Layout](https://github.com/aeon-keyboard/pcb)
- [Prototipagem Case](https://github.com/aeon-keyboard/case)

#### Protótipo da aplicação

Sua prototipagem está sendo mantida no repositório referente ao assunto. Para acompanhar, acesse:

- [Front-end](https://github.com/aeon-keyboard/aeon-fnd)
- [Back-end](https://github.com/aeon-keyboard/aeon-bkd)
- [Identidade Visual](https://github.com/aeon-keyboard/branding)

### Códigos das Principais Funcionalidades

Todo código da aplicação é aberto com licença MIT, então sintase livre para acompanhar através dos links abaixo:

- [Front-end](https://github.com/aeon-keyboard/aeon-fnd)
- [Back-end](https://github.com/aeon-keyboard/aeon-bkd)

---

## Conclusão

### Impacto do Sistema

Nosso usuário final está muito satisfeito com o modelo criado inicialmente. Ele teve uma curva de aprendizado consideravelmente alta — cerca de uma semana para conseguir digitar na mesma velocidade a que estava acostumado — considerando que já tinha prática em digitar corretamente.
Porém, ele se sente muito confortável com o novo modelo de teclado, e isso trouxe apenas um inconveniente: agora ele tem dificuldades com teclados normais kkk.

### Melhorias Futuras

#### Melhoria no Prótotipo

- Erramos ao prototipar a PCB; esqueci de enviar o arquivo com mais de duas camadas. Com isso, eu poderia ter conectado a bateria diretamente à PCB, o que deixaria o projeto mais premium.
- Adição de baterias
- Inclusão de trackpad

#### Melhoria no Software

- Inclusão de sistema de gamificação
- Adicionar Kubernetes na gestão de containers

---

## Homologação

Após as entregas parciais, realizadas de acordo com os requisitos do sistema  e cronograma, o MVP foi apresentado em uma reunião, realizada entre o time de desenvolvedores e o cliente.

<image>
<image>
<image>
<image>

## Divulgação

### Linkedin do Projeto

*[Link para o perfil do projeto no Linkedin](https://www.linkedin.com/in/aeon-teclado-a15697358/)*

---

## Seminário de Projetos de Software

...

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

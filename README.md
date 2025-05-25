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
  - [Carta de Autorização](#carta-de-autorização)
  - [Relato Individual do Processo](#relato-individual-do-processo)
    - [Álefe Guímel Vieira de Lacerda](#álefe-guímel-vieira-de-lacerda)
    - [André Luís da Silva Santos](#andré-luís-da-silva-santos)
    - [Caio Pontes Magalhães](#caio-pontes-magalhães)
    - [David Henrique Queiroz Viotti Fernandes](#david-henrique-queiroz-viotti-fernandes)
    - [Jean \*](#jean-)
    - [Laura  Santos Honório](#laura--santos-honório)
    - [Letícia Tavares Braga](#letícia-tavares-braga)
      - [Metodologia](#metodologia)
      - [Resultados e Discussão](#resultados-e-discussão)
      - [Considerações Finais](#considerações-finais)
    - [Lizandra Gomes de Souza](#lizandra-gomes-de-souza)
    - [Reian Reis \*](#reian-reis-)

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
| Álefe Guímel Vieira de Lacerda          | Ciências da Computação | Programação de Microcontroladores   |
| André Luís da Silva Santos              | Ciências da Computação | Programação de Microcontroladores   |
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
- [X] Conexão Bluetooth
- [X] Teclado Final

### Parte 2 - Software

#### Requisitos funcionais (Software)

- [X] Conversor JSON para keymap
- [x] Interface para criação do layout
- [X] Home Page

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

![Gantt](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/gantt.png)

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
- C#: Lógica da criação do layout e firmware
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

Temos uma aplicação baseada em TypeScript, com funcionalidades implementadas em C#, para uma conversão rápida de JSON para binário. Esse conversor envia o binário para a aplicação, que, antes de permitir a alteração do layout, estabelece uma conexão com a porta COM onde está conectado o teclado do usuário, sendo possível o envio do binário para o firmware.

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

<afazer>

## Divulgação

### Linkedin do Projeto

![Apresentacao](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/linkedin.png)
*[Link para o perfil do projeto no Linkedin](https://www.linkedin.com/in/aeon-teclado-a15697358/)*

---

## Seminário de Projetos de Software

Fotos com apresentação no dia do Seminário

<div href="https://youtu.be/rgqZIPgFl2g" target="_blank" align="center">
  <img
    src="https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/tumb.png"
    alt="Apresentação do Projeto Aeon"
    width="640"
/>
</div>

**Apresentação na semana da Tecnologia**
![Apresentacao](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/group_presentation.png)
**Pessoal assistindo a apresentação do grupo**
![Apresentacao](https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/spectators_presentation.png)

...

## Carta de Autorização

<div href="https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/Carta de Autorizacao-LTD-Assinada.pdf" target="_blank" align="center">
  <img
    src="https://raw.githubusercontent.com/aeon-keyboard/.github/main/assets/icon_pdf.png"
    alt="Autorização em PDF"
    width="210" />
    <p>📄 Clique na imagem para visualizar a autorização em PDF</p>
</div>


## Relato Individual do Processo

### Álefe Guímel Vieira de Lacerda

### André Luís da Silva Santos

### Caio Pontes Magalhães

O projeto foi uma quebra de expectativa, honestamente. Inicialmente, parecia que seria algo muito simples, pois nosso projeto seria apenas uma variação de alguns projetos existentes.
Mas, ao longo do desenvolvimento, tomamos muitas decisões técnicas em prol da performance, estética e usabilidade. Isso trouxe experiências incríveis para nós, com a inclusão de features como tela, bateria, alteração de layout simplificada e mudança de layout físico.

Trouxe muitos aprendizados que levarei para a vida. Aprendi como funciona uma PCB de forma real; tive que aprender a usar o KiCad para poder prototipar a minha PCB de acordo com o layout que eu queria, entender como funciona o upload de firmware, listar todos os possíveis microcontroladores e seus prós e contras, escolher um firmware que entregasse tudo o que eu queria, fazer engenharia reversa pegando os pacotes sniffer que eram enviados por uma aplicação para poder desenvolver minha própria API para isso...

Tive excelentes experiências com esse projeto e ainda vou ter. É algo ao qual ainda estou me dedicando e, sem sombra de dúvidas, vou sair melhor desse projeto.

### David Henrique Queiroz Viotti Fernandes

Desenvolver um teclado ergonômico não é nada simples! Mas, conforme mergulhamos no desenvolvimento, ficou claro que estávamos lidando com algo muito além de apenas programação.

Minha principal responsabilidade foi na parte de desenvolvimento e programação, e posso dizer com todas as letras: foi desafiador, sim, mas também extremamente enriquecedor. Um dos maiores perrengues foi colocar todo o sistema para rodar na nuvem. Na teoria, parecia algo direto… na prática, exigiu muito mais estudo, testes (muitos!), ajustes finos e uma boa dose de paciência. Cada detalhe fazia diferença: desde a comunicação entre os dispositivos até a responsividade e estabilidade do sistema. Tudo precisava funcionar de forma fluida e com excelência, porque quem vai usar realmente precisa que funcione.

Mas sabe o que foi mais marcante? Ver o código ganhando vida. Trabalhar na prototipação e implementação de funcionalidades que tornaram o teclado acessível de verdade foi transformador. Assistir a esse projeto deixar de ser só “um sistema” para virar uma ferramenta que pode fazer diferença real na vida de alguém… não tem preço.

Aprendi muito sobre acessibilidade, sobre integração com APIs e dispositivos físicos, e principalmente sobre como pensar no usuário final. E, nesse caso, o usuário final precisa de algo muito além do padrão. Isso mexeu comigo. Não só como programador, mas como ser humano.

Esse projeto me ensinou que a verdadeira tecnologia não é a mais complexa — é a que alcança pessoas. Fazer parte de algo que é funcional, sim, mas também inclusivo, é uma experiência que eu vou levar para a vida toda. E o mais incrível? Isso é só o começo.

### Jean *

### Laura  Santos Honório

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

### Letícia Tavares Braga

Neste projeto, fomos desafiados a desenvolver uma aplicação que envolvesse a linguagem C. Achei a proposta bastante interessante e encarei como mais um desafio a ser superado, já que eu já havia programado em C anteriormente, em uma disciplina anterior.

Minha principal contribuição foi na parte de frontend do projeto, ou seja, na construção da interface visual da aplicação, garantindo que ela fosse intuitiva e agradável para o usuário.

#### Metodologia

A experiência foi vivenciada na instituição de ensino em que estudamos, com a participação ativa minha, dos meus colegas e do professor orientador, todos mencionados neste mesmo documento. Também contamos com a colaboração do nosso cliente. O projeto foi desenvolvido ao longo de um semestre, entre fevereiro e junho de 2025.

Inicialmente, realizamos reuniões para definir a ideia central do projeto, chegando a um consenso sobre o desenvolvimento de uma aplicação para reconfigurar as teclas de um teclado ergonômico, que foi criado em conjunto com outra disciplina que um colega de projeto cursava. Em seguida, iniciamos a construção do esboço do projeto no Figma. Após essa etapa, desenvolvemos o LinkedIn para documentação e divulgação. Logo após, iniciamos a construção do frontend e, em seguida, do backend. Por fim, tivemos que criar um banner para a apresentação desse mesmo projeto.

#### Resultados e Discussão

Tínhamos um esboço inicial e uma expectativa de como iríamos desenvolver este projeto, e, até o momento, tudo tem se concretizado conforme o planejado. Fiquei muito satisfeita com o resultado que estamos alcançando, e ver algo que antes era apenas uma ideia no papel se transformar em uma aplicação funcional é extremamente empolgante.

Ao longo desse processo, aprendi e descobri muitas coisas novas. Senti mais facilidade na parte de frontend, pois eu já havia programado com linguagens um pouco parecidas anteriormente.

Fiquei muito feliz com o quanto conseguimos avançar e estou gostando bastante do resultado até agora.

#### Considerações Finais

Embora o projeto ainda não esteja completamente finalizado, conseguimos entregar uma grande parte das principais funcionalidades, atendendo ao objetivo inicial da aplicação. No entanto, há um grande potencial para aprimoramentos futuros, tanto na melhoria dos recursos já existentes quanto na adição de novas funcionalidades que podem tornar a aplicação ainda mais completa e eficiente.

### Lizandra Gomes de Souza

<Um breve relato pessoal sobre o trabalho extensionista desenvolvido>

### Reian Reis *

# Processo Seletivo (#2)

Olá,

Inicialmente, gostaria de agradecer muito pela vontade de fazer parte da equipe da UNIFAGOC. Nós somos um centro universitário referência na zona da mata mineira. Nós, do Departamento de Tecnologia da Informação, desenvolvemos e mantemos os sistemas pertinentes à atividade da instituição. Temos como clientes os colaboradores do centro universitário, parceiros externos e, principalmente, nossos alunos.

A idéia dessa avaliação é nos permitir identificar melhor as habilidades dos candidatos à vaga de desenvolvedor fullstack. Esse desafio deve ser feito por você. Qualquer dúvida técnica relacionada ao teste, entre em contato com o avaliador.

A entrega deve ser feita por meio de um repositório publico aqui no github. Não se esqueça de criar um arquivo README.md na raiz de seu projeto com as instruções para utilização do seu projeto. Seguiremos extritamente essas instruções, por isso, tente deixar o mais claro e específico possível. Você terá 15 dias para execução de seu teste a contar da hora de envio deste material para seu email por nossa equipe de Recursos Humanos.

>![Vida de Programador](https://vidadeprogramador.com.br/wp-content/uploads/2011/10/tirinha319.png)
>(FONTE: Vida de Programador. Disponível em: https://vidadeprogramador.com.br/2011/10/26/prova-pratica/)

Nosso principal objetivo com essa avaliação é observar não só o estado atual da sua maturidade como desenvolvedor, mas também observar o quanto você pode crescer e como podemos ajudar você a conseguir isso. Por isso, lembre-se: Precisamos ver o máximo de módulos funcionais possíveis. 

> ### Não deixe de nos mostrar seu trabalho!

------

## Mudanças no mercado à caminho

Desde outubro de 2020, o mercado financeiro brasileiro vem sendo balançado pela iniciativa de integração tecnológica promovida pelo Banco Central (BaCen). O lançamento do PIX, método de pagamento instantâneo, vem mudando a forma com que as pessoas interagem com as empresas prestadoras de serviços, comércio e indústrias. Já não é incomun a possibilidade de pagamento de nossas compras na Internet utilizando a nova ferramenta.

Na esteira do PIX, o BaCen agora propõe a implementação do _open banking_, uma plataforma institucional de compartilhamento de informações entre instituições financeiras, fintechs e bancos. Para saber um pouco mais, sugiro [esta matéria da InfoMoney](https://www.infomoney.com.br/guias/open-banking/).

Nosso disafio envolverá um protótipo dessa plataforma. 

Para nossa prova de conceito, desenvolveremos uma plataforma online com controle de acesso por usuário e senha. As entidades envolvidas na plaraforma serão:

![]()

#### A



Você precisará desenvolver o sistema em 3 partes: _Backend_, _API REST_, e _Frontend_. Para cada uma das partes, são requeridas algumas características, mas não se limite somente a elas. Mostre o máximo de features efetivamente funcionais que conseguir!

### Backend

O núcleo funcional do nosso sistema deverá ser desenvolvido em PHP 7+, considerando todas as boas práticas de desenvolvimento que achar importantes e em especial se atentando ao máximo as PHP Standard Recommendations (PSR). Esse backend deverá ser capaz de representar, modelar e tratar todos os dados envolvidos no sistema. É nele que as regras de negócios precisam estar implementadas e validadas. Os dados precisarão ser armazenados e recuperados de um banco de dados MySQL 5.5+ (indicamos a utilização da versão 5.7 por sua estabilidade). Atente-se à modelagem desse banco. Muitas vezes, um bom modelo de dados auxilia demais na implementação dos códigos.

### API REST

Toda a comunicação do aplicativo com suas diferentes instâncias precisará ser feita sob uma API REST privada. Os métodos precisarão representar a criticidade das informações e a segurança dos dados. Observer que para cada método existem operações conceitualmente já definidas.

### Frontend

A interface de visualização das informações precisará ser desenvolvida com tecnologias Javascript, CSS3 e HTML5. Indicamos fortemente a utilização do framework [Vue.js](https://vuejs.org/) e/ou [Quasar](https://quasar.dev/). Utilizamos esses dois nos nossos produtos e a implementação com eles será um diferencial, porém, bons códigos serão sempre bem avaliados, sejam em qual estrutura for. 

## Ambiente de Desenvolvimento e Entrega

O sistema deve ser implementado sobre um container Docker e seus arquivos de configuração (Dockerfile e/ou docker-compose.yml) precisam estar disponíveis no repositório a ser apresentado. Mais uma vez, é imprecindível que no arquivo README.md, na raiz do projeto, esteja bem definida todas as informações necessárias para a execução do projeto.

## Pontos de Avaliação

Além da completudo dos item acima descritos, serão avaliados:

* Arquivo README.md com as instruções para execução do sistema
* Legibilidade, facilide para modificação, eficiência e reusabilidade do código
* Orientação a Objetos
* Testes Automatizados (diferencial)
* Clean Code (diferencial)
* Object Calisthenics (diferencial)
* Princípios SOLID (diferencial)

## Material de Apoio

Os links abaixo são apenas material para apoio aos seus estudos. Não se limite à eles. Explore as possibilidades e expanções dos conceitos.

* *PHP Standard Recommendations* - [clique aqui](https://www.php-fig.org/psr/)
* *Clean Code: Boas práticas para escrever códigos impecáveis* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/2-clean-code-boas-pr%C3%A1ticas-para-escrever-c%C3%B3digos-impec%C3%A1veis-361997b3c8b5)
* *Object Calisthenics* - [clique aqui](https://www.neoassist.com/2017/05/31/object-calisthenics-9-regras-para-aperfeicoar-seus-codigos/)
* *O que é SOLID: O guia completo para você entender os 5 princícipos da POO* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
* *Entenda o que é Rest API e a importância dela para o site da sua empresa* - [clique aqui](https://rockcontent.com/br/blog/rest-api/)
# Processo Seletivo (#1)

Olá,

Inicialmente, gostaria de agradecer muito pela vontade de fazer parte da equipe da UNIFAGOC. Nós somos um centro universitário referência na zona da mata mineira. Nós, do Departamento de Tecnologia da Informação, desenvolvemos e mantemos os sistemas pertinentes à atividade da instituição. Temos como clientes os colaboradores do centro universitário, parceiros externos e, principalmente, nossos alunos.

A idéia dessa avaliação é nos permitir identificar melhor as habilidades dos candidatos à vaga de desenvolvedor fullstack. Esse desafio deve ser feito por você. Qualquer dúvida técnica relacionada ao teste, entre em contato com o avaliador.

A entrega deve ser feita por meio de um repositório publico aqui no github. Não se esqueça de criar um arquivo README.md na raiz de seu projeto com as instruções para utilização do seu projeto. Seguiremos extritamente essas instruções, por isso, tente deixar o mais claro e específico possível. Você terá 7 dias para execução de seu teste a contar da hora de envio pelo seu email.

------

## Uma nova ferramenta para nosso dia a dia

A informatização de sistemas antes baseados em documentos físicos veem transformando o dia a dia dos mais diversos setores da sociedade. De formas de pagamento à documentos governamentais, a revolução digital aproximou pessoas dos dados e elevou exponencialmente a capacidade de extração de informações e conhecimento. Uma das aplicações que já podemos ver no nosso dia a dia são sistemas de gestão de informações médicas, como o [Aplicativo do SUS](https://play.google.com/store/apps/details?id=br.gov.datasus.guardioes&hl=pt_BR) que possibilita a busca das informações médicas dos usuários e o acompanhamento de exames, vacinas e agendamentos.

A você é solicitado que desenvolva um sistema de controle de prontuário médico com as seguintes caracteristicas: 

* deverão existir três agentes no sistema: Paciente, Médico e Administrador. 
* os Administradores serão capazes de cadastrar os Pacientes e Médicos.
* os Médicos podem realizar lançamentos de resultados de exames e laudos médicos nas fichas dos Pacientes. 
* os Pacientes poderão solicitar Atendimentos com qualquer Médico inscrito no sistema, que por sua vez, deverá responder ao Paciente informado se esta disponível ou não. 
* os Pacientes não poderão solicitar Atendimentos a outro Médico antes da resposta da solicitação anterior.
* os Pacientes só poderão solicitar Atendimentos a Médicos que não possuam solicitações de Atendimento pendentes de resposta
* os Pacientes poderão solicitar a retirada dos seus dados do sistema, mas em razão de normas e legislação, esses dados precisarão ser anonimizados e não deletados.

Além das informações que achar necessário para o cadastro e autenticação dos agentes descritos, são obrigatórios as seguintes informações de acordo com o tipo do agente:

* Pacientes: Endereço residencial, Telefone de Contato, CPF (validar)
* Médicos: CPF (validar), Matrícula no Conselho Regional de Medicina (CRM), Especialidade Médica ([vide](https://pt.wikipedia.org/wiki/Lista_de_especialidades_m%C3%A9dicas))
* Administradores: CPF (validar)

Você precisará desenvolver o sistema em 3 partes: _Backend_, _API REST_, e _Frontend_. Para cada uma das partes, são requeridas algumas características abaixo listadas, mas não se limite somente a elas. Mostre o máximo de features efetivamente funcionais que conseguir!

### Backend

O núcleo funcional do nosso sistema deverá ser desenvolvido em PHP 7+, considerando todas as boas práticas de desenvolvimento que achar importantes e em especial se atentando ao máximo as PHP Standard Recommendations (PSR). Esse backend deverá ser capaz de representar, modelar e tratar todos os dados envolvidos no sistema. É nele que as regras de negócios precisam estar implementadas e validadas. Os dados precisarão ser armazenados e recuperados de um banco de dados MySQL 5.5+ (indicamos a utilização da versão 5.7 por sua estabilidade). Atente-se à modelagem desse banco. Muitas vezes, um bom modelo de dados auxilia demais na implementação dos códigos.

### API REST

Toda a comunicação do aplicativo com suas diferentes instâncias precisará ser feita sob uma API REST privada. Os métodos precisarão representar a criticidade das informações e a segurança dos dados. Observer que para cada método existem operações conceitualmente já definidas.

### Frontend

A interface de visualização das informações precisará ser desenvolvida com tecnologias Javascript, CSS3 e HTML5. Indicamos fortemente a utilização do framework [Vue.js](https://vuejs.org/) e/ou [Quasar](https://quasar.dev/). Utilizamos esses dois nos nossos produtos e a implementação com eles será um diferencial, porém, bons códigos serão sempre bem avaliados, sejam em qual estrutura for. 

Deverão existir as seguintes interfaces:

* uma interface de autenticação dos agentes, limitando o acesso às demais interfaces de acordo com o tipo de cada um
* uma interface para que os Administradores possam fazer a Criação, Leitura, Atualização e Deleção dos registros dos Pacientes e Médicos
* uma interface na qual aos Médicos poderão fazer o lançamento das informações sobre Exames e Laudos
* uma interface na qual os Médicos possam responder às solicitações de Atendimento dos Pacientes
* uma interface para que os Pacientes possam visualizar o histórico de Exames e Laudos cadastrados para eles.
* uma interface para que os Pacientes possam solicitar os Atendimentos pelos Médicos

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

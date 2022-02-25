# Processo Seletivo (#3)

Olá,

Inicialmente, gostaria de agradecer muito pela vontade de fazer parte da equipe da UNIFAGOC. Nós somos um centro universitário referência na zona da mata mineira. Nós, do Departamento de Tecnologia da Informação, desenvolvemos e mantemos os sistemas pertinentes à atividade da instituição. Temos como clientes os colaboradores do centro universitário, parceiros externos e, principalmente, nossos alunos.

A idéia dessa avaliação é nos permitir identificar melhor as habilidades dos candidatos à vaga de desenvolvedor fullstack. Esse desafio deve ser feito por você. Qualquer dúvida técnica relacionada ao teste, entre em contato com o avaliador.

A entrega deve ser feita por meio de um repositório publico aqui no github. Não se esqueça de criar um arquivo README.md na raiz de seu projeto com as instruções para utilização do seu projeto. Seguiremos extritamente essas instruções, por isso, tente deixar o mais claro e específico possível. Atente-se para o período de execução de seu teste. Ele estará explícito no email enviado por nossa equipe de Recursos Humanos.

>![Vida de Programador](https://vidadeprogramador.com.br/wp-content/uploads/2011/10/tirinha319.png)
>
>(FONTE: Vida de Programador. Disponível em: https://vidadeprogramador.com.br/wp-content/uploads/2011/10/tirinha319.png)

Nosso principal objetivo com essa avaliação é observar não só o estado atual da sua maturidade como desenvolvedor, mas também o quanto você pode crescer e como podemos ajudar você a conseguir isso. Por isso, lembre-se: Foque em entregar o máximo de pontos possível. Mesmo que não consiga completar tudo, envie o ponto em que chegar. Sabemos que a prova é muito grande, e é proposital! 

> ## Não deixe de nos mostrar seu trabalho!

------

## Pré-Enem dos Amigos

Um de nossos alunos quer, junto à amigos, crirar um cursinho pré-ENEM para ajudar os membros da comunidade dele a ingressarem na vida acadêmica. Nós, de pronto, apoiamos a ideia. Para ajudar na gestão do curso, nos propomos a desenvolver um pequeno sistema de cadastro dos alunos, horários das aulas e dos professores voluntário para as aulas. Nossa equipe já esta trabalhando em outras partes do sistema. Sua tarefa será desenvolver esse primeiro módulo: o cadastro de alunos, professores e turmas.

Para isso precisamos que os seguintes pontos sejam contemplados:

<ul>
  <li>
    De início, é preciso que exista ao menos um professor-administrador registrado no sistema para que os demais cadastros possam ser gerados.
  </li>
  <li>
    Cada aluno e professor precisam tem um perfíl de usuário único.
  </li>
  <li>
    Sendo um professor-administrador, é preciso que eu consiga cadastrar um novo aluno no sistema. Para isso, registrtarei obrigatoriamente:
    <ul>
      <li>Nome oficial</li>
      <li>Nome social</li>
      <li>
        Data de Nascimento
        <ul>
          <li>O aluno precisa ter mais de 16 anos completos.</li>
        </ul>
      </li>
      <li>
        Identificação de gênero
        <ul>
          <li>Homem.</li>
          <li>Mulher.</li>
          <li>Ambos.</li>
          <li>Nenhum.</li>
          <li>Prefiriu não informar.</li>
        </ul>
      </li>
      <li>
        Número do CPF
        <ul>
          <li>Precisa ser único.</li>
          <li>Precisa ser válido (http://www.macoratti.net/alg_cpf.htm).</li>
        </ul>
      </li>
      <li>
        CEP
        <ul>
          <li>Precisa ser válido (https://viacep.com.br).</li>
        </ul>
      </li>
    </ul>
    Opcionalmente registrarei:
    <ul>
      <li>
        Auto declaração de cor:
        <ul>
          <li>Afrodescendente</li>
          <li>Indígena</li>
          <li>Amarelo</li>
          <li>Negro</li>
          <li>Branco</li>
          <li>Preto</li>
          <li>Pardo</li>
        </ul>
      </li>
      <li>Observações textuais.</li>
    </ul>
  </li>
  <li>
    Sendo um professor-administrador, é preciso que eu consiga cadastrar um novo professor no sistema. Para isso, registrtarei obrigatoriamente: 
    <ul>
      <li>
        É Administrador?
        <ul>
          <li>Campo booleano</li>
          <li>Por padrão, marcado como falso</li>
        </ul>
      </li>
      <li>Nome oficial</li>
      <li>Nome social</li>
      <li>
        Data de Nascimento
        <ul>
          <li>O aluno precisa ter mais de 16 anos completos.</li>
        </ul>
      </li>
      <li>
        Identificação de gênero
        <ul>
          <li>Homem.</li>
          <li>Mulher.</li>
          <li>Ambos.</li>
          <li>Nenhum.</li>
          <li>Prefiriu não informar.</li>
        </ul>
      </li>
      <li>
        Número do CPF
        <ul>
          <li>Precisa ser único.</li>
          <li>Precisa ser válido (http://www.macoratti.net/alg_cpf.htm).</li>
        </ul>
      </li>
      <li>
        CEP
        <ul>
          <li>Precisa ser válido (https://viacep.com.br).</li>
        </ul>
      </li>
      <li>
        Graduação:
        <ul>
          <li>Graduand@</li>
          <li>Graduad@</li>
          <li>Especialista</li>
          <li>Mestrand@</li>
          <li>Mestre</li>
          <li>Doutorand@</li>
          <li>Doutor(a)</li>
          <li>Pós-Doutorand@</li>
          <li>Pós-Doutor(a)</li>
        </ul>
      </li>
      <li>
        Disciplina: (pode ser mais de uma)
        <ul>
          <li>Biologia</li>
          <li>Química</li>
          <li>Física</li>
          <li>História</li>
          <li>Geografia</li>
          <li>Filosofia</li>
          <li>Sociologia</li>
          <li>Língua Portuguesa</li>
          <li>Literatura</li>
          <li>Língua Inglesa</li>
          <li>Língua Espanhola</li>
          <li>Artes</li>
          <li>Educação Física</li>
          <li>Tecnologias da Informação e Comunicação</li>
          <li>Matemática</li>
          <li>Redação</li>
        </ul>
      </li>
    </ul>
    Opcionalmente registrarei:
      <ul>
        <li>
          Disponibilidade de horários para aula
          <ul>
            <li>Tipo de dado abstrato que representa a disponibilidade de horários de aula do professor durante cada um dos dias da semana. Sinta-se livre para propor a sua estrutura.</li>
          </ul>
        </li>
        <li>
          Email
          <ul>
            <li>Precisa ser válido</li>
          </ul>
        </li>
        <li>
          Telefone
          <ul>
            <li>Precisa ser válido</li>
          </ul>
        </li>
        <li>
          É WhatsApp?
          <ul>
            <li>Campo booleano</li>
            <li>Por padrão, marcado como falso</li>
          </ul>
        </li>
      </ul>
    </ul>
  </li>
  <li>
    Sendo um professor-administrador, é preciso que eu consiga cadastrar um novo horário de aula no sistema. Para isso, registrtarei obrigatoriamente:
    <ul>
      <li>Data Início das Aulas</li>
      <li>Data Término das Aulas</li>
      <li>Horário Início das Aulas</li>
      <li>Horário Término das Aulas</li>
      <li>Dias da Semana das Aulas</li>
      <li>Professor</li>
      <li>Disciplina</li>
      <li>Vagas da turma</li>
      <li>
        Horário ativo?
        <ul>
          <li>Campo booleano</li>
          <li>Por padrão, marcado como falso</li>
        </ul>
      </li>
    </ul>
  </li>
  <li>
    Sendo um professor-administrador, é preciso que eu consiga vincular professores aos horários de aula, respeitando:
    <ul>
      <li>Um professor não pode dar aula em dois horários que se sobreponham.</li>
      <li>Um professor não pode dar aula em mais que quatro horas por dia.</li>
      <li>Um professor não pode das aula em mais de duas disciplinas por dia.</li>
    </ul>
  </li>
  <li>
    Sendo um professor-administrador, é preciso que eu consiga vincular alunos aos horários de aula.
  </li>
  <li>
    Sendo um professor, é preciso que eu consiga visualizar, assim que acessar o sistema, uma listagem com todos os horários de aula vinculados à mim, com o dia da semana, horário de início, horário de término e disciplina.
  </li>
  <li>
    Sendo um professor, é preciso que eu consiga visualizar, assim que eu clicar sobre um horário, uma listagem com todos os alunos.
  </li>
  <li>
    Sendo um aluno, é preciso que eu consiga visualizar, assim que eu acessar o sistema, uma listagem com todos os horários de aula vinculados à mim, com o dia da semana, horário de início, horário de término e disciplina.
  </li>
  <li>
    Sendo um aluno, é preciso que eu consiga visualizar, assim que eu clicar sobre um horário, as informações do professor daquele horário, sendo nome social, graduação, telefone (caso cadastrado) e se é WhatsApp (caso cadastrado).
  </li>
</ul>

-----

## Entregas

Você precisará desenvolver o sistema em 3 partes: Backend, API REST, e Frontend. Para cada uma das partes, são requeridas algumas características, mas não se limite somente a elas. Mostre o máximo de features efetivamente funcionais que conseguir!

### BACKEND

O núcleo funcional do nosso sistema deverá ser desenvolvido em PHP 7+, considerando todas as boas práticas de desenvolvimento que achar importantes e em especial se atentando ao máximo as PHP Standard Recommendations (PSR). Esse backend deverá ser capaz de representar, modelar e tratar todos os dados envolvidos no sistema. É nele que as regras de negócios precisam estar implementadas e validadas. Os dados precisarão ser armazenados e recuperados de um banco de dados MySQL 5.5+ (indicamos a utilização da versão 5.7 por sua estabilidade). Atente-se à modelagem desse banco. Muitas vezes, um bom modelo de dados auxilia demais na implementação dos códigos.

### API REST

Toda a comunicação do aplicativo com suas diferentes instâncias precisará ser feita sob uma API REST privada. Os métodos precisarão representar a criticidade das informações e a segurança dos dados. Observer que para cada método existem operações conceitualmente já definidas.

### FRONTEND

A interface de visualização das informações precisará ser desenvolvida com tecnologias Javascript, CSS3 e HTML5. Indicamos fortemente a utilização do framework Vue.js e/ou Quasar. Utilizamos esses dois nos nossos produtos e a implementação com eles será um diferencial, porém, bons códigos serão sempre bem avaliados, sejam em qual estrutura for.

-----

## Não precisa reinventar a roda

Recomendamos fortemente a utilização de frameworks para cada uma das partes entregáveis para acelerar seu desenvolvimento. Fique a vontade para usar o que tem mais familiaridade. Nós, aqui, utilizamos frequentemente em nossos projetos para a UNIFAGOC e particulares Laravel, Slim, Lumen, Vue.js, React.js, Meteor.js, Sail entre outros.

-----

## Pontos de Avaliação

Nossa avaliação será bastante ampla. Não se preocupe em entregar todos os pontos perfeitos. Precisamos, primeiro, de entregas. Foque em blocos que você consegue desenvolver do início ao fim.

Iremos nos pautar pelos seguintes pontos:

* Arquivo README.md com as instruções para execução do sistema
* Legibilidade, facilide para modificação, eficiência e reusabilidade do código
* Orientação a Objetos
* Testes Automatizados (diferencial)
* Clean Code (diferencial)
* Object Calisthenics (diferencial)
* Princípios SOLID (diferencial)

-----
## Material de Apoio

Para qualquer dúvida, pode entrar em contato com nossa equipe pelo chat em http://comvoce.unifagoc.edu.br/.

Os links abaixo são apenas material para apoio aos seus estudos. Não se limite à eles. Explore as possibilidades e expanções dos conceitos.

* *PHP Standard Recommendations* - [clique aqui](https://www.php-fig.org/psr/)
* *Clean Code: Boas práticas para escrever códigos impecáveis* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/2-clean-code-boas-pr%C3%A1ticas-para-escrever-c%C3%B3digos-impec%C3%A1veis-361997b3c8b5)
* *Object Calisthenics* - [clique aqui](https://www.neoassist.com/2017/05/31/object-calisthenics-9-regras-para-aperfeicoar-seus-codigos/)
* *O que é SOLID: O guia completo para você entender os 5 princícipos da POO* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
* *Entenda o que é Rest API e a importância dela para o site da sua empresa* - [clique aqui](https://rockcontent.com/br/blog/rest-api/)

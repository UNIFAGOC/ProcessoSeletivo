# Processo Seletivo (#2)

Olá,

Inicialmente, gostaria de agradecer muito pela vontade de fazer parte da equipe da UNIFAGOC. Nós somos um centro universitário referência na zona da mata mineira. Nós, do Departamento de Tecnologia da Informação, desenvolvemos e mantemos os sistemas pertinentes à atividade da instituição. Temos como clientes os colaboradores do centro universitário, parceiros externos e, principalmente, nossos alunos.

A idéia dessa avaliação é nos permitir identificar melhor as habilidades dos candidatos à vaga de desenvolvedor fullstack. Esse desafio deve ser feito por você. Qualquer dúvida técnica relacionada ao teste, entre em contato com o avaliador.

A entrega deve ser feita por meio de um repositório publico aqui no github. Não se esqueça de criar um arquivo README.md na raiz de seu projeto com as instruções para utilização do seu projeto. Seguiremos extritamente essas instruções, por isso, tente deixar o mais claro e específico possível. Você terá 15 dias para execução de seu teste a contar da hora de envio deste material para seu email por nossa equipe de Recursos Humanos.

>![Vida de Programador](https://vidadeprogramador.com.br/wp-content/uploads/2011/10/tirinha319.png)
>
>(FONTE: Vida de Programador. Disponível em: https://vidadeprogramador.com.br/wp-content/uploads/2011/10/tirinha319.png)

Nosso principal objetivo com essa avaliação é observar não só o estado atual da sua maturidade como desenvolvedor, mas também observar o quanto você pode crescer e como podemos ajudar você a conseguir isso. Por isso, lembre-se: Precisamos ver o máximo de módulos funcionais possíveis. 

> #### Não deixe de nos mostrar seu trabalho!

------

## Mudanças no mercado à caminho

Desde outubro de 2020, o mercado financeiro brasileiro vem sendo balançado pela iniciativa de integração tecnológica promovida pelo Banco Central (BaCen). O lançamento do PIX, método de pagamento instantâneo, vem mudando a forma com que as pessoas interagem com as empresas prestadoras de serviços, comércio e indústrias. Já não é incomun a possibilidade de pagamento de nossas compras na Internet utilizando a nova ferramenta.

Na esteira do PIX, o BaCen agora propõe a implementação do _open banking_, uma plataforma institucional de compartilhamento de informações entre instituições financeiras, fintechs e bancos. Para saber um pouco mais, sugiro [esta matéria da InfoMoney](https://www.infomoney.com.br/guias/open-banking/).

Nosso disafio envolverá um protótipo dessa plataforma. 

## Do contexto e propostas

Para nossa prova de conceito, desenvolveremos uma plataforma online com controle de acesso por usuário e senha. As entidades envolvidas na plaraforma serão:

<a href="https://github.com/UNIFAGOC/ProcessoSeletivo/raw/master/assets/imagem1.png" target="_blank">
<img alt="imagem1" src="https://github.com/UNIFAGOC/ProcessoSeletivo/raw/master/assets/imagem1.png" height="400"/>
</a>

### Clientes

Esta entidade trará as informações pessoais sobre os proprietários da contas bancárias. Serão elas:

* **CPF** - Cadastro de Pessoa Física segundo padrão definido pela Receita Federal de 11 dígitos. Outras informações 
  podem ser localizadas [aqui](https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas)
* **Nome** - Nome da pessoa em texto, validado pela expressão regular disponibilizada [aqui](https://pt.stackoverflow.com/a/243008)
* **Endereço** - Descrição completa do endereçamento do cliente, com logradouro, número, complemento, bairro, cidade e 
  unidade federativa.
* **Data de Nascimento** - Data representada seguindo o padrão ISO 8601. Mais informações [aqui](https://en.wikipedia.org/wiki/ISO_8601)

### Instituição Financeira

Esta entidade trará as informações sobre as instituições registradas no Banco Central. 

* **CNPJ** - Candastro Nascional de Pessoas Jurídicas segundo padrão da Receita Federal de 14 dígitos. Outras informações podem ser localizadas [aqui](https://pt.wikipedia.org/wiki/Cadastro_Nacional_da_Pessoa_Jur%C3%ADdica)
* **Razão Social** - Nome único das empresas mediante as entidades fiscais.
* **Nome Fantasia** - Nome divulgado pelas empresas. Similar às marcas ou produtos. A título de exemplo, o Banco do Brasil (nome fantasia) tem por razão social "Banco do Brasil S.A.".
* **Código Bancário** - Cada instituição financeira que opera no Brasil possui um código identificador único. Alguns 
  desses valores podem ser localizados [aqui](https://contasimples.com/blog/lista-de-codigos-dos-bancos/)
* **Logomarca** - Identificação visual do banco. Pode-se utilizar uma imagem padrão, caso seja necessário.  

### Usuários

* **Login** - Nome único de identificação dos usuários dentro do sistema.
* **Senha** - Senha de acesso ao sistema. Deve ser criptografada em base64 para persistência no banco de dados. 
  Precisa apresentar o seguinte grau de complexidade:
  * Ao menos 6 caracteres
  * Ao menos 1 letra maiúscula
  * Ao menos 1 letra minúscula
  * Ao menos 1 dígito
  * Ao menos um caracter especial dentre: ( ) # @ ! ?
* **Tipo** - Os usuários do sistema podem ser de dois típos: Clientes ou Instituições. As regras de negócio 
  pertinentes a cada um serão descritas a frente.
* **Entidade** - Relacionamento com a entidade correspondente ao campo **Tipo**.
* **Ativo** - Campo booleano, com valor padrão `false` que limita o acesso dos usuários ao sistema. Esse limite 
  aplica-se apenas a usuários com `Tipo = Instituição`

### Contas

* **Identificador Único** - Afim de simplificar nosso protótipo, as contas bancárias serão representadas por 
  identificadores únicos e incrementais. Não é preciso verificar e/ou validar dígitos.
* **CPF do Cliente** - Relacionamento com a entidade Clientes
* **CNPJ da Instituição Financeira** - Relacionamento com a entidade Instituição Financeira
* **Saldo** - Valor monetário do saldo da conta em Reais. Atentar à representação e casas decimais pertinentes.
* **Data de Abertura** - Data de criação do registro da conta, automaticamente preenchida. Seguir padrão ISO 8601.
* **Data de Encerramento** - Data de fechamento da conta. Quando não encerrada, guardar valor `null`. Seguir padrão ISO 
  8601

### Produtos Financeiros

* **Identificador Único** - Identificador único, incremental, iniciando pelo valor `100000`
* **CNPJ da Instituição Financeira** - Relacionamento com a entidade Instituição Financeira
* **Descrição** - Campo em texto descrevendo o produto ofertado.
* **Valor Mínimo** - Valor monetário mínimo para acesso ao produto. Validar em confronto com o saldo na conta do 
  Cliente. Atentar para representação e casas decimais pertinentes.
* **Taxa de Administração** - Valor percentual cadastrado pela instituição com 4 algarismos significativos ([ver 
  aqui](https://pt.wikipedia.org/wiki/Algarismo_significativo)). Atentar para 
  representação e casas decimais pertinentes.

### Contratos

* **Identificador Único** - Identificador único e incremental
* **Número da Conta** - Relacionamento com a entidade Contas
* **Identificador do Produto Financeiro** - Relacionamento com a entidade Produto Financeiro
* **Valor Investido** - Valor montário utilizado na contratação do produto.
* **Taxa de Administração** - Valor percentual da taxa de administração. Deve sempre ser menor ou igual ao valor 
  registrado no campo relativo da entidade Produto Financeiro.
* **Data de Contratacao** - Data de assinatura do contrato. Sempre igual ou superior à data de abertura da conta. 
  Usar padrão ISO 8061.
* **Finalizado** - Indicador booleano de contrato devidamente quitado ou não.

### Compartilhamentos

Entidade que descreve a permissão pelo Cliente do compartilhamento do histórico de Contratos firmados entre uma 
determinada Instituição Financeira de àquele. Esse compartilhamento se dará por transferência de arquivo XML, a 
seguir definido.

* **CPF do Cliente** - Relacionamento com a entidade Cliente
* **CNPJ da Instituição de Origem** - Relacionamento com a entidade Instituição Financeira.
* **CNPJ da Instituição de Destino** - Relacionamento com a entidade Instituição Financeira.
* **Data do Aceite** - Data de aceite do compartilhamento de dados entre as instituições pelo cliente. Usar padrão 
  ISO 8061.
* **Ainda vigente** - Campo não persistido que indica se o compartilhamento de informações ainda pode ser acessado 
  pelas instituições.

#### XML de compartilhamento

O arquivo XML de compartilhamento de informações precisa seguir o seguinte XSD (Extended Markup Language Schema 
Definition):

``` xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="compartilhamento">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="cliente">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="cpf" />
              <xs:element name="nome" />
              <xs:element name="endereco" />
              <xs:element name="dataNascimento" />
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="contas">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="conta">
                <xs:complexType>
                  <xs:attribute name="identificador" type="xs:string" use="required" />
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="produtos">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="produto">
                <xs:complexType>
                  <xs:attribute name="dentificador" type="xs:string" use="required" />
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="contratos">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="contrato">
                <xs:complexType>
                  <xs:attribute name="dentificador" type="xs:string" use="required" />
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

Esse arquivo deve ser gerado no servidor de arquivos da aplicação, não sendo necessárias transmissões.

## Das regras de negócio

Sinta-se a vontade para apresentar regras que lhe façam sentido, mas tenha em mente os seguintes pontos:

* Somente usuário ativos podem acessar a plataforma
* Os registros de usuários são únicos para cada cliente.
* Uma mesma instituição financeira pode ter vários usuários cadastrados e vinculados à/por ela.
* Usuários do tipo "Cliente", uma vez ativados, sempre permanecerão ativos.
* Usuários do tipo "Cliente" podem autorizar, visualizar e encerrar compartilhamentos de dados próprios.
* Usuários do tipo "Cliente" podem autorizar e visualizar contratos de suas contas.
* Usuários do tipo "Instituição" podem cadastrar, visualizar compartilhamentos de dados.
* Usuários do tipo "Instituição" podem cadastrar, visualizar, editar e deletar clientes
* Usuários do tipo "Instituição" podem ativar usuários do tipo "Cliente" se, e somente se, esses possuírem contas para àquela instituição financeira.
* Usuários do tipo "Instituição" podem cadastrar, visualizar, editar e encerrar contas da instituição a qual pertence.
* Usuários do tipo "Instituição" podem cadastrar, visualizar, editar e deletar produtos financeiros.
* Usuários do tipo "Instituição" podem cadastrar, visualizar, editar, deletar e encerrar contratos.

* Clientes devem ter o CPF válido segundo termos já descritos anteriormente
* Clientes devem ter ao menos 16 (dezesseis) anos completos no momento de cadastro no sistema

* Instituições Financeiras precisam ter o CNPJ válido segundo termos já descritos anteriormente
* Instituições Financeiras precisam ter o Código Bancário único entre elas

* Conta não pode ter saldo inferior a 0 (zero) reais. 
* Conta precisa ter a data de abertura igual à data de registro. Não é permitido registros pretéritos ou futuros.
* Ao se encerrar uma conta, a data de encerramento precisa ser a data atual. Não é permitido registros pretéritos ou futuros.

* Produtos Financeiros precisam ter o identificador único, incremental, iniciando pelo valor `100000`
* Produtos Financeiros precisam ter valor mínimo maior que 0 (zero) reais
* Produtos Financeiros precisam ter taxa de administração entre 0 (zero) e 100 (cem) por cento, respeitando os critérios já descritos.
* Produtos Financeiros precisam ser únicos dentro de uma instituição em descrição, valor mínimo e taxa de administração.

* Contratos precisam ser autorizados pelo Cliente antes de serem debitados das contas daqueles.
* Contratos autorizados não podem mais ser editados ou deletados.
* Ao se tentar contratar um serviço não havendo saldo, o contrato precisa ser negado e o cliente alertado da falta de saldo.

* Compartilhamentos precisam ser aceitos pelos usuários tipo "Clientes" antes da geração dos arquivos de transmissão de informações (XML)
* Compartilhamentos encerrados precisam ter efeito imediato sobre o sistema.

## Das entregas

Você precisará desenvolver o sistema em 3 partes: _Backend_, _API REST_, e _Frontend_. Para cada uma das partes, são requeridas algumas características, mas não se limite somente a elas. Mostre o máximo de features efetivamente funcionais que conseguir!

### Backend

O núcleo funcional do nosso sistema deverá ser desenvolvido em PHP 7+, considerando todas as boas práticas de desenvolvimento que achar importantes e em especial se atentando ao máximo as PHP Standard Recommendations (PSR). Esse backend deverá ser capaz de representar, modelar e tratar todos os dados envolvidos no sistema. É nele que as regras de negócios precisam estar implementadas e validadas. Os dados precisarão ser armazenados e recuperados de um banco de dados MySQL 5.5+ (indicamos a utilização da versão 5.7 por sua estabilidade). Atente-se à modelagem desse banco. Muitas vezes, um bom modelo de dados auxilia demais na implementação dos códigos.

### API REST

Toda a comunicação do aplicativo com suas diferentes instâncias precisará ser feita sob uma API REST privada. Os métodos precisarão representar a criticidade das informações e a segurança dos dados. Observer que para cada método existem operações conceitualmente já definidas.

### Frontend

A interface de visualização das informações precisará ser desenvolvida com tecnologias Javascript, CSS3 e HTML5. Indicamos fortemente a utilização do framework [Vue.js](https://vuejs.org/) e/ou [Quasar](https://quasar.dev/). Utilizamos esses dois nos nossos produtos e a implementação com eles será um diferencial, porém, bons códigos serão sempre bem avaliados, sejam em qual estrutura for. 

## Ambiente de Desenvolvimento e Entrega

O sistema deve ser implementado sobre um container Docker e seus arquivos de configuração (Dockerfile e/ou docker-compose.yml) precisam estar disponíveis no repositório a ser apresentado. Mais uma vez, é imprecindível que no arquivo README.md, na raiz do projeto, esteja bem definida todas as informações necessárias para a execução do projeto.

Recomendamos fortemente a utilização de frameworks para cada uma das partes entregáveis para acelerar seu desenvolvimento. Fique a vontade para usar o que tem mais familiaridade. Nós, aqui, utilizamos frequentemente em nossos projetos para a UNIFAGOC e particulares Laravel, Slim, Lumen, Vue.js, React.js, Meteor.js, Sail entre outros. 


>![](https://vidadeprogramador.com.br/wp-content/uploads/2012/04/tirinha520.png)
>
>(FONTE: Vida de Programador. Disponível em: https://vidadeprogramador.com.br/wp-content/uploads/2012/04/tirinha520.png)

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

Para qualquer dúvida, estaremos à disposição no Telegram

https://t.me/joinchat/tuh90ZFpbwBmZGUx

<a href="https://t.me/joinchat/tuh90ZFpbwBmZGUx" target="_blank">
<img alt="telegram" src="https://raw.githubusercontent.com/UNIFAGOC/ProcessoSeletivo/master/assets/imagem2.png" height="400"/>
</a>

-----
## Material de Apoio

Os links abaixo são apenas material para apoio aos seus estudos. Não se limite à eles. Explore as possibilidades e expanções dos conceitos.

* *PHP Standard Recommendations* - [clique aqui](https://www.php-fig.org/psr/)
* *Clean Code: Boas práticas para escrever códigos impecáveis* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/2-clean-code-boas-pr%C3%A1ticas-para-escrever-c%C3%B3digos-impec%C3%A1veis-361997b3c8b5)
* *Object Calisthenics* - [clique aqui](https://www.neoassist.com/2017/05/31/object-calisthenics-9-regras-para-aperfeicoar-seus-codigos/)
* *O que é SOLID: O guia completo para você entender os 5 princícipos da POO* - [clique aqui](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
* *Entenda o que é Rest API e a importância dela para o site da sua empresa* - [clique aqui](https://rockcontent.com/br/blog/rest-api/)

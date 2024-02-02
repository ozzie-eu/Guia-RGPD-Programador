# Ficha n°2: Preparar o desenvolvimento

#### Os princípios da proteção de dados pessoais tem de ser integrados nos desenvolvimento de TI desde a fase de conceção e seguintes, para proteger a privacidade das pessoas a que pertencem os dados que vão ser tratados, dando-lhes assim mais controlo sobre os mesmos e limitando os erros, extravios, alteraçõs indevidas ou mau uso desses dados nas aplicações.

## Opções Metódicas

* **Colocar a proteção da privacidade no centro do desenvolvimento** adotando um método de [Privacidade desde a conceção](https://edpb.europa.eu/our-work-tools/public-consultations-art-704/2019/guidelines-42019-article-25-data-protection-design_en).

* Se houver recurso a metodologias Agile para os desenvolvimentos, considerar **integrar a segurança ao centro dos procedimentos**. A ANSSI disponibiliza um guia ["Segurança digital e Agilidade"](https://www.ssi.gouv.fr/uploads/2018/11/guide-securite-numerique-agile-anssi-pa-v1.pdf) (apenas em Francês) que mostra como realziar os desenvolvimentos dentro das ferramentas de uma metodologia Agile enquanto se leva também em conta os aspectos de segurança. Não hesitar em procurar inspiração neste documento.

* Para qualquer desenvolvimento que vise o público em geral, **considere a parametrização da privacidade**, e em particular os parâmetros por defeito, tais como as caraterísticas e conteúdos do utilizador visíveis por omissão.

* **Realizar uma [Análise de Impacto na Proteção de Dados (AIPD)](https://www.cnil.fr/en/privacy-impact-assessment-pia)**. Para [um leque de operações](https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/accountability-and-governance/data-protection-impact-assessments/) é obrigatório. Noutros casos é uma boa prática que permitirá identificar e gerir os potenciais riscos durante os desenvolvimentos. A CNIL tem uma secção especial no seu website e providencia um [software livre](https://www.cnil.fr/en/open-source-pia-software-helps-carry-out-data-protection-impact-assesment) dedicado a este tipo de análise.


## Opções Tecnológicas

#### Arquitetura e Funcionalidades

* **Incluir proteção de privacidade, incluir requisitos de segurança de dados, na fase de conceção da aplicação ou serviço**. Estes requisitos devem influenciar [as opções de arquitetura](05-Escolha-informada-da-arquitetura) (ex: distribuído vs. centralizado) ou funcionalidades (ex: anonimização a curto prazo, minimização de dados). Os parâmetros por defeito da aplicação devem cumprir com requisitos mínimos de segurança e estar em conformidade com a Lei. Por exemplo, a complexidade por defeito das passwords deve obedecer no mínimo à [recomendação da CNIL sobre esse aspecto](https://www.cnil.fr/fr/node/23803).

* **Manter controlo sobre o sistema**. É importante manter o controlo do sistema, tanto para assegurar a operacionalizaçaõ adequada como para garantir o elevado nível de segurança. Manter um sistema simples permite compreender precisamente como funciona e identificar os seus pontos fracos. Se um certo grau de complexidade for requerido, é aconselhável comocçar com um sistema simples, seguro e corretamente desenhado. Então, será possivel aumentar a complexidade incrementalmente, enquanto se continuaa a adicionar novas funcionalidades com garantia de segurança.

* **Não contar com uma linha única de defesa**. Apesar de todos os passos tomados para conceber um sistema seguro, pode acontecer que alguns componentes adicionado posteriormente não estejam suficientemente seguros. Para minimizar o risco nos utilizadores finais, é aconselhável defender o sistema em profundidade. Por examplo, conferir os dados introduzidos num formulário online faz parte das defesas periféricas. Se essa defese for ultrapassada, proteção a nível de instruções na base de dados pode entrar em ação.

#### Ferramentas e Práticas

* **Usar normas de programação que levam em conta a segurança**. Frequentemente, listas de normas, melhores práticas ou guias de código quer melhoram a segurança nos desenvolvimentos já existem disponíveis. Ferramentas auxiliares também podem ser incorporadas nos ambientes integrados de desenvolvimento ("**IDE**") por forma a validar automáticamente que o código-fonte cumpre com as diversas regras que são parte das normas ou boas práticas. São fácilmente obtidas listas de boas práticas para diversas linguagens de programação na Internet. Por exemplo [aqui](https://wiki.sei.cmu.edu/confluence/display/seccode/SEI+CERT+Coding+Standards) para C, C++ or Java. PAra desenvolvimento de aplicações Web, existem guias específicos de boas práticas, comom os publicados pela [OWASP](https://www.owasp.org).

* **As opções tecnológicas são críticas.** Alguns parâmetros têm de ser considerados:
    * Dependendo do campo da aplicação ou funcionalidade desenvolvida, uma linguagem ou tecnologia pode ser mais apropriada do que outra.
    * Linguagens e tecnologias mais maduras são mais seguras. Foram, no geral, escrutinadas para corrigir as vulnerabilidades mais conhecidas. No entanto, há que ter cautela no uso das versões mais recentes de cada um dos blocos tecnólogicos com que se constroi a solução.
    * Deve ser evitado programar a solução final numa linguagem em que os programadores não têm experiência suficiente e ainda não dominaram. Caso contrário, há maior exposição ao risco de uma falha de segurança devido à falta de experiência.
* **Montar um ambiente de desenvolvimento seguro que permita versionamento do código** seguinte [a ficha dedicada](03-Seguranca-do-ambiente-de-desenvolvimento.md) apresentada neste guia.

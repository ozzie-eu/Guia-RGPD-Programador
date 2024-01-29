# Ficha n°1: Identificar dados pessoais

#### Compreender as noções de "dados pessoais", "finalidades" e "tratamento" é essencial para assegurar que o software está conforme a lei quando trata dados do utilizador. Em particular, há que ter cautela para não confundir "anonimização" e "pseudonimização", que têm definições muito precisas e diferentes no RGPD.

## Definição
* O conceito de **dadso pessoais** está definido no [RGPD](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32016R0679) como "[qualquer informação relativa a uma pessoa singular identificada ou identificável (referida como "titular dos dados")](https://www.cnil.fr/en/personal-data-definition)". Fica coberto um âmbito amplo qur inclui dados que identificam diretamente (ex: primeiro e último nome) e dados que identificam indiretamente (ex. número telefone, matrícula de automóvel, identificador de equipamento, etc).

* Qualquer tratamento sobre este tipo de dados (recolha, gravação, transmissão, modificação, disseminação, etc.) constitutui **tratamento no enquadramento do RGPD** e portanto deve cumprir os requisitos estabelecidos por esse regulamento. Tais operações de tratamento devem ser lícitas e terem finalidades claramente definidas. Os dados pessoais recolhidos e tratados têm de ser relevantes e limitados aos estritamente necessários para atingir os objetivos.

## Exemplos de dados pessoais

* Quando dizem respeito a pessoas singulares, **estes tipos de dados são dados pessoais**:
    * apelido, nome, alcunha, data de nascimento;
    * fotos, gravações de voz;
    * contactos telefónicos fixos ou móveis, emndereço postal, endereço correio eletrónico;
    * Endereço IP, identificador de ligação de rede ou cookie identificativo;
    * Impressão digital, palma da mão ou respetiva rede de vasos, retina;
    * Matrícula de veículo, número da segurança social, número de identificação civil;
    * Dados de utilização de aplicações, comentários, etc...

* **Identificação de uma pessoa singular pode ser realizada**:
    * A partir de uma única fonte de dados (examplo: nome e apelido);
    * A partir do cruzamento de conjuntos de dados (examplo: uma pessoa do sexo feminino a viver em determinada morada, com uma data de nascimento fornecida e associada de uma dada organização).

* Alguns dados são considerados **particularmente sensíveis**. O RGPD proibe a recolha ou utilização destes dados, a não ser, em particular, que todos os titulares dos dados envolvidos tenham dado o seu consentimento expresso (ativo, explícito e preferencialmente escrito, que deve ser livre, específico e informado).

* Estes requisitos aplicam-se aos seguintes dados:

    * Dados relativos à **saúde de indivíduos**;
    * Dados relativos à **vida sexual** ou **orientação sexual**;
    * Dados reveladores de origem **racial** ou **étnica**;
    * Opiniões políticas, crenças religiosas, crenças filosóficas ou afiliações sindicais;
    * Dados **genéticos** ou **biométricos usados com o único propósito de identificar um indivíduo**.

## Anonimização de dados pessoais

* Um **processo de anonimização de dados pessoais** visa tornar impossivel a identificação de indivíduos dentro de conjuntos de dados. É portanto um processo irreversível. Quando esta anonimização é eficaz, a informação deixa de ser considerada como dados pessoais e os requisitos do RGPD já não se aplicam.

* Por omissão, recomenda-se que **nunca se considerem dados originais como anónimos**. Anonimização resulta de um tratamento de dados pessoais para que impeça de forma irreversível a identificação, seja por:

    * _destaque_: não é possivel destacar alguns ou todos os registos que identificam um individuo no conjunto de dados;
    * _associação_: o conjunto de dados não permite associar dois ou mais registos que dizem respeito ao mesmo titular de dados ou grupo de titulares;
    * _inferencia_:  não é possivel inferir,  com alta probabilidade, o valor de um atributo do titular dos dados com base no conjunto de outros atributos do titular.

* Estas operações de tratamento de dados implicam na maioria dos casos uma **perda de qualidade no conjunto de dados produzido**. A [opinião sobre técnicas de anonimização](https://ec.europa.eu/justice/article-29/documentation/opinion-recommendation/files/2014/wp216_en.pdf) do grupo de trabalho do Artigo 29 (Art. 29 WP) descreve as pricipais técnicas em uso presentemente, assim como providencia exemplos de conjuntos de dados erradamente considerados anónimos. É importante a ressalva de que as técnicas de anonimização têm insuficiências. A escolha de anonimizar ou não os dados, além da escolha da respectiva técnica, deve ser realizada casuisticamente, de  acordo como os diferentes contextos do uso pretendido (natureza dos dados, sua utilidade, riscos para os titulares, etc.).

## Pseudonimização de dados pessoais

* **Pseudonimização é um compromisso entre reter dados originais enquanto se produzem conjuntos anonimizados**.

* O procedimento refere-se ao tratamento de dados pessoais de um modo que **dados relativos a uma pessoa singular deixam de poder ser atribuidos sem estar num contexto com informaçaõ adicional**. O RGPD insiste que esta informação adicional deve ser mantida separadamente e sujeita a medidas técnicas e organizacionais que evitem a re-identificação dos titulares dos dados. Ao contrário da anonimização, pseudonimização pode ser um processo reversível.

* Na prática, o processo da pseudonimização consiste em **substituir atributos diretamente identificativos (apelido, nome, etc.) num conjunto, por dados de identificação indireta** (pseudónimo, número de um sistema de arquivo, etc.) por forma a reduzir o nível de sensibilidade da informação. Os dados podem resultar de uma hash de cifra a partir dos dados do titulares, como o seu endereço IP, nome de utilizador, endereço de e-mail.

* Dados resultantes de pseudonimização são considerados como **dados pessoais e portanto permanecem sujeitos às obrigações do RGPD**. No entanto, o regulamento Europeu encoraja o uso da pseudonimização no tratamento de dados pessoais. Além disso, o RGPD considera que a pseudonimização torna possivel a redução dos riscos para os titulares dos dados e contribui para a conformidade com o regulamento.

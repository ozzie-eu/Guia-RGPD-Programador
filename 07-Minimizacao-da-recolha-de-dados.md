# Ficha n°7: Minimização da recolha de dados

#### Você deve coletar apenas os dados pessoais que sejam adequados, relevantes e necessários em relação aos propósitos para os quais são processados, conforme definido no momento da coleta.

## Antes da coleta, pense nos diferentes tipos de dados que você precisa coletar e tente limitar sua coleta ao que é estritamente necessário.

* Pense nos diferentes **tipos de dados** que precisarão ser coletados antes de implementar uma aplicação e **documente** esse raciocínio.

* Se dados específicos não forem **necessários para uma determinada categoria de pessoas**, não os colete.

* Processe e armazene os dados de uma forma que **reduza a precisão** (semelhante à pseudonimização). Por exemplo, armazene apenas o ano de nascimento em vez de uma data de nascimento completa, se a aplicação precisar apenas do ano.

* Se estiver coletando dados particularmente sensíveis, como dados de saúde ou condenações criminais, certifique-se de coletar apenas o **mínimo necessário**. Devido às restrições regulatórias, a solução mais simples ainda é **não coletá-los** se puder prescindir deles.

* Minimize a quantidade de dados coletados também nos **dados de log** e não armazene dados sensíveis ou críticos (dados de saúde, senhas, etc.).

* Algumas funcionalidades podem melhorar a experiência do usuário, mas **não são estritamente necessárias para o funcionamento adequado da sua aplicação** (por exemplo, geolocalização para simplificar uma busca geográfica). Nesse caso, o usuário final deve poder **escolher se deseja ou não usar** essa funcionalidade. Se ele a utilizar, os dados que você precisar coletar para seu funcionamento devem ser mantidos apenas pelo tempo estritamente necessário para sua operação e nunca usados para outros fins.

* Lembre-se de associar **períodos de retenção** para cada categoria de dados, dependendo do propósito do processamento e das obrigações legais ou regulatórias relacionadas à sua retenção. Logs também devem ter um período de retenção. Documente as durações de retenção definidas. Você precisará ser capaz de justificá-las.

## Uma vez que os dados tenham sido coletados, configure mecanismos automáticos de exclusão.

* Implemente um sistema automático de **purga** ao final do período de vida útil. Você também pode realizar revisões manuais dos dados armazenados periodicamente.

* Para garantir a exclusão completa, apague **fisicamente** todos os dados que não são mais necessários usando ferramentas especializadas ou destruindo os meios físicos.

* Se os dados ainda forem úteis, você pode reduzir sua sensibilidade usando métodos de **pseudonimização** ou até mesmo de **anonimização**. No caso de pseudonimização, esses dados continuam sujeitos às regulamentações sobre dados pessoais (veja [Ficha 1](#Ficha_n°1_:_Identificar_dados_pessoais)).

* Registre os **procedimentos de exclusão automática**. Os logs correspondentes podem ser usados como uma **prova de exclusão** de um item de dado. data collection


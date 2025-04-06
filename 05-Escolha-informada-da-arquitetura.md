# Ficha n°5: Escolha informada da arquitetura

#### Ao projetar a arquitetura da sua aplicação, você deve identificar os dados pessoais que serão coletados e definir um caminho e ciclo de vida para cada um deles. A escolha dos ativos de suporte (armazenamento local, servidor, serviço em nuvem) é uma etapa crucial, que deve ser adaptada às suas necessidades, mas também ao seu conhecimento técnico. O registro e a condução de uma avaliação de impacto sobre a privacidade podem auxiliá-lo nessa escolha.

## Examinando o ciclo de vida dos dados e processos, desde a coleta até a exclusão

* Represente e descreva como o produto funciona de forma geral antes de iniciar seu projeto, com um diagrama de fluxos de dados e uma descrição detalhada dos processos realizados.

* Quando os dados são apenas **armazenados no terminal do usuário** (armazenamento local) ou permanecem **confinados em redes de comunicação sob o controle do usuário** (por exemplo, Wi-Fi ou outra rede local), o principal ponto de atenção é a segurança dos dados. A duração do armazenamento e a exclusão efetiva devem ser determinadas pelos indivíduos.

* **Quando os dados transitam por serviços online**, a escolha de hospedar os dados você mesmo ou usar um provedor de serviços deve ser feita de acordo com seu conhecimento de segurança e a qualidade de serviço esperada. Ofertas reconhecidas de nuvem podem oferecer níveis mais altos de segurança. No entanto, elas geram novos riscos que precisam ser dominados. [Recomendações para empresas que planejam usar serviços de computação em nuvem](https://www.cnil.fr/sites/default/files/typo/document/Recommendations_for_companies_planning_to_use_Cloud_computing_services.pdf) podem orientar nesta etapa de seleção.

## Em caso de uso de hospedagem externa

* **Escolha um provedor de serviços que garanta medidas adequadas de segurança e confidencialidade e seja suficientemente transparente**.

* **Certifique-se de conhecer a localização geográfica dos servidores que hospedarão seus dados**. Pode ser necessário transferir dados para fora da União Europeia (UE) e do Espaço Econômico Europeu (EEE). Embora os dados possam circular livremente dentro da UE/EEE, transferências para fora da UE/EEE são possíveis, desde que seja garantido um nível suficiente e apropriado de proteção de dados. A CNIL fornece um mapa no site mostrando os [diferentes níveis de proteção de dados nos países ao redor do mundo](https://www.cnil.fr/en/data-protection-around-the-world).

* **Se você precisar hospedar dados de saúde**, certifique-se de que o provedor utilizado seja [certificado](https://esante.gouv.fr/labels-certifications/hds/liste-des-herbergeurs-certifies) ou [aprovado](https://esante.gouv.fr/labels-certifications/hds/liste-des-herbergeurs-agrees) para essa atividade.

* Outros pontos a serem observados incluem:
    - a existência de uma política de segurança acessível;
    - medidas de segurança física e proteção no local de hospedagem;
    - criptografia de dados e outros processos para garantir que o provedor não tenha acesso aos dados confiados a ele;
    - a gestão de atualizações, a gestão de autorizações, a autenticação de pessoal e a segurança dos desenvolvimentos de aplicações;
    - a fácil reversibilidade/portabilidade dos dados em um formato estruturado e comumente usado, mediante solicitação e a qualquer momento. an informed choice of architecture


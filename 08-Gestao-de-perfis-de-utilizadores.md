Ficha n°8: Gerir perfis de utilizadores
#### A forma de gerir os perfis dos seus colaboradores e dos seus utilizadores finais deve ser pensada antecipadamente ao desenvolvimento. Consiste em definir diferentes perfis de acesso e autorização para que cada pessoa possa acessar apenas os dados que realmente necessita.


## Boas práticas para gestão de utilizadores 

* Tudo começa com o **uso de identificadores únicos e individuais**, sejam eles utilizadores da sua aplicação ou colaboradores no desenvolvimento.

* Certifique-se de **impor autenticação** antes de qualquer acesso a dados pessoais, de acordo com as [recomendações da CNIL](https://www.cnil.fr/en/passwords-minimum-security-recommendations-businesses-and-citizens).

* Para garantir que cada pessoa (utilizador ou colaborador) possa acessar apenas aos **dados que realmente necessita**, o seu sistema deve fornecer **políticas de gestão de acesso diferenciadas** (leitura, escrita, exclusão, etc.) de acordo com as pessoas e necessidades. Um mecanismo global de gestão de perfis de utilizadores permitirá agrupar diferentes direitos de acordo com um papel exercido por um grupo de utilizadores dentro da aplicação.

* A gestão de perfis de utilizadores pode ser usada juntamente com **sistemas de registo de atividades para rastrear atividades e detetar anomalias ou eventos relacionados à segurança**, como acessos fraudulentos e uso indevido de dados pessoais. Estes dispositivos não devem ser usados para qualquer outro propósito além de garantir o uso adequado do sistema informático. Os registos também não devem ser mantidos por mais tempo do que o necessário. Em geral, um período de seis meses é adequado.

* Pode também planear auditorias de código ou testes de penetração no seu ambiente de desenvolvimento para **garantir a robustez do seu sistema de gestão de perfis**.

## Simplifique a gestão de perfis de autorização

* Planeie **documentar ou automatizar a movimentação dos seus colaboradores**. Por exemplo, esses procedimentos devem orientar as ações a serem tomadas quando as pessoas não estão mais autorizadas a acessar uma sala ou um recurso de TI, ou no final do seu contrato.

* Gerir os seus utilizadores e colaboradores implica **uma revisão regular das permissões** de acordo com a evolução dos usos e movimentos organizacionais dentro do seu projeto. O uso de serviços de diretório, como o _Lightweight Directory Access Protocol_ (_LDAP_), ajudará a monitorizar essas mudanças e permitirá refinar as suas estratégias de acesso, por exemplo, atribuindo papéis com base em perfis de uso. Isso permite respeitar melhor o princípio do menor privilégio.


* O uso de contas "supremas" (tipo _root_, administrador, etc.) deve ser evitado para operações convencionais, pois constitui a pedra angular do seu sistema e um alvo privilegiado para um possível atacante externo. Recomendamos que associe uma política de senha forte a essas contas (10 a 20 caracteres ou multi-fator) e que limite o número de pessoas com conhecimento delas ao estritamente necessário.


* **Favoreça o uso de um gestor de senhas no seu projeto** e a transição para autenticação forte sempre que possível. Evite contas genéricas compartilhadas por várias pessoas. 

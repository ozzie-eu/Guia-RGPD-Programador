# Ficha n°6: Aplicar segurança nos websites, aplicações e servidores

#### Qualquer website, aplicação ou servidor deve incorporar regras básicas de segurança de última geração, não apenas nas comunicações de rede, mas também na autenticação e na infraestrutura.

## Protegendo redes de comunicação

* **Implemente TLS versão 1.2 ou 1.3** (substituindo o SSL) em todos os websites e para transmissões de dados de suas aplicações móveis, por exemplo, com [LetsEncrypt](https://letsencrypt.org/fr/), utilizando apenas as versões mais recentes e verificando sua correta implementação.

* **Torne obrigatório o uso de TLS** para todas as páginas do seu site e para suas aplicações móveis.

* **Limite as portas de comunicação** estritamente necessárias para o funcionamento adequado das aplicações instaladas. Se o acesso a um servidor web for possível apenas usando o protocolo HTTPS, somente as portas 443 e 80 desse servidor devem estar acessíveis; todas as outras portas podem ser bloqueadas pelo firewall.

* **A OWASP publicou em seu site algumas cheatsheets** para, por exemplo, [implementar corretamente o TLS](https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html) ou para [proteger um webservice](https://cheatsheetseries.owasp.org/cheatsheets/Web_Service_Security_Cheat_Sheet.html).

## Protegendo autenticações

* **Siga [a recomendação da CNIL sobre senhas](https://www.cnil.fr/fr/node/23803)**. Em particular, lembre-se de limitar o número de tentativas de acesso.

* **Nunca armazene senhas em texto claro**. Armazene-as como um hash usando uma biblioteca comprovada, como [bcrypt](https://en.wikipedia.org/wiki/Bcrypt).

* **Se cookies forem usados para autenticação**, recomenda-se:

    * forçar o uso de HTTPS via [HSTS](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security);

    * usar o atributo `secure`;

    * usar o atributo `HttpOnly`.

* **Teste as suítes criptográficas instaladas nos sistemas** e desative as obsoletas (RC4, MD4, MD5, etc.). Incentive o uso de AES256. [Leia a nota da OWASP sobre o assunto](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html).

* **Adote uma política de senhas específica para administradores**. Altere as senhas, pelo menos, sempre que um administrador sair e em caso de suspeita de violação. Incentive a autenticação forte sempre que possível.

* **Limite o acesso às ferramentas e interfaces de administração ao pessoal qualificado.** Incentive o uso de contas com privilégios reduzidos para operações do dia a dia.

* **O acesso remoto às interfaces de administração deve estar sujeito a medidas de segurança reforçadas.** Por exemplo, para servidores internos, implementar uma VPN com autenticação forte do usuário e do dispositivo que ele está utilizando pode ser uma boa solução.

## Protegendo infraestruturas

* **Faça backups, se possível criptografados e verificados regularmente**. Isso é especialmente útil em caso de um ataque de ransomware aos seus sistemas, pois ter backups de todos os seus sistemas será a única medida que permitirá restaurá-los.

* **Limite o tamanho da pilha de software utilizada** e, para cada elemento da pilha:

    * **Instale atualizações críticas** sem demora, agendando uma verificação automática semanal;
    * **Automatize uma vigilância de vulnerabilidades** assinando os [NVD Data Feeds](https://nvd.nist.gov/vuln/data-feeds), por exemplo.

* **Use ferramentas de detecção de vulnerabilidades** para os processos mais críticos, a fim de detectar possíveis falhas de segurança. Sistemas de detecção e prevenção de ataques em sistemas ou servidores críticos também podem ser utilizados. Esses testes devem ser realizados regularmente e antes de qualquer nova versão de software ser colocada em produção.

* **Restrinja ou proíba o acesso físico e de software às portas de diagnóstico e configuração remota.** Por exemplo, você pode listar todas as portas abertas usando a ferramenta *netstat*.

* **Proteja os bancos de dados que você disponibiliza na Internet**, pelo menos restringindo o acesso o máximo possível (por exemplo, por meio de filtragem de IP) e alterando a senha padrão da conta de administrador.

* Em termos de gerenciamento de bancos de dados, as boas práticas incluem:

    * **usar contas nominais** para acesso ao banco de dados e criar contas específicas para cada aplicação;
    * **revogar os privilégios administrativos** de contas de usuários ou aplicações para evitar modificações na estrutura do banco de dados (tabelas, visões, processos, etc.);
    * ter proteção contra ataques de injeção de SQL ou scripts;
    * incentivar a criptografia de disco e banco de dados em repouso.bsites, applications and servers


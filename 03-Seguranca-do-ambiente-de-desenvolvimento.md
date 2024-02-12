# Ficha n°3: Segurança do ambiente de desenvolvimento

#### A segurança dos servidores de produção, desenvolvimento e integração contínua, assim como dos postos de trabalho dos programadores, tem de ser prioritária porque centralizam o acesso a um grande volume de dados.

## Avaliar os riscos e adotar medidas de segurança apropriadas

* **Avaliar os riscos** nas ferramentas e processos utilizados para os desenvolvimentos. Fazer um inventário das medidas de segurança existentes e definir um plano de ação para melora a mitigação dos riscos. NBomear uma pessoa responsável pela implementação do plano.

* Considerar os riscos em todas as ferramentas utilizadas, incluindo os riscoa associados a SaaS (Software as a Service) e ferramentas colaborativas na nuvem (tal como o [Slack](https://slack.com), [Trello](https://trello.com), [GitHub](https://github.com), etc.).

## Tornar seguros os servidores e posto de trabalho de uma forma homogénea e reproduzível

* Listas de **recomendações** acerca da segurança de servidores, postos de trabalho e redes internas estão disponíveis nas [ficha n° 5 até 8](https://www.cnil.fr/sites/default/files/atoms/files/cnil_guide_securite_personnelle_gb_web.pdf) do **guia de segurança de dados pessoais** da CNIL.

* Escrever um **documento com a lista de medidas e e explicação da sua configuração** para assegurar que as medidas de segurança são implementadas uniformemente nos servidores e postos de trabalho. PAra reduzir a carga de trabalho, **ferramentas de gestão da configuração**, tal como [Ansible](https://github.com/ansible/ansible), [Puppet](https://github.com/puppetlabs/puppet) or [Chef](https://github.com/chef/chef), podem ser usadas.

* Atualizar servidores e postos de trabalho, se possivel de forma automática. Pod ser configurada uma monitorização sobre uma lista das vulnerabilidades mais importantes, por exemplo [NVD Data Feeds](https://nvd.nist.gov/vuln/data-feeds).

## Colocar especial enfâse na gestão de acessos e rastreio de operações

* Lembrar de documentar a gestão das **chaves SSH** (uso de criptografia e algoritmos de comprimento de chave de última geração, proteção das chaves provadas com uma palavra-frase, rotaçaõ de chaves). Para exemplos de boas práticas, ver [o documento sobre o uso seguro de (open)SSH](https://www.ssi.gouv.fr/uploads/2014/01/NT_OpenSSH_en.pdf).

* Encorajar autenticação forte nos serviços utilizados pelas equipas de desenvolvimento.

* **Rastreat** acessos às máquinas e, se possivel, implementar **análise automática de registos (logs)**. Para manter rastreios fidedignos, a utilização de contas genéricas é para ser evitado.

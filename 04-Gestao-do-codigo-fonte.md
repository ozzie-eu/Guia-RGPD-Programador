# Folha n°4: Gestão do código-fonte

#### Independentemente do tamanho do seu projeto, é altamente recomendável usar uma ferramenta de gerenciamento de código-fonte, como um *sistema de controle de versão*, para rastrear suas diferentes versões ao longo do tempo.

## Configure seu sistema de controle de versão de forma eficiente, pensando na sua segurança.

* Um sistema de controle de versão é um programa de software que permite armazenar **todo o seu código-fonte e arquivos associados**, mantendo a **cronologia de todas as alterações** realizadas. Um simples servidor FTP não é um sistema de controle de versão.

* Configure seu ambiente corretamente usando os recursos oferecidos pelo sistema de controle de versão. Recomenda-se implementar uma **autenticação forte** e/ou **autenticação com chaves SSH** no início do seu projeto.

* Além disso, atribua *níveis de acesso* ao seu projeto para os usuários do sistema de controle de versão e defina para cada nível as **permissões** correspondentes (por exemplo, um nível "convidado" com direitos de leitura limitados, um nível "desenvolvedor" com direitos de escrita, etc.).

* Faça **backups regulares** do seu sistema de gerenciamento de código-fonte. Em particular, lembre-se de fazer backup do servidor principal onde todas as alterações são salvas.

* Estabeleça procedimentos de desenvolvimento para trabalhar de forma eficiente, mesmo que **várias pessoas estejam desenvolvendo ao mesmo tempo**. Por exemplo, você pode decidir não trabalhar na mesma branch (_master_), mas configurar branches baseadas em funcionalidades, que serão mescladas na branch principal à medida que o desenvolvimento avança. Essas estratégias de desenvolvimento já estão bem documentadas, como no [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/). Além disso, alguns sistemas de controle de versão permitem configurar **branches protegidas** que impedem alterações não autorizadas nos arquivos dessas branches.

## Esteja ciente do conteúdo do seu código-fonte.

* Implemente **ferramentas de métricas de qualidade de código** que escanearão seu código assim que ele for _commitado_ para verificar sua qualidade. Você também pode adicionar scripts para verificar essas métricas na [configuração do sistema de controle de versão](https://git-scm.com/book/uz/v2/Customizing-Git-Git-Hooks): o _commit_ será cancelado se o código-fonte não tiver qualidade suficiente.

* Mantenha seus segredos e senhas fora do repositório de código-fonte:
  * em **arquivos separados, que não foram _commitados_**. Lembre-se de usar arquivos especiais do seu sistema de controle de versão (como _.gitignore_ para _Git_) para evitar _commitar_ arquivos sensíveis por engano.
  * em **variáveis de ambiente**, certificando-se de que as variáveis de ambiente não sejam acidentalmente gravadas em *logs* ou exibidas quando ocorrer um erro na aplicação.
  * usando [**software específico de gerenciamento de segredos ou configurações**](https://www.digitalocean.com/community/tutorials/an-introduction-to-managing-secrets-safely-with-version-control-systems#using-configuration-management-systems-for-secret-management).  

  Por fim, se você precisar incluir esses dados no repositório, considere **criptografar/descriptografar automaticamente** os arquivos usando um *plugin* do sistema de controle de versão (por exemplo, [_git-crypt_](https://github.com/AGWA/git-crypt)).

* Após um _commit_ que contenha dados pessoais ou outros dados críticos, não se esqueça de [purgar](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History) [completamente](https://help.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository#purging-a-file-from-your-repositorys-history) o repositório de código-fonte: mesmo após a modificação, os dados ainda podem estar disponíveis no histórico do repositório.

* Tenha cuidado antes de **publicar seu código-fonte online**. Revise **todo o conteúdo** para garantir que não haja dados pessoais, senhas ou outros segredos presentes, incluindo todo o histórico de alterações.

## Exemplos de ferramentas

* Diferentemente de ferramentas como [Subversion](https://subversion.apache.org/), que precisam de um servidor central para funcionar, os principais sistemas de controle de versão ([Git](https://git-scm.com/), [Mercurial](https://www.mercurial-scm.org/), por exemplo) são **descentralizados**.

* Para a maioria dessas ferramentas, é fornecida uma **interface web e ferramentas relacionadas** (gerenciamento de bugs, wiki para sua documentação, etc.). Essas soluções podem ser acessíveis via internet ([GitHub](https://github.com/), [Bitbucket](https://bitbucket.org/), etc.) ou integradas aos seus próprios servidores.urce code


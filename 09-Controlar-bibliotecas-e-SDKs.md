# Ficha n°09: Controle suas bibliotecas e SDKs
#### Você utiliza bibliotecas, SDKs ou outros componentes de software desenvolvidos por terceiros? Aqui estão algumas dicas sobre como integrar essas ferramentas mantendo o controle de seus desenvolvimentos.

## Faça uma escolha informada

* **Avalie o valor de adicionar cada dependência.** Alguns blocos de software comumente usados são apenas algumas linhas de código. No entanto, cada elemento adicionado aumenta a superfície de ataque do seu sistema. No caso de uma única biblioteca oferecer várias funcionalidades, integre apenas as funcionalidades que você realmente precisa. Ao ativar o número mínimo de funcionalidades, você reduz o número de possíveis bugs que podem ocorrer.

* **Escolha softwares, bibliotecas e SDKs mantidos:**

    * Se você deseja usar software livre ou de código aberto, tente escolher projetos ou soluções com uma comunidade ativa, atualizações regulares e boa documentação.

    * Se você usar outros tipos de soluções com suporte comercial, garanta contratualmente que o código será mantido e atualizado durante a vida útil do seu projeto.

* **Leve a privacidade em consideração.** Alguns SDKs ou bibliotecas se financiam utilizando dados pessoais coletados das aplicações ou sites nos quais estão integrados. Certifique-se de que esses terceiros cumpram as leis aplicáveis em relação aos dados pessoais, incluindo um mecanismo para obter o consentimento do usuário.

* **Se você usar mecanismos criptográficos, é fortemente desencorajado implementar algoritmos ou protocolos criptográficos por conta própria**, mas sim tentar escolher bibliotecas criptográficas que sejam mantidas, reconhecidas e fáceis de usar.

## Avalie os elementos selecionados

* **Leia a documentação e altere as configurações padrão.** É importante saber como suas dependências funcionam. Bibliotecas e SDKs de terceiros frequentemente vêm com arquivos de configuração padrão, que raramente são alterados por falta de tempo, o que causa muitas falhas de segurança.
* **Audite suas bibliotecas e SDKs.** Você realmente sabe o que todas as bibliotecas e SDKs que você integra fazem? Quais dados são enviados por meio dessas dependências e para quem? Essa auditoria permitirá determinar as obrigações de proteção de dados a serem respeitadas e estabelecer a responsabilidade dos atores.
* **Mapeie suas dependências.** Bibliotecas e SDKs de terceiros também podem integrar outros componentes: auditar seu código permitirá mapear melhor todas as suas dependências e agir melhor caso um problema afete uma delas. Também é recomendado realizar auditorias de segurança de seus componentes de terceiros e monitorá-los.
* **Cuidado com [typosquatting](https://en.wikipedia.org/wiki/Typosquatting) e outras técnicas maliciosas.** Verifique os nomes das dependências, bem como suas próprias dependências, para evitar ataques. Não copie e cole linhas de comando de sites desconhecidos.

## Mantenha bibliotecas e SDKs

* **Use sistemas de gerenciamento de dependências** (como yum, apt, maven, pip, etc.) para manter uma lista atualizada de suas dependências.
* **Gerencie as atualizações de suas dependências,** especialmente no caso de atualizações de segurança que corrigem vulnerabilidades. Você deve configurar um procedimento documentado para gerenciá-las e implantá-las o mais rápido possível.
* **Esteja ciente das versões de bibliotecas e SDKs que estão no fim do suporte** e que não serão mais mantidas: tente encontrar outra solução (escolha uma nova biblioteca, renove o suporte comercial).
* **Verifique o status de projetos de código aberto,** especialmente a mudança de domínio ou propriedade de pacotes, pois alguns ataques utilizam atualizações maliciosas de dependências populares.


<p align="center"><img src="https://github.com/LINCnil/GDPR-Developer-Guide/raw/master/templates/BANNIERE-EN.JPG" width="100%" align="middle"></p>


# Guia RGPD do Programador

#### Para orientar programadores web e de aplicações por formar a desenvolver o seu trabalho em conformidade com o RGPD, a CNIL um novo guia de boas práticas, com licença de código-aberto, que se pretenda que seja enriquecido por profissionais.

Este guia é publicado sob a [licença GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) e [open license 2.0](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf) (explícitamente compatível com [CC-BY 4.0 FR](https://creativecommons.org/licenses/by/4.0/deed.fr)). Pode contribuir livremente na sua redação.

A [versão francesa](https://github.com/LINCnil/Guide-RGPD-du-developpeur) é a versão autêntica deste guia. Uma versão italiana deste guia está também disponível [em PDF](https://github.com/LINCnil/GDPR-Developer-Guide/releases/tag/V1.0) e [para contributos](https://github.com/LINCnil/GDPR-Developer-Guide/tree/it). Existe ainda uma versão portuguesa também disponível [para contributos](https://github.com/ozzie-eu/Guia-RGPD-Programador).

#### Este guia é exclusivamente para programadores?

Este guia visa maioritáriamente programadores que trabalhem individualmente ou em equipa, chefes de equipa, prestadores de serviços, mas também todos os interessados em desenvolvimento web e de aplicações de software.

São providenciados conselhos e melhores práticas, apresentando conceitos-chave úteis na compreensão do RGPD para todos os intervenientes, independentemente da dimensão da sua organização. Pode também servir para estimular discussões e práticas dentro das organizações e nas relações com os clientes.

#### O que contém este guia?

Este guia está dividido em **16 fichas temáticas** a maioria das necessidades dos programadores em cada etapa dos projetos, desde a preparação do desenvolvimento até à utilização de ferramentas analíticas.

O Regime Geral de Proteção de Dados (ou RGPD) especifica que a proteção dos direitos e liberdades de pessoas naturais requer **"a adoção de medidas técnicas e organizativas adequadas, a fim de assegurar o cumprimento dos requisitos do presente regulamento."** (Recital 78).

A determinação destas medidas está **relacionada com o contexto das atividades de tratamento postas em prática**, e o responsável do tratamento (a entidade pública ou provada que trata os dados pessoais) deve consequentemente assegurar a segurança dos dados que se propõe tratar.

As boas práticas neste guia **não pretendem cobrir a totalidade dos requisitos do regulamento nem ser prescritivo**, elas providenciam um primeiro nível de medidas para considerar questões de proteção de privacidade em desenvolvimentos de TI, com a intenção de serem aplicadas a todos os projetos de tratamento de dados. Dependendo da natureza do tratamento realizado, em certos casos, medidas adicionais terão de ser implementadas com vista a cumprir inteiramente com o regulamento.

## Tabela de Conteúdos

0. [Desenvolver em conformidade com o RGPD](00-Desenvolver-em-conformidade-com-o-RGPD.md)

1. [Identificar dados pessoais](#)

2. [Preparar o desenvolvimento](#)

3. [Segurança do ambiente de desenvolvimento](#)

4. [Gestão do código-fonte](#)

5. [Escolha informada da arquitetura](#)

6. [Aplicar segurança nos websites, aplicações e servidores](#)

7. [Minimização da recolha de dados](#)

8. [Gestão de perfis de utilizadores](#)

9. [Controlar bibliotecas e SDKs](#)

10. [Assegurar a qualidade do código e a sua documentação](#)

11. [Testes à aplicação](#)

12. [Informar os utilizadores](#)

13. [Preparar o exercício de direitos pelas pessoas](#)

14. [Definir um período de retenção de dados](#)

15. [Considerar a base de licitude na implementação técnica](#)

16. [Uso de mecanismos analíticos nos websites e aplicações](#)



## Como posso contribuir para este guia?

**O guia original está disponível em 2 versões**:

* Uma [versão web no sítio Internet da CNIL](http://www.cnil.fr/en/gdpr-developers-guide) e no repositório original [no separador "Releases"](https://github.com/LINCnil/GDPR-Developer-Guide/releases);
* Esta [versão no GitHub](https://github.com/LINCnil/GDPR-Developer-Guide), que oferece a possibilidade a todos de contribuir.

**O contributo pode ser feito em alguns passos**:

* Criar um registo no Github;
* Navegar até à página do projeto;
* Pode:
    * Utilizar o separador "Issue" para enviar comentários ou participar no debate.
    * Utilizar a opção "Fork" para realizar as suas próprias modificações e propor a sua inclusão por via do botão "Pull Requests".

**A sua proposta de contributo será examinada pela CNIL antes da publicação**. a versão Web do guia RGPD do programador será regularmente atualizada.

## Utilização


Para publicar este repositório de forma autónoma, pode recorrer à ferramenta **Pandoc**. Esta ferramenta permite converter os registos num ficheiro docx ou um documento HTML.

Pode encontrar as instruções sobre como instalar [aqui]( https://pandoc.org/installing.html)

* **Para gerar um ficheiro .docx**:

```bash
pandoc -s --toc --toc-depth=1 -o Guia-RGPD-Programador.docx [0-9][0-9]*.md
```

* **Para gerar um ficheiro .html**:

```bash
pandoc -s --template="templates/mytemplate.html" -H templates/pandoc.css -o index.html README.md [0-9][0-9]*.md
```

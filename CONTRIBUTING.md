# Como contribuir / How to contribute

[Português (Brasil)](#português-brasil) · [English](#english)

## Português (Brasil)

Obrigado pelo interesse! Este projeto é **comunitário e não oficial**: não tem afiliação com a RNP, o EduPlay ou o Moodle HQ. Leia o [Código de Conduta](CODE_OF_CONDUCT.md) antes de participar.

### Relatar um problema ou sugerir algo
1. Procure nas issues do repositório do plugin se já existe algo igual.
2. Abra uma issue usando o modelo (bug ou sugestão). Informe a versão do Moodle e do PHP, o banco de dados, a versão do plugin, o navegador e os passos para reproduzir.
3. Para **vulnerabilidades**, não abra issue pública: siga o `SECURITY.md` do repositório.

Relatos de compatibilidade (versões do Moodle, navegadores, plugins de terceiros como o Interactive Video) são muito bem-vindos.

### Enviar código
1. Abra (ou comente) uma issue antes de uma mudança grande.
2. Faça um *fork* e crie uma branch a partir da `main` (sugestão: `issues/<número da issue>`).
3. Siga as convenções do Moodle: [Coding style](https://moodledev.io/general/development/policies/codingstyle), cabeçalho GPL, `@package` e PHPDoc, strings em `lang/en` (e `lang/pt_br`), Privacy API.
4. Escreva ou atualize **testes** (PHPUnit; Behat quando fizer sentido) e a **documentação** (`docs/en` e `docs/pt_BR`, quando houver mudança de comportamento) e o `CHANGELOG.md`.
5. Se alterar `amd/src`, gere também `amd/build` com `npx grunt amd` em um checkout do Moodle e inclua os arquivos gerados.
6. Aumente a versão em `version.php` quando mudar o comportamento do plugin.
7. Abra o pull request. O CI roda o `moodle-plugin-ci` (phpcs, phpdoc, mustache, grunt, PHPUnit) em Moodle 4.5 e 5.3, com PostgreSQL e MariaDB, e precisa passar.

### Mensagens de commit
Usamos *Conventional Commits* detalhados, em português: `tipo(escopo): [TAG] Descrição no imperativo`, com `[ADD]`, `[FIX]`, `[UPD]`, `[DEL]` ou `[UPG]`, e um corpo com **Motivo**, **Impacto** e **Arquivos/Mudanças**. Contribuições em inglês também são aceitas.

### Licença
Ao contribuir, você concorda que seu código será distribuído sob a **GNU GPL v3 ou posterior**, a mesma licença do projeto.

## English

Thanks for your interest! This is a **community, unofficial** project, with no affiliation with RNP, EduPlay or Moodle HQ. Please read the [Code of Conduct](CODE_OF_CONDUCT.md) first.

### Report a problem or suggest something
1. Search the plugin repository's issues for duplicates.
2. Open an issue using the template (bug or suggestion). Include the Moodle and PHP versions, database, plugin version, browser and steps to reproduce.
3. For **vulnerabilities**, do not open a public issue: follow the repository's `SECURITY.md`.

Compatibility reports (Moodle versions, browsers, third-party plugins such as Interactive Video) are very welcome.

### Send code
1. Open (or comment on) an issue before a large change.
2. Fork and branch from `main` (suggestion: `issues/<issue number>`).
3. Follow Moodle conventions: [coding style](https://moodledev.io/general/development/policies/codingstyle), GPL header, `@package` and PHPDoc, strings in `lang/en` (and `lang/pt_br`), Privacy API.
4. Write or update **tests** (PHPUnit; Behat when it makes sense), the **documentation** (`docs/en` and `docs/pt_BR`, when behaviour changes) and `CHANGELOG.md`.
5. If you change `amd/src`, also build `amd/build` with `npx grunt amd` in a Moodle checkout and include the generated files.
6. Bump the version in `version.php` when the plugin's behaviour changes.
7. Open the pull request. CI runs `moodle-plugin-ci` (phpcs, phpdoc, mustache, grunt, PHPUnit) on Moodle 4.5 and 5.3 with PostgreSQL and MariaDB, and must pass.

### Commit messages
We use detailed Conventional Commits, in Portuguese: `type(scope): [TAG] Imperative description`, with `[ADD]`, `[FIX]`, `[UPD]`, `[DEL]` or `[UPG]`, and a body with **Motivo** (reason), **Impacto** (impact) and **Arquivos/Mudanças** (files/changes). English contributions are welcome too.

### License
By contributing you agree that your code is distributed under the **GNU GPL v3 or later**, the project's license.

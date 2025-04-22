# Codeguard

## About

A lightweight hook system for enforcing code quality at commit and push time.

## Current checks

- PHPCS (based on WPCS) for all PHP files;
- Prettier for all JavaScript files;
- Commit message should be at least 20 characters;
- Commit message should start with one of the defined prefixes;

## Sample output

```zsh
> codeguard@1.0.0 prettier
> prettier --check **/*.js

Checking formatting...
All matched files use Prettier code style!
🟢 Prettier check is successful.

> codeguard@1.0.0 phpcs
> vendor/bin/phpcs --standard=phpcs.xml

🟢 PHPCS check is successful.

> codeguard@1.0.0 eslint
> eslint .

🟢 ESLint check is successful.
🟢 Commit message has the correct prefix.
🟢 Commit message has the required minimum length.
```

# ESLint config for DCISS

A shareable [ESLint](https://eslint.org/) config for DCISS TypeScript projects.

## Development

You will need to set an environment variable named `EC_NPM_TOKEN` with the value of a [personal access token](https://gitlab.com/profile/personal_access_tokens) (name: `npm`, scopes: `api`).

Run `npm install` to install the project dependencies.

### Publishing a new version

1. Run `npm version patch` (replace `patch` [as necessary](https://docs.npmjs.com/cli/version)) to increase the version number.
2. Run `git push && git push --tags` to push the version commit and tag.
3. Run `npm publish` to publish the new version.

## Unused rules

### Has issues

* `@typescript-eslint/no-extraneous-class`
    * https://github.com/typescript-eslint/typescript-eslint/issues/812
* `@typescript-eslint/no-unnecessary-condition`
    * https://github.com/typescript-eslint/typescript-eslint/issues/996
    * https://github.com/typescript-eslint/typescript-eslint/issues/1015
* `@typescript-eslint/strict-boolean-expressions`
    * https://github.com/typescript-eslint/typescript-eslint/issues/754
* `@typescript-eslint/unbound-method`
    * https://github.com/typescript-eslint/typescript-eslint/issues/636
    * https://github.com/typescript-eslint/typescript-eslint/issues/700
    * https://github.com/typescript-eslint/typescript-eslint/issues/743
* `no-invalid-this`
    * https://github.com/typescript-eslint/typescript-eslint/issues/491
* `require-atomic-updates`
    * https://github.com/eslint/eslint/issues/11899

### Too strict

* `@typescript-eslint/no-extra-parens` – extra parentheses sometimes aid readability.
* `@typescript-eslint/no-magic-numbers` – difficult to follow, especially in existing projects.
* `@typescript-eslint/no-type-alias` – partly handled by `@typescript-eslint/consistent-type-definitions`.
* `@typescript-eslint/prefer-readonly` – team decision.
* `@typescript-eslint/require-await` – see discussion in https://github.com/eslint/eslint/issues/6820.

### Handled by TypeScript

* `@typescript-eslint/no-unused-vars` – ts(6133) with `noUnusedLocals` and `noUnusedParameters`.
* `@typescript-eslint/typedef` – ts(7005), ts(7006), and ts(7008) with `noImplicitAny`.
* `getter-return` – ts(2378).
* `no-dupe-args` – ts(2300).
* `no-dupe-keys` – ts(1117).
* `no-func-assign` – ts(2539).
* `no-import-assign` – ts(2539).
* `no-obj-calls` – ts(2349).
* `no-unreachable` – ts(7027) with `allowUnreachableCode: false`.
* `no-unsafe-negation` – ts(2358), ts(2360), and ts(2365).
* `valid-typeof` – ts(2367).

### Unnecessary

* `block-scoped-var` – unnecessary with `no-var`.
* `no-async-promise-executor` – unnecessary with `@typescript-eslint/no-misused-promises`.
* `no-empty-function` – unnecessary with `@typescript-eslint/no-empty-function`.
* `no-eq-null` – unnecessary with `eqeqeq`.
* `no-extra-label` – unnecessary with `no-labels`.
* `no-implicit-globals` – unnecessary with `parserOptions.sourceType = module`.
* `no-magic-numbers` – unnecessary with `@typescript-eslint/no-magic-numbers`.
* `no-redeclare` – unnecessary with `no-var`.
* `no-unused-labels` – unnecessary with `no-labels`.
* `require-await` – unnecessary with `@typescript-eslint/require-await`.
* `vars-on-top` – unnecessary with `no-var`.

### No use for

* `no-warning-comments`

### Revisit later

* `prefer-named-capture-group` – code must be targeting ES2018.

## Used rules with issues

* `@typescript-eslint/ban-types`
    * https://github.com/typescript-eslint/typescript-eslint/issues/842
* `@typescript-eslint/member-naming`
    * https://github.com/typescript-eslint/typescript-eslint/issues/816
* `@typescript-eslint/member-ordering`
    * https://github.com/typescript-eslint/typescript-eslint/issues/929

# remark-preset-stoicism

<!-- Badges -->

[![test][test-badge]][test]

<!-- Brief description -->

_**Markdown processor for the Stoicism Compendium.**_

This is a [**`remark`**][remark] [preset][] defining a number of warnings.

<details>
<summary><strong>These are the warnings.</strong></summary>

Each of these plugins is configured to emit a warning for the issue mentioned:

<!-- Keep these sorted alphabetically. -->

| Plugin                                              | Issue                                                   |
| --------------------------------------------------- | ------------------------------------------------------- |
| [`remark-lint-blockquote-indentation`][]            | Block quote indentation spaces ≠ 2                      |
| [`remark-lint-checkbox-character-style`][]          | Check box not `x` for checked, ` ` for unchecked        |
| [`remark-lint-code-block-style`][]                  | Code block not fenced                                   |
| [`remark-lint-definition-case`][]                   | Definitions not lowercase                               |
| [`remark-lint-definition-spacing`][]                | Consecutive spaces in definitions                       |
| [`remark-lint-emphasis-marker`][]                   | Emphasis marker not `_`                                 |
| [`remark-lint-fenced-code-flag`][]                  | Fenced code flag not provided                           |
| [`remark-lint-fenced-code-marker`][]                | Fenced code marker not \`\`\`                           |
| [`remark-lint-file-extension`][]                    | File name without extension `.md`                       |
| [`remark-lint-final-definition`][]                  | Definitions not at end of file                          |
| [`remark-lint-final-newline`][]                     | Missing `\n` at end of file                             |
| [`remark-lint-hard-break-spaces`][]                 | Spaces for a [hard line break][md-hard-line-breaks] > 2 |
| [`remark-lint-heading-increment`][]                 | Heading level increments > 1                            |
| [`remark-lint-heading-style`][]                     | Heading not [ATX][md-atx-headings]                      |
| [`remark-lint-linebreak-style`][]                   | End-of-line character not `\n` (as in Unix)             |
| [`remark-lint-link-title-style`][]                  | Link title not using `"`                                |
| [`remark-lint-list-item-bullet-indent`][]           | Indented list item bullets                              |
| [`remark-lint-list-item-content-indent`][]          | Mixed indentation in list item content                  |
| [`remark-lint-list-item-indent`][]                  | Spaces after list bullet ≠ 1                            |
| [`remark-lint-maximum-line-length`][]               | Lines longer than 80 characters                         |
| [`remark-lint-no-auto-link-without-protocol`][]     | [Autolinks][md-autolinks] without protocol              |
| [`remark-lint-no-blockquote-without-marker`][]      | Blank lines without `>` in block quote                  |
| [`remark-lint-no-consecutive-blank-lines`][]        | Consecutive blank lines                                 |
| [`remark-lint-no-duplicate-defined-urls`][]         | Duplicate definition URLs                               |
| [`remark-lint-no-duplicate-definitions`][]          | Duplicate definitions                                   |
| [`remark-lint-no-duplicate-headings`][]             | Duplicate headings                                      |
| [`remark-lint-no-empty-url`][]                      | Empty URLs                                              |
| [`remark-lint-no-file-name-articles`][]             | File name starts with an article                        |
| [`remark-lint-no-file-name-consecutive-dashes`][]   | File name contains consecutive dashes                   |
| [`remark-lint-no-file-name-irregular-characters`][] | File name contains “irregular” characters               |
| [`remark-lint-no-file-name-mixed-case`][]           | File name uses mixed uppercase and lowercase characters |
| [`remark-lint-no-file-name-outer-dashes`][]         | File name contains initial or final dashes              |
| [`remark-lint-no-heading-content-indent`][]         | Indented heading text                                   |
| [`remark-lint-no-inline-padding`][]                 | Padded content for emphasis, strong, etc.               |
| [`remark-lint-no-literal-urls`][]                   | Literal URLs                                            |
| [`remark-lint-no-multiple-toplevel-headings`][]     | Level 1 headings (`#`) > 1                              |
| [`remark-lint-no-reference-like-url`][]             | References match URLs                                   |
| [`remark-lint-no-shell-dollars`][]                  | Shell code starts with `$`                              |
| [`remark-lint-no-shortcut-reference-image`][]       | [Shortcut][md-shortcut] reference images                |
| [`remark-lint-no-shortcut-reference-link`][]        | [Shortcut][md-shortcut] reference links                 |
| [`remark-lint-no-table-indentation`][]              | Indented tables                                         |
| [`remark-lint-no-tabs`][]                           | Tabs used for indentation                               |
| [`remark-lint-no-undefined-references`][]           | References to undefined definitions                     |
| [`remark-lint-no-unused-definitions`][]             | Unused definitions                                      |
| [`remark-lint-ordered-list-marker-style`][]         | Ordered list marker not using `.`                       |
| [`remark-lint-ordered-list-marker-value`][]         | Ordered lists with non-incrementing marker values       |
| [`remark-lint-rule-style`][]                        | Rule style not `---`                                    |
| [`remark-lint-strong-marker`][]                     | Strong emphasis marker not `*`                          |
| [`remark-lint-table-cell-padding`][]                | Table cell not padded                                   |
| [`remark-lint-table-pipe-alignment`][]              | Unaligned tables                                        |
| [`remark-lint-table-pipes`][]                       | Table row not fenced with pipes                         |
| [`remark-lint-unordered-list-marker-style`][]       | Unordered list marker not `*`                           |
| [`remark-validate-links`][]                         | Invalid link or image to local files and headings       |

These plugins were considered and rejected:

<!-- Keep these sorted alphabetically. -->

| Plugin                                   | Issue                                                                        |
| ---------------------------------------- | ---------------------------------------------------------------------------- |
| [`remark-lint-maximum-heading-length`][] | Headings too long. We don’t want to put a limit on headings.                 |
| [`remark-lint-no-emphasis-as-heading`][] | Emphasis or strong emphasis used as heading. Sometimes, that’s what we want. |
| [`remark-lint-no-heading-punctuation`][] | Heading ends with punctuation. We sometimes want punctuation.                |

We also use [`remark-retext`][] with [`retext-preset-stoicism`][] for text
warnings and spellchecking.

</details>

<!-- Sections -->

## Prerequisites

In the following sections, we describe how to install `remark-preset-stoicism`
with [`npm`][npm-cli] and how to use it with [`remark`][remark-cli] to check and
format Markdown files.

Alternatives include [`yarn`][yarn] instead of `npm`.

## Installation

Install `remark-preset-stoicism` and other dependencies as a [development
dependency][npm-dependencies]:

```sh
npm install --save-dev \
  remark-preset-stoicism \
  remark-cli
```

## Usage

### Configuration

Create a file called [`.remark.js`][unified-engine-config]:

```js
exports.plugins = [require('remark-preset-stoicism')]
```

### Script

Define [scripts][npm-run-script] in your `package.json` to run `remark` on your
Markdown files:

```json
"scripts": {
  "check-md": "remark --quiet --frail .",
  "format-md": "remark --quiet --frail --output ."
}
```

Run the scripts with `npm run`:

```sh
npm run check-md
npm run format-md
```

## License

[Blue Oak Model License 1.0.0][license] © [Sean Leather][author]

<!-- Definitions, sorted alphabetically -->

[`remark-lint-blockquote-indentation`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-blockquote-indentation
[`remark-lint-checkbox-character-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-checkbox-character-style
[`remark-lint-code-block-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-code-block-style
[`remark-lint-definition-case`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-definition-case
[`remark-lint-definition-spacing`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-definition-spacing
[`remark-lint-emphasis-marker`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-emphasis-marker
[`remark-lint-fenced-code-flag`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-fenced-code-flag
[`remark-lint-fenced-code-marker`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-fenced-code-marker
[`remark-lint-file-extension`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-file-extension
[`remark-lint-final-definition`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-final-definition
[`remark-lint-final-newline`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-final-newline
[`remark-lint-hard-break-spaces`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-hard-break-spaces
[`remark-lint-heading-increment`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-heading-increment
[`remark-lint-heading-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-heading-style
[`remark-lint-linebreak-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-linebreak-style
[`remark-lint-link-title-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-link-title-style
[`remark-lint-list-item-bullet-indent`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-list-item-bullet-indent
[`remark-lint-list-item-content-indent`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-list-item-content-indent
[`remark-lint-list-item-indent`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-list-item-indent
[`remark-lint-maximum-heading-length`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-maximum-heading-length
[`remark-lint-maximum-line-length`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-maximum-line-length
[`remark-lint-no-auto-link-without-protocol`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-auto-link-without-protocol
[`remark-lint-no-blockquote-without-marker`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-blockquote-without-marker
[`remark-lint-no-consecutive-blank-lines`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-consecutive-blank-lines
[`remark-lint-no-duplicate-defined-urls`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-duplicate-defined-urls
[`remark-lint-no-duplicate-definitions`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-duplicate-definitions
[`remark-lint-no-duplicate-headings`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-duplicate-headings
[`remark-lint-no-emphasis-as-heading`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-emphasis-as-heading
[`remark-lint-no-empty-url`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-empty-url
[`remark-lint-no-file-name-articles`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-file-name-articles
[`remark-lint-no-file-name-consecutive-dashes`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-file-name-consecutive-dashes
[`remark-lint-no-file-name-irregular-characters`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-file-name-irregular-characters
[`remark-lint-no-file-name-mixed-case`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-file-name-mixed-case
[`remark-lint-no-file-name-outer-dashes`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-file-name-outer-dashes
[`remark-lint-no-heading-content-indent`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-heading-content-indent
[`remark-lint-no-heading-punctuation`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-heading-punctuation
[`remark-lint-no-inline-padding`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-inline-padding
[`remark-lint-no-literal-urls`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-literal-urls
[`remark-lint-no-multiple-toplevel-headings`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-multiple-toplevel-headings
[`remark-lint-no-reference-like-url`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-reference-like-url
[`remark-lint-no-shell-dollars`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-shell-dollars
[`remark-lint-no-shortcut-reference-image`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-shortcut-reference-image
[`remark-lint-no-shortcut-reference-link`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-shortcut-reference-link
[`remark-lint-no-table-indentation`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-table-indentation
[`remark-lint-no-tabs`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-tabs
[`remark-lint-no-undefined-references`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-undefined-references
[`remark-lint-no-unused-definitions`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-no-unused-definitions
[`remark-lint-ordered-list-marker-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-ordered-list-marker-style
[`remark-lint-ordered-list-marker-value`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-ordered-list-marker-value
[`remark-lint-rule-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-rule-style
[`remark-lint-strong-marker`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-strong-marker
[`remark-lint-table-cell-padding`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-table-cell-padding
[`remark-lint-table-pipe-alignment`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-table-pipe-alignment
[`remark-lint-table-pipes`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-table-pipes
[`remark-lint-unordered-list-marker-style`]: https://github.com/remarkjs/remark-lint/tree/main/packages/remark-lint-unordered-list-marker-style
[`remark-retext`]: https://github.com/remarkjs/remark-retext
[`remark-validate-links`]: https://github.com/remarkjs/remark-validate-links
[`retext-preset-stoicism`]: https://github.com/stoicism-compendium/retext-preset-stoicism
[author]: https://github.com/spl
[license]: ./license.md
[md-atx-headings]: https://spec.commonmark.org/0.29/#atx-headings
[md-autolinks]: https://spec.commonmark.org/0.29/#autolinks
[md-hard-line-breaks]: https://spec.commonmark.org/0.29/#hard-line-breaks
[md-shortcut]: https://spec.commonmark.org/0.29/#shortcut-reference-link
[npm-cli]: https://docs.npmjs.com/cli/install
[npm-dependencies]: https://docs.npmjs.com/specifying-dependencies-and-devdependencies-in-a-package-json-file
[npm-run-script]: https://docs.npmjs.com/cli/run-script
[preset]: https://github.com/unifiedjs/unified#preset
[remark-cli]: https://github.com/remarkjs/remark/tree/main/packages/remark-cli
[remark]: https://github.com/remarkjs/remark
[test-badge]: https://github.com/stoicism-compendium/remark-preset-stoicism/workflows/test/badge.svg
[test]: https://github.com/stoicism-compendium/remark-preset-stoicism/actions?query=workflow%3Atest
[unified-engine-config]: https://github.com/unifiedjs/unified-engine/blob/main/doc/configure.md
[yarn]: https://yarnpkg.com/

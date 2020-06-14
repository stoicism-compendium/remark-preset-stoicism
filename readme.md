# remark-preset-stoicism

<!-- Badges -->

<!-- Brief description -->

> Markdown processor for the Stoicism Compendium.

This is a [**remark**][remark] [preset][] defining a number of
[warnings](#warnings).

<!-- Sections -->

## Installing and Configuring

The following instructions describe one way of using this package with
[**npm**][npm].

1. Install this package as a [development dependency][npm-dependencies]:

   ```sh
   npm install --save-dev remark-preset-stoicism
   ```

2. Configure [remark-cli][] to use this package by adding the following to your
   `package.json`:

   ```json
   "remarkConfig": {
     "plugins": [
       "preset-stoicism"
     ]
   },
   ```

3. Configure one or more [run-scripts][npm-run-script] to run `remark`. Here is
   an example `package.json` configuration:

   ```json
   "scripts": {
     "format-md": "remark --output --quiet --frail .",
     "test-md": "remark --quiet --frail .",
     "test": "npm run test-md"
   },
   ```

   This means that, for all Markdown files in the current directory, you can
   format them with `npm run format-md` or test the formatting with `npm run
   test-md` or `npm test`. You may want to add other tests to the `test` script.

## Warnings

Each of the following plugins is configured to emit warnings for the issue
mentioned: <!-- sorted alphabetically -->

* [remark-lint-blockquote-indentation][] – block quotes indentation ≠ 2 spaces.
* [remark-lint-checkbox-character-style][] – check box not `x` for checked, ` `
  for unchecked.
* [remark-lint-code-block-style][] – code block not fenced.
* [remark-lint-definition-case][] – definitions not lowercase.
* [remark-lint-definition-spacing][] – consecutive spaces in definitions.
* [remark-lint-emphasis-marker][] – emphasis marker not `_`.
* [remark-lint-fenced-code-flag][] – fenced code flag not provided.
* [remark-lint-fenced-code-marker][] – fenced code marker not `\``.
* [remark-lint-file-extension][] – file name without extension `.md`.
* [remark-lint-final-definition][] – definitions not at end of file.
* [remark-lint-final-newline][] – missing `\n` at end of file.
* [remark-lint-hard-break-spaces][] – > 2 spaces for a [hard line
  break][md-hard-line-breaks].
* [remark-lint-heading-increment][] – headings increment > 1 level.
* [remark-lint-heading-style][] – heading not [ATX][md-atx-headings].
* [remark-lint-linebreak-style][] – end-of-line character not `\n` (as in Unix).
* [remark-lint-link-title-style][] – link title not using `"`.
* [remark-lint-list-item-bullet-indent][] – indented list item bullets.
* [remark-lint-list-item-content-indent][] – mixed indentation in list item
  content.
* [remark-lint-list-item-indent][] – spaces after list bullet ≠ 1.
* [remark-lint-maximum-line-length][] – lines longer than 80 characters.
* [remark-lint-no-auto-link-without-protocol][] – [autolinks][md-autolinks]
  without protocol.
* [remark-lint-no-blockquote-without-marker][] – blank lines without `>` in
  block quote.
* [remark-lint-no-consecutive-blank-lines][] – consecutive blank lines.
* [remark-lint-no-duplicate-defined-urls][] – duplicate definition URLs.
* [remark-lint-no-duplicate-definitions][] – duplicate definitions.
* [remark-lint-no-duplicate-headings][] – duplicate headings.
* [remark-lint-no-empty-url][] – empty URLs.
* [remark-lint-no-file-name-articles][] – file name starts with an article.
* [remark-lint-no-file-name-consecutive-dashes][] – file name contains
  consecutive dashes.
* [remark-lint-no-file-name-irregular-characters][] – file name contains
  “irregular” characters.
* [remark-lint-no-file-name-mixed-case][] – file name uses mixed uppercase and
  lowercase characters.
* [remark-lint-no-file-name-outer-dashes][] – file name contains initial or
  final dashes.
* [remark-lint-no-heading-content-indent][] – indented heading text.
* [remark-lint-no-inline-padding][] – padded content for emphasis, strong, etc.
* [remark-lint-no-literal-urls][] – literal URLs.
* [remark-lint-no-multiple-toplevel-headings][] – > 1 top-level heading (i.e.
  the one with `#`).
* [remark-lint-no-reference-like-url][] – references match URLs.
* [remark-lint-no-shell-dollars][] – shell code starts with `$`.
* [remark-lint-no-shortcut-reference-image][] – [shortcut][md-shortcut]
  reference images.
* [remark-lint-no-shortcut-reference-link][] – [shortcut][md-shortcut] reference
  links.
* [remark-lint-no-table-indentation][] – indented tables.
* [remark-lint-no-tabs][] – tabs used for indentation.
* [remark-lint-no-undefined-references][] – references to undefined definitions.
* [remark-lint-no-unused-definitions][] – unused definitions.
* [remark-lint-ordered-list-marker-style][] – ordered list marker not using `.`.
* [remark-lint-ordered-list-marker-value][] – ordered lists with
  non-incrementing marker values.
* [remark-lint-rule-style][] – rule style not `---`.
* [remark-lint-strong-marker][] – strong emphasis marker not `*`.
* [remark-lint-table-cell-padding][] – table cell not padded.
* [remark-lint-table-pipe-alignment][] – unaligned tables.
* [remark-lint-table-pipes][] – table row not fenced with pipes.
* [remark-lint-unordered-list-marker-style][] – unordered list marker not `*`.
* [remark-validate-links][] – invalid link or image to local files and headings.

### Not Used

The following plugins were considered and rejected:

* [remark-lint-maximum-heading-length][] – headings too long. We don't want to
  put a limit on headings.
* [remark-lint-no-emphasis-as-heading][] – emphasis or strong emphasis used as
  heading. Sometimes, that's what we want.
* [remark-lint-no-heading-punctuation][] – heading ends with punctuation. We
  sometimes want punctuation.

## License

[Blue Oak Model License 1.0.0][license] © [Sean Leather][author]

<!-- Definitions, sorted alphabetically -->

[author]: https://github.com/spl
[license]: ./license.md
[md-atx-headings]: https://spec.commonmark.org/0.29/#atx-headings
[md-autolinks]: https://spec.commonmark.org/0.29/#autolinks
[md-hard-line-breaks]: https://spec.commonmark.org/0.29/#hard-line-breaks
[md-shortcut]: https://spec.commonmark.org/0.29/#shortcut-reference-link
[npm-dependencies]: https://docs.npmjs.com/specifying-dependencies-and-devdependencies-in-a-package-json-file
[npm-run-script]: https://docs.npmjs.com/cli/run-script
[npm]: https://docs.npmjs.com/cli/install
[preset]: https://github.com/unifiedjs/unified#preset
[remark-cli]: https://github.com/remarkjs/remark/tree/master/packages/remark-cli
[remark-lint-blockquote-indentation]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-blockquote-indentation
[remark-lint-checkbox-character-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-checkbox-character-style
[remark-lint-code-block-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-code-block-style
[remark-lint-definition-case]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-definition-case
[remark-lint-definition-spacing]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-definition-spacing
[remark-lint-emphasis-marker]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-emphasis-marker
[remark-lint-fenced-code-flag]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-fenced-code-flag
[remark-lint-fenced-code-marker]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-fenced-code-marker
[remark-lint-file-extension]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-file-extension
[remark-lint-final-definition]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-final-definition
[remark-lint-final-newline]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-final-newline
[remark-lint-hard-break-spaces]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-hard-break-spaces
[remark-lint-heading-increment]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-heading-increment
[remark-lint-heading-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-heading-style
[remark-lint-linebreak-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-linebreak-style
[remark-lint-link-title-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-link-title-style
[remark-lint-list-item-bullet-indent]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-list-item-bullet-indent
[remark-lint-list-item-content-indent]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-list-item-content-indent
[remark-lint-list-item-indent]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-list-item-indent
[remark-lint-maximum-heading-length]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-maximum-heading-length
[remark-lint-maximum-line-length]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-maximum-line-length
[remark-lint-no-auto-link-without-protocol]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-auto-link-without-protocol
[remark-lint-no-blockquote-without-marker]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-blockquote-without-marker
[remark-lint-no-consecutive-blank-lines]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-consecutive-blank-lines
[remark-lint-no-duplicate-defined-urls]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-duplicate-defined-urls
[remark-lint-no-duplicate-definitions]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-duplicate-definitions
[remark-lint-no-duplicate-headings]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-duplicate-headings
[remark-lint-no-emphasis-as-heading]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-emphasis-as-heading
[remark-lint-no-empty-url]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-empty-url
[remark-lint-no-file-name-articles]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-file-name-articles
[remark-lint-no-file-name-consecutive-dashes]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-file-name-consecutive-dashes
[remark-lint-no-file-name-irregular-characters]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-file-name-irregular-characters
[remark-lint-no-file-name-mixed-case]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-file-name-mixed-case
[remark-lint-no-file-name-outer-dashes]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-file-name-outer-dashes
[remark-lint-no-heading-content-indent]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-heading-content-indent
[remark-lint-no-heading-punctuation]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-heading-punctuation
[remark-lint-no-inline-padding]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-inline-padding
[remark-lint-no-literal-urls]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-literal-urls
[remark-lint-no-multiple-toplevel-headings]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-multiple-toplevel-headings
[remark-lint-no-reference-like-url]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-reference-like-url
[remark-lint-no-shell-dollars]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-shell-dollars
[remark-lint-no-shortcut-reference-image]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-shortcut-reference-image
[remark-lint-no-shortcut-reference-link]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-shortcut-reference-link
[remark-lint-no-table-indentation]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-table-indentation
[remark-lint-no-tabs]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-tabs
[remark-lint-no-undefined-references]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-undefined-references
[remark-lint-no-unused-definitions]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-no-unused-definitions
[remark-lint-ordered-list-marker-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-ordered-list-marker-style
[remark-lint-ordered-list-marker-value]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-ordered-list-marker-value
[remark-lint-rule-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-rule-style
[remark-lint-strong-marker]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-strong-marker
[remark-lint-table-cell-padding]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-table-cell-padding
[remark-lint-table-pipe-alignment]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-table-pipe-alignment
[remark-lint-table-pipes]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-table-pipes
[remark-lint-unordered-list-marker-style]: https://github.com/remarkjs/remark-lint/tree/master/packages/remark-lint-unordered-list-marker-style
[remark-validate-links]: https://github.com/remarkjs/remark-validate-links
[remark]: https://github.com/remarkjs/remark

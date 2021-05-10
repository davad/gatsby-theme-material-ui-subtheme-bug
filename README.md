When `gatsby-theme-material-ui` is nested inside another theme, it throws an error during the build.

To reproduce, run the following in the root of the repo.

1. yarn install
2. yarn workspace site build


Result:
```
failed Building production JavaScript and CSS bundles - 8.122s

 ERROR #98123  WEBPACK

Generating JavaScript bundles failed

<path to repo root>/node_modules/gatsby-theme-material-ui-top-layout/src/wrap-with-provider.js: Support for the
experimental syntax 'jsx' isn't currently enabled (7:10):

  5 |
  6 | export default function wrapWithProvider({ element }) {
> 7 |   return <TopLayout theme={theme}>{element}</TopLayout>;
    |          ^
  8 | }
  9 |

Add @babel/preset-react (https://git.io/JfeDR) to the 'presets' section of your Babel config to enable transformation.
If you want to leave it as-is, add @babel/plugin-syntax-jsx (https://git.io/vb4yA) to the 'plugins' section to enable parsing.

File: ../node_modules/gatsby-theme-material-ui-top-layout/src/wrap-with-provider.js:7:9


error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
error Command failed.
```

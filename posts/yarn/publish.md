# Publishing packages to npm

_#npm_ _#yarn_

Scoped packages (example: `@org/pkg`) are private by default, so you have to add the `--access` flag during (initial) publishing:

```bash
yarn publish --access public
```

## Sources

- [@rhalff](https://github.com/rhalff):
[You must sign up for private packages [402], although package is public.](https://github.com/npm/npm/issues/21033#issuecomment-399087546)
- Yarn documentation: [`yarn publish`](https://classic.yarnpkg.com/en/docs/cli/publish/)

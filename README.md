## Reproduce the issue

```sh
pnpm install --filter "package-a"
# seems like "package-b" is also installed. It gets a folder "node_modules" with the usual isolated modules structure
# and "moment" - which is a dependency of package-b but *not* package-a - is also installed.
# (this means: it is in node_modules/.pnpm/moment@2.29.4, and package-b has symlinks to it set up)
```

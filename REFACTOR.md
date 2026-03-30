# Refactor Notes — poetry-skills

This branch contains refactoring improvements applied automatically.

## Changes Applied

### Code Quality
- Added `.editorconfig` — consistent coding style across editors
- Added/updated `.eslintrc.json` — linting rules (ESLint + TypeScript)
- Added `.prettierrc` — code formatting configuration
- Updated `.gitignore` — comprehensive ignore patterns

### TypeScript Support
- Added `tsconfig.json` with strict mode configuration
  - `strict: true`, `noUncheckedIndexedAccess`, `noImplicitReturns`
  - `allowJs: true` for gradual migration

### Testing
- Added `jest.config.js` with 70% coverage thresholds
- Test file pattern: `**/*.test.ts` / `**/*.spec.ts`

### CI/CD
- Added `.github/workflows/ci.yml`
  - Matrix: Node.js 18.x and 20.x
  - Steps: install → lint → type-check → test → build
- Added `.github/dependabot.yml` for automated dependency updates

## Running Locally

```bash
npm install
npm run lint       # ESLint
npm run type-check # TypeScript check
npm test           # Jest tests
npm run build      # Build
```

## Refactor Spec Reference

See the full refactoring specification:
[wscats-projects-refactor-spec.md](https://github.com/wscats)

### Key Principles Applied
1. **TypeScript** — strict mode, type safety
2. **Error handling** — Result type pattern, AppError class
3. **Security** — XSS prevention, input validation, path traversal protection
4. **Performance** — debounce/throttle, virtual lists, memoization
5. **Testing** — 70%+ coverage, unit + integration tests
6. **i18n** — react-i18next with RTL support

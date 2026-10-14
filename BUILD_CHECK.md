# Build Verification Script

## Verifying Build Dependencies

Before building, run:

```bash
yarn install
yarn deps
```

## Check Chart.js Version

```javascript
node -e "console.log('Chart.js:', require('chart.js').version)"
```

## Running Tests

```bash
yarn test
```

## Build for Production

```bash
yarn release
```

### Expected Output
- `public/js/app.js` - bundled JavaScript
- `public/index.html` - static pages

## Troubleshooting

### Module not found: chart.js
- Run `yarn install` again
- Clear node_modules: `rm -rf node_modules && yarn install`

### Shadow-cljs compilation errors
- Check ClojureScript version in `shadow-cljs.edn`
- Ensure all dependencies are compatible

````md
# job-tracker-pwa

Frontend-only job application tracker built with React + TypeScript. Local-first persistence via IndexedDB (Dexie), with search/filter/sort + JSON/CSV export and JSON import. No backend.

## demo
- github pages: (add link after deploy)

## features
- add / edit / delete applications
- status pipeline: applied, interview, offer, rejected, ghosted
- search (company/role/location/notes)
- filter by status + sort (recently updated, applied date, company a-z)
- local storage in your browser (indexeddb)
- export json (full backup)
- export csv (shareable spreadsheet format)
- import json (replaces current data in this browser)
- sample data button for quick demo

## tech
- react + typescript + vite
- dexie (indexeddb)
- zod (validation)
- vitest (tests)
- github actions (ci + pages deploy)

## run locally
requirements: node 20+ recommended

```bash
npm install
npm run dev
````

## scripts

```bash
npm run test
npm run lint
npm run build
npm run preview
```

## deploy (github pages)

this repo includes a github actions workflow that deploys `dist/`.

1. push to `main`
2. github repo → settings → pages → source: **github actions**
3. wait for the deploy workflow, then paste the pages url into the demo section above

note: `vite.config.ts` uses `base: "./"` which works for most github pages setups.

## import/export notes

* export json = full backup of all applications
* import json = replaces existing stored data for this app in this browser
* export csv = exports the current filtered list you’re viewing

## project structure

```txt
src/
  app/              app shell + logic
  components/       form/table/filters/dialogs
  db/               indexeddb schema + helpers
  lib/              filter + csv + import/export utilities
  styles/           global css
  test/             vitest setup
.github/workflows/  ci + deploy
```

```
```

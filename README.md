# re-marfer
 My [deps-new](https://github.com/seancorfield/deps-new) template for a minimal [re-frame](https://day8.github.io/re-frame/) SPA.

 It's based on the static repo [kees-/t01-rf-template](https://github.com/kees-/t01-rf-template), which edited [day8/re-frame-template](https://github.com/day8/re-frame-template) based on changes I made while creating projects.

 However this template can be installed in one command thanks to `deps-new`!

---

## To run the app
Make sure Clojure and `deps-new` are installed.

Run:

```sh
clj \      
  -Sdeps '{:deps {io.github.kees-/re-marfer {:git/tag "0.1.0" :git/sha "7e42a3a"}}}' \
  -Tnew create \
    :template kees/re-marfer \
    :name your/app-name
```

replacing `your/app-name`.

Note the additional dash due to my github username in `io.github.kees-/re-marfer` which isn't in `:template kees/re-marfer`.

To complete setup,

```sh
cd app-name
npm install
```

Then jack in with your code editor, or as a fallback, `$ npm run watch` and connect to the REPL.

Browse to `http://localhost:8280/` to establish the JS runtime and see the initial webpage.

---

## What's changed?
- [`re-frame-10x`](https://github.com/day8/re-frame-10x) included by default
- `re-frame` and `re-frame-10x` updated
- Appropriate files ignored
- `core.cljs` renamed to `main.cljs`
- `events.cljs`, `subs.cljs`, `db.cljs` combined into `rf.cljs`
- `re-frame` shortcuts: `<sub`, `<sub-lazy`, `>evt`, `>evt-now`
- JavaScript output folder `js` renamed to `_js`
- Blank favicon
- Add a CSS reset and a basic CSS file
- Small reformatting and semantic changes

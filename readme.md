# Steps to Reproduce

```
node -v #=> v8.11.2
yarn -v #=> 1.7.0
parcel --version #=> 1.9.2
```

```
parcel index.html
```

Parcel now builds the package but the console shows the following warning:

"[HMR] vue-loader hot reload is only compatible with Vue.js 1.0.0+."

Saving files does not result in HMR.

```
yarn add vue-loader
parcel index.html
```

Warning goes away, but now saving files results in a new error:

```
[Error] TypeError: undefined is not an object (evaluating 'record.Ctor.super.extend') — vue.runtime.esm.js:8032
  (anonymous function) (parcel-vue-loader-test.c697d22e.js:7566)
  (anonymous function) (Anonymous Script 1 (line 58))
  anonymous (Anonymous Script 1 (line 68))
  newRequire (parcel-vue-loader-test.c697d22e.js:48)
  hmrAccept (parcel-vue-loader-test.c697d22e.js:7930)
  (anonymous function) (parcel-vue-loader-test.c697d22e.js:7816)
  forEach
  onmessage (parcel-vue-loader-test.c697d22e.js:7814)
[Warning] Something went wrong during Vue component hot-reload. Full reload required. (parcel-vue-loader-test.c697d22e.js, line 7567)

```

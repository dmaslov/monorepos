---
theme: default
background: ''
# apply any windi css classes to the current slide
class: 'text-center uppercase subpixel-antialiased'
highlighter: shiki
lineNumbers: true
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

<h1 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
Monorepos.2022
</h1>

The Good, the Bad, and the Ugly

<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
What is Monorepo?
</h2>

<div class="inline-flex">
  <img class="h-30" src="/wiki.png">
  <p class="m-2 italic underline decoration-green-500">In version control systems, a monorepo ("mono" meaning 'single' and "repo" being short for 'repository') is a software development strategy where code for many projects is stored in the same repository</p>
</div>
<div v-click="1">
  <h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
  What means..
  </h2>
  <p>All packages you may want to store in separated git repos, but fancy packed in one place (git repo)</p>
</div>
<div v-click="2">
<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
When we may want to use it?
</h2>
<ul>
  <li>We want easily code base management</li>
  <li>We have a huge codebase with cross depends on packages</li>
  <li>We have several <code>applications</code> and the <code>packages</code> we use inside every application</li>
  <li>We don't want to deal with <code>yarn link</code>, etc if we need to fix something inside our package</li>
  <li>We want flexible versioning, publishing, and changelog generation</li>
  <li v-click="3"><span class="text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">Just you can</span> <fxemoji-sunglasses /></li>
</ul>
</div>
<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
The Players
</h2>
<div class="my-4 italic text-xs"><span class="text-yellow-500 opacity-80">Based on <a href="https://2020.stateofjs.com/en-US/other-tools/#utilities" target="__blank">State of JS 2020</a> most popular projects are Lerna (12,7%) and NX (15,8%). Other tools don't present</span></div>
<div class="grid grid-cols-3 font-mono items-center gap-y-14">
  <div class="flex flex-col">
    <div class="flex items-center">
      <logos-npm class="text-4xl" />
      &nbsp;/&nbsp;
      <logos-yarn class="text-2xl" />
      &nbsp;
      Workspaces
    </div>
    <ul v-click="1" class=" text-sm">
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Link dependencies</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Run commands across the packages</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated packages publishing</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated version managing</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-xs italic text-orange-400 opacity-50"> Low-level primitive used by other tools</li>
    </ul>
  </div>
  <div class="flex flex-col">
    <div class="flex items-center">
      <vscode-icons-file-type-lerna class="text-4xl" />
      &nbsp;
      Lerna (<carbon-star-filled class="text-xs text-orange-400" />31.4k)
    </div>
    <ul v-click="2" class=" text-sm">
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Link dependencies</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Run commands across the packages</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Automated packages publishing </li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Automated version managing</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Caching</li>
    </ul>
  </div>
  <div class="flex flex-col">
    <div class="flex items-center">
      <TurboIcon size="32" /> (<carbon-star-filled class="text-xs text-orange-400" />5.3k)
    </div>
    <ul v-click="3" class=" text-sm">
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Link dependencies</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Run commands across the packages</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated packages publishing </li>
      <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated version managing</li>
      <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Caching</li>
    </ul>
  </div>
  <div class="flex flex-col">
  <div class="flex items-center">
      <logos-nx class="text-6xl" /> (<carbon-star-filled class="text-xs text-orange-400" />10.3k)
    </div>
      <ul v-click="4" class=" text-sm">
        <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> More than just monorepo</li>
        <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated packages publishing </li>
        <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Automated version managing</li>
        <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Caching</li>
        <li style="list-style-type:none; margin-left: 0;" class="text-red-400"><carbon-close-filled /> Not as easy as wanted</li>
    </ul>
  </div>
  <div class="flex flex-col">
    <div class="flex items-center py-6">
      BIT (<carbon-star-filled class="text-xs text-orange-400" />14.6k)
    </div>
    <ul v-click="5" class="text-sm">
        <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> More than just monorepo</li>
        <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Good for micro frontends</li>
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
    </ul>
  </div>
  <div v-click="6" class="flex flex-col">
    <div class="flex items-center py-4">
      <div v-click="6" class="flex text-4xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
        <span>Other..</span>
      </div>
    </div>
    <ul v-click="5" class=" text-sm">
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
        <li class="text-transparent">Save the alignment</li>
    </ul>
  </div>
</div>
<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
Before we go further..
</h2>
<div v-click="1" class="my-10 flex justify-between">
  <ul v-click="2" class=" text-sm">
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Smart rebuilds of affected projects</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Computation caching</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Code sharing and ownership management</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> High-quality editor plugins </li>
  </ul>
  <div class="flex flex-col items-center">
    <logos-nx class="text-10xl" />
    <p><a href="https://nx.dev/" target="__blank">Give it a try</a></p>
  </div>
  <ul v-click="2" class="text-sm">
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Rich plugin ecosystem</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Workspace visualizations</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Powerful code generators</li>
    <li style="list-style-type:none; margin-left: 0;" class="text-green-400"><carbon-checkmark-filled /> Consistent dev experience for any framework</li>
  </ul>
</div>
<div v-click="3" class="flex justify-center">
<span class="text-lg text-red-400"><carbon-close-filled /> Be ready for the challenges</span>
</div>
<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
The Winner..
</h2>
<div v-click="1" class="flex justify-center items-center font-mono mb-4">
  <TurboIcon size="64" />
</div>
<div class="grid grid-cols-3 font-mono gap-5">
  <div v-click="2" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Incremental builds</div>
      <div class="text-gray-400 text-xs pt-4">Building once is painful enough, Turborepo will remember what you've built and skip the stuff that's already been computed.</div>
    </div>
  </div>
  <div v-click="3" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Content-aware hashing</div>
      <div class="text-gray-400 text-xs pt-4">Turborepo looks at the contents of your files, not timestamps to figure out what needs to be built.</div>
    </div>
  </div>
  <div v-click="4" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Remote Caching</div>
      <div class="text-gray-400 text-xs pt-4">Share a remote build cache with your teammates and CI/CD for even faster builds.</div>
    </div>
  </div>
  <div v-click="5" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Parallel execution</div>
      <div class="text-gray-400 text-xs pt-4">Execute builds using every core at maximum parallelism without wasting idle CPUs.</div>
    </div>
  </div>
  <div v-click="6" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Task pipelines</div>
      <div class="text-gray-400 text-xs pt-4">Define the relationships between your tasks and then let Turborepo optimize what to build and when.</div>
    </div>
  </div>
  <div v-click="7" class="rounded-xl bg-true-gray-900 h-160px">
    <div class="p-6">
      <div class="text-sm">Profile in your browser</div>
      <div class="text-gray-400 text-xs pt-4">Generate build profiles and import them in Chrome or Edge to understand which tasks are taking the longest.</div>
    </div>
  </div>
</div>
<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
The Digits..
</h2>
<table class="my-20">
  <tr>
    <td></td>
    <td class="text-xs">
      <code>build-packages</code> <i>First Run</i>
    </td>
    <td class="text-xs">
    <code>build-packages</code> <i>Re-run</i>
    </td>
    <td class="text-xs">
    <code>build-app</code> <i>First Run</i>
    </td>
    <td class="text-xs">
    <code>build-app</code> <i>Re-run</i>
    </td>
  </tr>
  <tr>
    <td>
      <vscode-icons-file-type-lerna class="text-2xl" />
    </td>
    <td class="font-semibold text-green-400"><carbon-checkmark-filled /> 5.29 sec</td>
    <td class="font-semibold text-red-400"><carbon-close-filled /> 4.45 sec</td>
    <td class="font-semibold">88.74 sec</td>
    <td class="font-semibold text-red-400"><carbon-close-filled /> 36.47 sec</td>
  </tr>
  <tr>
    <td>
      <TurboIcon size="32" />
    </td>
    <td class="font-semibold text-red-400"><carbon-close-filled /> 19.25 sec</td>
    <td class="font-semibold text-green-400"><carbon-checkmark-filled /> 2.63 sec</td>
    <td class="font-semibold">90 sec</td>
    <td class="font-semibold text-green-400"><carbon-checkmark-filled /> 1.25 sec - 6 sec</td>
  </tr>
</table>
<div class="my-4 italic text-xs"><span class="text-yellow-500 opacity-80">The repo contains <strong class="text-yellow-500 opacity-100">one</strong> React application and <strong class="text-yellow-500 opacity-100">13</strong> packages. One of the packages is the UI Library Kit which contains <strong class="text-yellow-500 opacity-100">102</strong> React components</span></div>
<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500 mb-10">
The Changes..
</h2>

```ts
"devDependencies": {
    - "concurrently": "^5.0.0",
    - "lerna": "^3.16.4",
    + "turbo": "^1.0.24"
  },
  "scripts": {
    - "build-packages": "lerna run build --parallel --scope package-1 --scope package-n ... 11 more times",
    + "build-packages": "yarn turbo run packages:build",

    - "start": "concurrently --kill-others -n packages,app \"yarn build-packages:watch\" \"env-cmd env/.env.local yarn --cwd packages/app start\" ",
    + "app:start": "env-cmd env/.env.local yarn turbo run packages:build:watch app:start",

    - "build:test": "yarn build-packages && env-cmd env/.env.dev yarn --cwd packages/app build && mv packages/app/build build",
    + "app:build:test": "env-cmd env/.env.dev yarn turbo run app:build && yarn run artifact:copy",

    - "bootstrap": "lerna bootstrap",
    - "build-packages:watch": "lerna run build:watch --parallel --scope package-1 --scope package-n ... 11 more times",

    + "artifact:copy": "rm -rf build && mv packages/app/build build",
  }
```

<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>
---

<h2 class="font-mono text-6xl text-transparent bg-clip-text font-bold bg-gradient-to-r from-red-500 to-blue-500">
One more thing..
</h2>
<div class="flex justify-center items-center mt-6">
  <h3 class="font-mono font-bold">That's how the pipe looks like</h3>
</div>

```ts {}
  "turbo": {
    "baseBranch": "origin/master",
    "pipeline": {
      "packages:build": {
        "dependsOn": ["^packages:build"],
        "outputs": ["lib/**"]
      },
      "packages:build:watch": {
        "dependsOn": ["^packages:build:watch"],
        "outputs": ["lib/**"]
      },
      "app:build": {
        "dependsOn": ["packages:build"],
        "outputs": ["build/**"]
      },
      "app:start": {"cache": false},
      "test": {},
    }
  },
```

<div class="font-mono text-xs text-orange-400 absolute bottom-2 right-4">
  <SlideCurrentNo /> / <SlidesTotal />
</div>

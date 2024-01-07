# Arcane Quizz

# Description:
This project involves creating an 8-question quiz about the Netflix series "Arcane," based on the League of Legends universe from Riot Games. Each question is designed to test fans' knowledge about the series' intricate details. The quiz automatically calculates the number of correct answers and displays a score at the end. The development is carried out using a modern JavaScript framework, and the design is created in Figma, featuring visual elements inspired by Arcane's aesthetic. Special attention has been given to the user interface, ensuring it is intuitive and immersive, thereby providing a unique and engaging experience for fans of the series.

# Online website:
https://arcane-quizz.netlify.app/

# Features:
- Customized display based on the selected questions and answers, enhancing user engagement.
- Capability for users to select their answers, providing an interactive quiz experience.
- Automatic display of the correct answer in case of an incorrect response, adding an educational aspect to the quiz.
- Option to move to subsequent questions, allowing for a smooth user journey through the quiz.
- Final display of results, giving participants immediate feedback on their performance.

# Technologies Used:
- Vue3 for the application logic.
- TypeScript for robust typing and enhanced code maintainability and readability.
- Sass for styling.
- Figma for design.

# Mockup Desktop : 

<img width="1439" alt="Capture d’écran 2024-01-07 à 20 38 24" src="https://github.com/KingYano/arcane-quizz/assets/79844764/71765aa5-fbea-46bb-9840-4509cdac99df">


## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
    1) Run `Extensions: Show Built-in Extensions` from VSCode's command palette
    2) Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

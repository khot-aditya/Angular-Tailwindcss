# Angular with Tailwind CSS framework

## Quickly install and run code with npm command
- `npx @aditya6838/angular-starter <app-name>`
- eg. npx @aditya6838/angular-starter my-angular-app

<br>
<br>

---
## CLI Steps

- Run `ng new project-name`
  - use `--strict` to opt in to Strict Mode
  - use `--routing` to handle the navigation
- Run `cd project-name`
- Run `npm install -D tailwindcss postcss autoprefixer`
- Run `npx tailwindcss init`
- Modify tailwind.config.js
  ```
  module.exports = {
  		content: ["./src/**/*.{html,ts}"],
  };
  ```
- Modify src/styles.css
  ```
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  ```
- Add test code in app.component.html
  ```
  <h1 class="text-3xl font-bold underline text-red-400">
  		Hello world!
  </h1>
  ```
- Run `ng serve --open`

## To use components from [tailwind-elements.com](https://tailwind-elements.com/quick-start/)

- Run `npm install tw-elements`
- Modify tailwind.config.js 

  ```
  content:
  [
      "./src/**/*.{html,ts}",
      "./node_modules/tw-elements/dist/js/**/*.js",
  ],

  plugins:
  [
      require("tw-elements/dist/plugin"),
  ],
  ```

- Add `./node_modules/tw-elements/dist/js/index.min.js` in angular.json
  ```
  "projects": {
  	"project-name": {
  		"architect": {
  			"build": {
                  "options": {
                      "scripts": [
                          "./node_modules/tw-elements/dist/js/index.min.js"
                      ]
                  }
  			}
  		}
  	}
  }
  ```
- Add test code in app.component.html

  ```
  <h1 class="text-3xl font-bold underline text-red-400">
  		Hello world!
  </h1>
  ```

- Run `ng serve --open`

## Install Jquery using CLI

- `npm i --save-dev @types/jquery`
- Modify tsconfig.app.json
  ```
  "compilerOptions": {
      "types": [ "jquery" ]
  }
  ```

## Install [Angular Material](https://material.angular.io/components/categories)

- Run `ng add @angular/material`

<br>
<br>

# Angular version 13.3.5

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

# Namaste React 🚀

Episode - 02

* node_modules in a project is collection of dependencies in project.
* npm init will create package.json and package.json is configuration file for npm.
* npx command will excute the package, for example "npx parcel index.html"
* react in the end is javascript package hosted on npm.
* Though we can inject react & react-dom in app by using CDN link (https://unpkg.com/react@18/umd/react.development.js & https://unpkg.com/react-dom@18/umd/react-dom.development.js) but it is not good 
practice due to 2 main reason
    1. Everry time, we have to make network call to unpkg.com, so it will add overall latency to app
    2. Have to manually update react & react-dom version.
        So better to have react as one of the dependencies inside project 

* If we write "npm install -D <package_name>", then npm will install package inside "devDependencies" in package.json, otherwise without "-D" specifier, package will install in dependencies section.
* in React-18, "ReactDOM" will import from "react-dom/client"
* If you want to import React in some js file,then while injecting js file like <script type="module" src="App.j"></script>

# Parcel
    - creates Dev Build
    - spin up Local Server
    - Do HMR (Hot Module Replacement) due to File Watching Algorithm which is basically written in C++
    - supports cache
    - Image optimization
    - Minification in production build
    - Bundling
    - Compress files
    - Consistent Hashing
    - Code Splitting
    - Differential Bundling - to support older browser
    - Diagnostic
    - Good Error Handling
    - Tree Shaking - remove unused code
    - Different dev & prod bundles

* To create prod level code using parcel - npx parcel build index.html
  But it will give error, if you have not removed {main: App.js} from package.json

* For dev-build - npx parcel index.html
* browserslist in package.json will tell that app may run in maximum of browsers but it will definately run in mentioned value (last 2 Chrome version) of browsersList 

* You can verify or find value of browserslist from (https://browserslist.dev/)
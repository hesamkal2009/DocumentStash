# How to Create React Redux Application With Unit Test Support 
- npx create-react-app my-app --template redux        // installing react-redux with template - for (stand-alone create-react-app usage, you need to intsall react-redux manually) 
----
- yarn add react-router-dom lodash joi-browser query-string jwt-decode prop-types axios redux @reduxjs/toolkit immer redux-devtools-extension reselect moment react-app-polyfill
----
- yarn add jest @types/jest @babel/core @babel/preset-env babel-jest -D    * Note: jest and babel-jest might cause problems if it is already installed as dependency by another package *
----
- touch config.json
----
- touch globalConsts.js
----
- yarn add styled-components ***install_styled-components_for_BETTER_ISOLATION_DynamicName_themeing_Much_More_IN_SmallToMedium_APPS***\ OR yarn add sass ***install_sass_for_BETTER_PERFORMANCE_IN_LARGE_APPS***\
<pre>
In package.json:
      {
        "resolutions": {
          "styled-components": "^5"
        }
      }
</pre>
----
- yarn add bootstrap
----
- yarn add @fortawesome/fontawesome-svg-core @fortawesome/free-solid-svg-icons @fortawesome/react-fontawesome
----
- yarn add @fortawesome/free-brands-svg-icons @fortawesome/free-regular-svg-icons
----
- yarn add react-toastify
----

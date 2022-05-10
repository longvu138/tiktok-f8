# Customize-cra:

-   dùng để ghi đè cấu hình webpack
-   làm cái này trước: https://github.com/timarney/react-app-rewired/
    -   Tạo tệp _config-overrides.js_ trong thư mục gốc
    ```
    module.exports = function override(config, env) {
      //do stuff with the webpack config...
      return config;
    }
    ```
    -   Thay trong file package.json
    ```
     "scripts": {
     "start": "react-app-rewired start",
     "build": "react-app-rewired build",
     "test": "react-app-rewired test",
     "eject": "react-app-rewired eject"
     }
    ```
-   https://github.com/arackaf/customize-cra
<hr>

# babel-plugin-module-resolver

-   https://github.com/tleunen/babel-plugin-module-resolver
-   tạo file _.babelrc_ ở thư mục root paste code dưới vào file
    ```
    	{
      "plugins": [
    	[
    	  "module-resolver",
    	  {
    		"alias": {
    		  "~": "./src"
    		}
    	  }
    	]
      ]
    }
    ```
-   tao jsconfig.json:

    ```
    {
      "compilerOptions": {
    	"baseUrl": ".",
    	"paths": {
    	  "~/*": ["src/*"]
    	}
      }
    }

    ```

    <hr>

# Cài đặt và cấu hình Prettier

-   tạo file .prettierrc

    ```
    {
    	"arrowParens": "always",
    	"bracketSameLine": false,
    	"bracketSpacing": true,
    	"embeddedLanguageFormatting": "auto",
    	"htmlWhitespaceSensitivity": "css",
    	"insertPragma": false,
    	"jsxSingleQuote": false,
    	"printWidth": 120,
    	"proseWrap": "preserve",
    	"quoteProps": "as-needed",
    	"requirePragma": false,
    	"semi": true,
    	"singleQuote": true,
    	"tabWidth": 4,
    	"trailingComma": "all",
    	"useTabs": false,
    	"vueIndentScriptAndStyle": false
    }
    ```

<hr>

# Cấu hình sử dụng CSS/SASS

-   Tạo GlobalStyles component
-   Cài thư viện SASS: npm i -D sass
-   Reset CSS:
    -   npm i --save normalize.css
-   Default CSS: font-family, font-size, line-height
<hr>

# Cấu hình router / layout cho dự án

-   Cài đặt react router dom
-   Đưa router ra ngoài:
    -   Tạo file routes public ra ngoài
    -   dùng map để lấy vào trang app.js
-   ưu: dễ dàng tạo các Route.

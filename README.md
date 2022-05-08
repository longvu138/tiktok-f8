# Customize-cra:

- dùng để ghi đè cấu hình webpack
- làm cái này trước: https://github.com/timarney/react-app-rewired/
  - Tạo tệp _config-overrides.js_ trong thư mục gốc
  ```
  module.exports = function override(config, env) {
    //do stuff with the webpack config...
    return config;
  }
  ```
  - Thay trong file package.json
  ```
   "scripts": {
   "start": "react-app-rewired start",
   "build": "react-app-rewired build",
   "test": "react-app-rewired test",
   "eject": "react-app-rewired eject"
   }
  ```
- https://github.com/arackaf/customize-cra
<hr>

# babel-plugin-module-resolver

- https://github.com/tleunen/babel-plugin-module-resolver
- tạo file _.babelrc_ ở thư mục root paste code dưới vào file
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
- tao jsconfig.json:

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

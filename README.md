# Customize-cra:

- dùng để ghi đè cấu hình webpack
- làm cái này trước: https://github.com/timarney/react-app-rewired/
  - Tạo tệp config-overrides.js trong thư mục gốc
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

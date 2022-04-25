# @openeagle/miniprogram-webpack-plugin

`@openeagle/miniprogram-webpack-plugin` 是一个面向 webpack 的小程序开发者工具插件。

- 自动打开微信开发者工具
- 自动上传小程序（无需打开开发者工具）

## 使用

1. 安装小程序开发者工具并配置环境变量

    - `WX_MINIPROGRAM_HOME`：小程序开发者工具的安装路径

2. 安装依赖

    ```shell
    npm install @openeagle/miniprogram-webpack-plugin --save-dev
    ```

3. 集成配置

    ```js
    // vue.config.js
    const MiniprogramWebpackPlugin = require('@openeagle/miniprogram-webpack-plugin');

    module.exports = {
      plugins: [
        new MiniprogramWebpackPlugin({
          autoOpen: true, // 是否自动打开开发者工具
          autoPublish: true, // 是否自动上传代码
        }),
      ],
    }
    ```

## 配置

| Name        | Type    | **Description**                       |
| ----------- | ------- | ------------------------------------- |
| autoOpen    | boolean | 是否自动打开开发者工具，默认值 `true` |
| autoPublish | boolean | 是否自动上传代码，默认值 `true`       |


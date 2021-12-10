# vuecli-tutorial

## env.model

常见类型
````
开发环境（开发阶段，本地开发版本，一般会使用一些调试工具或额外的辅助功能）
测试环境（测试阶段，上线前版本，除了一些 bug 的修复，基本不会和上线版本有很大差别）
生产环境（上线阶段，正式对外发布的版本，一般会进行优化，关掉错误报告）
````

命名模式
````
.env                # 在所有的环境中被载入
.env.local          # 在所有的环境中被载入，但会被 git 忽略
.env.[mode]         # 只在指定的模式中被载入 如 ：production 和 development
.env.[mode].local   # 只在指定的模式中被载入，但会被 git 忽略
````

项目实践
````
npm install

- npm run dev
- npm run stage
- npm run production
````
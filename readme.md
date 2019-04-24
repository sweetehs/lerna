
``` 
  // 登录
  npm login 

  // 安装依赖
  npm install --registry=http://registry.npmjs.lianjia.com:7001

  // 测试路径 localhost:port/${dirname}
  npm run test
```

- 新建 `packages/{packagename}`
- `npm init`(包名：`@efficiency/${packagename}`)
- 如果内部组件有依赖，比如a依赖于b，`lerna add b --scope=a`
- `lerna bootstrap` 安装依赖
- lerna 发布之前要提交远程仓库
- `lerna publish` 发布包(注意：要到根目录下执行)

如果要单独发布注意registry 是否是http://registry.npmjs.lianjia.com:7001

```
{
  "publishConfig": {
    "access": "public"
  },
}
```
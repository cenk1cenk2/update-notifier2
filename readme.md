这是从 update-notifier fork 过来的项目，主要是增加了可以从 `updateNotifier` 中指定 registry 的能力，同时增加了可以修改 installCommand message 的能力，避免通过 message 参数全盘覆盖输出的 update 信息。


### 安装

```bash
npm install update-notifier -S
```

+ 指定 registry

```js
updateNotifier({
  pkg,
  registryUrl: 'http://npm.example.com',
})
```

+ 覆盖升级安装信息

```js
updateNotifier({
  pkg
}).notify({
  installCommand: `cnpm i -g ${pkg.name} --registry=${registryUrl}`,
})
```

其他使用请参考 update-notifier 的文档：[https://www.npmjs.com/package/update-notifier](https://www.npmjs.com/package/update-notifier)

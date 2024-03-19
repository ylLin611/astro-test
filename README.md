## 创建 Astro 项目

```bash
pnpm create astro@latest

选择基础模板
```

创建完成后执行 `pnpm dev`
打开`http://localhost:4321/`能看到这个页面就行
![astro-home](/assets/astro-home.png)

## 提交到 Github

- Github 创建一个空项目
- 打开`astro`项目控制台，开推！

```
git remote add origin https://github.com/xxxx
git branch -M main
git add .
git commit -m 'build: astro init'
git push -u origin main
```

## Github 配置

- 点击 `Setting` - `Pages` - `Source` - `Github Actions` - `Static HTML`
  ![Github 配置](/assets/github-setting-pages.png)

- 这时候会直接生成一个工作流文件，先不用管 直接 commit change
  ![Github 配置](/assets/github-workflow.png)

## 本地修改

- 回到本地`astro`项目中，执行`git pull`
- 修改`/.github/workflows/static.yml`
  - 由于推到 `static html` 方式推到`github.io`默认访问的是项目下的`index.html`文件，所以需要修改下`base path`
    ![yml 文件修改](/assets/yml.png)
- 修改 gitignore 文件，把`/dist`目录添加进去
- 执行 `pnpm build`
- 推代码

## 测试结果
- 在 `Github` 项目中点击 `Actions` 会看到工作流执行过程，点击最新工作流
![撒花](/assets/ending.png)
- 点击这个链接，撒花！ 恭喜你！ 成功部署到了 `github.io`

## 彩蛋

后面如果继续进行开发，当有一些引用文件的时候，例如样式文件，你会发现卧槽！不生效，遭骗了!
- 需要干的最后一步：
因为 `github.io` 访问文件路径是 `http://xxxx.github.io/xxxx/xxx`，所以需要在 `astro` 项目中添加一个 `base` 属性，
`astro.config.mjs`
![配置base](/assets/astro-config.png)
# 🌍 World News Map — GitHub Pages 发布说明

这个文件夹已初始化好 git 仓库并提交完毕。你只需要做 **2 步**：

---

## 第 1 步：在 GitHub 上建一个仓库

1. 打开 https://github.com/new （需要登录你的 GitHub 账号；没有就免费注册一个）
2. **Repository name** 填：`world-news-map`（随意，但记下这个名字）
3. 选 **Public**（Public = 任何人都能访问）
4. 其它全部默认，点 **Create repository**

## 第 2 步：把文件推上去（二选一）

### 方式 A：命令行推送（推荐，以后更新也用它）

在「终端」里运行（把 `你的用户名` 换成你的 GitHub 用户名）：

```bash
cd /Users/celinezl/Desktop/Publish/world-news-map
git remote add origin https://github.com/你的用户名/world-news-map.git
git branch -M main
git push -u origin main
```

第一次会弹出窗口让你登录 GitHub（浏览器授权），完成即可。

### 方式 B：网页直接上传（不装任何东西）

1. 打开你刚建的仓库页面：`https://github.com/你的用户名/world-news-map`
2. 点 **Add file → Upload files**
3. 把 `/Users/celinezl/Desktop/Publish/world-news-map/index.html` 拖进去
4. 点 **Commit changes**

---

## 第 3 步：打开 Pages（只需要做一次）

1. 进入仓库 **Settings → Pages**（左侧栏）
2. **Build and deployment → Source** 选 **Deploy from a branch**
3. **Branch** 选 `main`，文件夹选 `/ (root)`，点 **Save**
4. 等 1–2 分钟，你的地图就上线了：

```
https://你的用户名.github.io/world-news-map/
```

把链接发给任何人，打开就能看。

---

## 🔄 以后怎么更新地图？

每次 `Scripts/fetch_news.py` 重新生成地图后，**重新发布一次**：

```bash
cd /Users/celinezl/Desktop/Publish/world-news-map
cp ../../News/world-news-map.html index.html
git add index.html
git commit -m "update map"
git push
```

（想让我帮你把这个更新也加进每天 08:30 的自动任务里，随时说！）

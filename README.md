## Feature

- 只有一個 Markdown 檔案
- 沒有複雜的設定 ✅
- 寫一寫 📝 馬上部署到 Github Page 🚀
- Demo: [YingYi's Resume](https://ininyingyi.github.io/Markdown-Resume/)

## Getting Start

#### fork 專案

右上角 fork 按下去

#### Git Clone

```
$ git clone <forked url>
```

#### 寫履歷

使用習慣的編輯器修改 `index.md`，如果沒有習慣的編輯器可以選擇 [Visual Studio Code](https://code.visualstudio.com/) 或是 [Vim](https://www.vim.org/)

#### 看一下效果怎樣

如果你沒有 Jekyll，請先安裝

```bash
$ gem install jekyll
```

offical document: https://jekyllrb.com/docs/installation/

讓 Jekyll live 的 rebuild 我們的履歷，瀏覽器打開 http://127.0.0.1:4000 查看效果

```bash
$ jekyll serve
Configuration file: /Users/liyang/Markdown-Resume/_config.yml
            Source: /Users/liyang/Markdown-Resume
       Destination: /Users/liyang/Markdown-Resume/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.385 seconds.
 Auto-regeneration: enabled for '/Users/liyang/Markdown-Resume'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

> 此時編輯完 index.md, 只需要重新整理瀏覽器就可以看到結果

> 按 Control + C 可以退出這個程式

## Deploy to Github Page

設定 google analytics track id, 編輯 `_config.yml`

```
gtag_id: <gtag_id>
```

用下列指令將靜態的檔案 build 到 `_site`

```bash
$ jekyll build
```

靜態的檔案 build 好之後我們要將他部署在 GitHub Page 上
透過下列指令會自動幫你把 `_site` 資料夾放進 remote repo `origin` 的 `gh-pages` branch

```bash
$ ./bin/deploy
```

## Generate PDF

Use [https://wkhtmltopdf.org/](https://wkhtmltopdf.org/)

```
wkhtmltopdf --enable-local-file-access _site/index.html CV-Chinese.pdf
```

## Thanks

- [sindresorhus/github-markdown-css](https://github.com/sindresorhus/github-markdown-css/blob/gh-pages/github-markdown.css)

# team_schedule123

這個 repo 內建 GitHub Actions workflow，可以部署隊伍排程首頁到 GitHub Pages。

## 第一次啟用 GitHub Pages

1. 到 GitHub repo 的 `Settings`。
2. 進入 `Pages`。
3. `Build and deployment` 的 `Source` 選 `GitHub Actions`。

## 部署 HTML

1. 到 GitHub repo 的 `Actions`。
2. 選 `Deploy custom HTML to GitHub Pages`。
3. 點 `Run workflow`。
4. `html_content` 可以貼上你要部署的完整 HTML。
5. 如果 `html_content` 留空，workflow 會把 `source_file` 指定的檔案部署成首頁，預設是 `main.html`。

部署完成後，GitHub Pages 網址會出現在該次 workflow run 的 `deploy` job 裡。

## 新增隊伍

在 repo 根目錄新增隊伍資料夾，並在資料夾內放入 `schedule.html`。

例如：

```text
3隊/schedule.html
```

重新執行 workflow 後，首頁會自動掃描並顯示這個隊伍。點擊隊伍卡片會前往該資料夾底下的 `schedule.html`。

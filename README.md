# ICEIB 2027 IEEE conference starter

Unofficial modular IEEEtran template for the IEEE track. Confirm the final conference-specific format with organizers. The current conference site specifies 4–8 pages.

Upload the ZIP to Overleaf as a new project, choose main.tex and pdfLaTeX. Replace all placeholder content and the example citation. No experimental results are supplied.

Local build: `latexmk -pdf main.tex` (with IEEEtran and listed packages installed).

Conference: https://www.iceib.asia/  
IEEE templates: https://www.ieee.org/conferences/publishing/templates.html

---

## Antigravity 操作 Overleaf 網頁紀錄

本節記錄 2026-11-25 使用 Antigravity IDE 連接 Chrome，並檢查 Overleaf 專案的操作流程。此流程是由 Agent 依指令操作瀏覽器，**不是本機檔案與 Overleaf 之間的背景即時同步**。

### 1. 工作目標

使用 Antigravity IDE 操作已登入的 Overleaf 專案，確認瀏覽器連線及專案可正常存取，後續再透過瀏覽器更新 Overleaf 中的 LaTeX 檔案。

- Overleaf 專案：https://www.overleaf.com/project/6b06bf70945d623ce97f996b
- 專案名稱（檢查時顯示）：`Your Research Paper Title`
- 主要檔案：`main.tex`
- LaTeX 文件類別：`\\documentclass[conference]{IEEEtran}`

### 2. 使用環境

- 作業系統：Windows 11
- IDE：Google Antigravity IDE
- 瀏覽器：Google Chrome
- Overleaf：已登入的網頁專案
- 本機專案資料夾：`C:\\Users\\user\\Desktop\\ICEIB2027`
- Antigravity 已設定本機檔案系統 MCP：`iceib-filesystem`

### 3. 瀏覽器連線與專案檢查

1. 開啟 Google Chrome。
2. 前往 `chrome://inspect/#remote-debugging`，依 Antigravity IDE 所使用的瀏覽器連線方式啟用遠端除錯及授權。
3. 回到 Antigravity IDE，使用 Agent 的瀏覽器操作功能連接目前開啟的 Chrome。
4. 在 Chrome 開啟上述 Overleaf 專案網址。
5. 若尚未登入，應由使用者自行登入；不要將帳號密碼提供給 Agent。
6. 確認 Overleaf 專案頁面、檔案樹、`main.tex` 編輯器及 PDF 預覽均可正常顯示。

**本次已回報的檢查結果：**

- Chrome 瀏覽器連線成功，並在新分頁開啟指定 Overleaf 專案。
- Overleaf 已登入，沒有額外登入、驗證碼或錯誤頁面。
- 左側檔案樹可見 `figures`、`sections`、`tables` 資料夾，以及 `main.tex`、`README.md`、`references.bib`。
- `main.tex` 已選取，編輯器處於 Code 模式且可編輯。
- PDF 預覽顯示 `Compile finished`，當時預覽共 2 頁。
- 這次連線與檢查階段沒有修改、上傳或刪除任何檔案。

### 4. 瀏覽器檢查使用的 Agent 指令

連線測試時使用的指令內容如下：

```text
/browser

請開啟我的 Overleaf 專案：
https://www.overleaf.com/project/6b06bf70945d623ce97f996b

如果尚未登入，請暫停操作，讓我親自登入 Overleaf。
登入完成後，請繼續操作，找到專案中的 main.tex，讀取目前的論文標題，並回報目前標題內容。

這一步只允許檢查，不要修改任何檔案。
```

之後另以下達瀏覽器連線確認指令，要求只確認連線及頁面，不修改任何檔案：

```text
/browser 請連接我目前已開啟的 Google Chrome，並開啟
https://www.overleaf.com/project/6b06bf70945d623ce97f996b 。
目前只需要確認瀏覽器連線成功，以及能否看到 Overleaf 專案頁面。
請不要修改、上傳或刪除任何檔案。
```

### 5. 預定的標題修改任務（尚待確認執行結果）

後續已準備要求 Agent 將 Overleaf 的 `main.tex` 中標題改為：

```latex
\\title{I did it!}
```

要求 Agent 僅修改 `\\title{...}` 的內容，保留作者、摘要、章節、參考文獻及其他檔案；等待 Overleaf 儲存後執行 Recompile，並檢查 PDF 第一頁標題。

**狀態：** 目前紀錄只包含這項修改任務的操作指令，尚未收到修改成功、Overleaf 儲存完成或 PDF 標題更新的確認。因此不可將標題已更新視為完成。

### 6. 後續建議工作流程

1. 先確認本機需要修改的檔案及變更內容。
2. 在本機完成修改並檢查差異。
3. 指示 Antigravity 透過已連接的 Chrome 開啟 Overleaf 專案。
4. 對照本機檔案內容，更新 Overleaf 中對應檔案；只更新明確指定的檔案。
5. 等待 Overleaf 儲存，執行 Recompile。
6. 檢查編譯結果及 PDF 內容。
7. 將本機變更依正常 Git 流程提交並推送至 GitHub。

> 注意：瀏覽器操作是依照指令執行的工作流程，不代表本機資料夾與 Overleaf 會自動雙向同步。更新前應確認目標檔案及內容，避免覆蓋 Overleaf 上較新的修改。

### 7. 安全注意事項

- Overleaf 帳號密碼及雙重驗證由使用者親自輸入，不寫入 Prompt 或 GitHub。
- 不要將 API Key、存取權杖、Cookie、個人資料或其他機密提交至 Repository。
- Agent 若遇到不確定的程式碼結構，應先停止並回報，不應擅自修改其他檔案。
- 每次更新後檢查 Overleaf 的儲存狀態及編譯結果。

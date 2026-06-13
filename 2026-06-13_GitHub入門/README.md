# 📖 2026-06-13 GitHub 入門

![Date](https://img.shields.io/badge/日期-2026--06--13-blue)
![Duration](https://img.shields.io/badge/時數-1小時-green)
![Level](https://img.shields.io/badge/程度-入門-orange)
![Tool](https://img.shields.io/badge/工具-Git%20%7C%20GitHub-181717?logo=github)

> 從零開始學習 GitHub，建立第一個 Repo，完成第一次 Commit。

---

## 📋 課程資訊

| 項目 | 內容 |
|------|------|
| 日期 | 2026-06-13 |
| 主題 | GitHub 入門 |
| 對象 | 法律與 AI 課程學員 |
| 時數 | 1 小時 |
| 講師 | 錢世傑 |

---

## 📁 檔案清單

| 檔案 | 說明 |
|------|------|
| [🖥️ 線上瀏覽投影片](https://docs.google.com/presentation/d/1Xmoj_NOFbOl-JqpyeS0eRyxG99ItJVbYAVYDVo566y4/edit?usp=sharing) | 瀏覽器直接看（Google Slides）|
| `github_intro_2026-06-13.pptx` | 下載版（PowerPoint）|
| `README.md` | 本頁說明 |

---

## 🗂️ 課程大綱

| # | 主題 | 時間 |
|---|------|------|
| 1 | 為什麼要用 GitHub？ | 10 分鐘 |
| 2 | Git vs GitHub／核心概念 | 15 分鐘 |
| 3 | Git 安裝確認與實作示範 | 15 分鐘 |
| 4 | 動手操作：建立第一個 Repo | 10 分鐘 |
| 5 | GitHub 在你的場景 | 5 分鐘 |
| 6 | Q&A + 課後任務 | 5 分鐘 |

---

## ✨ 本堂課學完你會

- 知道 Git 和 GitHub 的差別
- 看懂 `git log`，理解 Commit 是什麼
- 在 GitHub 上建立自己的第一個 Repo
- 上傳一份檔案並完成第一次 Commit

---

## 📚 課程內容

### 1｜為什麼要用 GitHub？

你現在的做法：

```
訴狀_v1.docx
訴狀_v2_修改.docx
訴狀_final.docx
訴狀_final_真的final.docx
訴狀_final_老師改過.docx
```

GitHub 的做法：

- 一份檔案
- 每次修改自動記錄版本
- 可隨時回到任一個版本
- 多人協作不衝突
- 雲端備份，不怕遺失

---

### 2｜Git vs GitHub

| | Git | GitHub |
|---|---|---|
| 是什麼 | 安裝在你電腦上的工具 | 微軟提供的雲端平台 |
| 負責什麼 | 追蹤每一次修改 | 存放所有版本紀錄 |
| 比喻 | 你的個人版本紀錄本 | 把日記放到網路上讓大家讀 |

> 簡單說：**Git 是工具，GitHub 是雲端家**

---

### 3｜五個你一定要記住的名詞

| 名詞 | 中文 | 一句話說明 |
|------|------|-----------|
| Repository | Repo（倉庫）| 一個專案的完整資料夾 |
| Commit | 提交 | 一次「存檔 + 附說明」的動作 |
| Branch | 分支 | 平行宇宙，安全測試新功能 |
| Fork | 分叉複製 | 把別人的 Repo 複製到自己帳號 |
| Pull Request | PR（合併申請）| 申請把修改合併回主線 |

---

### 4｜先確認有沒有裝 Git

打開 CMD，輸入：

```bash
git --version
```

- ✅ 看到版本號（如 `git version 2.53.0.windows.1`）→ 已安裝，直接進下一步
- ❌ 看到錯誤訊息 → 前往 [git-scm.com/download/win](https://git-scm.com/download/win) 下載，一路按 Next 即可

> 沒有 Git 也沒關係，今天課程主要用 GitHub 網頁版，Git 是加分示範

---

### 5｜Git 實作：跟著做一遍

> ⚠️ Windows 用戶：先執行 `chcp 65001` 避免中文亂碼

```bash
# 1. 建立資料夾並進入
mkdir my-first-repo
cd my-first-repo

# 2. 初始化 Git
git init

# 3. 建立一個檔案
echo Hello GitHub > test.txt

# 4. 加入追蹤 → 第一次存檔
git add .
git commit -m "第一次存檔"

# 5. 修改檔案 → 第二次存檔
echo Second line >> test.txt
git add .
git commit -m "新增第二行"

# 6. 查看歷史紀錄 ← 重點！
git log --oneline
```

---

### 6｜git log 告訴你什麼？

執行 `git log --oneline` 會看到：

```
1da9a5b (HEAD -> master, origin/master) 修正編碼為 UTF-8
3afe46f 新增第二行
7e537bb 第一次存檔
```

- **左邊的亂碼**（如 `3afe46f`）→ Hash，全球唯一身份證
- **右邊的文字** → 你寫的 Commit message

**時光機功能：**

```bash
git checkout 7e537bb   # 回到第一次存檔
git checkout master    # 回到最新版本
```

**推到 GitHub（本地 → 雲端）：**

```bash
git remote add origin https://github.com/你的帳號/my-first-repo.git
git push -u origin master
```

---

### 7｜建立你的第一個 Repo（實作）

1. 登入 GitHub → 點右上角 `+` → `New repository`
2. 填入 Repository name（英文、不含空格）
3. 選 **Public**（公開），勾選 **Add a README file**
4. 按下 `Create repository`
5. 點 README.md 右上角鉛筆，編輯並儲存
6. 填寫 Commit message → 按 `Commit changes`

> 💡 Commit message 就是「這次改了什麼」的說明，養成好習慣很重要！

**Commit Message 怎麼寫？**

| ❌ 不好的寫法 | ✅ 好的寫法 |
|---|---|
| `update` | `新增 GitHub 入門課程講義` |
| `修改` | `修正第三章錯字` |
| `asdfgh` | `初始化課程總目錄 README` |
| `test` | `更新 2026-06 課表連結` |

> 原則：一句話說清楚「這次改了什麼」，未來的你會感謝現在的你

---

### 8｜建立 Branch 與 Pull Request

> Branch（分支）= 草稿紙，PR = 說「我的草稿寫好了，請合併進正式版」

全程在 GitHub 網頁操作，不需要任何指令。

**Step 1：建立 Branch**

1. 進入你的 repo 頁面
2. 左上角點 **`main`** 或 **`master`** 下拉選單
3. 在搜尋框輸入新名稱，例如 `my-first-branch`
4. 點 **`Create branch: my-first-branch`**

**Step 2：在 Branch 上修改**

1. 確認左上角已切換到 `my-first-branch`
2. 點任一檔案（例如 README.md）→ 右上角鉛筆編輯
3. 隨便改一行內容
4. 按 **`Commit changes`**（這次 commit 只在 branch 上，不影響 main）

**Step 3：送出 Pull Request**

1. GitHub 會自動出現黃色提示條：**`Compare & pull request`**，點它
2. 填寫說明（改了什麼）
3. 點 **`Create pull request`**
4. 確認沒問題後點 **`Merge pull request`** → 改動合併回 main
5. 合併完成後可點 **`Delete branch`** 刪除草稿分支

---

### 9｜GitHub 在你的工作場景

| 身份 | 應用方式 |
|------|---------|
| ⚖️ 法律人 | 合約範本版本管理、訴狀草稿協同修改、法條解釋文件歷史追蹤 |
| 🤖 AI 課程學員 | 分享程式作業、Fork 老師的範例 Repo、展示自己的 AI 作品 |
| 📚 研究者 | 公開資料集、論文草稿版本管理、追蹤共同作者貢獻 |

---

## 🏠 課後任務

| 難度 | 任務 |
|------|------|
| ⭐ 基本 | 建立自己第一個 Public Repo，上傳一份文件 |
| ⭐⭐ 進階 | Fork 本課程 Repo，在 README 加一行自我介紹 |
| ⭐⭐⭐ 挑戰 | 建立 Branch，修改後送出 Pull Request（步驟見上方第 8 節）|

完成後把你的 Repo 連結貼到群組，讓大家互相 Star！

---

## 🔗 返回

[← 回到課程總目錄](../README.md)

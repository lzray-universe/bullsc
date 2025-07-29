
# 猜数字（Bulls & Cows）网页版解算器

这是一个纯前端实现的 **四位数字「猜数字 / Bulls & Cows」** 游戏解算工具，无需后端即可在浏览器运行。

---

## 功能亮点
| | |
|---|---|
|  **浏览器即用** —— 本地通过 HTTP 服务打开 `index.html`，或部署到 GitHub Pages 即可。 |
|  **决策树引擎** —— 完全复刻原 C++ 逻辑，结合预生成的 `answer.all`，保证给出最优下一步猜测。 |
|  **完整日志** —— 显示猜测次数（如 `猜测 1`、`猜测 2`）、程序给出的数字，以及你输入的反馈 (`xAyB`)。 |
|  **零依赖** —— 仅使用原生 HTML、JavaScript、CSS。 |
|  **集成 GitHub Actions** —— 推送代码即可自动部署到 Pages。 |

---

## 快速开始

### 本地预览
```bash
git clone <your-repo>
cd <repo>
# 启动轻量 HTTP 服务（Python 3.x 自带）
python -m http.server 8080
# 浏览器访问 http://localhost:8080
````

> 直接双击 `index.html`（`file://` 协议）会因安全策略无法加载 **answer.all**，请务必使用 HTTP 服务。

### 部署到 GitHub Pages

1. 将完整仓库（含 `.github/workflows/deploy.yml`）推送到 **`main`** 分支。
2. 在 **Settings → Pages** 中，选择 **Source: GitHub Actions**。
3. 重新运行工作流或提交新代码，完成后站点地址为
   `https://<用户名>.github.io/<仓库名>/`。

---

## 使用方法

1. 页面加载后会打印 **初始猜测**，例如 `猜测 1: 0123`。
2. 在输入框中输入反馈，如 `1A2B`，然后回车。
3. 日志依次记录

   * `反馈: 1A2B`（你的输入）
   * `猜测 2: 0245`（程序下一步）
4. 循环直到出现 **“回答正确！答案是 XXXX”**。

---


## 个性化定制

* **深色模式 / 主题** —— 修改 `<style>` 中的 CSS 变量即可。
* **替换决策树** —— 用你的 C++ 工具重新生成 `answer.all` 并替换。
* **多语言** —— 修改 `index.html` 中的静态字符串，或使用本中文 README。

---



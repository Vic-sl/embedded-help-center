# 🤝 贡献指南（中文）

欢迎来到本 STM32 技术问答社区项目！

本项目致力于收集和整理 STM32 相关问题的解决方案，帮助更多开发者少踩坑、提升效率。  
我们鼓励所有使用者：**不仅提问，还能贡献解决方案文档**。

---

## 📌 一、提问前请先查找已有解决方案

在你提出新问题前，请先按以下方法检查：

1. 进入 [Issues 页面](https://github.com/Vic-sl/embedded-help-center/issues)
2. 在搜索框中输入关键词（如“串口”、“乱码”、“ADC 抖动”等）
3. 浏览是否已有类似问题被讨论或解决
4. 如果找到：可以在该 Issue 下留言交流，或参考已有文档
5. 如果未找到：请继续下一步，**创建新的 Issue**

---

## ✍️ 二、如何提交一个新的问题（使用 GitHub 网页）

### 第一步：点击页面上方的 **Issues → New issue**

或直接访问：[新建问题](https://github.com/Vic-sl/embedded-help-center/issues/new)

### 第二步：填写内容

建议标题格式为：

[Bug] STM32串口乱码问题

[Question] TIM定时器中断无法触发

正文中请尽可能详细写出：

- 使用的芯片型号、开发板型号（如 STM32F103C8T6）
- 使用的开发环境（如 CubeMX + HAL + Keil / CLion 等）
- 具体的问题现象
- 你已经尝试过的方案
- 串口输出、报错截图等附图信息

### 第三步: 点击`Submit new issue`提交问题

---

## 🧠 三、问题解决后如何归档？

每一个已解决的问题，我们都会鼓励提问者把它**整理成文档加入仓库**，这样其他人也能从中受益。

---

## 📥 四、如何将你的问题归档到仓库（详细流程）

### ✅ 第 1 步：Fork 仓库

1. 访问本项目首页  
2. 点击右上角的 `Fork` 按钮，将仓库复制到你自己的账号下

---

### ✅ 第 2 步：将仓库克隆到本地

> 💡 如果你没有安装 Git，可以用 GitHub Desktop 或直接用网页操作。  
> 建议安装 VSCode（可视化编辑器）配合操作。

使用 Git 命令行（推荐）：

```bash
git clone https://github.com/你的用户名/项目名.git
cd 项目名
```

### ✅ 第 3 步：在 docs/ 文件夹中新建 Markdown 文档
文件命名格式如下（必须使用英文小写 + 标号 + cn/en）：

- docs/
  - issue-003-uart-garbled-cn.md   # 中文版
  - issue-003-uart-garbled-en.md   # 英文版

#### 推荐内容结构模板如下：
```markdown
# Issue 003：STM32串口乱码问题

## 📌 问题描述
简要说明你的问题背景，开发环境、硬件型号等。

## 🔍 原因分析
说说你是如何一步步找到问题原因的。

## ✅ 解决方案
明确列出解决办法，如配置代码、注意事项、截图等。

## 💬 讨论过程摘录（可选）
可引用 Issue 中讨论的亮点发言或反思。

## 🔗 参考资料
可以附上相关链接或文档。
```
英文版结构保持一致，内容翻译成英文

### ✅ 第 4 步：提交改动

使用命令行：

```bash
git add docs/issue-003-uart-garbled-cn.md
git add docs/issue-003-uart-garbled-en.md
git commit -m "Add: issue-003 UART乱码问题中英解决方案"
git push origin main
```

如果你使用的是网页修改或 GitHub Desktop，也可以直接 push。

### ✅ 第 5 步：发起 Pull Request（请求合并）

1. 回到你的 GitHub 仓库页面
2. 会看到 `Compare & Pull Request` 按钮，点击
3. 填写 PR 标题，如：

```
Add: issue-003 串口乱码问题解决方案（中英文）
```

4. 提交 PR，等待管理员审核

审核通过后，你的文档就会被收录到主仓库！

---

## 📎 五、注意事项与命名规范

| 类型     | 要求                                |
| -------- | ----------------------------------- |
| 文件名   | `issue-编号-关键词-cn.md` / `en.md` |
| 文件格式 | 必须使用 Markdown (`.md`)           |
| 内容结构 | 问题描述 → 原因分析 → 解决方案      |
| 提交方式 | 统一通过 Pull Request 合并          |

---

## 🎉 六、贡献者致谢
我们感谢每一位愿意留下问题和经验的开发者。
你的每一个提问、每一份归档，都是帮助后来的开发者节省时间、走出困境的明灯✨。
欢迎你成为这个开源社区的建设者！

---

## 📦 七、如何同步主仓库更新（适用于多次参与者）

如果你之前已经 Fork 了本项目仓库，那么之后其他人提交了新文档或更新内容，你的仓库**不会自动同步这些更新**，你需要手动拉取主仓库（上游）的内容。

---

### ✅ 步骤一：添加主仓库（upstream）

只需添加一次即可。

```bash
git remote add upstream https://github.com/项目创建者/主仓库名.git
例:
git remote add upstream https://github.com/Vic-sl/embedded-help-center.git
```

### ✅ 步骤二：拉取主仓库的最新内容

```bash
git fetch upstream

```

### ✅ 步骤三：合并主仓库的更新到你的分支

```bash
git checkout main
git merge upstream/main
```

如果有冲突，Git 会提示你手动解决。

### ✅ 步骤四：推送更新到你自己的远程仓库

```bash
git push origin main
```

#### 🔁 建议

每次在提交 Pull Request 前，都先运行一次同步操作，避免出现冲突或基于过期内容写文档的问题：

```bash
git fetch upstream
git merge upstream/main
git push origin main
```

---


如你对流程还有疑问，可在 Issues 区留言，我们会协助你完成。
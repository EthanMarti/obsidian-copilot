# Contributing to Copilot for Obsidian

# 为 Obsidian Copilot 做贡献

First off, thank you for considering contributing to Copilot for Obsidian! It's people like you who make Copilot for Obsidian such a great tool!
首先，感谢您考虑为 Obsidian Copilot 做贡献！正是像您这样的人使 Obsidian Copilot 成为如此出色的工具！

## How Can I Contribute?

## 如何贡献？

### Reporting Bugs or Suggesting Enhancements

### 报告错误或提出改进建议

Before submitting a bug report or suggestion, please check the [issues](https://github.com/logancyang/obsidian-copilot/issues) page for a list of currently known issues to ensure the bug has not already been reported. If it's a new bug or suggestion, create an issue and provide the following information:
在提交错误报告或建议之前，请查看[问题](https://github.com/logancyang/obsidian-copilot/issues)页面，了解当前已知问题列表，确保该错误尚未被报告。如果是新的错误或建议，请创建一个问题并提供以下信息：

- Use a clear and descriptive title.
- 使用清晰且描述性的标题。
- Describe the exact steps which reproduce the problem in as much detail as possible.
- 尽可能详细地描述重现问题的确切步骤。
- Provide specific examples to demonstrate these steps.
- 提供具体示例来演示这些步骤。
- Describe the behavior you observed after following the steps, pointing out what exactly is the problem.
- 描述按照这些步骤后观察到的行为，指出问题的确切所在。
- Explain which behavior you expected to see instead and why.
- 解释您期望看到的行为以及原因。
- Include screenshots or animated GIFs showing you following the described steps and clearly demonstrating the problem.
- 包含截图或动画 GIF，显示您按照所描述的步骤操作并清晰地展示问题。

### Your First Code Contribution

### 您的第一次代码贡献

Unsure where to begin contributing to Copilot for Obsidian? You can start by looking through the `help-wanted` issues.
不确定从哪里开始为 Obsidian Copilot 做贡献？您可以从查看标记为 `help-wanted` 的问题开始。

### Pull Requests

### 拉取请求

The process described here aims to:
这里描述的流程旨在：

- Maintain the quality of Copilot for Obsidian.
- 维护 Obsidian Copilot 的质量。
- Fix problems that are important to users.
- 修复对用户重要的问题。
- Engage the community in working towards the best possible Copilot for Obsidian.
- 让社区参与进来，共同打造最好的 Obsidian Copilot。
- Enable a sustainable system for Copilot for Obsidian's maintainers to review contributions.
- 为 Obsidian Copilot 的维护者提供一个可持续的系统来审查贡献。

Please follow these steps to have your contribution considered by the maintainers:
请按照以下步骤操作，以便维护者考虑您的贡献：

1. Ensure the code adheres to a clean style consistent with the existing code.
1. 确保代码遵循与现有代码一致的整洁风格。
1. Thoroughly test your changes before submitting.
1. 在提交之前彻底测试您的更改。
1. Be descriptive in your pull request, linking to the issue it addresses, and showing screenshots demonstrating the change.
1. 在拉取请求中详细描述，链接到它所解决的问题，并显示展示更改的截图。
1. Once you receive feedback, update the code accordingly to address them before your pull request can be ultimately accepted.
1. 一旦收到反馈，相应地更新代码以解决这些问题，然后您的拉取请求才能最终被接受。

### How to Set Up Dev Environment

### 如何设置开发环境

Here is a great [writeup by Daniel Haven](https://medium.com/gitconnected/how-to-set-up-the-ideal-obsidian-plugin-development-workflow-b222fe72280f) on the best practices for setting up your dev environment for Obsidian plugins.
这里有一篇由 Daniel Haven 撰写的[优秀文章](https://medium.com/gitconnected/how-to-set-up-the-ideal-obsidian-plugin-development-workflow-b222fe72280f)，介绍了为 Obsidian 插件设置开发环境的最佳实践。

In the case of Copilot for Obsidian, you will need to:
对于 Obsidian Copilot，您需要：

1. Fork the repo.
1. 复刻（Fork）仓库。
1. Create a vault just for development.
1. 创建一个专门用于开发的保险库（vault）。
1. Clone the forked repo into your vault's `plugins` folder.
1. 将复刻的仓库克隆到您保险库的 `plugins` 文件夹中。
1. Run `npm install` to install all dependencies.
1. 运行 `npm install` 安装所有依赖项。
1. Install the recommended VS Code extensions (Prettier and ESLint).
1. 安装推荐的 VS Code 扩展（Prettier 和 ESLint）。
1. Ensure your editor respects the `.editorconfig` and Prettier settings.
1. 确保您的编辑器遵循 `.editorconfig` 和 Prettier 设置。
1. Run `npm run dev` in your repo to see the effect of your changes.
1. 在您的仓库中运行 `npm run dev` 以查看更改的效果。
1. Before committing, run `npm run format` to ensure all files are properly formatted.
1. 在提交之前，运行 `npm run format` 确保所有文件都正确格式化。
1. When you are ready to make a pull request, ensure to make your changes in **a branch on your fork**, and then submit a pull request to the **main repo**.
1. 当您准备提交拉取请求时，确保在**您复刻的分支上**进行更改，然后向**主仓库**提交拉取请求。

Try to be descriptive in your branch names and pull requests. Happy coding!
尽量在分支名称和拉取请求中使用描述性的名称。祝编码愉快！

## Manual Testing Checklist

## 手动测试清单

This is a list of items to manually test after any non-trivial code change. Test the items relevant to your code change. If not sure, randomly choose items below.
这是在任何非微小代码更改后需要手动测试的项目列表。测试与您的代码更改相关的项目。如果不确定，可以随机选择以下项目。

First, **turn on debug mode in settings**, and open the dev console.
首先，**在设置中打开调试模式**，并打开开发控制台。

The most basic ones are model changes and mode changes.
最基本的测试是模型更改和模式更改。

### Test Fresh Install

### 测试全新安装

- To ensure any **new users** can use the plugin on a **fresh install**, manually delete the `data.json` file in the plugin directory, disable the plugin in Obsidian, and re-enable it, enter the OpenAI API key and other API key(s) to see if **onboarding** is working.
- 为确保任何**新用户**可以在**全新安装**时使用插件，手动删除插件目录中的 `data.json` 文件，在 Obsidian 中禁用插件，然后重新启用它，输入 OpenAI API 密钥和其他 API 密钥，查看**入门引导**是否正常工作。

### Chat / Plus mode

### 聊天 / Plus 模式

- Switch the model and check if the log has the new model key
- 切换模型并检查日志中是否有新的模型密钥
- Test model selection: Ask the model "what company trained you" to double check. Models from OpenAI, Claude, Gemini models can properly answer this question.
- 测试模型选择：问模型"是哪家公司训练了你"进行双重检查。来自 OpenAI、Claude、Gemini 的模型可以正确回答这个问题。
- Test chat memory: Tell the model your name, and in a turn or two ask "what's my name" to ensure chat memory is working.
- 测试聊天记忆：告诉模型您的名字，然后在一两轮对话后问"我的名字是什么"，确保聊天记忆正常工作。
- Use `[[note title]]` in chat and see if the model can access the content.
- 在聊天中使用 `[[笔记标题]]` 并查看模型是否能访问内容。

### Vault QA / Plus mode (with a small test vault)

### 知识库问答 / Plus 模式（使用小型测试保险库）

- Use the "Refresh index" button and see if it properly starts indexing. If it says "index is up-to-date", use "Clear Copilot index" and start indexing again (or equivalently, use "force re-index" command).
- 使用"刷新索引"按钮，查看是否正确开始索引。如果显示"索引已是最新"，使用"清除 Copilot 索引"并重新开始索引（或等效地，使用"强制重新索引"命令）。
- Check if there's any error or warning during indexing in the console, and if the exclusions and inclusions are shown correctly in the notice banner. Click pause and resume.
- 检查控制台中索引过程中是否有任何错误或警告，以及排除项和包含项是否在通知横幅中正确显示。点击暂停和恢复。
- After indexing is successful, ask a specific question where the answer is in your docs. For example, two of my docs are a biography of a person named "Mike", I ask "who is mike" and it should be able to answer using the two docs.
- 索引成功后，提出一个答案在您文档中的特定问题。例如，我的两个文档是一个名为"Mike"的人的传记，我问"谁是 mike"，它应该能够使用这两个文档回答。
  - In Plus mode make sure you trigger this query with `@vault` or cmd/ctrl + shift + enter. And then check "Show Sources" button for the expected docs.
  - 在 Plus 模式下，确保您使用 `@vault` 或 cmd/ctrl + shift + enter 触发此查询。然后检查"显示来源"按钮，查看预期的文档。
- To debug any failed QA query, we need to understand if it failed at 1. indexing 2. retrieval 3. generation.
- 要调试任何失败的问答查询，我们需要了解它是在哪个环节失败的：1. 索引 2. 检索 3. 生成。
  - First use "list all indexed files" command to check if the docs are indexed correctly.
  - 首先使用"列出所有已索引文件"命令检查文档是否正确索引。
  - Then check the console log for "retrieved chunks" from the hybrid retriever.
  - 然后检查控制台日志中混合检索器的"检索到的块"。
  - If correctly retrieved, it means the Chat Model is too weak to process the context effectively. Use a stronger Chat Model
  - 如果正确检索，则意味着聊天模型太弱，无法有效处理上下文。使用更强大的聊天模型。

### Plus mode

### Plus 模式

- "Give me a recap of this week" or some other time-based query. If you have daily notes or modified notes in this period, it should be able to retrieve them.
- "给我一个本周的回顾"或其他基于时间的查询。如果您在此期间有日记或修改过的笔记，它应该能够检索它们。
- Pass an image with text and ask gpt-4o-mini or gemini flash to describe the image.
- 传递一张带有文本的图片，并要求 gpt-4o-mini 或 gemini flash 描述图片。
- Try some random `@` tool and see if it's working as expected.
- 尝试一些随机的 `@` 工具，看看它是否按预期工作。
- Use `+` or `[[]]` to add notes to context. Ask the AI to summarize.
- 使用 `+` 或 `[[]]` 将笔记添加到上下文中。要求 AI 进行总结。
- Paste a URL and ask the AI to summarize.
- 粘贴一个 URL 并要求 AI 进行总结。

### Settings

### 设置

- If you updated model logic, test adding/deleting a custom model, whether you can use a new model in chat correctly.
- 如果您更新了模型逻辑，测试添加/删除自定义模型，是否可以在聊天中正确使用新模型。
- Switch the embedding model and click "refresh index" to see if it starts from scratch (it should detect that the existing index has a different type of embedding, and hence start indexing from scratch).
- 切换嵌入模型并点击"刷新索引"，查看是否从头开始（它应该检测到现有索引具有不同类型的嵌入，因此从头开始索引）。
- Any behaviors related to the settings that you added, updated or may have affected.
- 任何与您添加、更新或可能影响的设置相关的行为。

### Copilot Commands

### Copilot 命令

- Select text in a note and apply a built-in one like "translation" or a custom one you have as Custom Prompts.
- 在笔记中选择文本并应用内置命令，如"翻译"，或您作为自定义提示的命令。
- Any commands that you added, updated or may have affected.
- 任何您添加、更新或可能影响的命令。
- Try the `/` custom prompt
- 尝试 `/` 自定义提示
- Whether custom prompt templating works correctly with `{folder}`, `{#tag1, #tag2}`, etc.
- 自定义提示模板是否与 `{folder}`、`{#tag1, #tag2}` 等一起正确工作。

## Getting Help

## 获取帮助

- **Discord**: [Join](https://discord.gg/bFtfKDQqZt) the server for Copilot dev discussions.
- **Discord**：[加入](https://discord.gg/bFtfKDQqZt) 服务器参与 Copilot 开发讨论。
- **Email**: logan@brevilabs.com
- **电子邮件**：logan@brevilabs.com

Thank you for contributing to Copilot for Obsidian!
感谢您为 Obsidian Copilot 做出贡献！

# OIer-Helper v0.1.0

面向 OI / ICPC / 算法竞赛学习者的智能助手 Skill。

## 核心功能

| 功能 | 说明 | 示例 |
|------|------|------|
| 题目解法分析 | 粘贴 OJ 题目链接或题面，联网搜索题解并给出 C++17 参考代码 | `https://www.luogu.com.cn/problem/P3371` |
| 算法系统讲解 | 输入算法名，搜索权威资料讲解思路、证明、复杂度、模板 | `讲一下 Dijkstra` |
| 代码 Debug | 粘贴题目 + 你的代码，对照标准做法逐项排查错误 | `这题为什么 WA？题目链接 + 代码如下` |
| 题目搜索推荐 | 按算法 / 难度 / 平台搜索推荐练习题（默认不给题解） | `推荐几道线段树的入门题` |

## 支持的 OJ 平台

洛谷、AtCoder、Codeforces、LibreOJ、AcWing、牛客、POJ、HDU 等主流 OJ。

## 安装

前往 SkillHub 安装：[https://skillhub.cn/skills/oier-helper](https://skillhub.cn/skills/oier-helper)

## 使用方式

导入 WorkBuddy 或其他支持 Skill 的 AI 工具后直接发送：

- 题目链接（如 `https://www.luogu.com.cn/problem/P1000`）：自动分析解法
- 算法名（如 `KMP`）：自动讲解算法
- 题目链接 + 代码：自动 Debug
- 算法名 + "推荐题"/"找题"（如 `有没有树形DP的题`）：自动搜索推荐

## 代码规范

- 默认语言：C++17
- 不使用 `#define int long long`
- 包含 `ios::sync_with_stdio(false); cin.tie(nullptr);`
- 变量命名清晰，关键部分有注释
- **Skill 不会编译或运行任何代码，所有代码需用户自行测试**

## 注意事项

- 没找到可靠题解时，会明确说明并基于推导给出参考代码，**不声称保证 AC**
- 题目搜索默认不提供题解，可选定具体题目后再请求分析
- 题面或数据范围不完整时，会提醒补充

## 版权声明

本 Skill 仅总结公开题解的思路，不搬运他人的完整代码，不绕过网站访问限制。

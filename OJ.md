# 主流 OJ 题目链接识别策略与知名 OI 知识库

## 一、主流 OJ 题目链接识别策略

### 1.1 识别策略概述
OJ（Online Judge）题目链接的识别通常采用 **正则表达式（Regular Expression）** 进行 URL 模式匹配。根据不同 OJ 的 URL 结构，可将题目分为两类：

- **比赛题目（contestProblem）** ：位于比赛/竞赛页面下的题目，通常包含比赛 ID 和题目编号。
- **普通题目（normalProblem）** ：位于题库/问题集中的题目，通常仅包含题目 ID。

一个典型的路径解析规则配置（JSON 格式）示例如下：
```json
{
  "pathParseRule": {
    "contestProblem": "c\\/(\\w+)\\/(\\w+)[\\.\\w]*\\.(\\w+)$",
    "normalProblem": "a\\/(\\w+)[\\.\\w]*\\.(\\w+)$"
  }
}
```
该规则中，`a` 文件夹存放普通题目（以题目 ID 命名），`c` 文件夹存放比赛题目（按比赛 ID/题目编号组织）。

### 1.2 主流 OJ 平台 URL 格式

#### 国内主流 OJ

| OJ 平台 | 域名 | URL 格式示例 |
|---------|------|-------------|
| **洛谷** | `luogu.com.cn` | `https://www.luogu.com.cn/problem/P1000` |
| **LibreOJ (LOJ)** | `loj.ac` | `https://loj.ac/p/1000` |
| **Universal OJ (UOJ)** | `uoj.ac` | `https://uoj.ac/problem/1` |
| **Hydro** | `hydro.ac` | `https://hydro.ac/p/xxx` |
| **可达信奥** | `keda.ac` | `https://keda.ac/`（具体路径见平台） |
| **Vijos** | `vijos.org` | `https://vijos.org/p/xxx` |
| **信息学奥赛一本通** | `ybt.ssoier.cn:8088` | `http://ybt.ssoier.cn:8088/problem_show.php?pid=xxx` |
| **POJ** | `poj.org` | `http://poj.org/problem?id=1000` |
| **OpenJudge** | `poj.openjudge.cn` | `http://poj.openjudge.cn/xxx/` |
| **HDU OJ** | `acm.hdu.edu.cn` | `http://acm.hdu.edu.cn/showproblem.php?pid=1000` |
| **ZOJ** | `acm.zju.edu.cn` | `http://acm.zju.edu.cn/onlinejudge/showProblem.do?problemId=1` |
| **牛客竞赛** | `ac.nowcoder.com` | `https://ac.nowcoder.com/acm/problem/xxx` |
| **AcWing** | `acwing.com` | `https://www.acwing.com/problem/content/xxx/` |
| **Comet OJ** | `cometoj.com` | `https://cometoj.com/contest/xxx/problem/xxx` |
| **RQNOJ** | `rqnoj.cn` | `http://www.rqnoj.cn/problem/xxx` |
| **计蒜客** | `jisuanke.com` | （平台结构较特殊，需具体分析） |
| **ACGO** | `acgo.cn` | 具体格式见平台 |

#### 国际主流 OJ

| OJ 平台 | 域名 | URL 格式示例 |
|---------|------|-------------|
| **Codeforces** | `codeforces.com` | `https://codeforces.com/problemset/problem/{contest_id}/{index}`<br>或 `https://codeforces.com/contest/{contest_id}/problem/{index}` |
| **AtCoder** | `atcoder.jp` | `https://atcoder.jp/contests/{contest_id}/tasks/{task_id}` |
| **USACO** | `usaco.org` | `https://usaco.org/index.php?page=viewproblem&cpid=xxx` |
| **LeetCode** | `leetcode.com` / `leetcode.cn` | `https://leetcode.cn/problems/xxx/` |
| **Topcoder** | `topcoder.com` | `https://community.topcoder.com/stat?c=problem_statement` |
| **CodeChef** | `codechef.com` | `https://www.codechef.com/problems/xxx` |

#### 聚合平台

| 平台 | 域名 | 说明 |
|------|------|------|
| **Virtual Judge** | `vjudge.net` | 聚合多个 OJ 的题目，支持统一提交 |

### 1.3 URL 识别通用规则
不同 OJ 的题目链接通常遵循以下模式：
- **题目 ID 模式**：纯数字（如 `1000`）、字母+数字（如 `P1000`、`ABC001`）
- **路径模式**：`/problem/{id}`、`/p/{id}`、`/problemset/problem/{id}`、`/contests/{id}/tasks/{id}` 等
- **查询参数模式**：`?pid={id}`、`?id={id}`、`?problemId={id}`

---

## 二、知名 OI 知识库

### 2.1 OI Wiki
**OI Wiki** 是信息学竞赛领域最知名、最全面的开源知识整合平台。

- **官方网站**：https://oi-wiki.org/
- **GitHub 仓库**：https://github.com/OI-wiki/OI-wiki
- **核心定位**：面向信息学奥林匹克竞赛（OI）、ACM/ICPC、NOI、NOIP、Codeforces、AtCoder 等各类编程竞赛选手与算法爱好者的开源知识型协作平台
- **内容覆盖**：竞赛中的基础知识、常见题型、解题思路以及常用工具等
- **特点**：免费开放、持续更新、系统性知识体系

### 2.2 其他重要学习资源与知识库

| 名称 | 域名/地址 | 说明 |
| :--- | :--- | :--- |
| **C++ Reference** | https://en.cppreference.com/w/ | 最权威的 C++ 语言及其标准库在线参考手册，信息更新及时，内容详尽。 |
| **C++ 学习网** | https://www.learncpp.com/ | 非常系统的英文 C++ 教程网站，从零基础到进阶，内容全面。 |
| **C语言网** | http://www.dotcpp.com | 国内老牌的编程学习社区，提供 C/C++ 教程、在线编程和 OJ 练习。 |
| **NOI 官网** | http://www.noi.cn | 全国青少年信息学奥林匹克竞赛官方网站，发布竞赛大纲、官方新闻和政策。 |
| **USACO 官方** | https://usaco.org/ | 美国信息学奥林匹克竞赛官网，提供训练题库和竞赛信息。 |

### 2.3 竞赛知识点体系
信息学奥林匹克竞赛知识点通常分为以下层级：
- **编程基础与入门算法（CSP-J）** ：基础语法、数据结构入门、基础算法
- **算法核心（CSP-S / NOIP）** ：进阶算法与数据结构
- **高级数据结构（CSP-S / NOIP / NOI）** ：高级数据结构与复杂算法

---

## 三、算法模板库

| 名称 | 域名/地址 | 说明 |
| :--- | :--- | :--- |
| **灵茶山艾府算法模板库** | https://github.com/EndlessCheng/codeforces-go | 知名博主“灵茶山艾府”维护的算法竞赛模板库，主要使用 Go 语言，代码风格清晰。 |
| **Codeforces-Cpp 模板库** | https://github.com/qxf-72/Codeforces-Cpp | 受灵茶山艾府启发而建立的 C++ 算法竞赛模板库，内容丰富，涵盖常用算法。 |
| **OI Wiki 模板库** | https://oi-wiki.org/ | OI Wiki 内嵌大量模板代码，涵盖各种算法和数据结构的实现。 |

---

## 四、主流 OJ 平台完整列表（附录）

### 国内平台
- 洛谷（luogu.com.cn）
- LibreOJ（loj.ac）
- Universal OJ（uoj.ac）
- Hydro（hydro.ac）
- 可达信奥（keda.ac）
- Vijos（vijos.org）
- POJ（poj.org）
- OpenJudge（poj.openjudge.cn）
- HDU OJ（acm.hdu.edu.cn）
- ZOJ（acm.zju.edu.cn）
- 牛客竞赛（ac.nowcoder.com）
- AcWing（acwing.com）
- Comet OJ（cometoj.com）
- ACGO（acgo.cn）
- 信息学奥赛一本通（ybt.ssoier.cn:8088）
- 计蒜客（jisuanke.com）
- RQNOJ（rqnoj.cn）

### 国际平台
- Codeforces（codeforces.com）
- AtCoder（atcoder.jp）
- USACO（usaco.org）
- LeetCode（leetcode.com / leetcode.cn）
- CodeChef（codechef.com）
- Topcoder（topcoder.com）

### 聚合平台
- Virtual Judge（vjudge.net）

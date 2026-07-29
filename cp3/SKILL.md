---
name: cp3
description: 简短 alias，等同于 acpte-tod（中国哲学三阶推演法）。用 /cp3 触发道家+兵家+儒家三阶推理；用户说 /cp3 时调用与 /acpte-tod 完全等价的推理流程。
---

# /cp3 — acpte-tod 的简短 alias

> **这是个 alias skill**：本 skill 不包含完整推理规则——所有规则、触发钩子、红线检查点、金句库都从父目录 `../SKILL.md` 继承。

## 调用方式

```
/cp3 [用户问题]
```

与 `/acpte-tod [用户问题]` **完全等价**。

## 何时用

- 用户偏好**短命令**：四字母比八个字母快
- 想在 prompt 里**更低调地引用**：避免 "acpte-tod" 这种技术名显眼
- 已有 `/acpte-tod` 的所有功能：包括中英双语、红线拦截、金句四档协议

## 实现机制

Claude 收到 `/cp3` 时，应按 `../SKILL.md` 的完整规范执行：

1. 读 `../SKILL.md` 加载三阶推理规则
2. 读 `../references/quotes-en.md` 加载 22 句英文金句（如需）
3. 按场景自动识别语言（中文 → 第一档；英文 → 第四档）
4. 应用红线检查点（心理健康 / 法律 / 重大财务）
5. 按场景优先级确定三阶顺序

## 与 /acpte-tod 的差异

**零功能差异**。只是命令名短 4 个字符。

---

## 安装说明（其他用户）

如果你通过 `git clone` 安装本仓库到 `~/.claude/skills/chinese-philosophy-3stage/`，会自动获得两个命令：

- `/acpte-tod`（完整名）
- `/cp3`（简短 alias）

两者指向同一套推理规则。
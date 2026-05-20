# 安装与更新

## cc-switch 安装

```bash
mkdir -p ~/.cc-switch/skills
git clone https://github.com/Jackywxsz/jacky-motion.git ~/.cc-switch/skills/jacky-motion
```

如果本地已经有旧版：

```bash
cd ~/.cc-switch/skills/jacky-motion
git pull
```

## skills installer 安装

```bash
npx skills add https://github.com/Jackywxsz/jacky-motion --skill jacky-motion -a codex -g -y
```

## 验证

安装后确认存在：

```bash
ls ~/.cc-switch/skills/jacky-motion/SKILL.md
```

在 agent 中调用：

```text
$jacky-motion
```

## 卸载

```bash
rm -rf ~/.cc-switch/skills/jacky-motion
```

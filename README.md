# schematic-design

这是给 AI 画硬件原理图用的一套 Skill，适合芯片最小系统、电源、接口和传感器电路，也能修改、检查已有图纸。

规则里包括功能分页、模块内短线连接，以及按原厂资料选型、绑定封装和 3D 模型。只处理原理图及必要的元件库，不做 PCB 布局布线。详细要求见 [SKILL.md](https://github.com/SmallCoral/schematic-design-skill/blob/main/SKILL.md)。

## 安装与使用

以 Codex 为例，在项目根目录执行下面的命令。需要先有 Git，目标目录应当尚不存在。

```sh
git clone https://github.com/SmallCoral/schematic-design-skill.git .agents/skills/schematic-design
```

然后在请求里指定这个 Skill，并说清电源、接口条件和目标 EDA。例如下面这条请求。

```text
请使用 schematic-design 设计 MCU 与 I²C 传感器的原理图。
输入 5V，器件工作在 3.3V，使用 KiCad，只处理原理图。
先确认型号和接口条件，交付可编辑文件，并列出检查结果及未验证项。
```

仓库提供设计规则，没有附带绘图程序。实际画图需要 Agent 能调用相应的 EDA 工具或文件编辑接口；ERC 等检查也取决于可用工具。

## 友链

[LINUX DO 社区](https://linux.do/)

# CLAUDE.MD: AI Collaboration Guide

## 1. Project Overview & Purpose

## Development Commands

### Bash Commands for Python Development
```bash
# active virtual environment
source venv/bin/activate

# install dependency
pip install -r requirements.txt

# load env var for dev
source .env

# Run tests
pytest
```
##  Python Code style
- Use snake_case for variable and .py filename
- Add `type hint` for python code
- Prefer function based test case
- Prefer **less than 400 lines** in single .py file

- 每个文件夹中 **文件数量不超过 8 个**, 若超过，需进行 **多层子文件夹拆分**

##  JS Code style
- Use ES modules (import/export) syntax, not CommonJS (require)
- Destructure imports when possible (eg. import { foo } from 'bar')

## Develop Workflow
- Apply Test Driven Development, plan the test case before start to develop
- Prefer running single tests, and not the whole test suite, for performance
- After finishing responding to my request or running a command, run `afplay /System/Library/Sounds/Pop.aiff` command to notify me


## 🧠 架构设计关注点（持续警惕）

以下“坏味道”会严重侵蚀代码质量，**必须时刻警惕并避免**：

### ❌ 1. 僵化（Rigidity）
> 系统难以变更，微小改动引发连锁反应

- **问题**：变更成本高，开发效率低
- **建议**：引入接口抽象、策略模式、依赖倒置原则等

### ❌ 2. 冗余（Redundancy）
> 相同逻辑重复出现，维护困难

- **问题**：代码膨胀，一致性差
- **建议**：提取公共函数或类，使用组合代替继承

### ❌ 3. 循环依赖（Circular Dependency）
> 模块相互依赖，形成“死结”

- **问题**：难以测试、复用与维护
- **建议**：使用接口解耦、事件机制、依赖注入等手段

### ❌ 4. 脆弱性（Fragility）
> 修改一处，导致看似无关部分出错

- **问题**：系统不稳定，回归问题频发
- **建议**：遵循单一职责原则、提高模块内聚性

### ❌ 5. 晦涩性（Obscurity）
> 代码结构混乱，意图不明

- **问题**：新人难以上手，协作困难
- **建议**：命名清晰、注释得当、结构简洁、文档完善

### ❌ 6. 数据泥团（Data Clump）
> 多个参数总是一起出现，暗示应封装为对象

- **问题**：函数参数臃肿，语义不清
- **建议**：封装为数据结构或值对象

### ❌ 7. 不必要的复杂性（Needless Complexity）
> 过度设计，小问题用大方案

- **问题**：理解成本高，维护难度大
- **建议**：遵循 YAGNI 原则，KISS 原则，按需设计


## IMPORTANT: Sound Notification After Finish

After finishing responding to my request or running a command, run this command to notify me by sound:

```bash
afplay /System/Library/Sounds/Pop.aiff
```
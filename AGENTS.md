# 瑞克莫蒂对战 (Rick & Morty Fight)

动作对战游戏，打斗风格参考《瑞克和莫蒂》。

## 角色

- **瑞克**: 传送枪+激光炮+科技小玩意
- **莫蒂**: 近战+意外暴击+莫名运气

## 用途与 Target 判定

| 平台 | 需要? | 方式 |
|------|-------|------|
| 移动端 | 需要 | Capacitor (`android/` + `ios/`) |
| 智能硬件 | 可选 | 触屏动作对战为主，穿戴手势可选（当前搁置） |

## Harness / Loop（助手）

- 遵循根 `/Users/skat/AGENTS.md`：**Harness Engineering** + **Loop Engineering**
- Guide = 本文件；Sensor = 下方验证命令；同类失误第二次须沉淀规则或测试（棘轮）
- 开干前写清 **Done**；每切片过验证环；显式停止（成功 / 上限 / 无进展 / 人审）
- 详解：`docs/HARNESS_ENGINEERING.md`、`docs/LOOP_ENGINEERING.md`

## 验证环 / Done

```bash
npm install
npm test          # 若有
npm run build     # 或 build:web
npx cap sync android   # 若有 android/
# 可选：JAVA_HOME=…/openjdk@17 npm run apk:debug
```

**Done 示例**：测试通过（若有）+ web 产物进 `www/`/`dist/` + `cap sync` 无报错。可选穿戴未做可搁置，不纳入强制 Done。

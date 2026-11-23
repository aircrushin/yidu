# 制作与来源

《已读》1.1.0，2026-09-08。

剧情和人物方案来自用户提供的《已读》完整制作方案与剧本 v1，以及相应执行包 `content/story.json`、`content/state_rules.json`。保留六章 18 幕与原三种结局，按用户后续反馈改写环境互动，新增声音信结局、10 处条件回应及各项决定的结局回响。

游戏代码、矢量场景与道具、程序合成音乐与物件声音：Codex，按用户委托制作。矢量插画源定义保存在 `tools/make_art.py` 与 `tools/make_interaction_art.py`，音频源定义保存在 `tools/make_audio.py`。AI 辅助参与了代码、矢量路径及合成配乐的编写。

2026-09-09 人物素材更新：按用户提供的第一张图确定角色形象、第二张图确定小清新手绘风格，使用内置 image_gen 制作站姿与坐姿图集，并同步用于场景、互动人物与聊天头像。图集及制作说明位于 `assets/characters/handdrawn/`；原矢量人物保留作源素材备份。

2026-09-13 动作重绘：直接以以上原始站姿、坐姿图集作为图像参考，使用内置 image_gen 重绘 12 个动作姿态，保存在 `assets/characters/handdrawn/redrawn/`。两张新图集沿用原作人物、服饰、蜡笔复线和品红抠色方式，12 个 AtlasTexture 资源按实际人物边界索引。旧 `generated/` 版本保留为停用草稿。提示词和索引说明见该目录 README.md。此次未新增第三方素材。

89 项 SVG 资产：9 张背景、60 张角色姿态和表情组合、19 件道具、1 枚图标。运行时独立背景、人物、静物、互动道具与 UI 分层。7 段原创 64 秒音乐循环、5 组环境声、12 个功能音效，基于数学合成，未使用第三方录音样本。

2026-09-09 美术统一更新：全套 SVG 使用暖纸、雾蓝、鼠尾草绿与杏色，加入铅笔复线、裁剪颗粒、场景植物和生活物件细节，补充人物表情与独立手部动作。规范见 `assets/ART_DIRECTION.md`；总览由 `tools/preview_art.gd` 在 Godot 中渲染。此次未新增第三方资产。

2026-09-09 章节过场更新：使用已有插画、人物图集和原创物件音效编排 18 段 Godot 原生分层动画，包含物件特写、移动、翻转、淡入与选择分支字幕；没有新增第三方素材或逐帧人物表演。编排源为 `tools/make_cutscenes.py`，时间线数据为 `content/cutscenes.json`。

Godot 4.7.2 标准版：MIT 许可。完整引擎及随引擎分发的第三方说明见 `licenses/Godot-MIT.txt` 和 `licenses/Godot-third-party.txt`。官方来源：[Godot](https://godotengine.org/download/windows/)、[许可证](https://github.com/godotengine/godot/blob/4.7.2-stable/LICENSE.txt)。

Noto Sans CJK SC Regular 与 Noto Serif CJK SC Regular：SIL Open Font License 1.1。字体未修改，分别附带官方许可；来源：[Noto CJK 官方仓库](https://github.com/notofonts/noto-cjk)。

制作和导出不代表商店发行审核或人工美术批准。人物制作阶段使用用户提供的参考图调用图像生成工具；游戏运行时保持离线，不上传玩家数据。

# 广东爱情故事（Guangdong Love Story）

一款纯前端网页互动视觉小说。2010 年的广东小城，打工青年阿榕与患再生障碍性贫血的女孩小满相爱相扛：
一笔两万四的手术首付，照见爱情与现实的拉扯。

## 在线试玩

- 游戏（可直接打开）：https://gd-love-story.app.workbuddy.host/?sharecode=TU2KUIG7MU
- 说明文档：https://gd-love-story.app.workbuddy.host/docs.html?sharecode=TU2KUIG7MU

## 本地运行

方式一：直接双击 `index.html`（需保持 `scenes/` `portraits/` `audio/` `assets/` 文件夹结构完整）。

方式二（推荐，起个本地服务器）：

```bash
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

> 另有单文件版（所有资源 base64 内联，任何环境打开都不会缺图），见仓库外 `广东爱情故事_提交版.html`。

## 玩法

- 点击屏幕任意处推进对话
- 左上「‹ 回退」回看上一句（跨不过选择点与章节）
- 右下「音·开/关」开启钢琴 BGM 与音效
- 剧情中的选择影响金钱与结局；两个小游戏（打螺丝 / 整理单据）

## 结局机制

- 高消费（老火汤 / 蛋糕）超过 3 次 → 凑不齐手术费 → **强制坏结局**
- 其余情况按概率判定：坏结局 70% / 好结局 30%（常量 `BAD_RATE` 控制）
- 结局后延伸「祠堂祭奠」终章

## 结构

```
index.html      游戏本体（HTML + CSS + JS 全部内联，无框架无构建）
scenes/         17 张实景风格场景图
portraits/crop/ 9 张角色立绘
audio/          背景音乐（CC-BY 3.0 / CC0，署名见 audio/README.txt）
assets/         标题页纸张底图
docs.html       说明文档网页版
提交说明.md      进度说明与 AI 使用声明
```

## 素材授权

- 背景音乐来自 OpenGameArt，CC-BY 3.0（MouthlessGames《Dark Piano》系列）/ CC0，署名要求见 `audio/README.txt`
- 角色立绘与场景背景由 AI 图像生成模型产出，人工完成抠图、水印裁切与画风统一
- 本项目仅用于比赛展示，非商用

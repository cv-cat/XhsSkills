# Spider_XHS Skills

https://github.com/cv-cat/Spider_XHS
这个仓库用于存放基于 `Spider_XHS` 封装的 Agent Skills。

## 目录结构

- `skills/xhs-apis`：封装小红书 PC 端与创作者平台 API 的 skill

## xhs-apis

`xhs-apis` 这个 skill 只保留并封装了两组核心接口：

- `xhs_pc_apis.py`
- `xhs_creator_apis.py`

运行时所需的 vendored Python 与 JS 文件位于：

- `skills/xhs-apis/scripts/runtime/spider_xhs_core`

## 安装

安装 Python 依赖：

```
pip install -r skills/xhs-apis/scripts/requirements.txt
```

安装 Node 依赖：

```
Set-Location skills/xhs-apis/scripts
npm install
```

查看当前可用方法：

```
python skills/xhs-apis/scripts/xhs_api_tool.py list
```

## 说明

- 仓库会保留 skill 所需的标准文件，例如 `SKILL.md`、`agents/openai.yaml`、`references/` 与 `scripts/`。
- vendored runtime 已裁剪为仅支持 `xhs_pc_apis.py` 和 `xhs_creator_apis.py` 所需的最小文件集合。


## 📈 Star 趋势

<a href="https://www.star-history.com/#cv-cat/XhsSkills&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=cv-cat/XhsSkills&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=cv-cat/XhsSkills&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=cv-cat/XhsSkills&type=Date" />
  </picture>
</a>

---

## 🍔 交流群

如果你对爬虫和 AI Agent 感兴趣，请加作者主页 wx 通过邀请加入群聊

ps: 请加群11、12，人满或者过期 issue | wx 提醒

![group11](https://github.com/user-attachments/assets/7fdded35-52ca-4bcb-a5b7-935928ed417c)

![group12](https://github.com/user-attachments/assets/8dd858be-5843-4074-a2d5-fc48b3d61856)


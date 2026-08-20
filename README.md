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

## 与 Spider_XHS 的同步关系

- `XhsSkills` 中的运行时代码来自 `Spider_XHS` 的裁剪版本，当前并非自动实时同步。
- 当前锁定的上游基线版本记录在 `skills/xhs-apis/upstream.json` 中。
- 当 `Spider_XHS` 上游更新时，维护者需要人工评估相关的 API 与签名变更，仅同步 `XhsSkills` 实际需要的文件，并在同步完成后更新 `upstream.json`。


## 📈 Star 趋势


<a href="https://cvcat.site/star-history/svg?repos=cv-cat/XhsSkills&type=Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://cvcat.site/star-history/svg?repos=cv-cat/XhsSkills&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://cvcat.site/star-history/svg?repos=cv-cat/XhsSkills&type=Date" />
    <img alt="Star History Chart" src="https://cvcat.site/star-history/svg?repos=cv-cat/XhsSkills&type=Date" />
  </picture>
</a>

---

## 🍔 交流群

如果你对爬虫和 AI Agent 感兴趣，可以加入群聊一起讨论~

ps: 请加群，人满或者过期 issue | wx 提醒 | qq提醒

| group-1 | group-2 | group-3 | group-4 (2000人qq群) |
|:--:|:--:|:--:|:--:|
| <img width="280" alt="group1" src="https://cvcat.site/assets/group1.jpg" /> | <img width="280" alt="group2" src="https://cvcat.site/assets/group2.jpg" /> | <img width="280" alt="group3" src="https://cvcat.site/assets/group3.jpg" /> | <img width="280" alt="group3" src="https://cvcat.site/assets/group4.jpg" /> |




---
name: xhs-apis
description: Use this skill when you need to call the vendored Xiaohongshu/XHS APIs from Spider_XHS for PC web data or creator-platform publishing data. This skill only wraps the APIs in xhs_pc_apis.py and xhs_creator_apis.py, including note, user, search, comment, topic, location, media upload, note publishing, and creator published-note queries.
---

# XHS APIs

## Overview

Use this skill to run the vendored `Spider_XHS` APIs for XHS PC and creator-platform workflows.
This skill only exposes the methods defined in `xhs_pc_apis.py` and `xhs_creator_apis.py`.

## Quick Start

1. Install Python dependencies:

```powershell
pip install -r skills/xhs-apis/scripts/requirements.txt
```

2. Install Node dependencies:

```powershell
npm --prefix skills/xhs-apis/scripts install
```

3. Inspect available methods:

```powershell
python skills/xhs-apis/scripts/xhs_api_tool.py list
```

4. Call an API:

```powershell
python skills/xhs-apis/scripts/xhs_api_tool.py call pc get_note_info --params "{\"url\":\"https://www.xiaohongshu.com/explore/...\",\"cookies_str\":\"a1=...; web_session=...\"}"
```

## Workflow

- Use the `pc` namespace for public-site note, user, search, comment, message, and feed APIs.
- Use the `creator` namespace for creator-platform topic lookup, location lookup, media upload, note publishing, and published-note queries.
- If you are unsure which method to use, run `list` first or read [api-index.md](references/api-index.md).

## Parameter Rules

- `pc` methods mostly expect `cookies_str`.
- `creator` source methods often expect a `cookies` dict. The CLI accepts either `cookies` or `cookies_str` and converts automatically.
- For creator file inputs, pass file paths in JSON. The CLI reads those files into bytes before calling the vendored API.
- For `creator.post_note`, pass `noteInfo.media_type` as `image` or `video`, then provide either `images` or `video`.

## Runtime Notes

- The runtime shipped with this skill is a trimmed vendor copy that keeps only the code needed by `xhs_pc_apis.py` and `xhs_creator_apis.py`.
- The CLI changes into its vendored runtime directory before import so the bundled JS signers can resolve their relative `static/` files.
- If `jsdom` or `crypto-js` errors appear, rerun `npm --prefix skills/xhs-apis/scripts install`.

## References

- Full method inventory and payload notes: [api-index.md](references/api-index.md)

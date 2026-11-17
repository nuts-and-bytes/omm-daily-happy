# 哦莫日常 · omm-daily-happy

一个日常记录网页原型，包含心情、待办和自我探索问题。这个仓库保存单文件构建快照，适合直接预览。

[打开网页](https://nuts-and-bytes.github.io/omm-daily-happy/) · [相关快照仓库](https://github.com/nuts-and-bytes/omm-daily-happiness) · [English](#english)

## 当前内容

- `index.html`：已内联脚本和样式的页面产物。
- 日常界面包含心情、待办、自我探索与记录入口，使用浏览器 LocalStorage 保存相关状态。
- 还保留了历史调剂信息展示模块；其中静态数据不是实时采集结果，请以院校官方信息为准。

两个快照并非完全相同，历史 AI 请求接口和响应处理存在差异。本说明不指定其中任何一个为后续开发主仓库，也不自动合并或删除它们。

## 本地预览

需要 Python 3。

```sh
git clone https://github.com/nuts-and-bytes/omm-daily-happy.git
cd omm-daily-happy
python3 -m http.server 8000
```

打开 <http://localhost:8000/>。仓库未提供原始组件、依赖清单或构建脚本，不适合按常规 React 源码项目运行 `npm install`。

## 边界

- 本次已将历史 HTML 中内嵌的 AI 凭据替换为占位符；AI 按钮会提示尚未配置，不提供可用的内置服务密钥。
- 从当前文件移除凭据不等于撤销凭据，也不会清除 Git 历史；历史凭据仍需在服务商处撤销或轮换。
- 重新启用 AI 前，应先恢复可维护源码并设置服务端凭据管理，不把密钥重新打包进公开 HTML。
- 本地状态不自动同步；清除浏览器数据可能丢失记录。未验证完整移动端、AI 服务或实时数据能力。
- 当前没有独立 `LICENSE` 文件，许可证待维护者明确。

## English

A single-file snapshot of a daily reflection prototype with mood, tasks and self-reflection prompts. [Open the page](https://nuts-and-bytes.github.io/omm-daily-happy/) or serve this repository with `python3 -m http.server 8000`.

The repository contains a built HTML artifact rather than editable React source. The historical embedded AI credential has been replaced with a placeholder; AI calls are not configured. Removal does not revoke an exposed credential or erase Git history. Browser data has no automatic sync, and the included historical information module is not a live data feed. No standalone LICENSE file is currently present.

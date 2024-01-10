# zotero-journalabbr

- Forked from `zoushucai/zotero-journalabbr`
- Based on release v0.3.1 (Nov 15, 2022) for Zotero 6
- **For self use only**

## Updates

All updates have been tested in Zotero 6 (v6.0.30), on Windows 10 Professional Education version 2009

### 2023.03.10, v0.3.1.1
- Remove useless functions and modify entries in right-click menu for clarity
- Fix some errors in the journal abbreviation list

### 2023.10.09, v0.3.1.2
- Add new function `updateJournalAbbrAdded()`, for automatically updating journal abbreviation in the modified version of [Zotfile](https://github.com/liuyujie0136/zotfile/)

### 2024.01.04, v0.3.1.3
- Fix some errors in the journal abbreviation list


## Original README
- 自用, 主要的功能是对 zotero 中的期刊进行缩写
- 安装该插件以后, 直接选中条目右键, 找到 `期刊缩写` -->`更新期刊缩写` , 并点击,则可以执行期刊缩写任务
- 期刊缩写的来源: [JabRef/abbrv.jabref.org](https://github.com/JabRef/abbrv.jabref.org), 我对其进行了整合,

  - 删除了一些特殊的期刊, 比如期刊中还有 单双引号, 单反斜杠
  - 删除了期刊字符超过 80 以及期刊字符小于5的期刊
  - 对于带点的优先顺序 `点的个数 > 大写个数> 缩写短的`
  - 对于不带点的优先顺序 `不带点的个数 > 大写个数> 缩写短的`, 参考[zoushucai/zotero-journalabbr-nodot](https://github.com/zoushucai/zotero-journalabbr-nodot)

- 仅在 `mac` 平台上进行测试

### 自定义期刊缩写数据库

- 可以更改 `chrome/content/scripts/journalabbrbyzsc.js` 文件来定义新的数据库,用的是 json 格式来定义的. 然后, 在主目录下执行,`bash build.sh` 即可生成新的插件
- 可以添加自己 csv 数据库, 数据格式要求, 第一列是原始期刊的 title, 第二列是缩写期刊, 中间用分号隔开(注意:如果用 excel 打开的话,默认是用的逗号,要注意) , 不需要列名

# OpenMdicts

词典数据全部提取到可读格式，便于编辑。为redictionary的开发作一些基础。

> Work in progress

## Format

The current text is directly exported from mdx files, and processed by replacing undocumented syntax with html. Still, the content and its styling and other unrelated stuff are interweaved. This issue will be left as is until I decide to get a new format, open dictionary format or something.

[Proposed readable format for editing](./dict.yaml)

And it will get serialized when preparing for software releases. Then redictionary would load it into memory, searching it with a nodejs fulltext engine or simply regex.
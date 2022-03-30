# OpenMdicts

词典数据全部提取到可读格式，yaml，便于编辑。为redictionary的开发作一些基础。

## Format

All data from mdx files are extracted and stored into yaml. Currently there are a lot of errors in it. Yaml was chosen for its readability, and because the form of dictionary content often varies. Later the data could be stored in bson and indexed by nosql for application uses. 

List of dictionaries (by priority):

- [x] 简明英汉汉英词典（Chinese-English）
- [x] 21世紀電腦英漢漢英雙向辭典
- [x] 汉语大词典(简体精排)（Chinese+Literary Chinese）
- [x] 柯林斯COBUILD高阶英汉双解学习词典

## From

```bash
node cli-utility --export -f static/简明英汉汉英词典.mdx -d ../OpenMdicts  
node cli-utility --export -f static/21世紀電腦英漢漢英雙向辭典.mdx -d ../OpenMdicts
node cli-utility/index.js --export -f static/汉语大词典\(简体精排\).mdx -d ../OpenMdicts/
```
# OpenMdicts

词典数据全部提取到可读格式，yaml，便于编辑。为redictionary的开发作一些基础。

## Format

All data from mdx files are extracted and stored into yaml. Currently there are a lot of errors in it. Yaml was chosen for its readability, and because the form of dictionary content often varies. Later the data could be stored in bson and indexed by nosql for application uses. 

List of dictionaries (by priority):

- [x] 简明英汉汉英词典（Chinese-English）
- [x] 21世紀電腦英漢漢英雙向辭典
- [x] 汉语大词典(简体精排)（Chinese+Literary Chinese）
- [x] 柯林斯COBUILD高阶英汉双解学习词典

Samples:

```yaml
# 简明英汉汉英词典
- word: internal
  definitions:
    - type: adj.
      CN: 内部的
      examples:
        - CN: 他正在内线电话上与汤姆交谈。
          EN: He is talking to Tom on the internal telephone.
        - CN: 掌握了事物的内部联系你就不难理解这个世界。
          EN: >-
            It's not difficult to understand this world when you mastered the
            internal relations of things.
    - type: adj.
      CN: 国内的, 内政的
      examples:
        - CN: 这个国家的内部情况很乱。
          EN: The nation's internal affairs are bad.
    - type: adj.
      CN: 体内的
      examples:
        - CN: 他在一次意外事故中受了内伤。
          EN: He suffered internal injuries in an accident.
# 21世紀電腦英漢漢英雙向辭典
- definitions:
    - definitions:
        - CN: ‘希腊神话’崔坦
          examples:
            - Triton among the minnows
            - CN: 鹤立鸡群
              EN: Triton among the minnows
        - CN: ((在平庸的人群中特别杰出的人))
      etymology:
        - ((人头人身鱼尾海神, 为波赛顿 (Poseidon) 之子, 吹海螺在海上兴风作浪或使风平浪静))
      pronunciation:
        - "`traɪtn"
        - ˈtraitn
      title: Tri.ton
      type: 名词
    - definitions:
        - CN: ‘动物’梭尾螺; 梭尾螺壳; 蝾螈
      pronunciation:
        - "`traɪtn"
        - ˈtraitn
      title: tri.ton
      type: 名词
    - definitions:
        - CN: 氚核
      etymology:
        - ((有两个中子和一个质子))
      pronunciation:
        - "`traɪˌtɑn"
        - ˈtraitɔn
      title: tri.ton
      type: 名词
  index: 120037
  word: Triton
# 汉语大词典
- definitions:
    - CN: 干扰，扰乱。
      examples:
        - 元杨显之《酷寒亭》第二摺：“我如今洗剥了，慢慢的打你，待我关上门，省的有人来打搅。”
        - 《老残游记》第七回：“立刻便要传出号令：某人立足之地，不许打搅。”
        - 冰心《庄鸿的姊姊》：“天冷人静，我似乎无家可归了，忽然想起你来，所以就来找你谈话，却打搅了你们姊弟怡怡的乐境。”
    - CN: 犹打扰。受人招待或请人帮助时表示谢意之词。
      examples:
        - 元乔吉《扬州梦》楔子：“多有打搅，小生不敢久留，就此告辞长行去也。”
        - 《英烈传》第十七回：“我在此打搅了一番，自然算房钱、饭钱、酒钱还你。”
        - 曹禺《日出》第三幕：“对不起，打搅你们了。”
    - CN: 搅动。
      examples:
        - 明吕坤《呻吟语·天地》：“譬之一盆水，打搅起来，大小浮沤以千万计，原是假借成的，少安静时，还化为一盆水。”
  index: 120035
  word: 打搅
# 柯林斯COBUILD高阶英汉双解学习词典
- definitions:
    - CN: 由选举产生的;选任的
      EN: >-
        An elective post or committee is one to which people are appointed as a
        result of winning an election.
      examples:
        - CN: 布坎南从未就任过经选举产生的职位。
          EN: Buchanan has never held elective office.
      info: 【搭配模式】：usu ADJ n 【语域标签】：FORMAL 正式
      type: "ADJ\t形容词"
    - CN: （外科手术）非急需的，可选择的
      EN: >-
        Elective surgery is surgery that you choose to have before it becomes
        essential.
      info: 【搭配模式】：usu ADJ n 【语域标签】：FORMAL 正式
      type: "ADJ\t形容词"
    - CN: 选修课
      EN: >-
        An elective is a subject which a student can choose to study as part of
        his or her course.
      examples:
        - CN: 选修课包括太极拳和高级舞蹈练习。
          EN: Electives are offered in Tai Chi and advanced dance exercise.
      info: 【语域标签】：AM 美
      type: "N-COUNT\t可数名词"
  index: 10105
  tip:
    - in BRIT, use 英国英语用 option
  word: elective
```

## From

```bash
node cli-utility --export -f static/简明英汉汉英词典.mdx -d ../OpenMdicts  
node cli-utility --export -f static/21世紀電腦英漢漢英雙向辭典.mdx -d ../OpenMdicts
node cli-utility/index.js --export -f static/汉语大词典\(简体精排\).mdx -d ../OpenMdicts/
```


MainPartExtractor
=================

主谓宾提取器的Java实现

提取中文句子主干
--

 - 调用方法
 
```java
    public static void main(String[] args)
    {
        String[] testCaseArray = {
                "我一直很喜欢你",
                "你被我喜欢",
                "美丽又善良的你被卑微的我深深的喜欢着……",
                "只有自信的程序员才能把握未来",
                "主干识别可以提高检索系统的智能",
                "这个项目的作者是hankcs",
                "hankcs是一个无门无派的浪人",
                "搜索hankcs可以找到我的博客",
                "静安区体育局2013年部门决算情况说明",
                "这类算法在有限的一段时间内终止",
        };
        for (String testCase : testCaseArray)
        {
            MainPart mp = MainPartExtractor.getMainPart(testCase);
            System.out.printf("%s\t%s\n", testCase, mp);
        }
    }
```
 - 编译说明
 
 请使用Maven编译，会自动下载依赖项。
 - 算法详解
 
 利用依存关系可以提取句子的主要成分(也就是小学和公务员考试中出现的“提取主干”)，可以实现语义上的智能理解。
 详见[《提取中文句子主谓宾的Java实现》][1]

  [1]: http://www.hankcs.com/nlp/chinese-sentences-svo-java-extraction.html
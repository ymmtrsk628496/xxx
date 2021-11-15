# 外株用TruValueファクター開発

## About
[TruValueデータ](https://insight.factset.com/resources/at-a-glance-truvalue-labs-insight360-datafeed)を用いて[KOKUSAI](https://www.msci.com/search?keywords=KOKUSAI)に有効な新ファクターを開発する．

### What is TruValue?
TruValueスコアは企業のESG行動を評価したスコアであり，4つのタイプに分類される．
- Pulse
    ```math
    {Pulse}_t = 
    ```
- Insight
- Momentum
- Volume

![tv_4type](https://insight.factset.com/hubfs/Resources%20Section/OpenFactSet%20Partner%20Profiles/Truvalue%20Labs/4%20Insight%20360%20Score.png)


## Plan
### Flow
```flow
st=>start:>http://www.google.com[blank]
e=>end:>http://www.google.com
op1=>operation: Basic analysis of all-catecory-score for each TruValue type
op2=>operation: Identify the kye points for alpha.
para=>parallel: Select the importance to key

st(right)->op1
op1->op2
op2->para(path1, top)
```

### Schedule
```mermaid
gantt
    title Create a new factor for KOKUSAI
    dateFormat YYYY-MM-DD
    section Basic <br/> Analysis of <br/> all-category <br/> -score
    Optimize dev. env.:done,  a1, 2021-11-01, 3d
    Calcultate statistics:done, a2, after a1, 11d
    Calculate IC, Q1uantile, Turnover, Coverage:done, a3, after a1, 11d
    Calculate region specific:done, a4, after a1, 11d
    Calculate sector specific:done, a5, after a1, 11d
    Summarize :a6, after a2, 3d

    section Basic <br/> Analysis for  <br/> each <br/> materiality
    Calcultate statistics: b1, after a6, 21d
    Calculate IC, Q1, ...: b2, after a6, 21d
    Calculate region specific: b3, after a6, 21d
    Calculate sector specific: b4, after a6, 21d

    section Create factors
    Idntify key points: b1, after a6, 3d  
    another task: 24d

    section Evaluate factors
    Evaluation (IC, Quantile): b1, after a6, 3d  
    Submition: : b1, after a6, 3d  
```

## What is important?

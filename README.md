# Strategy to create new factor

## Schedule
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

```mermaid
gantt
    title Create a new factor for KOKUSAI
    dateFormat YYYY-MM-DD
    section Basic <br/> Analysis of <br/> all-category <br/> -score
    Optimize dev. env.: a1, 2021-11-01, 3d
    Calcultate statistics: after a1, 11d
    Calculate IC, Q1, ...: a2, after a1, 11d
    Summarize :after , after a2, 3d
    section Create factor
    Task in sec      :2021-12-31  , 12d
    another task      : 24d
```

## What is important?
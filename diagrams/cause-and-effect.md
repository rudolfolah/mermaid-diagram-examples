> Cause and effect diagrams are useful because they let you list out all the causes that you and/or your team can think of.
> 
> ...
> 
> Having a team think of possible causes is similar to the concept of peer review in software development projects. Where one person thinks of a few causes, another person will think of different causes. This gives a broader range of causes to investigate.
> 
> -- Rudolf Olah, ["Cause and Effect Diagrams"](https://rudolfolah.com/cause-and-effect-diagrams/)

The following are diagrams that are featured in the article ["Cause and Effect Diagrams"](https://rudolfolah.com/cause-and-effect-diagrams/).

## Simple Approach to Cause and Effect Diagrams

### Flowchart

```mermaid
---
title: Simple Approach to Cause and Effect Diagrams (Flowchart)
---
flowchart TD
    a[Cause A]
    b[Cause B]
    c[Cause C]
    d[Cause D]
    e[Cause E]
    problem --> a & b
    a --> c
    b --> d & e
```

### Mindmap

```mermaid
---
title: Simple Approach to Cause and Effect Diagrams (Flowchart)
---
mindmap
root((Problem)
  Cause A
    Cause C
  Cause B
    Cause D
    Cause E
```


## Systemic Approach to Cause and Effect Diagrams
Systemic approach uses _categories_ and _templates_ to make finding the root cause simpler.

```mermaid
---
title: Systemic Approach to Cause and Effect Diagrams
---
mindmap
  root((Problem))
    Category A
      Cause A
        Cause C
    Category B
      Cause B
        Cause D
        Cause E
    Category C
      Usual Cause A
      Usual Cause B
    Category D
      Usual Cause C
      Usual Cause D
```

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
root((Problem))
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

## MVPS: IT Project Causes
```mermaid
mindmap
root{{IT Project Problem}}
  (Material<br/>Hardware/Software)
  (Vendors)
  (People)
  (Systems)
```

## MCPS: Software Development Project Causes
```mermaid
mindmap
root{{Software Development<br/>Project Problem}}
  (Method)
  (Code)
  (People)
  (Systems)
```

## Marketing Common Causes
```mermaid
mindmap
root{{Marketing Problem}}
  (Product/Service)
    Cause
  (Price)
    Cause
    Cause
  (Place)
    Cause
  (Promotion)
    Cause
  (People/personnel)
  (Process)
    Cause
      Cause
  (Physical Evidence)
    Cause
  (Publicity)
    Cause
```

## Manufacturing Common Causes
```mermaid
mindmap
root{{Manufacturing Problem}}
  (Machine)
  (Method)
  (Material)
  (Man Power/Mind Power)
  (Measurement)
```

## Service Industry Common Causes

```mermaid
mindmap
root{{Service Problem}}
  (Surroundings)
  (Suppliers)
  (Systems)
  (Skills)
```

## Case Studies

### Low Developer Velocity: Causes and Effects
```mermaid
mindmap
root{{Low Developer Velocity}}
  (Method)
    too many meetings
    lack of proper planning
    lack of agile methodologies
    unclear requirements
  (Code)
    too much technical debt
      not enough tests
      outdated technology
      code duplication
      tightly coupled components
      inconsistent coding standards
    complex codebase
    lack of proper documentation
  (People)
    lack of necessary skillsets
    inadequate team size
    high employee turnover
    communication barriers among team members
    insufficient onboarding and training
    burnout and low morale
  (Systems)
    development servers are down
      server hardware is failing
      firewall rules are incorrect
      domain name setup is incorrect
      went over the billing limit
    slow or unstable development environment
    lack of proper development tools
    inadequate version control system
    insufficient testing infrastructure
```

### Server Procurement Takes Too Long: Causes and Effects
```mermaid
mindmap
root{{Server Procurement Takes Too Long}}
  (Material)
    not sure what hardware requirements to use as a baseline
    obsolete hardware specifications
    high demand for specific hardware components
  (Vendors)
    convoluted, slow billing process
    limited vendor options
    long lead times for hardware delivery
    inconsistent communication from vendors
  (People)
    too many approvals required
    unclear when costs for server are passed to client
    client is unwilling to procure server
      budget unavailable until milestone is met
      does not see the need for the server
      already has on premises servers
      client does not want to use public cloud infrastructure
    lack of dedicated procurement personnel
    miscommunication between teams
  (Systems)
    procurement is not automated
    outdated procurement software
    lack of integration between procurement and project management tools
    manual tracking of procurement status
```

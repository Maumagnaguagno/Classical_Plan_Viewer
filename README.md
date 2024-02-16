# Classical Plan Viewer
**Graph visualization of classical plans**

Convert a JSON plan into a [DOT](https://www.graphviz.org/doc/info/lang.html) graph to be client-rendered using [d3-graphviz](https://github.com/magjac/d3-graphviz).
The plan format is made of an array of action objects, each action with at least a name, arrays of parameters, preconditions and effects.
Arrays can be empty, while all leaf elements are strings.
The input format and visualization can be modified to support more elements.

```Json
[
  {"action": "a1",
   "parameters": ["a", "b"],
   "precondition": ["pred1 a", "pred2", "not = a b"],
   "effect": ["not pred1 a", "pred1 b"]},
  ...
]
```

A URL query can be used to load a JSON file already hosted online.

```
https://maumagnaguagno.github.io/Classical_Plan_Viewer?from=https://maumagnaguagno.github.io/Classical_Plan_Viewer/plan.json
```

This project is the counterpart of [HTN Plan Viewer](../../../HTN_Plan_Viewer).
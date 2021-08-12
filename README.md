# Classical Plan Viewer
**Graph visualization of classical plans**

Convert a JSON-based user-provided plan into a [DOT](https://www.graphviz.org/doc/info/lang.html) graph to be client-rendered using [d3-graphviz](https://github.com/magjac/d3-graphviz).
The plan format is made of an array of action objects, each object with an action name, arrays of parameters, preconditions and effects.
Arrays can be empty, while all leaf elements are strings.
The input format and visualization may change to support more elements, use with caution.

```Json
[
  {"action": "a1",
   "parameters": ["a", "b"],
   "precondition": ["pred1 a", "pred2", "not = a b"],
   "effect": ["not pred1 a", "pred1 b"]
  },
  ...
]
```

Modify the ``toDOT(plan)`` function to return a different DOT description to be visualized.  
This project is the counterpart of [HTN Plan Viewer](../../../HTN_Plan_Viewer).
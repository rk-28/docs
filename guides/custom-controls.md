TODO: Big thing for us to decide is whether the control or the action/behavior should be
the top level (eg view-toggle vs button-group). Pretty sure we want the behavior
to be top level. Just easier to understand what the controls are doing at a
quick glance.

### Color legend

**Example**

```
color-legend {
  direction: vertical;
  colors: red "Red things", blue "Blue things";
}
```

**Supported properties**

- direction: vertical (default) or horizontal
- colors:
  - color "label", color "label", etc 
  - inherit (will try to build from element-color/connection-color settings)

**Advanced usage**

This control also supports nested `color` blocks for advanced use cases:

```
color-legend {
  direction: vertical;
  
  color {
    value: red;
    label: "Red things";
  }
  
  color {
    value: blue;
    label: "Blue things";
  }
}
```

Supported properties for `color` blocks:
- value 
- label
- selector

### Map select

Once maps control which views are relevant we can allow the current view
to carry across map changes (if relevant to the new map).

```
map-select {
  type: toggle-one; // toggle-one or select-one
}
```

### View select

```
view-select {
  type: toggle-one;
}
```

### View toggle

Allows you to turn on multiple views / partials at the same time.

```
view-toggle {
  // shorthand
  views: "View one", "View two";
  views: pers-123, pers-234;

  // nested?
  view {
    label: "
  }
}
```

### Cluster

```
// behavior-driven approach
cluster {
  option {
    value: person by "skills offered" as "Skill";
    label: "By offers";
  }
  
  option {
    value: person by "skills needed" as "Skill";
    label: "By needs";
  }
}

// control-driven approach
button-group {
  type: toggle-one; 
  action: cluster;
  
  button {
    value: "element type";
    label: "By type";
  }
}
```

### Control groups

Groups allow you to place components side-by-side instead of stacking on top of each other.

```
group {
  stat {
    value: element-count;
    label: "Elements";
  }
  
  stat {
    value: connection-count;
    label: "Connections";
  }
}
```

### Stat

Include map-level stats.

```
stat {
  value: count(person);
  label: "People";
}
```

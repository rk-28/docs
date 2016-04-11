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

### Cluster toggle

```
// control-driven approach
button-group {
  type: toggle-one; 
  action: cluster;
  
  button {
    value: "element type";
    label: "By type";
  }
}

// behavior-driven approach
cluster {
  type: toggle-many;
  selector: *;

  cluster-option {
    value: "element type";
    label: "By type";
    // selector?
  }
  
  cluster-option {
    value: "location";
    label: "By location";
  }
}
```

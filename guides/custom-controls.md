TODO: Big thing for us to decide is whether the control or the action/behavior should be
the top level (eg view-toggle vs button-group). Pretty sure we want the behavior
to be top level. Just easier to understand what the controls are doing at a
quick glance.

Here's some inspiration for how we might document the controls:
https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIToolbar.html#//apple_ref/doc/uid/TP40012857-UIToolbar-SW1

### Title

```
title {f
  value: "The map title";
}
```

### Text

```
text {
  value: "This is for longer text.";
}
```

### Label

```
label {
  value: "This is for small bold labels.";
}
```

### Color legend

**Example**

```
// inherited colors
color-legend {
  colors: inherit;
}

// explicit colors
color-legend {
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

**Supported properties**

- direction: vertical (default) or horizontal
- colors:
  - color "label", color "label", etc 
  - inherit / inherit-element-color (build from @settings)

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
  cluster-option {
    value: person by "skills offered" as "Skill";
    label: "By offers";
  }
  
  cluster-option {
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

### Toolbar

```
toolbar {
  toolbar-button {
    action: filter;
    label: "Filter";
    icon: filter;
  }
  
  toolbar-button {
    action: focus;
    label: "Focus";
    icon: focus;
  }
}
```

### Tagged Timeline

TODO: include vs ignore, select one or many

```
tagged-timeline {
  range: 2007..2016; // required
  target: element;   // optional, defaults to *
}
```

### Filter

```
filter {
  type: toggle-many;
  target: element; // optional, defaults to *
  field: "state";
  values: auto;
  multiple: true;
}

filter {
  type: select;
  
  filter-option {
    selector: 
  }
}
```

### Field filter

```
field-filter {
  field: "State"; // required
  values: auto;   // optional, defaults to auto
  multiple: true; // optional, defaults to false
  required: true; // optional, defaults to false to allow selection to be cleared
  as: dropdown;   // optional, either dropdown | buttons | labels
}

field-filter {
  field: "State";
  values: Alabama, Alaska, ...;
}

field-filter {
  field: "State";
  
  option {
    label: Hawaii;
    value: HI;
  }
  
  ...
}
```

### Dropdown

```
dropdown {

}

dropdown {
  dropdown-option {
    label: "Hawaii";
    value: "HI";
  }
}
```

### Adjust

For toggling inline partials on/off

```
???
```

### Toggle

I don't think generic top-level controls will work but just want to flush out what they might look like.

```
toggle {
  type: simple; // simple, pillselect
  style: subtle;
  multiple: true;
  
  toggle-option {
    label: "2008";
    selector: element[year~=2008]; // selector or target?
    
    declarations {
      display: none;
    }
  }
}
```

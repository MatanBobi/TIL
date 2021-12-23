## Explanation

When using native HTML `select` element, an auto role is being assigned.  
This role by default is `combobox` but if you add `multiple` attribute to your select, the assigned role will now be `listbox`.  

Relevant references:  
[The ARIA HTML spec for select](https://w3c.github.io/html-aria/#el-select-multiple-or-size-greater-1)  
[The combobox role spec](https://www.w3.org/TR/wai-aria-1.1/#combobox)  
[The listbox role spec](https://www.w3.org/TR/wai-aria-1.1/#listbox)  

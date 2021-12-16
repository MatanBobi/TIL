## Problem

When writing markdown, you sometimes want github to render different image on light mode than dark mode.

## Solution
We can provide the theme context in the markdown image.

>
> This solution is a github only solution., 

```markdown
![GitHub-Mark-Light](https://user-images.githubusercontent.com/3369400/139447912-e0f43f33-6d9f-45f8-be46-2df5bbc91289.png#gh-dark-mode-only)![GitHub-Mark-Dark](https://user-images.githubusercontent.com/3369400/139448065-39a229ba-4b06-434b-bc67-616e2ed80c8f.png#gh-light-mode-only)
```

This markdown will create the following behavior:
![image](https://user-images.githubusercontent.com/12711091/146358424-7a0722be-969f-4d5b-a8dd-3addab420f7d.png)

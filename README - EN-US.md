# Leap-Motion-Unity-2021

## Leap motion error for unity in 2021, failing to compile.

- The error happens not allowing to play in the environment created with a leap motion, after importing the CORE.

- This happens because there is a flaw in the Hotkeys.cs file causing some parameters to be obsolete for the new versions and preventing the core from running.

### Error

The error appears in the line of code, as we can see in the image below in red:

![Hotkeys](https://user-images.githubusercontent.com/33674966/140668139-a9c97be9-02a1-4db9-af5a-75545a6857a1.jpg)

## Fixing

### Steps to fixing

- [ ] Find code snippet that contains error.
- [ ] Replace in first part
- [ ] Find too many parts with error
- [ ] Replace snippets
- [ ] Delete code header comments

1. Change the code

```
      GameObject[] objs = Selection.GetFiltered<GameObject>(SelectionMode.Editable);
      if (objs.Length == 0) {
        return;
      }
```

- [X] Find code snippet that contains error.
- [X] Replace in first part
- [ ] Find too many parts with error
- [ ] Replace snippets
- [ ] Delete code header comments

2. After changing this code snippet, you must change all others that appear ** _ (SelectionMode.ExcludePrefab | SelectionMode.OnlyUserModifiable | SelectionMode.Editable) _ ** to just ** _ (SelectionMode.Editable) _ **

- [X] Find code snippet that contains error.
- [X] Replace in first part
- [X] Find too many parts with error
- [X] Replace snippets
- [ ] Delete code header comments

3. Delete the comments in lines ** 1 ** to ** 8 **

- [X] Find code snippet that contains error.
- [X] Replace in first part
- [X] Find too many parts with error
- [X] Replace snippets
- [X] Delete code header comments

## Conclusion

- After these steps, leap motion will work normally, thus being able to load the other packages.

 ![4185b53d71c0d7e7995f51aee3c6cbcd](https://user-images.githubusercontent.com/33674966/140669197-488eba36-8c8b-4c48-8f9c-a092e91509b5.gif)

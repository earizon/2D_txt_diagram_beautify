
# Apropos

This Keep it simple and stupid script (KISS) lets you draw 2D diagrams
with your keyboard and then, beautify them with Unicode.

Example:

```

    ORIGIN TEXT            BEAUTIFIED
     DIAGRAM              OUTPUT DIAGRAM
  ---------------         ---------------
  Example 1:
    /----v----\             ┌────┬────┐
    |    |    |             │    │    │
    }----+----{             ├────┼────┤
    |    |    |             │    │    │
    \----^----/             └────┴────┘
                       
  Example 2:

  }- level 1.1            ├─ level 1.1
  |  |                    │  │
  |  }- level 2.1         │  ├─ level 2.1
  |  |                    │  │
  |  \- level 2.2         │  └─ level 2.2
  |                       │
  \- level 1.2            └─ level 1.2

 NOTE: github use a CSS line height "too tall".
       vertical lines do not look so "beautiful" :(/
       It will look much better in your console,
       IDE or some other markdown viewer with better
       CSS default.
```

# Writing Rules:

  ```
     ┌─········· ORIGINAL TEXT (easy to type in your keyboard)
     ·    ┌─···· FINAL TEXT    (beautified output)
     v    v
    /-    ┌─

    -v-   ─┬─

    -\    ─┐

    }-    ├─

    -+-   ─┼─

    -{    ─┤

    \-    └─

    -^-   ─┴─

    -/    ─┘
  ```

# PRESETUP:

* Copy and place the script into your PATH.
* make it executable For example:

  ```sh
  chmod a+x ~/bin/b
  ```

# Daily use:

  ```sh
  $ cat input_2d.txt  | b > output_2d.txt
  ```

# TIPs:

- Consider using an editor with column and/or block mode
  support to "draw" in 2D.
  For example, to enter "block mode" edition in vim just
  press: `[esc] ─> Ctrl+v`

- Some editors (vim, Visual Code Studio, ....) allow to pass
  selected text as input to a command, then the output is
  replaced inside the text being edited.
  For example, in vim:
  1. Select text like:
     ```
     [esc] -> v -> "move around" lines
     ```
  2. Pass selected text to b(eautify) like:
     ```
     :.! b
     ```

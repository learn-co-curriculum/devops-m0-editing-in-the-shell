# Editing Text in the Shell

## Learning goals

- Learn how to edit text in the shell
- Understand the pros and cons of editing text in the shell
- Learn the basics of `nano`

## Introduction

Often times, you'll find that you want to edit text in the shell itself, instead of complicating yourself with setting up remote editing in your own favorite editor of choice. We'll explore using your own editor with those protocols in a future module, but for the time being, editing text using command-line tools is more than enough. 

There are quite a few advantages to using the shell/terminal to edit text:

- **Speed**: Editing text in the shell can actually be faster than using a graphical text editor, especially if you are already working in the shell and don't want to bother switching to a different program.
- **Remote access**: Often times, if you log-in to a remote server, you will not have access to a graphical text editor. In this case, using a CLI text editor can be the only way to edit files on that remote system.
- **Scripting**: You can use shell commands like the ones we went over in the previous chapters to automate tasks or perform multiple actions.

With that out of the way, we should begin by taking a look at two of the most popular CLI text editors: `nano` and `vim`.

`nano` and `vim` are both command-line text editors, but they share some fundamental differences. **Nano** is a simple and beginner-friendly editor that provides a straightforward interface and relatively basic editing functionality. **Vim**, on the other hand, is far more advanced and capable, known for its powerful and efficient editing capabilities, but has a steep learning curve as it relies on keyboard shortcuts for most tasks.

Both editors are very popular and come preinstalled on the majority of *Linux/UNIX* operating systems (e.g. MacOS, Ubuntu, etc.) In general, you can't go wrong with either one, though you will find it hard to work on more complex codebases with `nano` in general. 

In this lesson we'll go over how to use Nano, and we'll dedicate the next one to Vim.

## Nano

To begin using nano, simply use the `nano` command followed by the name of the file you want to edit, for example:

```bash
$ nano file.txt
```

You should now be in the `nano` editor! At the bottom of the screen you will see a list of commands with their respective keybinds: you can always fall back to these when in doubt.

As with most editors, if the file doesn't exist, `nano` will create it for you the moment you save. If it exists, you will see the contents of that file displayed in the editor.

To edit, type or delete text as needed as you would in a standard graphical text editor. To move around, simply use the arrow keys.

To save, you can press `Ctrl+o`, after which `nano` will ask you to confirm the file name. Just press `Enter` to save the file.

You can exit the editor by pressing `Ctrl+x`. If you have unsaved changes, `nano` will ask if you want to save the changes made. Just press `y` or `n` whether you want to save the changes or not.

Some other useful commands in Nano are:

- `Ctrl+k`: Cuts/deletes a line of text.
- `Ctrl+u`: Pastes text that has been cut/copied.
- `Ctrl+w`: Searches for a specific word/phrase in the file.
- `Ctrl+g`: Accesses the `nano` help menu, which provides a list of commands and their keystrokes.

## Conclusion

Using CLI text editors is an extremely important skill to learn as a developer of any kind. At times you need to remote into a server without a GUI, need to edit text files from the CLI (maybe as part of a script/automation process), or maybe just want a lightweight and fast way of editing text.

While `nano` can definitely hold its own, it doesn't quite lend itself to the most efficient way of editing, which can become quite cumbersome for more complex tasks like editing in a codebase. That's why next chapter we'll go over `vim` and how to make use of it!

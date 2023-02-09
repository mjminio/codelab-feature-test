# CodeLab Test Repo

This repo contains example code for testing the functionality of the CodeLab VSCode plugin.

---

## Test CodeLab Specific Commands

### `{{ execute }}` command

If you want to execute a command with a button click, enclose the commands in `` and add {{ execute }} after.

List files on Mac/Linux
`ls -lah` {{ execute }}

List files on Windows
`dir` {{ execute }}

Run a Docker Command
`docker ps -a` {{ execute }}

Run a ping on Mac/Linux
`ping -c 5 google.com` {{ execute }}

Run a ping on Windows
`ping google.com` {{ execute }}

---

### `{{ execute_interrupt  }}` command

If you want to interrupt a command that does not complete on its own, enclose the commands in `` and follow the command with {{ execute interrupt }}.

Start a ping on Mac/Linux
`ping -c 100 google.com` {{ execute }}

Interrupt the ping on Mac/Linux
`Ctrl + C` {{ execute interrupt }}

Run a ping on Windows
`ping -n 100 google.com` {{ execute }}

Interrupt the ping on Windows
`Ctrl + C` {{ execute interrupt }}

---

### `{{ execute T# }}` command

If the user has 2 consoles open side-by-side in VSCode, the leftmost is T1 and the right is T2. You can reference them by adding "T1" and "T2" to the "execute" command.

List files on Mac/Linux in Terminal 1
`ls -lah` {{ execute "T1"}}

List files on Mac/Linux in Terminal 2
`ls -lah` {{ execute "T2"}}

List files on Windows in Terminal 1
`dir` {{ execute "T1"}}

List files on Windows in Terminal 2
`dir` {{ execute "T2"}}

Run "htop" on Linux in Terminal 1
`htop` {{ execute "T1"}}

Run a docker command in Terminal 2
`docker run hello-world` {{ execute "T2"}}

---

### `{{ copy }}` command

If you want to copy some text, provide the text in `` and follow with {{ copy }}.

Copy this text to the clipboard
`This is the special text I want to copy` {{ copy }}

Copy this big block of text
`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.` {{ copy }}

---

### `{{ open }}` command

If you want to open a file, provide the path to the file in `` and follow with {{ open }}.

Open a sample json file
`./sample.json` {{ open }}

---

## Test Core MarkDown & HTML

### Test image embed
<img title="minio logo" alt="minio logo" src="minio.png" width="200">

### Test web links

Visit us at the Minio Website: https://min.io

Visit us at [Min.io](http://min.io)

### Test bullets

- Test bullet 1
- Test bullet 2
  - Test sub-bullet
    - Test sub-sub-bullet

### Test a table

| One  | Two  |  Three  | Four  | Five  |
|---|---|---|---|---|
| 1  |  2 |  3 |  4 | 5  |
|  10 | 20  | 30  | 40  |  50 |
| 100  | 200  | 300  | 400  | 500  |

### Test numbering

1. One
2. Two
3. Three

### Test Text Decoration

# Heading level 1

## Heading level 2

### Heading level 3

#### Heading level 4

##### Heading level 5

###### Heading level 6

*Italics*

**BOLD**

***BOLD ITALIC***

~~strike-through text~~

> Block quote of some lorem ipsum

> Block quote of some lorem ipsum
> WIth multiple lines
>
> of text in the block.

<u> Underline </u> 

`single line code block`

```
# This is some code
Multi
Line
Code
Block
```


# About MinIO

Visit us at [Min.io](http://min.io)
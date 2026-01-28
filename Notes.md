# Notes

## SQLite Basics

- architecture:
```
Tokenizer
    |
    V
Parser
    |
    V
Code Generator
    |
    V
Virtual Machine
    |
    V
B-Tree
    |
    V
Pager
    |
    V
OS Interface
```

- how a SQL query is processed:
```
                 |--- Front End ---|    |--- Back End ----|

(a SQL query) -> [    Tokenizer    ] --> [ Virtual Machine ]
                          |                      |
                          V                      V
                        Parser                 B-Tree
                          |                      |
                          V                      V
                    Code Generator             Pager
                          |                      |
                          V                      V
                      (byte code)           OS Interface
```

- B-tree:
    - stores data of a SQLite database
    - like a binary tree but:
        - each node has many child nodes
        - overall height of tree is shorter
        - tree is always balanced
        - leaf nodes are all at the same level

## Part 2 Notes

- SQLite hard-coded table schema:
```
column      type
id          integer
username    varchar(32)
email       varchar(255)
```

## Part 7 Notes

- todo

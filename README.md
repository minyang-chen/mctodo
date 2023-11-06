# mctodo - CLI Todo App
a simple yet colorful command line utility to keep track of my todo list. 

### Why I need this?
When you want a simple way to keep track of Todo list without leaving a Terminal based environment or integrated this as module to another CLI app. 

## Installation

#### Dependencies

preferer setup own virtual python environment for a clean setup.

```bash
virtualenv venv --python=3.10
then activate the environment
source venv/bin/activate
```
```bash
Method #2 wheel
pip install ./dist/mctodo-0.1.1-py3-none-any.whl
```
or
```bash
Method #1 poetry
poetry install 
```

## Usage

1.Initialize todo persistance file 

```bash
❯ mctodo init
to-do database location? [/home/mc/.mc_todo.json]: 
The todo database is /home/mc/.mc_todo.json
```
2.Add Todo Item

```bash
❯ mctodo add buy coffee bean -p 1
to-do: "buy coffee bean." was added with priority: 1
```
3.View todo list 
```bash
❯ mctodo list
                            my todo list                            
┏━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━┓
┃ ID ┃ Description                              ┃ Priority ┃  Done ┃
┡━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━┩
│  1 │ buy coffee bean.                         │    1     │ False │
│  2 │ book dentist appointment 12:PM/11/11     │    2     │ False │
│    │ friday.                                  │          │       │
│  3 │ call Rick for help to clean engine.      │    3     │ False │
└────┴──────────────────────────────────────────┴──────────┴───────┘
```
4.Mark Todo Complete
```bash
❯ mctodo complete 1 
to-do # 1 "buy coffee bean." completed!
```
5.Remove Todo Item
```bash
❯ mctodo remove 1
Delete to-do # 1: buy coffee bean.? [y/N]: y
to-do # 1: 'buy coffee bean.' was removed
```

## Help Menu
Initialize todo persistance file 

```bash
mctodo --help
                                                                                                                                                        
Usage: mctodo [OPTIONS] COMMAND [ARGS]...                                                                                                                     
                                                                                                                                                        
╭─ Options ───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╮
│ --version             -v        Show the application's version and exit.                                                                                    │
│ --install-completion            Install completion for the current shell.                                                                                   │
│ --show-completion               Show completion for the current shell, to copy it or customize the installation.                                            │
│ --help                          Show this message and exit.                                                                                                 │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯
╭─ Commands ──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╮
│ add                   Add a new to-do with a DESCRIPTION.                                                                                                   │
│ clear                 Remove all to-dos.                                                                                                                    │
│ complete              Complete a to-do by setting it as done using its TODO_ID.                                                                             │
│ init                  Initialize the to-do database.                                                                                                        │
│ list                  List all to-dos.                                                                                                                      │
│ remove                Remove a to-do using its TODO_ID.                                                                                                     │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯

```
## Development Tools
Poetry is a tool for dependency management and packaging in Python.
https://python-poetry.org/docs/

## Contributing
To contribute: Clone the repo locally -> Make a change -> Submit a PR with the change. 

Here's how to modify the repo locally: 
Step 1: Clone the repo 
```
git clone https://github.com/minyang-chen/mctodo.git
```

Step 2: Navigate into the project, and install dependencies: 
```
cd mctodo
poetry install
```

Step 3: Test your change:
```
cd mctodo/tests 
pytest .
```

Step 4: Submit a PR with your changes! 🚀
- push your fork to your GitHub repo 
- submit a PR from there 

## Tool Stack

- Poetry is a tool for dependency management and packaging in Python.
https://python-poetry.org/docs/

- Typer is a library for building CLI applications that users will love using and developers will love creating. 
https://github.com/tiangolo/typer

- Rich is a Python library for rich text and beautiful formatting in the terminal.
https://github.com/Textualize/rich




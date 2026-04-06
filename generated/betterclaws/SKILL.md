---
name: betterclaws
description: Use this skill when working with the betterclaws library. Triggers when user mentions betterclaws or imports from it.
---

# Betterclaws

## What this is
Betterclaws is a Python library designed to simplify the process of building and managing command-line interfaces. It provides an intuitive API for creating commands, handling arguments, and managing output. With betterclaws, developers can focus on writing functional code rather than boilerplate.

## Installation
```bash
pip install betterclaws
```

## Key concepts
The most important APIs in betterclaws include the `Command` class, which represents a single command, and the `Argument` class, which defines a command's arguments. For example:
```python
from betterclaws import Command, Argument

class MyCommand(Command):
    def __init__(self):
        super().__init__("my_command")
        self.add_argument(Argument("foo", help="The foo argument"))
        self.add_argument(Argument("bar", help="The bar argument"))

    def execute(self, args):
        print(f"Foo: {args.foo}, Bar: {args.bar}")
```

## Correct usage patterns
To use betterclaws, create a `Command` subclass and define its arguments using the `add_argument` method. Then, override the `execute` method to handle the command's logic. For example:
```python
from betterclaws import Command, Argument

class MyCommand(Command):
    def __init__(self):
        super().__init__("my_command")
        self.add_argument(Argument("foo", help="The foo argument"))
        self.add_argument(Argument("bar", help="The bar argument"))

    def execute(self, args):
        print(f"Foo: {args.foo}, Bar: {args.bar}")

if __name__ == "__main__":
    MyCommand().run()
```

## Common mistakes to avoid
One common mistake when using betterclaws is forgetting to call the `super().__init__` method in the `Command` subclass's `__init__` method. Another mistake is not overriding the `execute` method, which will result in a default implementation being used.

## File and folder conventions
Betterclaws projects typically have a `commands` folder containing Python files, each defining a single `Command` subclass. The main entry point of the application should be a Python file that imports and runs the desired command. For example:
```python
# commands/my_command.py
from betterclaws import Command, Argument

class MyCommand(Command):
    # ...

# main.py
from commands.my_command import MyCommand

if __name__ == "__main__":
    MyCommand().run()
```
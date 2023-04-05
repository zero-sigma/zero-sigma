```python
import json
from dataclasses import asdict, dataclass


@dataclass
class Stack:
    languages    : tuple = ("Python", "JS/TS", "C++")
    databases    : tuple = ("MySQL", "PostgreSQL", "Redis", "MongoDB")
    libraries    : tuple = ("React", "Vue")
    frameworks   : tuple = ("FastAPI", "Django", "Next.js")
    misc_tech    : tuple = ("Docker", "Celery", "RabbitMQ")

    def serialize(self):
        return json.dumps(asdict(self), indent=4)


stack = Stack()
print(stack.serialize())
```

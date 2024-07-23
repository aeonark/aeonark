```python
from universe.earth import aeonark
from typing import List, Dict, Any

class KnowledgeBase:
    def __init__(self, items: List[str]):
        self.items = items

    def __str__(self):
        return "\n".join(f"- {item}" for item in self.items)

class FutureGoal:
    def __init__(self, goal: str):
        self.goal = goal

    def __str__(self):
        return self.goal

class AboutMe:
    def __init__(self):
        self.languages = KnowledgeBase([
            "Python",
            "C++",
            "Java"
        ])
        self.tools = KnowledgeBase([
            "VS Code",
            "Git",
            "PyCharm",
            "Kali Linux",
            "VirtualBox",
            "Arduino"
        ])
        self.frameworks = KnowledgeBase([
            "OpenCV",
            "TensorFlow",
            "Pandas",
            "Spring Boot",
            "Processing",
            "Docker"
        ])
        self.pursuits = KnowledgeBase([
            "MMA",
            "Robotics",
            "AI",
            "Hacking"
        ])
        self.future_goal = FutureGoal("To develop opensource software & pentesting tools.")

    def get_info(self) -> Dict[str, Any]:
        return {
            "Languages": self.languages,
            "Tools": self.tools,
            "Frameworks": self.frameworks,
            "Pursuits": self.pursuits,
            "Future Goal": self.future_goal
        }

    def __str__(self):
        info = self.get_info()
        return "\n\n".join(f"## {key}\n{value}" for key, value in info.items())

# Example usage
if __name__ == "__main__":
    about_me = AboutMe()
    print(about_me)


```

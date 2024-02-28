# Flet-app
Simple cross platform application using Python Flet

**Insall flet**
```
pip install flet --user
```
**Run application**
```
flet run app.py
```
or python app.py


## Coding
### Creating a window
```python
import flet as ft

def main(page: ft.Page):
    pass

ft.app(target=main)
```
for web: `ft.app(target=main, view=ft.WEB_BROWSER)`

# Flet-app
Aplicativos multi plataforma com Python

**Instalação do flet**
```
pip install flet --user
```
**Rodar aplicação**
```
flet run app.py
```
ou `python app.py`


## Codificando
### Criando uma janela
```python
import flet as ft

def main(page: ft.Page):
    pass

ft.app(target=main)
```
for web: `ft.app(target=main, view=ft.WEB_BROWSER)`

### Controls
Com os Controladores é possível criar tudo em sua interface, desde textos a inputs complexos

![image](https://github.com/IK-R-S/Flet-app/assets/73291742/a0927160-7c04-4f3c-ab96-edbb8b6647d2)


```
import flet as ft
from flet import Text, Image

def main(page: ft.Page):
    page.title = 'Flet app'
    page.window_width =  600
    page.window_height = 500
    page.vertical_alignment = 'center'
    page.horizontal_alignment = 'center'
    welcome = Text('Welcome to Flet'.upper())
    logo = Image(src='https://flet.dev/img/logo.svg', width=30, height=30)

    page.add(welcome, logo)

ft.app(target=main)
```
Note que `page.add(welcome, logo)` atualiza os controladores (elementos) da página main, logo, se trocar a ordem a imagem irá aparecer em cima do texto de "welcome";

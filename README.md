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


```python
import flet as ft
from flet import Text, Image


def main(page: ft.Page):
    # Page attributes
    page.title = 'Flet app'
    page.window_width =  600
    page.window_height = 500
    page.vertical_alignment = 'center'
    page.horizontal_alignment = 'center'

    # Creating Controls (Widgets)
    welcome = Text('Welcome to flet'.upper())
    logo = Image(src='https://flet.dev/img/logo.svg', width=30, height=30)

    # Adding Controls to Page
    page.add(welcome, logo)

# Running application
ft.app(target=main) #view=ft.WEB_BROWSER

```
Note que `page.add(welcome, logo)` atualiza os controladores (elementos) da página main, logo, se trocar a ordem a imagem irá aparecer em cima do texto de "welcome";

### Entrada e saída de valores
![image](https://github.com/IK-R-S/Flet-app/assets/73291742/fadf4874-b5a1-4b20-8306-565fdbaa0a40)

```python
import flet as ft
from flet import Text, Image, TextField, TextButton


def main(page: ft.Page):
    # Page attributes
    page.title = 'Flet app'
    page.window_width =  600
    page.window_height = 500
    page.vertical_alignment = 'center'
    page.horizontal_alignment = 'center'

    # Functions
    def bemvindo(e):
        print('Bem vindo!')
        welcome.value = f'WELCOME TO FLET, {nome.value}!'.upper()
        page.update()
        
    # Creating Controls (Widgets)
    welcome = Text('Welcome to flet'.upper())
    bt = TextButton('Clique', on_click=bemvindo)
    logo = Image(src='https://flet.dev/img/logo.svg', width=30, height=30)
    nome = TextField(label='Nome', width=300)
    # Adding Controls to Page
    page.add(nome, bt, welcome, logo)

# Running application
ft.app(target=main) #view=ft.WEB_BROWSER
```

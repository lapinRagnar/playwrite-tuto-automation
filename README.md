# playwrite-tuto-automation

# Objetctif
créer un scipt pour automatiser une tache répetitive (dans le navigateur) avec playwright

## environnement
```
python -m venv env
env\Scripts\activate
pip freeze > requirements.txt
```

## installation des dependances
``` cmd
pip install --upgrade pip
pip install playwright
playwright install
```

## le code de demmarage
on crée le fichier `main.py`
```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch()
    page = browser.new_page()
    page.goto("http://playwright.dev")
    print(page.title())
    browser.close()
```

## To DO
la suite du tuto à finir

# ressources
## site du tuto
https://www.youtube.com/watch?v=q1GDSHhaH0E&list=WL&index=23&t=433s

## installation du playwrite
https://playwright.dev/python/docs/library

## demo de playwrite
https://www.youtube.com/watch?v=CeLkUDmTRkE

## codegen de playwrite

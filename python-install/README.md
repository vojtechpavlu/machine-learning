# Instalace jazyka Python


*Jako Python budeme uvažovat jazyk ve verzi 3.X. Starší (2.X) již používat nebudeme. Jako Windows předpokládejme Windows 10.*

Tento stručný návod obsahuje základní sadu kroků pro instalaci programovacího jazyka Python do svého lokálního prostředí. Návod je připraven pro operační systémy Windows, linuxové systémy a pro MacOS ***(TODO)***.

Rychlé odkazy:
---
- [Instalace pro Windows](#windows)
- [Instalace pro Linux](#linux)
- [Instalace pro MacOS](#mac) - Ještě bohužel nedostupné
- [Rychle o jazyku Python](#about)

---

### Návod pro Windows <a name="windows"></a>

1. Stáhněte si instalační program ze stránek
    - Odkaz zde: [https://www.python.org/downloads/](https://www.python.org/downloads/)
    - Doporučuji stáhnout verzi 3.8 nebo 3.9, ale v zásadě je to jedno. V nejhorším případě bude třeba přeinstalovat.

2. Spusťte instalační program a nainstalujte
    - *Install Python 3.X (64-bit)*
      - Zaškrtněme dole *Add Python 3.X to PATH
      - Vyberme *Custom installation*
    - *Optional Features*
      - Všechno zaškrtnout (Dokumentace, pip, tcl/tk and IDLE, Python test suite)
    - *Advanced Options*
      - Ideálně pro všechny uživatele (ale asi volitelné)
      - Určitě zaškrtnout *Add Python to environment variables*
      - Co není třeba zaškrtávat - *Download debugging symbols* a *Download debug binaries* (čistě volitelné)

3. Můžete spustit a dokončit instalaci


Nyní by měl být Python *ready to use*. To ověříme zadáním příkazu:

```bash
python --version
```

Mělo by se nám objevit něco jako toto:

```
Python 3.8.7
```

Pokud se nám verze Pythonu vrátila, provedli jsme úspěšnou instalaci jazyka a tím návod končí.

V případě nejasností, [toto video](https://www.youtube.com/embed/UvcQlPZ8ecA?start=0&end=250) na Youtube ukazuje celý postup instalace. Pro nás bude zajímavá pouze vyznačená část, tedy 0:00-4:10. 



------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Instalace jazyka pro Linux <a name="linux"></a>

Při instalaci nezapomeňte nainstalovat balíčkovací manager *pip*, konkrétně `python3-pip`.

Pro *Ubuntu* lze použít následující sekvence kroků:

1. Otevřeme terminál
2. Proveďte update. *Jde spíše o dobrou praktiku.* <a name="update"></a>
    
    ```bash
    sudo apt-get update
    ```
    
    Pravděpodobně budete po tomto kroku vyzváni k zadání svého uživatelského hesla. Dále provedeme upgrade.
    
    ```bash
    sudo apt-get upgrade
    ```

3. Nainstalujeme podpůrný software

    ```bash
    sudo apt-get install software-properties-common
    ```

4. Přidáme *Personal Package Archive* (PPA)

    ```bash
    sudo add-apt-repository ppa:deadsnakes/ppa
    ```
    
    Poté provedeme znovu [update](#update) a pokračujeme následujícím [krokem](#install-python).


4. Nainstalujeme Python <a name="install-python"></a>
    
    ```bash
    sudo apt-get install python3.8
    ```
    
    Vedle samotného jazyka nainstalujme i balíčkovací manager Pythonu *pip*.
    
    ```bash
    sudo apt-get install python3-pip
    ```
    

5. Vyzkoušíme, zda je vše funkční

    Na další řádek zadáme požadavek na verzi jazyka. Pokud při provádění příkazu dojde k nějaké chybě, znamená to, že se něco při instalaci pokazilo.

    ```bash
    python3 --version
    ```

    Mělo by se nám objevit něco jako toto:

    ```
    Python 3.8.7
    ```
    
    
Pokud se nám verze Pythonu vrátila, provedli jsme úspěšnou instalaci jazyka a tím návod končí.


Podobně by se měl chovat i balíček `python3-pip`.


Celý návod pro více různých distribucí je uveden zde [https://docs.python-guide.org/starting/install3/linux/](https://docs.python-guide.org/starting/install3/linux/), alternativně zde [https://phoenixnap.com/kb/how-to-install-python-3-ubuntu](https://phoenixnap.com/kb/how-to-install-python-3-ubuntu).

V případě nejasností můžete využít i [tohoto videa](https://www.youtube.com/watch?v=Br2xt6B57SA).

------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Instalace jazyka pro MacOS <a name="mac"></a>


***TODO - Nastudovat MacOS***



# O jazyku Python  <a name="about"></a>

Jazyk Python je jedním z nejpoužívanějších jazyků dneška. Lze se s ním setkat v desktopových aplikacích, běží na backend serverech a velmi hojně je používán i v oblasti strojového učení a zpracovávání dat.

## Důležité odkazy:

- [Dokumentace](https://docs.python.org/3/) jazyka
- [Python wiki](https://wiki.python.org/moin/)


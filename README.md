# Příprava virtuálního prostředí

Vytváříme si virtuální prostředí, aby bylo možné oddělit nástroje využívané výhradně pro strojové učení od nástrojů obecně v Pythonu používaných. V tomto tutoriálu je použit název **machine-learning**, ale na názvu prakticky nezáleží. Můžete si vybrat prakticky libovolná název, mějte to však v mysli, že musíte příkazy upravit před jejich zadáním.


Rychlé odkazy
---

- [Instalace virtuálního prostředí](#venv)
- [Před instalací knihoven](#pip)
- [Instalace knihoven](#libs)
- [První spuštění Jupyter Notebook](#first-jupyter-start)
- [Každé další spouštění Jupyter Notebook](#every-jupyter-start)


Odkazy na dokumentace
---
- [Dokumentace PIP](https://pip.pypa.io/en/stable/)
- [Dokumentace virtualenv](https://docs.python.org/3/tutorial/venv.html)
- [Dokumentace Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/stable/)

---

### Instalace virtuálního prostředí <a name="venv"></a>

1. Otevřme si příkazovou řádku
2. Přemístíme se do libovolného adresáře, kde budeme chtít pracovat
    Budeme sem stahovat větší objemy dat. Záleží tedy na tom, zda-li máme na příslušném disku dostatek místa. Jinak je to víceméně jedno.
    
    Musíte nejdříve nainstalovat *pythoní balíček* `virtualevn`. Ten nainstalujete pomocí package manageru `pip`. To uděláme následovně:
    
    ```bash
    pip install virtualenv
    ```
    
    Pro ty z Vás, kteří používají Linux může dojít k chybě. Zkuste tento příkaz upravit na
    
    ```bash
    sudo pip install virtualenv
    ```

    Nyní máme balíček virtuálního prostředí připraven a můžeme se přesunout do vytvoření prostředí pro práci.
    
    
    Pro Windows, linux a MacOS zadáme
    
    ```bash
    python -m venv machine-learning
    ```
    
    To nám vytvoří virtuální prostředí s názvem *machine-learning*. 
    
    **Nyní budeme virtuální prostředí spouštět.**<a name="start-venv"></a>
    
    Pro Windows to uděláme následovně:
    
    ```bash
    .\machine-learning\Scripts\activate
    ```
    
    Zatímco pro Linux a MacOS použijeme
    
    ```bash
    source machine-learning/bin/activate
    ```
    
    Prostředí je spuštěno. Všimněme si závorky vždy na začátku řádku. Pokud budeme chtít prostředí ukončit, stačí napsat <a name="end-venv"></a>
 
    ```bash
    deactivate
    ```

---

### Před instalací <a name="pip"></a>

**Pokud máme virtuální prostředí aktivované, než budeme pokračovat - [deaktivujme ho](#end-venv).**

Dále v tomto tutoriále budeme používat nástroj *pip*. Ujistěte se, že ho máte nainstalován. 

Pro všechny OS lze ověřit přítomnost pomocí příkazu

```bash
pip --version
```

Pokud jste tak ještě neučinili či ho nemáte z jiného důvodu, nainstalujte si balíčkovací manager *pip*, viz [návod na instalaci Pythonu](https://github.com/vojtechpavlu/machine-learning/blob/prep_python-install/python-install). Pro linux stačí jen zadat

```bash
sudo apt-get install python3-pip
```

Pro Windows bude pravděpodobně třeba provést reinstalaci Pythonu a ujištění se, že instalujete včetně jazyka i toto.

---

### Instalace potřebných knihoven <a name="libs"></a>

**Pokud nemáme virtuální prostředí aktivováno, neý budeme pokračovat - [spusťmě ho](#start-venv).** Pokud by prostředí nebylo spuštěno, bude se vše instalovat globálně.

Máme-li vše takto připraveno, stačí již nainstalovat všechny potřebné knihovny do našeho virtuálního prostředí. To uděláme pomocí následujícího příkazu:

```bash
pip install jupyter matplotlib numpy pandas scipy scikit-learn
```

V případě, že by tento příkaz rovnou nefungoval, lze použít

```bash
python -m pip install jupyter matplotlib numpy pandas scipy scikit-learn
```

To se nyní bude chvilku stahovat a instalovat.


### První spuštění Jupyter Notebooku
<a name="first-jupyter-start"></a>

Nyní můžeme zadat příkaz pro spuštění Jupyter notebook následující příkaz:

<a name="start-jupyter"></a>
```bash
jupyter notebook
```

Mějme na paměti z jakého adresáře Notebook spouštíme. Spouštíme ho z virtuálního prostředí (uvnitř další hierarchie) a budeme schopni pracovat se soubory z aktuálně používaného adresáře.

### Každé další spouštění
<a name="every-jupyter-start"></a>

Každé další spouštění Notebooku bude probíhat následovně:

1. Dostat se do tohoto adresáře
2. Spustit virtuální prostředí (viz [spouštění venv](#start-venv))
3. Spustit Jupyter Notebook (viz [spouštění notebooku](#start-jupyter))

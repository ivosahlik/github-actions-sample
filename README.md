[![01 - Building Blocks](https://github.com/ivosahlik/github-actions-sample/actions/workflows/01-building-blocks.yaml/badge.svg)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/01-building-blocks.yaml)

# Github docs 
https://docs.github.com/en/actions/writing-workflows/quickstart

# Posts
https://victoronsoftware.com/posts/github-reusable-workflows-and-steps/



````
actions/checkout@v4 je GitHub akce, která zajišťuje klonování vašeho repozitáře do $GITHUB_WORKSPACE, 
aby váš workflow měl přístup ke kódu. 
Tato akce se běžně používá ve workflows, aby bylo zajištěno, že kódová základna je dostupná pro následující kroky,
 jako je build, testování nebo nasazení aplikace.
 
Klíčové vlastnosti:
Klonování repozitáře: Klonuje repozitář do runneru, čímž zpřístupňuje kód pro workflow.
Hloubka fetch: Ve výchozím nastavení fetchuje pouze jeden commit, který spustil workflow, což lze konfigurovat.
Submoduly: Podporuje klonování submodulů, pokud je váš repozitář používá.
LFS (Large File Storage): Podporuje Git LFS, pokud je váš repozitář používá.

Příklad použití:
- uses: actions/checkout@v4
  with:
    # Volitelné: Fetch všechna historie pro všechny větve a tagy
    fetch-depth: 0
    # Volitelné: Klonování submodulů
    submodules: true
    # Volitelné: Nastavit na 'true' pro použití Git LFS
    lfs: true
    
Vysvětlení možností:
fetch-depth: Řídí hloubku klonování. Nastavení na 0 fetchuje celou historii.
submodules: Pokud je nastaveno na true, inicializuje a aktualizuje submoduly.
lfs: Pokud je nastaveno na true, fetchuje soubory Git LFS.





https://github.com/actions/checkout/tree/v4#readme

````

# Github Actions 
https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions#filter-pattern-cheat-sheet
https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions

# Github APi
https://docs.github.com/en/rest/actions/artifacts?apiVersion=2022-11-28



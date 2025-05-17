.
# Monitoring - add status and badge
[![01 - Building Blocks](https://github.com/ivosahlik/github-actions-sample/actions/workflows/01-building-blocks.yaml/badge.svg)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/01-building-blocks.yaml)

[![29-Auto approve PR](https://github.com/ivosahlik/github-actions-sample/actions/workflows/29-pr-automerge.yml/badge.svg)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/29-pr-automerge.yml)

[![10 - Controlling the Execution Flow](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml/badge.svg)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml)

[![10 - Controlling the Execution Flow](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml/badge.svg?branch=main)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml)

[![10 - Controlling the Execution Flow](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml/badge.svg?branch=main&event=create)](https://github.com/ivosahlik/github-actions-sample/actions/workflows/10-execution-flow.yaml)

![Testing Workflow](https://github.com/ivosahlik/github-actions-sample/actions/workflows/18-3-reusable-workflows.yaml/badge.svg)



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


# Run your GitHub Actions locally - docker run
https://nektosact.com/introduction.html

* `brew install act` - install client for mac os
* `act -h` - help
* `act -j test` - run the tests
* `act -j test-composite`
* `act` - run the the entire pipeline
* `act -l` - view the execution graph
* `act -j echo-hello -l` - list actions for specific job
* `act -j test-composite -s GITHUB_TOKEN_TEST=mockedsecret`
* `act -j build-and-push-to-docker-repository -P ubuntu-latest=quay.io/jamezp/act-maven`



# Runner

Použití vlastního runneru v GitHub Actions má několik výhod:

1. **Vlastní prostředí**: Můžete si nakonfigurovat runner s konkrétním softwarem, nástroji nebo závislostmi, které nejsou dostupné na hostovaných runnerech GitHubu.

2. **Úspora nákladů**: Vlastní runner může snížit náklady, zejména u velkých nebo častých workflowů, protože hostované runnery GitHubu mají omezení využití.

3. **Výkon**: Vlastní runner lze optimalizovat pro specifické úlohy, což zajišťuje lepší výkon u náročných úkolů.

4. **Přístup k privátním zdrojům**: Lze jej nastavit v rámci vaší privátní sítě, což umožňuje přístup k interním systémům, databázím nebo jiným neveřejným zdrojům.

5. **Kontrola a bezpečnost**: Máte plnou kontrolu nad hardwarem, operačním systémem a bezpečnostními konfiguracemi runneru.

6. **Škálovatelnost**: Můžete přidávat další stroje nebo zdroje podle potřeb vaší organizace.

7. **Přizpůsobení**: Můžete instalovat vlastní skripty, nástroje nebo konfigurace přizpůsobené vašim workflowům.

Vlastní runnery jsou ideální pro organizace s konkrétními požadavky, které nelze splnit pomocí hostovaných runnerů GitHubu.



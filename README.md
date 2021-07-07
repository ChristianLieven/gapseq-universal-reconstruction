[![memote tested](https://img.shields.io/badge/memote-tested-blue.svg?style=plastic)](https://jotech.github.io/gapseq-universal-reconstruction)

# gapseq-universal-reconstruction

* Brief description

> For the construction of genome-scale metabolic network models we have built a biochemistry database, that is derived from the ModelSEED biochemistry database. In total, the resulting curated gapseq metabolism database comprises 15,150 reactions (including transporters) and 8446 metabolites. All metabolites and reactions from the biochemistry database are incorporated in the universal model that gapseq utilises for the gap-filling algorithm. If all dead-end metabolites and corresponding reactions would be removed, the universal model comprises 10,792 reactions and 3885 metabolites. However, since genome-scale metabolic networks are also used as structured knowledge-bases, no dead ends are removed from the universal model. It needs to be noted, that the current biochemistry database and the derived universal model represents mainly bacterial metabolic functions and that, at the current version of gapseq, the database does not include all archaea-specific nor eukaryotic-specific reactions. However, those reactions and, thus, also the possibility to use gapseq for the reconstruction of archaeal and eukaryotic models will be included in a later version of the software.

from [gapseq: informed prediction of bacterial metabolic pathways and reconstruction of accurate metabolic models](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-021-02295-1#citeas)

* Reconstruction keywords:
**GEM Category:** Pan-species; **Utilisation:** reference knowledgebase; **Field:** metabolic-network reconstruction; **Type of Model:** curated, reconstruction; **Model Source:** [ModelSEED](https://modelseed.org/biochem/reactions); **Taxonomy:** Prokaryota; **Metabolic System:** General Metabolism; **Automated Draft Reconstruction**

* Last update: 2021-07-02

* The reconstruction:

|Taxonomy | Template Model | Reactions | Metabolites| Genes |
|:-------:|:--------------:|:---------:|:----------:|:-----:|
|Prokaryota|[ModelSEED](https://modelseed.org/biochem/reactions)|1994|1650|0|

## Usage

The reconstruction exists both as a collection of flat files in the `/data/knowledgebase` subdirectory, and combined in YAML and SBML/XML formats. 

The colaborative workflow consists of 
1. Reading the tables (R and Python scripts are provided in `/scripts`) - Or manipulating the tables directly
2. Modifying the reconstruction in the tool of your choice ([Sybil](https://cran.r-project.org/web/packages/sybil/index.html), [Cobrapy](https://opencobra.github.io/cobrapy/))
3. Saving the reconstruction as tables
4. Saving the reconstruction as SBML
5. `memote run`
6. `git commit` (TODO: Implement a commit hook to autogenerate a MEMOTE test result)


## Requirements

### Python
TODO: `pip freeze | requirements.txt`

### R
TODO: `renv::snapshot()`

## Roadmap:


---

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

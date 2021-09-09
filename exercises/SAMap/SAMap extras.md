# SAMap extras

Javier has kindly prepared some code for loading the planarian and schistosome datasets into python and viewing their properties.

## Scanpy
Import packages:
`import scanpy as scan`

Load original h5ads:
```
fn1 = 'example_data/planarian.h5ad'
fn2 = 'example_data/schistosome.h5ad' 
plan = scan.read('example_data/planarian.h5ad')
schi = scan.read('example_data/schistosome.h5ad')
```

Plot each species umap plots:
```
print("Planarian adata object:")
print(plan) ##
print()
print("Schistosome adata object:")
print(schi) ##
print("##########################")
print("Plots:")


print("Planarian")
print("_________")
scan.pl.umap(plan, color="cluster")
print("Schistosome")
print("___________")
scan.pl.umap(schi, color = 'tissue')
```

Number of cells in a cluster:
```
print("Planarian")
print("_________")
print(plan.obs['cluster'].value_counts())
print()
print("Schistosome")
print("___________")
print(schi.obs['tissue'].value_counts())
print()
```

### Maybe useful: gene expression in a UMAP
Explore variable genes:
```
print("Gene IDs Planarian:")
print(plan.var.index)
print()
```

Plot expression on UMAP:
```
print("Planarian")
print("_________")
scan.pl.umap(plan, color=['dd_Smed_v4_10945_0_1', 'dd_Smed_v4_100263_0_1', 'dd_Smed_v4_10001_0_1'])
```
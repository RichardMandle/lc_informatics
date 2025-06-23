# lc_informatics
## What is it?
A module (moldataview) and some python workbooks for interacting with data on liquid crystals. This is useful for looking at relations in large datasets.<br>

## Required Packages
* pandas
* numpy
* rdkit
* dash
* plotly
* UMAP
* tqdm
* matplotlib
* re, base64, os, collections, itertools, sklearn, etc.

## Data structure
Store your LC data in a .csv file with columns "title",	"SMILES",	"Transitions / dC",	"Reference".<br>
The column "SMILES" will be used to generate molecular structures.<br>
The column "Transitions / dC" should contain data in the style "K xx N yy I", where xx and yy refer to the K-N and N-I transitions, respectively. Use K == Crystal / melting point, and I == isotropisation / clearing point. <br>
The column "Reference" should have the DOI of the molecule in questions; some functions retrieve a .ris file directly from this DOI.

## Example usage:
```
import moldataview as mdv
data = mdv.read_data_from_csv('nf_list.csv')
mdv.transition_plot_app(data)
```

Gives:<br>
![newplot (2)](https://github.com/user-attachments/assets/411b0b66-9eff-47ad-9552-7207a28bc588)

And you can click on the points and select molecules of interest:<br>
![image](https://github.com/user-attachments/assets/ce14134a-22ae-4dfa-a549-72cb0e805aa9)



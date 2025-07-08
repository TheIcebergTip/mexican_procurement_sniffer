# mexican_procurement_sniffer
Python-based personal tool for local use to search and analyse Mexican procurement data from the federal database [Compranet](https://comprasmx.buengobierno.gob.mx/datos-abiertos). Built to improve my investigative workflow and offline contract research in case of the data stored online its deleted or hidden.

## 🔍What it does

Allows to filter and explore millions of publicly available Mexican procurement contracts from 2013 to 2023 using a combination of the following criteria:

**PROVEEDOR**   (*supplier name*)

**SIGLAS**      (*government agency acronym*)

**DESCRIPCION** (*word(s) within the contract description*)

It outputs a single '.xlsx' file with the matching results from both administrations.


## 📁Files used

The script parses through two '.xlsx' files that contain contract data from the past administrations since 2013 to 2023. 
*2024 data is being cleaned*

- **EPN**   Enrique Peña Nieto (2012-2018)              
*`compranet_grouped_epn_by_provider.xlsx`*

- **AMLO**  Andrés Manuel López Obrador (2019-2024)     
*`compranet_grouped_amlo_by_provider.xlsx`*


## ⚙️Use example

Run script on the local machine.
It will prompt to enter one or more search terms:

- *One term example:*

```python
Enter search term for PROVEEDOR: demos desarrollo
Enter search term for SIGLAS: "leave in blank"
Enter search term for DESCRIPCION_CONTRATO: "leave in blank"
```
*dummy quotes*

This will return all contracts involving the supplier **demos desarrollo**, across both administrations.

It is also possible to combine filters as needed:

- *Three term example:*
```python

Enter search term for PROVEEDOR: demos desarrollo
Enter search term for SIGLAS: SEGOB
Enter search term for DESCRIPCION_CONTRATO: difusion
```

This will return all contracts involving *demos desarrollo*, awarded by *SEGOB*, and mentioning *difusion* in the contract description, across both administrations.

The combinations allow us to be as **surgical** or **broad** as needed — whether we're tracking a specific supplier or scanning for keywords across contracts.

## ⚠️Warning

If you enter two or more search terms and one of these isn't found, the script will not return results. 

To avoid this:
1. Start by searching one therm at a time
2. Double-check spelling
3. Be aware of the keywords used



# SeqDB, the CGI Use-cases

## Introduction
The below suggestion are written after testing the “SeqDB Version 3.18-SNAPSHOT”

## Import of the excel-sheet.
        1. That we are able to put in an arbitrary number of Alleles (so instead of the current 16 Alleles, we can choose an arbitrary length)
        2. Better Error-messages when something goes wrong.
            For instance :  Which record (row in the Excel-file) and which column is breaking the import.
        3. Help-page for the importers ?

## Documentation and Language
'Help'-Headline and the links to documentation :Today the links are ending up in the agr.gc.ca-redmine instance (redmine.biodiversity.agr.gc.c)

        1. Could we create our own links to documentation and point them to our wiki ? 
            Especially , the ‘User Documentation’.
        2. The language-toggle between English and Francais is not working
        3. A language-toggle between  : ‘English’ and ‘Swedish’.
            If possible, we could provide translation (‘bundle’_sv_SE.properties-file)

## 'Genotype Details'-page
https://seqdb.nrm.se/seqdb.web-3.189/editGenotype.html?genotypeId=7


Current layout, see the 'Alleles'-section

Changing the layout for the ‘Alleles’-section 

Future layout : Either Example 1 or Example 2. (without the numbering-list)

**Example 1**

1. Locus	Size
2. MU23	173
3. Locus	Size
4. MU23	176

**Example 2**

1. Locus	Size
2. MU23	173
3. MU23	176


## BUGS

Exporting from Genotypes

        1. NOT OK ? Exporting to cvs does not give me the column-names, is that the default behavior ?
        2. OK! Exporting to excel, XML and PDF gives me the column-names
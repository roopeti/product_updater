# Adding new fields to the product updater


## Documents

All of the mapping for the functions is done in the Legrand.js file 
The documents are mapped in the function called "mapLegrandToFullTT"
The documents are mapped under "//Document assets":

<img width="765" height="695" alt="image" src="https://github.com/user-attachments/assets/9236efe5-7c29-48ec-8d70-ef646231040e" />


I have not labeled the specific documents, but looking at the AS-codes you can figure out which document is in question. So if new documents need to be added, using the helpers and logic that I have used here, more can be added. 
1. If there are documents that have multiple languages and the finnish language is to be prioritized. Use the "findAssetUrlByLanguage" helper when making the mapping.
2. If the document is in a link format, use the "findAssetUrl" helper in the mapping.



## Info fields

The info fields are mapped in the function called "mapLegrandProductInfoFields"
There is a variable that holds the TT codes for the info fields called "INFO_FIELDS", when adding new fields to the mapping make sure to add the TT codes to this variable. This always checks that atleast one of these fields is present in the final mapped file. If not the product gets removed from the file.

You would add new info fields under these:
<img width="901" height="311" alt="image" src="https://github.com/user-attachments/assets/9bc22ba6-e141-4e27-a3c9-6a4a3cad2355" />

Currently the logic is so that the "LFLG2061A" info field from "values" is mapped to TT202, and if that isn't found it is mapped from "LFLG2066A".
And similarly for TT203 "LFLG0025" is prioritized, but if not found then "LFLG2061A" is used. 

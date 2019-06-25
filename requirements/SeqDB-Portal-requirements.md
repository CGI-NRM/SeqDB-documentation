# Public UI for the SeqDB
https://seqpublic.nrm.se/

## First set of requirements

### Non-Functional requirements

Start with a capital letter: 

1. That every word starts with a capital letter .
2. Example:  "Taxonomy : Species" - and so forth.

Mouse-over:
1. To have a 'mouse-over'-functionality over (wgs84) that says 'epsg:3006'

@Info
here is more on epsg -> http://epsg.io/?q=swede

Providing 2 example of latitude and longitude positions:
1. See the page : http://www.ensembl.org
2. The example provided for ‘Search’ , one can click on of the 4 different links.
3. An example for seqdb_public could be a position in Sweden, for instance the ‘City Hall’ in Stockholm (https://en.wikipedia.org/wiki/Stockholm_City_Hall)

Layout
1. We would like to customize/brand the page with for instance with a 'header' and a 'footer' You can see the footer in www.naturforskaren.se , where we have put x number of logos and contact-information.

2. Ability to Switch between British-English and Swedish ? (we can do the translation). Use of a ‘flag’-icon (flag of ‘Great-Britain’ and the Swedish flag ) ?

4. Questions : Is paging possible, if our results are greater than x ( for instance 100 records ) ?

## Introduction (after testing the “3.17-SNAPSHOT”) 
The below suggestion are written after testing the “3.17-SNAPSHOT”<p>
The public-UI is using the database from SeqDB.

## Bugs

### Swedish Translation

        1. [TRANSLATON] : headline  locality: should be 'plats' 
        2. [RENAME txt] : 'Stad/Region' should be 'Stad/Län' - changes should also be done in mouseover
        2. [TRANSLATON] : mouseover 'datum', text still in English  
        3. [RESUT-LIST] : Provins should be ‘Län’ ( more: shows 'Jämtlands län' etc. ,  'län' could be removed )
        4. [RESUT-LIST, TRANSLATON] :  Common-name should be traslated into 'Namn'

### Others

A. Result-list

        1. Column 'Region' has no value, remove the column (In the Result-table, Our Region is empty  - we should remove that column (2) the Provins should be 'Län' (3) That said , then we need to change the label 'Stad/Region' to 'Stad/Län' and make the search in 'Stad/Län' instead of 'Stad/Region' - do you think that I could change this, would you like to guide me here ?)
        2. Button : 'Clear'/'Rensa' should go back to the orignal state (empty search-fields, empty table, reset the URL)

B. Exempel: 1 and 2

        1. create better examples ...

C. HTTPS

        1. OBS: the browser-padlock is now yellow due to the map, how can this be fixed?


D. Mobile-version ?

### the sample data

        1. remove the sample-data, this should be done in seqdb


## new functionality

Discussion with Thomas K, 20180406

        1. Add  'about'/'om' (layout: left of the language-links)
            1. Here there should be short info of what this portal is (Spilling ... )
            2. Thomas had a short summary : both in English and in Swedish
            3. add the 'about'/'om' page on github-wikipages ...
        2. Layout-changes:
            1. Move the 2 icons from footer  'nrm' & 'naturvårdsverket' to the header
                1. top right corner ?
            2. reason ? The icons are more visible, and even more visible on the mobile
        3. Rename the 'SeqDb portal' to something else (left corner, change the html-title as well) ? 
            1. colour-schema : change the colour of the header ?
        4. function ? :  (Ask Thomas)
            1. ad a  on/off-toggle button - to show only 'spillning' / 'individual bears'
        5. Om man kan använda något fält på de olika posterna (det finns ett fält som heter 'restricted' som kan togglas mellan true och false - om false så kan man inte söka på detta ? )
        6. export from the result-tables, if you would like to have the Genotypes as well - you must mail to cgi@xxx.yyy 


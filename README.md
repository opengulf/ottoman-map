# ottoman-map

This repository contains data concerning an Ottoman map (c 1910) and data used for a forthcoming publication in the *Journal of the Ottoman Turkish Studies Association*

This release contains four datasets: (1) shape files created from georeferencing *Harita 93677* from the Istanbul University Rare Sources Library image collection, (2) a companion data table included with the map (3) data about weapons extracted from John Gordon Lorimer, [*Gazetteer Of The Persian Gulf Oman And Central Arabia Vol-ii Geographical And Statistical*](https://archive.org/details/in.ernet.dli.2015.206964), and (4) data about toponyms extracted from the second chapter of the Najd section of Ibrahim Fasih bin al-Sayyid Sibghat-Allah al-Haydari al-Baghdadi’s *‘Unwan al-Majd fi Bayan Ahwal Baghdad wa-l-Basra wa Najd*

#1 "*Harita93677_shapefiles*"  This folder contains shape files created using the Georeferencer tool for QGIS. There are two subfolders: Iraq shapefiles; and Najd shapefiles. 

#2 "*TribesMapData*"  This folder contains a data table giving the values as listed in the original source, in addition to corrected numbers for clear errors. Errors and other ambiguities also described below. The key to the columns in the csv file are found below.

A UniqueID (assigned by us)
B Tribe number (as given in original table)
C Tribe name (in Arabic script)
D number of bands
E sect
F male population_original
G male population_corrected
H female population_original
I female population_corrected
J total population_original
K total population_corrected
L tents
M sarifas (reed dwellings)
N cavalry
O foot soldiers
P weapons
Q location (in Arabic script)

Note on errors and ambiguities: We identified 21 cells in which the Ottoman scribe made clear transcription or calculation errors (for example, dropping a zero) for which the “correct” answer based on the other data for that tribe was clear. The columns marked “original” in the data table (F, H, and J) reproduce the data in the table as it was transcribed. The columns marked “corrected” (G, I, and K) include corrected values for cells with errors.

There are several other places in the original table where data appears to be wrong, or non-numeric qualifiers were added by the scribe. These have been removed from the table, and are listed below for reference.

Other errors and ambiguities:

In the “Border” section (UniqueID 268-287), it is unclear which categories the three data columns refer to. We have assigned them to cavalry, foot soldiers, and weapons based on the fact that the columns 1 and 2 often sum to column 3; and one entry in column 1 indicates mounted men.
UniqueID 278 - “column 1” (cavalry) is listed as 4000 mashhuf (canoe)
UniqueID 219 no data given, just the sentence, “Samiye çölünde sakin gayet vahşi ve silahsiz bulunduklarından haiz-i ehmiyyet bir aşiret değildir (This tribe, which lives in the Syrian desert, is not important because they are very savage and have no weapons).” 
UniqueID 233 - number of bands listed as neighborhoods not bands
UniqueID 236, 241, 247, 266 - cavalry specified as mounted on camels, listed in “foot soldier” column rather than cavalry column
UniqueID 230, 231, 232, 266 - number of bands listed as villages not bands
UniqueID 256 - in sarifa section note says “there are also villages”
UniqueID 233 - dwellings section notes “in houses”
UniqueID 242 - dwellings section notes “also villages”
UniqueID 265, 267 - no data, just the sentence “miktarları-ı layıkı vechile ma’lum değildir” (the appropriate numbers are not known)
UniqueID 57 - sect listed as “Hadidi,” which is the name of the tribe 
UniqueID 4 - cavalry listed as 33,679 - clear error as this is more than total population but not clear what is correct
UniqueID103 - sarifas, could be either 64 or 94 - printing unclear, we have listed as 94

Note on translation and transliteration: Tribe names and location names are rendered in Arabic script because of lack of clarity about transliteration and voweling. Table categories are translated into English and sects are transliterated using a modified version of the IJMES system for transliterating Arabic without diacritic marks.

#3 "*WeaponsArabistanIraqKuwait*"  This folder contains a data table with selected places from volume 2 of Lorimer's *Gazetteer* where keywords and values related to weapons were found.

This dataset focuses on a large number of weapons, namely rifles, which were reported in the Arabistan area as well as in the region of Iraq and Kuwait.

The key to the columns in the csv file is as follows: 

A textfile: corresponding to a chapter found in Lorimer's Gazetteer.
B type: instances of rifles are described in locations or with tribe. Tribes which do not have a stable location identified in the text, but are rather described as being located between place X and place Y, have been omitted here.
C region: the location assigned by OpenGulf as the general region in which the locations are found
D GEOID: the GeoNames ID found for the place; there are some values without GEOID listed as unknown, including where a tribe is situated by Lorimer. 
E latitude: in the case where a GeoNames ID is found, this value comes from it. Else, it is a valued derived from eyeballing the map 
F latitude: in the case where a GeoNames ID is found, this value comes from it. Else, it is a valued derived from eyeballing the map 
G place_name: the Latin alphabet toponym listed in Lorimer's Gazetteer
H: quantity_rifles: the number of rifles associated by Lorimer with place_name. In the case that a non-numerical value is given by Lorimer ("few", "many", "well armed")  the location is omitted. 

#4 “*HaydariNajd*” This dataset contains place names extracted from the second chapter of the Najd section of al-Haydari’s *‘Unwan al-Majd fi Bayan Ahwal Baghdad wa-l-Basra wa Najd*.
The key to the columns in the csv file are as follows:

A place_name: the Arabic toponym listed in al-Haydari’s historical treatise
B latitude: value derived from a GeoNames ID
C longitude: value derived from a GeoNames ID
D GEOID: the Geonames ID found for the toponym in column A; there are some values without GEOID listed as unknown
E region_tag: the region al-Haydari links the corresponding toponym to in his treatise.  These include: Qassim, Shammar, Sudayr, Rashm, Mahmal, Aridh, Kharj, Far‘a, Aflaj, Sulayl.  There are two additional tags we assigned to the toponyms: “border”, for toponyms al-Haydari described as marking the border of Najd; and “outside”, for toponyms al-Haydari described as being outside Najd, which are not represented on the map.

Releases of this data are versioned at Zenodo.


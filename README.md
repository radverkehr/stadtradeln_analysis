# stadtradeln_analysis


Im Rahmen eines Forschungsprojekts an der TH Wildau wurden die aggregierten Daten aus der [Stadtradeln-Kampagne](https://www.stadtradeln.de/home) unter der [Lizenz](https://www.radverkehr-in-deutschland.de/2024/02/28/ergebnisdaten-jetzt-auch-unter-open-data-lizenz-verfuegbar/) [Creative Commons Lizenz CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.de) von [RiDE (Radverkehr in Deutschland)](https://www.radverkehr-in-deutschland.de/) beschafft. Diese Daten stehen hier zum Download und in einer beispielhaften Visualisierung (WIP) zur Verfügung.

Für die Jahre 2021, 2022 und 2023 stehen die durchschnittlichen Geschwindigkeiten sowie die Anzahl von Radfahrenden je OSM way-Abschnitt und Richtung für folgende Kommunen zur Verfügung.
- Wildau, Stadt (ARS: 120610540540)
- Zeuthen, Gemeinde (ARS: 120610572572)
- Königs Wusterhausen, Stadt (ARS: 120610260260)
- Schulzendorf, Gemeinde (ARS: 120610444444)
- Eichwalde, Gemeinde (ARS: 120610112112)
- Schönefeld, Gemeinde (ARS: 120610433433)

## Datensätze
Die Datensätze liegen hier als GeoPackage in EPSG:4326 vor. Sie beziehen sich auf alle erfassten SR Daten des entsprechenden Jahres im o.g. Gebiet. Die einzelnen erfassten Tracks wurden mit einem OSM-Netz (Stand Jahresbeginn des entsprechnden Jahres) gematched und je OSM way-Abschnitt agreggiert. Dabei wurden relevante OSM highways genutzte und an allen Knotenpunkten (OSM Nodes) getrennt.
* Verkehrsmengen 2.0_SR (trafficvolumes.gpkg)
  * je OSM way-Abschnitt
  * Attribute: fid, osm_way_id, number_of_matched_trips
* Geschwindigkeiten 2.0_SR (speeds.gpkg): 
  * Je Richtung, je OSM way-Abschnitt
  * Attribute: fid, osm_way_id, number_of_matched_trips, average_speed_kmh



__________________

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

# CH Data PostGIS

Projet de mise à niveau SIG et PostGIS.

## Stack

- PostgreSQL
- PostGIS
- QGIS

## Objectif

Construire une base de données spatiale suisse avec les données fédérales open data.




# Import des communes suisses

## Dataset utilisé

swissBOUNDARIES3D

Source :
https://www.swisstopo.admin.ch/

## Données importées

- communes
- projection : EPSG:2056
- type géométrique : MultiPolygon

## Structure PostgreSQL

Schema :
- admin

Table :
- communes

## Étapes réalisées

1. création de la base geo_suisse
2. activation PostGIS
3. création du schéma admin
4. import de la couche communes via QGIS DB Manager
5. renommage de la table

## Requête utilisée

```sql
ALTER TABLE admin.tlm_hoheitsgebiet
RENAME TO Limites_communales;
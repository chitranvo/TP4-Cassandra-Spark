# TP4 — Cassandra et PySpark

## Objectif
Lire les données Cassandra dans PySpark, effectuer des transformations et agrégations, puis observer Lazy Evaluation, partitions et Shuffle dans Spark UI.

## Données
- Keyspace : `velib_tp2`
- Table : `stations_by_id`
- Colonnes : `station_id`, `name`, `capacity`, `capacity_category`, `zone`
- Nombre de lignes observé : 20

## Questions métier
- Filtrer les stations par capacité.
- Calculer des indicateurs de capacité.
- Compter les stations par catégorie et par zone.
- Observer l'exécution distribuée et le Shuffle.

## Résultats observés
- Capacité moyenne : 30,5
- Capacité minimale : 17
- Capacité maximale : 54
- Somme des capacités : 610
- Catégories : 11 stations `petite`, 9 stations `moyenne`
- Partitions : 4 initialement, 8 après `repartition(8)`
- Spark UI : Job 25, Stage 30, 4/4 Tasks réussies, Shuffle Write 568 B / 8 records

## Notebook
Le notebook complet est dans `notebook/tp_cassandra_spark.ipynb`.
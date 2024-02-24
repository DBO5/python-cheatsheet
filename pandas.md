# Etapes souvent utiles au démarrage d'un notebook
## montrer toutes les colonnes dans l'affichage
pd.set_option('display.max_columns', None)

## récupérer la liste des intitulés de colonnes
df.columns.tolist()

## Faire un subset d'un dataset

cols = ['','',...] # on choisit les colonnes qu'on veut garder dans df
df[cols] # on appelle dans df

# Nettoyer les données

## faire une recherche (query) pour trouver d'où viennent les valeurs manquantes

(df[cols].query('column_name.isna()')


## remplir une colonne de Nan et en faire une catégorie (ex: catégorie "Autres")

 df[cols].assign(column_name = df.column_name.fillna('Other').astype('category'))

## renommer des colonnes
### manuellement
df.rename({'2023':'investissement_2023','2024':'investissement_2024',
                    '2025':'investissement_2025',
                    '2026':'investissement_2026',
                    '2027':'investissement_2027',
                    '2028':'investissement_2028',
                    '2029':'investissement_2029',
                    '2030':'investissement_2030'}, **axis = 1**)
### en masse



Voir notamment https://medium.com/codex/how-to-batch-rename-columns-in-pandas-based-on-patterns-7d2382b5fc9a

##Récupérer une liste avec le nom des colonnes

df.columns.to_list()


## Méthodes

* .loc
* .index : permet de récupérer l'index des lignes en attribut

exemple : index_with_nan = data_conso.index[data_conso.loc[:,'Année'].isnull()]


méthode .str.replace pour remplacer du texte dans une colonne.
exemple : 
source : https://www.youtube.com/watch?v=KokJHxiE14s&ab_channel=RobMulla à 5:40

# Matplotlib





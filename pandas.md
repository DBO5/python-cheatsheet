# Etapes souvent utiles au démarrage d'un notebook
## montrer toutes les colonnes dans l'affichage
pd.set_option('display.max_columns', None)

## récupérer la liste des intitulés de colonnes
df.columns.tolist()

## Subsetting a dataset

#cols = ['','',...]
#df[cols]

## Querying to find where the missing values come from

#(df[cols].query('column_name.isna()')


## filling a Nan column and make it to a categoy

 df[cols].assign(column_name = df.column_name.fillna('Other').astype('category'))

## Méthodes

.loc
.index : permet de récupérer l'index des lignes en attribut

exemple : index_with_nan = data_conso.index[data_conso.loc[:,'Année'].isnull()]


méthode .str.replace pour remplacer du texte dans une colonne.
exemple : 
source : https://www.youtube.com/watch?v=KokJHxiE14s&ab_channel=RobMulla à 5:40


# Matplotlib





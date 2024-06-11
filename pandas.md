# Etapes souvent utiles au démarrage d'un notebook
## montrer toutes les colonnes dans l'affichage
pd.set_option('display.max_columns', None)

## récupérer la liste des intitulés de colonnes
df.columns.tolist()

## Faire un subset d'un dataset

cols = ['','',...] # on choisit les colonnes qu'on veut garder dans df
df[cols] # on appelle dans df

# insérer une image html dans le markdown

<img src="http://ac.matra.free.fr/FB/20240322EB.jpg" alt="imagepixels" style="width:200px;"/>

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
## snippet pour générer des noms de colonnes avec suffixes multiples

annees = range(2010,2022)
fluides = ['elec','gaz','RCU','fioul','totale']
liste_DJU = []
for annee in annees:
    for fluide in fluides:
        annee_conso_fluide_DJU = str(annee) + '-conso_' + fluide + '_DJU'
        liste_DJU.append(annee_conso_fluide_DJU)
print(liste_DJU)

résultats :

['2010-conso_elec_DJU', '2010-conso_gaz_DJU', '2010-conso_RCU_DJU', '2010-conso_fioul_DJU', '2010-conso_totale_DJU', '2011-conso_elec_DJU', '2011-conso_gaz_DJU', '2011-conso_RCU_DJU', '2011-conso_fioul_DJU', '2011-conso_totale_DJU', '2012-conso_elec_DJU', '2012-conso_gaz_DJU', '2012-conso_RCU_DJU', '2012-conso_fioul_DJU', '2012-conso_totale_DJU', '2013-conso_elec_DJU', '2013-conso_gaz_DJU', '2013-conso_RCU_DJU', '2013-conso_fioul_DJU', '2013-conso_totale_DJU', '2014-conso_elec_DJU', '2014-conso_gaz_DJU', '2014-conso_RCU_DJU', '2014-conso_fioul_DJU', '2014-conso_totale_DJU', '2015-conso_elec_DJU', '2015-conso_gaz_DJU', '2015-conso_RCU_DJU', '2015-conso_fioul_DJU', '2015-conso_totale_DJU', '2016-conso_elec_DJU', '2016-conso_gaz_DJU', '2016-conso_RCU_DJU', '2016-conso_fioul_DJU', '2016-conso_totale_DJU', '2017-conso_elec_DJU', '2017-conso_gaz_DJU', '2017-conso_RCU_DJU', '2017-conso_fioul_DJU', '2017-conso_totale_DJU', '2018-conso_elec_DJU', '2018-conso_gaz_DJU', '2018-conso_RCU_DJU', '2018-conso_fioul_DJU', '2018-conso_totale_DJU', '2019-conso_elec_DJU', '2019-conso_gaz_DJU', '2019-conso_RCU_DJU', '2019-conso_fioul_DJU', '2019-conso_totale_DJU', '2020-conso_elec_DJU', '2020-conso_gaz_DJU', '2020-conso_RCU_DJU', '2020-conso_fioul_DJU', '2020-conso_totale_DJU', '2021-conso_elec_DJU', '2021-conso_gaz_DJU', '2021-conso_RCU_DJU', '2021-conso_fioul_DJU', '2021-conso_totale_DJU']

## Méthodes

* .loc
* .index : permet de récupérer l'index des lignes en attribut

exemple : index_with_nan = data_conso.index[data_conso.loc[:,'Année'].isnull()]


méthode .str.replace pour remplacer du texte dans une colonne.
exemple : 
source : https://www.youtube.com/watch?v=KokJHxiE14s&ab_channel=RobMulla à 5:40

# Matplotlib





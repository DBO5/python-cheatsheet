Python Cheatsheet personnelle de DBO5


# Github

Rajouter des modules python dans Github :

les mettre dans requirements.txt

folium==0.12.1

Partager un Jupyternotebook à quelqu'un qui n'a pas d'installation en local : passer par mybinder https://mybinder.org/

Deploying Voilà : 
https://voila.readthedocs.io/en/stable/deploy.html

Va rajouter un bouton "Voila" dans Jupyternotebook qui, une fois cliqué, exporte le fichier sans le code i.e. seuls les outputs et le markdown, sous forme de rapport HTML ! Génial pour communiquer un rapport.

On peut même créer ensuite une "appli" via Ipywidget en surcouche de Voila : https://ipywidgets.readthedocs.io/en/stable/

# Python



# Numpy




# Pandas

Méthodes

.loc
.index : permet de récupérer l'index des lignes en attribut

exemple : index_with_nan = data_conso.index[data_conso.loc[:,'Année'].isnull()]


méthode .str.replace pour remplacer du texte dans une colonne.
exemple : 
source : https://www.youtube.com/watch?v=KokJHxiE14s&ab_channel=RobMulla à 5:40


# Matplotlib




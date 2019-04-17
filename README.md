# README

2.2.3. Questions
Maintenant que ta BDD est prête, tu vas répondre aux questions ci-dessous :

a) Niveau facile

Quel est le nombre total d'objets Album contenus dans la base (sans regarder les id bien sûr) ?

Album.count

=> 347

Qui est l'auteur de la chanson "White Room" ?

author = Track.find_by(title: "White Room")
author.artist

=> "Eric Clapton"

Quelle chanson dure exactement 188133 milliseconds ?

duration = Track.find_by(duration: 188133)
duration.title

=> "Perfect"

Quel groupe a sorti l'album "Use Your Illusion II" ?

groupe = Album.find_by(title: "Use Your Illusion II")
groupe.artist

=> "Guns N Roses"

b) Niveau Moyen

Combien y a t'il d'albums dont le titre contient "Great" ? 

great = Album.where("title like ?", "%Great%")
great.count

=> 13

Supprime tous les albums dont le nom contient "music".

album = Album.where("title like ?", "%music%")
album.destroy_all

Combien y a t'il d'albums écrits par AC/DC ?

album_ACDC = Album.where(artist: "AC/DC")
album_ACDC.count

Combien de chanson durent exactement 158589 millisecondes ?

duration = Track.where(duration: 158589)
duration.count

Il n'y a pas de chansons qui durent 158589 millisecondes.



# challenge-mimse2014

Challenge d’apprentissage supervisé du Master 2 MIMSE :

<https://adrtod.github.io/challenge-mimse2014/>

Généré à l'aide du package [rchallenge](http://adrien.tspace.fr/rchallenge/) avec le code suivant :
```R
library(rchallenge)

new_challenge(template = "fr",
              title = "Challenge MIMSE 2014",
              author = "Adrien Todeschini",
              email = "adrien.todeschini@inria.fr",
              date_start = "7 oct. 2014",
              deadline = "2015-01-07 23:59:59")
              
new_team("CA_IB_YQ", "CLF_KH_VG", "FCS_CS_CD", "MP_DS_BT",
         "CC_JC_CD", "DZ_JK_MG", "GB_AD_BH", "Anonymous")
")

publish(output_file = "index.html")
```

Mise à jour automatique avec le cron suivant :

```
0 * * * * cd path/to/challenge && Rscript -e 'rchallenge::publish(output_file = "index.html")' && git commit -m "maj html" index.html && git push 
```

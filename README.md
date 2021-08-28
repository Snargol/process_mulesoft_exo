# process_mulesoft_exo


- Application 2:
```
- Créer des spec api permettant de récupérer les données via un endpoint “/processed-contracts” et une methode “GET”
- Ajouter au spec une queryParam “isPair” de type Boolean
- Créer un flow “fetch_data” qui va récupérer les données depuis “Application1” (le composant “Request” du module “Http” peut être utilisé)
- Créer un flow “process_data” qui va appeler le flow “fetch_data” et filtrer les données sur les Contract_ID paires si “isPair” = true sinon, filtrer les Contract_ID qui sont impaires dans un transformeMessage avec la fonction “filter” de dataweave.
- Ajouter au flow un transform message permettant de calculer le “amount_per_month” : = Amount / (End_Date(en mois) - Start_Date (en mois))
- Convertir le résultat en xml
- Appeler le flow “process_data” depuis le flow généré par les spec api
- (S’il y a le temps) Ajouter le protocol https en suivant ce tuto : https://docs.mulesoft.com/mule-runtime/4.3/build-an-https-service
```

# spring-cloud_streams-kafka

Dans ce projet on va met en pratique le broker kafka et comment l'utiliser et leurs APIs alors kafka en principe fourni un
broker généralement besoine de démarrer ce forme d'un cluster donc on peut démarrer plusieure instance de broker kafka
et pour  coordonner ces instances kafka besoin d'un utile qui s'appele zookeeper et aussi dans l'API kafka contiene
producer API qui permet à n'importe quel application d'envoyer des messages
consumer API qui permet à n'importe quel application de consumer des données ou des  messages
streams API qui permet de faire des traitement en temp réelle
connector API qui permet de connecter le cluster kafka avec autres systèmes comme les base de données

1- kafka fournit des outils comme kafka-console-consumer
   et kafka-console-producer pour consumer ou envoyer des données par un topic.
   Donc on va créer un application spring boot pour produire un événement et envoyer
   un message dans une topic kafka on utilisent RestController.Mais tout d'abord on va démarrer kafka après le démarrage de zookeeper.
   
   -start kafka et zookeeper.
   
   ![start kafka](https://user-images.githubusercontent.com/102171677/171921362-b967825c-ea43-45c8-8d7c-4d0c20028712.png)

   
   -kafka-console-consumer et kafka-console-producer.
   
   ![pruducer_consomuer_console](https://user-images.githubusercontent.com/102171677/171921452-7ff3218e-78ef-49a0-83b5-b29d2386f83f.png)

   
   -test de RestController.
   
   ![demager la fonction pour push des message](https://user-images.githubusercontent.com/102171677/171921555-78134e07-178b-480b-b6c0-67cdfb24916d.png)
     
   ![pruducer_consomuer_console](https://user-images.githubusercontent.com/102171677/171921659-d06eb9bd-1f7e-4ff2-ac19-beb602ca45ac.png)



   
2- créer un consumer qui permet de faire un subscribe vers le topic kafka c'est-à-dire les message que j'envoie dans cette
   application on va les lires a partir de se consumer il suffit de récupérer ces messages et ces données qui sont envoyés .
   
   ![consumer_java](https://user-images.githubusercontent.com/102171677/171920238-57977c87-5e41-4eb8-a64a-4d8773895fd4.png)

  
3- créer un supplier  de telle sorte que a chaque seconde je voie un message sur un topic.

   ![dibi message 100ms](https://user-images.githubusercontent.com/102171677/171920357-73eac4d4-ef96-4e90-8ad6-af7d37a225ba.png)
   
   
   ![topic4 avec spesification de key et value et teme](https://user-images.githubusercontent.com/102171677/171920506-bf66d093-81e3-4b97-a9ed-cdf07475c855.png)


4- Créer un consumer et un producer pour lire et envoyer des messages sous format JSON.

   ![pruducer_consomuer_console](https://user-images.githubusercontent.com/102171677/171920582-b95e7ad4-cbe4-4cea-bece-b3d2029d8a5c.png)


5- comment utiliser kafka streams c'est - à -dire faire un traitement de données en temps réel.

   - Afficher les enregistrements en temps réel.
     
     ![tou les enregestrement dans le store](https://user-images.githubusercontent.com/102171677/171920862-2f0c6c4a-87e2-485b-80fb-2bda8e2cd1bf.png)
     
   - le flux de données en temps réel comme des statistiques.  
     
     ![statistic des page](https://user-images.githubusercontent.com/102171677/171921064-10d25ae1-3026-462a-886e-e6d68f498515.png)


Dans cette application on va faire toutes les use case dans la même application

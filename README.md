pieges-homestead
================

Quelques pièges à éviter avec Homestead

# activer Livereload

Parce que Livereload est un client qui a besoin de se connecter à un serveur qui sert sur le port 35729 (à vérifier), il est nécessaire de forwarder le port en question dans la config de Homestead. Le fichier à modifier est Homestead/scripts/homestead.rb

Il faut ajouter la ligne `config.vm.network "forwarded_port", guest: 35729, host: 35729` puis re-provisionner la VM.

# mettre à jour Ruby

Si l’installation de Compass ou autres pose problème, il faut peut-être mettre à jour Ruby. Pour ça `sudo apt-get install ruby-dev`



deployment redis server 

ansible-playbook -i hosts site_db.yml  --ask-pass

deployment application in plate forme stage

ansible-playbook -i hosts site_stage.yml --extra-vars="APP_VERSION=1.0-RELEASE" --ask-pass

deployment application in production plate forme 

ansible-playbook -i hosts site_prod.yml --extra-vars="APP_VERSION=1.0-RELEASE" --ask-pass

##Plugin pipeline sous jenkins qui permet d'orchestrer entre les différents environnements
### j'ai déployé le socle technique sous nexus , pour résoudre le problème du réseau 
##pour lancer en mode autonome , il faut changer les urls de downloads apache tomcat httpd apr apr-util et redis



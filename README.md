# freebox-delta-docker

http://mafreebox.freebox.fr
Se connecter
Aller dans "VMs"
Créer une VM ( CPU 2, Ram 957, OS via liste OS pré-installé: Ubuntu LTS ) 
Renseigner un nom d'utilisateur (<votre user>)
Créer une clé SSH via la commande suivante: 
ssh-keygen -o -a 100 -t ed25519 -f /home/user/.ssh/<nom de la clé> -C "<votre com>"
Copier le contenu de la clé publique générée ( en .pub ) dans le champ "clé SSH" de Freebox OS
Continuer installation de la VM avec taille disque 42Go et terminer
Allumer la VM
Lui ajouter un bail DHCP afin d'éviter que son IP locale ne change

Connection à la VM en ssh via:
ssh -i /home/user/.ssh/<nom de la clé> <votre user>@<ip vm>

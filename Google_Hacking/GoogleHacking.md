# Google_Hacking_Recap

![Google hacking is interesting](https://github.com/Gisc4rd/images/blob/main/google_hacking.png)

## I-Comment fonctionnent les recherches sur Google

**Google** indexe presque tout ce qui est connecté à Internet, ce qui inclut également différentes informations privées de services mal configurés. Cela peut souvent être utile et tout aussi nocif en même temps. Vous devez vous assurer de ne vous connecter à aucun des services, même si le mot de passe est exposé, car cela pourrait vous causer des ennuis car vous n'en avez pas l'autorisation. Cependant, si vous avez quelque chose d'hébergé en ligne, vous pouvez utiliser certaines des commandes dork sur votre domaine juste pour vous assurer que vous n'avez rien laissé exposé que le pirate peut utiliser pour vous obtenir.


## II-C'est quoi Google Dorks?

La première étape a été d'essayer de comprendre le terme **Google hacking**, ce à quoi il fait référence et ce qu'il impliquait. Nous nous sommes donc retrouvés avec un terme qui revenait: **Google dorks**.

Google Dorks c'est justement l'ensemble des possibilités de recherches avec lasyntaxe propre à Google, et qui permet de faire du hacking de sites web ou d'application web ou SaaS. 

Grâce à Google Dorks on utilise donc Google comme un outil de hack, on parle donc de Google Hacking ou de Google Dorking.

Il est alors possible de :

> Trouver des informations sensibles (des mails stockés en ligne, des mots de passe, ...).
> 
> Trouver des pages d'authentification d'application web.
> 
> Trouver du matériel connecté à Internet (caméras vidéo, routeurs internet, imprimantes, mais aussi matériel industriel, ...).
> 
> Trouver des serveurs web mal configurés, ou installés par défaut.
> 
> Trouver les technologies ou des outils sur le serveur web (phpmyadmin, phpinfo(), zones d'administration du site, ...).
> 
> Trouver des vulnérabilités qui permettent de pirater la cible.

Le Google dorking, aussi appelé Google hacking, peut retourner des informations qu’il est difficile de localiser grâce à des recherches dîtes simples. Bien souvent, les résultats de recherche renvoyés par Google sont des informations que le propriétaire du site internet n’avait pas l’intention de dévoiler au public.

## III-Quels sont principaux dorks et leur utilité?

a-**site**

Il retourne les fichiers localisés sur un domaine particulier. Par exemple *site:www.monsite.com* "terme à rechercher" renverra les pages de www.monsite.com qui contiennent "terme à rechercher".

b-**Filetype**

Suivi sans espace par l’extension du fichier souhaité comme DOC, PDF, XLS ou autre, il limite les résultats à un type de document donné
*filetype:pdf "anonymat"* retournera les documents PDF contenant le mot anonymat.

c-**inurl**

Suivi par une phrase donnée, il retourne tous les résultats avec cette même phrase placée dans l’URL. inurl:"login.php" renverra toutes les pages ayant login.php dans leur url.

d-**intitle**

Suivi par une phrase donnée, il retourne tous les résultats avec cette même phrase placée dans le titre de la page. *intitle:"sécurité informatique"* permet de retrouver les pages dont les titres contiennent l'expression sécurité informatique.

e-**Cache**

Cela vous montrera la version en cache de n'importe quel site Web. Exemple : *cache: site.com*

f-**allintext**

La commande allintext permet de restreindre la recherche à la balise body des pages HTML, c'est-à-dire le corps de la page. Syntaxe: *allintext:{mots}*


g-**allintitle**

La commande allintitle permet de restreindre la recherche à la balise title des pages HTML. Syntaxe: *allintitle:{mots}*


## IV-Exemples de Google Dorking

#### a-Explorer les fichiers LOG pour les identifiants de connexion**

Il s'agit d'un processus pour trouver les fichiers .LOG accidentellement exposés sur Internet. Il s'agit essentiellement d'un fichier LOG contenant des indices sur les informations d'identification du système ou sur les différents comptes d'utilisateur/administrateur qui existent dans le système.

***allintext:username|password filetype:log***

#### b-Explorer les configurations à l'aide de fichiers ENV

.env est utilisé par divers frameworks de développement Web populaires pour déclarer des variables générales et des configurations pour les environnements locaux et de développement.

***DB_USERNAME filetype:env  
DB_PASSWORD filetype:env***

En utilisant la commande, vous pouvez trouver la liste des sites qui exposent publiquement leur fichier env sur Internet. La plupart des développeurs insèrent leur fichier .env dans le répertoire public principal du site Web, ce qui peut causer de graves dommages à leur site s'il tombe entre les mains de cybercriminels.

Si vous cliquez sur l'un des fichiers .env exposés, vous remarquerez que les noms d'utilisateur, mots de passe et adresses IP non chiffrés sont directement exposés dans les résultats de la recherche.

#### c-Pour explorer les serveurs FTP ouverts

L'absence de définition des autorisations d'accès dans le FTP peut être la cause directe de la publication involontaire d'informations internes. Même dangereux, si le serveur FTP est en état "Write", cela peut créer un risque que le serveur soit utilisé comme "stockage" pour les virus informatiques et les fichiers copiés illégalement.

Avec la commande dork suivante, vous pourrez facilement explorer les serveurs FTP exposés publiquement, qui peuvent parfois explorer beaucoup de choses.

***intitle:"index of" inurl:ftp***

### Refer to this: <https://tryhackme.com/room/googledorking>

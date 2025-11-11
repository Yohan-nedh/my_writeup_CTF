# Taking LS

**Résolution**

Tout d'abord exécutons la commande **unzip The Flag.zip** ce qui nous donne un dossier nommé **The Flag** dans lequel nous avons deux autres dossier


<img width="366" height="109" alt="image" src="https://github.com/user-attachments/assets/86353293-8340-491d-8788-b655ef121e6a" />

mais regardons le dossier The flag dans lequel nous remarquons qu'il y a un pdf 

<img width="407" height="170" alt="image" src="https://github.com/user-attachments/assets/769ede77-a80f-4a30-ac03-62e644725d4a" />


nous remarquons que pour acceder à ce pdf il nous faut un mot de passe, nous serions bien tenté d'effectuer un brute force mais tout d'abord essayons de bien analyse le dossier **The Flag**

<img width="463" height="269" alt="image" src="https://github.com/user-attachments/assets/fa4405a0-ca57-49b5-9bf7-5fabe2be7e4a" />

dans terminal la commande ls -laR affiche tous les fichiers (même les cachés) de tous les dossiers (récursivement) avec plein de détails

<img width="500" height="576" alt="image" src="https://github.com/user-attachments/assets/024a5ba3-08e0-49f5-89d5-802eb5bce5be" />

nous remarquons un autre dossiers nommé **/.ThePassword** avec un fichier **ThePassword.txt** exécutons la commande cat pour voir ce qu'il contient

<img width="500" height="67" alt="image" src="https://github.com/user-attachments/assets/c199821a-821f-4ec4-88f3-2008fe2cd197" />

Donc le mot de passe du pdf est: Im The Flag

Bingo voici le flag:

<img width="500" height="67" alt="image" src="https://github.com/user-attachments/assets/135c831f-1680-4392-bcbd-680d1cac4fac" />

#

# I'm a dump

Dans ce défi nous avec fichier nommé **file** la première étape est de vérifier la nature du fichier en utilisant la commande **file file**

<img width="938" height="82" alt="image" src="https://github.com/user-attachments/assets/b2b5eac5-3fbd-4b87-95be-79ebb87ce004" />

Il s'agit d'un exécutable ELF 64 bits pour Linux (x86-64), compilé avec GCC sur Arch Linux, non dépouillé (contient les symboles de débogage), et dynamiquement lié à la glibc.
Ensuite utilisons les commandes **strings et less** pour afficher les chaînes de caractères et peut-être le flag

<img width="299" height="59" alt="image" src="https://github.com/user-attachments/assets/029cf01b-ee33-4209-bcfc-1116eba1ace1" />

dont la sortie est celle-ci:

<img width="358" height="941" alt="image" src="https://github.com/user-attachments/assets/2cb9b0d3-5e3d-448c-ad4a-20d8233846a1" />


voici ce que nous avons **CTFlearnH{fl4ggyfHl4g}H** mais nous remarquons que nous avons des **H** en trop et si nous les enlevons nous **CTFlearn{fl4ggyfl4g}**.

Et pour confirmation nous avons Le fichier source principal s’appelle flaggyFlag.c qui nous confirme que le flag est bien celui-ci.

<img width="358" height="62" alt="image" src="https://github.com/user-attachments/assets/1b412257-f284-4c7b-bde7-f9d9571102e1" />





#

# Binwalk
Dans ce défi nous avons une image

<img width="480" height="320" alt="PurpleThing" src="https://github.com/user-attachments/assets/2e9f564f-df3a-4720-a150-366c7b70effc" />


premièrement le défi s'appel **binwalk** alors nous allons utiliser cette commande

<img width="700" height="150" alt="1_binwalk" src="https://github.com/user-attachments/assets/d1c74d12-48de-4826-8b8b-15c4bd279ce8" />

et nous remaquons que nous avons une autre image dans l'image utilisons **dd if=PurpleThing.jpeg of=fl.png bs=1 skip=153493** qui nous permet d'extraire la photo

<img width="682" height="89" alt="image" src="https://github.com/user-attachments/assets/b3a259aa-6af1-4e22-871b-a539a9df701c" />


J'ai  nommé la photo **fl.png** et quand nous l'ouvrons bingo nous avons le flag

<img width="401" height="59" alt="fl" src="https://github.com/user-attachments/assets/fcb4aa11-8744-47ff-bc53-a0d8ae108772" />

#

# Git is Good

dans ce défi nous avons un fichier nommé **gitIsGood.zip** que nous dézippons avec la commande **unzip**

<img width="669" height="815" alt="image" src="https://github.com/user-attachments/assets/d278de51-d1fa-4571-bb11-0d110eef1be1" />

et nous remarquons que nous avons un fichier nommé **flag.txt** donc nous faisons ceci

<img width="387" height="111" alt="image" src="https://github.com/user-attachments/assets/3c248850-e16c-482d-b449-fda87a13bdd3" />

et hop voici le flag ah ah ah, non ce n'est qu'un indice rappeler vous que le nom du défi est git is good et ce que nous avons eu comme flag{REDACTED}. Le flag est dans l’historique Git, supprimé du fichier actuel (flag.txt → flag{REDACTED}), mais toujours présent dans un ancien commit. De ce fait nous allons exécuter cette commande
**git log --all --full-history -- flag.txt**

<img width="543" height="316" alt="image" src="https://github.com/user-attachments/assets/32faf1e3-ca93-4b4a-80e2-aba59ac11b1c" />

maintenant pour voir ce qui été supprimer nous pouvons utiliser la commande **git show** suivi du hash 

<img width="543" height="250" alt="image" src="https://github.com/user-attachments/assets/c1a38999-4379-41c9-bed7-6726470288c7" />

et voici le flag: **flag{protect_your_git}**













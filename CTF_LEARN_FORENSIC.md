**Taking LS**

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




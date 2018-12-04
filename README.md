0)$ git config --global user.name "Mazzola"
0bis)$ git config --global user.email "mailFreeTax@protonmail.com"
IMPORTANTE: prima di iniziare a creare un progetto github è necessario impostare username e password. in caso contrario i commit verranno fatti ad altro nome !

1)$ git init //comando per creare una repo locale
2)$ touch .gitignore //il comndo crea  un file .gitignore. all'interno di esso verranno elencati i file da ignorare quando si esegue l'add. Nel nostro caso i file .exe. se il file non fosse stato creato, in fase di merging GIT ci avrebbe restituito un errore che indica la impossibilità di mergiare automaticaamente i file .exe.
3)$ git add *; 
4)$ git commit -m "Inizializazione del progetto"; 
5)$ git add *;
6)$ git commit -m "busines core implementato";
7)$ git checkout -b "FIX_BUG"; //importante, la prima volta che si esegue un checkout è necessario inserire il parametro -b. -b serve a creare la nuova brenche su cui poi si sposterà il progetto.
8)$ git add *;
9)$ git commit -m "corretto errore nelle condizioni del for: prima contava solo fino a 9, adesso conta fino a dieci";
10)$ git checkout "master"
11)$ git add *;
12)$ git commit -m "system("PAUSE") inserito";
13)$ git checkout "FIX_BUG"
14)$ git add *;
15)$ git commit -m "inclusione namespace";
16)$ git checkout "master"
17)$ git merge "FIX_BUG"
18)$ git remote add "link1" https://github.com/Francescomazzola/stampatore-da-1-a-10.git //il comando git remote serve ad inizializzare una variabile che conterrà il link relativo alla repositori.  
19)$ git add *;
20)$ git commit -m "merge fatto ma con errori"
21)$ git push link1 master //importante, il push va eseguito per ogni branch
22)$ git push link1 FIX_BUG

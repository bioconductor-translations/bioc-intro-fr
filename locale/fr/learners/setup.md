---
title: Setup
---

- Veuillez vous assurer d'avoir accès à un tableur, tel que LibreOffice, Microsoft Excel ou Google Sheets.

- Installez R, RStudio et les packages (voir ci-dessous).

### R et RStudio

- R et RStudio sont des programmes a télécharger separemment et demandent des installations distincts. R est l'environnement de calcul statistique sous-jacent, mais utiliser R seul peut être pénible. RStudio est un environnement de développement graphique intégré
  (IDE) qui rend l'utilisation de R beaucoup plus simple et plus interactive. Vous avez besoin d' installer R avant d'installer RStudio. Après avoir installé les deux programmes, vous devrez installer des paquets R spécifiques depuis
  RStudio. Suivez les instructions ci-dessous pour votre système d'exploitation,
  puis suivez les instructions pour installer des paquets.

### You are running Windows

<br>

:::::::::::::::  solution

## Si vous avez déjà installé R et RStudio

- Ouvrez RStudio et cliquez sur « Aide » > « Rechercher les mises à jour ». Si une nouvelle version est
  disponible, quittez RStudio et téléchargez la dernière version de RStudio.

- Pour vérifier quelle version de R vous utilisez, démarrez RStudio et la première chose
  qui apparaît dans la console indique la version de R que vous
  exécutez. Alternativement, vous pouvez taper `sessionInfo()`, qui affichera également
  quelle version de R est installée. Allez sur
  le [site Web du CRAN](https://cran.r-project.org/bin/windows/base/) et vérifiez
  si une version plus récente est disponible. Si c'est le cas, veuillez le télécharger et l'installer. Vous pouvez [consulter ici](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) pour
  plus d'informations sur la façon de supprimer les anciennes versions de votre système si vous souhaitez le faire.

- Suivez les étapes décrites dans les instructions [pour tout le monde](#pour-tout-le-monde) en bas de cette page.

:::::::::::::::::::::::::

:::::::::::::::  solution

## Si vous n'avez pas encore installé R et RStudio

- Téléchargez R depuis le [site Web CRAN](https://cran.r-project.org/bin/windows/base/release.htm).

- Exécutez le fichier « .exe » qui vient d’être téléchargé

- Accédez à la [page de téléchargement de RStudio](https://www.rstudio.com/products/rstudio/download/#download)

- Under _All Installers_ select **RStudio xxxx.yy.zz-uuu.exe - Windows 10/11** (where x, y, z, and u represent version numbers)

- Double-cliquez sur le fichier pour l'installer

- Une fois installé, ouvrez RStudio pour vous assurer qu'il fonctionne et que vous n'obtenez aucun message d'erreur

- Suivez les étapes décrites dans les instructions [pour tout le monde](#pour-tout-le-monde) en bas de cette page.

:::::::::::::::::::::::::

### Vous utilisez macOS

<br>

:::::::::::::::  solution

## Si vous avez déjà installé R et RStudio

- Ouvrez RStudio et cliquez sur « Aide » > « Rechercher les mises à jour ». Si une nouvelle version est
  disponible, quittez RStudio et téléchargez la dernière version de RStudio.

- Pour vérifier quelle version de R vous utilisez, démarrez RStudio et la première chose qui apparaît dans la console indique la version de R que vous exécutez. Alternativement, vous pouvez taper `sessionInfo()`, qui affichera également quelle version de R est installée. Allez sur le [site Web de CRAN](https://cran.r-project.org/bin/macosx/) et vérifiez si une version plus récente est disponible. Si c'est le cas, veuillez le télécharger et l'installer.

- Suivez les étapes décrites dans les instructions [pour tout le monde](#pour-tout-le-monde) en bas de cette page.

:::::::::::::::::::::::::

:::::::::::::::  solution

## Si vous n'avez pas encore installé R et RStudio

- Téléchargez R depuis le [site Web CRAN](https://cran.r-project.org/bin/macosx/).

- Sélectionnez le fichier « .pkg » avec la dernière version de R

- Double-cliquez sur le fichier téléchargé pour l'installer

- Ça peut aussi être utile d'installer [XQuartz](https://www.xquartz.org/) (qui est nécessaire pour certains _packages_)

- Accédez à la [page de téléchargement de RStudio](https://www.rstudio.com/products/rstudio/download/#download)

- Under _All Installers_ select **RStudio xxxx.yy.zz-uuu.dmg - macOS 10.15+** (where x, y, z, and u represent version numbers)

- Double-cliquez sur le fichier pour l'installer

- Une fois installé, ouvrez RStudio pour vous assurer qu'il fonctionne et que vous n'obtenez aucun message d'erreur.

- Suivez les étapes décrites dans les instructions [pour tout le monde](#pour-tout-le-monde) en bas de cette page.

:::::::::::::::::::::::::

### Vous utilisez Linux

<br>

:::::::::::::::  solution

## Installez R à l'aide de votre gestionnaire de paquets et de RStudio

- Suivez les instructions pour votre distribution
  sur [CRAN](https://cloud.r-project.org/bin/linux), elles fournissent des informations pour obtenir la version la plus récente de R pour la plupart des  distributions Linux. Pour la plupart des distributions, vous pourriez utiliser votre gestionnaire de paquets (par exemple, pour Debian/Ubuntu, exécutez
  `sudo apt-get install r-base`, et pour Fedora `sudo yum install R`), mais nous
  ne recommandons pas cette approche car les versions fournies par ces gestionnaires sont généralement obsolètes. Dans tous les cas, assurez-vous d'avoir au moins R 4.2.0.
- Go to the RStudio download
  page
- Under _All Installers_ select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-xxxx.yy.zz-uuu-amd64.deb` at the terminal).
- Une fois installé, ouvrez RStudio pour vous assurer qu'il fonctionne et que vous n'obtenez aucun message d'erreur.
- Suivez maintenant les étapes dans les [instructions pour tout le monde](#for-everyone)

:::::::::::::::::::::::::

### Pour tout le monde

Après avoir installé R et RStudio, vous devez installer quelques packages
qui seront utilisés pendant l'atelier. Pendant le cours, nous verrons en détail comment installer des packages et les commandes ci-dessous. Pour l'instant, suivez simplement les instructions ci-dessous :

- Démarrez RStudio en double-cliquant sur l'icône puis tapez :

```r
install.packages(c("BiocManager", "remotes"))
BiocManager::install(c("tidyverse", "SummarizedExperiment", "hexbin", "patchwork", "gridExtra", "lubridate"))
```

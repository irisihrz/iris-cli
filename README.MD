# Iris-CLI
**Iris-CLI** est un outil en ligne de commande inspiré par **ani-cli**, mais entièrement repensé avec une interface améliorée. Il permet de scraper des épisodes d'animés en **VOSTFR** et **VF** (contrairement à ani-cli qui ne supporte pas ces options). Vous pouvez ainsi facilement accéder à vos épisodes préférés dans les deux langues !

---

## Quick Install (Copier-Coller)
### Pour Arch Linux
```bash
# Installer les dépendances de Yay
sudo pacman -S base-devel git

# Cloner et installer Yay
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# Installer les dépendances nécessaires
sudo yay -S youtube-dl
sudo pacman -S mpv sed curl awk grep

# Installer Iris-CLI
yay -S iris-cli
```

### Pour Debian/Ubuntu
```bash
# Installer les dépendances
sudo apt update
sudo apt install -y git curl youtube-dl mpv sed awk grep

# Supprimer le dossier existant si nécessaire
if [ -d "$HOME/iris-cli" ]; then
    rm -rf "$HOME/iris-cli"
fi

# Cloner le dépôt
git clone https://github.com/irisihrz/iris-cli.git "$HOME/iris-cli"
cd "$HOME/iris-cli"

# Installer en tant que commande système
sudo mv iris-cli /usr/local/bin/iris-cli
sudo chmod +x /usr/local/bin/iris-cli

# Vérifier l'installation
iris-cli --version
```

### Pour Fedora
```bash
# Installer les dépendances
sudo dnf update -y
sudo dnf install -y git curl youtube-dl mpv sed awk grep

# Supprimer le dossier existant si nécessaire
if [ -d "$HOME/iris-cli" ]; then
    rm -rf "$HOME/iris-cli"
fi

# Cloner le dépôt
git clone https://github.com/irisihrz/iris-cli.git "$HOME/iris-cli"
cd "$HOME/iris-cli"

# Installer en tant que commande système
sudo mv iris-cli /usr/local/bin/iris-cli
sudo chmod +x /usr/local/bin/iris-cli

# Vérifier l'installation
iris-cli --version
```

---

## Installation sur Arch Linux
### Étape 1 : Installer Yay
Si vous n'avez pas encore installé **Yay** (un AUR helper), suivez ces étapes :
1. **Installer les dépendances de Yay** :
   ```bash
   sudo pacman -S base-devel git
   ```
2. **Cloner le dépôt Yay depuis AUR** :
   ```bash
   git clone https://aur.archlinux.org/yay.git
   ```
3. **Se rendre dans le répertoire de Yay** :
   ```bash
   cd yay
   ```
4. **Construire et installer Yay** :
   ```bash
   makepkg -si
   ```
Une fois installé, vous pouvez utiliser Yay pour installer iris-cli.

---

### Étape 2 : Installer Iris-CLI
Une fois que Yay est installé, vous pouvez installer **iris-cli** avec la commande suivante :
```bash
yay -S iris-cli
```

---

## Installation sur n'importe quel OS
Si vous souhaitez installer **iris-cli** sur n'importe quel système d'exploitation, vous pouvez utiliser **git** pour cloner le dépôt et l'exécuter directement depuis votre terminal :
1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/irisihrz/iris-cli.git
   ```
2. **Se rendre dans le répertoire** :
   ```bash
   cd iris-cli
   ```
3. **Lancer Iris-CLI** :
   ```bash
   ./iris-cli
   ```

---

## Installation en tant que commande sur Linux
Pour installer **iris-cli** en tant que commande sur Linux, vous pouvez le déplacer dans `/usr/local/bin` :
1. **Déplacer le fichier vers `/usr/local/bin/`** :
   ```bash
   sudo mv iris-cli /usr/local/bin/iris-cli
   ```
2. **Lui donner les permissions** :
   ```bash
   sudo chmod +x /usr/local/bin/iris-cli
   ```
Vous pouvez maintenant lancer **iris-cli** simplement en utilisant la commande `iris-cli` depuis n'importe quel terminal.

---

## Dépendances
Avant d'utiliser **iris-cli**, assurez-vous d'avoir installé toutes les dépendances nécessaires. Vous pouvez les installer en utilisant les commandes suivantes :
```bash
sudo yay -S youtube-dl
sudo pacman -S mpv
sudo pacman -S sed
sudo pacman -S curl
sudo pacman -S awk
sudo pacman -S grep
```

---

## Utilisation
Une fois **iris-cli** installé, vous pouvez l'utiliser pour scraper des épisodes d'animés en **VOSTFR** et **VF** directement depuis votre terminal.
Par exemple, pour rechercher un anime et obtenir les options disponibles :
```bash
iris-cli <nom-de-l-anime>
```
Vous pourrez choisir parmi les différentes options en **VOSTFR** ou **VF** proposées.

---

## Contribuer
Les contributions sont les bienvenues ! Si vous souhaitez améliorer **iris-cli**, n'hésitez pas à fork le projet et à soumettre une pull request.

---

## License
Ce projet est sous licence MIT. Vous pouvez le redistribuer et le modifier librement.

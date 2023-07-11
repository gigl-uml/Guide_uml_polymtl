# Guide de référence UML 2.0 - Polytechnique Montréal
_____

## Installation sur Windows

### Installation de Ruby
1. Téléchargez Ruby sur votre machine au lien suivant: https://rubyinstaller.org/downloads/. *Il n'est pas nécéssaire de télécharger une version avec Devkit*

2. Une fois le programme téléchargé, vous pouvez le lancer, accepter sa license, choisir un emplacement puis vous laisser cochée la case `Run 'ridk install' ... ` avant de cliquer sur Finish

3. Une fenêtre de terminal devrait s'ouvrir. Entrez les commandes 1, 2 et 3 dans l'ordre lorsque la dernière est terminée.

Ruby devrait maintenant être bien installé. Pour vous en assurer, vous pouvez ouvrir une ligne de commande ordinaire et entrez la commande `ruby -v`, votre version devrait s'afficher.

### Installation de Jekyll
1. Dans votre terminal, entrez la commande `gem install jekyll bundler`. Ceci devrait avoir bien installé Jekyll, vous pouvez vous en assurer avec la commande `jekyll -v` qui est sensée afficher votre version.


### Lancer le projet pour la première fois
1. Lors du premier lancement de l'application, sur la racine du projet, lancez la commande `bundle exec jekyll serve`. Ceci devrait lancer votre site à l'adresse localhost:4000 (127.0.0.1/4000).

Pour les prochaines fois, la simple commande `jekyll serve --open-url` suffira pour lancer le site.

## Installation sur Linux (Ubuntu)

### Installation de Ruby
`sudo apt-get install ruby-full build-essential zlib1g-dev`

### Installation de Jekyll
    echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
    echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
    echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
    source ~/.bashrc

Puis

`gem install jekyll bundler`

### Lancer le projet pour la première fois
1. `bundle install`
2. `bundle exec jekyll serve`

Pour les prochaines fois, la simple commande `jekyll serve --open-url` suffira pour lancer le site.

# Git

Sowohl private als auch chaosdorfnahe Projekte können in unserem GitLab abgelegt werden. Repositories sind dort entweder privat (nur für ausgewählte Personen sichtbar), intern (nur für Chaosdorf) oder öffentlich. Beachte, dass Externe zwar lesend zugreifen, sich aber nicht im GitLab registrieren und damit auch keine Issues oder Pull Requests erstellen können.

Für einige Projekte gibt es inzwischen auch öffentliche Repositories auf GitHub. Um dort Commit-Rechte zu kriegen, registriert ihr euch auf GitHub, und wir fügen euch dann der chaosdorf-Organization hinzu. Schreibt einfach eine E-Mail an [github@chaosdorf.de](mailto:github@chaosdorf.de).

## HowTos

- GitHub Anleitungen
  - [https://training.github.com/](https://training.github.com/)
  - git cheat sheet [https://training.github.com/downloads/de/github-git-cheat-sheet/](https://training.github.com/downloads/de/github-git-cheat-sheet/)
- Git explained with cats: [https://girliemac.com/blog/2017/12/26/git-purr/](https://girliemac.com/blog/2017/12/26/git-purr/) 
- Interaktiver Kurs für Einsteiger: [https://learngitbranching.js.org/?locale=de_DE](https://learngitbranching.js.org/?locale=de_DE) / Learn Git Branching [https://pcottle.github.io/learnGitBranching/](https://pcottle.github.io/learnGitBranching/)
- First Aid Git: Ich möchte $sacheX machen, wie geht das? [http://firstaidgit.io/](http://firstaidgit.io/)
- Interaktiver Kurs: [https://try.github.io/levels/1/challenges/1](https://try.github.io/levels/1/challenges/1)
- eine einfache Anleitung um git zu lernen. Kein Schnick-schnack: [git - Der einfache Einstieg](https://try.github.io/levels/1/challenges/1)
- Ein Einstieg: [https://www.atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials)
- Rewriting history [https://www.atlassian.com/git/tutorials/rewriting-history](https://www.atlassian.com/git/tutorials/rewriting-history)
- Oh shit, git! [http://ohshitgit.com/](http://ohshitgit.com/)
- An Introduction to Using Git [https://www.linux.com/learn/intro-to-linux/2018/7/introduction-using-git](https://www.linux.com/learn/intro-to-linux/2018/7/introduction-using-git)
- OH MY GIT! Ein Spiel um git zu lernen [https://ohmygit.org](https://ohmygit.org)

### username/email

How to show or change your Git username or email address

### mergetool

Das einem am sympatischsten erscheinende merging tool in git einrichten:

```
git config --global merge.tool meld
```

und den aktuellen konflikt mit

```
git mergetool
```

beheben.

| name+url | license	| used by |
| -------- | -------- | ------- |
| meld	   | GPLv2    | bison   |

Andere diff-tools:

vimdiff, meld, opendiff, kdiff3, tkdiff, xxdiff, tortoisemerge, gvimdiff, diffuse, ecmerge, p4merge, araxis, vimdiff, emerge, bc3 (Beyond Compare 3)

### README.md

Um auf GitHub die README.md Dateien ordenlich formatieren zu können, gibt es diverse nützliche Tutorials:

GitHubs offizielle Hilfe: [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)
Markdown: [Syntax](http://daringfireball.net/projects/markdown/syntax)
Praktisches Beispiel: [GitHub Flavored Markdown Examples](https://github.com/mojombo/github-flavored-markdown/blob/gh-pages/_site/sample_content.md)
Code des Parsers: [GitHub Markup](https://github.com/github/markup#readme)

## git clients

| name | type | Platform | Url | license |
| ---- | ---- | -------- | --- | ------- |
| GitKraken | GUI | Win, Lin, Mac | [https://www.gitkraken.com/](https://www.gitkraken.com/)| proprietary, free, pro, enterprise |

- git GUI client liste: [https://git-scm.com/downloads/guis/](https://git-scm.com/downloads/guis/)

## Extended

- [Please, oh please, use git pull --rebase](https://coderwall.com/p/7aymfa?utm_source=feedburner&utm_medium=twitter&utm_campaign=Feed%3A+hnycombinator+%28HN+-+hnycombinator%29)
- [.gitignore file generator](https://www.gitignore.io/)
- [Oh my git - An open source game about learning Git!](https://ohmygit.org/)
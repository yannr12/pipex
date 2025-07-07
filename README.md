# Pipex: Maîtrise des Pipes UNIX ⚙️

## Introduction

Bienvenue dans Pipex! 🚀 Ce projet vous plonge au cœur d'un mécanisme UNIX fondamental : les pipes. Vous allez implémenter un programme capable de reproduire le comportement des redirections et des enchaînements de commandes shell. Préparez-vous à jongler avec les processus et les entrées/sorties ! 💾

## Le Concept

Le but de ce projet est de comprendre et de reproduire le fonctionnement de la commande shell suivante :

$< file1 cmd1 | cmd2 > file2 

Votre programme pipex prendra un fichier en entrée, exécutera une première commande dont la sortie sera redirigée vers l'entrée d'une seconde commande, et enfin, la sortie de cette seconde commande sera écrite dans un fichier de destination.

## Utilisation

Votre programme s'exécute avec les arguments suivants :

./pipex <file1> <cmd1> <cmd2> <file2> 

    <file1>: Le fichier d'entrée.

<cmd1>: La première commande shell avec ses paramètres.

<cmd2>: La seconde commande shell avec ses paramètres.

<file2>: Le fichier de sortie.

## Exemples 📋

    ./pipex infile "ls -l" "wc -l" outfile doit se comporter comme < infile ls -l | wc -l > outfile.

./pipex infile "grep a" "wc -w" outfile doit se comporter comme < infile grep a | wc -w > outfile.

## Partie Obligatoire 🧑‍💻

Le programme principal se trouve à la racine de votre dépôt.

    Nom du programme : pipex 

Fichiers à rendre : Makefile, *.h, *.c 

Règles Makefile : NAME, all, clean, fclean, re 

Arguments : file1 cmd1 cmd2 file2 

Fonctions externes autorisées : open, close, read, write, malloc, free, perror, strerror, access, dup, dup2, execve, exit, fork, pipe, unlink, wait, waitpid. Vous pouvez également utiliser 

ft_printf ou tout équivalent que vous avez codé.

Libft : Autorisée ✔️ 

Description : Le projet consiste à gérer des pipes.

## Contraintes spécifiques :

    Votre programme doit être écrit en C.

Respect de la Norme.

Pas de crash inattendu (segmentation fault, bus error, double free, etc.).

Aucune fuite de mémoire ne sera tolérée.

Votre Makefile doit compiler vos sources avec les flags 

-Wall, -Wextra, et -Werror.

Votre Makefile ne doit pas 

relink inutilement.

## Partie Bonus (Optionnel) ✨

Les bonus ne seront évalués que si la partie obligatoire est 

PARFAITE (complète et sans aucun dysfonctionnement).

Vous obtiendrez des points supplémentaires si vous implémentez :

    Gestion de plusieurs pipes : Par exemple, ./pipex file1 cmd1 cmd2 cmd3 ... cmdn file2 doit se comporter comme < file1 cmd1 | cmd2 | cmd3 | ... | cmdn > file2.

Gestion de here_doc (<< et >>) : Lorsque le premier paramètre est "here_doc", par exemple ./pipex here_doc LIMITER cmd cmd1 file doit se comporter comme cmd <<< LIMITER puis cmd1 >> file.

## Rendu et Évaluation 🤝

    Rendez votre travail sur votre dépôt Git assigné.

Seul le travail présent sur votre dépôt sera évalué.

Vérifiez bien les noms de vos fichiers et dossiers pour qu'ils soient conformes au sujet.

L'évaluation de la partie obligatoire et de la partie bonus sont séparées.

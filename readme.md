# Examen 2 – Logique de programmation et sécurité  
## Instructions 
- Il s’agit d’un travail individuel.
- La durée prévue de l’examen est de 2h (2 x 1h), mais tout le monde a droit à 4h (2 x 2h).
- C’est un examen à livre ouvert, vous avez le droit à tout sauf internet et l’IA.
- Le notes de cours et Omnivox sont autorisées.

## Critères d’évaluation 


| Question                        |Critères d’évaluation	                                                                            | Points  |
|---------------------------------|----------------------------------------------------------------------------------------------------  |---------|
| **Résolution de problème (lundi)**	 |Production d’un algorithme adéquat qui répond à un problème donné.	                                | /6      |
| 	                               |Production d’un programme fonctionnel conforme aux normes et standards du cours.	                | /6      |
| 	                               |Production d’une documentation de qualité respectueuse des normes du cours et des règles d’orthographe et de grammaire  | 	    /3 |
| **Tests et débogage   (jeudi)**	    |Repérage complet des erreurs et corrections pertinentes du code fourni                             | /6      |
| 	                               |Production d’un plan de tests	                                                                    | /3      |
| 	                               |Production de tests unitaires adéquats                                                             | 	/6     |

## Partie 2 : Tests et débogage

1. Commencer par faire un fork pour avoir votre propre copie du projet d'examen
2. Inviter l'enseignante comme collaboratrice
3. Faire un clône de votre _repository_ dans PyCharm
4. Faire des commit-push régulièrement
5. Vous êtes responsable de vérifier que votre dernier push contient tout votre code.

## Sujet : Calcul des notes d’une compétition de patinage

### Objectifs
- Production de plan de tests
- Production de tests adéquats selon le plan de tests 
- Repérage complet des erreurs et correction du code fourni 
---

## Contexte
Dans une compétition de patinage artistique, les compétiteurs exécutent un enchaînement de mouvements acrobatiques (sauts, tours, etc.).  
Chaque mouvement est évalué selon deux critères :
1. **La difficulté**, exprimée par une *valeur de base* (un nombre décimal).
2. **La qualité d’exécution**, évaluée par **9 juges** qui attribuent chacun une note entre **-3 et +3**.

Le but de cet exercice est d’écrire un programme qui calcule les **points totaux** attribués à chaque patineur, à partir de ces données.

---

## Règle de calcul
Pour chaque mouvement :
1. On prend les **9 notes des juges**.
2. On **retire la note la plus haute et la plus basse** (une seule occurrence de chacune, même si elles apparaissent plusieurs fois).
3. On calcule la **moyenne** des 7 notes restantes.
4. Le **total des points** = `valeur_de_base + moyenne`.

Exemple :  
> Valeur de base = 3.2  
> Notes = [3, 2, 1, 2, 3, 3, 2, 2, 3]  
> → On enlève un `1` (min) et un `3` (max).  
> → Moyenne = 17 / 7 = 2.43  
> → Total = 3.2 + 2.43 = **5.63**

---

## Structure du projet : 

### Programme principal: `main.py`
- Exemple de programme principal
- Vous pouvez le lire
- Rien à modifier ici.
### Plan de tests: `plan_tests.md`
- Plan de test à compléter
### Tests unitaires: `test_notation.py`
- Fichier pour programmer vos tests unitaires
- Les 2 fonctions doivent être testées
- Utilisez les donneés du plan de tests
### Module: `notation.py`
- La documentation des fonctions est correcte
- Le code contenu dans les fonctions doit être corrigé
```python
def valider_notes(notes: list[float]) -> bool:
    """
    Vérifie que la liste de notes contient exactement 9 entiers entre -3 et +3.
    :param notes: liste de notes
    :returns: vrai si la liste et valide, sinon faux.
    """
    
def calculer_points(vbase, notes):
    """
    Calcule le total des points pour un mouvement de patinage.
    Paramètres :
        vbase (float) : valeur de base du mouvement
        notes (list[int]) : 9 notes des juges (valeurs entre -3 et 3)
    Retourne :
        float : total des points (vbase + moyenne des notes restantes)
    """
``` 
# Imane
Exercice 1 : 

*Algorithme* : le processus de saisie de code PIN  
*Variables* : `code`, `i`, `tenta` : Entier  
*Constante* `PIN = 0692`  

*Début*  
  écrire ("Veuillez saisir un code de 4 chiffres")  
  lire (code)  
  tenta ← 0  
  Pour i de 1 à 3, pas = 1, faire  
    tenta ← 0 + i  
    Si tenta > 3  
      écrire ("blocage")  
    Si code = PIN  
      écrire ("succès")  
    Sinon  
      écrire ("erreur")  
    Fin Si  
  Fin si  
 Fin pour  
Fin
Exercice 2 : 

 Algorithme: permutation de deux variables

*Variables:*
`A`, `B`, `C`: Entier

*Début*
  écrire ("Donner la valeur de A et B")
  lire (`A`, `B`)

  `C ← A`
  `A ← B`
  `B ← C`

  écrire ("la valeur de A est:", `A`)
  écrire ("la valeur de B est:", `B`)

*Fin*
Exercice 3 :
1)

*Algorithme* : PGCD euclide  
*Variables* : N₁, N₂, reste : Entier  

*Début*  
  écrire ("Donner nombres N₁ et N₂")  
  lire (N₁, N₂)  
  Tant que N₂ ≠ 0 Faire  
    reste ← N₁ mod N₂  
    N₁ ← N₂  
    N₂ ← reste  
  Fin tant que  
  écrire ("le PGCD est :", N₁)  

*Fin*
2)
Algorithme PGCD d'Euclide*

*fonction PGCD*
Début
  Si N₂ = 0 alors
    retourne N₁
  sinon
    retourne PGCD(N₂, N₁ mod N₂)
  Fin
Fin

*Variables A, B, résultat: Entier*
Début
  écrire ("entrer nombre A et B.")
  lire (A, B)
  résultat ← PGCD(A, B)
  écrire ("le PGCD est:", résultat)
Fin
3)
PGCD (Euclide) Valeur des nombres (N) O(\log N) Logarithmique (Très rapide)
Exercice 4 :
1)

*Algorithme: les diviseurs de n*
*Variables:* `n`, `b`: Entier
*Début*
  écrire ("Entrer un entier n:")
  lire (n)
  Pour `b` de 1 à `n` faire
    Si `n mod b = 0` alors
      écrire (`b`)
    Fin Si
  Fin Pour
*Fin*
*Complexité:* O(n

2)

*Algorithme: les diviseurs de n*
*Variables:* `n`, `d`: Entier
*Début*
  écrire ("Entrer un entier n:")
  lire (n)
  Pour `d` de 1 à racine carrée(n) faire
    Si `n mod d = 0` alors
      écrire (`d`)
      Si `d ≠ n/d` alors
        écrire (`n/d`)
      Fin Si
    Fin Si
  Fin Pour
*Fin*
*Complexité:* O(√n)

3)

Analyse comparative

- La *1ère méthode* est plus simple à comprendre.
- La *2ème méthode* est nettement plus efficace pour les grands nombres, car elle réduit le nombre de tests nécessaires tout en garantissant que tous les diviseurs sont trouvés.
- Exercice 5 :

Algorithme: Jeu de devinette

*Variables:*
- `n`: Entier (le nombre secret)
- `essai`: Entier (nombre de tentatives)
- `reponse`: Entier (saisie de l’utilisateur)
- `rejouer`: Caractère (réponse de l’utilisateur pour rejouer)

*Début*
   *répéter*
    `n ← aleatoire(1, 100)`
    `essai ← 0`
     *répéter*
      écrire("Devinez le nombre entre 1 et 100:")
      lire(`reponse`)
      `essai ← essai + 1`
       *Si* `reponse = n` *alors*
        écrire("Félicitations! Vous avez trouvé le nombre.")
         *quitter la boucle*
       *sinon si* `reponse> n` *alors*
        écrire("Trop grand.")
       *sinon*
        écrire("Trop petit.")
       *Fin Si*
     *jusqu’à* `essai = 5` *ou* `reponse = n`
     *Si* `reponse ≠ n` *alors*
      écrire("Désolé, le nombre était:", n)
     *Fin Si*
    écrire("Voulez-vous rejouer? (oui/non)")
    lire(`rejouer`)
   *jusqu’à* `rejouer ≠ "oui"`
*Fin*
Exercice 6 :

Algorithme: Triangle de Floyd

*Variables:*
- `n`, `i`, `j`, `val`: Entiers

*Début*
  écrire("Entrez le nombre de lignes n:")
  lire(n)
  `val ← 1`
  Pour `i` de 1 à `n` faire
    Pour `j` de 1 à `i` faire
      écrire(`val`, " ")
      `val ← val + 1`
    Fin Pour
    écrire()  // saut de ligne
  Fin Pour
*Fin*

---
Complexité de l’algorithme

- Le nombre total d’éléments affichés est: `1 + 2 + 3 +... + n = n(n+1)/2`
- *Complexité:* O(n²)
  Car le nombre d’opérations croît quadratiquement avec le nombre de lignes .
Exercice 7 :

 Algorithme avec boucle

*Variables:* `n`, `i`, `somme`: Entiers
*Début*
  écrire("Entrez un entier n:")
  lire(n)
  `somme ← 0`
  Pour `i` de 1 à `n` faire
    `somme ← somme + i`
  Fin Pour
  écrire("La somme est:", somme)
*Fin*

*Complexité:* O(n)
→ On effectue n additions.


Algorithme avec fonction récursive

*Fonction somme(n):*
  Si `n = 0` alors
    retourne 0
  Sinon
    retourne `n + somme(n - 1)`
  Fin Si

*Programme principal:*
  écrire("Entrez un entier n:")
  lire(n)
  écrire("La somme est:", somme(n))

*Complexité:* O(n)
→ n appels récursifs, donc même complexité que la version avec boucle.

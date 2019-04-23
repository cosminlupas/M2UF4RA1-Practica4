# Cosmin Mihai Lupas

## 1 – Realitza les següents consultes

### 1) Obtenir el nom de totes les assignatures classificades per ordre alfabètic
SELECT Nom 
FROM Assignatura 
ORDER BY Nom;
### 2) 
   #### a) Obtenir les ciutats dels alumnes majors de 18 anys
   SELECT Ciutat 
   FROM Alumne 
   WHERE Edat > 18;
   #### b) El mateix però sense tuples (registres) repetides
   SELECT DISTINCT Ciutat 
   FROM A lumne 
   WHERE Edat >= 18;
### 3) Extreure totes les dades de l'assignatura amb nom 'LABOSOFT'
SELECT * 
FROM Assignatura 
WHERE Nom LIKE "LABOSOFT";
### 4) Obtenir els noms i l'edat dels alumnes que són de Lleida per ordre alfabètic (segons el camp nom).
SELECT Nom, Edat 
FROM Alumne 
WHERE Ciutat LIKE Lleida 
ORDER BY Nom
### 5) Si fem la següent consulta ens dona error, perquè?
   #### SELECT nom, numalumnes FROM assignatura ORDER BY 3;
   
### 6) Obtenir el llistat de tots els alumnes majors d’edat (igual o major que de 18 anys), classificant-los per la ciutat d'origen en ordre creixent i per la seva edat en ordre decreixent dins dels de la mateixa ciutat.

### 7) El mateix però volem que enlloc de nom, ens surti IDENTITAT, i enlloc de ciutat que ens surti ORIGEN.

### 8) Suposem ara que volem saber el nom, l’edat i l’any de naixement de cada alumne. Ordeneu la sortida per l'any de naixement en ordre decreixent.

### 9) Trobeu les assignatures que tenen com a mínim 20 alumnes menys que 'EDI'. Ordeneu el resultat alfabèticament per nom de l'assignatura

### 10) Suposem ara que inserim el següent alumne 
#### (Observeu que el camp edat no s'omple, per tant tindrà valor nul):
#### INSERT INTO Alumne (nom, ciutat) VALUES('Pere', 'Tremp');
#### a) Trobar el nom dels alumnes que no tenen edat. Ordeneu el resultat pel camp nom.
#### b) Trobeu ara els noms dels alumnes que si que tenen edat

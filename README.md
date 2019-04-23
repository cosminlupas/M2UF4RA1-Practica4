# Cosmin Mihai Lupas

## 1 – Realitza les següents consultes

### 1) Obtenir el nom de totes les assignatures classificades per ordre alfabètic
SELECT Nom  <br/>
FROM Assignatura <br/>
ORDER BY Nom;<br/>

### 2) 
   #### a) Obtenir les ciutats dels alumnes majors de 18 anys
   SELECT Ciutat <br/>
   FROM Alumne <br/>
   WHERE Edat > 18;<br/>
   
   #### b) El mateix però sense tuples (registres) repetides
   SELECT DISTINCT Ciutat <br/>
   FROM A lumne <br/>
   WHERE Edat >= 18;<br/>
   
### 3) Extreure totes les dades de l'assignatura amb nom 'LABOSOFT'
SELECT * <br/>
FROM Assignatura <br/>
WHERE Nom LIKE "LABOSOFT";<br/>

### 4) Obtenir els noms i l'edat dels alumnes que són de Lleida per ordre alfabètic (segons el camp nom).
SELECT Nom, Edat <br/>
FROM Alumne <br/>
WHERE Ciutat LIKE Lleida <br/>
ORDER BY Nom<br/>

### 5) Si fem la següent consulta ens dona error, perquè?
   #### SELECT nom, numalumnes FROM assignatura ORDER BY 3;
Perque el ORDER BY dona error perque 3 no es ningun nom de columna i no fa res  <br/>

### 6) Obtenir el llistat de tots els alumnes majors d’edat (igual o major que de 18 anys), classificant-los per la ciutat d'origen en ordre creixent i per la seva edat en ordre decreixent dins dels de la mateixa ciutat.
SELECT * <br/>
FROM Alumne <br/>
WHERE edat >= 18 <br/>
ORDER BY  Ciutat ASC, edat DESC;<br/>

### 7) El mateix però volem que enlloc de nom, ens surti IDENTITAT, i enlloc de ciutat que ens surti ORIGEN.
SELECT Nom AS Identitat, Ciutat AS Origen <br/>
FROM Alumne <br/>
WHERE Edat >= 18 <br/>
ORDER BY Ciutat ASC, Edat Desc <br/>
### 8) Suposem ara que volem saber el nom, l’edat i l’any de naixement de cada alumne. Ordeneu la sortida per l'any de naixement en ordre decreixent.
SELECT Nom, Edat, (EXTRACT(YEAR FROM CURRENT_DATE)-Edat) AS Any_Naixement <br/>
FROM Alumne <br/>
ORDER BY AnyNaixement Desc <br/>
### 9) Trobeu les assignatures que tenen com a mínim 20 alumnes menys que 'EDI'. Ordeneu el resultat alfabèticament per nom de l'assignatura

### 10) Suposem ara que inserim el següent alumne 
#### (Observeu que el camp edat no s'omple, per tant tindrà valor nul):
#### INSERT INTO Alumne (nom, ciutat) VALUES('Pere', 'Tremp');
#### a) Trobar el nom dels alumnes que no tenen edat. Ordeneu el resultat pel camp nom.
#### b) Trobeu ara els noms dels alumnes que si que tenen edat

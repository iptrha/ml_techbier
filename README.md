# Machine Learning Tutorial

## Disclaimer
Das ist alles nur geklaut von [Pieter Buteneers (@pieterbuteneers) und Bart De Vylder von CoScale
](https://github.com/pbutenee/ml-tutorial)

## Installation


1. Download & Install [Anaconda mit Python 2.7](https://www.continuum.io/downloads) 
2. Git auschecken:
	* ````git clone https://github.com/iptrha/ml_techbier.git ```` oder 
	* [Zip-Datei](https://github.com/iptrha/ml_techbier/archive/master.zip) runterladen
3. In Techbier Ordner wechseln: ````cd ml_techbier````

4. iPython ausführen: ````ipython notebook machine_learning_aufgaben.ipynb````
5. Browser sollte starten...

## Verwendung
Nachdem das Browserfenster gestartet ist, kann man den Workshop durcharbeiten. Auf die Python-Codezeilen kann man einfach mit der Maus draufklicken und dann Shift-Enter drücken. Dann wird der Python Code ausgeführt.

Die Teile des Codes die folgenden Code beinhalten müssen implementiert werden und die Exception auskommentiert werden:

````python
##### Implement this part of the code #####
raise NotImplementedError()
# plt.scatter( ? , ? )
````

zu:

````python
##### Implement this part of the code #####
# raise NotImplementedError()
plt.scatter( total_page_views , cpu_usage )
````

## Python help
Gaaaaanz einfache Python Hilfe von Jemandem, der auch keine Ahnung hat.

### np.reshape

np.reshape (#rows, #cols) hilft, eine Matrix umzuformen.
Wir gehen davon aus, dass eine Matrix aus Reihen und Kolonnen besteht. Z.B. 3 Reihen, 2 Kolonnen:

````python
A = array([[0, 1],
       [2, 3],
       [4, 5]])
````
Mit np.reshape können wir das Array umformen. Z.B. so dass es 3 Kolonnen sind statt 2

````python
B = A.reshape (2, 3)

array([[0, 1, 2],
       [3, 4, 5]])
````

Wenn man eine Dimension nicht weiss oder angeben möchte, kann man den Wert ````-1```` einsetzen

````python
C = B.reshape (-1, 6)

array([[0, 1, 2, 3, 4, 5]])
````


### np.ones

Dieser einfache Befehl erstellt einfach eine Matrix in den gewünschten Dimensionen, die aus 1en besteht.

````python
D = np.ones ((5, 3))

array([[ 1.,  1.,  1.],
       [ 1.,  1.,  1.],
       [ 1.,  1.,  1.],
       [ 1.,  1.,  1.],
       [ 1.,  1.,  1.]])
````

### np.mean
Fast zu kompliziert für mich. 

Man berechnet den Durchschnitt einer Matrix. 

* Ohne Achse einfach Durchschnitt aller Werte
* Achse 0 = Durchschnitt der Kolonnen
* Achse 1 = Durchschnitt der Reihen

````python
>>> a = np.array([[1, 2], [3, 4]])
>>> np.mean(a)
2.5
>>> np.mean(a, axis=0)
array([ 2.,  3.])
>>> np.mean(a, axis=1)
array([ 1.5,  3.5])
````

### np.argmin

Ogottogott. 

Gibt den Index (0-based) des kleinsten Wertes eines Arrays oder einer Matrix an. Das ganze Achsen-Gedöns von oben gilt auch hier.

````python
>>> a = array([[0, 1, 2],
       		[3, 4, 5]])
       
>>> np.argmin(a)
0
>>> np.argmin(a, axis=0)
array([0, 0, 0])
>>> np.argmin(a, axis=1)
array([0, 0])
````

Die Ästhetik eines 0-based Indexes hat mir auch noch niemand erklären können. Das erste Kind ist ja nicht das nullte Kind. "Es ist das erste Kind, aber es hat Index 0"... Oder wie?

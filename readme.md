Try outs for PRA2

**Descripció del dataset. Perquè és important i quina pregunta/problema pretén
respondre?**

Hem utilitzat el dataset "Titanic: Machine Learning from Disaster", disponible a https://www.kaggle.com/c/titanic

Aquest famós joc de dades conté informació sobre els passatgers que viatjaven al Titanic quan es va enfonsar, el 15 d'Abril del 1912. Les variables incloses en el joc de dades són:

**Variable	Definició**
survival 	Va sobreviure 	0 = No, 1 = Yes
pclass 	Classe de bitllet 	1 = 1st, 2 = 2nd, 3 = 3rd
sex 	Gènere 	
Age 	Edat, en anys 	
sibsp 	# de german(e)s / marit/muller viatjant al Titanic 	
parch 	# of pares / fills viatjant al Titanic 	
ticket 	Número de bitllet 	
fare 	Preu del bitllet 	
cabin 	Número de cabina	
embarked 	Port d'embarcament 	C = Cherbourg, Q = Queenstown, S = Southampton


A la pàgina de Kaggle, com que el dataset es presenta com a material de base per a un exercici de machine learning, es divideix el datatset en un grup 'train' i un grup 'test'. La idea és utilitzar el grup 'train' per elaborar un model que pugui predir la supervivència dels passatgers del grup 'test'.

A nosaltres, en canvi, ens interessa aquest dataset per fer un estudi d'interès sociològic/històric, en el qual no ens centrem en l'accident del Titanic ni en els índex de supervivència, sinó que aprofitem la informació del dataset per aprofundir sobre factors demogràfics i econòmics que ens ajudin a construir una imatge del moviment migratori envers els EUA a principis del segle XX. En aquest sentit doncs, (utilitzarem el joc de dades complet, ajuntant els grups 'train' i 'test', i descartant la variable 'survival')(?), i plantejarem preguntes com: viatjar era més car pels homes que per les dones? Els preus dels bitllets es definien tenint en compte l'edat del passatger? Viatjaven més nens a tercera classe que a primera? Viatjaven més homes joves a tercera classe?   




Els fitxers continguts en aquest repositori són:  

* age_imputation.rmd --> Conté els scripts d'imputació dels valors nuls (missing) de la variable Age així com de la variable Embarked. També conté una primera exploració de valors extrems (outliers).  
* viz_ages.rmd --> Conté les visualitzacions que donarien suport a l'estratègia d'imputació que plantegem per a la variable 'Age' al script anterior.  


**ANÀLISIS ESTADÍSTICS (PROPOSTA):  

Anàlisis inferencials a partir d'una mostra de les dades, el subconjunt de train publicat a la plataforma kaggle.  

* Prova 1: Comparació de dues variables numèriques  
           Comparació de les mitjanes de preu de bitllet segons el sexe: una variable numèrica en dos grups independents. Test d'hipòtesi de dues mostres sobre les mitjanes.  
           H0 --> la mitjana de preu (a primera classe) és la mateixa per homes i dones  
           H1 --> la mitjana és diferent ( o unilateral = els bitllets per homes són més cars)  
           Alternativa unilateral:  
           H0 --> la mitjana del preu dels bitllets (a primera classe) és més alta per a homes que per a dones  

* Prova 2: Correlació entre dues variables numèriques  
           Ens plantegem si hi ha relació lineal entre les variables Age i Fare. A priori creiem que no, però farem la prova per a sortir de dubtes.  
           
* Prova 3: Comparació de dues variables categòriques  
           Realització d'un test chi-squared sobre les variables Embarked i Survived  
           
* Prova 4: Comparació d'una variable numèrica i una de categòrica  
           Comparació de la proporció d'infants entre classes. Test d'hipòtesis de dues mostres sobre la proporció.  
           H0 --> la proporció d'infants a primera classe i a tercera és la mateixa.  
           
* Prova 5: Comparació d'una variable numèrica i una de categòrica (segona proposta)  
           Test estadístic entre les variables 'Age' i 'PClass'  
           H0 --> la mitjana d'edat de passatgers de 1a classe i 3a classe és la mateixa.  
           Proposem ANOVA o t-Student com a proves paramètriques (amb alternatives no paramètriques respectives en cas que fos necessari)  

Anàlisis estadístics per a determinar la normalitat:  
* QQ-plot  
* Kolmogorov-Smirnov  
* Shapiro-Wilk  

Anàlisis estadístics per a determinar homocedasticitat:  
* Levene  
* Fligner-Killeen  
* (funció var.test de R)  

Try outs for PRA2

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

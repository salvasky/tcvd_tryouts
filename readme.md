Try outs for PRA2


**ANÀLISIS ESTADÍSTICS (PROPOSTA):

Anàlisis inferencials a partir d'una mostra de les dades, el subconjunt de train publicat a la plataforma kaggle.  

* Prova 1: Comparació de dues variables numèriques (edats?)  
           P.ex. Mitjana d'edat dels menors de 12 anys supervivents, separats en nens i nenes  
           H0 --> Els menors de 12 anys sobreviuen igual independentment del seu gènere  

* Prova 2: Comparació de dues variables categòriques --> Port embarcament + Survival (?)  
           P.ex. Morts segons el port d'embarcament  
           H0 --> El punt d'origen d'un passatger no té influència per a determinar que no es salvarà  
           
* Prova 3: Comparació d'una variable numèrica i una de categòrica --> mitjana d'edat per classe (?)  
           P.ex. Mitjana d'edat dels passatgers per classe  
           H0 --> A primera classe viatgen més famílies riques, per tant hi ha més infants que a segona o tercera classe.  

Anàlisis estadístics per a determinar la normalitat:  
* QQ-plot  
* Kolmogorov-Smirnov  
* Shapiro-Wilk  

Anàlisis estadístics per a determinar homocedasticitat:  
* Levene  
* Fligner-Killeen  
* (funció var.test de R)  

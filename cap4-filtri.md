Filtri audio
====

---

##### Introduzione

La forma più semplice di elaborazione audio è il filtraggio, e con i filtri è possibile fare molte cose interessanti con i segnali audio. In questo capitolo, esploreremo cosa sono i filtri, cosa fanno e forniremo alcuni esempi di filtri relativamente semplici. Quelli che comunemente chiamiamo filtri sono, tecnicamente, filtri lineari e invarianti nel tempo. Lineare significa che i filtri obbediscono a proprietà associate alla linearità dei sistemi, mentre invariante nel tempo implica che i filtri non cambiano nel tempo, il che ci consente di analizzarli più facilmente e di comprenderli indipendentemente dal tempo. Esistono anche filtri non invarianti nel tempo, di cui vedremo alcuni esempi sotto forma di effetti audio.

I filtri digitali si presentano sotto forma di equazioni alle differenze, che nella forma che tratteremo qui, sono somme di versioni ritardate dell’ingresso. Ognuna di queste versioni ritardate viene scalata da un numero reale chiamato coefficiente del filtro. È interessante notare che i filtri digitali sono molto più semplici dei loro equivalenti analogici. Mentre il risultato dei filtri digitali è determinato dalle equazioni alle differenze, il risultato dei filtri analogici dipende da equazioni differenziali e integrali. La matematica coinvolta nel secondo caso è dunque molto più complessa rispetto al primo. Inoltre, con i filtri digitali è possibile realizzare elaborazioni molto più complesse rispetto ai filtri analogici. Vi sono quindi vari motivi per preferire i filtri digitali rispetto a quelli analogici.
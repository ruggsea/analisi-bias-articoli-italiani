# Analisi bias titoli di articoli italiani - Parallasse/Scomodo

## Introduzione

Questa repo contiene dati e codice per analisi e visualizzazioni dei titoli di articoli italiani di tre testate giornalistiche: Repubblica, Corriere della Sera e Libero. L'analisi è stata condotta per la rubrica Parallasse, la rassegna stampa critica del 54 numero di [Scomodo](https://www.scomodo.org). 

## Contenuto

- `article_bias.ipynb`: questo notebook contiene il codice per analisi esplorativa dei titoli, tentativi di classificazione tramite LLM e draft di alcune visualizzazioni.
- `dspy_experiment.ipynb`: questo notebook contiene il codice per un ulteriore esperimento di classificazione utilizzando [DSPy](https://github.com/stanfordnlp/dspy), il framework di StanfordNLP che permette l'automizzazione del prompt engineering per ottimizzare task tramite LLM. 
- `accuracies.csv`: file csv contenente alcuni risultati preliminari di tentativi di classificazione, utilizzando vari combinazioni di tecniche (vari numeri di esempi per il fewshot learning, vari ripetizioni di ogni classificazione per plurility classification).
- `examples.json`: file json contenente 10 esempi per il fewshot learning, manualmente classificati e corredati di razionale per la classificazione, per permettere il Chain of Thought. 
- `test_articles.json`: file json contenente 47 titoli di articoli italiani manualmente classificati come dateset di benchmark per testare le performance del modello di classificazione. 

## Dettagli dei modelli

I modelli LLM utilizzati sono stati una quantizzazione di Mixtral MoE 8x7B in locale e GPT-3.5-turbo attraverso l'API di OpenAI.


# mode_of_transportation_notebooks

Notebooks usados para determinar los modos de transporte en la RM

- `EOD_Model_v3` : Contiene la construcción del modelo de regresión multinomial a partir de la encuesta Origen Destino
- `Flow_TSNMF_Model-mindist` : Contiene la iteración sobre TSNMF para obtener los flujos y la posterior inicial de los modos
- `Flow_LDA_Model` : Contiene una iteración usando LDA con priors usando [Tomotopy](https://bab2min.github.io/tomotopy/v0.7.0/en/#tomotopy.LDAModel.set_word_prior), esta iteración permite asociar las torres con los distintos modos, no así el flujo. Para correr NMF es necesario un paso previo que consistiría en armar una posterior.
- `NMF_reModel_W` : varías iteraciones de NMF sobre el resultado obtenido de `Flow_TSNMF_Model-mindist`. La matriz H inicial es el posterior, mientras que para la matriz W inicial se va usando la matriz W resultante de la iteración anterior.

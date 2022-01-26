# ClassifyingPropositions
Pipelines and models created for classification of propositions of fact, value, or policy

HOW TO USE MODELS:

FOR BERT + SCIKIT MODELS:

      Code for testimg Scikit models should be in this format:

      loaded_model = pickle.load(open('SVC_model.sav', 'rb'))
      result = loaded_model.score(dataset_features, dataset_labels)
      print(result)

FOR FINE TUNED BERT MODEL:

      Code for testing Scikit models should be in this format:
      
      from sklearn.metrics import classification_report
      model_predicted, _, _ = BERT_model.predict(eval_dataset)
      ypred = np.argmax(model_predicted, axis=1)
      print(classification_report(eval_labels, ypred))

TODO: Clean pipelines for external use

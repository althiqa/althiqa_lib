.. _Quickstart:

Quickstart
==========

Leveraging on althiqa's API, data scientists are empowered to craft simple and efficient AI reports. It boils down to four steps: login to your session, create your project, push your models and push your metrics.

1. Login to your session
------------------------

.. code-block:: python

    import althiqa_lib
    
    url = #the url to connect to the SaaS (given to you)
    email = #email you used to sign in
    pwd = #password you used to sign in
    sess = althiqa_lib.Session(url, email, pwd )
    
2. Create a project
-------------------
To create a project to althiqa's SaaS, you you can use :py:func:`create_project` method. 

Note that ``"X_train"`` and ``"X_test"`` should be passed as Pandas Dataframes. 

``"y_train"`` and ``"y_test"`` can either be numpy arrays or a list. 

``"project_type"`` has to be chosen between ``"reg"`` (for regression tasks) or ``"classif"`` (for classification tasks).

.. code-block:: python

    project = sess.create_project(project_name: str,
                               X_train: pd.DataFrame, 
                               y_train: list or np.array, 
                               X_test: pd.DataFrame, 
                               y_test list or np.array,
                               project_type: str)
                              
3. Push a model
---------------
Push a ML Model to althiqa's platform. 

For regression projects: the model_object should be an object with a predict() method.

For classification projects: the model_object should be an object with a predict_proba() model, and a threshold between 0 and 1 should be given as argument. 

.. code-block:: python

    project.push_model('model_name', model_object, threshold = None) #for classification
    project.push_model('model_name', model_object) #for regression
    
4. Push a custom metric
-----------------------
althiqa already provides a wide range of metrics that are computed by default when you push a new model to your project. Though, you can write your own custom metric and push it to your project. You will then be able to use it as one of the metric of interest for evaluation.

``"metric_name"`` is the name you give to your metric

``"metric_function"`` is the metric function that you have implemented. 

``"protected_attribute"`` is only required for fairness metrics.

``"description"`` is a high level description (str) that you can write and that will be displayed on the interface. Best practice is to keep it short. 

.. code-block:: python

    project.create_metric(metric_name: str, metric_function , protected_attribute = None, description = None, h_is_b = False )





Metrics repository
==================

Description
-----------

althiqa maintains a wide range of metrics that are available by default
in the trust radar. 

The relevance of a metric is use case dependant. Therefore, we assign a project type to those metrics to only display them when they make sense for a specific use case.

You can select or unselect any of those metrics using the UI directly.


Classification metrics
----------------------

.. autofunction:: default_metrics.f1_score
.. autofunction:: default_metrics.balanced_accuracy_adjusted
.. autofunction:: default_metrics.accuracy
.. autofunction:: default_metrics.roc_auc_score
.. autofunction:: default_metrics.expected_calibration_error
.. autofunction:: default_metrics.matthews_corr_coef
.. autofunction:: default_metrics.fpr
.. autofunction:: default_metrics.tpr
.. autofunction:: default_metrics.fnr
.. autofunction:: default_metrics.tnr
.. autofunction:: default_metrics.CO2_emission
.. autofunction:: default_metrics.inference_time
.. autofunction:: default_metrics.NetTrustScore
.. autofunction:: default_metrics.fairness_DI_demographic_parity


Regression metrics
------------------

.. autofunction:: default_metrics.r2
.. autofunction:: default_metrics.mean_absolute_error
.. autofunction:: default_metrics.mean_squared_error
.. autofunction:: default_metrics.CO2_emission_regression
.. autofunction:: default_metrics.inference_time_regression



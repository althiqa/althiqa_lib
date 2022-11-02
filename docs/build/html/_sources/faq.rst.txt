.. _faq:

Frequently Asked Questions
===========================

* **What is the trust radar and what kind of information dos it summarize?**
	The trust radar is althiqa's main functionality. It aims at summarizing information contained in a wide range of metrics in a geometrical way. When morre than one model is passed to the trust radar, althiqa then agregate all the metrics ranks of each models to produce a final ranking. If more than one metric is selected, the user can define importance weights for each metric and the ranking will be adjusted accordingly.

* **Where can I see how predefined metrics are computed?**
	You can look at the code for each predefined metrics in our `metric repo file <https://github.com/althiqa/althiqa_V0/blob/main/new_metrics.py>`_.

* **What if I want to change the way predefined metrics are computed ?**
    You are very welcome to do so. You can copy the code of the metric you want to change from our `metric repo file <https://github.com/althiqa/althiqa_V0/blob/main/new_metrics.py>`_. You can paste the code on your notebook, edit your changes and once you are done, give a new name to the resulting custom metric and push it with the API so it can be displayed and be ready to use in the interface.
    
* **How can I help?**
    We are actively releasing new functionalities that will complement the trust radar. If you find that a functionality you use to report or communicate ML information to your stakeholders is missing in the althiqa service, please `open an issue <https://github.com/althiqa/althiqa_V0/issues>`_ so that we can help on it. The API will evolve based on users' needs. 
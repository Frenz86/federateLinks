# Federate Learning Links
- [Breve tutorial Nvidia Flare client-server](https://www.youtube.com/watch?v=8x7oY3xAgek)
- [Nuove funzionalità con web UI di interazione](https://developer.nvidia.com/blog/federated-learning-from-simulation-to-production-with-nvidia-flare/)
- [NVIDIAFlare_on_AWS](https://www.youtube.com/watch?v=4Yz_A0X04j0)
- [FL_Prostate_Cancer_Histopathology_Paper](https://arxiv.org/pdf/2206.05617.pdf)
- [MONAI_ZOO_MODEL](https://developer.nvidia.com/blog/open-source-healthcare-ai-innovation-continues-to-expand-with-monai-1-0/)
- [Problema_armonizzazione_scannere_MRI](https://www.sciencedirect.com/science/article/abs/pii/S0730725X18306490)
- [cuCIM_Digital_Patology](https://developer.nvidia.com/blog/accelerating-digital-pathology-workflows-using-cucim-and-nvidia-gpudirect-storage/)


NVFLARE Release 2.2.1
FL Simulator -- A lightweight simulator of a running NVFLARE FL deployment. It allows researchers to test and debug their application without provisioning a real project. The FL jobs run on a server and multiple clients in the same process but in a similar way to how it would run in a real deployment. Researchers can quickly build out new components and jobs that can then be directly used in a real production deployment.

FLARE Dashboard NVFLARE's web UI. In its initial incarnation, the Flare Dashboard is used to help project setup, user registration, startup kits distribution and dynamic provisions. Dashboard setup and apis can be found here

Site-policy management -- Prior to NVFLARE 2.2, all policies (resource management, authorization and privacy protection, logging configurations) can only be defined by the Project Admin during provision time; and authorization policies are centrally enforced by the FL Server. NVFLARE 2.2 makes it possible for each site to define its own policies in the following areas:

Resource Management: the configuration of system resources that are solely the decisions of local IT.
Authorization Policy: local authorization policy that determines what a user can or cannot do on the local site. see related Federated Authorization
Privacy Policy: local policy that specifies what types of studies are allowed and how to add privacy protection to the learning results produced by the FL client on the local site.
Logging Configuration: each site can now define its own logging configuration for system generated log messages.
Federated XGBoost -- We developed federated XGBoost for data scientists to perform machine learning on tabular data with popular tree-based method. In this release, we provide several approaches for the horizontal federated XGBoost algorithms.

Histogram-based Collaboration -- leverages recently released (XGBoost 1.7.0) federated versions of open-source XGBoost histogram-based distributed training algorithms, achieving identical results as centralized training (trees trained on global data information).
Tree-based Collaboration -- individual trees are independently trained on each client's local data without aggregating the global sample gradient histogram information. Trained trees are collected and passed to the server / other clients for aggregation and further boosting rounds.
Federated Statistics -- built-in federated statistics operators that can generate global statistics based on local client side statistics. The results, for all features of all datasets at all sites as well as global aggregates, can be visualized via the visualization utility in the notebook.

MONAI Integration In 2.2 release, we provided two implementations by leveraging MONAI Bundle.

MONAI ClientAlgo Integration -- enable running MONAI bundles directly in a federated setting using NVFLARE
MONAI ClientAlgoStats Integration -- through NVFLARE Federated Statistics we can generate, compare and visualize all clients' data statistics generated from MONAI summary statistics

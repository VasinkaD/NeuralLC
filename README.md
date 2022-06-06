# Neural network modeling of polarization in liquid crystals

This repository provides data and supplementary material to the paper **Bidirectional deep learning of polarization transfer in liquid crystals with application to quantum state preparation**, [Physical Review Applied 17, 054042 (2022)](https://doi.org/10.1103/PhysRevApplied.17.054042), by Dominik Vašinka, Martin Bielak, Michal Neset, and Miroslav Ježek.

Direct_model.h5
- a file containing a deep neural network built in Keras library with Tensorflow backend
- the neural network coresponds to the direct model from section "Direct models and dataset-size scaling"

Compound_model.h5
- a file containing a deep neural network built in Keras library with Tensorflow backend
- the network coresponds to the compound model from section "Inverse and compound model"

Auxiliary_models folder
- contains neural networks for evaluating the Fig. 2 (c): Dependence on the number of trainable parameters 

Data_files folder
- contains files required by corresponding jupyter notebooks

Dataset_size_scaling.ipynb
- a Jupyter Notebook for reproducting the Fig. 2 (a): The infidelity dependence on the number of samples in the training set
- requires loading of the following files contained within "Data_files" folder:
    - DNN_all_fidelity_val_tensor_part_1.npy, DNN_all_fidelity_val_tensor_part_2.npy
    - DNN_all_fidelity_test_tensor_part_1.npy, DNN_all_fidelity_test_tensor_part_2.npy
    - LI_all_fidelity_val_tensor_part_1.npy, LI_all_fidelity_val_tensor_part_2.npy
    - LI_all_fidelity_test_tensor_part_1.npy, LI_all_fidelity_test_tensor_part_2.npy
    - RBF_all_fidelity_val_tensor_part_1.npy, RBF_all_fidelity_val_tensor_part_2.npy
    - RBF_all_fidelity_test_tensor_part_1.npy, RBF_all_fidelity_test_tensor_part_2.npy

Evaluation_of_DNN.ipynb
- a Jupyter Notebook for reproducing the infidelity results of direct and compound deep learning models
- requires loading of models "Direct_model.h5" and "Compound_model.h5", together with following files from "Data_files" folder:
    - training_voltages.npy, validation_voltages.npy, test_voltages.npy
    - training_rhos.npy, validation_rhos.npy, test_rhos.npy

Evaluation_of_interpolation_methods.ipynb
- a Jupyter Notebook for reproducing the infidelity results of linear and radial basis function interpolation models
- requires loading of the following files from "Data_files" folder:
    - training_voltages.npy, validation_voltages.npy, test_voltages.npy
    - training_rhos.npy, validation_rhos.npy, test_rhos.npy

Logo_projection.ipynb
- a Jupyter Notebook for reproducting the Fig. 5: Palacký University logos on the Bloch sphere
- requires loading of the "Compound_model.h5" file, together with the following files from "Data_files" folder:
    - logo_points_cartesian.npy
    - weak_signal_heralded_stokes.npy
    - entangled_state_density_matrix_MN.npy

All the files were prepared and tested with Python 3.9.6, Keras 2.4.3, and Tensorflow 2.5.0






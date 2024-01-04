# Detection of Alzheimer's Disease with Neuroimaging Data Using a Shallow 2D-CNN Architecture
Man Ho Wong  
School of Computer Science  
Georgia Institute of Technology. Atlanta, GA.

## Introduction
This project aims to build a deep learning model to detect Alzheimer's disease with cross-sectional MRI data (more than 86,000 MRI slice images) using 2D-convoluted neural networks (CNN). Normalization and regularization techniques were used to create a stable model with good generalization performance. Despite its shallow architecture, the preliminary model developed here (SCNN4) was able to achieve an accuracy of 99.9%, a significant improvement from the current deep learning models (Zhao et al., 2023). The training time at the moment is 18 minutes using a T4 GPU provided by Google Colab.

## Future work
Currently, the model is trained without considering class imbalance. In addition, images were split for training, validation and testing randomly without considering subject identity. The former issue may lead to a biased model (see the section "Exploring the dataset") and the latter may impact the model's generalization performance due to data leakage (Yagis et al., 2021). These issues will need to be addressed in the future. In terms of performance metrics, other metrics besides accuracy will be needed to assess the model more comprehensively, such as the model's prediction precision and generalization performance.

## Data sourcing
The training dataset was compiled by the [Open Access Series of Imaging Studies (OASIS)](https://www.oasis-brains.org/) (Marcus et al., 2007). The derived dataset was partially preprocessed by Ninad Aithal (Centre for Brain Research IISc - Bangalore, IN), including .nii to .jpg file conversion and patient classification (see [this page](https://www.kaggle.com/datasets/ninadaithal/imagesoasis/data) for more information).

## Acknowledgments
Data were provided by OASIS-1: Cross-Sectional: Principal Investigators: D. Marcus, R, Buckner, J, Csernansky J. Morris; P50 AG05681, P01 AG03991, P01 AG026276, R01 AG021910, P20 MH071616, U24 RR021382.

## References
Marcus, D.S., Wang, T.H., Parker, J., Csernansky, J.G., Morris, J.C., Buckner, R.L. (2007). Cross-Sectional MRI Data in Young, Middle Aged, Nondemented, and Demented Older Adults. Journal of Cognitive Neuroscience, 19, 1498-1507. https://doi.org/10.1162/jocn.2007.19.9.1498

Yagis, E., Atnafu, S.W., García Seco de Herrera, A., Marzi C., Scheda R., Giannelli M., Tessa C., Citi L. & Diciotti S. (2021). Effect of data leakage in brain MRI classification using 2D convolutional neural networks. Nature Science Report, 11, 22544. https://doi.org/10.1038/s41598-021-0168

Zhao, Z., Chuah, J. H., Lai, K. W., Chow, C. O., Gochoo, M., Dhanalakshmi, S., Wang, N., Bao, W., & Wu, X. (2023). Conventional machine learning and deep learning in Alzheimer's disease diagnosis using neuroimaging: A review. Frontiers in computational neuroscience, 17, 1038636. https://doi.org/10.3389/fncom.2023.1038636
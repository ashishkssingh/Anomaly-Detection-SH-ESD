# SH-ESD (Seasonal Hybrid Extreme Studentized Deviate) :

The primary algorithm, Seasonal Hybrid ESD (S-H-ESD), builds upon the Generalized ESD test for detecting anomalies. S-H-ESD can be used to detect both global and local anomalies.

This two step process allows SH-ESD to detect both global anomalies that extend beyond the expected seasonal minimum and maximum and local anomalies that would otherwise be masked by the seasonality.

This is achieved by employing time series decomposition and using robust statistical metrics, viz., median together with ESD. In addition, for long time series such as 6 months of minutely data, the algorithm employs piecewise approximation. 
This is rooted to the fact that trend extraction in the presence of anomalies is non-trivial for anomaly detection.

The figure below shows large global anomalies present in the raw data and the local (intra-day) anomalies that S-H-ESD exposes in the residual component via our statistically robust decomposition technique.

![screen shot 2019-02-06 at 2 51 08 pm](https://user-images.githubusercontent.com/15687230/52369402-ad83eb00-2a1e-11e9-895f-20e683b6ce86.png)

## Project involves developing an algorithm to remove noise from heart rate data collected from wrist sensors, in order to better estimate stress. 

**In collaboration with Northeastern University Health Behavior Informatics Lab** https://hbi.ccs.neu.edu/

## To download repository
- ```git clone https://github.com/tjeng/HRV_analysis.git``` 

## Background and Goals
Stress has devastating effects on health, resulting in headaches, stomach upset, high blood pressure, chest pains, heart problems, depression, and anxiety. Chronic, untreated stress, could eventually lead to lifetime emotional disorder, and such cases happen more than 50% of the time (https://www.webmd.com/balance/guide/causes-of-stress#2). Stress could be overcome by deep breathing techniques, which is often overlooked because stress occurs unconsciously. By making people aware of stress through vibration on wrist sensors and providing relaxation techniques, chronic stress could be reduced. However, heart rate signals from wrist sensors contain noise generated from everyday movement. To estimate stress accurately, noise needs to be removed, which is the focus of the project.

For full details, refer to the paper (Kos et al., 2017) https://ieeexplore.ieee.org/document/8037141

## Methods

### Data collection (referenced in data folder)

Data on interbeat intervals (also known as RR intervals), denoting time between successive heart beats, are collected from wrist sensors (Empathica 4, E4, and Microsoft Band 2, MB), and ECG, used as the gold standard to compare measurements, from 9 healthy participants. 

### Algorithm development (referenced in code folder)

1. Remove short interval and add it to the subsequent interval
2. Impute long interval based on moving average within a certain window size
3. Implement Singular Spectrum Analysis (SSA), a dimensional reduction technique, to smooth irregularities in heart rate signals and reconstruct function of heart rate over time

For full details, refer to the poster (Kos et al., 2017) https://www.researchgate.net/publication/320911791_The_Accuracy_of_Monitoring_Stress_from_Wearable_Devices_Background_and_Objective_References

## Evaluation & Conclusion

After implementing the data cleaning algorithm, the RR interval of data from wrist sensors was correlated with that of ECG. The cleaned data had 10% higher correlation with ECG than the raw data, indicating that the algorithm improves heart rate estimates by 10%.

## Future work

Future work would focus on stress detection algorithms based on cleaned heart rate signals. 


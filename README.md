# Minimal Counters, Maximum Insight: Simplifying System Performance with HPC Clusters for Optimized Monitoring

- PerformanceCounters_List.csv: List of all performance counters
- performance_counter_correlations_score.csv: Pearson Correlation scores of HPCs
- Dendogram.png: Dendogram formed using Ward's Method

### Mean Squared Error (Full Prediction)
![MSE Full](plots/mse_full_prediction.png)

### Mean Squared Error (Initial run-time Prediction)
![MSE Short](plots/mse_less_time.png)

### Bartlett Lake SPEC Predictions with Standard Deviation

Bartlett Lake configuration specifications:

- #Big-cores = 12
- #Small-cores = 0
- Cache Size = [18M,24M,30M]
- Frequency = [1.8GHz, 3.4GHz]
- Hyperthreading = [Enable, Disable]

In the Bartlett Lake setup, the number of cores could not be modified—it is fixed at 12 big-cores, and this version of the architecture does not support small cores. As a result, variations in SPEC ratios are somewhat limited. However, we were able to vary other configuration parameters, including cache sizes (18MB, 24MB, and 30MB), frequencies (1.8 GHz and 3.4 GHz), and hyper-threading (enabled and disabled). Despite the restricted core configuration, as shown in figure below, the standard deviation remains low across runs, especially for the Decision Tree model, which consistently makes accurate predictions. The Decision Tree model also showed the best prediction performance on the Alder Lake dataset. To capture standard deviation, we performed five runs for each configuration. 

![SPEC BartlettLake](plots/spec_bartlettlake_predictions.png)
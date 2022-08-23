# General: 

 > [Assignment PDF (Farsi)](https://github.com/WuedK/CS-SBU-MachineLearning-BSc-2022/blob/main/submits/98222036/project3/ML_Project3_2022.pdf)
 
 ## Abstract
  
   In this project, 4 different services are implemented and they can be tested using [Postman](https://www.postman.com/) or similar applications.
   The input and output format of the services' API is JSON and its documantation can be found [here](https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/swagger). There are also some input examples in the [app/input_outputs](https://github.com/WuedK/CS-SBU-MachineLearning-BSc-2022/tree/main/submits/98222036/project3/app/input_outputs) route.
   
   * Service 1: Time Series Interpolation Service
   
     This Service takes some Date-Time data (either in Chiristian(miladi) or Persian(shamsi) date-time format) along with some values. The sevice then useses interpolation methods to resample missing data. The interpolation can be done by one or more years, months, days, hours, minutes or seconds and the interpolation method can be either polynomial or spline with order of 1 or 2. Moreover, it can also skip interpolating data when the date is a weekend in Persian.
     
   * Service 2: Time Series Interpolation and Date Format Transformation from Christian(miladi) to Persian(shamsi) Service
   
     This service is almost the same as the first service. The only difference is that in this service, input dates are always in miladi format and the output dates are all in shamsi format
     
   * Service 3: Outlier Detection Service
   
     This service takes some data which can be time-series or not, and then it uses different outlier detection methods to predict whether a data is outlier or not. The output is a JSON consisting of 5 (if the data format is not time-series) or 3 (if the data is time-series) parts. One part is the id or the date-time and other parts are the results of applying different interpolation methods on the dataset. For instance, if the second element of the first part of the output(excluding the id) is false then the second element is not considered to be an outlier by the first outlier detection method.
     The methods used for the anomaly detection of time-series data are isolation forest and dbscan and the methods used for other data types are z-score, Local Outlier Factor(LOF), isolation forest and one class SVM.
     
# Routes:

 > Interpolation: https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/service1
 
 > Interpolation From Miladi To Shamsi: https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/service2
 
 > Outlier Detection: https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/service3
 
 > Imbalanced Data Management: https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/service4
 
 > [API Documentation](https://sbu-ml-project-3-service-arman-sbu-ml-cloud.fandogh.cloud/swagger)

# References:

 > https://blog.paperspace.com/outlier-detection-with-abod/
 
 > https://towardsdatascience.com/5-outlier-detection-methods-that-every-data-enthusiast-must-know-f917bf439210
 
 > https://www.analyticsvidhya.com/blog/2021/05/feature-engineering-how-to-detect-and-remove-outliers-with-python-code/
 
 > https://machinelearningmastery.com/model-based-outlier-detection-and-removal-in-python/
 
 > https://aditya-bhattacharya.net/2020/07/20/sales-and-demand-forecast-analysis/3/
 
 > https://neptune.ai/blog/anomaly-detection-in-time-series
 
# Note

 > [Input examples](https://github.com/WuedK/CS-SBU-MachineLearning-BSc-2022/tree/98222036/submits/98222036/project3/app/input_outputs)

 > polynomial interpolation of order 1 is as the same as linear interpolation

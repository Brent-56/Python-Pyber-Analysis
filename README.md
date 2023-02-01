# Python-Pyber-Analysis
### Overview

The purpose of this data analysis is to identify ride sharing metrics/trends based on city type. Once this is complete we will were tasked with creating a  representation of the total weekly fares and based on the city types. This representation will help improve accesibility to ride sharing services and determine ride affordability for each type by providing a clear picture as to what challenges people from different city types may be facing and what solutions we can implement to mitigate the challenges our customers are facing


- The first step in this process is to load and read all CSVs that will be involved in the analysis process. Here we read "city_data.csv" and "ride_data.csv". After I read each CSV into jupyter notebook I am sure to display it via head.() or simply by adding it into a cell and running it to ensure it was properly read/imported. 

![D6FF67D1-9019-44B9-BDD1-AEBFEC55AEA2](https://user-images.githubusercontent.com/112785655/216108777-1c6c70fc-f1a2-486c-90c7-a03115c79ab8.jpeg)
![14246BFA-D3C3-4ABA-9501-0D1BD69E4CBC](https://user-images.githubusercontent.com/112785655/216112824-8c84f108-939f-4e9c-89e0-ceb3ef2cb962.jpeg)

- For the next step I decided to merge both CSVs("city_data.csv", "ride_data.csv") on the "city" column as which is a column that both datasets have individually. This is similar to how we use joins in SQL. The finished table will be named pyber_data_df which is why we are setting it equal to the merged datase.

![91D21622-E864-4B99-94FC-743BB1320A3F](https://user-images.githubusercontent.com/112785655/216115044-320c746b-0f18-48d8-bc66-d1339ef4bb9e.jpeg)

- Next I began gathering metrics. The first metric is to discover the amount of rides per city type from January to April 2019. We can see the Rural city type has the least amount of total rides with 125 in 4 months. Secondly we display the number of drivers by city type. We can see the number of drivers for Rural cities is significantly less than that of Suburban and Urban city types. We then display the total amount of fares for each city type. Rural is significantly less than both Urban and Suburban once more. After this I calculate average price per ride for each city type. Rural is the most expensive as they have the least amount of available drivers and the least amount of fares. Finally we calculate the average fare per driver for eah city type and as estimated, Rural is still the highest average fare by driver price. 
![ED8E877E-49D5-4CB1-A128-34E685E803CA](https://user-images.githubusercontent.com/112785655/216137765-72a085ef-f8b2-442a-9c09-0d42313e14ed.jpeg)
![E24267AE-2CB0-4C50-90F6-4931F7F0EA06](https://user-images.githubusercontent.com/112785655/216138100-590f32c8-c944-46b0-8e2e-a462e23495bc.jpeg)

- Once I gathered everything it was important to put all of our findings in a central location so viewers could see everything quickly and be able to conclude metrics from the dataset efficiently. I did this by putting all the metrics into a dictionary and using a key word to identify each metric. After that we converted it into a dataframe and printed the results as:

![0F77DE09-CF56-4586-8648-1A9E94417AC2](https://user-images.githubusercontent.com/112785655/216139273-6e1dd90b-3e10-487b-a496-c1e5bb011689.jpeg)

- Next I decided to make the dataframe more presentable by deleting the index name which in this case was'type'. I ran "pyber_summary_df.index.name = None" to complete the task and ran "pyber_summary_df" in the cell afterwards to see if it did as I intended. With everything aligned I was successfully able to delete the index name and the ending result came out to:
![E91F1316-7FB6-45EC-AEDC-89D33AA234DF](https://user-images.githubusercontent.com/112785655/216140311-f0be85b2-de89-46a8-b72c-44d7415bea36.jpeg)


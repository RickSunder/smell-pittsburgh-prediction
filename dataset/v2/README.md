# smell-pittsburgh-dataset-v2

This is the second version of the Smell Pittsburgh dataset from 10/31/2016 (month/day/year) to 1/23/2022, including the following zipcodes in the Pittsburgh region in Pennsylvania, USA:

15006, 15007, 15014, 15015, 15017, 15018, 15020, 15024, 15025, 15028, 15030, 15031, 15032, 15034, 15035, 15037, 15044, 15045, 15046, 15047, 15049, 15051, 15056, 15064, 15065, 15071, 15075, 15076, 15082, 15084, 15086, 15088, 15090, 15091, 15095, 15096, 15101, 15102, 15104, 15106, 15108, 15110, 15112, 15116, 15120, 15122, 15123, 15126, 15127, 15129, 15131, 15132, 15133, 15134, 15135, 15136, 15137, 15139, 15140, 15142, 15143, 15144, 15145, 15146, 15147, 15148, 15201, 15202, 15203, 15204, 15205, 15206, 15207, 15208, 15209, 15210, 15211, 15212, 15213, 15214, 15215, 15216, 15217, 15218, 15219, 15220, 15221, 15222, 15223, 15224, 15225, 15226, 15227, 15228, 15229, 15230, 15231, 15232, 15233, 15234, 15235, 15236, 15237, 15238, 15239, 15240, 15241, 15242, 15243, 15244, 15250, 15251, 15252, 15253, 15254, 15255, 15257, 15258, 15259, 15260, 15261, 15262, 15264, 15265, 15267, 15268, 15270, 15272, 15274, 15275, 15276, 15277, 15278, 15279, 15281, 15282, 15283, 15286, 15289, 15290, 15295

This dataset is released under the Creative Commons Zero (CC0) license. Please feel free to use this dataset for your own research. If you found this dataset and the code useful, we would greatly appreciate it if you could cite our paper below.

Yen-Chia Hsu, Jennifer Cross, Paul Dille, Michael Tasota, Beatrice Dias, Randy Sargent, Ting-Hao (Kenneth) Huang, and Illah Nourbakhsh. 2020. Smell Pittsburgh: Engaging Community Citizen Science for Air Quality. ACM Transactions on Interactive Intelligent Systems. 10, 4, Article 32. DOI:https://doi.org/10.1145/3369397. Preprint:https://arxiv.org/pdf/1912.11936.pdf.

A similar previous version [v1 dataset](/dataset/v1) (with a smaller number of zipcodes and time range) was used for the data analysis in the above paper. This version v2 dataset has not been analyzed and remains an open challenge.

Below are descriptions about what each column means in the file that contains smell reports (the "smell_raw.csv"):
- EpochTime: the Epoch timestamp when the smell is experienced
- skewed_latitude: the skewed latitude of the location where the smell is experienced 
- skewed_longitude: the skewed longitude of the location where the smell is experienced
- smell_value: the self-reported rating of the smell (described on the [Smell Pittsburgh website](https://smellpgh.org/how_it_works)) 
- smell_description: the self-reported description of the smell (e.g., woodsmoke)
- feelings_symptoms: the self-reported symptoms that may caused by the source of the smell (e.g., eye irritation)
- additional_comments: the self-provided comment to the agency that receives the smell report
- zipcode: the zipcode of the location where the smell is experienced

Information about the metadata (e.g., latitude, longitude, feed ID, channel name) of the sensor monitoring stations used in this dataset (all files in the "esdr_raw" folder) can be found on the [ESDR data visualization page](https://environmentaldata.org/#time=1642345888.849,1642950688.849&cursor=1642730480.675&plotHeight=5.000&plotAreaHeight=40.000&showFilters=true&showSettings=true&showResults=true&center=40.445982705178,-79.96401491796037&zoom=12). ESDR means the [Environmental Sensor Data Repository](https://esdr.cmucreatelab.org/), a service for hosting environmental data. The feed ID and the channel name in the [code for gettting the sensor data](/py/prediction/getData.py) corresponds to the metadata on the visualization page.

## Important
- The Lawrenceville ACHD sensor (Feed ID 26) does not have PM2.5 data since the end of year 2020, which means that file "esdr_raw/Feed_26_Lawrenceville_ACHD.csv" has a lot of missing data on year 2021 and 2022.
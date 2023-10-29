# Component Failure Prediction using sensor data

# Problem Statement :

**Dataset : Sensor Data in CSV form of batche's**

**Problem statement :**

The system in focus is the Air Pressure system (APS) which generates pressurized air that are utilized in various functions in a truck, such as braking and gear changes. The datasets positive class corresponds to component failures for a specific component of the APS system. The negative class corresponds to trucks with failures for components not related to the APS system.

The problem is to reduce the cost due to unnecessary repairs. So it is required to minimize the false predictions.

|True class | Positive | Negative | | | ----------- | ----------- | | | |Predicted class||| | | Positive | - | cost_1 | | | Negative | cost_2 | | |

Cost 1 = 10 and Cost 2 = 500

The total cost of a prediction model the sum of Cost_1 multiplied by the number of Instances with type 1 failure and Cost_2 with the number of instances with type 2 failure, resulting in a Total_cost. In this case Cost_1 refers to the cost that an unnessecary check needs to be done by an mechanic at an workshop, while Cost_2 refer to the cost of missing a faulty truck, which may cause a breakdown.

Total_cost = Cost_1 * No_Instances + Cost_2 * No_Instances.

From the above problem statement we could observe that, we have to reduce false positives and false negatives. More importantly we have to reduce false negatives, since cost incurred due to false negative is 50 times higher than the false positives.

Challenges and other objectives
Need to Handle many Null values in almost all columns
No low-latency requirement.
Interpretability is not important.
misclassification leads the unecessary repair costs.



### Step 1 - Install the requirements

```bash
pip install -r requirements.txt
```

### Step 2 - Run main.py file

```bash
python main.py
```


This is changes made in IDE 


Git commands

If you are starting a project and you want to use git in your project
```
git init
```
Note: This is going to initalize git in your source code.


OR

You can clone exiting github repo
```
git clone <github_url>
```
Note: Clone/ Downlaod github  repo in your system


Add your changes made in file to git stagging are
```
git add file_name
```
Note: You can given file_name to add specific file or use "." to add everything to staging are


Create commits
```
git commit -m "message"
```

```
git push origin main
```
Note: origin--> contains url to your github repo
main--> is your branch name 

To push your changes forcefully.
```
git push origin main -f
```


To pull  changes from github repo
```
git pull origin main
```
Note: origin--> contains url to your github repo
main--> is your branch name


.env file has
```
MONGO_DB_URL="mongodb://localhost:270XXXXXXXXXX"
AWS_ACCESS_KEY_ID="XXXXXXXXXXXXXXXXXXXXXXXXXXXX"
AWS_SECRET_ACCESS_KEY="XXXXXXXXXXXXXXXXXXXXXXXX"
```
Note: Setup MongoDB Connection By Adding your ip in Network Access and grant access
add your ip by adding 
```
0.0.0.0/0
```
connect to database with string
```
mongodb+srv://username:<password>@cluster0.lllhm4w.mongodb.net/
```

**Data Collection Architecture :**


![data collection](https://github.com/sohel-jagirdar/sensors/assets/52422511/7956a22a-b6ca-4f83-90da-2bce29a6e971)


**Project Architecture :**


![project arch](https://github.com/sohel-jagirdar/sensors/assets/52422511/ade4e6a2-d5bb-4f6a-b8fe-f9092ea1a91f)


**Deployment Architecture :**


![deplyement arch](https://github.com/sohel-jagirdar/sensors/assets/52422511/12646343-5d3f-4022-abc1-ea6555a6a3ec)

**Airflow Training Pipeline and Retraining Trigger :**


![airflow result](https://github.com/sohel-jagirdar/sensors/assets/52422511/ce8c2669-6b23-4f27-8e51-c4f42c0cb589)


**Airflow Batch Prediction Pipeline :**


![airflow prediction](https://github.com/sohel-jagirdar/sensors/assets/52422511/628faff2-6097-4fe0-92cf-c61b2d3b28a0)

**Amazon S3 Bucket ( Artifact, Saved Models, Input files for Prediction, Prediction Result) :**


![S3 Results](https://github.com/sohel-jagirdar/sensors/assets/52422511/51727716-2f88-49f6-9705-3b4cd7be4f63)



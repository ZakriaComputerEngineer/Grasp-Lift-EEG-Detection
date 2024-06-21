# Grasp-Lift-EEG-Detection

An EEG grasp and lift solution using a Random Forest algorithm involves analyzing brainwave data (EEG signals) to predict hand movements such as grasping and lifting objects. The Random Forest, a machine learning model, is trained on features extracted from EEG data to recognize patterns corresponding to these specific motor actions. By aggregating the predictions from multiple decision trees, the Random Forest can accurately classify the intent to grasp or lift, enabling responsive control for applications like prosthetics or brain-computer interfaces.

Link to test data generated results:https://drive.google.com/file/d/1LWJq_9S3MxkiQo1wXrrt8zgZaoQX_uXu/view?usp=drive_link

Statistical Analysis
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/96949125-a163-41f9-8b4c-a7ddb22e7b6f)
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/eb3fb7bd-3a07-490f-91bc-18d510675d85)

Feature evaluation
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/f174dee3-a985-4b0d-a8a9-fb7c1733f05b)

Feature selection
The following features are selected which showed most relation to the selected events I chose to predict.
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/a875f00f-28e8-49b5-b2b4-c10a6038b064)

Event Selection
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/9b2aea34-c17d-411e-8eec-84120fb6facd)

Moving AVG
Moving average is being taken to normalize the sharp changes which is a recommended approach of preprocessing on large dataset like this.
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/b1eb5062-bf7d-4d45-9697-3e465c1d9376)

Train Validation Split
Training is done on 95% of the data present in the train folder and 5% for evaluate model’s performance because data of events happening isn’t available in the testing folder!
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/98779535-e550-49d4-8475-323ae1aded1c)

 Model selection
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/b83965a1-2792-4cca-a621-ee64ba6f1f27)
 Although I selected these models for training but due to the intensive training time and load on my pc I wasn’t able to train the SVM and Gradient Boosting classifier models!

 Model Training
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/c9bb8e20-e07e-4b67-b3b7-2d44067ca587)
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/9ee89bbb-396f-4573-8194-a0a1b7752d42)

 Model Size
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/9579b8a6-b083-41b6-9588-670417aa05bd)

 Evaluation
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/10d655c9-f0e8-4a13-a2ed-bf2268666ce0)
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/7f38e69a-2856-4af0-b088-ce3830dab457)
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/7f3a2baa-44fd-4fb1-b4af-f201d8f358c1)

 Generating the results from test folder
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/ca0ebc92-4dab-42dc-b7ac-dbea23304a72)
 ![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/638ea9fe-e338-4216-8713-51657aa005a7)

 Results that are generated are threshold and set to 1/0, all the test results are saved in the results file.
Here are first few rows of Results.csv

Event 1 = HandStart
Event 1 = FirstDigitTouch
Event 1 = BothStartLoadPhase

id              	event1	event2	event3
subj10_series10_0  	0      	0      	1
subj10_series10_1	  0      	0      	1
subj10_series10_2	  0      	1      	0
subj10_series10_3	  0      	1      	0
subj10_series10_4	  1      	0  	    0
subj10_series10_5	  0      	1      	0
.
.
.

Testing one input

INPUT
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/b6bae3ab-d482-42cd-b0c8-6908e83906f1)
OUTPUT
![image](https://github.com/ZakriaComputerEngineer/Grasp-Lift-EEG-Detection/assets/150436890/5fa290ec-bb45-4c85-81b7-6cecb901ecc5)




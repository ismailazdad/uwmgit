# uwmgit
UW-Madison GI Tract Image Segmentation

This repo contain code for the kaggle competition https://www.kaggle.com/competitions/uw-madison-gi-tract-image-segmentation

resume : i developp training based to microsoft coco json file datatset

![image](https://user-images.githubusercontent.com/74118071/172184249-5e3ad74a-c631-46e1-9490-a2ff9abed9e5.png)

In 2019, an estimated 5 million people were diagnosed with a cancer of the gastro-intestinal tract worldwide. Of these patients, about half are eligible for radiation therapy, usually delivered over 10-15 minutes a day for 1-6 weeks. Radiation oncologists try to deliver high doses of radiation using X-ray beams pointed to tumors while avoiding the stomach and intestines. With newer technology such as integrated magnetic resonance imaging and linear accelerator systems, also known as MR-Linacs, oncologists are able to visualize the daily position of the tumor and intestines, which can vary day to day. In these scans, radiation oncologists must manually outline the position of the stomach and intestines in order to adjust the direction of the x-ray beams to increase the dose delivery to the tumor and avoid the stomach and intestines. This is a time-consuming and labor intensive process that can prolong treatments from 15 minutes a day to an hour a day, which can be difficult for patients to tolerate—unless deep learning could help automate the segmentation process. A method to segment the stomach and intestines would make treatments much faster and would allow more patients to get more effective treatment.

The UW-Madison Carbone Cancer Center is a pioneer in MR-Linac based radiotherapy, and has treated patients with MRI guided radiotherapy based on their daily anatomy since 2015. UW-Madison has generously agreed to support this project which provides anonymized MRIs of patients treated at the UW-Madison Carbone Cancer Center. The University of Wisconsin-Madison is a public land-grant research university in Madison, Wisconsin. The Wisconsin Idea is the university's pledge to the state, the nation, and the world that their endeavors will benefit all citizens.

In this competition, you’ll create a model to automatically segment the stomach and intestines on MRI scans. The MRI scans are from actual cancer patients who had 1-5 MRI scans on separate days during their radiation treatment. You'll base your algorithm on a dataset of these scans to come up with creative deep learning solutions that will help cancer patients get better care.


In this competition we are segmenting organs cells in images. The training annotations are provided as RLE-encoded masks, and the images are in 16-bit grayscale PNG format.

Each case in this competition is represented by multiple sets of scan slices (each set is identified by the day the scan took place). Some cases are split by time (early days are in train, later days are in test) while some cases are split by case - the entirety of the case is in train or test. The goal of this competition is to be able to generalize to both partially and wholly unseen cases.

Note that, in this case, the test set is entirely unseen. It is roughly 50 cases, with a varying number of days and slices, as seen in the training set.

How does an entirely hidden test set work?
The test set in this competition is only available when your code is submitted. The sample_submission.csv provided in the public set is an empty placeholder that shows the required submission format; you should perform your modeling, cross-validation, etc., using the training set, and write code to process a non-empty sample submission. It will contain rows with id, class and predicted columns as described in the Evaluation page.

When you submit your notebook, your code will be run against the non-hidden test set, which has the same folder format (<case>/<case_day>/<scans>) as the training data.

  
![image](https://user-images.githubusercontent.com/74118071/172184479-6292a3c5-f15c-400e-9e3e-89ff3193e42b.png)
  
Example inference :
  
  
  ![image](https://user-images.githubusercontent.com/74118071/172619374-4551c1f0-f7ca-4589-8523-f31b41653596.png)

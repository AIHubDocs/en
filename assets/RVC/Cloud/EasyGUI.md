---
icon: chevron-right
order: 5000
visibility: private
---
``Last update: Mar 4, 2024`` 
‎  

***
## Introduction :icon-book:
***
- The EasyGUI Colab is a port of the custom layout of <u>[Mainline]()</u> made by <u>[Rejekts](https://ko-fi.com/rejekts)</u>, named as the Colab.

- Its strongest points are its active maintenance & that it holds the simplicity of Mainline.

- The Colab offers two ways to use it, with or without the UI. The latter being available **only** for Pro tier users.        
‎         
#### Pros & Cons :icon-tasklist:
==- *Learn more*
!!! *The pros & cons are subjective to your necessities.*        
!!! 
||| ✔️ **PROS** 
- Very complete
- Active maintenance          
- UI version
- Feature to save model to HF
||| ❌ **CONS** 
- Has less features    
- No <u>[Mangio-Crepe</u>](https://aihubdocs.github.io/en/rvc/resources/inference-settings/#pitch-extraction-algorithm) 
- Manual model upload
- Usage limit for free users
||| 
===
###### ‎
***

## Setting Up :icon-download:
***
###### ‎
#### 1. Prepare dataset
- Open your Google Drive storage, make a new folder & place your dataset in it.

    <img src="..\easygui-img\2-dataset.png" alt="image" width="300">

*** 
###### ‎
#### 2. Enter the Colab
a. Access the Colab space <u>[here](https://colab.research.google.com/drive/1r4IRL0UA7JEoZ0ZK8PKfMyTIBHKpyhcw#scrollTo=Sb5fzhzEXK8X)</u>.      
b. Then **Log in** to your Google account.
***
###### ‎
#### 3. Set up Colab
- Execute the **INSTALL RVC** cell & grant all the permissions requiered.

    <img src="..\easygui-img\2-install.png" alt="image" width="500">‎    
‎
- When it finishes the cell will look like this.    
‎       
<img src="..\easygui-img\2-doneinstall.png" alt="image" width="500">

###### ‎

***
## Training :icon-rocket:
***
==- **STEP 1** 
###### ‎
##### a. Model name
###### ‎
- Insert a name for your model. Don't include spaces/special characters.        
‎   
    <img src="..\easygui-img\3-modelname.png" alt="image" width="500">‎  
***
###### ‎
##### b. Dataset folder
###### ‎
i. Click the folder on the left ( :icon-file-directory-fill: ).         
    For mobile users: tap the three lines on the top left & `Show file browser`.      
‎   
ii. Go to **drive**, right-click your dataset **folder** & click `Copy path`.    
‎       
    <img src="..\easygui-img\3-dataset.png" alt="image" width="350">‎       
‎       
‎   
iii. Paste the path in the **dataset_folder** bar. Then run the **STEP 1** cell.        
‎   
    <img src="..\easygui-img\3-step1.png" alt="image" width="420">‎  

===

=== **STEP 2**
###### ‎
##### a. f0method
###### ‎
‎ ‎ ‎ ‎ <img src="..\easygui-img\3-step2.png" alt="image" width="390">‎   
‎       
i. Select the **RMVPE_GPU** <u>[algorithm](https://aihubdocs.github.io/en/rvc/resources/inference-settings/#pitch-extraction-algorithm)</u>.     
    Only use that one, as PM & Harvest are obsolete, and normal RMVPE is slower in this case.     
‎   
ii. Then run the cell.      



===

=== **STEP 3**
###### ‎
##### a. Train index
###### ‎
i. Run the **STEP 3** to generate the <u>[.INDEX](https://aihubdocs.github.io/en/essentials/voice-models/#voice-model-files)</u> of the model.

ii. Open the file explorer & go to RVC, logs, and in your model's folder locate the INDEX named **added_** & download it.

<img src="..\easygui-img\3-indexdl.png" alt="image" width="390">‎   
‎ 
===

=== **FINAL STEP**

===

- step 1 will take around 4 minutes
***
## Inference :icon-unmute:
***
***
## Troubleshooting :icon-tools:
***
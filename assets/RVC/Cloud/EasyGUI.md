---
icon: chevron-right
order: 5000
visibility: private
---
``Last update: Mar 6, 2024`` 
‎  

***
:::content-center
## Introduction
:::

- The EasyGUI Colab is a port of the custom layout of <u>[Mainline](https://aihubdocs.github.io/en/rvc/local/mainline/)</u> made by <u>[Rejekts](https://ko-fi.com/rejekts)</u>, named as the Colab.

- Its strongest points are its active maintenance & that it holds the simplicity of Mainline.

- The Colab offers two ways to use it, with or without the UI. The first one being ideal for newbies.        
‎         
#### Pros & Cons
==- *Learn more*
!!! *The pros & cons are subjective to your necessities.*        
!!! 
||| ✔️ **PROS** 
- Active maintenance          
- UI version
- Automatic model upload
- Feature to save model to HF
||| ❌ **CONS** 
- Has less features    
- No <u>[Mangio-Crepe</u>](https://aihubdocs.github.io/en/rvc/resources/inference-settings/#pitch-extraction-algorithm) 
- Usage limit for free users
||| 
===
###### ‎

***
:::content-center
## Setting Up
‎    
:   ‎

:::

#### 1. Prepare dataset (optional)
- If you're going to train models, go to Google Drive & make a new folder with your dataset in it.

    <img src="..\easygui-img\dataset.png" alt="image" width="300">

*** 
###### ‎
#### 2. Enter the Colab
a. Access the Colab space <u>[here](https://colab.research.google.com/drive/1r4IRL0UA7JEoZ0ZK8PKfMyTIBHKpyhcw#scrollTo=Sb5fzhzEXK8X)</u>.  

b. Then **Log in** to your Google account.
***
###### ‎
#### 3. Set up Colab
- Tick `save_to_drive`, execute the **INSTALL RVC** cell & grant all the permissions requiered.       

    <img src="..\easygui-img\2-installrvc.png" alt="image" width="300">‎    
‎
- When it finishes the cell will look like this.    
‎       
<img src="..\easygui-img\2-installdone.png" alt="image" width="220">‎    


***
###### ‎
#### 4. Open UI (optional)
a. Run **Open the easyGUI**.

    <img src="..\easygui-img\2-openui.png" alt="image" width="320">‎    
‎     
- If you are going to train models, first ensure **load_models_from_drive** & **open_tensorboard** are ticked.

b. Then open the **public url**.

    <img src="..\easygui-img\2-publicurl.png" alt="image" width="530">‎    
‎    
!!!warning Don't close Colab until you're done using EasyGUI, or it will stop working.
!!!     

***
:::content-center
## With UI
:::
‎    
:   ‎    

### Inference 

#### 1. Download model
a. Go to the **Download Model** tab & paste the <u>[model link](https://aihubdocs.github.io/en/essentials/voice-models/#how-to-search-voice-models)</u> in the upper bar.

    <img src="..\easygui-img\ui-i-modellink.png" alt="image" width="450">‎      
‎   
b. In **Name your model** insert a name for it. Don't include spaces/special characters.        
Then press ``Download``.

    <img src="..\easygui-img\ui-i-namemodel.png" alt="image" width="520">‎ 

***
###### ‎
#### 2. Select model
a. Return to the **Model Inference** tab & click `Refresh voice list and index path`.

b. Then select the model in **Inferencing voice**. 

    <img src="..\easygui-img\ui-i-refreshselect.png" alt="image" width="620">‎ 

***
###### ‎
#### 3. Input vocals
a. Click the upload box & select your vocals. Or simply drag & drop.

    <img src="..\easygui-img\ui-i-uploadaudio.png" alt="image" width="320">‎        
‎    
b. Once it's done uploading, click `Refresh` again.
***
###### ‎  
#### 4. Modify settings (optional)
- If you wish, modify the [inference settings](https://aihubdocs.github.io/en/rvc/resources/artifacting/) for better results. Unfold the **General settings** menu to see more.

- The **Index Rate** is in the **Auto-detect index path** bar, and **Pitch** is on the right of `Refresh`.

***
#### 5. Convert
a. Begin processing by clicking the `Convert` button on top.

b. Once done, you'll be able to hear the results in the **Export audio** box. To download it, click the 3 dots on the right & `Download`.

    <img src="..\easygui-img\ui-i-output.png" alt="image" width="590">‎ 

***
###### ‎
### Training :icon-rocket:

>**For newbies:** if a setting isn't mentioned, leave it untouched.

###### ‎
#### 1. Name the model
a. Go to the **Train** tab. 

b. First set a name for your model in **Enter the experiment name**.

    <img src="..\easygui-img\ui-t-name.png" alt="image" width="520">‎   
‎       
- Don't include spaces/special characters, to avoid errors.
***
###### ‎
#### 2. Target sample rate
- Select your dataset's <u>[sample rate](https://aihubdocs.github.io/en/rvc/resources/sample-rate--formats/#sample-rate)</u>.

    <img src="..\easygui-img\ui-t-samplerate.png" alt="image" width="300">‎ 

***
###### ‎
#### 3. Select dataset

a. Press the upload box & select your dataset. Or simply drag & drop. 

    <img src="..\easygui-img\ui-t-inputds.png" alt="image" width="500">‎    
‎   
b. Once it's done uploading, press **Process Data**. It'll finish when the logs say ``end preprocess``. 

    <img src="..\easygui-img\ui-t-endpreprocess.png" alt="image" width="500">‎ 

***
###### ‎
#### 4. Feature extraction
- Press `Feature extraction`

***
###### ‎    
#### 5. Total training epochs
- Input the total amount of <u>[epochs](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/)</u> (training cycles) for the model.

- But since we'll use <u>[TensorBoard](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/#tensorboard)</u>, use an arbitrarily large value like `1000`

    <img src="..\easygui-img\ui-t-epochs.png" alt="image" width="420">‎

***
###### ‎
#### 6. Save frequency
- Rate at which the model will be saved, based on the <u>[epochs](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/)</u>. The saved models are known as the "checkpoints".    

- If you are a newbie, leave it at `15`.  

    <img src="..\easygui-img\ui-t-saverate.png" alt="image" width="570">‎     
‎   
- E.g: with a value of ``10``, it will be saved after the epoch 10, 20, 30, etc.   

***
###### ‎
#### 7. Batch size
- If you are a newbie, use `8`. But if your dataset is short (around 2 minutes or less), use `4`.

    <img src="..\easygui-img\ui-t-gpu.png" alt="image" width="590">‎  

***
###### ‎
#### 8. Cache (optional)
- For a faster training, set **Cache all training sets to GPU memory** as ``Yes``, if your dataset is less 10 minutes.

    <img src="..\easygui-img\ui-t-cache.png" alt="image" width="590">‎  


***
###### ‎
#### 9. Train INDEX
- Press ``Train feature index`` to get the model's [.INDEX](https://aihubdocs.github.io/en/essentials/voice-models/#-index) file.

***
## Without UI
***

###### ‎
***
### Inference :icon-unmute:
***
#### 1. Input model
- Depending on your device, the process of inputting the model varies.

    +++ :icon-device-desktop: ‎ DESKTOP
    a. Upload the model to Google Drive.    
    ‎   
    <img src="..\easygui-img\4-modelfolder.png" alt="image" width="350">‎   
    ‎   
    b. Click the folder symbol ( icon-file-directory ) & go to **drive -> MyDrive**.
    
        <img src="..\easygui-img\4-pthgd.png" alt="image" width="260">‎     
    ‎   
    c. Drag & drop the .PTH to the folder **RVC -> assets -> weights**.       
    ‎   
    <img src="..\easygui-img\4-weights.png" alt="image" width="270">‎  
    ‎  
    d. In **model_name** input the name of the PTH followed by `.pth`.      
    ‎   
    <img src="..\easygui-img\4-modelname.png" alt="image" width="320">‎  
    +++ :icon-device-mobile: MOBILE
    a. Upload the model's INDEX to Google Drive.
    +++
***
###### ‎
#### 2. Upload INDEX
a. Open the file explorer, open **MyDrive**, right-click the INDEX & click **Copy path**.

    <img src="..\easygui-img\4-index.png" alt="image" width="400">‎     
‎   
b. Then paste it in the **index_path** bar.

    <img src="..\easygui-img\4-indexpath.png" alt="image" width="550">‎  
***
###### ‎
#### 3. Input vocals
a. Upload the vocals to GD & copy the path.

    <img src="..\easygui-img\4-audio.png" alt="image" width="380">‎     
‎   
b. Paste it in the **input_path** & **output_path** bars.       

   <img src="..\easygui-img\4-inputoutput.png" alt="image" width="430">‎      

***
###### ‎
#### 4. Modify settings (optional)
- Modify the <u>[inference settings](https://aihubdocs.github.io/en/rvc/resources/inference-settings/)</u> for better results if you wish.


***
###### ‎
#### 5. Convert
a. Run the cell to begin processing the audio. 

b. Once done, a playable audio will 


### Training :icon-rocket:
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

==- **STEP 2**
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

==- **STEP 3**
###### ‎
##### a. Train index
###### ‎
i. Run the **STEP 3** to generate the <u>[.INDEX](https://aihubdocs.github.io/en/essentials/voice-models/#voice-model-files)</u> of the model.

ii. To download it, open the file explorer & go to RVC, logs, and in your model's folder right-click the INDEX named **added_** & press `Download`.

<img src="..\easygui-img\3-indexdl.png" alt="image" width="390">‎   

===

=== **FINAL STEP**
##### a. Model name
- The name you assigned the model previously.

##### b. Save frequency
- Rate at which the model will be saved, based on the <u>[epochs](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/)</u>. The saved models are known as the "checkpoints".

- If you are a newbie, leave it at `15`.      

- **E.g:** with a value of ``10``, it will be saved after the epoch 10, 20, 30, etc.   

##### c. Epochs
- Total amount of <u>[epochs](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/)</u> for the model.
- But since we'll use <u>[TensorBoard](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/#tensorboard)</u>, use an arbitrarily large number like ``2000``.

##### d. Batch size
- If you are a newbie, leave it at `8`. If your dataset is smaller (around 2 minutes or less) use `4` instead.

##### e. Start training
i. Begin training by running said cell. All the training files will be stored in your GD storage, so 

ii. <u>[TB](https://aihubdocs.github.io/en/rvc/resources/epochs-overtraining--tensorboard/#tensorboard)</u> will open in a momment. Remember to monitor it, as well as the cell's logs just in case.     

    The latter will show you errors if they happen, and information about the epochs & checkpoints.   

    <img src="..\easygui-img\3-logs.png" alt="image" width="500">‎   
‎   

!!!warning While training, you might get disconnected if you:    
- <u>[Stay AFK](https://rentry.org/colab_workarounds)</u> for a long time.     
- Disconnect from your Internet.       
- Don't solve the captchas that (might) pop up occasionally.    
- Run out of <u>[GPU runtime](http://aihubdocs.github.io/en/extra/glossary/#google-colab)</u>. 
!!!

- If the session ends due to exhausting GPU runtime, don't worry, if you followed the [Setting Up]() procedure, all the training files will be stored in your GD storage.

- Once the GPU runtime refills, begin the [retraining]() procedure.
===


***
## Troubleshooting :icon-tools:
***
---
icon: chevron-right
---

``Last update: Feb 28, 2024``  

***
###### ‎
:::content-center
## Introduction :icon-book:
:::     
- A vocal isolation app is a software designed to extract a person's vocals from an audio file, usually through the use of AI models.

- They can remove undesired noises, like background noise, reverb, echo, music, etc.    

- The goal is to get an audio sample with clean vocals, which is what RVC needs to give the most accurate & quality results.

- For RVC users, the best app is Ultimate Vocal Remover 5 (or **UVR**). It can be used either <u>[locally](https://aihubdocs.github.io/en/extra/glossary/#local-running)</u> or through the <u>[cloud](https://aihubdocs.github.io/en/extra/glossary/#cloud-based)</u>. 
***
<img src="../uvrmvsep-img/3.jpg" alt="image" width="" height="auto">‎       

###### ‎ 
:::content-center
## Local UVR :icon-device-desktop:
:::
***
:::content-center
###### ‎ 
### <u>Installation</u> :icon-download: 
!!!warning 
*You'll require great specs & GPU to run it effectively. Otherwise, use the <u>[cloud version](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#cloud-version--)</u>.*
!!!
:::
###### ‎ 
1. Go to their <u>[official website</u>](https://ultimatevocalremover.com/) & press `Download UVR`. 

    <img src="../uvrmvsep-img/1.jpg" alt="image" width="" height="auto">   

***
###### ‎ 
2. It will redirect you their GitHub page. Click the download link for your **operating system**.   
UVR is available both on **Windows & Mac**.
***
###### ‎ 
3. Once the installer finishes downloading, execute it & follow the instructions.     
Make sure to tick `🗹 Create a desktop shortcut` for an easier access to UVR.

    <img src="../uvrmvsep-img/2.jpg" alt="image" width="500" height="auto"> 
***
###### ‎       
###### ‎     
:::content-center
### <u>How to Use</u> :icon-checklist:  
!!!success
*If you an issue arises, be sure read the <u>[Troubleshooting](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#troubleshooting--)</u> chapter.*
!!!
:::
###### ‎       
==- *Extracting Vocals From Songs 🎶*
‎        
#### 1. Input audio.        
###### ‎  
- Click `Select input` to select your audio/s. Or just drag the files to it.  
‎   
- In `Select output` you can define the folder for the results.      

    <img src="../uvrmvsep-img/4.jpg" alt="image" width="300" height="auto">         ‎    

!!!success 
For better results, have the audio in a <u>[lossless format](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/)</u> (**WAV** or **FLAC**), & not MP3.
!!!
***
‎ 
#### 2. Select FLAC & GPU Conversion.
###### ‎  
a. At the right you can select the output format.       
We recommend picking `FLAC`. Learn why <u>[here](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/)</u>.   
‎  
b. If your GPU is **compatible with <u>[CUDA](https://aihubdocs.github.io/en/extra/glossary/#cuda)</u>**, toggle `GPU Conversion` on for a faster process.    

    <img src="../uvrmvsep-img/16.png" alt="image" width="350" height="auto">‎      

###### ‎       
>This step is not mandatory, but recommended for better results.
***
‎
#### 3. Extract vocals. 
###### ‎  
a. In **CHOOSE PROCESS METHOD** select `MDX-Net`, and select the `MDX23C` model.   

    <img src="../uvrmvsep-img/5.jpg" alt="image" width="250" height="auto">‎      
###### ‎  
###### ‎    
b. Now click the long `Start Processing` button.    
###### ‎  
!!!success 
<u>**TIP:**</u> To **test** models/options more efficiently, tick `Sample Mode` to only process 30 seconds of your sample.
!!!   
***
‎
#### 4. Clean vocals. 
###### ‎    
- Usually songs include reverb & backing vocals. These **negatively** impact the results in RVC. 

- So if the output has any undesired noises, follow the procedure on **Cleaning Vocals**.
===

=== *Cleaning Vocals 🗣️*

‎      
#### 1. Input audio.
###### ‎      
- Click `Select input` to input the vocals. Or just drag the files to it.  
‎   
- In `Select output` you can define the folder for the results.    

    <img src="../uvrmvsep-img/4.jpg" alt="image" width="300" height="auto">         ‎    

!!!success 
For better results, have the audio in a [lossless format](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/)</u> (**WAV** or **FLAC**), & not MP3.
!!!
***
‎   
#### 2. Select FLAC & GPU Conversion.
###### ‎      
a. At the right you can select the output format.       
We recommend picking `FLAC`. Learn why <u>[here](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/)</u>.     
‎   
b. If your GPU is **compatible with <u>[CUDA](https://aihubdocs.github.io/en/extra/glossary/#cuda)</u>**, toggle `GPU Conversion` on for a faster process.    
    ‎       
        <img src="../uvrmvsep-img/16.png" alt="image" width="350" height="auto">‎      
###### ‎       
>This step is not mandatory, but recommended for better results.
***
‎   
#### 3. Select model.  
###### ‎      
a. In **Process Method** select `VR`.     
‎   
b. Set **Window Size** to ``320``. (optional)        
Lower Window Size yield a higher output **quality**, but will take **longer** to process.   
‎   
b. Check the <u>[model list](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#uvrs-best-models-)</u>. In **Select VR Model** pick the one according to what you need to remove.         
‎       
If you need to remove multiple noises, follow this pipeline for the best results:   
``Remove reverb -> Extract main vocals -> Remove noise``  
###### ‎  
!!!success 
<u>**TIP:**</u> To **test** models/options more efficiently, tick `Sample Mode` to only process 30 seconds of your sample.
!!!  
***
‎  
#### 4. Process.
###### ‎      
Click the `Start processing` button at the bottom. And that will be all. 

***

:::content-center
[!button variant="danger" size="m" corners="pill" icon="heart-fill" iconAlign="right" text="Support UVR"](https://www.buymeacoffee.com/uvr5)
:::     
###### ‎  
===

###### ‎       
###### ‎     

:::content-center
### <u>Troubleshooting</u> :icon-tools:
:::
###### ‎ 
==- *The model isn't there.*
###### ‎ 
- Click the wrench (🔧) on the left & go to `Download Center`
- Select the category of the model (MDX-NET or VR)
- Unfold its dropdown & select the model that you need
- Then click the download button (📥). The model will download, which will take a few minutes
===

==- *UVR extracted too little/too much.*
###### ‎
- Modify the `Aggression Setting` value on the right. 
- This determines the **depth** of the extraction. Only the **VR** method has it.
- A higher value will deepen the extraction, and a lower one will soften it.
- Each audio is different, so you'll have to test the ideal value.
===

==- *I can't remove some of the backing vocals.*
###### ‎
- Run the audio through MDX23C or DeNoise. Modify the <u>[Aggression Setting](http://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#uvr-extracted-too-little-too-much)</u> if necessary.
===

###### ‎ 
###### ‎ 
###### ‎ 
:::content-center
## Cloud UVR :icon-cloud:

###### ‎ 

### <u>Setting Up</u> :icon-download: 
###### ‎
:::

1. First log in to your Google account <u>[here](https://accounts.google.com/)</u>.
***
2. Then access the Colab space <u>[here](https://colab.research.google.com/github/Eddycrack864/Ultimate-Vocal-Remover-5.6-for-Google-Colab/blob/main/Ultimate_Vocal_Remover_5_6_for_Google_Colab.ipynb)</u>. Credits to <u>[Eddy](https://github.com/Eddycrack864)</u> for the Colab.
***
3. Execute the `Install` cell. UVR will start loading & will take between 5 to 10 minutes.

    <img src="../uvrmvsep-img/18.png" alt="image" width="270" height="auto">‎   
‎   
- It'll finish when it says `Installation Completed`.

    <img src="../uvrmvsep-img/19.png" alt="image" width="270" height="auto">‎   
***
4. Then below, execute the `WebUI` cell. This will take around 3 minutes.
***For advanced users***, tick `VIP_MODELS` if you wish to use them.
***
5. Open the **public URL**. That **Gradio** link contains the UVR app.

    <img src="../uvrmvsep-img/20.png" alt="image" width="425" height="auto">‎  
***
!!!warning <U>IMPORTANT NOTES:</u>
Don't close the Colab tab until you're done using UVR, and don't press buttons continuously too quickly, as it may cause errors.   
As it's a port to <u>[Google Colab](https://aihubdocs.github.io/en/extra/glossary/#google-colab)</u>, switch accounts if you run out of the usage time.       
!!!
***
###### ‎  
###### ‎  
:::content-center
### <u>How to Use</u> ‎ :icon-checklist:
!!!
*If you come across a problem, read the <u>Troubleshooting</u> chapter.*
!!!
:::
###### ‎  
==- *Extracting Vocals From Songs* 🎶
###### ‎  
#### 1. Extract Vocals
###### ‎ 
a. Tap the `Input Audio` box & select your audio, or simply drag the file into it.      
‎       
    <img src="../uvrmvsep-img/21.png" alt="image" width="425" height="auto">‎       
‎       
‎       
b. Once it's done uploading, in **CHOOSE PROCESS METHOD** select ``MDX-NET``, and select the ``Voc_FT`` model.      
    Then click START PROCESSING.      

    <img src="../uvrmvsep-img/25.png" alt="image" width="530" height="auto">‎       
‎           
‎    
c. After a moment, the audios of the vocals & instrumental will appear on the output boxes below.        
To download them, click the three dots on their right & `Download`.

***
###### ‎  
#### 2. Remove Reverb
###### ‎ 
- Usually songs include reverb in the vocals. Reverb **negatively** impacts the results in RVC, so be sure to remove it.
‎       
a. Input the vocals & select the `VR Arc` **Process Method**. Use the ``UVR-DeEcho-DeReverb`` model.        
‎        
    <img src="../uvrmvsep-img/22.png" alt="image" width="540" height="auto">‎   
‎       
‎       
b. Tick `GPU Conversion` & ``No Reverb Only``, and set **WINDOWS SIZE** as `320`. Then Start Processing.     
Lower Window Size yield a higher output **quality**, but will take **longer** to process.       
‎       
    <img src="../uvrmvsep-img/23.png" alt="image" width="320" height="auto">‎   
‎   
‎   
c. Download the output.         
***    
!!!success
<u>**TIP:**</u> To **test** models/options more efficiently, tick `Sample Mode` to only process 30 seconds of your sample.
!!!  
***
###### ‎  
#### 3. Extract Lead Vocals
###### ‎ 
- Just like reverb, songs also normally include backing vocals, that affect the results in RVC.     
       
a. Input the vocals with no reverb & choose the ``UVR-BVE`` model.          
‎   
    <img src="../uvrmvsep-img/24.png" alt="image" width="320" height="auto">‎   
‎       
‎    
b. Ensure `Vocals Only` isn't ticked, if you wish to keep the backing vocals. Then Start Processing.        
‎   
If you then notice some noise, run the output through the ``UVR-DeNoise`` model (not the "lite" one). 
***
!!!warning For the best results, follow the pipeline explained before:       
Extract vocals -> Remove reverb -> Extract main vocals -> Remove noise
!!!  
===

==- *Only Cleaning* 🗣️ 
###### ‎  
#### 1. Select Vocals & Options
###### ‎  
a. Tap the `Input Audio` box & select your audio, or simply drag the file into it.     
‎        
    <img src="../uvrmvsep-img/21.png" alt="image" width="425" height="auto">‎           
‎       
‎       
b. Once it's done uploading, in **CHOOSE PROCESS METHOD**, select ``VR Arc``.       
‎   
<img src="../uvrmvsep-img/22.png" alt="image" width="600" height="auto">‎       
‎       
‎       
c. On the left, tick `GPU Conversion` & set **WINDOWS SIZE** to `320`.       
Lower Window Size yield a higher output **quality**, but will take **longer** to process.       
*** 

###### ‎ 
#### 2. Select Model
###### ‎  
d. Check the <u>[model list](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#uvrs-best-models-)</u> & in `CHOOSE VR MODEL` pick the one according to what you need to remove.    
‎       
If you need to remove multiple noises, follow this pipeline for the best results:   
``Remove reverb -> Extract main vocals -> Remove noise``  
***
###### ‎  
#### 3. Start Processing
###### ‎  
a. Click the orange **Start Processing** button. Wait a moment for your audio to process.       
‎       
b. Playable audios will then appear in the output boxes below. To download the output, click the three dots on the right and `Download`.            
‎       
If you're extracting lead vocals, remember to download the backing ones if you wish to keep them.    
***
!!!success 
<u>**TIP:**</u> To **test** models/options more efficiently, tick `Sample Mode` to only process 30 seconds of your sample.
!!!  

===
###### ‎  
###### ‎  
:::content-center
### <u>Troubleshooting</u> :icon-tools:
:::
###### ‎
==- *UVR extracted too little/too much.*
###### ‎
- Modify the `Aggression Setting` value on the right. 
- This determines the depth of the extraction. Only the VR method has it.
- A higher value will deepen the extraction, and a lower one will soften it.
- Each audio is different, so you'll have to test the ideal value.
===

==- *I can't remove some of the backing vocals.*
- Run the audio through MDX23C or DeNoise. Modify the Aggression Setting if necessary.
===

==- *I get a red error message.*
- This is normal. Try repeating your action.
- If it persists, reload the Gradio page.
===

***

###### ‎
###### ‎ 

:::content-center 
‎   
<img src="../uvrmvsep-img/8.png" alt="image" width="400" height="auto">

###### ‎       
## MVSEP
:::
###### ‎      

### Important Notes ‎ :icon-alert:
- MVSEP is a website for isolating vocals, that works similarly as UVR.

- The <u>[UVR Colab](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#cloud-version--)</u> is much faster & convenient for this task. Use MVSEP as a last resort.     

- For free users, you can't convert audios in batches or longer than 10 minutes. If that's your case, trim it into two pieces.
***
###### ‎  
### How to Use ‎ :icon-checklist:
!!!
*If you come across an issue, be sure to read the ***Troubleshooting*** chapter.*
!!!

==- *Extracting & Cleaning Vocals From <u>Songs</u>* 🎶
###### ‎     
#### 1. Log in.  
###### ‎
a. First, make an account <u>[here</u>](https://mvsep.com/register).        
‎       
b. Once logged in, go to the <u>[main page</u>](https://mvsep.com).     

!!!
Logging in is not mandatory, but recommended for **shorter waiting lists**.
!!!
***
###### ‎
#### 2. Select audio.   
###### ‎
a. Click `Browse File` & select your audio. The audio will begin to upload. (or just drag the file into it)    

    
    <img src="../uvrmvsep-img/9.png" alt="image" width="330" height="auto">‎   
    
***
###### ‎
#### 3. Extract vocals.
###### ‎
a. In `Separation type` select `MDX23C`     
‎     
b. In `Output encoding` select `FLAC`.          
We recommend selecting FLAC from now on. Learn more <u>[here</u>](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/).        
‎     
c. Once the audio is done uploading, click `Separate`       

    <img src="../uvrmvsep-img/11.png" alt="image" width="400" height="auto">‎   

!!! Leave "Model Type" untouched.
!!!
***
###### ‎
#### 4. Download output.      
###### ‎
- When it's done converting it will redirect you to a page where you can listen the results.      
     
a. Tap the three buttons of the **Vocals** audio and then `Download`.    
‎     
b. Do the same for the `Instrumental` one, if you wish to keep it.      

    <img src="../uvrmvsep-img/12.png" alt="image" width="400" height="auto">‎   
***

###### ‎
#### 5. Remove reverb.       
###### ‎
- Usually songs include reverb to the vocals. Leaving them in will **negatively** impact the quality in RVC.    

a. Go to the main page & input the vocals.      
‎     
b. In `Separation type` select `Ultimate Vocal Remover HQ`.      
‎     
c. In `Model Type` select the model `UVR-DeEcho-DeReverb`.      
‎     
c. Click `Separate` & then download the vocals with no reverb.      

    <img src="../uvrmvsep-img/13.png" alt="image" width="420" height="auto">‎   

***
###### ‎
#### 6. Extract main vocals. 
###### ‎
- Just like reverb, songs also normally include backing vocals.

a. Go to the main page & input the vocals with no reverb.       
‎     
b. In `Separation type` select `Ultimate Vocal Remover HQ`.         
‎     
c. Select the model `UVR-BVE-4B_SN-44100-1`.        
‎     
c. Click `Separate` and then download the main vocals. Also the backing vocals stem too, if you wish to keep them.

    <img src="../uvrmvsep-img/14.png" alt="image" width="420" height="auto">‎   
    ‎     

e. If you then notice background noise, use the model `UVR-DeNoise`.        
‎     
!!!warning For the best results, follow the pipeline explained before:       
Extract vocals -> Remove reverb -> Extract main vocals -> Remove noise
!!!  
***
:::content-center
[!button variant="danger" corners="pill" icon="heart-fill" iconAlign="right" text="Support MVSEP"](https://mvsep.com/billing)
:::
===

==- Only Cleaning 🗣️   
###### ‎     
#### 1. Log in.  
###### ‎
a. First, make an account <u>[here</u>](https://mvsep.com/register).      
‎     
b. Once logged in, go to the <u>[main page</u>](https://mvsep.com).     

!!!
Logging in is not mandatory, but recommended for **shorter waiting lists**.
!!!
***
###### ‎
#### 2. Select audio & output format.    
###### ‎
a. Click `Browse File` and select your audio. The audio will begin to upload. (or just drag the file into it)       
‎     
    <img src="../uvrmvsep-img/9.png" alt="image" width="330" height="auto">‎        
‎       
‎     
b. In `Output encoding` select `FLAC`.      
We recommend selecting FLAC from now on. Learn more <u>[here</u>](https://aihubdocs.github.io/en/rvc-resources/audio-formats--sample-rate/).        

    <img src="../uvrmvsep-img/10.png" alt="image" width="420" height="auto">‎    
***
###### ‎
#### 3. Select model.  
###### ‎
a. In `Separation Type`, select `Ultimate Vocal Remover 5 HQ`.      
‎     
b. Check the <u>[model list](https://aihubdocs.github.io/en/vocal-isolation--datasets/vocal-isolation/#mvseps-best-models-)</u> & in `Select VR Model` pick the one according to what you need to remove.         
‎       
If you need to remove multiple noises, follow this pipeline for the best results:       
``Remove reverb -> Extract main vocals -> Remove noise`` 
*** 
###### ‎
#### 4. Download output.       
###### ‎
a. Click `Separate` & when it's done converting it will redirect you to a page, where you can listen the results.    
‎     
b. Tap the three dots of the audio you need and then `Download`. If you wish to keep the backing vocals stem, remember to download it too.      
      
    <img src="..\uvrmvsep-img\12.png" alt="image" width="400" height="auto">‎   
***
:::content-center
[!button variant="danger" corners="pill" icon="heart-fill" iconAlign="right" text="Support MVSEP"](https://mvsep.com/billing)
:::

===
***
###### ‎ 
### Troubleshooting ‎ :icon-tools:
==- *MVSEP extracted too much/too little.*
###### ‎ 
- Using the **Separation Type** of `Ultimate Vocal Remover HQ`, you can modify the `Aggressiveness` value. 
This determines the depth of the extraction.
- A higher value will deepen the extraction, and a lower one will soften it.
- Each audio is different, so you'll have to test the ideal value.
===

==- *I can't remove some of the backing vocals.*
###### ‎ 
- Try running the audio through MDX23C or DeNoise. Modify the Aggression Setting if necessary.
===

‎       
‎  
:::content-center
## <u>Best Models</u> :icon-star-fill:         
#### `Their most convenient models, oriented to RVC.`    
###### ‎ 
:::

+++ UVR
Extraction | Process Method | Model
:---: | :---: | :---:
Vocals/Instrumental | MDX-Net | MDX23C
Reverb | VR | DeEcho-DeReverb
Main Vocals | VR | UVR-BVE-4B_SN-44100-1
Noise | VR | UVR-DeNoise 

+++ MVSEP
Extraction | Separation Type | Model
:---: | :---: | :---:
Vocals/Instrumental | MDX23C | - 
Reverb | Ultimate Vocal Remover 5 HQ | UVR-DeEcho-DeReverb
Backing Vocals | Ultimate Vocal Remover 5 HQ | UVR-BVE-4B_SN-44100-1
Noise | Ultimate Vocal Remover 5 HQ | UVR-DeNoise

+++

###### ‎ 
:::content-right
``Written by Julia``
:::
‎     
:::content-right
[!badge variant="info" size="xl" corners="pill" icon="paper-airplane" iconAlign="right" text="Report Issues"](http://aihubdocs.github.io/en/#contributions)   
::: 
‎     
‎  
***

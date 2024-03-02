---
icon: chevron-right
order: 3000
---

``Last update: Feb 25, 2024`` 
‎  
***
###### ‎  
:::content-center
## Introduction :icon-book:
:::

- AICoverGen UI is a port of the AICoverGen <u>[fork</u>](https://aihubdocs.github.io/en/essentials/whats-rvc/#forks) to <u>[Google Colab</u>](https://aihubdocs.github.io/en/extra/glossary/#google-colab). Port by <u>[Hina](https://huggingface.co/HinaBl)</u>, original repo by <u>[SociallyIneptWeeb</u>](https://github.com/SociallyIneptWeeb/AICoverGen).    

- It's ideal for users who want '*quick & dirty*' AI covers, as the whole process of inputting audio, vocal isolation & song mixing is automated. 

- The pitch control is limiting & inconvenient. So if you want an output with a perfect pitch, use <u>[Ilaria RVC](https://aihubdocs.github.io/en/rvc/cloud/ilaria-rvc/)</u> instead.  
‎          
### Pros & Cons :icon-tasklist:
==- *Learn more*
!!! *The pros & cons are subjective to your necessities.*      
!!!
||| **✔️ PROS:**       
- Automatic vocal extraction.           
- Song mixing tool.                 
- Has Mangio-Crepe.      
- Automatic model upload.               
- Input audio with YouTube links
- Great UI.
- Can get the stems files.
||| **❌ CONS:**       
- Usage limit for free users.           
- Takes 6 mins to load.        
- No control over the stem separation.
- The extraction will always run, you'll waste time if you input clean vocals. 
- Little control of the mixing tools.
- Inconvenient pitch control.
|||    

===

###### ‎  
###### ‎  
:::content-center
## Setting Up
:::
###### ‎  
1. Access the Colab space <u>[here](https://colab.research.google.com/github/hinabl/AICoverGen-Colab/blob/main/Hina_Mod_AICoverGen_colab.ipynb)</u>.
Then login to your Google account.
***
2. In the **Clone Repository** cell, select the pitch change.

    <img src="..\aicovergenui-img\clonerepo.png" alt="image" width="400">‎      
    ‎   
- Use ``1`` if you're going to use models of the same gender as the vocals.
- Use ``12`` if you're going to use models over the opposite gender.
- To change this, you'll have to start the Colab from scratch.
***
3. Then go to **Runtime** on top & press ``Run all``.

    <img src="..\aicovergenui-img\runall.png" alt="image" width="400">

***
4. After a moment the **Run WebUI** cell will show you two links. Open the **public URL** one.

    <img src="..\aicovergenui-img\url.png" alt="image" width="600">‎    
###### ‎   
!!!warning Don't close the Colab until you're done using it, or it will stop working.
!!!
***
###### ‎  
###### ‎  
:::content-center
## How to Use
:::
###### ‎  
#### 1. Upload model
- You can input models either using **its link** or **manually**.   
    +++ Link
    a. Go to the **Download model** tab & paste the <u>[model link](https://aihubdocs.github.io/en/essentials/voice-models/#how-to-search-voice-models)</u> in the bar.

    b. Name it in **Name your model**. Don't introduce spaces/special characters.

    c. Click **Download**.

        <img src="..\aicovergenui-img\modellink.png" alt="image" width="750">

    +++ Manually
    a. Zip the model into a .ZIP file, if you haven't already.

    b. Go to the **Upload model** tab, press the upload box & submit the ZIP.

    c. Name it in **Model name**. Don't introduce spaces/special characters.

    d. Press **Upload model**.

        <img src="..\aicovergenui-img\manualupload.png" alt="image" width="600">

    +++

###### ‎  
#### 2. Select model
- Return to the **Generate** tab & press **Refresh Models**. Then select it in the **Voice Models** dropdown.

    <img src="..\aicovergenui-img\selectmodel.png" alt="image" width="400">
***
###### ‎  
#### 3. Select audio
- On its right, input the YouTube link.

    <img src="..\aicovergenui-img\link.png" alt="image" width="380">‎  
‎  
- Or, press **Upload file instead**, click **Upload** & input the audio file.
***
###### ‎  
#### 4. Modify settings (optional)
- Unfold **Voice conversion options** to modify the <u>[inference settings](https://aihubdocs.github.io/en/rvc/resources/inference-settings/)</u> for better results.

***
###### ‎  
#### 5. Select output format
- Unfold **Audio mixing options** & set **Output file type** as ``wav``, for a better quality result.

    <img src="..\aicovergenui-img\wav.png" alt="image" width="600">‎    
‎   
- Modify the mix too if you wish.
***
###### ‎  
#### 6. Convert
- Press **Generate**. The audio will start processing.
- Once it's done, you can hear the results in the **AI Cover** output box.
- To download it, press the download symbol ( :icon-download: ) on its right.

    <img src="..\aicovergenui-img\output.png" alt="image" width="400">

***
###### ‎  
#### 7. Download stems (optional)
- To download the stems, go to Colab & click the folder symbol ( :icon-file-directory: ) on the left.       
(For mobile users, tap the three lines ( :icon-three-bars: ) on the top left & press **Show File Explorer**)

- Go to **Hina_RVC**, **song_output**, open the new folder, right-click the stem you wish & click `Download`.

    <img src="..\aicovergenui-img\stems.png" alt="image" width="470">‎    
‎    
- #### If the voice glitches out, click <u>[here](https://aihubdocs.github.io/en/rvc/resources/inference-settings/)</u>.
***
:::content-right
`Written by Julia`   
:::
‎    
:::content-right
[!badge variant="info" size="xl" corners="pill" icon="paper-airplane" iconAlign="right" text="Report Issues"](http://aihubdocs.github.io/en/#contributions)
::: 
:::
###### ‎ 
###### ‎ 
***
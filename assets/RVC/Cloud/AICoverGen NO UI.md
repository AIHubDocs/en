---
icon: chevron-right
order: 4000
---

``Last update: Feb 17, 2024`` 
‎  
***
###### ‎  
:::content-center
## Introduction :icon-book:
:::
- AICoverGen NO UI is a port of the AICoverGen RVC <u>[fork</u>](https://aihubdocs.github.io/en/extra/glossary/#fork) to <u>[Google Colab</u>](https://aihubdocs.github.io/en/extra/glossary/#google-colab). Base notebook by <u>[Ardha27</u>](https://github.com/ardha27).    

- This version (**Eddy's Version**) is an upgrade from the original Colab space, bringing bug fixes, improvements, & extra features. Credits to Eddy & Raid.

- It's ideal for users who want '*quick & dirty*' AI covers, as the whole process is automated. You can input a YouTube link and the vocal isolation & song mixing process will be automatized.
‎               
### Pros & Cons :icon-tasklist:
==- ***Learn more***
!!! *The pros & cons are subjective to your necessities.*      
!!!
||| **✔️ PROS:**       
- Automatic vocal extraction.           
- Song mixing tool.            
- Tool to add reverb.       
- Includes Mangio-Crepe algorithm.      
- Model download through links.               
- Can input audio with YouTube links. 
- Automatic stem separation (can get each later).
||| **❌ CONS:**       
- Usage limit for free users.           
- Takes 6 mins to load.        
- UI is not great.  
- No control over the stem separation process. Could be a problem.
- Said extraction will always run. You'll waste time if you input clean vocals. 
- Little control of the mixing-reverb tools. Using a DAW is more convenient
|||     
===               
***
###### ‎  
:::content-center
## How to Use :icon-checklist:
:::
###### ‎  
#### 1. <u>Enter the space.</u>      
a. Log in to Google <u>[here</u>](https://accounts.google.com/).     
b. Then access the Colab space <u>[here</u>](https://colab.research.google.com/drive/1u1brjK8IZt647UsbZuGYfW29oFM2I4tk?usp%3Dsharing&sa=D&source=editors&ust=1704303145687891&usg=AOvVaw3M9tmokG80RXF-GD1LJqCL).    

    <img src="../aicovergennoui-img/page.png" alt="image" width="500" height="auto">     

***     
‎       
#### 2. <u>Clone and Install.</u>     
- Execute the ``Clone and Install``.     
This will install RVC.      

    <img src="../aicovergennoui-img/cloneandinstall.png" alt="image" width="280" height="auto">‎         
‎    
- It will take around 15 minutes.       
It'll be done when you see a check symbol (✔️) on the corner.        

    <img src="../aicovergennoui-img/check.png" alt="image" width="370" height="auto">‎
‎         
>Don't worry if red text appears, it's normal.          

***
‎       
#### 3. <u>Download voice model.</u>    
<img src="../aicovergennoui-img/model.png" alt="image" width="550" height="auto">‎       
‎ 
a. Go to `Model Download Function` cell.        
Paste the model's link in the ``url`` bar.     
       

b. In `dir_name` name the model. Don't include spaces/special characters.        
           
c. Then execute the cell. 

!!!
The models you download will be saved until the Colab session ends.  
!!!
***
###### ‎  
#### 4. <u>Input the audio.</u>      
Input the vocals/song in the `Generate Cover` cell.     

You have two ways of doing this: using a <u>**YouTube link**</u> or a <u>**Google Drive file**</u>:     

+++ **YouTube link**
Copy a YouTube link, and paste it in the ``SONG_INPUT`` bar.

<img src="../aicovergennoui-img/generatecoveryt.png" alt="image" width="420" height="auto">‎              

+++ **Google Drive file**       
###### ‎   
a. Execute the cell ``Mount Drive`` that's below `Generate Cover`.      
‎       
     <img src="../aicovergennoui-img/mountdrive.png" alt="image" width="210" height="auto">‎           

***      
b. Click `Connect to Google Drive` & select your Google Account.   
‎        
    <img src="../aicovergennoui-img/connect.png" alt="image" width="280" height="auto"> 
***      
c. Click the folder symbol ( :icon-file-directory: ) on the right.      
(For mobile users: tap the three lines on the top left & `Show file browser`)

    Go to ``drive`` folder, then ``MyDrive``, & you'll find your Google Drive storage.        
    Find your audio, right-click it, & press ``Copy path``.       
‎       
    <img src="../aicovergennoui-img/1.png" alt="image" width="320" height="auto">           
***        
d. Paste the path file in the `SONG_INPUT` bar, located in the `Generate Cover` cell.    
‎            
    <img src="../aicovergennoui-img/inputaudio.png" alt="image" width="420" height="auto">
+++
###### ‎  
#### 5. <u>Select voice model.</u>        
Under it in ``RVC_DIRNAME`` type the model's name that you have assigned before.       

<img src="../aicovergennoui-img/2.png" alt="image" width="400" height="auto">    

***     
###### ‎   
#### 6. <u>Modify settings.</u> (optional)        
Below ``RVC_DIRNAME`` until ``Audio Mixing Options`` you'll find the <u>[inference settings</u>](https://aihubdocs.github.io/en/rvc-resources/inference-settings/).     
Tweak them accordingly for better results if you wish.

 <img src="../aicovergennoui-img/3.png" alt="image" width="270" height="auto">        

‎       
> • ‎ `REMIX_MIX_RATE` works like *Volume Envelope*.        
> • ‎ `FILTER_RADIUS` lowers the volume of breath sounds. (not suppress) 
***
###### ‎  
#### 7 . <u>Modify mix & reverb.</u> (optional)         

- In ``Audio Mixing Options``, you can change the values to determine the volume of main vocals, backing vocals, & instrumental.      

    <img src="../aicovergennoui-img/4.png" alt="image" width="240" height="auto">‎                
    ‎     
- In `Reverb Control`, you can add reverb to the output vocals.      
    ‎       
<img src="../aicovergennoui-img/6.png" alt="image" width="240" height="auto"> ‎  
 ‎      
==- <u>*Reverb Control options:*</u>
REVERB_SIZE
:    How "wide" the reverb sounds, like the size of a room.       

REVERB_WETNESS
:    Volume of the reverb itself.        

REVERB_DRYNESS
:    Volume of the vocals.       

REVERB_DAMPING
:    Level of absorption of the reverb's *high frequencies*:       
‎ ‎ ‎ ‎ ‎ ‎ • ‎ Higher values yield a warmer, natural-sounding reverb.       
‎ ‎ ‎ ‎ ‎ ‎ • ‎ Lower ones sound brighter & more present.   
===

***
###### ‎    
#### 8. <u>Begin the inference.</u>      
Once you are ready, execute the `Generate Cover` cell to begin the conversion.      

It'll be done when the last message says "**Cover generated at**" followed by the file path.    

<img src="../aicovergennoui-img/9.png" alt="image" width="850" height="auto">

***
###### ‎   
#### 9. <u>Download the output.</u>     
a. Click the folder symbol ( :icon-file-directory: ) on the right.      
(For mobile users: tap the three lines on the top left & `Show file browser`)        

    Open the `song_output` & then the one with a bunch of numbers.

b. Right-click the first file & press `Download`. The rest of the audios are the stems, that you can download too if you wish.

    <img src="../aicovergennoui-img/10.png" alt="image" width="550" height="auto">‎   

###### ‎  
- #### If the voice glitches out, click <u>[here</u>](https://aihubdocs.github.io/en/rvc-resources/artifacting/).
***
###### ‎   
:::content-center
``Original guide: Eddy``     
:::
:::content-center
``Redone by: Julia``  
:::
:::content-center
[!button variant="primary" corners="pill" icon="feed-discussion" iconAlign="right" text="Send Suggestions"](http://aihubdocs.github.io/en/#contributions)
::: 
***

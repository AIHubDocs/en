---
icon: chevron-right
order: 2000
---

# GPT-So-VITS
**COLAB TUTORIAL COMING SOON**		
This tutorial is made by Delik. If you have any questions and/or suggestions you can contact me on discord (**delik**) or wechat (**Dellikk**)

!!!info GPT-SoVITS is an open-source repository focused on TTS and cross language inference. Currently it only supports Chinese, English and Japanese. More languages coming soon!
!!!note Acknowledgements
	First of all, I would like to thank **[RVC-Boss](https://space.bilibili.com/5760446)** for making this repository for TTS.
	There is a **[Chinese tutorial](https://www.yuque.com/baicaigongchang1145haoyuangong/ib3g1e)** for GPT-SoVITS that is made by **[白菜工厂1145号员工](https://space.bilibili.com/518098961)**, this guide will be a translation of the chinese guide with a few little tweaks.

!!!warning Please read the colab tutorial if you do not have a Nvidia GPU with >=6G vram.
### 1, Download the **[latest prezip](https://huggingface.co/datasets/Delik/gptsovits_i18nfix/resolve/main/GPT-SoVITS-beta0306.7z?download=true)**

### 2, Open webui
Extract the **whole folder** then double click **go-web.bat** to open webui
!!!note It is best to use 7-zip to extract. You can download the software [here](https://www.7-zip.org)

### 3, Initialize dataset
!!!note Your dataset should be between 1 to 30 minutes. Prioritize quality over quantity.
!!!note GPT-SoVITS is made for TTS only, so it is best to remove any singing parts or parts with muffled voice. Before running GPT-SoVITS, you should perform audio denoising to enhance the quality of the model. There is a tutorial: **[Perfecting Audio Isolation On Low End Rigs: A Comprehensive Guide](https://docs.google.com/document/d/1HmkG9cmL8SLX7-vJcPT1-1KgUQtCrwXB8CicYmG4LW8/edit#heading=h.ub20t3fkdp39)** by Lista the Dancer and Faze Masta
!!!warning Just do the denoise section for the guide above

Bandit plus is a great model for denoising if you guys want a simple solution, you can use that model on [mvsep.com](https://mvsep.com/). Create an account to skip queues. 


##### 3.1, Audio Slicer
![](https://i.postimg.cc/7Lnnt3gN/screenshot-2.png)

There are only two things you need to change, which is **Audio slicer input** and **Audio slicer output**.
For **Audio slicer input**, just copy the path of your dataset file (usually ends in .wav or .mp3) and paste it inside the textbox
For **Audio slicer output**, you need to **create a new folder** somewhere to store your outputs, then copy the path and paste it inside the textbox.
Adjust the parameters **if needed**.
Finally, click **Start Audio Slicer** to complete this step.
### 4, ASR & text labelling
##### 4.1, ASR
![](https://i.postimg.cc/8cfrYztT/screenshot-2.png)
The **Input folder path** should be the same as **Audio slicer output**, just copy the path and paste it inside the textbox.
If the dataset is in English or Japanese, use **Faster-Whisper large v3**.
If the dataset is in Chinese, use **达摩ASR**.

Then, click **Start batch ASR**

!!!info If you run GPT-SoVITS for the first time, you might need to wait for a few minutes for it to download the ASR model you select.

Finally, locate the .list file and copy the path. It will be in **output/asr_opt** (if you didnt change the folder for **Output folder path**)
#####4.2, Text Labelling (Optional)
![](https://i.postimg.cc/DZ1WGDWf/screenshot-2.png)
Paste the .list file path into **.list annotation file path**
Tick **Open labelling WebUI** to open text labelling webui (A new window will popout in the browser)
![](https://i.postimg.cc/mrG9PGjD/screenshot-2.png)
Listen to each clip and edit the text if it is not transcribed properly.
The functions are pretty self explanatory. Use **next index** and **previous index** to check the next/previous page.  if you make any changes, remember to **save file** and **submit text**.






### 5, Train models
##### 5.1, Formatting
Click **1-GPT-SOVITS-TTS** (and **1A-Dataset formatting**) to enter the training page
![](https://i.postimg.cc/YqGYtLsN/screenshot-2.png)
Input the name of your model to **Experiment/model name** and the .list file path to **Text labelling file**.

Then scroll down to the end, click start **one-click formatting** to complete the first step.
##### 5.2, Training
Scroll up then click **1B-Fine-tuned training**
![](https://i.postimg.cc/0Q1SrsVy/screenshot-2.png)
Here are the reccomended settings for **SoVITS training**:
- Batch size: 2 (1 if your gpu has 6G vram)
- Total epochs: 8
- Text model learning rate weighting: <=0.4
- Save frequency: 4

After that click **Start SoVITS training**

Here are the reccomended settings for **GPT training**:
- Batch size: 2 (1 if your gpu has 6G vram)
- Total epochs: 10
- Save frequency: 5
- DPO training disabled (I will talk about this later)

After that click **Start GPT training**

!!!danger YOU CANNOT TRAIN THESE TWO SIMOTANEOUSLY UNLESS YOU HAVE 2 OR MORE GPUS. WAIT FOR ONE TO FINISH TRAINING THEN TRAIN THE OTHER ONE!!!

##### DPO training (optional)
DPO training greatly improves the performance (not audio quality wise) and stability of the model. It can infer more text at once without slicing, and there wont be any funny errors (such as repeating certain words or skipping words) when infering.
!!!warning You need to have a gpu that has 12G or more VRAM  AND a  VERY HIGH quality dataset (you need to do text labelling) to enable this. Otherwise IT WILL MAKE YOUR MODEL WORSE!!!

You need to change your batch size to 1, while keep the other settings same as above.


### 6, Inference
![](https://i.postimg.cc/6qdPzLkw/screenshot-2.png)
Click 1**C-inference**, then click **refreshing model paths** to make your models appear on the dropdown.

Choose your models from the dropdowns respectively then tick **Open tts inference WEBUI**
![](https://i.postimg.cc/Xvr27Gfw/screenshot-2.png)
#####6.1 Reference information
Upload a clip for reference audio (**must be 3-10 seconds**) then fill in the **Text for reference audio**, which is basically what does the character say in the audio. Choose the language on the right.

!!!info The reference audio is very important as it determines the speed and the emotion of the output. Please try different ones if you did not get your desired output.
!!!note You can reopen the text proofreading tool to download the reference audio and copy and paste the text for reference audio
!!!note Hover above the "duration" to adjust the length of the reference audio and hover above "it" to delete the current refernce audio
!!!warning No reference text mode exists but I DO NOT reccommend using it. It will affect the quality alot.

##### 6.2 Inference
Fill the **inference text** and set the **inference language**, then click **Start inference**.
!!!info If the text is too long choose the options in **How to slice the sentence**.
!!!note If you did not get your desired output, you can infer it **again** or **change reference audio** and/or **adjust GPT parameters**.

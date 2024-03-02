---
icon: chevron-right
---

``Last update: Mar 2, 2024``
***

## Introduction :icon-book:
***
- TTS is an abbreviation of Text To Speech, an AI that converts any given text into vocal speech.

- Some TTS make the speech from scratch, but others mentioned here are mixed with <u>[RVC](http://localhost:5000/en/essentials/whats-rvc/)</u>, converting audio to audio.

- but in some cases like Applio, it generates a TTS Audio of Edge TTS and then it changes the audio voice to the RVC model voice.

- Here's a list of some of the best TTS tools out there.
***
## ElevenLabs/11Labs
***
- <u>[ElevenLabs](https://elevenlabs.io/)</u> is a **freemium** (only one in this guide) service that offers TTS, training TTS models & translating videos from different languages.

***
## Bark TTS
***

- Bark is a **multilingual** TTS model created by Suno AI. It’s good at expressing **emotions** & non-speech sounds, such as laughter, laughs, sighs, music, gasps, clearing throat, hesitations ( - or … ), ♪ for song lyrics, emphasis of words.
MAN/WOMAN: for bias towards speaker

- It can be used both <u>[locally](https://aihubdocs.github.io/en/extra/glossary/#local-running)</u> or on the <u>[cloud](http://aihubdocs.github.io/en/extra/glossary/#cloud-based)</u>:

+++ **:icon-device-desktop: ‎ LOCAL**
- [Official Bark TTS Guide](https://github.com/suno-ai/bark)
- [Fixed Fork](https://github.com/Nick088Official/bark-gui-fix) (Gradio UI & finetuning)
- [Voice Cloning Fork](https://github.com/KevinWang676/Bark-Voice-Cloning/tree/main) (0 shot training. Remember that it needs GPU to train voices)

+++ **:icon-cloud: ‎ CLOUD**
- [Easier Bark TTS Colab](https://colab.research.google.com/github/Nick088Official/Easier-Bark-TTS-Google-Colab/blob/main/Easier_Bark_TTS.ipynb)
- [Official Bark TTS Hugging Face Space](https://huggingface.co/spaces/suno/bark)
- [Bark GUI Google Colab](https://colab.research.google.com/github/Nick088Official/bark-gui-fix-google-colab/blob/main/Bark_GUI_Fix.ipynb) (Gradio UI with finetuning)
- [Easier Bark 0 Shot Voice Cloning Fork Google Colab](https://colab.research.google.com/github/Nick088Official/Easier-Bark-Voice-Cloning-Google-Colab/blob/main/Bark_Voice_Cloning.ipynb)
- [Bark GUI 0 Shot Voice Cloning Hugging Face Space](https://huggingface.co/spaces/kevinwang676/Bark-with-Voice-Cloning) (Need GPU for Voice Cloning 0 shot training, so unless you duplicate the space with your paid GPU, you can only TTS)
+++
***
## Edge TTS

- This is Microsoft Edge TTS, which is **good quality**, multilingual & works great on long sentences. It can be used only online (API):

  - **Online**
  - [Edge TTS Google Colab](https://github.com/Nick088Official/Edge-TTS-Google-Colab/tree/main)
  - [Edge TTS Hugging Face Space](https://huggingface.co/spaces/Nick088/Edge-TTS)
  - [Use Ilaria TTS inside of Ilaria RVC UI Colab](https://colab.research.google.com/drive/16LkwvFZeudTpUOsE_6bMjOq2qkxFo8Hr?usp=sharing#scrollTo=t8gn3pmO14On) (with Voice Cloning, mixing with RVC)
  - [Use Ilaria TTS Inside of Ilaria RVC Hugging Face Space](https://huggingface.co/spaces/TheStinger/Ilaria_RVC) (with Voice Cloning, mixing with RVC)
  - [Use the TTS in Applio RVC Fork UI Google Colab](https://colab.research.google.com/github/iahispano/applio/blob/master/assets/Applio.ipynb) (with Voice Cloning, mixing with RVC)
  - [Use the TTS in Applio RVC Fork Hugging Face Space](https://huggingface.co/spaces/IAHispano/Applio) (with Voice Cloning, mixing with RVC)
  - [Use Applio RVC Fork](https://github.com/IAHispano/Applio) (with Voice Cloning, mixing with RVC)
  - Microsoft Edge:
  a. Download the Microsoft Edge Browser
  
  b. Open your Notepad
  
  c. Paste the following code:
  
```
<!DOCTYPE html>
<html>
<body style="background-color:#dddddd">

<h3 aria-hidden="true">Browser TTS "Hack"</h3>

<textarea rows="10" cols="50" id="ttsText" style="background-color:#eeeeee"></textarea>
<br />
<button aria-hidden="true" onclick="genText()"><font aria-hidden="true">Generate</font></button>

<pre id="tts"></pre>

<script>
function genText() {
  var x = document.getElementById("ttsText").value;
  document.getElementById("tts").innerHTML = x;
}
</script>



</body>
</html>
```

  d. Save it as “Microsoft Edge TTS.txt”
  
  e. Rename the file to “Microsoft Edge TTS.html”
  
  f. Open Microsoft Edge
  
  g. Drag the .html to it
  
  h. Write anything you want
  
  i. Use [Audacity](https://www.audacityteam.org/download/) to record the audio, set the recording mode to loopback and it allows to record the internal audio (Realtek driver might be needed)
  
  j. Click Generate and then stop recording when the voice is done.
  
  k. After you click generate, you can also select Voice options in the toolbar and change the speed to a faster or slower speech pace.
***
## StyleTTS2
***
- StyleTTS 2 aims to achieve human-level TTS synthesis only in English, It works better on full sentences, both available locally and online.
It's possible to finetune on your own dataset.
It has 2 versions:
**LJSpeech** & **LibriTTS**.

**Key Difference:**

**LJSpeech**: The dataset consists of **single-speaker** recordings, making it suitable for training TTS models with a consistent voice.
**LibriTTS**: The dataset includes **multispeaker** recordings, allowing StyleTTS 2 to adapt to different voices.

**Locally**
- [Official StyleTTS2 Guide](https://github.com/yl4579/StyleTTS2)

**Online**
- [StyleTTS2 Hugging Face Space](https://huggingface.co/spaces/styletts2/styletts2) (If you duplicate the space to skip queue, without GPU you can only inference)
- [StyleTTS2 LJSpeech Inference Google Colab](https://colab.research.google.com/github/yl4579/StyleTTS2/blob/main/Colab/StyleTTS2_Demo_LJSpeech.ipynb)
- [StyleTTS2 LibriTTS Inference Google Colab](https://colab.research.google.com/github/yl4579/StyleTTS2/blob/main/Colab/StyleTTS2_Demo_LibriTTS.ipynb)
- [StyleTTS2 Finetuning Google Colab](https://colab.research.google.com/github/yl4579/StyleTTS2/blob/main/Colab/StyleTTS2_Finetune_Demo.ipynb) 

***
## Tortoise TTS
***
Tortoise is expressive but it’s kinda slow.
You can use it both locally and online:

**Locally**
- [Official Tortoise TTS Github Repository](https://github.com/neonbjb/tortoise-tts)

**Online**
- [Tortoise TTS Hugging Face Space](https://huggingface.co/spaces/Manmay/tortoise-tts)
- [Easier Tortoise TTS Google Colab](https://colab.research.google.com/github/Nick088Official/Easier-Tortoise-TTS-Google-Colab/blob/main/Easier_Tortoise_TTS.ipynb)

***
## XTTS2
***
Developed by Coqui AI, which has been **discontinued** unfortunately, Built on the 🐢Tortoise, ⓍTTS has important model changes that make **cross-language 0 Shot voice cloning** and **multilingual** speech generation super easy. **You need less training data, at least a 2 minutes audio.**
You can use it either online or locally:

**Locally**
- [Official XTTS 2 Guide](https://docs.coqui.ai/en/latest/models/xtts.html)
- [XTTS 2 UI Fork](https://github.com/BoltzmannEntropy/xtts2-ui)

**Online**
- [XTTS 2 Hugging Face Space](https://huggingface.co/spaces/coqui/xtts)
- [XTTS 2 Inference UI Google Colab](https://colab.research.google.com/github/camenduru/coqui-XTTS-colab/blob/main/coqui_XTTS_v2_colab.ipynb): Run it and click the Gradio Public Link
- [XTTS 2 Training & Inference UI Google Colab](https://colab.research.google.com/drive/1GiI4_X724M8q2W-zZ-jXo7cWTV7RfaH-?usp=sharing): [Watch this Video Tutorial for it!](https://www.youtube.com/watch?v=8tpDiiouGxc)

***
## MetaVoice
***
**MetaVoice-1B** is a 1.2B parameter base model **trained on 100K hours of speech for TTS** (text-to-speech). It has been built with the following priorities:
**Emotional speech rhythm and tone in English.**
**Zero-shot cloning for American & British voices, with 30s reference audio.**
It can be used both locally and online:

**Locally**
- [Official MetaVoice 1B Model Github Repository](https://github.com/metavoiceio/metavoice-src) 

**Online**
- [MetaVoice 1B Model TTS with 0 Shot Training Demo](https://ttsdemo.themetavoice.xyz/)
- [MetaVoice 1B Model TTS with 0 Shot Training Hugging Face Space](https://huggingface.co/spaces/mrfakename/MetaVoice-1B-v0.1)
- [Easier MetaVoice 1B Model TTS with 0 Shot Training Google Colab](https://colab.research.google.com/github/Nick088Official/Easier-MetaVoice-1B-Google-Colab/blob/main/Easier_MetaVoice_1B.ipynb)
- [Freemium MetaVoice Studio Only Premade Voices](https://colab.research.google.com/github/Nick088Official/Easier-MetaVoice-1B-Google-Colab/blob/main/Easier_MetaVoice_1B.ipynb)

***
## MeloTTS
***
MeloTTS is a **high-quality multilingual** text-to-speech library by MyShell.ai with **almost real time inference**.
It can be used both locally and online:

**Locally**
- [Official MeloTTS Github Repository](https://github.com/myshell-ai/MeloTTS)

Online:
- [MeloTTS Hugging Face Space](https://huggingface.co/spaces/mrfakename/MeloTTS)
- [MeloTTS UI Google Colab](https://colab.research.google.com/github/Nick088Official/MeloTTS-Google-Colabs/blob/main/MeloTTS_UI.ipynb)
- [MeloTTS NO UI Google Colab](https://colab.research.google.com/github/Nick088Official/MeloTTS-Google-Colabs/blob/main/MeloTTS_NO_UI.ipynb)

***
## GPT-SoVITS
***
GPT-SoVITS has **cross language inference**, but there could be some noises, it's also very good especially with **chinese**, but also with english.
**WARNING: MOST PARTS OF THIS PROGRAM ARE IN JAPANESE AND NOT DEEPLY TESTED, will prolly have have a deeper guide when Delik releases it.**
It can be used both locally and online:

**Locally**
- [Official GPT-SoVITS Github Repository](https://github.com/RVC-Boss/GPT-SoVITS/)

**Online**
- [GPT-SoVITS Google Colab Finetuning & Inference UI](https://colab.research.google.com/github/RVC-Boss/GPT-SoVITS/blob/main/colab_webui.ipynb#scrollTo=4oRGUzkrk8C7)

***
## gTTS
***
**Google Text To Speech**, the same one used in Google Translator, it has **very few voices in different languages**, kinda **robotic** and doesn’t let you choose the gender of the voice, except in the colab version where i made a function to change the pitch of it, but it isn't that great. It can be used only online (API) :

**Online**
- [gTTS Google Colab](https://colab.research.google.com/github/Nick088Official/gTTS-Google-Colab/blob/main/gTTS.ipynb)
- [gTTS Hugging Face Space](https://huggingface.co/spaces/Nick088/gTTS)
- [Official gTTS Guide](https://github.com/pndurette/gTTS)
- Use Google Translator

***
:::content-right
``Written by Nick088 - Redone by Julia``    
:::
‎   
:::content-right
[!badge variant="info" size="xl" corners="pill" icon="paper-airplane" iconAlign="right" text="Report Issues"](http://aihubdocs.github.io/en/#contributions)
:::
‎   
***

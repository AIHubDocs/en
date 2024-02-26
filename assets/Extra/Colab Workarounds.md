---
icon: chevron-right
visibility: private
---

``Last update: Feb 26, 2024``
***
###### ‎
:::content-center

## Runtime disconnected due to inactivity

<img src="../colabworkarounds-img/1.png" alt="image" width="520" height="auto">‎

:::
- Happens when you remain AFK (not interacting with the space) for a long time.

- Depending on the device, the workaround varies:
+++ PC Method
1. Run the necessary cells.
***
2. When you wish to go AFK, in Colab open **Inspect Element** by pressing **Ctrl + Shift + I** (for Mac, Command + Option + C)
***
3. On the top right corner, click on the 3 dots, then Other Tools, and click DevTools
3. Then goto the Console Tab and paste (without the “”) :
“function ClickConnect(){
console.log("Working"); 
document.querySelector("colab-toolbar-button#connect").click() 
}
setInterval(ClickConnect,60000)”
4. Press Enter on your keyboard.

+++ Mobile Method

1. Bookmark any site
2. Edit the bookmark and paste the following script in the URL box (without the “”) :
“javascript:(function () { 
    var script =  document.createElement('script');
    script.src="//cdn.jsdelivr.net/npm/eruda"; 
    document.body.appendChild(script);
    script.onload = function () { 
        eruda.init() 
    } 
})();”
4. Change the Bookmark Name to Inspect Element (or ChromeDevTools, whatever you want it doesn’t really matter).
5. Now go to the site,in this case the Colab, and go on the search bar where you will search Inspect Element (or whatever name you gave the bookmark), there will be a result that is the Bookmarked one, click it.
6. Now after 5 seconds you will have a gear icon at the bottom right of the site,click it and now you have the inspect element view.

+++

#### If you get a warning when trying to paste the code, not letting you to, you got 2 methods to fix it:
**Manual Toggle:**
  A. Open DevTools.
  B. Navigate to Experiments.
  C. In the filter, type “Pasting” to find the relevant option.
  D. Toggle “Show warning about self-XSS when pasting code” to disable the warning.
  E. Just paste again the code and press enter.

:::content-center
## Cannot connect to GPU backend
:::

![image](https://github.com/AIHubDocs/en/assets/91847579/98d8dc7e-99e9-4596-ade4-f0bef40385d6)

Was using a colab and then got this popup? It means you finished the GPU Hours of Colab.

**Google Colab** offers for **free around 12 hours daily of GPU**,
**but depends on the colab task usage**,
**if its high**, like for RVC and W-Okada,
its then **around 4 hours a day**.

You can connect without GPU, but most colabs need GPU to run, like RVC/W-Okada.

**Solutions**
- Use an alternative account.
- Wait 12-24 hours for it to get reset.
- [Buy Colab Subscriptions](https://colab.research.google.com/signup)
- Use CPU Runtime on colabs when the task doesn’t need GPU to not waste the GPU Hours

![image](https://github.com/AIHubDocs/en/assets/91847579/c6694b45-5bec-44d3-8360-2bf0559c5742)

:::content-center
## Disallowed code
:::
![image](https://github.com/AIHubDocs/en/assets/91847579/c97cc6de-4eaf-4862-aeb3-27c203a4b780)

Got a popup saying the colab has disallowed code? It means the code runs activities which are restricted for free users, see them all at [FAQ](https://research.google.com/colaboratory/faq.html#limitations-and-restrictions)

It could also mean the colab you are running is outdated, usually new colabs found ways to bypass this using a Link Shortener or Encrypting the code in Rot 13

***
:::content-right
``Written by Nick088``    
:::
‎   
:::content-right
[!badge variant="info" size="xl" corners="pill" icon="paper-airplane" iconAlign="right" text="Report Issues"](http://aihubdocs.github.io/en/#contributions)
:::
‎    
***

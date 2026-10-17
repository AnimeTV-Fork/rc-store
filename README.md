 I was able to fix the issue using the repo. If you could add these changes so it's slated for the newest release that would be awesome. 

I was able to fix this by making some changes to the repo and turns out it affects all devices not just my streaming box since it's reproducible in a VM. It is caused by adjusting the outline settings to medium or thick and it affects certain fonts. 

Why the Bug Happens

In AnimeTV v5.15.0+, subtitle customization introduced Google Fonts variable fonts (Outfit, Reddit Sans) and some of these fonts are constructed on the fly instead of using the native font and there were some bugs with how they were being created and rendered. 

Only two files need to be edited. You can replace them with the files I provided or follow the change directions that I provided. 

The Exact Lines to Change: 

app/src/main/assets/view/m.css
app/src/main/assets/view/fm.css


Conclusion: In my own test build I the outline settings show up correctly without distorting the font. I also have some images showing the difference fixing those files will do. 


<img width="2549" height="1518" alt="Screenshot_2026-10-11_222145" src="https://github.com/user-attachments/assets/baaf004d-a924-41d3-849d-0dcb1e9a769a" />
<img width="1280" height="764" alt="Screenshot_2026-10-11_223517" src="https://github.com/user-attachments/assets/bf926cb9-460c-4151-a47d-0598f0d57967" />

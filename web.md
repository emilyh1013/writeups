### Web
## GET aHEAD
use burp and modify the request to a head instead of post or get to get the header
`picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}`
## Cookies
i literally just brute forced the cookie value up to 18
<img width="736" alt="image" src="https://github.com/emilyh1013/writeups/assets/138421980/2bcde627-53b7-46a3-bd5c-04efd9420025">
`picoCTF{3v3ry1_l0v3s_c00k135_88acab36}`
## Insp3ct0r
control shift i the first part is <img width="414" alt="image" src="https://github.com/emilyh1013/writeups/assets/138421980/64f2a4aa-3c97-4143-8d38-41368f130bc9">
next you can notice it references "mycss.css" and "myjs.js" which gives the 2nd and 3rd parts `t3ct1ve_0r_ju5t` and `_lucky?2e7b23e3}`
`picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}`
## Scavenger Hunt 
same exact thing as inspector like step for step up to the js part 
<img width="1117" alt="image" src="https://github.com/emilyh1013/writeups/assets/138421980/5a44fffc-c5b2-4ea4-8f96-190cb3572b65">
googling "google website index" showed me this result 
## 
<https://www.bing.com/ck/a?!&&p=2e88218963fab31cJmltdHM9MTY5MDE1NjgwMCZpZ3VpZD0zNDQxMTczMy05MTFlLTZiOWEtMjdlYy0wNDY2OTA5YTZhYmImaW5zaWQ9NTIzMg&ptn=3&hsh=3&fclid=34411733-911e-6b9a-27ec-0466909a6abb&psq=google+website+indexing&u=a1aHR0cHM6Ly9haHJlZnMuY29tL2Jsb2cvZ29vZ2xlLWluZGV4Lw&ntb=1> 
##
which mentions a robot.txt file. 
going to /robots.txt gives me the next part `t_0f_pl4c` the next hint is "# I think this is an apache server... can you Access the next flag?"
googling ![image](https://github.com/emilyh1013/writeups/assets/138421980/4f4f43ff-2d4c-4edf-8420-f825216082dc)
going to .htaccess gives me the the fourth part `3s_2_lO0k`. i didnt really get the next hint which was "# I love making websites on my Mac, I can Store a lot of information there" but writeups online told me the capitalized store was apparently a reference to .DS_Store so going there gives me the lsat part. 
`picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}`
## Some Assembly Required 1
inspecting the source shows me the script source is in "G82XCw5CX3.js."
## 
<img width="637" alt="image" src="https://github.com/emilyh1013/writeups/assets/138421980/743a5bf8-86ec-40df-b8b2-13c922178584">

## 
in the big block of stuff i see a path. going there gives the flag. (strings it and grep for pico)
`picoCTF{a2843c6ba4157dc1bc052818a6242c3f}`

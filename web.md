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
```
<https://ahrefs.com/blog/google-index/> 
```
which mentions a robot.txt file. 
going to /robots.txt gives me the next part `t_0f_pl4c` the next hint is "# I think this is an apache server... can you Access the next flag?"
googling ![image](https://github.com/emilyh1013/writeups/assets/138421980/4f4f43ff-2d4c-4edf-8420-f825216082dc)
going to .htaccess gives me the the fourth part `3s_2_lO0k`. i didnt really get the next hint which was "# I love making websites on my Mac, I can Store a lot of information there" but writeups online told me the capitalized store was apparently a reference to .DS_Store so going there gives me the lsat part. 
`picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}`
## Some Assembly Required 1
inspecting the source shows me the script source is in "G82XCw5CX3.js."
```
const _0x402c=
['value','2wfTpTR','instantiate','275341bEPcme','innerHTML','1195047NznhZg','1qfevql','input','1699808QuoWhA','Correct!','check_flag','Incorrect!',
'./JIFxzHyW8W','23SMpAuA','802698XOMSrr','charCodeAt','474547vVoGDO','getElementById','instance','copy_char','43591XxcWUl','504454llVtzW','arrayBuffer',
'2NIQmVj','result'];const _0x4e0e=function(_0x553839,_0x53c021){_0x553839=_0x553839-0x1d6;let _0x402c6f=_0x402c[_0x553839];return _0x402c6f;};
(function(_0x76dd13,_0x3dfcae){const _0x371ac6=_0x4e0e;while(!![]){try{const _0x478583=-parseInt(_0x371ac6(0x1eb))+parseInt(_0x371ac6(0x1ed))+-
parseInt(_0x371ac6(0x1db))*-parseInt(_0x371ac6(0x1d9))+-parseInt(_0x371ac6(0x1e2))*-parseInt(_0x371ac6(0x1e3))+-
parseInt(_0x371ac6(0x1de))*parseInt(_0x371ac6(0x1e0))+parseInt(_0x371ac6(0x1d8))*parseInt(_0x371ac6(0x1ea))+-
parseInt(_0x371ac6(0x1e5));if(_0x478583===_0x3dfcae)break;else _0x76dd13['push'](_0x76dd13['shift']());}catch(_0x41d31a){_0x76dd13['push'](_0x76dd13['shift']
());}}}(_0x402c,0x994c3));let exports;(async()=>{const _0x48c3be=_0x4e0e;let _0x5f0229=await fetch(_0x48c3be(0x1e9)),_0x1d99e9=await
WebAssembly[_0x48c3be(0x1df)](await _0x5f0229[_0x48c3be(0x1da)]()),_0x1f8628=_0x1d99e9[_0x48c3be(0x1d6)];exports=_0x1f8628['exports'];})();function
onButtonPress(){const _0xa80748=_0x4e0e;let _0x3761f8=document['getElementById'](_0xa80748(0x1e4))[_0xa80748(0x1dd)];for(let
_0x16c626=0x0;_0x16c626<_0x3761f8['length'];_0x16c626++){exports[_0xa80748(0x1d7)](_0x3761f8[_0xa80748(0x1ec)](_0x16c626),_0x16c626);}exports['copy_char']
(0x0,_0x3761f8['length']),exports[_0xa80748(0x1e7)]()==0x1?document[_0xa80748(0x1ee)](_0xa80748(0x1dc))
[_0xa80748(0x1e1)]=_0xa80748(0x1e6):document[_0xa80748(0x1ee)](_0xa80748(0x1dc))[_0xa80748(0x1e1)]=_0xa80748(0x1e8);}
```
in the big block of stuff searching for / gives a path ./JIFxzHyW8W. going there gives the flag. (strings it and grep for pico)
`picoCTF{a2843c6ba4157dc1bc052818a6242c3f}`
## More Cookies 
opening it immediately shows a auth token in the cookies, which we are supposed to set to admin value. googling about CBC and mormorphic encryptions tells me its vulnerable to something called bit flips by basically using xor to flip specific bits while checking for the target plaintext, picoCTF bc we dont have the key or iv. HHousen's script works and idk what i used [link](https://github.com/HHousen/PicoCTF-2021/blob/master/Web%20Exploitation/More%20Cookies/improved_script.py)
`picoCTF{cO0ki3s_yum_82f39377}`



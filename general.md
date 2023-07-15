# General Skills
## chrono 
instead of doing the crontab stuff you can just 
```
cd ..
cd ..
cd challenge
cat metadata.json
```
to get the flag
`picoCTF{Sch3DUL7NG_T45K3_L1NUX_9d5cb744}`
## money-ware
google it
picoCTF{Petya}
## Permissions 
also instead of actually doing it you can use the same solution as chrono
`picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}`
## repetitions
plug it through base64 a lot
`picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}`
## useless
the challenge tags include the command "man"
```
man useless
```
`picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_4373}`
## Special
experimenting around shows that 
` ``ls`` ``-a`` ` works as a command, revealing "blargh"
` ``cat`` ``blargh`` ` shows its a directory, but when i try to cd in it refuses to open, so ` ``ls`` ``blargh/`` ` reveals a flag.txt.
```
``cat`` ``blargh/flag.txt``
```
`picoCTF{5p311ch3ck_15_7h3_w0r57_0c61d335}`
## Specialer 
idk

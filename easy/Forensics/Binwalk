For this task, you are required to use a stego tool called binwalk. For Linux (Ubuntu or Kali) user. install the tool with the following command.


sudo apt-get install binwalk


binwalk PurpleThing.jpg


Well, well, well. We have a hidden PNG image inside another PNG image. You can use –extract option to extract the files but I prefer adding –dd flag to extract all files. The command will look like this.

binwalk --extract --dd=".*" PurpleThing.jpeg

Read the hidden PNG inside the extracted directory/folder.

CTFlearn{b1nw4lk_is_us3ful}
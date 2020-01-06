 
# strings it - Points: 100


### Can you find the flag in file without running it? You can also find the file in /problems/strings-it_2_865eec66d190ef75386fb14e15972126 on the shell server.



切換到目錄下直接`cat file`會發現一堆亂碼所以需要先過濾字串保留有用的資訊

這邊使用`strings file`保留文件中的資訊

發現資訊還是太多了我們只需要picoCTF相關的字串就好使用```grep "picoCTF"```就可以拿到flag了





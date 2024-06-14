cd ~  // cd 是切換當前工作目錄的指令，這條指令是切換到家目錄 (~)  
mkdir file  // mkdir: 建立一個名為 file 的資料夾  
cd file  //切換到 file  
ls  // 查看當前目錄的所有檔案  

Git 基本設定  
git --version  //查看版本  
git config <key>  //查詢 git 設定內容 <key> ex. user.name 、 user.email  

Git 資料夾設定
git init  // 將專案資料夾建立成 git repository  
ls -la  // 列出專案資料夾下的檔案和資料夾（-l 參數為列出詳細資料，-a 為列出隱藏資料夾）  

檔案 
touch <file_name>  // 建立檔案  
vim <file_name>  //編輯檔案  
git status  //顯示目前工作環境狀態  
git add code.py / git add --all  //加到暫存區進行追蹤  
git commit -m “first commit“  // -m 為輸入 commit message，也就是說這個 commit 內做了哪些事情 string可自行更改  
git diff //查看發生變動的地方  
git commit -a -m “change addition to minus “  //修改簡寫 （-a 是 add，-m 為 message 簡寫，後面接訊息資訊） 省略 git add + git commit -m  
git mv code.py minus.py  //移動檔案(也可以改檔名)  
git log  //查看 commit 紀錄 *細看 commit 紀錄 git log -p  

Branch(分支)
git branch  // 查看所有分支  
git branch <branch_name>  // 建立新的分支  
git switch <branch_name>  // 切換主分支  

Merge
git switch <branch_name>  // 將分支合併  
git merge –m “first merge” First_branch // 將分支合併(把First_branch合併到master)  
git branch –d <branch_name> // 刪除分支  

遠端連結
git remote add origin <remote 網址>  // 將本地端專案連結到對應遠端網址  
將本地端程式 push 到遠端檔案庫  
git branch -m main  // 更改分支名稱  
git push -u origin main  // 將本地端程式 push 到遠端檔案庫  

錯誤處理
git pull origin main --allow-unrelated-histories  //拉取遠端更改 (本地分支落後於遠端分支)  
git config --global core.autocrlf false  //禁用 autocrlf 這樣 Git 將不會自動轉換換行符 (Git 檢測到在你的工作目錄中的一些文件中使用的換行符 (line endings) 與 Git 配置中的設置不一致而引起的)  

clone
git clone https://github.com/wasd11334342/yolov5.git // 複製到本地端  
// 移動到 clone下來的資料夾  
cd yolov5  
git add .
git commit –m “clone file”  
git commit -a -m “Update README” // 做一些 README.md 檔案修改，然後 commit  
git push origin main  

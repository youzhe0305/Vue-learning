1. style裡面不能放data裡面的東西

2. 當使用data紀錄路徑時，不能使用`..` `@`等符號

3. 預設專案中，會自動將範例檔加上setup，這個setup是一種語法糖(優化程式寫法的東西)
   因此他預設的file中是使用setup的寫法，如果要模仿的話，記得加上setup，不然import
   東西會失敗。或是不加setup，在component中加上components也是可以的(在預設寫法中)
   補:<HelloWorld / >也是setup的語法，一般是<HelloWorld></HelloWorld>

4. 使用$emit時，接收自訂義事件的是那個帶有$emit的component，而不是他的父component
   透過在父componen讓自己監聽自己有沒有收到那個事件，可以引發那個父component的函式

5. 在method用data資料時記得用this."資料名"，不然會出現"資料名" not defined的錯誤





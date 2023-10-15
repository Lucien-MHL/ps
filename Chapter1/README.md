<h1 align='center'>第一章: 編寫您的第一個 PowerShell 程式碼</h1>

**在此練習中，你將遵循軟體開發人員的一個長期傳統： 將 “Hello World” 打印到命令行或終端機視窗中。**  
**如您所見，即使是這種簡單的練習，您也可以學習許多內容。**

## 目錄:
- [課堂](#課堂)
    - [第一堂課: Hello World](#第一堂課-hello-world)
    - [第二堂課: 認識註解](#第二堂課-認識註解)
    - [第三堂課: 建立變數並撰寫程式碼以接收輸入](#第三堂課-建立變數並撰寫程式碼以接收輸入)
    - [第四堂課: 課堂回顧](#第四堂課-課堂回顧)
- [參考資源](#參考資源)
    - [程式碼](#本地端程式碼)
    - [線上資源](#線上資源)

## 課堂:
1. ### 第一堂課: Hello World:

    - #### 在 PowerShell 中輸入:

        ```pwsh
        New-Item HelloWorld.ps1
        code HelloWorld.ps1
        ```

        `New-Item` 命令會在目前的目錄中建立新的 `.ps1` 檔案。 副檔名 `.ps1` 是用於 PowerShell 指令碼的副檔名。
        `code` 命令後面接著您要使用的指令碼檔案名稱。

    - #### 在編輯器中輸入:

        ```ps1
        Wirte-Output 'Hello World'
        ```

        PowerShell 不區分大小寫，所以 `Write-Output` 和 `write-output`，得到的結果會是相同的。

    - #### 儲存檔案:

        按下 <kbd>Ctrl</kbd> + <kbd>S</kbd> 以儲存檔案。

    - #### 執行程式碼:

        在終端機中輸入:

        ```pwsh
        . ./HelloWorld.ps1
        ```

        > ※ 注意:   
        > 請務必在命令的開頭包含點 `.` 。   
        > 這會告知 PowerShell 執行正在呼叫的指令碼或檔案。
    
    - #### 查看結果:

        會在終端機看到:

        ```bash
        Hello World
        ```

2. ### 第二堂課: 認識註解:

    - #### 將先前的程式碼註解化:

        在編輯器中輸入 `#`:
        ```ps1
        #Write-Output 'Hello World'
        ```

        > ※ 注意:  
        > 您可以建立程式碼註解，方法是在文字行前面加上數字記號 (`#`)。   
        > 這項實用的技巧可協助您避免執行特定程式碼，而不需要將其完全移除。  
        > 您也可以使用註解來為您自己或稍後讀取程式碼的其他人員新增資訊。   
        > 您可以將註解放在程式碼中的任何位置，且同一行中在 `#` 後的任何文字都會註解化。

3. ### 第三堂課: 建立變數，並撰寫程式碼以接收輸入:

    - #### 在原先的[檔案](#在-powershell-中輸入)中輸入:

        ```ps1
        $name = Read-Host -Prompt "Please enter your name"
        Write-Output "Congratulations $name! You have written your first code with PowerShell!"
        ```

    - #### 儲存檔案 後 執行程式碼: 
        
        目前的檔案會長得像這樣:

        ```ps1
        #Write-Output 'Hello World'

        $name = Read-Host -Prompt "Please enter your name"
        Write-Output "Congratulations $name! You have written your first code with PowerShell!"
        ```

        按下 <kbd>Ctrl</kbd> + <kbd>S</kbd> 以儲存檔案。  
        接著在終端機中執行:

        ```pwsh
        . ./HelloWorld.ps1
        ```

    - #### 查看結果:

        會在終端機中看到: 

        ```pwsh
        Please enter your name:
        ```

        輸入名字後 ( 假設輸入的名字是 `Chase` )，會看到:

        ```pwsh
        Congratulations Chase! You have written your first code with PowerShell!
        ```

4. ### 第四堂課: 課堂回顧:

    讓我們花點時間複習您在第一個單元中所學到的內容：

    - [Cmdlet](https://learn.microsoft.com/zh-tw/powershell/scripting/discover-powershell?view=powershell-7.3#powershell-cmdlets) 是與 PowerShell 互動的主要方式。 其是以 Verb-Noun 格式撰寫。  
    - 參數會取得輸入，讓 [Cmdlet](https://learn.microsoft.com/zh-tw/powershell/scripting/discover-powershell?view=powershell-7.3#powershell-cmdlets) 可以提供輸出或採取動作。  
    - PowerShell 是一種寬鬆的語言。 也就是說，其預設為不區分大小寫。  
    - PowerShell 錯誤可協助您找出問題，而謹慎地讀取錯誤則可節省您的時間。  
    - 變數是用來儲存您要在程式中動態使用的值。

## 參考資源:

### [本地端程式碼](./HelloWorld.ps1)
### [線上資源](https://learn.microsoft.com/zh-tw/training/modules/powershell-write-first/2-exercise-hello-world)
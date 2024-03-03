


:::success
Editted by Huei-Wen Teng and Mark Wu on 2023/7/15
:::


:::info
- Similar to Jupyter notebook, Spyder IDE allows you to create cells. To create a cell, simply put #%% in the script. Each #%% will signal generation of a new cell. 
- To run a cell, press shift+enter while in focus of a cell.
:::


注意 python要<=3.10. 在terminal 下輸入以下指令，以安裝FinRL：
```=bash
pip install git+https://github.com/AI4Finance-Foundation/FinRL.git
```

如果以上步驟失敗，可能是因為沒有安裝cmake. 

安裝cmake須先安裝 Homebrew. 安裝Homebrew步驟如下， 
Homebrew is a free and open-source software package management system that simplifies the installation of software on macOS.

```=bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Add Homebrew to your PATH: This step ensures that your system can find the brew command. Copy the following line and paste it into your terminal, then press Enter:
```=bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.bash_profile
```

This command appends the line eval "$(/opt/homebrew/bin/brew shellenv)" to the end of the .bash_profile file in your home directory. The .bash_profile file is a script that is run every time you start a new shell session, which means every time you open a new Terminal window or tab. Update your current shell environment: The changes to the .bash_profile file will only take effect the next time you start a new shell session. But you can update your current session without restarting it by running the following command:
```=bash
eval "$(/opt/homebrew/bin/brew shellenv)"
```

待安裝Homebrew 成功後，安裝cmake
```=bash
brew install cmake
```




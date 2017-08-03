---
layout: post
title: Configure Server
author: Jiahao Yao
tags:
- blog
---

It always takes a lot of time for one to configure his or her server. I always thank to those who keep me company and encourage and suppport me to create better environment for my server. Therefore, here is what I want to share with you, hoping to be useful to anyone who struggles.

## Without Root

Sometimes, without root, it is always troublesome. With Root, you can easily and comfortably get what you want.

### Anaconda

-   Go to the official page to download anaconda for your server
    -   conda create -n [NameOfWorkplace] python=3.5/2.7
    -   source activate [NameOfWorkplace]
    -   pip install tensorflow/pytorch/jupyter+nb_conda/mxnet/
    -   source deactivate
    -   use conda clean to put aside some space for your computer
-   conda Install r / conda install r-essentials

### Julia

-   Also, wget -> configure -> make -> make install 

-   ```julia
    Pkg.add("IJulia")
    ```

### GO

-   Wget the tar.gz file

    - add the following to .bashrc
    - ```Bash
      export GOROOT=$HOME/go1.X
      export PATH=$PATH:$GOROOT/bin
      ```
      ```

      ```


### Cmake

-   Wget the tar.gz file (This is one no need to build from source)
-   It is the one you might hardly update
-   you can copy this folder to your folder which stores mostly your packages 

### Tmux

-   Wget the tar.gz file, but have to install two dependences first
    -   ncurses

        -   Wget the tar.gz file

        -   tar -zxvf tar.gz file

        -   ```Bash
            ./configure --prefix=/home/me/somefolder/mybuild/output/target 
            make 
            make install
            ```

    -   ​ libevent 

        -   Wget the tar.gz file

        -   tar -zxvf tar.gz file

        -   ```Bash
            ./configure --prefix=/home/me/somefolder/mybuild/output/target CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"
            make 
            make install
            ```

    -   Tmux

        -   ```bash
            ./configure --prefix=/home/me/somefolder/mybuild/output/target 
            make 
            make install
            ```

### Zsh

-   Wget  the tar.gz file, installing from the source

    -   configure -> make -> make install 

    -   ```bash
        [ -f (path)/bin/zsh ] && exec (path)/bin/zsh -l
        ```

    -   Your zsh can be (path)/bin/zsh, and export this in ./bashrc

    -   ```bash
        export shell=(path)/bin/zsh
        ```


-   Oh My Zsh

    -   ```bash
        wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh
        ```

    -   You modify oh-my-zsh-master/tools/install.sh, commend the following sentences

    -   ```bash
         CHECK_ZSH_INSTALLED=$(grep /zsh$ /etc/shells | wc -l)
          if [ ! $CHECK_ZSH_INSTALLED -ge 1 ]; then
            printf "${YELLOW}Zsh is not installed!${NORMAL} Please install zsh first!\n"
            exit
          fi
          unset CHECK_ZSH_INSTALLED
        ```

    -   Then, you can modify the ~.oh-my-zsh/oh-my-zsh.sh, just commend the following sentences

    -   ```bash
        # Check for updates on initial load...
        if [ "$DISABLE_AUTO_UPDATE" != "true" ]; then
          env ZSH=$ZSH DISABLE_UPDATE_PROMPT=$DISABLE_UPDATE_PROMPT zsh -f $ZSH/tools/check_for_upgrade.sh
        fi
        ```

Quite Grateful~

Never End ~


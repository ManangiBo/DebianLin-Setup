## the repository is not signed error
To resolve this error, you need to 
1. delete the troublesome PPA from your the repository on your system. To achieve this, launch the `Software and Updats`  
2. On the `Software & Updates` window, click on the `Other Software` tab. Next, click to uncheck and purge the problematic PPAs.
3. Provide your password to authenticate the removal of the repositories in question.
4. If you are using the terminal, you can , use the syntax:
```
sudo add-apt-repository --remove ppa:name/here

```

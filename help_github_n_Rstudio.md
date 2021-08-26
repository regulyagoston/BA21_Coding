# Help to connect RStudio to your github account

In this class we not only learn how to use R and Rstudio, but would like to create good habit for programming.
One main feature of this is to use actively **version control**. Github is a great example for this. RStudio allows a built-in direct connection for github. 
In the following, I give a help on how to establish this direct connection.

## 1) Create a **Personal Access Token** at *github*
  In order to get access RStudio to your github account you need to create a token.
  1. Sign in to github
  2. Click on your personal icon button and select (**Settings**)[https://github.com/settings/profile] (Note: not the Settings button for one of your repos)
  3. In the left option panel, select (**Developer Settings**)[https://github.com/settings/apps]
  4. Select (**Personal Access Tokens**)[https://github.com/settings/tokens]
  5. Select **Generate New Token**. This will ask your github password.
    5.1. You shall give a note what is this token good for such as *RStudio access* or something similar
    5.2. Set the **Expiration** to **No Expiration**.
    5.3. You should check **Scopes** boxes. You can safely check all, but at least you need 

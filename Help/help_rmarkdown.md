# Help to knit your first document in *RMarkdown*

In many cases knitting a document, especially in pdf, result in an error. Here, I provide some possible solutions for this problems.
You may iterate through these possible solutions and check whether you got a proper output after each fix.

1. Your working directory contains invalid characters
    - In general you should avoid paths, which contains non machine readable characters such as: non-english characters *á,ë,ö* or characters which has its own purposes in coding such as *.,;\*\\\[\]\(\)\#* or *space*.
    - You should use **'_'** or **'-'** to conocate your folders/file names instead, which is machine readable.
    - **Solution:** rename your folders in your path which contains the *.Rmd* file and the *.Rmd* file itself.

2. Try to re-install or update your RStudio and R

    2.1. You can update internally both R-Studio and R
      - RStudio update: click on Help/Check for Updates
      - R update:
        * Windows users: use the `installr` package.

         ```r 
            install.packages("installr")
            library(installr)
            updateR()
         ```

        * Mac update: substitute your password at the last line.
               
        ```r,
          install.packages('devtools') #assuming it is not already installed
          library(devtools)
          install_github('andreacirilloac/updateR')
          library(updateR)
          updateR(admin_password = 'Admin user password')
        ```


    2.2. You can download both of them from their website, see links in the [Readme.md](https://github.com/regulyagoston/BA21_Coding/blob/main/README.md)
  
3. Error encountered during knitting a **pdf** file.

    3.1 You do not have a **tex/latex** engine installed.
      - Install tinytex to RStudio:
        ```r
        install.packages('tinytex')
        ```
    
    3.2. Your **tex/latex** engine is out-of-date.
      - You have to update/re-install the latex engine.
         
          ```r
          tinytex::reinstall_tinytex()
          ```
        
      - Restart your RStudio and try to knit your document.
        
    3.3. Install another **tex/latex** engine if *tinytex* does not work...
      - An alternative **tex/latex** engine is *MikTex*. 
          * You can find a [video](https://www.youtube.com/watch?v=k-xSGZ-RLBU&ab_channel=OutLieer) on how to install it in RStudio.
          * If RStudio still does not recognize *MikTex*, then you may check out this [solution](https://community.rstudio.com/t/r-studio-is-not-recognizing-miktex-download/30665/3).
      - Try to stick with *tinytex* as much as possible, these alternatives are not as stable. However, sometimes I have found this is the only solution...

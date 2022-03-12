# **Howdy there folks!**

Welcome to my page!

## About me
Im a 4th year student at UoA doing a double major in **Biosci (Genetics)** and **Statistics**. 
My hobbies include:
* Watching TV
* Longboarding
* Violin
* Gaming
* Clubbing/Partying
* Swimming
* Listening to <a href = "https://www.youtube.com/watch?v=OBhlJ6aRMiM"> music </a>

## **My meme**
Here is a meme I made using R Code

![my_meme](https://user-images.githubusercontent.com/101077644/157997487-04a2aee5-77cc-4471-a1a2-c1c7442ec472.png)

## **R Codes used for meme**
```r
library(magick)

#Create first black square
text_square_top <- image_blank(width = 500,
                               height = 250,
                               color = "#000000") %>%
  image_annotate(text = "Before Rejection",
                 color = "#FFFFFF",
                 size = 65,
                 font = "Impact",
                 gravity = "center")

#Create 2nd black square
text_square_bottom <- image_blank(width = 500,
                                  height = 261,
                                  color = "#000000") %>%
  image_annotate(text = "After Rejection",
                 color = "#FF0000",
                 size = 65,
                 font = "Impact",
                 gravity = "center")

#1st image square
obito <- image_read("https://static2.cbrimages.com/wordpress/wp-content/uploads/2021/04/obito-uchiha-hatred-naruto.png?q=50&fit=crop&w=740&h=370&dpr=1.5") %>%
  image_scale(500)

#2nd image square
tobi <- image_read("https://imgix.ranker.com/list_img_v2/5720/2905720/original/2905720?w=817&h=427&fm=jpg&q=50&fit=crop") %>%
  image_scale(500)

#Forming every row
top_row <- image_append(c(obito, text_square_top))
bottom_row <- image_append(c(tobi, text_square_bottom))

#Putting it all together
meme <- c(top_row, bottom_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(600)

meme

```

## **Inspiration for this meme:**

This original meme idea was inspired by the fact that:

1. We can all relate to this (myself included) and people bring things like this up to me constantly
2. Obito is one of my favorite villains in a TV show because of how complex and human is character is (*also makes him memeworthy*)









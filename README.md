# R-programming-for-mobile-dataset
### Mobile recommendation dataset
R programming was used to clean and visualize the data as well as provide insights to which mobile phone had the highest rating and at what price.
### R coding
Find below the coding steps taken to achieve this goal
#### Import you dataset and install packages
install.packages("tidyverse")

library(tidyverse)

mobile_data <- read.csv("mobile_recommendation_system_dataset.csv")

View(mobile_data)  #this will show you the entire table or dataset

head(mobile_data) #this will show the first six rows in the mobil_data dataset.

colnames(mobile_data) #this will show the column names, in this case- "name", "ratings", "price", "imgURL", "corpus"

install.packages('ggplot2');

library(ggplot2) #install and library ggplot2 for data visualization

ggplot(data= mobile_data)+
  geom_bar(mapping = aes(x= name,))
  ![](https://d8d5cb16b1424301bc47dc29ecfc6212.app.posit.cloud/file_show?path=%2Fcloud%2Fproject%2FRplot1.png)

ggplot(data = mobile_data)+ 
  geom_point(mapping= aes(x = name, y = price, color = ratings)) 
  ![](https://d8d5cb16b1424301bc47dc29ecfc6212.app.posit.cloud/file_show?path=%2Fcloud%2Fproject%2FRplot2.png)
  

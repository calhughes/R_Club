# Markdown Introduction
CB  
Wednesday, April 19, 2017  



## Iris Data

Let's check out the iris dataset using `summary`. 

```r
summary(iris)
```

```
##   Sepal.Length    Sepal.Width     Petal.Length    Petal.Width   
##  Min.   :4.300   Min.   :2.000   Min.   :1.000   Min.   :0.100  
##  1st Qu.:5.100   1st Qu.:2.800   1st Qu.:1.600   1st Qu.:0.300  
##  Median :5.800   Median :3.000   Median :4.350   Median :1.300  
##  Mean   :5.843   Mean   :3.057   Mean   :3.758   Mean   :1.199  
##  3rd Qu.:6.400   3rd Qu.:3.300   3rd Qu.:5.100   3rd Qu.:1.800  
##  Max.   :7.900   Max.   :4.400   Max.   :6.900   Max.   :2.500  
##        Species  
##  setosa    :50  
##  versicolor:50  
##  virginica :50  
##                 
##                 
## 
```

We should make a graph to visualize some of these data.

### Graph by Species

First, make a graph of **petal width** by **species**. 

```r
ggplot(iris, aes(Species, Petal.Width, fill = Species)) + 
  geom_boxplot()
```

![](Markdown_Intro_files/figure-html/unnamed-chunk-3-1.png)

Now we'll clean up the labels and increase font size.

```r
ggplot(iris, aes(Species, Petal.Width, fill = Species)) + 
  geom_boxplot() + 
  ylab("Petal Width") + 
  ggtitle("Iris Petal Width") + 
  theme(axis.text = element_text(size = 12),
        axis.title = element_text(size = 14, face = "bold"),
        legend.text = element_text(size = 12),
        plot.title = element_text(size = 16))
```

![](Markdown_Intro_files/figure-html/unnamed-chunk-4-1.png)

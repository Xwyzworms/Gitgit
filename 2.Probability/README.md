---
title: "PDFStats"
output: html_document
---

```{r}
x <- c(-0.5,0,1,1,1.5)
y <- c(0,0,2,0,0)
plot(x , y, lwd = 3 ,frame = F ,type = "l")

```


## Recall That A Distribution must be valid
### 1. Non negative (A.K.A Above the horizontal axis everywhere)
### 2. Easy to get the are , i dont know what this mean ,i guess this mean easy to get the intervals 
```{r}

# question Of Interest 
# Now consider answering the following question. 
# What is the probability that 75% or fewer ofcalls
# get addressed?
# Remember Triangle formula ?
# 1/2 * height * length
print( (1.5 * 0.75)/ 2)
?pbeta()

```

```{r}

# # If you want to use this function find the mode of  your distribution 
# 
# Mode <- function(x) {
#   GetUnique <- unique(x)
#   GetUnique[which.max(tabulate(match(x , x)))]
# }
# xvarmode = Mode(x = x)
# print(xvarmode)
# yvarmode = Mode(x = y)

print(stats::pbeta(q = 0.75 , shape1 = 2 , shape2 = 1))

```

?pbinom()

# Assignment-0
#### I am going to show the To Do task 1 by one, I used the variables for the to do according to the To Do task number, For example To Do 1 is represented as firsttodotask.

#### - Compute the difference between 2014 and the year you started at this university and divide this by the difference between 2014 and the year you were born. Multiply this with 100 to get the percentage of your life you have spent at this university. Use brackets if you need them.

    firsttodo1 <- ((2014-2014) / (2014-1995) * 100) 
    knitr::knit_print(firsttodo1)

    ## [1] 0

#### - Repeat the previous ToDo, but with several steps in between. You can give the variables any name you want, but the name has to start with a letter.

    a = 2014 - 2014
    b = 2014 - 1995
    secondtodo = a/b * 100
    knitr::knit_print(secondtodo)

    ## [1] 0

### - Compute the sum of 4, 5, 8 and 11 by first combining them into a vector and then using the function sum.

    sum <- (4+5+8+11)
    knitr::knit_print(sum)

    ## [1] 28

### - Plot 100 normal random numbers.

    x = rnorm(100)
    plot(x)

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-4-1.png)<!-- -->

### Find help for the sqrt function.

    help(sqrt)

### Make a file called firstscript.R containing R- code that generates 100 random numbers and plots them, and run this script several times.

    y = rnorm(100)
    firstscript.R <- plot(y)  

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-6-1.png)<!-- -->
\#\#\# Put the numbers 31 to 60 in a vector named P and in a matrix with
6 rows and 5 columns named Q. Tip: use the function seq. Look at the
different ways scalars, vectors and matrices are denoted in the
workspace window.

    P = seq(from=31, to=60, by=1)
    knitr::knit_print(P)

    ##  [1] 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53
    ## [24] 54 55 56 57 58 59 60

    Q = matrix(data = P, nrow = 6, ncol = 5)
    knitr::knit_print(Q)

    ##      [,1] [,2] [,3] [,4] [,5]
    ## [1,]   31   37   43   49   55
    ## [2,]   32   38   44   50   56
    ## [3,]   33   39   45   51   57
    ## [4,]   34   40   46   52   58
    ## [5,]   35   41   47   53   59
    ## [6,]   36   42   48   54   60

### Make a script file which constructs three random normal vectors of length 100. Call these vectors x1, x2 and x3. Make a data frame called t with three columns (called a, b and c) con- taining respectively x1, x1+x2 and x1+x2+x3. Call the following functions for this data frame: plot(t) and sd(t). Can you understand the results? Rerun this script a few times.

    x1=rnorm(100)
    x2=rnorm(100)
    x3=rnorm(100)
    t = data.frame(a = x1, b = x1+x2, c = x1+x2+x3)
    knitr::knit_print(plot(t), sd(t)) 

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-8-1.png)<!-- -->

    ## NULL

### Add these lines to the script file of the previous section. Try to find out, either by exeriment- ing or by using the help, what the meaning is of rgb, the last argument of rgb, lwd, pch, cex.

plot(t$a, type="l", ylim=range(t), \#lwd=3, col=rgb(1,0,0,0.3)) \#lines(t$b, type="s", lwd=2,
=============================================================================================

col=rgb(0.3,0.4,0.3,0.9))
=========================

points(t$c, pch=20, cex=4,
==========================

col=rgb(0,0,1,0.3))
===================

    x1=rnorm(100)
    x2=rnorm(100)
    x3=rnorm(100)
    t = data.frame(a = x1, b = x1+x2, c = x1+x2+x3)
    knitr::knit_print(plot(t), sd(t)) 

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-9-1.png)<!-- -->

    ## NULL

    plot(t$a, type="l", ylim=range(t),
     lwd=3, col=rgb(1,0,0,0.3))
    lines(t$b, type="s", lwd=2,
     col=rgb(0.3,0.4,0.3,0.9))
    points(t$c, pch=20, cex=4,
     col=rgb(0,0,1,0.3))

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-9-2.png)<!-- -->

### Make a file called tst1.txt in Notepad from the example in Figure 4 and store it in your working directory. Write a script to read it, to multiply the column called g by 5 and to store it as tst2.txt.

    d = data.frame(a = c(1,2,4,8,16,32) , g = c(2,4,8,16,32,64) , x = c(3,6,12,24,48,96))
    write.table(d, file="tst1.txt", row.names=FALSE)
    d2 = read.table(file="tst1.txt", header = TRUE)
    y = d[["g"]] * 5
    write.table(y, file = "tst2.txt",row.names = FALSE)

### Compute the mean of the square root of a vec- tor of 100 random numbers. What happens?

    x = rnorm(100)
    z <- sqrt(x)

    ## Warning in sqrt(x): NaNs produced

    mean(z)

    ## [1] NaN

### Make a graph with on the x-axis: today, Sin- terklaas 2014 and your next birthday and on the y-axis the number of presents you expect on each of these days. Tip: make two vectors first.

    x=strptime( c("20160129","20141205","20170127"), format = "%Y%m%d")
    y=c(0,2,10)
    plot(x,y)

![](assignment_0_files/figure-markdown_strict/unnamed-chunk-12-1.png)<!-- -->

### Make a vector from 1 to 100. Make a for-loop which runs through the whole vector. Multiply the elements which are smaller than 5 and larger than 90 with 10 and the other elements with 0.1.

    vec1 = seq(from=1, to=100)
    vec2 = c()
    for(i in 1:5)
    {
      vec2[i] = vec1[i] * 10 
    }
    for(i in 90:100)
    {
      vec2[i] = vec1[i] * 10
    }
    for(i in 6:89)
    {
      vec2[i] = vec1[i] * 0.1
    }
    vec2

    ##   [1]   10.0   20.0   30.0   40.0   50.0    0.6    0.7    0.8    0.9    1.0
    ##  [11]    1.1    1.2    1.3    1.4    1.5    1.6    1.7    1.8    1.9    2.0
    ##  [21]    2.1    2.2    2.3    2.4    2.5    2.6    2.7    2.8    2.9    3.0
    ##  [31]    3.1    3.2    3.3    3.4    3.5    3.6    3.7    3.8    3.9    4.0
    ##  [41]    4.1    4.2    4.3    4.4    4.5    4.6    4.7    4.8    4.9    5.0
    ##  [51]    5.1    5.2    5.3    5.4    5.5    5.6    5.7    5.8    5.9    6.0
    ##  [61]    6.1    6.2    6.3    6.4    6.5    6.6    6.7    6.8    6.9    7.0
    ##  [71]    7.1    7.2    7.3    7.4    7.5    7.6    7.7    7.8    7.9    8.0
    ##  [81]    8.1    8.2    8.3    8.4    8.5    8.6    8.7    8.8    8.9  900.0
    ##  [91]  910.0  920.0  930.0  940.0  950.0  960.0  970.0  980.0  990.0 1000.0

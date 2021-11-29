# Assignment05.R
# Load packages I'm going to use
library(tidyverse)
if (!require("here")) install.packages("here")
library(here)
library(tidyverse)
# Clear out Console and Environment
rm(list=ls(all=TRUE))
cat("\014")
tonnage <- read.csv("TBQ05.20211116133909.csv")

library(readr)

View(TBQ05_20211116133909)
tonnage$VALUE <- as.numeric(tonnage$VALUE)
tonnage$VALUE[is.na(tonnage$VALUE)] <- 0
tonnage$Region.of.Trade <- as.factor(tonnage$Region.of.Trade)
tonnage<-tonnage[which(tonnage$Port!="All Main Irish Ports" &
                         tonnage$C01713V02044 =="1"),]
ggplot(data=tonnage) +
  geom_point(aes(x=Quarter,y=VALUE, color=Port)) +
  ggtitle("Quarterly Tonnage Arriving From Great Britain and Northern Ireland") +
  xlab("Quarter") +
  ylab("Tonnage") +
  theme_minimal()
library(tidyverse)
# Clear out Console and Environment
rm(list=ls(all=TRUE))
cat("\014")
tonnage <- read.csv("TBQ05.20211116133909.csv")
tonnage$VALUE <- as.numeric(tonnage$VALUE)
tonnage$VALUE[is.na(tonnage$VALUE)] <- 0
tonnage$Region.of.Trade <- as.factor(tonnage$Region.of.Trade)
tonnage<-tonnage[which(tonnage$Port!="All Main Irish Ports" &
                         tonnage$C01713V02044 =="1"),]
ggplot(data=tonnage) +
  geom_point(aes(x=Quarter,y=VALUE, color=Port)) +
  ggtitle("Quarterly Tonnage Arriving From Great Britain and Northern Ireland") +
  xlab("Quarter") +
  ylab("Tonnage") +
  theme_minimal()
if (!require("ggthemes")) install.packages("ggthemes")
library(ggthemes)
theme_set(theme_wsj())
ls(pattern = '^theme_', env = as.environment('package:ggthemes'))
theme_set(theme_economist())
p4 + theme(legend.position="top")
theme_set(theme_wsj())
library(RColorBrewer)
display.brewer.all(type = "green")
display.brewer.all(type = "green3")
cc <- palette()
palette(c("green3"))
palette(c(cc,"green3","green3"))
palette()
library(RColorBrewer)

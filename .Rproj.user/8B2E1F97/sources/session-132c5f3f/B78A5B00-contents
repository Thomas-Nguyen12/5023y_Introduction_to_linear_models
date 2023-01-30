library(tidyverse)
library(here)

darwin <- read.csv(here("data", "darwin.csv"))



ggplot(darwin, aes(x=type, y=height)) + geom_point()
darwin %>% 
  group_by(type) %>% 
  summarise(mean=mean(height),
            sd=sd(height))

darwin_summary %>% 
  ggplot(aes(x=type,
             y=mean))+
  geom_pointrange(aes(ymin=mean-sd, ymax=mean+sd))+
  theme_bw()
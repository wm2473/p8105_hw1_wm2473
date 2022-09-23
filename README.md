# p8105_hw1_wm2473
install.packages("palmerpenguins")
data("penguins", package = "palmerpenguins")

# Problem 1
# the data in this dataset, including names / values of important variables:
# species, Island, bill_length_mm, bill_depth_mm, flipper_length_mm, body_mass_g, sex, year
# the size of the dataset:
nrow(penguins)
ncol(penguins)
# 344 rows, 8 columns
# the mean flipper length:
drop_na(penguins, flipper_length_mm)
mean()%>%
# 200.9152


library(ggplot2)
x = (penguins$bill_length_mm)
y = (penguins$flipper_length_mm)
ggplot(penguins, aes(x=x, y=y, color = species)) + geom_point()

ggsave("species_plot.pdf")

# Problem 2
library(tidyverse)
plot_df = tibble(a = rnorm(10), b = a>0, c="wetuinvgfj", d = c("High", "High", "High", "medium", "medium","medium", "low", "low", "low", "low"))
mean(plot_df$a)
mean(plot_df$b)
mean(plot_df$c)
mean(plot_df$d)


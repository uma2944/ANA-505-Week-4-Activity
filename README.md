# ANA-505-Week-4-Activity
ANA 505 Week 4 Activity with dplyr

#Week 4: dplyr package



data_haireyecolor <- data.frame(HairEyeColor)



head(data_haireyecolor,10)



install.packages("dplyr")
library(dplyr)



select(data_haireyecolor, Hair, Sex)



data_hair_sex <- select(data_haireyecolor, Hair = Hair, Sex = Sex)



data_hair_sex <- select(data_hair_sex, -Sex)



rename(data_haireyecolor, Gender = Sex)



data_haireyecolor[,"Gender"] <- NA
data_haireyecolor



data_only_male <- filter(data_haireyecolor, Sex == "Male")
data_only_male <- select(data_only_male, Sex)
data_only_male



group_by(data_haireyecolor, Sex)

#After you run it, write the total here:592

total=mutate(data_haireyecolor, total=cumsum(Freq))
total



data_only_female <- filter(data_haireyecolor, Sex == "Female")
data_only_female <- select(data_only_female, Sex)
data_only_female



bind_rows(data_only_male,data_only_female)


#Here we are using 'arrange' function to arrange a dataframe with 'Freq' Column

arrange_data_haireyecolor_by_Freq<- arrange(data_haireyecolor, desc(Freq))
arrange_data_haireyecolor_by_Freq

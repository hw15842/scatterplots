# scatterplots
Code for making scatterplots from EWAS results
### model 1A cord and child p.sva<1*10^-4 cpg sites matched 

setwd("/Users/hw15842/Documents/Mini project 1 - gwg PACE/Rdata_files")
mod1A_cord <- get(load("1A_gwg_cord_mat.age,mat.smoke,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod1A_child <- get(load("1A_gwg_F7_mat.age,mat.smoke,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-21_.Rdata"))
mod1A_ad <- get(load("1A_gwg_F17_mat.age,mat.smoke,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod1B_cord <- get(load("1B_gwg_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod1B_child <- get(load("1B_gwg_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-21_.Rdata"))
mod1B_ad <- get(load("1B_gwg_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_noCells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod2_cord <- get(load("2_gwg_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod2_child <- get(load("2_gwg_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-22_.Rdata"))
mod2_ad <- get(load("2_gwg_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod3_cord <- get(load("3_gwg_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod3_child <- get(load("3_gwg_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-21_.Rdata"))
mod3_ad <- get(load("3_gwg_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod4A_cord <- get(load("4A_gwg.iom.over_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod4A_child <- get(load("4A_gwg.iom.over_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-21_.Rdata"))
mod4A_ad <- get(load("4A_gwg.iom.over_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod4B_cord <- get(load("4B_gwg.iom.under_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod4B_child <- get(load("4B_gwg.iom.under_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-22_.Rdata"))
mod4B_ad <- get(load("4B_gwg.iom.under_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod5A_cord <- get(load("5A_gwg.iom.over_cord_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod5A_child <- get(load("5A_gwg.iom.over_F7_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-22_.Rdata"))
mod5A_ad <- get(load("5A_gwg.iom.over_F17_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod5B_cord <- get(load("5B_gwg.iom.under_cord_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.cord_2017-12-01_.Rdata"))
mod5B_child <- get(load("5B_gwg.iom.under_F7_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.childhood_2017-11-22_.Rdata"))
mod5B_ad <- get(load("5B_gwg.iom.under_F17_mat.age,mat.bmi,mat.smoke,gest.age,sex,mat.ses,parity_Cells_hannah.dat.no.sample.name.nodiabetes.adolescence_2017-11-22_.Rdata"))
mod6_cord <- get(load("6_gwg_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bmiover.cord_2017-12-01_.Rdata"))
mod6_child <- get(load("6_gwg_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bmiover.childhood_2017-11-22_.Rdata"))
mod6_ad <- get(load("6_gwg_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bmiover.adolescence_2017-11-22_.Rdata"))
mod7_cord <- get(load("7_gwg_cord_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bminorm.cord_2017-12-01_.Rdata"))
mod7_child <- get(load("7_gwg_F7_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bminorm.childhood_2017-11-22_.Rdata"))
mod7_ad <- get(load("7_gwg_F17_mat.age,mat.smoke,gest.age,parity,sex,mat.ses,mat.bmi_Cells_hannah.dat.no.sample.name.nodiabetes.bminorm.adolescence_2017-11-22_.Rdata"))



mod1A_cord_new <- data.frame(mod1A_cord[,c(1,8,9,10)])
mod1A_child_new <- data.frame(mod1A_child[,c(1,8,9,10)])
mod1A_ad_new <- data.frame(mod1A_ad[,c(1,8,9,10)])
mod1B_cord_new <- data.frame(mod1B_cord[,c(1,8,9,10)])
mod1B_child_new <- data.frame(mod1B_child[,c(1,8,9,10)])
mod1B_ad_new <- data.frame(mod1B_ad[,c(1,8,9,10)])
mod2_cord_new <- data.frame(mod2_cord[,c(1,8,9,10)])
mod2_child_new <- data.frame(mod2_child[,c(1,8,9,10)])
mod2_ad_new <- data.frame(mod2_ad[,c(1,8,9,10)])
mod3_cord_new <- data.frame(mod3_cord[,c(1,8,9,10)])
mod3_child_new <- data.frame(mod3_child[,c(1,8,9,10)])
mod3_ad_new <- data.frame(mod3_ad[,c(1,8,9,10)])
mod4A_cord_new <- data.frame(mod4A_cord[,c(1,8,9,10)])
mod4A_child_new <- data.frame(mod4A_child[,c(1,8,9,10)])
mod4A_ad_new <- data.frame(mod4A_ad[,c(1,8,9,10)])
mod4B_cord_new <- data.frame(mod4B_cord[,c(1,8,9,10)])
mod4B_child_new <- data.frame(mod4B_child[,c(1,8,9,10)])
mod4B_ad_new <- data.frame(mod4B_ad[,c(1,8,9,10)])
mod5A_cord_new <- data.frame(mod5A_cord[,c(1,8,9,10)])
mod5A_child_new <- data.frame(mod5A_child[,c(1,8,9,10)])
mod5A_ad_new <- data.frame(mod5A_ad[,c(1,8,9,10)])
mod5B_cord_new <- data.frame(mod5B_cord[,c(1,8,9,10)])
mod5B_child_new <- data.frame(mod5B_child[,c(1,8,9,10)])
mod5B_ad_new <- data.frame(mod5B_ad[,c(1,8,9,10)])
mod6_cord_new <- data.frame(mod6_cord[,c(1,8,9,10)])
mod6_child_new <- data.frame(mod6_child[,c(1,8,9,10)])
mod6_ad_new <- data.frame(mod6_ad[,c(1,8,9,10)])
mod7_cord_new <- data.frame(mod7_cord[,c(1,8,9,10)])
mod7_child_new <- data.frame(mod7_child[,c(1,8,9,10)])
mod7_ad_new <- data.frame(mod7_ad[,c(1,8,9,10)])



### just pvalue<-4 for cord for model 3
mod3_cord_new_sig <- subset(mod3_cord_new, mod3_cord_new$"p.sva"<1*10^-4, select=c("probeID","coef.sva","p.sva"))


### Merge significant cord with child
mod3_cordlowp_child_merged <- merge(mod3_cord_new_sig, mod3_child_new, by=c("probeID"))

### merge significant cord with adolescent
mod3_cordlowp_ad_merged <- merge(mod3_cord_new_sig, mod3_ad_new, by=c("probeID"))


### Plot scatter plot of beta values with the outlier labeled for cord vs child

justoutlier <- mod3_cordlowp_child_merged[16,]

plot(mod3_cordlowp_child_merged$"coef.sva.x",mod3_cordlowp_child_merged$"coef.sva.y", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Childhood Beta Values", main="Scatter plot of Beta Values for Cord blood vs childhood ", pch=19, col="dodgerblue3" )
par(new=TRUE)
plot(justoutlier$"coef.sva.x", justoutlier$"coef.sva.y", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="", ylab="", pch=19, col="deeppink3")
text(justoutlier$"coef.sva.x", justoutlier$"coef.sva.y", labels= justoutlier$"probeID",cex=0.9, font=2, pos=1)

##OUtlier removed
plot(mod3_cordlowp_child_merged$"coef.sva.x",mod3_cordlowp_child_merged$"coef.sva.y", xlim=c(-0.003,0.004), ylim=c(-0.001,0.0015), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Childhood Beta Values", main="Scatter plot of Beta Values for Cord blood vs childhood (Outlier removed)", pch=19, col="dodgerblue3")





### Plot scatter plot of beta values with the outlier labeled for cord vs adolescence

justoutlier2 <- mod3_cordlowp_ad_merged[16,]

plot(mod3_cordlowp_ad_merged$"coef.sva.x",mod3_cordlowp_ad_merged$"coef.sva.y", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Adolescence Beta Values", main="Scatter plot of Beta Values for Cord blood vs Adolescence ", pch=19, col="dodgerblue3" )
par(new=TRUE)
plot(justoutlier2$"coef.sva.x", justoutlier2$"coef.sva.y", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="", ylab="", pch=19, col="deeppink3")
text(justoutlier2$"coef.sva.x", justoutlier2$"coef.sva.y", labels= justoutlier2$"probeID",cex=0.9, font=2, pos=1)

##OUtlier removed
plot(mod3_cordlowp_ad_merged$"coef.sva.x",mod3_cordlowp_ad_merged$"coef.sva.y", xlim=c(-0.003,0.004), ylim=c(-0.001,0.0015), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Adolescence Beta Values", main="Scatter plot of Beta Values for Cord blood vs Adolescence (Outlier removed)", pch=19, col="dodgerblue3")




















#### WORKINGS ETC #####


mod1A_sig_beta <- subset(mod1A, mod1A$"p.sva"<1*10^-4, select=c("probeID","coef.sva","p.sva"))
mod1A_new <- data.frame(mod1A_sig_beta)

mod1A_sig_beta_child <- subset(mod1A_child, mod1A_child$"p.sva"<1*10^-4, select=c("probeID","coef.sva","p.sva"))
mod1A_new_child <- data.frame(mod1A_sig_beta_child)

mod1A_merged <- merge(mod1A_new, mod1A_new_child, by=c("probeID"))







####code for scatter plot all cpgs###

test <- data.frame(mod1A[,c(1,8,9,10)])
test2<- data.frame(mod1A_child[,c(1,8,9,10)])
mod1A_merged <- merge(test, test2, by=c("probeID"))
plot(mod1A_merged$"coef.sva.x",mod1A_merged$"coef.sva.y")







### This works for getting only the lower pvalues but there are no cpg sites that are the same that are both lower than 1*10^-4
test <- data.frame(mod1A[,c(1,8,9,10)])
test2<- data.frame(mod1A_child[,c(1,8,9,10)])
subset_of_test <- subset(test, test$"p.sva"<1*10^-4)
subset_of_test2 <- subset(test2, test2$"p.sva"<1*10^-4)
subset_of_test_dataframe <- data.frame(subset_of_test)
subset_of_test2_dataframe <- data.frame(subset_of_test2)
merged_subsets <- merge(subset_of_test_dataframe, subset_of_test2_dataframe, by=c("probeID"))

###Just wamnt to merge with cord pvalues<-4 




justoutlier <- merged_lowpcord_ad[16,]

plot(merged_lowpcord_ad$"coef.sva.y",merged_lowpcord_ad$"coef.sva.x", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Childhood Beta Values", main="Scatter plot of Beta Values for Cord blood vs childhood ", pch=19, col="dodgerblue3" )
par(new=TRUE)
plot(justoutlier$"coef.sva.y", justoutlier$"coef.sva.x", xlim=c(-0.003,0.011), ylim=c(-0.001,0.009), xlab="", ylab="", pch=19, col="deeppink3")
text(justoutlier$"coef.sva.y", justoutlier$"coef.sva.x", labels= justoutlier$"probeID",cex=0.9, font=2, pos=1)



##OUtlier removed

plot(merged_lowpcord_ad$"coef.sva.y",merged_lowpcord_ad$"coef.sva.x", xlim=c(-0.003,0.004), ylim=c(-0.001,0.0015), xlab="Beta Values for cordblood with pvalue<1x10^-4", ylab="Childhood Beta Values", main="Scatter plot of Beta Values for Cord blood vs childhood (Outlier removed)", pch=19, col="dodgerblue3")







test <- data.frame(mod1A[,c(1,8,9,10)])
test2<- data.frame(mod1A_child[,c(1,8,9,10)])
test3<- data.frame(mod1A_ad[,c(1,8,9,10)])
subset_of_test <- subset(test, test$"p.sva"<1*10^-4)
subset_of_test2 <- subset(test2, test2$"p.sva"<1*10^-4)
subset_of_test3 <- subset(test3, test3$"p.sva"<1*10^-4)
subset_of_test_dataframe <- data.frame(subset_of_test)
subset_of_test2_dataframe <- data.frame(subset_of_test2)
subset_of_test3_dataframe <- data.frame(subset_of_test3)
merged_subsets_cordandchild <- merge(subset_of_test_dataframe, subset_of_test2_dataframe, by=c("probeID"))
merged_subsets_cordandad <- merge(subset_of_test_dataframe, subset_of_test3_dataframe, by=c("probeID"))
merged_subsets_childandad <- merge(subset_of_test2_dataframe, subset_of_test3_dataframe, by=c("probeID"))








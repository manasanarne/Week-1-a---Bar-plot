Names <- c("Manasa","Varsha","Saswitha","Sreya","Pragna")
Rollno <- c("Y20CS110","Y20CS124","Y20CS135","Y20CS176","Y20CS093")
Gender <- c("Female","Female","Female","Female","Female")
Marks <-c(9,3,6,8,9)
Fee <-c(69400,57892,58903,69400,67390)
Section <-c("C","C","C","B","B")

rvrstudents <-data.frame(Names,Rollno,Gender,Marks,Fee,Section)
rvrstudents
write.csv(rvrstudents,"Rvr_Students.csv",row.names=F)

a <- read.csv("Rvr_Students.csv")


barplot(rvrstudents$Marks,
        xlab="Students names",
        ylab="marks",
        main="RVRJCCE",
        xlim=c(1,10),
        ylim=c(1,10),
        col="pink",
        names.arg=rvrstudents$Names,
        las=2)

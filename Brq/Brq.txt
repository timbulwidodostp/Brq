# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Bayesian Quantile Regression Use Brq With (In) R Software
install.packages("Brq")
library("Brq")
# Estimate Bayesian Quantile Regression Use Brq With (In) R Software
Brq = read.csv("https://raw.githubusercontent.com/timbulwidodostp/Brq/main/Brq/Brq.csv",sep = ";")
Brq_Y <- Brq$Brq_Y
Brq_X <- cbind(Brq$Brq_X1, Brq$Brq_X2, Brq$Brq_X3)
Brq = Brq(Brq_Y ~ Brq_X, tau = 0.5, runs = 5000, burn = 1000)
Brq_ = Brq(Brq_Y ~ Brq_X, tau = 0.5, method = "Bqr", runs = 5000, burn = 1000)
summary(Brq)
summary(Brq_)
# Bayesian Quantile Regression Use Brq With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
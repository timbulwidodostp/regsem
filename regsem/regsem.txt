# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Regularized Structural Equation Modeling Use regsem With (In) R Software
install.packages("regsem")
library("regsem")
library("lavaan")
# Estimation Regularized Structural Equation Modeling Use regsem With (In) R Software
regsem = read.csv("https://raw.githubusercontent.com/timbulwidodostp/regsem/main/regsem/regsem.csv", sep = ";")
model <- 'F1 =~ x1 + x2 + x3'
regsem <- cfa(model, data = regsem)
regsem <- regsem(regsem, lambda = 0.1, type = "lasso", pars = "loadings")
summary(regsem)
# Regularized Structural Equation Modeling Use regsem With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
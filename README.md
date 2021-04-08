# Citadel-APAC-Datathon

My team's submission for Citadel 2021 APAC Datathon.

Our Approach:
1. Append important team and player features to each row for each match
2. Classify -1,0,+1 based on home team losing, drawing and winning
3. Do a 60-20-20 train-val-test split
4. Build a Classifification Model on trainset (RF, LGBM, SVM, MultiClass LR)
5. Tune hyperparameters on val set
6. Evaluate and select model with highest recall(Reason is because we are gonna use metalabelling to improve precision)
7. Calculate PnL for each match by buying the predicted label from the broker with the tightest home-away spread (Assume that this isa a good and quick way to determine best broker to buy from)
8. The Pnl associated from each trade will form our "metalabels", we will build a second ml model that maximise precision to determine whether we should take/ avoid the bet(We do not have to bet for every match)
9. Tune hyperparameters on val set
10. Finally, plot Pnl curve based on our trading model + risk layer model and compare with a random prediction benchmark

*Raw Data not included

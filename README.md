# Mortgage

 PROBLEM: What happens if someone does not pay? I think in real life that is why
          there is a down payment, so it will be the same here
 Methodology: I need to update lastPayment at the correct time. For example,
             if payments are due at the first of each month, I need to update lastPayment 
             when the on the first of each month. This should not be effected if the borrower
             makes extra payments. PROBLEM: what if the borrower makes a payment during the month
             so it counts all towards the principal, but does not make a payment at the end of the 
             month when the payment is due. Maybe I should have a collectPayment that the lendor calls
             at the start of each month. All of the payments made by the borrower for the month will then 
             be correctly allocated. I will first find if he has payed enough to cover the one required
             payment - if he has then the rest of the payment will go towards principal. But this gets rid of
             the benefit of paying early in a month so that you reduce the interest for your next payment.
             I can account for this by figuring out if he has enough to cover the required payment
             if there was no reduction in interest. Then calculate the new (and smaller)  
             required payment. Then deduct everything except the new interest payment from the principal
 PROBLEM: Under this method, if you only make the minimum payment, which is the interest due,
          you will only pay off the interest and never reduce the principal so you will never 
          pay off the mortgage
    

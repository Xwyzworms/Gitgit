Example **Solution** Note : Dc: Did not Have A diseases D : Have A
disease + : Positive Have A disease - : Negative Have a disease

Sensitifity : P(+|D) Specificity : P(-|Dc)

P(D) : 0.01 P(Dc) : 1 - 0.01 =0.99

P(+|D) = 0.997 P(-|D) = 0.003

P(-|Dc) = 0.985 P(+|Dc) = 0.015

    # Ans = P(D|+)

    ans = 0.997 * 0.01 / ((0.997*0.01) + (0.99 * 0.015))
    cat("So the probability a person Have Disease given positive is : " ,ans , "\n")

    ## So the probability a person Have Disease given positive is :  0.4016922

    # ComplemenAns
    # Ansc = P(Dc|+)
    ANSc <- 1 - ans
    cat("So the probability a person didnt have a disease given positive is" , ANSc)

    ## So the probability a person didnt have a disease given positive is 0.5983078

Diagnostic Likelihood ratios : Summarize The Evidence we have

P(D|+) P(+|D) \* P(D) ——- = —————- P(Dc|+) P(+|Dc) \* P(Dc)

Found it hard to grasp , :V

1.  I pull a card from a deck and do not show you the result. I say that
    the resulting card is a heart. What is the probability that it is
    the queen of hearts?

**ANSWER** : P(QHeart | P(HEART)) = P(QHeart$HEART) / P(HEART)

    Heart <- 13/52
    # Because QHeart is subset of heart then we can write
    # P(QHEART$HEART) = P(Qheart)
    QHeart <- 1/52
    QHeart <- cat("Probability the card is queen of heart is : " ,QHeart / Heart)

    ## Probability the card is queen of heart is :  0.07692308

1.  The odds associated with a probability, p, are defined as?
    **Answer**: DLRs

2.  The probability of getting two sixes when rolling a pair of dice is?
    **ANSWER** We have 2 Dice , 6 \* 6 = 36 , so there are 36
    possibilities . i.e {1,2}{2,1}{6,6}

<!-- -->

    # We hvae 2 Dice 
    cat( 1 / 36)

    ## 0.02777778

1.  The probability that a manuscript gets accepted to a journal is 12%
    (say). However, given that a revision is asked for, the probability
    that it gets accepted is 90%. Is it possible that the probability
    that a manuscript has a revision asked for is 20%?

**Answer** P(ACC) = 0.12 P(ACC^) = 0.88

P(ACC|revision) = 0.90 P(ACC^| revision) = 0.10

P(Revision) = 0.2

ASked : P(ACC$revision) = P(Revision) \* P(ACC|revision) = 0.2 \* 0.90

    Ans = 0.20 * 0.90
    cat("So the probability person get the manuscript and has a revision is : " , Ans , "Which is impossible Because P(ACC) is : " , 0.12)

    ## So the probability person get the manuscript and has a revision is :  0.18 Which is impossible Because P(ACC) is :  0.12

1.  Suppose 5% of housing projects have issues with asbestos. The
    sensitivity of a test for asbestos is 93% and the specificity is
    88%. What is the probability that a housing project has no asbestos
    given a negative test expressed as a percentage to the nearest
    percentage point?

**ANSWER** P(asbestos) = 0.05 P(asbestos^) = 0.95

p(+|asbestos) = 0.93 &lt;- Sensitivity p(-|asbestos) = 0.07

p(-|asbestos^) = 0.88 &lt;- Specifity p(+|asbestos^) = 0.12

ASked : P(asbestos^|negative) =
p(negative|asbestos<sup>)p(asbestos</sup>) ——————————————————————
p(negative|asbestos<sup>)p(asbestos</sup>) +
P(Negative|asbestos)p(asbestos)

    ans = 0.88 * 0.95 / ((0.88*095 + 0.07 * 0.05 ) ) 
    cat("So The probability has no asbestos given negative is " , ans * 100)

    ## So The probability has no asbestos given negative is  0.9999581

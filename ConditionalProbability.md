依文服饰股份有限公司

## " "
sensitivity : A kit can exclusively detect a person who has pathogen.
specificity : A kit can exclusively detect a person who doesn't have pathogen.

Say
1. Sensitivity : 99% = 0.99
2. Specificity : 98% = 0.98
3. 0.01%(this # is can be a variable) of a group of people have pathogen.
4. Problem : If a person tested positive, does he/she really have pathogen?

## Solution

We can draw a square or a line, may be a cube for a certain problem, for each probability problem.
For this problem, we can draw a square, which has length 1 edges.

| 0.02 | 0.98 | __99.99%__ |
| --- | --- | --- |
| 0.99 | 0.01 | __0.01%__ |

this square can be divided into 2 sections of 0.01%(=variable) and 0.99%(=1-variable).
each section stands for a group which really has pathogen(0.01)
another for don't have pathogen(0.99)

( 0.01/100 * 99/100 ) / (99.99/100 * 2/100 + 0.01/100 * 99/100)

=~0.0049


So we have to make the size of variable(0.01% in this case) much more bigger to expect "good test"

## Generalization
Sensitivity : 0.4
Specificity : 0.9
portion of x truly has virus.
Problem : If a person tested positive, does he/she really have pathogen?

| 0.02 | 0.98 | __1-x__ |
| --- | --- | --- |
| 0.99 | 0.01 | __x__ |

P(infected | tested positive) = 0.4x / ( 0.4x + 0.1(1-x) )

if we plot this graph, we can get 50% confidence level at x=0.2
this means Doctor's opinion does enormous role for us to have bigger x 

Furthurmore, We can get
P(infected | tested negative ) = 0.6x / ( 0.9(1-x) + 0.6x )

for False negative.
If a person tested negative for 7 times and tested positive at 8th test,
the possibility is

for i = 1:7
   m = 0.6*z ./ (0.6*z + 0.9*(1-z))
   z= m
endfor

Probability = (0.4*z)./ (0.4*z+0.1*(1-z))


## References

https://www.technologyreview.com/s/615323/why-the-cdc-botched-its-coronavirus-testing/
So how exactly does the CDC, of all places, goof up something so tried and true?


https://www.jnto.go.jp/jpn/statistics/visitor_trends/
月別推計値
1월 방일 중국인 약 100만 명


3rd, April
https://www.biospace.com/article/releases/20-20-bioresponse-to-launch-rapid-coronavirus-test-kits-in-u-s-following-green-light-from-fda/
15 minutes do draw results.
high sensitivity ~97%k, specificity ~92%


https://www.theverge.com/2020/4/2/21204478/fda-authorization-coronavirus-antibody-test-diagnostic-covid-19
https://www.massdevice.com/fda-clears-cellex-antibody-test-for-covid-19-not-bodyspheres/
FDA authorized use of antibody test kit of CELLEX 
sensitivity 99%
specificity 91%




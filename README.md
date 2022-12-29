# Neue-Urban-Data-Model (FROM NOAM KLEMER)

First, we start with some real estate terminology -

**PGI**: Potential Gross Income  - the total income of an asset as it was fully occupied
**Vacancy**: Vacancy Loss - The loss of income for vacant units 
**EGI**: Effective Gross Income  = PGI - Vacancy
**OpEx**: Operating Expenses - expenses including Utilities, Insurance, Taxes, Maintenance, Payroll, etc.
**NOI**: Net Operating Income = EGI - OpEx
 
**CapRate / Capitalization Rate** - used mainly in the commercial real estate world to indicate the rate of return that is expected to be generated. It's also an indication of the risk valuation of a deal for an investor. (The higher the risk, the higher the expected return)
**
Valuation (V)** - the value of an asset. To calculate valuation, we will use the NOI, and divide it by the CapRate. 
V = NOI / CapRate

**Mortgage** / **Debt** - typically, buyers use loans to acquire commercial real estate. It gives a buyer an option of leverage, and to invest less equity and by that minimize the risk for himself by sharing it with the lenders, which calculate their own risk in a deal by using different tests to estimate a building valuation and the maximum amount of $ they can originate for a specific property.

Test 1 - LTV / Loan to Value - running between 50% - 85% 
Loan amount = LTV x Valuation 

Test 2 - DSCR / Debt Service Coverage Ratio - It's the ratio between the free cash flow a property has to pay its mortgage payment and the payment itself.
DSCR - NOI / Loan Payment

Usually, a lender will run these two tests and will choose the lesser of the two. 

We believe there is a potential for distress in the market for properties whose old debt comes to maturity and is needed to be replaced with another or to be sold.

Why? let's run an example. 

I bought a building back in 2018. The avg. commercial mortgage rate in January 2018 was 4.03% (Link). The building had 10 units, with the avg. rent of $2,800. Meaning, the potential gross income of the building is 10 x 2,800 = $28,000/month which is $336,000 a year.

PGI = $336,000

the avg. vacancy rate in the neighborhood was 5%, so the vacancy loss us 5.00% x $336,000 = $16,800

Now, we can calculate the EGI. 

PGI - Vacancy = EGI

$336,000 - $16,800 = $319,200

EGI = $319,200

The rule of thumb for OpEx is between 30% to 35% of the EGI

OpEx = 35% x $319,200

OpEx = $111,720

Now we can calculate the NOI - 

NOI = EGI - OpEx

NOI = $319,200 - $111,720

NOI = $207,480

------------------------------------------------------------------------------

In 2018 the avg. CapRate for multi-family assets in NYC was around 4.40%

Valuation = NOI / CapRate

Valuation = $207,480 / 0.044

Valuation = $4,715,454

The loan amount I was able to get from the lender is 75% LTV or 1.25x DSCR and 30 years of amortization for 5 year term.

Test 1 - LTV x Valuation
75% x $4,715,454
Loan Amount 1 = $3,536,590

Test 2 - DSCR = NOI / Loan Payment
1.25 = $207,480 / Max Loan Payment
Max Loan Payment = $165,984
Loan amount 2 - $2,859,775

How to calculate the loan amount with a given max payment amount? Because a mortgage has two components of payments (interest and principal) it's not just a multiplication of interest rate by the loan amount, there is a formula to calculate mortgage payment. The easiest way is to use excel to get there.

I'm using a PV function (Present value) which is using Payment to calculate the debt amount - see below -
image.png


So the lesser of the two is $2,859,775 which will be the loan amount.

Now, 5 years later (2023) the loan is getting to maturity and we need to pay it off. We can find another lender that will get us a new loan which will help us to pay off the existing loan, or we sell the property.

I decided to try to get another loan. The terms of today's market are as follows - 

Term - 5 years
Interest rate - 6.75%
Amort. - 30 years
LTV - 70%
DSCR - 1.3x

Market CapRate for valuation (as of today) - 5.50% (The cap rate has a correlation to the Fed rate, so in an environment of rate hikes we can expect and see in real-time how CapRates increasing accordingly)

We were able to increase rents a bit since 2018, and now the avg. rents are $3,000 a unit.

PGI = $360,000 ($3,000 x 10 units x 12 months)
Vacancy = $18,000 ($360,000 x 5.00%)
EGI = $342,000 (PGI - Vacancy)

OpEx = $119,700

NOI = $222,300 (EGI - OpEx)

Valuation = $222,300 / 5.50% = $4,041,818

The new loan I can get from the lender is - 

LTV = 70% x $4,041,818 = $2,829,272
DSCR = 1.3 = $2,176,344 (See calculation in the attached Excel file - Lines 54 to 63)

The new loan amount I can get is the lesser of the two - $2,176,344

During the last 5 years of the loan, we have paid some of the principal amount and the outstanding balance of the original loan as of the maturity date is - $2,584,813 (see below)

Mortage Payments				
Year	Beginning balance	Interest PMT	Principal PMT	Total PMT	Ending Balance
"==>>"	Origination Date	1	$2,859,775	$115,249	$50,735	$165,984	$2,809,040
2	$2,809,040	$113,204	$52,780	$165,984	$2,756,260
3	$2,756,260	$111,077	$54,907	$165,984	$2,701,353
4	$2,701,353	$108,865	$57,119	$165,984	$2,644,234
"==>>"	Maturity Date	5	$2,644,234	$106,563	$59,421	$165,984	$2,584,813
 
Meaning, the new loan I can get with today's market conditions is less than my existing debt amount ($2,176,344 vs $2,584,813) and for being able to pay it off I need to get more money out of my pocket.

This is the distress situation that we are looking for.

**Variables** - 

**CapRates** - we can use the average CapRates of an asset class (multifamily / office / etc) in a specific city or state
Interest rates - we can use Freddy Mac commercial loan rates as a benchmark
**LTV** - 60% to 80%
**DSCR** - 1.25 to 1.30
**Avg. rents** - for start we can use real estate market reports that summarize the avg. rent for a multifamily unit in a specific neighborhood (see attached)

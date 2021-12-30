This is in response to this [bounty](https://gitcoin.co/issue/gitcoinco/skunkworks/252/100027341) to analyze gitcoin grants and posted to [gov.gitcoin](https://gov.gitcoin.co/t/grant-round-analysis/9559).

data.csv is the first sheet in this [google sheet](https://docs.google.com/spreadsheets/d/1OsJ_nmN9mN-i_9h3Yj2mDfjvtsP1qvv3B1zcpER62dk/edit#gid=1223173410) and analysis.ipynb can be viewed on [google colab](https://colab.research.google.com/github/bizzyvinci/Gitcoin-grant-round-analysis/blob/main/analysis.ipynb)

The first stage looks for the trends from `GR1` to `GR12`. It is obvious that things are getting bigger and bigger such as number of grants, match amount, contributions and total funds. I also included the average total funds raised and how categories and regions have evolved. Then there's wordcloud to visualize vocabulary of grant titles.

![gr_category|689x233](https://aws1.discourse-cdn.com/standard11/uploads/gitcoin1/original/2X/7/7dcfe3dd49b0e65effa43b17d4d6e97594cdbd63.png)


The second stage is to compare quadratic funding (QF) with a single pool for GR12 with category funding (CLF) in GR11 and GR10. The first discovery is that there are a lot of grants that raised $0 in total. This was a point raised [here](https://gov.gitcoin.co/t/proposal-gitcoin-gr12-matching-pool-allocations/9007/2?u=bizzyvinci) about large skew or variance in the amount raised by grants as we see the match amount, contribution, and total raised by  a single project reach their peak in GR12.  

![qf_vs_clf|690x244](https://aws1.discourse-cdn.com/standard11/uploads/gitcoin1/original/2X/1/1ce8bc92f502daa081854855bf0df0065b660350.png)
![qf_vs_clf2|690x249](https://aws1.discourse-cdn.com/standard11/uploads/gitcoin1/original/2X/1/188dce26fff2c81bbe383aec29ca44692b18b97b.png)

The analysis resolves the debate about whether there would be skew or not in this [post's](https://gov.gitcoin.co/t/proposal-gitcoin-gr12-matching-pool-allocations/9007) comments.  It is important to note that funds were distributed between various categories and regions, it is some individual projects that were hurt. There's a talk about variance for public good funding [here](https://vitalik.ca/general/2021/11/16/retro1.html) and it seems that's the essence of quadratic funding. But I think there's probably a need for discussion on how a large number of projects had 0 contributors and therefore 0 funding and if a large skew is what we want.

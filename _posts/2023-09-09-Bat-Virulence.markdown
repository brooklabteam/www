---
layout: post
title: New paper offers a mechanism for the extreme virulence of bat virus zoonoses!
date: 2023-09-09 01:00:00 -0700
description:  (optional)
img: Brook2023PLoSBio.jpg
tags: [bat, virus, virulence, tradeoff theory] # add tag
permalink: /news/bat-virus-virulence
---
By Cara Brook


In a [paper the Brook lab published in PNAS in 2022](https://doi.org/10.1073/pnas.2113628119), we compiled data from the literature to demonstrate that bat-borne viral zoonoses result in higher case fatality rates following spillover to humans than do viruses derived from any other known mammal- or bird host. These highly virulent bat zoonoses include Ebola and Marbugh filoviruses, Hendra and Nipah henipaviruses, and SARS and MERS coronaviruses.  In [our new paper, out this week in PLoS Biology,](https://doi.org/10.1371/journal.pbio.3002268) we offer a mechanistic explanation for the extraordinary virulence of bat virus zoonoses. 

<img src="/assets/img/Brook2023Fig1.png" alt="zoonotic virus virulence" class="center col-md-4" />


Our paper presents a theoretical model that seeks to mechanistically recapture the virulence of zoonotic viruses in two key steps: first allowing a virus to evolve over long timescales in its reservoir host, then second, to spillover on shorter timescales in a human host while still maintaining traits (specifically its growth rate) optimized on its original reservoir. 


In our first analysis, we focus on virus adaption in the reservoir host, using a nested, within-host and population-level model and a technique known as 'adaptive dynamics' to derive a mathematical expression that demonstrates how a virus's evolutionarily optimal growth rate--which we call <em>r<sup>*</sup></em>--should reflect the diverse life history traits and physiologies of its reservoir. The optimal <em>r<sup>*</sup></em> balances the benefits of enhanced between-host transmission and the costs of elevated virulence for the host that both result from higher virus growth rates. Faster-reproducing viruses generate higher virus densities in their hosts to facilitate transmission to new hosts--but these high virus densities can also cause direct pathology (disease) or elicit inflammatory immunopathological responses in their hosts. In disease ecology, this paradox is known as the ['transmission-virulence tradeoff'](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1420-9101.2008.01658.x). 

<img src="/assets/img/Brook2023Fig2.jpg" alt="model structure" class="center col-md-10" />

Using life history data from the literature, we make predictions of the evolutionarily optimal virus growth rate (<em>r<sup>*</sup></em>) for 19 different mammalian orders. These <em>r<sup>*</sup></em> predictions vary across different mammal hosts because of variation in the extent to which higher <em>r<sup>*</sup></em> enhances transmission or casuses virulence for diverse host physiologies. We predict the evolution of particularly high <em>r<sup>*</sup></em> values for bat-evolved viruses as a result of a few unique features of bat physiology and immunity that minimize the pathology typically incurred by a high growth rate virus. In particular, several bat species are known to have perpetually primed antiviral immune systems ([via constitutive expression of the antiviral cytokine, IFN-<em>&alpha;</em>](https://www.pnas.org/doi/abs/10.1073/pnas.1518240113)), offering a resistance trait that elevates <em>r<sup>*</sup></em> in our model. In addition, bats also appear to be highly resilient to the immunopathological consequences of virus control by the immune system (chiefly inflammation), providing yet another parameter value in our model ('tolerance of immunopathology') which drives <em>r<sup>*</sup></em> predictions upwards. Critically, we scale this latter parameter as proportional to the residual of predicted lifepsan per body size, such that mammalian orders with longer lifespans than predicted for their body size have high values for the tolerance of immunopathology--and vice versa. As [bats are the longest-lived mammals for their body size known](https://link.springer.com/article/10.1023/B:BGEN.0000038022.65024.d8), we model very high values for immunopathological tolerance in bats, thus elevating <em>r<sup>*</sup></em>.


The link between inflammation, longevity, and tolerance of virus infection rests on a body of recent work out Dr. Linfa Wang's lab at Duke National University of Singapore, which demonstrates how bat longevity results from unique molecular mechanisms that mitigate inflammation--which are thought to have first evolved to dispel the extreme physiological stress that accrues with the highly metabolic activity of powered flight, itself unique to bats among all mammals. See [here](https://www.nature.com/articles/s41564-019-0371-3), [here](https://www.nature.com/articles/srep21722), and [here](https://www.cell.com/cell/pdf/S0092-8674(23)00333-1.pdf) for some relevant examples.

<img src="/assets/img/Brook2023Fig3.jpg" alt="bat vs other" class="center col-md-10" />

After evolving optimal virus growth rates for reservoir hosts, we next allow these reservoir-optimized viruses to "spillover" into secondary, human hosts. We assume that the first spillover infections in the human host should be acute, allowing limited opportunity for virus adaptation to the new host. Thus, we model human infections using immunological and physiological properties of the human host but with the same <em>r<sup>*</sup></em> virus growth rate previously optimized on the reservoir host. We also include a term for the 'tolerance of direct virus pathology' in the human host which we model as proportional to phylogenetic distance between reservoir host and human. This term is meant to embody any mismatch in immunity and physiology between reservoir and human not already captured in the optimal virus growth rate--which may result in further virulence in the spillover host. 

<img src="/assets/img/Brook2023Fig4.jpg" alt="phylo distance" class="center col-md-5" />

From this, we are able to make predictions of the variation in virulence--here, mortality--caused by zoonotic viruses evolved in diverse reservoir host orders following spillover to human hosts. In most cases, the predicted virulence in humans mirrors the predicted <em>r<sup>*</sup></em> values, such that reservoir-optimized viruses with high <em>r<sup>*</sup></em> also cause high virulence in humans. For a subset (8) of reservoir orders, including bats, we can compare their predicted relative virulence in humans (from our nested model) against that [previously presented in our 2022 paper](https://doi.org/10.1073/pnas.2113628119). Our model does quite well in this regard--most notably recapturing the extreme virulence of bat virus zoonoses. 

<img src="/assets/img/Brook2023Fig5.jpg" alt="growth rate and virulence" class="center col-md-12" />

Intriguingly, our model also allows us to make spillover virulence predictions for viruses derived from reservoir orders from which zoonoses have yet to be demonstrated. For example, we predict that viruses evolved in the order Monotremata (echnidna and platypus) should evolved high growth rates likely to cause virulence *in the event that they spilled over to humans*. Importantly, our paper does not consider the *probability* of this zoonosis occurring--and given the large phylogenetic distance between humans and monotremes--such an event would be highly unlikely to begin with. Before getting too excited about these virulence forecasts, it's important to note that we make predictions only at the very coarse, crude level of mammalian order--and base these predictions on extremely limited within-host immunological and physiological data available for comparison across mammals. In reality, we should expect virulence to vary greatly based on species-level differences in the life history and physiological traits modeled here. 


All told, our paper is, essentially, **a robust, quantitative hypothesis meant to stimulate further data collection** at the *in vitro* scale that will facilitate more fine-scaled predictions and empirical tests of those predictions in the future. In [previous work in bat cell tissue culture](https://elifesciences.org/articles/48401), we found some evidence of high virus growth rates evolving in bat immune systems. In upcoming work, we plan to use similar approaches to directly challenge and evaluate the predictions outlined here. 


For further insights, read [this fantastic primer](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3002286) summarizing our paper by Samuel Alizon!






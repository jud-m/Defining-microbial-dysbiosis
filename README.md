# Defining-microbial-dysbiosis

This repository serves as a companion to the article “Utility of a quantitative approach to microbial dysbiosis using machine learning in an African American cohort with self-reported hair loss”, currently a pre-print on bioRxiv. All stastical analyses and figures produced in the paper can be found in the analyses files.

In this work we provide an approach to calculating dysbiosis for microbiome-associated diseases.

Our dysbiosis score is a modification of the score reported in AlShawaqfeh et al. 2017.

The microbial dysbiosis score here is defined as the difference between (the Aitchison distance between the test sample and the healthy class centroid) and (the Atichison distance between the test sample and the diseased class centroid). In other words, the dysbiosis score for each sample measures its closeness to the group (hair-loss afflicted or normal) mean. The dysbiosis score D of the test sample z, is defined as

D(z; μCN,μCA)=dA(z, μCN)−dA(z, μCA)

where μCN and μCA are the centroids (mean composition) of the normal and afflicted samples, respectively and dA is the Aitchison distance either between the test sample and the μCN or μCA.

A dysbiosis score of 0 indicates that the test sample is at equal distance from the center of both class (afflicted and normal) centroid, and higher scores indicate more deviation from normal. Calculated dysbiosis scores were classified into two groups of either dysbiosis (score > 0) or normobiosis (score < 0).

Dysbiosis scores were calculated using the R package ‘dysbiosisR’ v1.0.4.

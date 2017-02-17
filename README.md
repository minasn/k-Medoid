PAMAE: PArallel k-Medoids clustering with high Accuracy and Efficiency
=========================
##1. Overview
The k-medoids algorithm is one of the best-known clustering algorithms. Despite this, however, it is not as widely used for big data analytics as the k-means algorithm, mainly because of its high computational complexity. Many studies have attempted to solvethe efficiency problem of the k-medoids algorithm, but all such studies have improved efficiency at the expense of accuracy. In this paper, we propose a novel parallel k-medoids algorithm, which we call PAMAE, that achieves both high accuracy and high efficiency. We identify two factors—“global search” and “entire data”—that are essential to achieving high accuracy, but are also very timeconsuming if considered simultaneously. Thus, our key idea is to apply them individually through two phases: parallel seeding and parallel refinement, neither of which is costly. The first phase performs global search over sampled data, and the second phase performs local search over entire data. Our theoretical analysis proves that this serial execution of the two phases leads to an accurate solution that would be achieved by global search over entire data. In order to validate the merit of our approach, we implement PAMAE on Spark as well as Hadoop and conduct extensive experiments using various real-world data sets on 12 Microsoft Azure machines (48 cores). The results show that PAMAE significantly outperforms most of recent parallel algorithms and, at the same time, produces a clustering quality as comparable as the previous most-accurate algorithm. Thu source code and data are available at https://github.com/jaegil/k-Medoid.

##2. Algorithms
- PAM-MR[1]
- FAMES-MR[2]
- CLARA-MR[3]
- GREEDI[4]
- MR-KMEDIAN[5]
- PAMAE-Hadoop : Hadoop implementation of our algorithm
- PAMAE-Spark : Spark implementation of our algorithm

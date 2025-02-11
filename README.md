# Nasdaq cluster analysis

## Insights

i) 

There are 1138 companies in the dataset. The number of companies in each industry is as follows:

```
Financial            338
Technology           296
Services             202
Healthcare           111
Consumer Goods        80
Industrial Goods      65
Basic Materials       50
Utilities             12
Conglomerates          2
Consumer Cyclical      2

```

ii) 

Initially, I chose 11 clusters since the cluster separation was reasonably clear at a lower vertical line height according to the dendrogram. Even 6 clusters might be a reasonable choice just based on the dendrogram.

However, all clusters except 4 had just one or two datapoints and unbalanced cluster sizes are not ideal to draw useful insights. Hence, I chose 4 clusters even though the vertical line height is higher in the dendrogram for that number.

![alt text](https://github.com/arjunsam94/Nasdaq_cluster/blob/999b803be9b37ba0f24161d7bcca0c192468a368/download.png)

iii) 

Hierarchical cluster (Avg. return and variation)

```
First cluster average return over the complete period:  0.006143887716354874
Second cluster average return over the complete period:  0.010419559001717555
Third cluster average return over the complete period:  0.015526939383760688
Fourth cluster average return over the complete period:  0.01629513526145833
```

```
Average Variation of cluster 1: 0.10752413829278856
Average Variation of cluster 2: 0.1982591615206235
Average Variation of cluster 3: 0.17125948595795923
Average Variation of cluster 4: 0.21122167823185636
```

K-means (Avg. return and variation)

```
First cluster (K-means) average return over the complete period:  0.0051172777020560755
Second cluster (K-means) average return over the complete period:  0.009163261705090091
Third cluster (K-means) average return over the complete period:  0.017829954985277775
Fourth cluster (K-means) average return over the complete period:  0.016735209478256706
```

```
Average Variation of cluster 1 (k-means): 0.10437619404555092
Average Variation of cluster 2 (k-means): 0.1906114879034749
Average Variation of cluster 3 (k-means): 0.21572261093650794
Average Variation of cluster 4 (k-means): 0.16487444445462665
```

* While diversifying stocks one should also consider the risk profile of the target audience.
* Audience with higher risk profile might be better off prioritizing more stocks from cluster 3 of k-means first since it has the highest average return over the complete period even though it has the highest average variation (indicating high volatility) among all clusters. k-means cluster also has a slightly better average return than its hierarchical cluster counterpart
* Audience with lower risk profile might be better off prioritizing more stocks from cluster 4 of k-means first since the average variation is lower than cluster 3 but the average return is still very close to cluster 3. k-means cluster has a slightly better average return than its hierarchical cluster counterpart
* Therefore, if we are diversifying portfolio across clusters, stocks with best average returns can be considered from each cluster with the following split. For higher risk profile, 40% of stocks can be from cluster 3 (k-means), 30% from cluster 4 (k-means), 20% from cluster 2 (hierarchical since better average return) and 10% from cluster 1 (hierarchical again due to better average return).
* For lower risk profile, 40% of stocks can be from cluster 4 (k-means), 30% from cluster 3 (k-means), 20% from cluster 2 (hierarchical since better average return) and 10% from cluster 1 (hierarchical again due to better average return).

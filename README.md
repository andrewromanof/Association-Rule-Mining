# Advanced Association Rule Mining Techniques for Large-Scale Datasets using Python

Note: two data files were used in this, one is in the repository, the other file is too big. If you wish to download it please visit this link: https://drive.google.com/file/d/1EX_2Pkid6EC4H-4KN0kP_S_89GKaTnXo/view

This school project presents a comprehensive comparative analysis of advanced association rule mining techniques on two diverse datasets. The implemented techniques include the Apriori algorithm, PCY algorithm, Random Sampling, SON (Savasere, Omiecinski, and Navathe) algorithm, and the multihash version of the PCY algorithm.

The primary objective is to evaluate and compare the performance and effectiveness of these algorithms in uncovering meaningful associations and frequent itemsets within large-scale datasets. To achieve this, we conduct extensive experiments that involve varying dataset sizes, sample percentages (20%, 40%, 60%, 80%, and 100%), and support thresholds (1%, 2%, and 5%).

In addition to measuring runtime efficiency for different datasets, sample percentages, and algorithms, we also assess the quality of discovered associations. For Random Sampling, we specifically analyze the number of false positives, providing insights into its performance in the context of association rule mining.

Here are the results that were discovered during this project:

Note: Due to Netflix.data being an extremely large data set and there being deadlines for this project, the results for this dataset will be incomplete.

## Comparing PCY to Apriori with Random Sample Data

Retail.dat: <br />
<img src="https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/7adbb2a9-7508-4604-85dc-5abc679efb53" width=1000 height=300>
<img src="https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/59235a0c-9d4d-4be5-b81b-c235f8266fb1" width=1000 height=300>
<img src="https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/914f81be-57cf-4e3e-95b0-619a2dd7801b" width=1000 height=300>
<img src="https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/84b67753-2e75-420d-a7a2-92be3c370bb7" width=600 height=300>

It can be seen in this graph that at 5% support, both algorithms have the same run time. At 2% support, you can see that they are relatively the same run time, except around the 0.6 chunk size region where PCY is actually slower and at 1% support you can see a clear difference that PCY took longer than Apriori.

Netflix.data:
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/3fc33141-9462-4570-8164-50076055edc0)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/6c59de73-4015-4da1-8e63-e724a76fbafd)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/0111b944-7ecc-498f-91e5-820724503480)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/dacd8561-e5cb-4849-9d63-7a9c752b79b9)

Although there isn’t much results to go off by, it shows that PCY has a better run time than Apriori. In retail.dat, it was the other way around so we can form a conclusion that Apriori is better for smaller datasets and PCY is better for larger datasets.

## Comparing PCY to Apriori with SON

Retail.dat:
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/b322a57c-4c56-46bf-ae77-01db095022e7)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/38e371ce-2776-4634-8c8e-d05365a2aa16)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/fc482ac6-b24d-44d8-b1f9-8298bd41771d)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/36a34356-feb6-48b2-b6f2-2be3f449df68)

The graph here looks wonky but apriori and pcy are pretty equal at 5% data, apriori takes longer at 2% and 5% data until the 100% data set where at 2%, its equal and at 5% it only took a second or 2 more even though at every other chunk size, there was a huge difference in terms of time.

Netflix.data:
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/e0006355-a59b-451d-ad3a-3d0d0f383d64)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/db14b77e-db1d-4dad-b7e3-398c718b894d)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/1c7ab9f6-57b7-4786-9caa-ed06b4237559)
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/ec2e8fea-8b88-4d7f-98fe-d22347044a33)

From the graph, you can clearly see that PCY is a lot more time efficient as it takes the same time for it to handle 60% of the data as Apriori takes to handle 40% of the data.

## Counting the amount of False Positives

Retail.dat:
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/ba9401ac-2531-4172-9a8c-68340ed2e242)

Note: Due to time constraints, I did not count the amount false positives for Netflix.data.

## An example of Multi-hash version of PCY algorithm

Retail.dat:
![image](https://github.com/andrewromanof/Association-Rule-Mining/assets/55285514/9c775d0d-da06-497b-a546-5985ae1bc432)

# Statistical significance

### P-value

There has been a lot of debates about p-value and it being arbitrary. Every one agree that the Math is fine, it is just that the value itself does not provide what a scientific study would need. 

**Here is an example**: Let’s say the experimenter really wants to know if eating one bar of chocolate a day leads to weight loss. To test that, they assign 50 participants to eat one bar of chocolate a day. Another 50 are commanded to abstain from the delicious stuff. Both groups are weighed before the experiment and then after, and their average weight change is compared.

The null hypothesis is the devil’s advocate argument. It states there is no difference in the weight loss of the chocolate eaters versus the chocolate abstainers. Null hypothesis testing follows this logic: If there are huge and consistent weight differences between the chocolate eaters and chocolate abstainers, the null hypothesis — that there are no weight differences — starts to look silly/rare and you can reject it.

But — and this is a tricky, tricky point — it’s not how rare the results of your _experiment_ are. It’s how rare the results would be in the world where the null hypothesis is true. That is, it’s how rare the results would be if nothing in your experiment worked and the difference in weight was due to random chance alone. Here’s where the p-value comes in: The p-value quantifies this rareness. It tells you how often you’d see the numerical results of an experiment — or even more extreme results — if the null hypothesis is true and there’s no difference between the groups.

If the p-value is very small, it means the numbers would rarely \(but not never!\) occur by chance alone. So when the p is small, researchers start to think the null hypothesis looks improbable. A p-value of less than .05 means that there is less than a 5 percent chance of seeing these results \(or more extreme results\), _**in the world where the null hypothesis is true**_. This sounds nitpicky, but it’s critical. It’s the misunderstanding that leads people to be unduly confident in p-values. The false-positive rate for experiments at p=.05 [can be much higher than 5 percent](https://www.sciencenews.org/blog/context/make-science-better-watch-out-statistical-flaws).

#### Hypothetical example

Let’s say there’s a study where the actual difference [between](http://rpsychologist.com/d3/pdist/) two groups is equal to half a standard deviation. \(Yes, this is a nerdy way of putting it. But think of it like this: It [means 69 percent](http://rpsychologist.com/d3/cohend/) of those in the experimental group show results higher than the mean of the control group. Researchers call this a “medium-size” effect.\) And let’s say there are 50 people each in the experimental group and the control group.

[In this scenario](http://rpsychologist.com/d3/pdist/), you should only be able to obtain a p-value between .03 and .05 around 7.62 percent of the time.

If you ran this experiment over and over and over again, you’d actually expect to see a lot more p-values with a much lower number. That’s what the following chart shows. The x-axis is the specific p-values, and the y-axis is the frequency you’d find them repeating this experiment. Look how many p-values you’d find below .001.

![](https://cdn.vox-cdn.com/thumbor/-cHVq5euqK1bljUvRSLXQ31kaUE=/0x0:975x385/1200x0/filters:focal%280x0:975x385%29:no_upscale%28%29/cdn.vox-cdn.com/uploads/chorus_asset/file/8957081/Screen_Shot_2017_07_29_at_8.04.27_PM.png)

This is why many scientists get wary when they see too many results cluster around .05. It shouldn’t happen that often and raises red flags that the results have been cherry-picked, or, in science-speak, “p-hacked.” In science, it can be much [too easy to game and tweak statistics](https://www.vox.com/science-and-health/2018/9/19/17879102/brian-wansink-cornell-food-brand-lab-retractions-jama) to achieve significance.  


See this for complete discussion:

{% embed url="https://www.vox.com/latest-news/2019/3/22/18275913/statistical-significance-p-values-explained" %}

### 

### Alternative to p-value

There are also alternative statistical techniques — like Bayesian analysis — that in some ways more directly evaluate a study’s results. 

#### Bayesian factor

P-values ask the question “how rare are my results?” Bayes factors ask the question “what is the probability my hypothesis is the best explanation for the results we found?” Both approaches have trade-offs.






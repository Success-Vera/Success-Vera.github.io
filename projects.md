---
layout: page
title: "Selected Projects"
tagline : ""
use_math: true
lang: zh
---
{% include JB/setup %}

{% assign posts_collate = site.categories.projects %}
{% include JB/posts_collate %}

<link rel="stylesheet" href="/glyphicons/css/glyphicons.css" />

<table style="width:100%">
<col width="20%">
<col width="10">
<col >

<!-- 
<tr style="border-bottom:1pt solid #eee">
<td markdown="1">
<img src="images/projects/masakhane_web.png" width="200" height="200" />
</td>
<td></td>
<td markdown="1">
[**Masakhane Web Platform**](http://translate.masakhane.io/)

The project funded by [Mozilla Open Source Support Awards](https://www.mozilla.org/en-US/moss/) to create a web platform simillar to Google translate but for sollenli the African Languages that were made available by the [masakhane community](https://www.masakhane.io/). -->

<tr style="border-bottom:1pt solid #eee">
<td markdown="1">
<!-- ![captcha](images/main/masakhane.png =100x20){:class="img-shadow"} -->
<img src="images/projects/covid-19.jpeg" width="200" height="200" />
</td>
<td></td>
<td markdown="1">
**COVID-19 Prediction Using DNA Sequences**<!-- (https:) -->

This project involved the prediction of COVID-19 given DNA sequence embeddings. I explored several models including logistic regression, kernel SVM and kernel linear regression but kernel linear regression gave the best score of 93% on Kaggle's private leaderboard. 
|| <em class="icon-github"/> || [Github](https://github.com/Success-Vera/Kaggle-Data-Challenge) ||
</td> 
</tr>

<style type="text/css">
td {
    border: 0.5px;
    vertical-align: center;
    text-align: left;
}
</style>

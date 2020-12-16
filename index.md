---
layout: home
---
<center>
    <img src="assets/banner.png" style="width:850px;height:300;">
    <br>
    <div style="color:orange;
        display: inline-block;
        color: #999;
        padding: 2px;"><a href="https://xkcd.com/1432/">Copyright © xkcd</a></div>
</center>


<center>
<p style="font-family: times, serif; font-size:22pt; font-style:italic">
    By swallowing evil words unsaid, no one has ever harmed his stomach. — Winston Churchill
</p>
</center>

Everyone communicates with other people. Most of the time, the conversations will have happy endings. But sometimes, the conversations maybe go awry. This kind of conversations gone awry are more often on the internet. Due to the anonymity, online conversations are notorious for simple misunderstandings, personal attacks and antisocial behaviors.

Suppose you are a peace-loving linguist, and what you cannot tolerate are personal attacks, whether it is physical or verbal. One day, you are browsing the Wikipedia, and you find some entries should be modified or corrected. So you make some comments on the Wikipedia talk page. However, some other editors do not agree with your changes, and deny your suggestions. Hence you have a conversation with them:

<br>
<center>
    <img src="assets/conversation.png" style="width:700px;height:600;">
    <br>
    <div style="color:orange;
        display: inline-block;
        color: #999;
        padding: 2px;">Your conversation with the editors.</div>
</center>

<br>
Wow, this is so implite. This is **personal attack**!! As a linguist, you come up with a brilliant idea: can we detect such kind of unfriendly conversations on the internet automatically? Further more, is there any linguistic cues that we can use to predict whether the conversation will go awry before it actually happens?

Let's try to utilize a linguistic dataset to analyze this hypothesis. Here we are going to use the **Conversations Gone Awry Dataset**, which is a collection of conversations among Wikipedia editors from Wikipedia talk pages. In the dataset, some of the conversations will derail into personal attacks.

## Dataset Observation
Let's have a closer look at this dataset. This dataset contains 2010 **speakers**, 6363 **utterances** and 1168 **conversations**.

- Each **conversation** includes some metadata, and the most important is:
*conversation_has_personal_attack*, which indicates whether any comment in this conversation contains a personal attack according to crowdsourced annotators.
- Each **conversational turn** on the talk page is viewed as an *utterance*. For each utterance, there is also some metadata, and the most important is:
*comment_has_personal_attack*, which indicates whether this comment was judged by 3 crowdsourced annotators to contain a personal attack.
- For each **utterance**, there are some attributes:
    + id: index of the utterance
    + speaker: the speaker who author the utterance
    + conversation_id: id of the first utterance in the conversation this utterance belongs to
    + reply_to: index of the utterance to which this utterance replies to (None if the utterance is not a reply)
    + timestamp: time of the utterance
    + text: textual content of the utterance

## Linguistic Harbingers of Conversational Failure?
We want to study the predictive power of some linguistic cues on conversation failure detection. So, what kind of linguistic cues hidden in the sentences or utterances can be used? Well, we think **sentiment**, **politeness** and **talktiveness** might be able to do that. Intuitively, 

### Sentiment

### Politeness

### Talktiveness

## Predictive Power

## Conclusion



{% include plotly_test.html %}
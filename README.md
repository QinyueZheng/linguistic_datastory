**1. Title:** Linguistic Harbingers of Conversational Failure: A Case Study on an Online Strategy Game

**2. Abstract:** 
The paper has constructed the methodology to analyze linguistic betrayal based on an online game. We here want to apply this framework to a real-world social interaction, the Wikipedia “talk page wars”, to further explore its general applicability. To do so, we will use the Conversations Gone Awry Dataset, which is a collection of conversations from Wikipedia talk pages that derail into personal attacks (4,188 conversations, 30,021 comments). In our project, we mainly focus on three linguistic cues, politeness, sentiment and talkativeness. After feature calculation, we want to see whether there exist linguistic imbalance signals in the Wikipedia talk pages that can indicate a forthcoming conversational failure. This will allow us to better understand the linguistic balance and stability in conversations. Furthermore, we will test the predicting power of the framework by conducting logistic regression to see how well the linguistic features can foretell the trajectory of conversations.

**3. Research Questions:**
    1.Do there exist linguistic imbalance signals in the Wikipedia talk pages that can indicate a forthcoming conversational failure?
    2.How well can the linguistic features be used to predict the trajectory of conversations?

**4. Proposed dataset:**
***Conversations Gone Awry Dataset***  from the paper -- *Conversations gone awry: Detecting early signs of conversational failure*. This dataset is a collection of conversations among Wikipedia editors from Wikipedia talk pages (4,188 conversations, 30,021 comments). In the dataset, some of the conversations will derail into personal attacks.

Each **conversation** includes some metadata, and the most important is:
- conversation_has_personal_attack: whether any comment in this comment’s conversation contains a personal attack according to crowdsourced annotators.

Each **conversational turn** on the talk page is viewed as an utterance. For each utterance, there is also some metadata, and the most important is:
- comment_has_personal_attack: whether this comment was judged by 3 crowdsourced annotators to contain a personal attack

For each **utterance**, there are some attributes:
- id: index of the utterance
- speaker: the speaker who author the utterance
- conversation_id: id of the first utterance in the conversation this utterance belongs to
- reply_to: index of the utterance to which this utterance replies to (None if the utterance is not a reply)
- timestamp: time of the utterance
- text: textual content of the utterance

**5. Method:**
- Data collection<br>
We will get access to the dataset via [Convokit](https://convokit.infosci.cornell.edu/). To do so, we will install **convokit** via `pip` and get familiar to this tool kit.

- Feature selection and computing<br>
The linguistic cues that we are goint to use are `politeness`, `sentiment` and `talkativeness`. To compute `politeness`, we are going to use the Stanford Politeness classifer. To compute `sentiment`, we are going to use the Stanford Sentiment Analyzer. For `talkativeness`, we will simply use the number of utterances, the average number of sentences per utterance, and the average number of words per utterance.

- Data analysis<br>
Like the framework used for `Linguistic Harbingers of Betrayal`, we would like to analyze whether there exist linguistic imbalances in the selected features that signals the incoming personal attack. Besides, we will use logistic regression to test whether these linguistic cues have any predictive power and explore how good they are for the prediction.
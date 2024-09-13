+++
chapter = 1
title = 'Artificial Intelligence'
+++

This chapter provides an overview of recent A.I. trends with an emphasis on the social impact. I have tried to give you an idea of what A.I. looks like, using as little jargon as possible.

For this reason, accuracy is sacrificed. For example, if I would say:

"**✕** (is classified as ○, □, or etc., but the discussion here focuses on ○. ○) **is using △** (in most cases)."

I will have to explain about ○ and □, which is not the main point, and it gets longer and longer.
So I simply say:

"**✕ is using △**"

Please read this document with the understanding that it is such a document.

## Three factors that determine A.I. performance
{{< figure
place="right"
src="images/neuron.webp"
caption="Network image (far more complex in reality)"
>}}

The human brain functions through a vast network of neurons.
Varying the strength of the connections between neurons allows for a variety of learning and computations.
A.I. is achieved by bringing the idea of computing with a combination of simple elements of neurons into the computer.

Here are three factors that determine A.I. performance

1. network structure
2. computer resources
3. training data

The network structure is determined by how many neurons are available and how they are connected.
The network structure fundamentally determines what the A.I. can do.
Researchers are working every day to find higher-performing structures.
As researchers find a new network structure, it will determine what the A.I. can do, the computer resources required, and the content and amount of training data needed.


The network structure and computer resources are the “mechanism for learning” and the training data are the “what to learn from”.
A.I. cannot learn what is not inherently part of the training data.

## A.I. a while ago
More advanced processing requires a larger network, and
the larger the network, the more computer resources are needed.
A while ago, A.I. was for specific tasks such as image recognition, recommendations and so on.
At that time, computer performance was already high enough, but simply increasing the network size could not make A.I. smarter.
Rather, an excessively large network caused the A.I. to become stupid.
Therefore, a major focus of A.I. research topics has been to find the proper connection to achieve A.I. performance.

It is also important to prepare training data for practical A.I.
How much data will be needed depends on what is being learned, but A.I. is not a good way to learn and requires a huge amount of data.

{{< figure
place="center"
src="images/learning.en.webp"
caption="Training phase(left) and inference phase(right)"
>}}

Training an A.I. means determining the strength of the connections between the vast number of neurons so that the A.I. functions properly.
A.I. finds patterns and makes predictions on training data.
The accuracy of each prediction is then expressed as a probability, and seeks the answer that is the most likely in terms of probability.
Large amounts of training data are fed to the A.I. and the neuron connections are adjusted over and over again until the difference between the A.I.'s answer and the teacher's answer is sufficiently small.
The parameters of the trained network are called the **model**.
The **training phase** is the phase up to the creation of the model, and the phase in which the model is used is called the **inference phase**.
I have tried to avoid jargon as much as possible, but please just understand the word "model" and the image of "creation of a model by training".
<span class="footnote">
A trained model can also be viewed as a compression of all the given training data, that is, the redundancy of the data has been stripped away and converted into an essential representation of all the information that the data contains.
In this way, it can be said that the inference phase only extracts the necessary portions from all the information trained.
Knowing this will improve your outlook, but even if you don't, it will not be a problem to read this book.
If this is even more confusing, please forget this description.
</span>
The training phase is computationally demanding because it is repeated many times on a large amount of training data.
The inference phase is computationally smaller than the training phase because it is computed only once for each input.
In addition, once a trained model is available, it is replicable and used as much as desired, and we can run small-scale models even on smartphones.

## Importance of training data

{{< figure
place="right"
src="images/coco_sample.png"
caption="Example of COCO data. Labeled regions in the image are labeled to indicate the type of object."
>}}

As an example of training data, here is 
COCO(COmmon Objects in Context)<span class="footnote">
https://cocodataset.org/
</span>, a dataset for learning image recognition.
COCO provides more than 300,000 images plus data labeled to the regions in each image.
The total number of labelings is more than one million.
The sample images confirm that even the curve of the dog's feet is carefully partitioned.
These data are manually created one by one.
Imagine doing this work.
It would take a reasonable amount of time for just one image.
Doing hundreds of thousands of these would be very costly.<span class="footnote">
Technology is also advancing in which A.I. roughly draws a frame and then a human fine-tunes it.
Still, there is also the job of actually checking that the work is done properly and establishing rules to ensure that there are no differences among the people doing the work, such as how to handle cases where the object is out of sight.
Furthermore, if some problems come to light after the researcher has used the product, they may have to start over from the beginning.
</span>
<ins>Realizing A.I. requires not only researchers and engineers but also people to create training data</ins>.

Also, if the training data is biased, an A.I. will be biased.
For example, if the attributes of the photo donor (nationality, age, gender, etc.) are biased, the A.I. will learn to reflect that bias.
They must also consider how to collect data universally.
Thus, “what to learn from” is an important factor in determining A.I. performance.

## Emergence of Generative A.I.
The difficulties regarding training data are transformed by the advent of generative A.I.  
As an example, suppose we want to create an A.I. that “for a sentence with only one word blank, generates the appropriate word for that blank".
Training data for this task can be obtained in the following ways
First, we obtain a completed sentence from somewhere.
Then, if you extract a word from it, you will get a question text in which the extracted word is the "answer".
If the sentence is “I took a walk with my dog,” then the question is to guess the word in X in “I took a walk with X” and the answer “dog” can be made.
I said “dog” was the answer, but it could also be “father,” or someone might walk with a “cat.”
Nevertheless, the A.I. will learn to assume that “dog” is the “answer” for this training data.
The vast amount of training data should include “answers” other than “dog” and will be adjusted accordingly.
When learning is finally complete, the A.I. will know the probability of occurrence of the word in X in “I took a walk with X” and will know which word is the most like it.  
When generating sentences, you can create a set of questions and answers by hiding the completed sentences in the middle.
Predicting sentences seems impossible, but computers are able to push through the training with sheer volume because they can continue to do as they are told without slacking off a huge amount.  
For this reason, training data for generative A.I. can now be prepared simply by scouring the Internet for vast amounts of data.  
To achieve such learning, a large-scale sized network structure is required.
The breakthrough came with an innovative network structure that dynamically adjusts the parameters of the model based on contextual knowledge.
This dynamic adjustment allows the A.I. performance to increase as much as possible the larger the model is made.

Two of the three factors for A.I. performance have been resolved, and now it is a matter of how much computer resources to devote to it.
And indeed, ChatGPT is the result of the enormous resources that have been poured into the project.  
If you try to build a high-performance model like ChatGPT, you need to devote weeks of enormous computer resources and spend tens to hundreds of millions of dollars.
The number of neurons connected to the model is called the number of parameters.
The previous version of the ChatGPT model, GPT-3, has 175 billion parameters.
OpenAI has not disclosed details about the latest model, such as the number of parameters, but GPT-3.5 is rumored to have about 300 billion parameters and GPT-4 over 1 trillion parameters, and is expected to have cost over $100 million to train.
It takes that much just to calculate one model, so if it needs to be redone, it will cost that much more.
You all know the performance of ChatGPT, which was made possible by paying such a cost.
<span class="footnote">
OpenAI is spending over $10 billion on computer resources for the training and inference phases combined and is expected to be deeply in deficit in 2024
</span>

Another notable feature of ChatGPT is that it is known to “learn with just a little additional training”.
<span class="footnote">
2020/7/22 ["Language Models are Few-Shot Learners"](https://arxiv.org/abs/2005.14165)
</span>
As a specific application, ChatGPT has received additional training to avoid fake news and discriminatory statements.
Previously, you had to sort through the vast amount of documents on the Internet to sort out the right ones, and the A.I. had to learn them. ChatGPT can learn them all together and then tell you what's wrong afterward.  
The ability to learn in addition to the model makes it possible to create an A.I. suitable for a specific purpose at a low cost.

## A.I. in the Future
We will discuss the future of A.I. according to the three factors for A.I. performance.

#### 1. network structure
Current A.I. only generates something that looks like it probabilistically, so it may not notice if it is logically inconsistent.
Research continues to be conducted to solve such problems and to achieve an A.I. that can think more logically.
It is also expected that the range of applications of A.I. will expand as affinities with other technologies develop.

In another direction, improving efficiency is an important issue.
The ability to create high-performance A.I.s while keeping the model size constrained will lower the cost of creating A.I.s and the barrier to entry.
In addition, the ability to run the inference phase on a PC or smartphone will require a significant compression of the model size.
Efficiency has a significant impact on the scope of practical use both in terms of monetary cost and in term of energy resources.

#### 2. computer resources
Currently, the more enormous resources are consumed, the better the performance but no ceiling has yet been seen.
We can reduce the resource load if we find ways to improve efficiency in the future.  Conversely, the discovery of more advanced A.I. network structures may require even more enormous resources.

#### 3. training data
With the rise of generative A.I., it is now enough to collect training data anyway.
I predict that we are moving into an era of <ins>quality over quantity of training data</ins>.
The goal of traditional learning was to be able to do “what everyone else can do” with A.I., but I feel that such a level of learning is already coming to an end.  
It will be important for smarter A.I. to prepare good quality training data properly.

## summary
The following is summary necessary for reading the subsequent chapters.

- A.I. probabilistically derives the most plausible answer from training data.
- Training data is essential. A.I. does not know what is not inherently part of the training data, and if the training data is biased, A.I. will be biased.
- The cost of the learning phase of A.I. is high. The cost of the inference phase, which uses the models that result from the training, is much smaller.
- Models can be replicated.

# LyricsGeneration

Writing lyrics has always been a challenging task as it involves not only creativity but also inspiration. With the introduction and development of various neural network-based methodologies that have shown quite a promise in applications to a wide range other fields, it is promising to see how these new technologies can cater to the domain of musical creativity. Even though there has been significant amount of research done focusing on musical composition, it is not the same for musical song writing.
 This project demonstrates the effectiveness of Recurrent Neural Networks in an efforts to generate song lyrics. The goal of this project is to try out different model
architectures and understand how recurrent Neural networks are able to learn the
song lyric structures.
The experiments were conducted on an English Song dataset.	
In addition to that, a web-based inference tool is developed, which allows us to easily generate lyrics when we provide input.

**RNN**

A recurrent neural network (RNN) is a class of artificial neural network where
connections between units form a directed graph along a sequence. This allows it
to exhibit dynamic temporal behavior for a time sequence. Unlike feedforward
neural networks, RNNs can use their internal state (memory) to process
sequences of inputs. This makes them applicable to tasks such as unsegmented,
connected handwriting recognition or speech recognition.
Recurrent Neural Network comes into the picture when any model needs context
to be able to provide the output based on the input. Sometimes the context is the
single most important thing for the model to predict the most appropriate output.

![alt text](https://miro.medium.com/max/627/1*go8PHsPNbbV6qRiwpUQ5BQ.png)

**Problem of Long Term Dependencies**
Sometimes we only need to look at recent information to perform the present task. For example : Consider a language model trying to predict next word based on previous ones.
*PREDICT : "THE CLOUDS ARE IN ..."*
 We don't need to further context as it is obvious that the word is sky. In such cases, where the gap between the relevant information and the place that is needed to predict is small , RNN can learn to use the past information. But there can be cases where we need to remember large content to predict the next word .
 
 *PREDICT : I grew up in France .It is often described as a country with six sides. Three are coasts. The others are borders with neighbouring countries.There are mountains in which are snow-capped all year round. I speak ........."*
 
 Recent information suggests that the next word is probably the name of a language but if we want to narrow down which language, we need context of France. Therefore, it is possible that the gap between the relevant information and the point where it is needed to become very large. When gap grows, Simple RNN is unable to learn and predict correct information.
 
 Although Simple RNN should theoretically be able to retain at time t information about inputs seen many timesteps before, in practice, such long-term dependencies are impossible to learn. This is due to the vanishing gradient problem, an effect that is similar to what is observed with non-recurrent networks (feedforward networks) that are many layers deep: as we keep adding layers to a network, the network eventually becomes untrainable. The LSTM and GRU layers are designed to solve this problem.
 

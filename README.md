# TheEndlessTuning

*The Endless Tuning* by [Elio Grande](www.linkedin.com/in/elio-grande-2ba249194) (National PhD in AI & Society, University of Pisa, Italy) is a relational approach to artificial intelligence, the method of which was originally depicted in the paper [Towards a Relational Ethics in AI. The Problem of Agency, The Search For Common Principles, The Pairing of Human and Artificial Agents](https://link.springer.com/chapter/10.1007/978-3-031-76961-0_2) and further implemented in the paper [The Endless Tuning. An Artificial Intelligence Design to Avoid Human Replacement and Trace Back Responsibilities](https://arxiv.org/pdf/2507.14909) (PLEASE CITE) where human beings and artificial intelligence itself work as each other's mirror. Particularly, it consists of a design method made of just two rules:

*   the machine should in general be able to make the user reflect, the user should directly or indirectly be able to put learning constraints on the machine;
*   *every* interaction, together with useful and randomly produced information must be recorded in a permanent log (which here is just simulated as a .csv file)

The *Endless Tuning* aims to be a solution to two main artificial intelligence issues: human replacement and the so-called responsibility gap.

While the Endless Tuning might theoretically be adopted also with respect to generative artificial intelligence, here we present it in three silly protocol examples, on three decision-making settings (loan granting, art style recognition, pneumonia diagnosis). Machine's suggestions will be given by a particular use - say, a *hermeneutic* one - of eXplainability in machine learning.
In the end, you'll be able to download the .csv file of your interactions, with respect to the current sessions.

So as not to have issues with localtunnels (we are using the streamlit library), it is strongly recommended to start the runtime from zero in case you try it on Colab (see the bottom of the page). While the first cell is mainly introductive, the other cells run separately. So, f. e., you have to manually stop the execution of the "loan-granting" cell in order to run the "WikiArt" cell.

Moreover, if possible, please use a GPU runtime to get faster processing in case of WikiArt and Pneumonia versions.

To extract black boxes' explanations, the algorithms [RISE](https://github.com/eclique/RISE) and [Grad-CAM](https://github.com/jacobgil/pytorch-grad-cam) were used (last seen March 23th, 2025), but slightly modified to be optimized due to memory constraints.

A decision tree was trained on 20k applicant cases extracted from https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data, license [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0). You'll have to decide, together with suggestions coming from the algorithm, hether to grant or deny the loan to an applicant. In the end, if you'll have reached a sufficient number of new data, the algorithm will automatically retrain itself.

A ResNet50 from torchvision.models was fully finetuned on 28k artworks' images, extracted from the *WikiArt* dataset (https://www.kaggle.com/datasets/steubk/wikiart), resized with padding to 224x224 pixels and reduced to 7 classes. You'll have to decide, together with suggestions coming from the algorithm, whether the image pertains to baroque, romanticism style and so on. In the end, if you'll have reached a sufficient number of new data, the algorithm will automatically retrain itself. A ResNet34 was adopted also with 1080x1080px images, with padding.

A ResNet18 from torchvision.models was fully finetuned on 2.5k chest x-ray images extracted from the *ChestX-Ray Images (Pneumonia)* dataset (https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia), resized with padding to 224x224 pixels. You'll have to decide, together with suggestions coming from the algorithm, whether the image indicates the presence of pneumonia or not. In the end, if you'll have reached a sufficient number of new data, the algorithm will automatically retrain itself. Same done with 1080x1080px images.

[Here a jupyter notebook to test it on Google Colab](https://colab.research.google.com/drive/1m1mDWTlE5egzT_oSR18hHLlcwwrX401N?authuser=1#scrollTo=3pMgbEeXeB5X).

A single environment will be sufficient to test all the versions. See the requirements. 


## License
This code is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0).


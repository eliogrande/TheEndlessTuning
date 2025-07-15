# TheEndlessTuning

*The Endless Tuning* by [Elio Grande](www.linkedin.com/in/elio-grande-2ba249194) (National PhD in AI & Society, University of Pisa, Italy) is a relational approach to artificial intelligence, the method of which was originally depicted in the paper [Towards a Relational Ethics in AI](https://link.springer.com/chapter/10.1007/978-3-031-76961-0_2), (PLEASE CITE THIS PAPER) where human beings and artificial intelligence itself work as each other's mirror. Particularly, it consists of a design method made of just two rules:

*   the machine should in general be able to make the user reflect, the user should directly or indirectly be able to put learning constraints on the machine;
*   *every* interaction, together with useful and randomly produced information must be recorded in a permanent log (which here is just simulated as a .csv file)

The *Endless Tuning* aims to be a solution to two main artificial intelligence issues: human replacement and the so-called responsibility gap.

While the Endless Tuning might theoretically be adopted also with respect to generative artificial intelligence, here three silly protocol examples follow, on three decision-making settings (loan granting, art style recognition, pneumonia diagnosis). Machine's suggestions will be given by a particular use - say, a *hermeneutic* one - of eXplainability in machine learning.
In the end, you'll be able to download the .csv file of your interactions, with respect to the current sessions.

So as not to have issues with localtunnels (we are using the streamlit library), it is strongly recommended to start the runtime from zero. While the first cell is mainly introductive, the other cells run separately. So, f. e., you have to manually stop the execution of the "loan-granting" cell in order to run the "WikiArt" cell.

Moreover, if possible, please run the cells within a GPU runtime to get faster processing in case of WikiArt and Pneumonia versions.

To extract black boxes' explanations, the algorithms [RISE](https://github.com/eclique/RISE) and [Grad-CAM](https://github.com/jacobgil/pytorch-grad-cam) were used (last seen March 23th, 2025).

# csci544-homework-2-solved
**TO GET THIS SOLUTION VISIT:** [CSCI544 Homework 2 Solved](https://www.ankitcodinghub.com/product/csci544-homework-2-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91255&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI544 Homework 2 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Introduction

The goal of this assignment is to get some experience with sequence labeling. Specifically, you will be assigning dialogue acts to sequences of utterances in conversations from a corpus. In sequence labeling it is often beneficial to optimize the tags assigned to the sequence as a whole rather than treating each tag decision separately. With this in mind, you will be using a machine learning technique, conditional random fields, which is designed for sequence labeling. You will be using the toolkit, CRFsuite.

The raw data for each utterance in the conversation consists of the speaker name, the tokens and their part of speech tags. Given a labeled set of data, you will first create a baseline set of features as specified below, and measure the accuracy of the CRFsuite model created using those features. You will then experiment with additional features in an attempt to improve performance. The best set of features you develop will be called the advanced feature set. You will measure the accuracy of the CRFsuite model created using those features. Your programs should also be able to assign dialogue act tags to unlabeled data. We will use your code to evaluate your baseline and advanced features on unseen test data.

Data

The Switchboard (SWBD) corpus was collected from volunteers and consists of two person telephone conversations about predetermined topics such as child care. SWBD DAMSL refers to a set of dialogue act annotations made to this data. This (lengthy) annotation manual defines what these dialogue acts mean. In particular, see section 1c (The 42 Clustered SWBD-DAMSL Labels). Note, the statistics in this manual use a different training set than our experiments here but give you a rough idea of how frequently each dialogue act appears. We recommend that you skim the annotation manual to get an understanding of what the tags mean and help you think of good features.

If you have a question about the corpus and can’t find an answer in the annotation manual, please post on Piazza or ask a TA or instructor. DO NOT use resources from the web other than the annotation manual.

Download a zip file from Blackboard of SWBD dialogues labeled with SWBD-DAMSL dialogue acts. Individual conversations are stored as individual CSV files. These CSV files have four columns and each row represents a single utterance in the conversation. The order of the utterances is the same order in which they were spoken. The columns are:

• act_tag – the dialogue act associated with this utterance. Note, this will be blank for the unlabeled test data we use to test your code.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ul>
<li>speaker – the speaker of the utterance (A or B).</li>
<li>pos – a whitespace-separated list where each item is a token, “/”, and a part of speech tag (e.g., “What/WP are/VBP your/PRP$ favorite/JJ programs/NNS ?/.”). When the utterance has no words (e.g., the transcriber is describing some kind of noise), the pos column may be blank, consist solely of “./.”, have a pos but no token, or have an invented token such as MUMBLEx. You can view the text column to see the original transcription.</li>
<li>text – The transcript of the utterance with some cleanup but mostly unprocessed and untokenized. This column may or may not be a useful source of features when the utterance solely consists of some kind of noise.
You will also notice a Python file hw2_corpus_tool.py included with the data. We have written this code to help you read the data. You should use this code to ensure that you will be reading the test files in the proper order. You should include the code with your submission to ensure that it imports smoothly when we grade your programs. Read the documentation in the file for more information or use Python’s help() function.

CRFsuite

You will need to install pycrfsuite (https://pypi.python.org/pypi/python-crfsuite), a Python interface to CRFsuite (http://www.chokkan.org/software/crfsuite/). As discussed in the CRFsuite tutorial, and the pycrfsuite tutorial, you add training data to the Trainer object using the append method which takes two arguments (feature_vector_list,label_list) and loads the training data for a single sequence. In our case, each sequence corresponds to a dialogue, and the feature_vector_list is a list of feature vectors (one for each utterance in the dialogue). The label_list corresponds to the dialogue acts for those utterances. Each feature vector is a list of individual features which are binary. The presence of a feature indicates that it is true for this item. Absence indicates that the feature would be false. Here are the features for a training example using features for whether a particular token is present or not in an utterance.

[‘TOKEN_i’, ‘TOKEN_certainly’, ‘TOKEN_do’, ‘TOKEN_.’]

After loading the training data, you need to set the CRFsuite training parameters. The following parameters are taken from the pycrfsuite tutorial. You are not expected to optimize these hyper parameters. The official solution will use these hyper parameters so it is safer to use them given the unseen test data. The max_iterations parameter is particularly important to keep training times reasonable. We will talk more about conditional random fields and these parameters in class.
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
trainer.set_params({

‘c1’: 1.0, # coefficient for L1 penalty ‘c2’: 1e-3, # coefficient for L2 penalty ‘max_iterations’: 50, # stop earlier

# include transitions that are possible, but not observed }) ‘feature.possible_transitions’: True

The last step is to train the model using the train method which takes a single argument, the name of the file in which to save the model. As discussed below, the two programs you will submit will both train models and use them to tag data. Thus, you can give the model whatever name you like because you will be creating a Tagger object and using its open method to read the model. The tag method of the Tagger object processes a single sequence at a time (i.e., one dialogue) represented as a list of feature value vectors (i.e., one per utterance) in the same format used by the Trainer object. The tagger will output a list of labels (i.e., dialogue acts): one per utterance. You will need to print them one per line with a blank line separating sequences/dialogues. It is okay to print a blank line after the last dialogue.

For labeled data, you will also be able to generate a true label list for the utterances of each dialogue, compare to the tagger output and at the end print an accuracy score which you will need to complete your report. However, your programs should be robust and handle unlabeled data (i.e., skip calculating and printing accuracy but continue to output the label list generated by the tagger).

What to do

You will be writing two dialogue act taggers for SWBD DAMSL. You will use your labeled data to debug them and pick the best features for the “advanced” tagger. You could simply split the labeled data by randomly putting roughly 25% of the data in the development set and using the rest to train your classifier. In this case, you would include entire conversations in either the training or development sets. In this assignment, it is up to you how you use your labeled data to evaluate different features. You could use a certain percentage of conversations for development, or you could use k-fold cross-validation.

You should try a set of features that we’ll call baseline. In the baseline feature set, for each utterance you include:

<ul>
<li>a feature for whether or not the speaker has changed in comparison with the previous utterance.</li>
<li>a feature marking the first utterance of the dialogue.</li>
<li>a feature for every token in the utterance (see the description of CRFsuite for an
example).
</li>
<li>a feature for every part of speech tag in the utterance (e.g., POS_PRP POS_RB POS_VBP POS_.).</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
You’ll need to create a Python program (baseline_tagger.py) that reads in a directory of CSV files (INPUTDIR), trains a CRFsuite model, tags the CSV files in (TESTDIR), and prints the output labels to OUTPUTFILE

&gt;python3 baseline_tagger.py INPUTDIR TESTDIR OUTPUTFILE

You should try at least one other set of features that we’ll call advanced. The advanced feature set should include more information than the baseline feature set. The idea is that you want to improve performance. As discussed in the grading section, part of your grade depends on developing a feature set better than the baseline. You’ll need to create a Python program (advanced_tagger.py) that reads in a directory of CSV files (INPUTDIR), trains a CRFsuite model using the advanced features, tags the CSV files in (TESTDIR), and prints the output labels to OUTPUTFILE

&gt;python3 advanced_tagger.py INPUTDIR TESTDIR OUTPUTFILE

Your programs, baseline_tagger.py and advanced_tagger.py, will need to be able to tag CSV files with blank labels as well as labeled development data.

</div>
</div>
</div>

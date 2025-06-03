# 🧠 Weka from the Command Line: Beach Dataset

A quick guide for running operations on an ARFF file using Weka's command-line interface.

---

## 📊 1. View Dataset Summary

Print metadata about the dataset (number of attributes, types, instances, etc.):

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.core.Instances beach.arff

### 🔎 Example Output:

    Relation Name:  beach
    Num Instances:  16
    Num Attributes: 3

        Name          Type  Nom  Int Real     Missing  Unique  Dist
    1   condition     Nom  100%   0%   0%        0%       3      3
    2   temperature   Num    0% 100%   0%        0%      15     15
    3   class         Nom  100%   0%   0%        0%       2      2

---

## 👀 2. View First Few Instances

Use a filter to remove all rows after the first 4:

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.filters.unsupervised.instance.RemoveRange -R 5-last -i beach.arff

### ✂️ Output:

    @relation beach-weka.filters.unsupervised.instance.RemoveRange-R5-last

    @attribute condition {Sunny,Cloudy,Raining}
    @attribute temperature numeric
    @attribute class {Yes,No}

    @data
    Sunny,85,Yes
    Sunny,75,Yes
    Cloudy,95,Yes
    Cloudy,60,No

---

## 🌲 3. Run a Classifier

Train a simple J48 decision tree classifier:

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.classifiers.trees.J48 -t beach.arff

This builds a model using the ARFF file and outputs the decision tree and evaluation.

---

## 📈 4. Get Attribute Statistics

Run basic stats (e.g. mean, stddev) on numeric attributes:

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.filters.unsupervised.attribute.NumericTransform -i beach.arff

*(Note: `weka.experiment.Stats` does not output to console directly — use filters or classifiers for visible stats.)*

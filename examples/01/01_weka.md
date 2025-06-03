# 🧠 Weka from the Command Line: Iris Dataset

This guide walks you through using [Weka](https://www.cs.waikato.ac.nz/ml/weka/) from the command line. You'll learn to train and evaluate classifiers using the built-in **Iris** dataset.

---

## ⚙️ Setup

### 1. Install Weka

**Download here:**  
[https://sourceforge.net/projects/weka/](https://sourceforge.net/projects/weka/)

### 2. Open Command Prompt and Change Directory

    cd "C:\Program Files\Weka-3-8-6"
    dir

You should see files like:

- `weka.jar`
- `data\` (containing datasets like `iris.arff`)
- `.dll`, `.exe`, and `.bat` files

---

## 🧪 Step-by-Step: Train and Evaluate Classifiers

We'll use the `iris.arff` dataset located in `data\`.

---

### ▶️ Step 1: Run J48 (Decision Tree) on Iris Dataset

    java -cp weka.jar weka.classifiers.trees.J48 -t data\iris.arff

#### ✅ You should see output like:

- The decision tree structure
- Accuracy and error metrics
- Confusion matrix
- 10-fold cross-validation results (default behavior)

<details>
<summary>Example Output</summary>

    === Run information ===
    Scheme:       weka.classifiers.trees.J48
    Relation:     iris
    Instances:    150
    Attributes:   5
                  sepallength
                  sepalwidth
                  petallength
                  petalwidth
                  class
    Test mode:    10-fold cross-validation

    === Classifier model (full training set) ===

    J48 pruned tree
    ------------------

    petallength <= 2.45: Iris-setosa (50.0)
    petallength > 2.45
    |   petalwidth <= 1.75
    |   |   petallength <= 4.95
    |   |   |   petalwidth <= 1.65: Iris-versicolor (47.0)
    |   |   |   petalwidth > 1.65: Iris-virginica (1.0)
    |   |   petallength > 4.95: Iris-virginica (3.0)
    |   petalwidth > 1.75: Iris-virginica (49.0)

    Number of Leaves  :     5

    Size of the tree :  9

    === Stratified cross-validation ===
    Correctly Classified Instances        144               96%
    Incorrectly Classified Instances        6                4%
    Kappa statistic                          0.94
    Mean absolute error                      0.03
    Root mean squared error                  0.16
    Relative absolute error                  6.48 %
    Root relative squared error             32.31 %
    Total Number of Instances              150

</details>

---

## 📚 More Classifiers to Try

### Naive Bayes

    java -cp weka.jar weka.classifiers.bayes.NaiveBayes -t data\iris.arff

### Random Forest

    java -cp weka.jar weka.classifiers.trees.RandomForest -t data\iris.arff

### Logistic Regression

    java -cp weka.jar weka.classifiers.functions.Logistic -t data\iris.arff

---

## 📂 Train/Test Split Instead of Cross-Validation

Use `-split-percentage` with `-x` or `-T`:

### Example: 70% Train, 30% Test

    java -cp weka.jar weka.classifiers.trees.J48 -t data\iris.arff -split-percentage 70

---

## ✅ Tips

- Add `-i` to display detailed results:
  
      java -cp weka.jar weka.classifiers.trees.J48 -t data\iris.arff -i

- Output model to file:
  
      java -cp weka.jar weka.classifiers.trees.J48 -t data\iris.arff -d j48.model

- Use a saved model to classify new instances:
  
      java -cp weka.jar weka.classifiers.trees.J48 -l j48.model -T data\iris.arff -i

---

## 🧼 Clean Output

Use `-o` for a more compact summary (no model dump):

    java -cp weka.jar weka.classifiers.trees.J48 -t data\iris.arff -o

---

## 💡 Resources

- Weka Manual: https://waikato.github.io/weka-wiki/documentation/
- Classifier Options: Add `--help` to any classifier

      java -cp weka.jar weka.classifiers.trees.J48 --help

---

## 🛠️ Troubleshooting

- **Command not recognized?** Make sure you are in the directory with `weka.jar`.
- **Can't find file?** Use absolute paths or check if paths have spaces.
- **Java not installed?** Install [Java JDK](https://www.oracle.com/java/technologies/javase-downloads.html).

---

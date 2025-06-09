# 🧠 Weka from the Command Line: Applying Filters 

## 🧰 Requirements:
Ensure Weka is installed and accessible from the command line (`java -cp weka.jar weka.filters.unsupervised.attribute.Remove` should work).

## Remove an Attribute

### 🧪 Apply the `Remove` Filter via CLI

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.filters.unsupervised.attribute.Remove -R 3 -i weather.nominal.arff -o weather.nominal.filtered.arff

✅ This should:

- remove the 3rd attribute (humidity) from `weather.nominal.arff`
- write the cleaned version to `weather.nominal.filtered.arff`

### 🧪 How to Verify
You can open the `.filtered.arff` file in Notepad or VS Code and confirm that the humidity attribute is gone.

### 💡 Tip: For Reuse
If you're doing this often, consider defining an environment variable or alias in PowerShell for easier use:

    $wekaJar = "C:\Program Files\Weka-8-6\weka.jar"
    java -cp $wekaJar weka.filters.unsupervised.attribute.Remove -R 3 -i weather.nominal.arff -o weather.nominal.filtered.arff

## Remove an Instance

### ✅ PowerShell Command to Remove Instances with `humidity = high`

    java -cp "C:\Program Files\Weka-3-8-6\weka.jar" weka.filters.unsupervised.instance.RemoveWithValues -C 3 -L 1 -i weather.nominal.arff -o weather.nominal.filtered2.arff

### 📘 Explanation of Parameters

| Parameter          | Description                                              |
| ------------------ | -------------------------------------------------------- |
| `-cp`              | Points to your `weka.jar`                                |
| `RemoveWithValues` | The filter that removes rows (instances) based on values |
| `-C 3`             | Attribute index 3 (which is `humidity`)                  |
| `-L 1`             | Nominal value index 1 (i.e., `high`)                     |
| `-i`               | Input dataset                                            |
| `-o`               | Output filtered dataset                                  |

### 🔍 Optional: Preview ARFF Value Indices

If you're unsure which value maps to which index in a nominal attribute (e.g., `1 = high`, `2 = normal`), you can open the ARFF file in a text editor. The `@attribute` line will show:

    @attribute humidity {high,normal}


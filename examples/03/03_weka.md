# 🧠 Weka from the Command Line

## 🟡 1. `weather.nominal` — Values of the attribute `temperature`

    Select-String -Pattern 'temperature' -Path .\weather.nominal.arff

### Output:

    weather.nominal.arff:4:@attribute temperature {hot, mild, cool}

## 🔍 2. `iris` — How many instances does this dataset have?

    Get-Content .\iris.arff | Where-Object {
        $_ -and -not ($_.Trim().StartsWith("@")) -and -not ($_.Trim().StartsWith("%"))
    } | Measure-Object

### Output:

    Count    : 150

## 🔍 3. `iris` — How many attributes does this dataset have?

    Get-Content .\iris.arff | Select-String -Pattern '^@attribute ' | Measure-Object

### Output:

    Count    : 5

## 🔍 4. `iris` — What is the range of possible values of the attribute petallength?

### Output:

    Maximum  : 6.9
    Minimum  : 1
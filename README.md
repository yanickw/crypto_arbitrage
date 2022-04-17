# Crypto Arbitrage
*CRYPTO ARBITRAGE* is a Financial analysis tool sorting historical data between two exchanges to find arbitrage opportunity.

---

## Requirements

This application was writen in Jupyter Lab 3.3.2 using Python 3.9.7

**Operating System:**
* Window 10 (or higher) using Gitbash.
* MacOS 10.14 (or higher) using a terminal.
* Linux Ubuntu 20.04 (or higher) using a terminal.

**Will need to be installed:**

*jupyter lab* 3.3.2
```
$ pip install jupyterlab
```

*pandas* 1.4.2

```
$ pip install pandas
```

*pathlib* 1.0.1

```
$ pip install pathlib
```

*matplotlib* 0.1.3

```
$ pip install matplotlib
```
---

## Installation

To install the application you will need to clone the GitHub repository.

```
$ git clone https://github.com/yanickw/crypto_arbitrage
```

---

## Get Started

Using the *Crypto Arbitrage*:

Open a gitbash, navigate to your github cloned repositery. Start *Jupyter Lab*
```
$ jupyter lab
```

### 1. Import and collect the data
Once the Jupyter Lab application running, you will need to link your dataframes (.csv) accessed from a relative path location in the /Resources folder.

```
# Import the data by reading in the CSV file and setting the DatetimeIndex.
<name of dataframe> = pd.read_csv(Path("./Resources/<new file>.csv"),
                           index_col = "<date column name>",
                           parse_dates = True,
                           infer_datetime_format = True)
```

### 2. Prepare the data
Series process to clean both dataframe for analysis.
1. Using `.dropna` fonction replace and drop all NaN or missing data.
2. Using `.str.replace` to take out "$" signs.
3. Using `.astype("float")` to make all data to float.
4. Verify for duplicates and drop them if any.

### 3. Analyze the Data
After getting the summary statistic and visualize the data we then aim our focus on the analysis of specific dates to run an arbitrage profits simulation.

### 4. Calculate the Arbitrage Profits
First order of business is to mesure the arbitrage spread. Followed by the spread returns which leads us to find the positive returns exceeding 1% minimum threshold that we need to cover our costs. The following steps calculates the potential arbitrage profits on each days. Finally, we total the cumulative sum using the `.cumsum` and visual graph of the results.

---

## Contributors

This application originated from a Berkeley Bootcamp.

For any inquieries, feedbacks or comments about this project please email me at yanickw@gmail.com

I can also be reached on [LinkedIn](https://www.linkedin.com/in/yanickwilisky/)
or  [Twitter](https://twitter.com/yanickwilisky).

---

## License

MIT License

Copyright (c) 2022 Yanick Wilisky

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

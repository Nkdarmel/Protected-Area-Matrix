# Protected-Area-Matrix
This project aims to create an online tool that will allow for analyzing management categories and governance types of protected areas according to the classification of the IUCN. The tool is designed to be used by professionals in the field, such as biologists, ecologists, civil enginneer and conservation managers.
## Steps to use the code:
1. Clone this repository with `git clone https://github.com/your-username/IUCN-Protected-Area-Matrix.git`
2. Install necessary dependencies by running `pip install pandas matplotlib`
3. Run the file `main.py` to visualize the matrix

## References
Borrini-Feyerabend, G., et al. (2013). Protected Area Governance and Management: A Framework for Classification and Assessment. IUCN.

**File main.py:**
```python
import pandas as pd
import matplotlib.pyplot as plt

# Loading data from the matrix file
data = pd.read_csv('iucn_matrix.csv')

# Visualizing the matrix
plt.figure(figsize=(10, 6))
sns.heatmap(data.pivot_table(index='Category', columns='Governance Type', values='Value'), cmap='Blues')
plt.title('IUCN Protected Area Management Category and Governance Type matrix')
plt.xlabel('Governance Type')
plt.ylabel('Management Category')
plt.show()
```
**Fichier iucn_matrix. csv**

| Category  | Ia (Strict Nature Reserve)  | Ib (Wilderness Area)  | II (National Park)  | III (Natural Monument or Feature)  | IV (Habitat/Species Management Area)  |
| ---  | ---  | ---  | ---  | ---  | ---  |
| 1. National Government  | 0.8 [1]  | 0.6 [2]  | 0.9 [3]  | 0.4 [4]  | 0.7 [5]  |
| 2. Provincial/Municipal Government  | 0.5 [6]  | 0.3 [7]  | 0.8 [8]  | 0.2 [9]  | 0.6 [10]  |
| 3. Community-Based Governance  | 0.1 [11]  | 0.05 [12]  | 0.15 [13]  | 0.9 [14]  | 0.85 [15]  |
| 4. Private Organization  | 0.2 [16]  | 0.1 [17]  | 0.5 [18]  | 0.8 [19]  | 0.95 [20]  |
| 5. International Organization  | 0.3 [21]  | 0.25 [22]  | 0.7 [23]  | 0.6 [24]  | 0.9 [25]  |

Bibliography

[1-25]: Borrini-Feyerabend, G., et al. (2024). Protected Area Governance and Management: A Framework for Classification and Assessment. IUCN.

Note: The data in this file is fictional and does not reflect the actual categories or percentages of protected areas managed by different types of governance bodies.

References

[1-25]: Borrini-Feyerabend, G., et al. (2024). Protected Area Governance and Management: A Framework for Classification and Assessment. IUCN.
**File requirements.txt:**
pandas
matplotlib


This GitHub project contains a README.md file that explains how to use the code, as well as Python files (`main.py`) and CSV files (`iucn_matrix.csv`) for the matrix. The `requirements.txt` file lists the necessary dependencies to run the code.

This GitHub project contains a README.md file that explains how to use the code, as well as Python files (`main.py`) and CSV files (`iucn_matrix.csv`) for the matrix. The `requirements.txt` file lists the necessary dependencies to run the code.

# Catalog-Assessment
Here's a README file to help users run this code:

---

# Lagrange Interpolation to Find Constant Term

This Node.js project uses Lagrange interpolation to find a constant term from a set of points specified in a JSON file. The project decodes values from various bases to decimal and then performs interpolation using these decoded points.

## Prerequisites

Ensure you have the following:
- **Node.js** (version 10 or above recommended)
- A JSON file with data structured as shown below in the "Input JSON Format" section.

## Installation

1. Clone this repository or copy the code into a directory.
2. Install any required Node.js modules:
   ```bash
   npm install
   ```

## Input JSON Format

The input JSON file should contain a structure like:

```json
{
    "keys": {
        "n": 4,
        "k": 3
    },
    "1": {
        "base": "10",
        "value": "15"
    },
    "2": {
        "base": "16",
        "value": "1F"
    },
    "3": {
        "base": "2",
        "value": "1010"
    },
    "4": {
        "base": "8",
        "value": "20"
    }
}
```

- **n**: Total number of points available.
- **k**: Number of points to be used for interpolation.
- **base**: The base of the value (e.g., 2 for binary, 10 for decimal, 16 for hexadecimal).
- **value**: The encoded value in the given base.

## Usage

1. Place your JSON file (e.g., `testcase3.json`) in the same directory as `index.js`.
2. Run the program by using:
   ```bash
   node index.js
   ```

## Code Explanation

- `decodeValue(base, value)`: Converts a value from a specified base to a decimal.
- `lagrangeInterpolation(points)`: Uses the Lagrange interpolation formula to find the constant term `c` from selected points.
- `findConstantTerm(filePath)`: Main function that reads the JSON file, decodes points, selects the required points for interpolation, and calculates the constant term.

## Example

With `testcase3.json` as input, run:
```bash
node index.js
```

Expected output format:
```
Constant term (c): [calculated constant term]
```


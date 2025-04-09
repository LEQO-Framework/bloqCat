# BloQCat

This service is used for aggregating Quantumcomputing Pattern concrete solutions.

Features

QASM3 Parsing: Parses quantum circuits written in OpenQASM 3 format.

Circuit Combination: Supports merging and optimizing multiple QASM3 circuits.

Custom Operations: Allows injecting custom quantum gates and transformations.

Error Handling & Validation: Ensures circuit integrity and compliance with QASM3 standards.

API Support: Provides an API for interacting with circuit processing functions.

Installation

Ensure you have Python 3.8+ installed. Then, clone the repository and install dependencies:
# Clone the repository
git clone https://github.com/your-org/LEQO-Framework.git
cd LEQO-Framework/bloqCat-modeling

# Install dependencies
pip install -r requirements.txt
---

This project is based on the [flask-template](https://github.com/buehlefs/flask-template) project. The template documentation can be found in `docs/templatedocumention.md`

---
## Development
1. to install the dependencies run

    ```bash
    poetry install
    ```
1. start the service with
    ```bash
    poetry run flask run
    ```

Contribution Guidelines

Fork the repository and create a new branch.

Ensure your changes pass all tests.

Submit a pull request with a clear description.

## Disclaimer of Warranty

Unless required by applicable law or agreed to in writing, Licensor provides the Work (and each Contributor provides its
Contributions) on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including,
without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
PARTICULAR PURPOSE. You are solely responsible for determining the appropriateness of using or redistributing the Work
and assume any risks associated with Your exercise of permissions under this License.

## Haftungsausschluss

Dies ist ein Forschungsprototyp. Die Haftung für entgangenen Gewinn, Produktionsausfall, Betriebsunterbrechung,
entgangene Nutzungen, Verlust von Daten und Informationen, Finanzierungsaufwendungen sowie sonstige Vermögens- und
Folgeschäden ist, außer in Fällen von grober Fahrlässigkeit, Vorsatz und Personenschäden, ausgeschlossen.

## Acknowledgements

The initial code contribution has been supported by the
project [SeQuenC](https://www.iaas.uni-stuttgart.de/forschung/projekte/sequenc/).


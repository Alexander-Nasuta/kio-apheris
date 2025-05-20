<div id="top"></div>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <a>
    <img src="./resources/logo-optipack.svg" alt="Logo" height="180">
  </a>


  <h1 align="center">
     Minimalistic Machine Learning Example for Optimized Machine Parameterization in Recycled Plastic Packaging
  </h1>


</div>

# About The Project 

This repository contains a minimalistic example of a machine learning model for optimized machine parameterization in recycled plastic packaging. 
The goal is to predict the temperature, time, and pressure required for the thermoforming process based on various input features related to the material and machine configuration.

# Dataset

The dataset contains labeled datapoints related to material validation processes for thermoforming equipment. Each datapoint reflects a specific use case or validation scenario, including information on the material used, equipment configuration, validation method, and outcome.

Thermoforming machine manufacturers typically offer a predefined material portfolio aligned with their equipment specifications. Converters can select suitable materials based on the intended application. To ensure contractual performance targets are met, manufacturers validate the machine's efficiency using standard materials. Using alternative materials is generally at the converter's own risk. However, some manufacturers support formal validation of unapproved materials—either through practical testing on identical or comparable machines or via structured methods such as Design of Experiments (DOE). These validation processes are typically completed within one day based on prior experience.

Each datapoint captures the relevant parameters and results from these validation efforts.

```python
{
    "ListeKomponenten": ["K000055", "K000057"],  // List of materials (id or material name)
    "Massenanteile": [0.5, 0.5],  // mass ratios of the materials (unit: g/g)
    "Flächenanteilmodifiziert": 0,  // modified surface (unit: %)
    "Geometrie": "Quader",  // geometry (unit: list of types)
    "Kopfraumatmosphäre": None,  // headspace atmosphere (unit: Pa)
    "Masse": None,  // mass (unit: g)
    "Verpackungstyp": "Folie",  // packaging type
    "CAD": None,  // link to CAD file
    "RauheitRa": 0.08666666666666667,  // roughness Ra (unit: µm)
    "RauheitRz": 0.924,  // roughness Rz (unit: µm)
    "Trübung": 216.1,  // haze (unit: HLog)
    "Glanz": 36.7,  // gloss (unit: GE)
    "Dicke": 738.6666666666666,  // thickness (unit: µm)
    "Emodul": 807.9225728004443,  // elastic modulus (unit: MPa)
    "MaximaleZugspannung": 33.22942107172407,  // maximum tensile stress (unit: MPa)
    "MaximaleLängenänderung": 14.57795412214027,  // maximum elongation (unit: %)
    "Ausformung": 1,  // forming process rating  (unit: class (1 to 6))
    "Kaltverfo": 1,  // cold forming rating (unit: class (1 to 3))
    "Temp": 300,  // [LABEL] temperature (unit: °C) 
    "Zeit": 12,  // [LABEL] time (unit: s)
    "Druck": 4.33  // [LABEL] pressure (unit: bar)
}
```
Temperature (`"Temp"`), time (`"Zeit"`), and pressure (`"Druck"`) are the target variables for the machine learning model.


# Running the Code

0. create a python environment with the required packages. here is an example with conda:
   ```bash
   conda create -n kio-apheris python=3.11
   conda activate kio-apheris
   ```

1. Clone the repository:
   ```bash
   git clone 
   ```

2. Install the code locally (this will also install the dependencies):
   ```bash
   pip install -e .
   ```

3. Run the code:
   ```bash
   python ./src/openhub/ml_code_standalone.py
   ```


## Contact

If you have any questions or feedback, feel free to contact me via [email](mailto:alexander.nasuta@wzl-iqs.rwth-aachen.de) or open an issue on repository.
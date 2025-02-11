![Version](https://img.shields.io/badge/version-0.0.1-blue)
[![license](https://img.shields.io/badge/license-AGPL%20V3-blue)](https://github.com/QUEL-Imaging/mcx-exeml/blob/main/LICENSE)
# MCX-ExEM: MCX Excitation Emission
Welcome to **mcx-exem**! 

## Getting Started


### Prerequisites
- **MCX** v2024.1 with GPU


## Running MCX
- **num_photons**: Number of photons to use in MCX, MCX-ExEm simulations used 10^7
- **file_id**: Input filename for Simulation 1 JSON file with geometry and optical property inputs
- **output_file**: Output filename for results for Simulation 1 (output = 3D energy volume)

### Simulation 1: Excitation
```
mcx -A 1 -n \"num_photons\" -f \""file_id".json\"  -s \"output_file\" -B rrrrrr000000 -S 1 -O E -X 1 -b 1 -F jnii"
```

### Simulation 2: Emission
- **num_photons2**: Number of photons to use in MCX, MCX-ExEm simulations used 10^7
- **file_id2**: Filename for Simulation 2 JSON file with geometry and optical property inputs
- **output_file2**: Output filename for results for Simulation 1 (output = 3D fluence volume with diffuse reflectance layer)

```
mcx -A 1 -n \"num_photons2\" -f \""file_id2".json\"  -s \"output_file2\" -B rrrrrr000000 -S 1 -O F -X 1 -U 0 -b 1 -F jnii"
```

## License
The source code in this repository is licensed under the [GNU Affero General Public License v3.0 (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html). 


### Notes
- If you contribute to this repository, you agree that your contributions to the source code will be licensed under AGPL-3.0.
- Please ensure compliance with this license when using or modifying the content of this repository.

## Funding
This work is partially funded by the NIH and ARPA-H:
- **NCI** Contract 75N91021C00035
- **NCI/ARPA-H** Contract 75N91023C00052
- **NIBIB** Grants R43/44 EB029804

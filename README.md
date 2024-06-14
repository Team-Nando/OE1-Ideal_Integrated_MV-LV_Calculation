# Assessment of Integrated MV-LV OE Calculations to Orchestrate DERs - OE Algorithm 1: Ideal

This repository is part of the project [Accelerating the Implementation of Operating Envelopes Across Australia](https://electrical.eng.unimelb.edu.au/power-energy/projects/accelerating-the-implementation-of-operating-envelopes-across-australia) funded by CSIRO. This project provided key metrics, recommendations, and guidance for distribution companies (known as Distribution Network Service Providers [DNSPs] in Australia) and AEMO (the Australian system operator) to assist them in improving and, hence, accelerating the use of Operating Envelopes (OEs) across Australia.

In this repository, we use interactive code via Jupyter Notebook and Python as well as a [realistic integrated medium voltage and low voltage (MV-LV) network](https://github.com/Team-Nando/MV-LV-Networks) to demonstrate the process and necessary calculations for the *Ideal OE Algorithm with Integrated MV-LV Calculations* produced by The University of Melbourne. This demonstration is useful for different stakeholders (e.g., DNSPs, AEMO, CSIRO, regulators, consultancy companies, technology providers) as it can help them familiarise with the corresponding algorithm and the required inputs as well as the pros and cons.

## Ideal OE with Integrated MV-LV Calculations
The Ideal OE with Integrated MV-LV Calculations is the most advanced and, hence, the most accurate OE approach as it uses power flows to carry out calculations. However, it needs a full MV-LV electrical network model, full monitoring of customers, and monitoring at the MV head of feeders, which make its implementation complex and likely impractical. But if the electrical model and monitoring data are all correct, this approach can produce OEs for flexible customers that can ensure the adequate operation of the MV-LV network within technical limits (i.e., voltage and thermal). Therefore, this operating envelope is used as a benchmark for the simpler ones studied in the project.
- Required Monitoring: At MV head of feeders (V, I, P, and Q, all per phase), at all customers (net demand P and Q).
- Required Electrical Models: Full three-phase integrated MV-LV electrical network model.

## Pre-Requisites
- Python (Anaconda) and Jupyter Notebook (comes with Anaconda). For download links and more info: https://www.anaconda.com/download. Note that you must install the Anaconda that is compatible with your operating system (e.g., Windows, Mac). Also note that this repository is meant to be used by individuals (who can get free access to Anaconda).
- dss_python module. We use this Python-native module to run power flows based on OpenDSS (https://sourceforge.net/projects/electricdss/). To install, run `pip install dss_python` in the Anaconda Prompt. For more info: https://github.com/Team-Nando/Tutorial-DERHostingCapacity-0-dss_python#part-0-using-dss_python.
- To guarantee that you have all the necessary packages you can also run the **`requirements.txt`** file using **`pip install -r requirements.txt`** in the Anaconda prompt.

## Run the Code
Make sure you have installed all the pre-requisites (Anaconda, dss_python, requirements). Otherwise, you will not be able to go through the repository.

1. Download all the files using the green **`<> Code`** button at the top right.
   - You will get a ZIP file with a folder that contains all the files.
   - Unzip the file and place the folder somewhere on your computer/laptop.
2. To open the Jupyter Notebook file (extension **`ipynb`**) you need to:
   - Open Anaconda Navigator
   - Click on Launch Jupyter Notebook (it will open in your browser)
   - Upload the unzipped folder (with all the corresponding files) to Jupyter Notebook (the location is up to you)
   - Go inside the folder and open the **`ipynb`** file

All the instructions will be in the **`ipynb`** file.

## Credits
Arthur Gonçalves Givisiez (a.goncalvesgivisiez@unimelb.edu.au)

Nando Ochoa (luis.ochoa@unimelb.edu.au ; https://sites.google.com/view/luisfochoa)

## Acknowledgements
We acknowledge AusNet Services for providing the data listed below, which was essential to create this repository.
- Anonymised historical active power demand of some customers (smart meter data)
- The data (i.e., topology, impedances, distribution transformers) of one of their MV feeders (indirectly used by this repository)

More details of this data can be found in the [Team Nando GitHub repository for Australian MV-LV Networks](https://github.com/Team-Nando/MV-LV-Networks), files named "Network_4_Urban_CRE21" and "Profiles".
 
We also acknowledge the Australian Bureau of Meteorology for providing the solar radiation data.

## Licenses
Since this repository uses dss_python which is based on OpenDSS, both licenses have been included. This repository uses the BSD 3-Clause "New" or "Revised" license. Check all corresponding files (`LICENSE-OpenDSS`, `LICENSE-dss_python`, `LICENSE`).

# AQUASET (Affective Physiological QUAlity-of-Experience Streaming service dataSET)

## Dataset

AQUASET is a multimodal dataset for Quality of Experience (QoE)
estimation in adaptive video streaming using affective computing.

## Description

AQUASET contains objective, subjective, physiological, and affective
data collected during video streaming experiments with dynamic
quality variations.

## Dataset Access

The complete dataset is available through Zenodo.

DOI: https://doi.org/10.5281/zenodo.22741195

## Citation

Castañeda Herrera, L. M., Arciniegas Herrera, J. L., & Baldassarri, S., Beltran, J. R.
AQUASET: Affective Physiological QUAlity-of-Experience Streaming
service dataSET. Zenodo.

# Description of the Dataset File Structure
## Main Folders

- **e1, e2, e3, e4, e5**
These folders represent the different **experiments** conducted. Each one corresponds to a distinct set of tests or experimental conditions.

- **e1/u1, e2/u1, e3/u1, ...**
  Within each `eX` folder, the `uX` subfolders contain the data corresponding to the **users** who participated in that specific experiment.

## Contents of a User's Folder

Inside a user's folder (for example, `e1/u1`), you can find the following files and folders:

### 1. **emotions**
   This folder contains the **emotions labeled** with the assigned tag using the **VGG19** model. These images have been classified according to the recognized emotions.

### 2. **open-face**
   This folder contains files with **facial features** extracted from user images using the **OpenFace** tool. This tool provides data such as facial expressions, facial landmarks, etc.

## CSV Files

### 1. **respuestas.csv**  
   This file contains the answers provided by the user to question forms or questions related to the experiment. Each row represents one user answer.

### 2. **Sensor CSV Files**
   The CSV files for each sensor follow this naming convention: `sensor_measurement.csv`.
   Example: **`accelerometer_empatica.csv`** contains data from the **accelerometer** measured by the **Empatica** device.

   Each sensor CSV file contains the following columns:

   - **task**: Indicates the specific task to which the data corresponds.
   - **seconds**: Represents the time in seconds since the start of the task when the data was collected.

   Depending on the sensor, there may be additional columns containing the collected data. For example, the Muse accelerometer has three additional columns (X, Y, Z).

   All data in the CSV files has been **resampled** to its corresponding frequency. This ensures that the interval between the previous and current values in the `seconds` column is **constant**.





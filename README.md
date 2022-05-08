# Electric Motor Temperature

## problem statement

All data is deanonymized now. Moreover, 17 additional measurement profiles were added, expanding the dataset from 138 hours to 185 hours of records.

The data set comprises several sensor data collected from a permanent magnet synchronous motor (PMSM) deployed on a test bench. The PMSM represents a german OEM's prototype model. Test bench measurements were collected by the LEA department at Paderborn University.

All recordings are sampled at 2 Hz. The data set consists of multiple measurement sessions, which can be distinguished from each other by column "profile_id". A measurement session can be between one and six hours long.

The motor is excited by hand-designed driving cycles denoting a reference motor speed and a reference torque.
Currents in d/q-coordinates (columns "id" and iq") and voltages in d/q-coordinates (columns "ud" and "uq") are a result of a standard control strategy trying to follow the reference speed and torque.
Columns "motor_speed" and "torque" are the resulting quantities achieved by that strategy, derived from set currents and voltages.

Most driving cycles denote random walks in the speed-torque-plane in order to imitate real world driving cycles to a more accurate degree than constant excitations and ramp-ups and -downs would.

## Data set link is also given below
```bash
https://www.kaggle.com/datasets/wkirgsn/electric-motor-temperature?select=measures_v2.csv
```

Names of the columns is also given
```bash
u_q-->Voltage q-component measurement
coolant-->Coolant temperature 
stator_winding-->Stator winding temperature
u_d-->Voltage d-component measurement
stator_tooth-->Stator tooth temperature
motor_speed-->Motor speed
i_d-->Current d-component measurement
i_q-->Current q-component measurement
pm-->Permanent magnet temperature
stator_yoke-->Stator yoke temperature  ---> Target variable
```

## My solution for this problem

### Step 1: Create a new environment and activate is follow the steps below:
```bash
conda create -n project python=3.7 -y
activate project
```
### Step 2: Install all the required dependencies in the environment 
```bash
pip install -r requirements.txt
```
### Step 3: 
open the notebook and start coding.....

For EDA I am using pandas profiling

Checking the VIF score for my data and its highly colinear

Remove multicollinearities
To remove multicollinearities, we can do two things. We can create new features or remove them from our data.
Removing features is not recommended at first. The reason is that there’s a possibility of information loss because we remove that feature. Therefore, we will generate new features first.




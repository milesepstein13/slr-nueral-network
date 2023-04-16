# slr-nueral-network
Neural network that can be used to forecast SLR from temperatures, winds, and humidity. The full project is available at https://github.com/milesepstein13/slr-model

The neueral network can be used in two ways:

1. Using Keras, download the slr_model folder and load the model using Keras with 
```
from tensorflow import keras
model = keras.models.load_model('path/to/slr_model')
```

2. From slr_model.h5, using any package that can read .h5 files

When using the model, the following inputs in the following order must be used: Temperatures* (K), U-components of wind* (m/s), V-components of wind* (m/s), specific humidities* (kg/kg), vertical velocities* (Pa/s), instantaneous 10 m wind gust (m/s), 10 m u-component of wind (m/s), 10 m v-component of wind (m/s), 2 m temperature (K), 2 m dew point (K), 100 m u-component of wind (m/s), 100 m v-component of wind (m/s), for 122 total inputs.

Where values marked with * must be input at each pressure level of 1000, 975, 950, 925, 900, 875, 850, 825, 800, 775, 750, 700, 650, 600, 550, 500, 450, 400, 350, 300, 250, 225, and 200 kPa.

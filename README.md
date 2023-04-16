# slr-nueral-network
Neural network that can be used to forecast SLR from temperatures, winds, and humidity. The full project is available at https://github.com/milesepstein13/slr-model

The neueral network can be used in two ways:

1. Using Keras, download the slr_model folder and load the model using Keras with 
```
from tensorflow import keras
model = keras.models.load_model('path/to/slr_model')
```

2. From slr_model.h5, using any package that can read .h5 files

#### Q model {#q-model}

Q model can apply spatially and time varying attenuation to a seismic data volume. Q data volume must be loaded. Q model expects interval Q data \(while the Q filter algorithm expects an effective value\).

Go to: **Processing** → **Q Model**

![](/assets/034_Processing.png)

_Q –Model_

There are two basic modes (directions) of Q modeling.

**Inverse modelling**

Applies a compensation for attenuation that already exists in the data, based on the attenuation data loaded.

**Forward modelling**

Applies attenuation to the seismic data (filtering of high frequencies), based on the loaded attenuation data.

**Modelling Type** and **Modelling Parameter** are analog to the **Q Filter** algorithm. You can change the FFT window length (**Change FFT-Resolution**) to a higher value when artifacts get introduced to the data.


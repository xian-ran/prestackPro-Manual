## Import Q data {#import-q-data}

Seismic data gets attenuated as the energy is transmitted through the earth. One effect is that high frequencies are lost and the other that the phase is changed. These effects can be corrected independently in the attenuation algorithms. Q data volume is a prerequisite.

The supported formats are either SEG-Y or an ASCII based column format like for velocity or Eta field.

Import of velocity

These ﬁles have to consist of at least one column for the inline information, one column for the crossline information, one column for the time/depth information and one column with the Q data.
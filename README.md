# EXP.NO.11-Simulation-of-Spread-Spectrum-Modulation-Techniques


# AIM
To simulate the process of Direct Sequence Spread Spectrum (DSSS) modulation using Binary Phase Shift Keying (BPSK).
# SOFTWARE REQUIRED
Python (Version 3.x)

NumPy (for numerical operations)

Matplotlib (for plotting the graphs)
# ALGORITHMS

Generate random binary data.

Create a PN sequence of length 8.

Perform BPSK modulation on the data (0 → -1, 1 → +1).

Spread the BPSK modulated signal using the PN sequence.

Modulate the spread signal using a BPSK carrier.

Plot the DSSS spread signal and the BPSK modulated carrier waveform

# PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt

# System Parameters
data_length = 4                # Number of bits
chips_per_bit = 8              # PN sequence length
bit_rate = 1e3                 # 1 kbps
chip_rate = bit_rate * chips_per_bit
carrier_freq = 20e3            # 20 kHz carrier
sample_rate = 160e3            # 160 kHz sampling rate
samples_per_chip = int(sample_rate / chip_rate)

# Generate random binary data
def generate_data(length):
    return np.random.randint(0, 2, length)

import numpy as np
import matplotlib.pyplot as plt

# System Parameters
data_length = 4                # Number of bits
chips_per_bit = 8              # PN sequence length
bit_rate = 1e3                 # 1 kbps
chip_rate = bit_rate * chips_per_bit
carrier_freq = 20e3            # 20 kHz carrier
sample_rate = 160e3            # 160 kHz sampling rate
samples_per_chip = int(sample_rate / chip_rate)

# Generate random binary data
def generate_data(length):
    return np.random.randint(0, 2, length)

# Generate PN sequence: ±1 chips
def generate_pn_sequence(length):
    return np.random.choice([-1, 1], length)

# BPSK mapping: 0 → -1, 1 → +1
def bpsk_modulate(bit):
    return 2 * bit - 1

---
title: Wav to Graph
tags: [Python,]
comment: 1
date: 2024-12-02
---
# Interactive Audio Waveform Visualization

I generated this code using Chatgbt to converted wav files to a graph that you can view it, zoom in, and annotate all in one place.
 
{% include more.html content="[Use this colab to view a pie chart and wav graph](https://colab.research.google.com/drive/121p66Cm2YvKCLvFQZDWplQgX31Kwh-f_?usp=sharing)." %}

{% include more.html content="[Use this link to view a annotatable graph.](https://colab.research.google.com/drive/11NFnN1HV8gDKXeXEoguG-LBP2Tf4eQOl?usp=sharing)." %}


## Python Code For Annotatable Graph

```python
# Install necessary libraries
!pip install plotly scipy

# Import libraries
import numpy as np
import plotly.graph_objects as go
from scipy.io import wavfile
from google.colab import files

# Step 1: Upload the audio file
print("Please upload your .wav file.")
uploaded = files.upload()  # Upload audio file

# Step 2: Load the audio file
file_name = list(uploaded.keys())[0]  # Get the uploaded file name
sample_rate, data = wavfile.read(file_name)

# Step 3: Convert to mono if stereo
if len(data.shape) > 1:
    data = data.mean(axis=1)

# Step 4: Create time array
duration = len(data) / sample_rate  # Duration in seconds
time = np.linspace(0, duration, len(data))

# Step 5: Define initial range for display
initial_duration = 10  # seconds
end_index = int(initial_duration * sample_rate)

# Step 6: Create and display the interactive graph
fig = go.Figure()

# Plot the data
fig.add_trace(go.Scatter(x=time, y=data, mode='lines', name='Amplitude'))

# Customize layout with interactive zoom options
fig.update_layout(
    title="Interactive Audio Waveform Graph",
    xaxis_title="Time (seconds)",
    yaxis_title="Amplitude",
    xaxis=dict(range=[0, initial_duration]),  # Initial zoom range
    yaxis=dict(range=[data.min(), data.max()]),  # Set amplitude range dynamically
    dragmode="zoom",  # Enable zooming
    autosize=True,  # Automatically adjust size to the display
)

# Show the graph
fig.show()

print("Use the mouse to zoom in/out and pan the graph. Double-click to reset the view.")

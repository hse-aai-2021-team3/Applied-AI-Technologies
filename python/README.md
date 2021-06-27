# Applied-AI-Technologies/python - Overview
Each ipynb represents one step of the processing-chain.</br>
Data (audio files) are exchanged between the different notebooks within the in Colab integrated google-drive.</br>
Below are listed the required files for each individual ipynb.</br>
</br>

## upload
input:</br>
&nbsp;&nbsp;&nbsp;-</br>
output:</br>
&nbsp;&nbsp;&nbsp;content.wav</br>
&nbsp;&nbsp;&nbsp;style.wav</br>
</br>

## preProcessing

### BPM
input:</br>
&nbsp;&nbsp;&nbsp;content.wav</br>
&nbsp;&nbsp;&nbsp;style.wav</br>
</br>
output:</br>
&nbsp;&nbsp;&nbsp;style_synced.wav</br>

### spleeter
input:</br>
&nbsp;&nbsp;&nbsp;content.wav</br>
&nbsp;&nbsp;&nbsp;style_synced.wav</br>
</br>
output:</br>
&nbsp;&nbsp;&nbsp;content_vocal.wav, content_drums.wav, content_bass.wav, content_other.wav</br>
&nbsp;&nbsp;&nbsp;style_vocal.wav, style_drums.wav, style_bass.wav, style_other.wav</br>
</br>

## styleTransfer

### -all variants-
input:</br>
&nbsp;&nbsp;&nbsp;content_vocal.wav, content_drums.wav, content_bass.wav, content_other.wav</br>
&nbsp;&nbsp;&nbsp;style_vocal.wav, style_drums.wav, style_bass.wav, style_other.wav</br>
</br>
output:</br>
&nbsp;&nbsp;&nbsp;transfered_vocal.wav, transfered_drums.wav, transfered_bass.wav, transfered_other.wav</br>
</br>

## postProcessing

### denoise
input:</br>
&nbsp;&nbsp;&nbsp;transfered_vocal.wav, transfered_drums.wav, transfered_bass.wav, transfered_other.wav</br>
output:</br>
&nbsp;&nbsp;&nbsp;transfered_vocal_clean.wav, transfered_drums_clean.wav, transfered_bass_clean.wav, transfered_other_clean.wav</br>

### combine
input:</br>
&nbsp;&nbsp;&nbsp;transfered_vocal_clean.wav, transfered_drums_clean.wav, transfered_bass_clean.wav, transfered_other_clean.wav</br>
output:</br>
&nbsp;&nbsp;&nbsp;transfered_sum.wav</br>
</br>

## download
input:</br>
&nbsp;&nbsp;&nbsp;transfered_sum.wav</br>
output:</br>
&nbsp;&nbsp;&nbsp;-</br>
</br>
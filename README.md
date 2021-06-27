# Applied-AI-Technologies - StyleChanger

Repo for the lecture "Applied Artificial Intelligence" at the University of Applied Sciences Esslingen created by [Dionysios Satikidis](mailto:dionysios.satikidis@gmail.com) and [Jan Seyler](mailto:Jan.Seyler@gmail.com).

[Module Description HS Esslingen](https://www.hs-esslingen.de/fileadmin/media/Fakultaeten/it/FAKULTAET/Studiengaenge/Modulhandbuecher/Wahlfachmodul/HE-IT_Modulhandbuch-Wahlfachmodul-_Wahlpflichtfaecher_SWB_TIB_WKB_2019-02-15.pdf)</br>

Check out the Applied-AI [Wiki](https://github.com/MrDio/Applied-AI-Technologies/wiki) for detailed Information. First start with the chapters and intro to NN and DL.

## Description of this Repo
This Repo is part of an group work from the lecture "Applied Artificial Intelligence", as decripted above.</br>
The goal was to use an styletransfer, which is intended for image-transformation, to transfer audio.
The expectations were some sort of genre change of the audio.</br>
First, there is already some information and code available, which includes the same approach.
For example this repo: https://spiyer99.github.io/Change-Audio-Pytorch/.
But it is intended to work only with voices.</br>
</br>
So out first step was to try this code with other audio.
The result was mostly noise and garbage.
So we decided to move towards two directions:</br>
One idear was to preprocess the audio file somehow, that the available code works for more different audio.
We tried to first match the BPM of the both input samples and further spit up the audio in different parts, corresponding to different 'voices'.
For both we used available code, as stated in the code and below.
There were some improvements, but the result didn't change that much.</br>
The other option was to try to modify an existing image-transformation-network to work with audio.
For this we decided to use the VGG16 convolutional network, as there is plenty of documentary available.
To get the audio from time domain to image domain, we used fft.
The result is an matrix, which can be treated as an grayscale-image.
To get back to time domain, we used also available code.
However the VGG16 expects RGB images.
So we used various methodes to map the grayscale image to an RBG image.
But this method doesn't work good either.</br>
</br>
The final state of this group work is an more or less working approach to transfer audio styles.
This code should not be expected to work as it is, but it can be used for further research of this idea.</br>

## Getting started
To get a first impression of the current state of this project, you can open the "getting_started.ipynb" from the github-repo in google-colab.</br>
Then you have to setup the runtime to work with hardware acceleration. This can be done via the "Runtime" tab and then "Change runtime type".
There you have to switch the "Hardware accelerator" option from "None" to "GPU".</br>
Then you can run the whole Notebook.</br>
First the script requires you to upload the stlyle-audio-file via the upload-promt.
In the next step you have to upload an content-audio-file.
After that the style-transfer starts.
Depending on the chosen audio-file-length, this can take al lot of time.
When done yout get an promt where you can download the resulting-audio-file.

## Resources
https://github.com/scaperot/the-BPM-detector-python</br>
https://spiyer99.github.io/Change-Audio-Pytorch/</br>
https://github.com/spiyer99/spiyer99.github.io/blob/master/nbs/Neural%20Transfer%20of%20Audio%20in%20Pytorch.ipynb</br>
https://www.codespeedy.com/python-understanding-style-transfer-using-cnns/</br>
https://github.com/deezer/spleeter</br>
https://github.com/AP-Atul/Audio-Denoising</br>
[musicfox](https://www.musicfox.com/)</br>
https://www.diagrams.net/
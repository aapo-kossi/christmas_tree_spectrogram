# christmas_tree_spectrogram
Jupyter notebook to generate spectrogram from an audio clip and "wrap" the spectrogram around a programmable led installation  with led coordinates provided [like here](https://github.com/standupmaths/xmastree2021). The spectrogram wraps an octave to the full circle in the xy-plane and the log frequency is used as hue for led brightness. The final brightnesses are sums of brightnesses of the notes in each octave, normalized.

## Built with
* [Google Colab, including inbuilt libraries such as NumPy, Pandas, SciPy](https://colab.research.google.com/)
* [pydub](https://github.com/jiaaro/pydub)

## Installation
No installation needed, runs online on a virtual machine provided by Google.

## Usage
To generate your own spectrogram you can simply change the `src` and `led_src` variables in the colab notebook and run all cells. The `src` should be a url address to the download link of the mp3 file to be used, to use a file from your local machine, do `google.colab.files.upload()`. `led_src` is a file containing your led locations in GIFT format as described in [this](https://www.youtube.com/watch?v=WuMRJf6B5Q4) video. The notebook will render the led brightnesses (run time was approx 25 minutes for 156 seconds of sound for the original notebook) and download the csv that can then be run on the physical lights using a RasPi using the code in [this repository](https://github.com/GSD6338/XmasTree). You can also modify the frames per second used when generating the animation according to your preferences and hardware.

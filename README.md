# spectrology

Images to audio files with corresponding spectrograms encoder.

## Dependencies

You can use virtualenv module for python. Create a virtual environment:

```bash
python3 -m venv venv

# For Unix-like systems
source venv/bin/activate

# For Windows
./venv/Scripts/activate.bat
```

And then install dependencies using

```bash
pip install -r requirements.txt
```

Or you can install dependencies standalone:

```bash
pip install -r requirements.txt
```

## Usage

```
usage: spectrology.py [-h] [-r] [-o OUTPUT] [-b BOTTOM] [-t TOP] [-p PIXELS]
                      [-s SAMPLING]
                      INPUT

positional arguments:
  INPUT                 Name of the image to be convected.

optional arguments:
  -h, --help            show this help message and exit
  -r, --rotate          Rotate image 90 degrees.
  -o OUTPUT, --output OUTPUT
                        Name of the output wav file. Default value: out.wav).
  -b BOTTOM, --bottom BOTTOM
                        Bottom frequency range. Default value: 200.
  -t TOP, --top TOP     Top frequency range. Default value: 20000.
  -p PIXELS, --pixels PIXELS
                        Pixels per second. Default value: 30.
  -s SAMPLING, --sampling SAMPLING
                        Sampling rate. Default value: 44100.
```

```bash
python3 spectrology.py test.bmp -b 13000 -t 19000
```

![spectrogram](https://solusipse.net/blog/img/posts/audio-samples/7.png)

For more informations on this techique, see this article: https://solusipse.net/blog/post/basic-methods-of-audio-steganography-spectrograms/.

## License

See `LICENSE`.

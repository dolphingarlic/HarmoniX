# HarmoniX[^1]

_HarmoniX_ is an automatic harmonizer for monophonic melodies.
Simply provide it with a .wav file of a tune, and it will spit
out a new .wav file of the audi in ~perfect~ four-part harmony.

## How it works

_HarmoniX_ consists of three main components:

1. **Pitch detection** using the YIN algorithm[^2].
2. **Melody-to-chord generation** using a bidirectional LSTM[^3].
3. **Pitch shifting** using a digital phase vocoder[^4].

See [HarmoniX.ipynb](HarmoniX.ipynb) for the code and more
details.

## Running the code locally

First, install the dependencies using the following commands:

```shell
python3.11 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

Then go to [HarmoniX.ipynb](HarmoniX.ipynb) and run all the cells.
By default, the code does not save the trained PyTorch model.
However, you can uncomment the commented-out code block to
save your own model if you decide to change any hyperparameters.

## Examples

See [examples.ipynb](examples.ipynb)

[^1]: Pronounced "harmonic". The "X" is an uppercase Greek chi.
[^2]: http://recherche.ircam.fr/equipes/pcm/cheveign/ps/2002_JASA_YIN_proof.pdf
[^3]: https://archives.ismir.net/ismir2017/paper/000134.pdf
[^4]: https://www.di.ens.fr/~mallat/papiers/Vocoder.pdf

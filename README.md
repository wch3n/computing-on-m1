# Scientific computing on Apple M1 machines

## Rosetta 2

For the time being, we rely on Rosetta 2 to translate the ```intel/x86_64``` code into the native ```apple/arm64``` binary.

```sh
% softwareupdate --install-rosetta --agree-to-license
```
## Homebrew

```sh
% arch -x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

From here on, use ```arch /x86_64 brew install``` to install a homebrew formulae. 
To save keystrokes, we create an alias for ```brew```
```sh
% echo "alias brew='arch -x86_64 brew'" >> ~/.zshrc
% . ~/.zshrc
```

## GCC/GFortran

```sh
% brew install gcc
```

## LAPACK/OpenBLAS

```sh
% brew install lapack openblas
```

## FFTW

```sh
% brew install fftw
```

## Python

### python 3.9

```sh
% brew install python3
```

### numpy

```sh
% brew install numpy
```
or

```sh
% python3.9 -m pip install numpy
```

### scipy

```sh
% brew install scipy
```

### matplotlib, seaborn, scikit-learn, pandas, and (perhaps) many more

```sh
% python3.9 -m pip install <package>
```

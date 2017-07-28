Hi there! In this tutorial, you'll learn how to install Node.js using NVM. If you want to learn more about Node.js and why it's useful, there's a [good explaination over on the Modulus blog](http://blog.modulus.io/top-10-reasons-to-use-node).

Let's get started!

We'll be using NVM (the Node Version Manager). Not to be confused with npm (the Node Package Manager), NVM is a simple bash script to manage multiple active Node.js versions. Basically, NVM allows you to install Node.js and gives you some extra tools to be able to switch between Node.js versions if particular projects require that.

### Installing NVM

To install NVM, we'll use `curl` to download and run an install script. (To all the security folks out there, yes, I hear you.)

Copy and past the following line into your Terminal application, and hit enter.

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.29.0/install.sh | bash
```

Now, quit and reopen your Terminal app. We need to check whether NVM was able to successfully install itself in your bash profile. Type `nvm` and hit enter. If you get an error, you'll need to add NVM to your bash profile manually.

Type `nano .bash_profile`. This will open up your `.bash_profile` document. Paste the following text into your `.bash_profile` document.

```sh
. ~/.nvm/nvm.sh
```

Press `Ctrl + X` to save, `Y` to agree to save. Now you should be able to quit your Terminal, open it again, type `nvm`, hit enter, and see the Node Version Manager help text.

YAY!

### Installing Node

Now that we have NVM installed, we can download and install Node.js.

We'll install the latest stable version. Type `nvm install stable`.

You'll see a loading bar, and then

```sh
Now using node v5.0.0 (npm v3.3.6)
```

To test whether Node.js is _really truly_ installed, type `node --version`. You should get back `v5.0.0`, with a version number corresponding to the version NVM installed.

If at any time you need to use a different version of Node.js, and have installed multiple versions from NVM, just use

```sh
nvm use X.X.X
```

... where `X.X.X` is the version number you wish to use.

Congratulations, you just installed Node.js, and have a sweet version manager to keep yourself up to date.

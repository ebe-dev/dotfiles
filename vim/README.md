1) Install vim from source
sudo apt-get install libncurses5-dev libgnome2-dev libgnomeui-dev \
libgtk2.0-dev libatk1.0-dev libbonoboui2-dev \
libcairo2-dev libx11-dev libxpm-dev libxt-dev python-dev ruby-dev mercurial

sudo apt-get remove vim vim-runtime gvim

sudo apt-get remove vim-tiny vim-common

cd ~
hg clone https://code.google.com/p/vim/
cd vim
./configure --with-features=huge \
--enable-rubyinterp \
--enable-pythoninterp \
--enable-perlinterp \
--enable-gui=gtk2 --enable-cscope --prefix=/usr
make VIMRUNTIMEDIR=/usr/share/vim/vim73
sudo make install

2) Install bundle
https://github.com/gmarik/vundle.git

3) Install YCM
https://github.com/Valloric/YouCompleteMe.git
cd ~/.vim/bundle/YouCompleteMe
./install.sh --clang-completer

4) :BundleInstall

5) Fix powerlone fonts
https://powerline.readthedocs.org/en/latest/installation/linux.html#font-installation

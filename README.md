# ~/.tmux.conf

```sh
sudo apt install -y libevent-dev libncurses-dev bison pkg-config build-essential autoconf automake
git clone --depth=1 -b 3.6 https://github.com/tmux/tmux.git
cd tmux
sh autogen.sh
./configure --enable-sixel
make -j$(nproc)
sudo make install
hash -r
tmux kill-server
which tmux && tmux -V    # confirm /usr/local/bin/tmux and 3.6
```

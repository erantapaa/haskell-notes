
## vim modules

Modules relavant to Haskell development:

| Module     | Best Features |
|------------|---------------|
| pathogen   | base requirement |
| haskellmode-vim | syntax coloring |
| syntastic  | automatic compile check on save |
| vimproc    | requirement for ghcmod-vim |
| ghcmod-vim | running hlint |
| hdevtools  | type interrogation |
| vim-haskellfold | better folding |
| vim2hs     | ... | 
| vim-hoogle | hoogle queries |
| neco-ghc   | name completion |
| cumino     | ghci interaction (requires python) |
| ariadne    | go-to definitions |
| scion      | ... (requires python) |

Other resources:

- http://blog.mno2.org/blog/2011/11/17/vim-plugins-for-haskell-programmers/

### pathogen.vim

Execute the following commands in a shell:

    mkdir -p ~/.vim/autoload ~/.vim/bundle
    curl -so ~/.vim/autoload/pathogen.vim \
        https://raw.github.com/tpope/vim-pathogen/master/autoload/pathogen.vim

Then add this to your ~/.vimrc:

    execute pathogen#infect()

### haskellmode-vim

Install via pathogen:

    cd ~/.vim/bundle
    git clone https://github.com/lukerandall/haskellmode-vim.git

Might have use `:GHCReload` to get type info commands working.

### vim-haskellfold

    cd ~/.vim/bundle
    git clone https://github.com/Twinside/vim-haskellFold.git

### syntastic

Source: https://github.com/scrooloose/syntastic

Adding syntastic as a pathogen module:

    cd ~/.vim/bundle
    git clone https://github.com/scrooloose/syntastic.git

### vimproc

Source: https://github.com/Shougo/vimproc.vim

`vimproc` is needed for `ghcmod-vim`. It is installable as a `pathogen` module:

    git clone https://github.com/Shougo/vimproc.vim.git ~/.vim/bundle
    cd ~/.vim/bundle/vimproc.vim
    make

### ghcmod-vim

Source: https://github.com/eagletmt/ghcmod-vim

Make sure the cabal package `ghc-mod` is installed:

    cabal install ghc-mod

Then install via the following commands:

    cd ~/.vim/bundle
    git clone https://github.com/eagletmt/ghcmod-vim.git

### hdevtools

First install the the cabal package:

    cabal install hdevtools

THen install the `vim-hdevtools` vim package:

    cd ~/.vim/bundle
    git clone https://github.com/bitc/vim-hdevtools.git

Add the following lines to your .vimrc file:

    au FileType haskell nnoremap <buffer> <F1> :HdevtoolsType<CR>
    au FileType haskell nnoremap <buffer> <silent> <F2> :HdevtoolsClear<CR>

### vim2hs

    cd ~/.vim/bundle
    git clone https://github.com/dag/vim2hs.git

### vim-hoogle

    cd ~/.vim/bundle
    git clone https://github.com/Twinside/vim-hoogle.git

### neco-ghc

    cd ~/.vim/bundle
    git clone https://github.com/ujihisa/neco-ghc.git

### cumino

Requires vim with python support. See https://github.com/adinapoli/cumino

### ariadne

Install the Ariadne server:

  cabal install ariadne

Install the vim plugin:

  https://github.com/feuerbach/ariadne-vim

### scion

See https://github.com/nominolo/scion


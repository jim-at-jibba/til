# Fixing triggering completion in insert mode

I wanted to be able to trigger the completion popup in *insert* mode. I had previous had it set to
`ctrl+space` which is the same as VSCode. When I set it up I was using iTerm2 and it worked fine. 
Later I switched to Allacritty and the Kitty and somewhere along the way I realised that this command
no longer worked. I did not put it down to a change of terminal and just thought it was lsp flake.

It turns out terminal emulators handle the spacebar differently. The source explains it very well.

[Source](https://stackoverflow.com/a/2269587)

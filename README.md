# wavefile.py

Initial version of this file come form [Scipy](https://github.com/scipy/scipy/blob/v0.14.0/scipy/io/wavfile.py) project.

It lacks markers and loops features, so it has been moded by Joseph Ernest as [wavefile.py (extended)](https://gist.github.com/josephernest/3f22c5ed5dabf1815f16efa8fa53d476), as explained in this [article](https://josephbasquin.fr/pythonaudiomodules)

It had few bugs to fix though, and some critical functions were still missing, like the preservation of unsupported chunks.

That's why I had to mod it to bring new features. Here is the list:

* read: also returns bitrate, cue markers + cue marker labels (sorted), loops, pitch
* read: 24 bit & 32 bit IEEE files support (inspired from wavio_weckesser.py from Warren Weckesser)
* read: added normalized (default False) that returns everything as float in [-1, 1]
* read: added forcestereo that returns a 2-dimensional array even if input is mono

I'm no python expert, and I may not have tested every scenario. Be very careful by using this script. Makes copy of you files to be sure.

Though it has less objectively bugs than previous versions, it may still contains some in certain circumstances.

Please test it and report if something is wrong!

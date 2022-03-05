---
layout: page
title: Projects
permalink: /projects/
---

### Cheap Blue
[![](/assets/favicon.ico)][cheap-blue]

The project I am most proud of is my chess engine, [Cheap Blue][cheap-blue]. I am continuing to work on and improve it. At some point maybe it will be able to compete with the big boys like Stockfish and Lc0 (Leela chess zero) and I will need to change the name to something more dignified.

### Stegasaurus 2
This project originated back when I was in an undergraduate software engineering class. The class was centered around a semester-long group project. In the beginning of the semester everyone had to come up with ideas for a project and then people would join your team if they liked your idea. I was pretty excited about my idea having just watched a [YouTube video][computerphile-video] about steganography so I was able to get people to join me. We ended up with a team of eight people, by far the biggest group project I was involved in during school. The project involved [steganography][steganography] so we decided to name it Stega-saurus.. hilarious I know. Because it was originally my idea and I genuinely cared a lot about making something cool, I was very involved. I was pretty much solely responsible for the backend code to do the steganography and also worked on some of the database and web framework stuff. We used [Django][django] and I remember it being very frustrating dealing with binary file objects and storing them in the database.

Sadly, the only variety of steganography we implemented was LSB substition with PNG images even though we were conscious of a few others, including the one discussed in the Computerphile video I linked above: JPEG steganography using DCT. After the semester was finished I still had an interest in steganography, and I especially wanted to try an implement one method that used GIF images as a cover. I read about this method in a presentation I found online and, as far as I knew, it was just a theoretical idea that no one had tried to implement so I thought it would be a great opportunity to create something new and open source. I didn't get around to doing it until after I graduated but I finally did and called it [Stegasaurus 2][stegasaurus-2] to differentiate it from the original project.

There are plenty of other varieties of steganography using all types of media and I would love to continuing adding to this library. I think it would be really cool to do something similar for the HEIC/HEVC image file format that already exists for JPEG images. It would likely involve a lot of research and effort but because this file format is highly relevant there is a high chance the software would actually be used. Also an easier addition to the library would be a method using an audio file format like WAV as a cover.


[stegasaurus-2]: https://github.com/dfish13/Stegasaurus2
[django]: https://www.djangoproject.com/start/overview/
[computerphile-video]: https://youtu.be/TWEXCYQKyDc
[steganography]: https://en.wikipedia.org/wiki/Steganography
[cheap-blue]: https://d16mc0nsndq3dv.cloudfront.net/
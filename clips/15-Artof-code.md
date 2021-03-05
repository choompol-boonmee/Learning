```
The Art of Code - Dylan Beattie
https://youtu.be/6avJHaC3C2U


00:00
good afternoon NDC thank you have you
00:05
had a good few days I have it's been a
00:08
blast and they have asked me to to come
00:11
along and close out the conference for
00:14
some of you those of you who were wise
00:16
enough to be here because there's some
00:18
strong competition in this spot by
00:20
talking to you about something that I
00:23
call the art of code now does anyone
00:25
recognize the language that this little
00:28
intro sequence here is written in logo
00:32
this is not only is this logo this is
00:35
original Amstrad logo from 1985 because
00:40
the first computer that I ever had was
00:44
this the Amstrad six one two eight it
00:49
was rubbish I mean it was brilliant
00:52
because I'd never had a computer before
00:54
but it had the games that it had were
00:57
all this kind of green screen and they
00:58
weren't much fun compared to the games
01:00
in the arcades and everything and you
01:02
couldn't do very much with it no modem
01:04
no dial-up no BBS or bulletin boards or
01:06
internet but what it did have on it was
01:09
this logo programming language and logo
01:12
got me hooked because using logo I could
01:15
make the computer draw pictures and that
01:19
was a big deal in 1985 because I'd never
01:24
seen like I could put things on that
01:25
screen using logo that maybe nobody had
01:27
ever seen on any screen before and I got
01:31
hooked on it and I got this this lovely
01:34
kind of you know feedback loop where I
01:37
liked it because I could make the
01:39
computer do what I wanted and every time
01:42
I did that I'd get this little thrill
01:43
and this rush and I'd go back and I'd
01:45
have another go and you know throughout
01:47
my entire career developing software and
01:50
designing systems that thrill for me has
01:52
never gone away and I hope for you all
01:54
you here as well you know you have good
01:56
days and bad days but you still get that
01:58
rush when you know all your tests are
02:00
green or when you you know you hit
02:01
monitoring and it's a hundred percent or
02:03
something just works and you're like I
02:05
did that I made that work and over the
02:08
last three days here at NDC London we've
02:10
had some
02:11
amazing brilliant people telling us how
02:14
to solve useful important problems how
02:17
to design scalable services deployment
02:19
strategies information security the
02:21
ethics of artificial intelligence and
02:23
machine learning I'm not going to talk
02:26
to you about anything useful because I
02:28
am going to talk to you about art and
02:31
all art is quite useless says Oscar
02:34
Wilde now I don't entirely agree with
02:37
this quote I like this quote a lot
02:40
better the function of art is to hold a
02:43
mirror up to nature and if we want to
02:47
use art as a tool to explore and
02:51
understand the world around us we can
02:54
hold a mirror up to it but before we can
02:56
do that we need to invent to the mirror
02:58
and that is where science and technology
03:01
and engineering come in because for
03:03
centuries we humans have built machines
03:05
and tools to help us explore and
03:08
understand the world around us we've
03:10
created scanning electron microscopes
03:12
that have allowed us to see things like
03:14
this this is shards on the eyelid of a
03:19
beetle it's been there the whole time
03:21
and nobody had ever seen it until we
03:23
invented machines that could take
03:25
photographs of something that's only a
03:27
handful of micrometers across this is
03:30
crystals growing in a dish of soy sauce
03:33
this is the stems inside one strand of a
03:37
banana leaf this amazing beautiful
03:39
microscopic world we had never ever seen
03:41
and we've sent machines and cameras and
03:44
telescopes and people into space and
03:46
we've looked back we've seen you know
03:49
our planet Earth rising above the moon
03:51
we've looked back from beyond the rings
03:53
of Saturn this is us down here this is
03:57
the pillars of creation this is six
03:59
thousand light-years away in the
04:01
Horsehead Nebula and until we invented
04:03
machines to show us these things nobody
04:05
had ever seen it and within the last
04:08
thirty years maybe we've started
04:10
exploring another hidden world that's
04:13
been there the whole time until we
04:15
developed the machines that allowed us
04:17
to go in and see it and play around with
04:19
it it's a world of mathematics and
04:22
information throughout the 1970s there
04:25
was a guy called Martin Gardner who
04:27
wrote a column for Scientific American
04:29
magazine about mathematical puzzles and
04:32
curiosities and certainly the most
04:34
influential of his columns he ever
04:36
published was this one October 1970
04:38
where he described something called
04:41
Conway's Game of Life created by an
04:44
English mathematician called John Conway
04:45
now as games go Conway's Game of Life
04:49
does not look terribly exciting it is a
04:53
game for no players played on an
04:55
infinite board and it has four rules the
04:58
rules of life the first rule each of
05:01
these cells on our grid can either be
05:02
living or dead if a cell has zero or one
05:06
neighbors it will die of loneliness if a
05:10
cell has two or three neighbors it
05:13
survives to another generation if a cell
05:16
has four or more neighbors it's like
05:18
being in London it dies of overcrowding
05:21
or it moves to Germany I don't know but
05:23
it's not there anymore and finally and
05:26
this is where it gets a little bit
05:27
spooky weird if a dead cell has exactly
05:30
three neighbors it will come back to
05:33
life and that's it
05:35
that is you now understand everything
05:37
that there is to understand about the
05:39
rules of Conway's Game of Life
05:41
now when Martin Gardner's article was
05:43
first published 1970 very very few
05:46
people had computers and so they used
05:49
pens and graph paper to play the game of
05:52
life and they drew diagrams like this
05:54
now these these five shapes of what we
05:55
call the tetrominoes there are five
05:57
Tetris tiles and this shows you the
06:00
evolution of each of those shapes under
06:03
the rules of Conway's Game of Life but
06:05
you know looking at this it's like go
06:07
new Museum where they have the
06:08
butterflies pinned in a glass case you
06:10
can see what the butterfly looks like
06:12
but you don't understand anything about
06:14
a butterfly from looking at this kind of
06:17
representation it wasn't until we
06:19
started using computers to actually
06:22
simulate this stuff that we really
06:24
understood the behavior we were looking
06:26
at because these four patterns they all
06:28
stabilized quickly but this one over
06:30
here this is just gonna keep going
06:32
over and over and over
06:33
and once we could visualize things like
06:35
this exploring the game of life became
06:38
addictive people started saying you know
06:40
are there packings that will move across
06:43
the grid and just keep going are there
06:44
limits is the game bounded or is it
06:46
infinite this was one of the first
06:48
shapes this is known as a glider repeats
06:50
itself every six generations and it just
06:52
keeps crawling across the grid forever
06:54
and once we realized bladers were
06:56
Possible's people started looking for
06:58
more and they found hundreds of these
07:00
shapes spaceships they call them these
07:03
incredibly elaborate beautiful creations
07:06
that just glide across this grid driven
07:08
by four simple rules and that's it one
07:12
of the earliest questions that came up
07:13
in the game of life can you create
07:15
patterns that will grow infinitely it's
07:19
a guy called Bill Cosby was a founding
07:20
artificial intelligence researcher and
07:22
computer scientist some of you may have
07:24
heard of and his team at MIT in the
07:26
1970s they created something absolutely
07:30
wonderful they created a thing called
07:33
gospel glider gun now what the glider
07:36
gun is is it's a stable configuration
07:38
and every 27 generations it creates a
07:43
glider and since these gliders streaming
07:46
out across the grid and gossip esteem
07:48
discovered another you know lots of
07:50
configurations while they were exploring
07:52
this they also discovered this thing
07:53
here which was called Villita
07:54
now we have a glider generator and we
07:57
have a glider consumer we can generate
07:59
signals and we can destroy signals we
08:01
have one and we have zero and if we have
08:04
one and 0 we have binary logic and we
08:07
can use that to create logic gates so
08:10
this thing here is a NAND gate built in
08:12
the game of life these little
08:14
highlighted cells are our inputs now
08:18
what we're going to do first of all
08:20
we're going to start the circuit running
08:22
and then we're going to say ok we're
08:24
gonna take that blocker out so that our
08:25
input a becomes true there we go
08:29
a is now switched on we have no output
08:33
signal we only have one input let's flip
08:35
the inputs what happens if we switch B
08:37
on will be as on but we still have no
08:41
output signal because this is a NAND
08:43
gate in order to get an output signal
08:44
here we need to enable a and
08:46
be we switch on both of those inputs we
08:49
switch on our circuit and there we go we
08:52
have a NAND gate now the brilliant thing
08:54
about this is that if you have logic
08:58
gates you can make circuits and if you
09:01
can make circuits you can create
09:02
computers and if you can create
09:05
computers you can run programs including
09:09
this program that you may have heard
09:10
about a little while ago it's a thing
09:12
called John Conway's Game of Life and it
09:14
goes a little something like this
09:43
now Conway's Game of Life is just one of
09:46
a whole category of systems that exhibit
09:51
very very complex behavior based on what
09:53
looked like very very simple rules
09:55
simple inputs you've probably heard of
09:57
this thing called the butterfly effect
09:59
it's a term we get from a branch of
10:01
science called chaos theory the idea
10:03
that weather prediction is impossible
10:05
because if a butterfly flaps its wings
10:07
that input is gonna change the output
10:09
and you're gonna get hurricanes instead
10:11
of sunshine in Tokyo two weeks later or
10:13
something and over the last few decades
10:17
mathematicians everywhere have started
10:20
studying systems in a different way for
10:22
a long time
10:22
maths was only interested in problems
10:24
you could solve give us the solution if
10:26
you can't give us the solution this
10:27
problem is not interesting we're just
10:29
gonna go and find something else to look
10:31
at but mathematicians kind of embraced
10:36
this this whole at different school a
10:37
different way of thinking we created
10:41
imaginary numbers now the basic rule of
10:45
an imaginary number we have this number
10:47
I and in the natural world negative
10:51
numbers don't have a square root 2 times
10:53
2 is 4 minus 2 times minus 2 is also 4
10:55
so how do you get what times what equals
10:57
minus 4 well nothing it doesn't exist
11:00
and mathematicians go no problem we'll
11:02
just make something up we'll invent I
11:04
it's an imaginary number and I squared
11:06
equals minus 1 and they just this is
11:08
where the rest of the world goes you
11:09
can't do that and mathematicians go we
11:10
can do anything we want it's an
11:13
imaginary we don't we don't care but
11:15
then once they've developed this and
11:17
they've come up with a rigorous set of
11:18
mathematics around it you can do some
11:20
really interesting things with it now
11:22
this thing here zero point eight plus
11:25
one point two I I hang on a second give
11:28
me one second there's a bunch of slides
11:29
of gonnna stare and this is not making a
11:31
huge amount of sense that yet no wicked
11:36
will get we get we get one slide is
11:39
missing right now this number here no
11:42
point eight plus one point two I this is
11:43
what's called a complex number a complex
11:45
number is like a project plan it has a
11:47
part that is real and it has a part that
11:49
is imaginary and it is very difficult to
11:52
predict what is going to happen next
11:54
once these things get involved now there
11:58
is a whole study of systems and the
12:01
behavior of systems that we can talk
12:03
about this thing here is called an
12:05
Argand diagram and the the blue bit is
12:08
imaginary the red bit is real so not
12:10
point eight over there on one point two
12:12
I plot it up there and this way we can
12:13
plot numbers in in complex mathematics
12:16
in this this kind of space
12:17
and we can do arithmetic with these
12:19
numbers just like you used to do in high
12:21
school so we take point eight plus one
12:22
point two I you just expand the numbers
12:25
out as you go and you multiply and all
12:28
you need to do is remember that anywhere
12:31
you have two blue numbers multiplied
12:33
together the result is going to come out
12:35
negative it's gonna come out backwards
12:37
so this one point two times one point
12:40
two I will you square them and then you
12:41
stick a minus on the beginning and you
12:43
take negative complex inputs you get
12:45
complex numbers out the other end now
12:47
what's really interesting is when you
12:49
start studying the behavior of systems
12:51
that are driven by these let's take a
12:53
really simple function e we're gonna
12:54
take some real number X so we're back in
12:56
in ordinary mathematics and every
12:58
generation X is gonna go to X plus 1 so
13:01
one two three four and you can already
13:04
intuitively see you know how this system
13:06
is gonna behave you can can't be
13:08
confident you understand its behavior
13:09
all the way up to infinity let's try
13:12
another one so if we take this example x
13:14
equals 2 minus X it's gonna go to there
13:16
not - - - - - not - - round and round
13:21
and round if we apply the same thing to
13:24
this complex number what we're gonna do
13:25
is we're gonna keep taking that number
13:27
and squaring it first time we square it
13:30
it goes to here we square it again goes
13:32
to here we square it again it ends up
13:34
over here and then over here and then it
13:37
disappears off to infinity we're gonna
13:39
move it ever so slightly and we're gonna
13:42
run the same sequence again this time
13:44
point six and it goes to here and here
13:46
and here and here but it doesn't escape
13:49
this time
13:50
it goes into this little kind of weird
13:52
almost circular orbiting pattern now
13:54
those two points are right next to each
13:56
other but they exhibit dramatically
13:58
different behavior when we iterate them
14:00
over and over again by squaring them and
14:03
squaring them and squaring them and
14:04
eventually this one disappears now the
14:08
first really rigorous study of these
14:10
kinds of systems was done by this guy a
14:12
Polish mathematician called benoit
14:14
mandelbrot and Mandelbrot was fascinated
14:17
by the mathematics of real life he had
14:19
this quote clouds are not spheres
14:21
mountains are not cones coastlines are
14:23
not circles a bark is not smooth not as
14:25
lightning travel in a straight line
14:27
now Mandelbrot had a brilliant job he
14:30
taught mathematics at Harvard and when
14:32
he got bored he went to IBM and played
14:34
on the computers because this is the
14:36
1970s when IBM had computers and nobody
14:39
else did so he would come up with these
14:41
you know wonderfully complex
14:42
mathematical ideas and then he'd go over
14:44
to IBM and spend a couple of months
14:45
playing around and simulating them and
14:47
then he'd go back to Harvard and you
14:49
know talk to his graduate students about
14:50
all this kind of stuff and he was the
14:54
first person to see the shape which now
14:56
bears his name it's his name was
14:58
Mandelbrot but everyone calls it the
15:00
Mandelbrot set and I know that I'm gonna
15:01
do that so let's just call it the
15:03
Mandelbrot set basically it took each of
15:06
these numbers in this grid and he said
15:09
we are going to square this and add it
15:11
to itself and square it and add it to
15:13
itself and we are gonna see whether it
15:16
stays on the grid or not and if it stays
15:18
on the grid
15:19
we are gonna color it in black and if it
15:22
disappears and vanishes off the grid
15:24
we are gonna color it in a different
15:26
color depending how quickly it what's
15:29
called tends towards infinity he started
15:32
off with these very very low resolution
15:33
renditions of this image but the one
15:36
that you're probably used to the one
15:37
that all of us have seen is this the
15:40
Mandelbrot set now the astonishing thing
15:42
about this from this incredibly simple
15:44
mathematical rule there is an infinite
15:47
amount of complexity we're going to take
15:49
a Mandelbrot set here and we're just
15:51
gonna start magnifying and we are gonna
15:53
start zooming in and when we get to
15:56
around about here we're gonna say that's
15:59
1 times magnification and we're gonna
16:01
keep zooming and zooming and zooming and
16:03
by the time we get about here that
16:07
original shape is now size of this
16:09
building and we are still zooming in
16:11
when we get to around about here that is
16:16
2 to the 21st Amana fication the
16:19
original shape is now bigger than London
16:21
and we are still zooming in and around
16:24
about now the original shape is bigger
16:27
than the United Kingdom and we are still
16:29
zooming in and we are still zooming in
16:31
and we can continue zooming into the
16:32
shape forever it never repeats it is
16:35
what's called self-similar which means
16:37
it resembles itself at different scales
16:40
but it never repeats exactly there is an
16:44
infinite amount of detail buried inside
16:47
this one shape and this has been there
16:49
the whole time nobody invented this we
16:51
discovered it now this the Mandelbrot
16:55
set some people have called it the
16:56
thumbprint of God now I'm not a very
16:59
spiritual person but I do play a lot of
17:01
computer games and I love that thing in
17:04
a computer game where you're doing
17:05
something silly that maybe isn't part of
17:07
the main campaign and you find that the
17:09
game designers left something there to
17:12
persuade you that you were supposed to
17:14
be here and you're on the right track
17:15
and this thing has been hidden in
17:17
mathematics since you know our universe
17:19
was created and no one ever saw it until
17:22
we humans we invented computers which
17:24
means taking lightning and sticking it
17:26
in a rock until it learns to think and
17:28
we invented advanced mathematics we
17:30
invented high-definition color displays
17:32
and rendering technologies all this kind
17:34
of stuff and this is what we found
17:36
something that was hidden there the
17:37
whole time nobody had ever seen until we
17:39
built the machines and the technology to
17:42
allow us to visualize it now in this day
17:45
and age just putting pictures on a
17:47
computer screen is not actually that big
17:49
a deal anymore this was from Tron which
17:52
was a movie Disney made in 1982 first
17:54
film to have completely
17:56
computer-generated sequences Tron did
17:59
not win the Academy Award for Best
18:01
Visual Effects it was disqualified
18:03
because using a computer to make a film
18:06
was cheating according to the Academy of
18:09
Motion Picture Arts and Sciences they
18:11
changed their minds eventually and they
18:13
gave it a lifetime award but we've got
18:15
really really good at using computers to
18:17
simulate things luxo jr. was the first
18:20
completely computer-generated film 1985
18:22
Jurassic Park 1994 the first time we had
18:25
computer-generated characters on screen
18:27
with human actors and it looked
18:29
convincing you know it looked compelling
18:31
it became part of the story
18:33
a couple of years ago we had this guy on
18:35
our cinema screens don't who this is
18:38
because there's one bunch of people who
18:40
say that's Peter Cushing and he's my
18:41
grandfather and he's dead and you
18:43
shouldn't have done that and there's
18:44
another bunch of people going that's
18:46
grand moff tarkin copyright Lucasfilm
18:48
Entertainment 1978 we own him you know
18:51
and you know who is it is it the actor
18:53
or the fictional character it's
18:55
triggered this really interesting left
18:56
ethical and legal debate but the point
18:58
is we can put I saw a review of the last
19:01
Jedi the last door which says we've now
19:03
that living actors playing dead
19:04
characters and dead actors playing
19:05
living characters it's come full circle
19:07
thanks to computer technology and we're
19:10
at the point where we can do anything
19:12
you could turn to your computer and go
19:13
you know what I'm bored what would it
19:15
have been like if they'd made friends
19:16
with Nicolas Cage playing all the parts
19:19
and we can just do that now
19:36
now the reason we can do things like
19:39
this is that we have created computers
19:42
and algorithms that work on the same
19:45
principle as some of the the most
19:47
complicated firmware in our own brains
19:48
you ever rely on your back in a field on
19:50
a sunny day and you're watching clouds
19:52
and your brain is kind of filling in
19:54
shapes for you it's cloud looks like a
19:56
rabbit that looks like an aeroplane that
19:58
whenever there looks like a house and
19:59
you're running all of these pattern
20:02
recognition algorithms and filling in
20:05
shapes and recognizing things and one of
20:06
the things that we are hardwired to do
20:08
is to recognize faces now we've got very
20:11
very good we don't entirely understand
20:13
how they work but we can now create
20:15
something called a convolutional neural
20:17
network you build a whole stack of
20:19
layers of logic and you give it input
20:22
you say these are cats and these are
20:24
dogs learn and it goes away and it
20:26
learns and it learns and it learns and
20:29
eventually it creates an algorithm that
20:32
you can give it a photograph and it will
20:33
say with confidence that's a cat or
20:35
that's a dog now you know that doesn't
20:37
sound terribly difficult right I mean
20:39
how hard can it be to tell a difference
20:40
between a puppy and a muffin you know it
20:47
can be a lot harder than you think
20:48
but we're getting good at this but what
20:50
gets really interesting is when people
20:53
take the dog detection algorithm the dog
20:56
detector and they wire it backwards and
20:59
they say this is now a dog amplifier and
21:01
the Machine goes alright and then you
21:04
give it a picture like this and you say
21:06
amplify the dogs and the computer says
21:09
this is a horrible idea please please
21:12
please don't make me and you say neural
21:14
network find the dogs and enhance the
21:16
dogs and it goes
21:19
you're gonna regret this and you cannot
21:21
turn up the power maximum dog
21:24
amplification and you get stuff like
21:26
this either this is a whole new kind of
21:29
art that has become possible because of
21:31
machine learning that nobody had ever
21:33
even thought of before and the technique
21:36
that's used to do this is something
21:37
called deep dreaming came out of a
21:38
project in Google in 2015 it's really
21:42
unsettling isn't it because you're
21:44
looking at it and what's happening is
21:45
those same circuits in your brain that
21:47
we've learned to emulate in in hardware
21:49
those circuits are going dog no it's not
21:52
dog dog no it's not a dog dog and kind
21:54
of your peripheral vision is finding
21:56
patterns you recognize but then when you
21:57
look at them it turns out you've been
21:58
tricked and so you get the kind of very
22:01
very complex perception around what's
22:04
going on with it now this is just one of
22:06
a whole bunch of ways that people are
22:08
using modern technology and software as
22:11
artists to create new kinds of art I
22:14
wanna introduce you now to a guy called
22:15
Robert Felker who I met in Warsaw the
22:18
other week who's doing some really
22:20
really interesting stuff when I start a
22:22
new art work it's just an inspiration
22:25
you just have a feeling so between the
22:28
first ID and the end wizard
22:31
there's just the same feeling it's not
22:33
about the visual I'm not interesting in
22:36
what you see I'm interested in what you
22:38
feel I'm Robert my everyday job I'm a
22:43
flutter dev and project manager and I'm
22:46
also photo artists previously I wasn't
22:50
kind of locked by the tool I can do a
22:53
lot of stuff but only what the tool
22:55
permits me when I found the flutter it
22:59
opened the door inside me now I can
23:03
really push further
23:05
[Applause]
23:07
generative art is a lot of research like
23:11
a lot it's a lot of failure it's a lot
23:14
of failure finding the color finding the
23:16
form understanding the good behavior of
23:19
light what's really good with flutter is
23:22
the speed of the feedback
23:24
it's nearly instant
23:29
currently artists do not understand the
23:32
full potential of the tool when you
23:34
start further you start with material
23:36
design or you start with the iOS
23:39
component and you think this is flat but
23:42
this is just the the tip of the iceberg
23:44
now if you want to push then you start
23:47
to enter the photo engine and the photo
23:50
engine is like the juice of the cone
23:55
each time I start to cut
23:58
I just feel joy so some people are
24:02
painting so people are cooking I just do
24:05
flutter and photo in and this is an
24:12
example of one of Roberts works this is
24:15
a photograph he took in Tokyo at night
24:17
that he then used machine learning to do
24:19
a depth perception analysis to identify
24:22
from the photograph the depths of all
24:24
the elements in this and then use
24:26
software and tools to creatively rebuild
24:30
the photograph working in layers and I
24:33
think this is quite beautiful it's kind
24:35
of hypnotic and every time you watch it
24:36
loop through it reveals something new
24:38
and this is just one of hundreds of ways
24:41
that artists are using code to create
24:43
new kinds of artworks we've never seen
24:45
before but what if we stopped talking
24:49
about using code to create art and we
24:52
start talking about code as an art form
24:56
in its own right now this very famous
24:59
book one of the great text books or
25:01
volume set of text books in computing
25:03
science Donald Knuth's the art of
25:05
computer programming and we can debate
25:07
for a long time is programming an art is
25:09
it science is it engineering is it
25:11
typing is it you know now but I'm sure
25:13
many of you have reviewed code that came
25:16
from somewhere maybe somebody on your
25:18
team was was tired or out of that depth
25:21
with it or maybe you were just having a
25:22
bad day and you look back at it a few
25:24
days later and you're like I don't know
25:26
what this is it's not engineering it's
25:29
not art I don't think it's terribly
25:31
creative I wouldn't dignify it by
25:34
calling it hacking I have no idea what
25:36
this is but fortunately there is now a
25:39
safe space for this kind of
25:41
code and these kinds of programs and it
25:43
is the International obfuscated
25:45
speedboat contest the goals are to write
25:49
the most obscure C program to show the
25:51
importance of programming style in an
25:53
ironic way to stress compilers with
25:55
unusual code to illustrate some of the
25:58
subtleties of the C language and to
26:00
provide a safe forum for port C code I
26:03
just like to share some examples with
26:06
you so this was a black I think Jonathan
26:10
Mills contributed this this is the
26:11
entire source code for this program very
26:13
C programs here in the room today
26:15
you want to tell me what this does and
26:17
it's just code right there's only one
26:18
screen of it how hard can it be
26:20
let's just run it and find out because
26:22
you know why not we'll just run that to
26:24
make file and then we'll run it and
26:26
there it is
26:27
it's flappy bird running in a terminal
26:34
here's another one lynnium zoom out give
26:38
you a little bit of context so this code
26:39
actually generates and draws the
26:41
Mandelbrot set in a text window and it
26:44
does it in a relatively kind of compact
26:46
code base that's shaped like the thing
26:51
it dramas which i think is rather neat
26:53
now brevity is one of the objectives of
26:56
obfuscated code you want to do something
26:57
really surprising with a very very small
26:59
amount of code this is the entire source
27:02
code for a program by a guy called Oscar
27:04
Pulido gee if you copy and paste this
27:07
into your web browser it plays chess it
27:11
doesn't draw a chess board it plays
27:13
chess it is a chess algorithm
27:16
implemented in just under a kilobyte
27:18
including JavaScript HTML graphics
27:21
behavior logic engines all the rules of
27:24
chess and an engine that is actually
27:25
better at chess than me this thing beat
27:27
me in games is that much JavaScript now
27:31
there are some astonishing examples of
27:34
programs that do wonderful things with
27:36
very very small amounts of code but none
27:39
of them is quite as good as this one
27:41
this was submitted to the International
27:43
obfuscated contest by Simona syncovich
27:46
in 2005 and it was accompanied with
27:50
documentation saying if you compile this
27:53
using this
27:54
compiler it will print its own source
27:56
code there's nothing here this is an
27:59
empty file but that compiler had a quirk
28:02
that if you fed it empty input it would
28:05
create a C program and compile it that
28:07
produced no output and so he quite
28:10
rightly said this program prints its own
28:13
source code now the obfuscated C
28:15
competition when okay one very clever to
28:18
have a price three we're changing the
28:19
rules from now on all programs have to
28:22
have at least one character of input
28:24
otherwise they are just this program
28:26
completed again but this idea of a
28:28
program that prints its own source code
28:30
is something called a quiet the word
28:31
comes from from this book which some of
28:33
you may have read which is that's kind
28:35
of fascinating riff on mathematics and
28:37
recursion and fractals and poetry and
28:40
music and stuff and it turns out that
28:43
writing a program that prints its own
28:45
source code is actually surprisingly
28:47
hard now you're not allowed to just read
28:49
it from disk and printed that would be
28:51
cheating you have to generate the source
28:53
from within itself so let's let's write
28:55
one I don't write a coin for you now
28:57
using c-sharp so we need a class program
28:59
with a static void main method and then
29:02
we obviously need to write line the
29:04
class program and close the bracket and
29:05
we need to write line the static void
29:07
main and now we need to write line the
29:10
right line and then we need to write
29:13
line the bright line with the and you
29:15
very quickly get tangled up in oh this
29:17
is just kind of e strings all the way
29:18
down but every language out there has
29:21
quirks loopholes that we can exploit to
29:24
make it do things that it wasn't
29:26
supposed to do now in c-sharp there is a
29:30
feature called string templating so we
29:33
can define a string that looks like this
29:35
and we can put placeholders in it these
29:37
little things here say when you see an
29:39
argument put that in the string at this
29:41
point and then we are going to feed this
29:44
string back into itself as a placeholder
29:46
variable so that when it gets to that
29:49
bit it prints itself and it doesn't go
29:51
into an infinite loop what it does is it
29:53
prints itself it prints its own source
29:55
code and different languages have
29:57
different loopholes you can exploit to
29:59
make coins JavaScript coins are very
30:01
easy because every function in
30:02
JavaScript has a two string that prints
30:05
it so this javascript function
30:07
itself in JavaScript and ACMA script six
30:09
this is a coin and I didn't believe this
30:13
because that doesn't look like anything
30:15
so I ran it in a console and sure enough
30:18
that's the output that gets produced
30:20
when you run it but what's really
30:22
interesting this is an idea I got from a
30:24
guy called Leon BAM brick who wrote it a
30:26
great post about this is can you make a
30:29
coin in HTML now HTML like you know is
30:32
it a real programming language I'm not
30:33
touching that argument can you write a
30:35
coin in it well let's find out here is
30:38
some simple HTML source code title head
30:41
body couple of paragraphs and a link to
30:43
Leon's original thing on this and this
30:46
is what it looks like in a browser right
30:49
start breaking some rules so first we're
30:52
going to put some style on that says
30:53
display everything as a block even
30:55
things that are supposed to be invisible
30:57
this star will match everything we run
31:00
that in a browser and now we can see our
31:03
CSS our source code is coming through in
31:05
that browser now we're gonna put some
31:07
rules in let's say well before HTML we
31:09
want you to display this and afterwards
31:11
you displayed this now the slash HTML is
31:14
actually down here off the bottom of the
31:15
screen because it knows it has to draw
31:17
it but we haven't told it where to put
31:18
anything and the safety is off at this
31:20
point we have no idea no the browser is
31:22
like you're on your own kids have fun we
31:24
plug in a bunch more rules style here we
31:26
have to put a backslash to escape the
31:29
slash because the web browser is
31:30
actually running three different passes
31:32
it's pausing HTML it's pausing CSS and
31:34
it's pausing JavaScript and they're all
31:36
fighting over who gets to eat the next
31:37
bit of input and at this point if we put
31:40
slash style our CSS parser is going to
31:42
go yep I'm done and HTML is gonna choke
31:45
on the rest of this chunk here so we
31:46
have to escape it now we have before and
31:50
after tags now there's no way of
31:52
generating these we just need to go and
31:53
plug-in head body title anchor paragraph
31:55
and we get this now you'll notice that
31:58
down here we've got this a but we don't
32:00
have the href equals with the web
32:01
address we want to link to can we do
32:03
that using HTML and CSS oh yeah no
32:07
problem
32:07
if you see a with an href we want you to
32:09
take this attribute and put it into some
32:11
content and stick it in before the thing
32:13
and there you go
32:15
and the last thing that we're going to
32:16
do just to make it look nice
32:18
is we're going to put a margin on there
32:19
and change the height of the age
32:21
and there we go we have a web page that
32:24
actually prints its own source which is
32:26
completely useless and utterly pointless
32:29
but how many of you learned something
32:31
you didn't know about the ages here's
32:33
our parser when you were watching that
32:34
little run-through there look at some
32:37
more here is some source code who wants
32:41
to tell me what language this code is
32:43
written in si si si any other votes for
32:47
si well let's let's apply a C
32:49
preprocessor to it well take out the
32:51
comments include standard IOH main char
32:55
I mean that the formatting on this is a
32:56
little wonky but yeah this is this is
32:58
fine this is completely valid C code but
33:02
what happens if we apply Ruby syntax
33:04
highlighting and highlight the strings
33:08
because that looks to me like perfectly
33:11
valid Ruby code right
33:15
let's try running it and see what
33:17
happens so I'm going to take that
33:21
program poly coin see there it is and
33:25
now I'm gonna feed that program into the
33:27
GCC compiler and I'm gonna run it it's
33:30
got a warning but we're way past the
33:34
point where we care about warnings and
33:36
there we go that program prints its own
33:38
source code and now because why not we
33:41
are going to run the same thing through
33:42
the Ruby interpreter and we are gonna
33:45
get look at that it prints its own
33:46
source code now we're going to run it in
33:48
Python because we can and it prints its
33:54
own source code and now hey in for a
33:57
penny let's run it in Perl and see what
33:59
we get
34:00
and it prints its own source code again
34:02
and apparently it'll also do it in C++
34:05
if you can find an old enough compiler
34:06
this is a poly coin this is a program
34:09
that is valid in more than one language
34:12
at the same time and in this example it
34:15
always prints its own source code now
34:18
who would like to tell me what language
34:20
this program is written in well let's
34:24
break it down alright let's do some
34:25
syntax highlighting so we got system dot
34:27
console which is kind of like a dotnet
34:29
II kind of a thing right and then we got
34:31
this chunk here which is an XML
34:33
namespace we got a console dot log in a
34:36
for each in the lower case so that
34:37
smells kind of JavaScript T to me right
34:39
we've got an ADA textio procedure we've
34:44
got begin in capital letters which is
34:46
either COBOL or SQL it's definitely from
34:48
the 1970s and it lives in a bank and up
34:52
here we've got act 1 scene 1 enter Ajax
34:55
which doesn't look like any program I've
34:58
ever seen now this is an excerpt from
35:02
something called the or Robert Quine
35:05
it's a ruby program that creates a rust
35:08
program and the rust program creates a
35:10
scholar program and the scala program
35:12
creates a scheme program which said
35:14
Shakespeare all the way around the
35:15
circle 128 languages until you end up
35:19
with a RC program that creates a Rex
35:21
program that creates the original rust
35:24
program again this was written by a
35:27
Japanese developer called Yosuke and
35:29
though who
35:29
one of the contributors to the Ruby core
35:31
language and the fact that it exists at
35:34
all is astonishing this is what the
35:37
source code to that coin looks like
35:42
[Laughter]
35:46
which is also incredible and if you zoom
35:49
in on the end of the source code you'll
35:53
notice that the last four lines all just
35:55
say buffer for future bug fixes because
35:57
they don't want to mess up the shape of
35:59
the source you know now this is the most
36:05
astonishing thing about this all 128 of
36:08
those languages can be installed on a
36:10
win to Linux by going apt-get recs
36:12
apt-get Shakespeare apt-get TC so there
36:15
is a github actions continuous build
36:17
pipeline for this thing that whenever
36:19
changes to it are committed it runs them
36:20
through all 128 languages and tells you
36:23
whether it succeeded or not which I just
36:25
think is fantastic and you know weird
36:28
but I love the fact that we can do that
36:30
but let's backtrack a little bit in that
36:33
chunk of code we looked at there was
36:34
some C and there's some JavaScript but
36:36
there's also act 1 scene 1 & 2 Ajax now
36:39
that is an excerpt of a program written
36:43
in the Shakespeare programming languages
36:45
one of a family of what are called the
36:47
esoteric languages ISA Lange's and
36:49
Shakespeare is designed to let you write
36:51
computer programs that are also
36:53
Shakespeare plays this is hello world in
36:57
Shakespeare the infamous hello world
37:00
program now all variables in Shakespeare
37:02
have to be declared as the characters in
37:04
the play so we have Romeo and we have
37:07
Hamlet act 1 scene 1 that's a namespace
37:10
and a block enter Hamlet in Romeo this
37:13
is variable scope we are dealing with
37:15
right now and then the way variables
37:18
work in Hamlet is when they say nice
37:20
things they increment and when they say
37:23
insulting things they decrement so at
37:26
this point Hamlet is talking to Romeo
37:28
and Hamlet says you lying stupid
37:31
fatherless big smelly half-witted coward
37:33
you are a stupid as the difference
37:35
between a handsome rich brave hero and
37:37
myself speak your mind
37:40
that puts the letter H into Romeo and
37:43
then outputs it because H is the first
37:47
character in hello world the next chunk
37:50
here will print e and so on hello world
37:53
and Shakespeare is about three pages of
37:55
fairly florid prose which is fine
37:58
because it's Shakespeare and that's what
38:00
it's supposed to look like how about
38:03
this one can anyone tell me what
38:05
programming language this is written in
38:07
this is white space let's have a look at
38:10
that with syntax highlighting applied
38:12
white space is a programming language
38:15
that only cares about spaces and tabs it
38:18
ignores everything else it's brilliant
38:19
if you want to hide programs inside
38:21
other programs mix up your tabs and
38:23
spaces and you can put whitespace
38:25
alongside anything else this is hello
38:27
world in white space let's take a look
38:30
at the hello world souffle now this is a
38:33
programming language called chef and
38:35
chef is designed for writing programs
38:37
that are also recipes now 72 grams of
38:43
haricot beans a hundred 1 X 108 grams of
38:46
lard 111 cups of oil you know 33
38:50
potatoes it's a valid program but would
38:53
you like to eat this souffle you know
38:56
and so somebody called a guy called Mike
38:59
worth looked at the chef's programming
39:01
language and when challenge accepted I'm
39:03
going to write a hello world program
39:04
that's actually a sensible recipe you
39:07
can make in your kitchen and he came up
39:09
with the hello world cake with chocolate
39:12
sauce now I think this is brilliant if
39:15
you compile this on a computer it says
39:18
hello world if you compile it in a
39:20
kitchen you get an edible cake with a
39:23
kind of chocolate sauce ganache that you
39:24
can pour over the top of it but the
39:26
thing I think about this that's
39:27
beautiful is if you didn't know about
39:29
chef you'd think this was just a recipe
39:32
it fits so well into two different
39:35
domains of human creativity that from
39:38
one you'd have no idea that it also
39:39
worked in the other one I'm going to
39:42
show you how to square a number in a
39:44
programming language called Pete that is
39:48
how to square a number in Pete
39:51
Pete is named after the Dutch artist
39:53
Piet Mondrian and Piet is a graphical
39:56
language where the instruction set is
39:58
dictated by what happens when you cross
40:01
from one color into another every Piet
40:04
program starts with an instruction
40:05
pointer in the top-left travelling
40:07
towards the right traveling due east so
40:10
what's actually happening here is when
40:13
we cross from light blue to dark green
40:15
that says input a number prompt the user
40:17
and put that on the top of the stack
40:19
when we get to black turn the
40:21
instruction pointer through 90 degrees
40:22
when we cross from green into red that
40:25
means whatever's on the top of the stack
40:26
duplicated when we cross from red to
40:30
yellow multiply top two numbers off the
40:32
stack multiply them put the product back
40:34
on the stack when we cross from yellow
40:37
into red that is output whatever is
40:39
currently on the top of the stack omit
40:41
that to standard out when we cross white
40:43
that is a no operation we reach the end
40:45
of the grid we turn right again and then
40:48
we follow this blue instruction certain
40:50
till we end up with black on all sides
40:51
which means you have reached the end of
40:53
the program please hold so that's a
40:55
completely Turing complete language
40:57
whose instruction set consists of areas
41:00
of light and shade and the transition
41:02
between colors this is hello world in
41:05
Piet one of many many examples but you
41:09
could hang this on the wall in your
41:11
house and somebody could come in and
41:13
take a look at it
41:14
they'd have no idea they were looking at
41:15
hello world they just think you like
41:17
kind of slightly weird 16-bit art you
41:19
know the Windows 3.1 school of
41:21
Expressionism now we've talked so far
41:25
about this whole idea of you know using
41:28
we've talked about using code to create
41:30
art we've talked about code that is art
41:32
and over the course of MDC you've
41:34
probably seen a couple of speakers here
41:36
doing live demos which are you know the
41:38
the tightrope the high wire act ooh the
41:41
death-defying circus thrill of the
41:43
technology industry because someone is
41:45
coding something on a laptop live and it
41:47
might work and it might not work and
41:49
there's always this element of kind of
41:50
risk and then it works and it runs like
41:52
yeah and you got a big round of applause
41:53
but generally as an industry we don't
41:56
like that you know we like consistency
41:59
we like reproducibility we like
42:01
automation we like being able to do the
42:03
same thing over an
42:04
over and over again if you've ever
42:06
worked in a place where there is a
42:08
server under a desk or maybe in a rack
42:11
somewhere that's running Windows 2003
42:13
Small Business Edition and you're not
42:16
allowed to touch it
42:17
do not put Windows Update on that or the
42:19
payroll will stop working on pain of
42:22
immediate gross dismissal you know and
42:25
we have a name for these kinds of boxes
42:27
that everyone is frightened to touch we
42:30
call it snowflakes snowflake servers
42:32
snowflake processes it's completely
42:34
unique but if you go out in the snow and
42:38
you pluck a snowflake out of a blizzard
42:40
and you watch it melt on your hand you
42:43
have just been part of a performance
42:44
that will never ever be repeated
42:46
anywhere your participation in that has
42:49
created a unique human experience that
42:52
nobody else will ever understand or be
42:55
part of and maybe we can do the same
42:58
kind of thing using code this guy here
43:01
is Sam Aaron and Sam is the creator of a
43:06
programming language called Sonic pi was
43:08
anyone in the last talk in this room
43:09
yesterday where Laura did her talk about
43:11
programming with music and she was
43:14
showing us had a program write computer
43:16
programs whose output is not text or
43:18
graphics it's music and tones and sounds
43:21
and melodies and she ended up by you
43:24
know doing this this wonderful kind of
43:26
layering thing because sonic pie is a
43:28
live coding music synthesizer I'll give
43:32
you a very quick demo of how sonic pie
43:33
works which I'm not gonna live code for
43:35
you because I don't want this to get too
43:37
meta
43:37
now when you start sonic pie it gives
43:40
you a prompt and you say play this note
43:42
and it plays that note now sonic pie
43:46
runs all your instructions in parallel
43:47
unless you tell it not to imagine if
43:49
JavaScript if you want things to happen
43:52
one after another you have to put sleep
43:55
instructions in and say we want to
43:56
introduce some kind of delay to this and
44:00
where it gets really interesting is we
44:03
can go in and we can start putting loops
44:05
around our notes and our musical
44:07
patterns so we got 16 times do that and
44:10
we've got the world's least exciting
44:12
bass line going
44:13
so let's crank up the tempo a little bit
44:16
we're gonna say use beats per minute
44:17
240-foot all right we're getting
44:21
somewhere and we're gonna change it
44:23
because the sine wave is not a terribly
44:24
exciting noise we're gonna use a
44:25
built-in synthesizer here called Tex
44:27
Soares now this is interesting but where
44:34
it gets really interesting as you'll
44:36
have seen in Laura's talk yesterday is
44:38
when we introduce the concept of
44:40
something called a live loop now live
44:42
loops allow you to run multiple
44:44
components of your program so I'm gonna
44:49
put a light blue there around that
44:50
baseline and then I am gonna drop
44:53
another loop over the top of it
45:00
[Music]
46:07
the fizzbuzz now sonic pie is fantastic
46:12
it's enormous amount of fun to play
46:13
around with I've seen people do live
46:15
coding with multiple you musicians that
46:17
picture of the beginning was Sam on
46:18
stage with the London Philharmonic
46:20
Orchestra doing live coding in the Royal
46:22
Albert Hall and you know it's an
46:23
absolutely astonishing tool and just one
46:26
of the brilliant and creative ways that
46:28
we're coming up with to use code to do
46:30
fascinating and unexpected things but I
46:34
want to finish today I've talked you all
46:35
about all kinds of things that other
46:36
people did I want to finish by telling
46:38
you about something that I did now you
46:41
are probably familiar with the trope of
46:43
the rock star developer because we've
46:46
all read job advertisements from people
46:48
looking for a rock star senior front-end
46:50
rock star JavaScript engineer rock star
46:53
senior Java software developer this has
46:55
been endemic in our industry for years
46:57
and last year Paul Stovall put this on
47:02
Twitter he said to really confuse
47:04
recruiters someone should make a
47:05
programming language called rock star
47:07
and I had this experience because I
47:12
thought this is it this is my purpose
47:15
this is why I was put here because what
47:18
the world clearly needs is a programming
47:22
language that allows you to write
47:24
programs that are also bad 1980s
47:27
heavy-metal songs and so rock star was
47:31
born a dynamically typed Turing complete
47:33
programming language for creating
47:34
computer programs that are also song
47:36
lyrics heavily influenced by the lyrical
47:39
conventions
47:40
of 1980s hard rock and pala balance now
47:43
Rockstar was created in a bar as a joke
47:46
that will become important shortly sad a
47:50
bar with a laptop and a beer and
47:52
thinking
47:52
could you make a language where rock
47:54
songs could compile to something now I
47:56
used to work in VB script and Perl a lot
47:59
and I've done work in Ruby so I'm used
48:01
to languages which try and you know
48:03
borrow a lot of elements from natural
48:04
language and incorporate them into
48:05
programming syntax so I thought all
48:08
right first of all if you were write
48:09
songs in it there's more than one way to
48:10
do it like the Perl idiom attempt Tony
48:12
you know so HelloWorld in rock star is
48:15
say hello world or scream or whisper or
48:18
shout these are all syntactically valid
48:21
programming requires variables and
48:23
assignment now you're probably used to
48:25
in x equals five var my string the
48:28
message now we don't need int because
48:32
rock star is a dynamically typed
48:34
language we are going to take those out
48:36
we don't need semicolons on the end
48:38
because if JavaScript can live without
48:40
them so can we now the equals sign in
48:42
the middle how do you sing that and
48:44
those you know let's just put is X is
48:47
five my string is hello world
48:49
the message is flutter rocks because I
48:50
forgot to update that that should say
48:52
NDC rocks now there's this ongoing
48:56
debate about casing you've had one of
48:59
those arguments longer than an hour
49:00
about Pascal case versus camel case
49:02
versus get bad case versus underscore
49:04
case and I shall Douglas Crockford the
49:06
guy created JSON give a talk two years
49:09
ago where he said we have all these
49:10
stupid arguments what we want are
49:12
variable names with spaces in them well
49:15
guess what when you're inventing a
49:16
programming language in a bar you can do
49:18
anything you like
49:18
so Rockstar has variable names with
49:21
spaces and it's not a complete
49:22
free-for-all there are three kinds of
49:24
variables simple variables work like
49:26
they do in JavaScript and Ruby common
49:28
variables have to start with my you're
49:30
the an a and proper variables need
49:33
capital letters so we can write programs
49:35
about dr. feelgood and black Betty and
49:36
Billy gene and all these you know great
49:38
characters who inhabit the world of rock
49:40
and roll
49:40
now initializing variables we normally
49:43
do with numbers fizz is three buzzes
49:46
five the limit is 100
49:48
I didn't want to do this because it
49:51
doesn't sound terribly metal really and
49:54
I thought how can you define a numeric
49:57
literal without having to use digits in
49:59
your source code and I had this idea
50:00
what if we take the lengths of the words
50:04
modulo 10 and we treat those as digits
50:08
so ice is 3/5 the limit is a love-struck
50:13
Ladykiller one that's 10 10 modulo 10 is
50:16
zero zero we've got three we've got five
50:18
we've got 100 without having to put
50:20
digits in our source code it works with
50:23
floating-point numbers as well and C
50:25
decimal PI 3.14159 and JavaScript var pi
50:28
equals we're kind of almost you probably
50:31
got something close to that back out
50:32
because hey JavaScript right in rock
50:35
star my heart was ice a life unfulfilled
50:39
waking everybody up taking booze and
50:41
pills 3.14159265 3/5 easy right you
50:50
gotta have to do arithmetic right now we
50:53
have these common you know ways of
50:54
talking glitch how much is it I the
50:55
total is the price with the tax well
50:57
what about the the net Anana that's the
50:59
total without the tax how many do you
51:01
need get me the quantity of the product
51:03
how fast were you going well speed is
51:05
the distance over the time you know we
51:06
have these things it's easy but this
51:08
mathematical convention also allows us
51:10
to write a girl with a dream a man
51:13
without a face the wings of the night
51:15
and a whisper over the water we need
51:17
comparison your love is a lie true or
51:21
false
51:21
well is it the whiskey ain't the answer
51:24
my heart is stronger than steel and my
51:27
soul is weaker than water as strong as a
51:29
lion as low as a snake we'd each
51:32
function syntax now the sort of
51:35
simplistic version here let's have a
51:37
function modulus it takes a number and a
51:39
divisor so those are input arguments and
51:41
while a number is as high as a divisor
51:43
put a number without a divisor into a
51:45
number and give back a number this is
51:47
how you implement modulus when your
51:49
building blocks are just addition and
51:50
subtraction and loops and stuff now this
51:53
works but we can do better right because
51:57
midnite takes your heart and your soul
51:59
and while your heart is as high as your
52:01
soul you
52:02
put your heart without your soul into
52:04
your heart and give back your heart now
52:08
at this point I'm about three beers in I
52:10
have a parody specification that is just
52:13
complete enough to implement fizzbuzz
52:14
and I have fizzbuzz in Rockstar I stick
52:18
this thing up on github and I'm just
52:20
like hey everyone introducing Rockstar
52:22
proposal for a turing-complete
52:24
programming language and I think this is
52:26
gonna be funny for like three hours you
52:28
know it gets 2,000 github stars
52:32
overnight it makes the front page of
52:34
hakkon news and just kind of starts this
52:37
buzz it made it into a Boing Boing
52:39
magazine Cory Doctorow wrote a thing
52:40
about it in there it made the front page
52:42
of Reddit people and reddit we're
52:44
actually saying complimentary things
52:46
about it the weirdest thing that
52:48
happened is I got an email from classic
52:52
rock magazine which is a real music
52:55
magazine that is nothing to do with
52:56
computers saying what's this Rockstar
52:58
thing that we keep hearing about so I
53:00
wrote a little thing for like an email
53:03
interview for them and I'm thinking like
53:05
this can't possibly get any weirder and
53:06
then people start filing issues against
53:09
my parody specification and I'm looking
53:16
at these and you know some of them are
53:17
just ideas like what a fool the numbers
53:19
go up to 11 and I'm like don't know that
53:20
arithmetics hard enough as it is but
53:22
some of them are like this undefined
53:23
behavior and I'm like what do you mean
53:25
there's undefined behavior why do you
53:26
care and they're like I built a rock
53:28
star compiler in Scala over the weekend
53:30
and it has edge cases like you did what
53:33
and within about a week there was a
53:35
Scala interpreter so I would have built
53:38
a compiler for in rust somebody had
53:39
built a rock star to Python transpiler
53:41
and the fascinating thing is all of them
53:44
had managed to do like 95% of it just
53:47
based on this random stuff I came up
53:49
with in a bar as a joke and some of it
53:52
makes no sense and you know if I'd known
53:54
it was ever gonna be real I'd of course
53:55
have done it differently but programming
53:57
is like that you know now I really liked
54:01
the idea of Dylan Beattie the creator of
54:04
rock star and I didn't think I'd done
54:05
enough work at this point to really earn
54:07
that and I also wanted rock star to be
54:10
you know scholar and Rustin and Python
54:12
are all very well but I want it to be
54:13
something accessible something
54:15
that anybody could just open up in a web
54:17
browser and write some Rockstar code and
54:19
see what it did and so this time last
54:22
year I basically spent about five
54:24
weekends we teaching myself how to build
54:26
compilers and parsers and meta-circular
54:28
evaluator x' and stuff and i built a
54:31
rock star interpreter in javascript
54:32
which is definitely the stupidest
54:34
dumbest thing i've ever done
54:35
and it's online and it is here it is at
54:38
code with rock star calm and everybody
54:41
here in this room is welcome to go and
54:43
try this put some code in there and you
54:46
will then be a rock star developer now I
54:49
just want to shout out one thing the
54:50
logo here in the top left I wanted to
54:53
borrow some like real over-the-top
54:55
access 1980s rock and roll heavy metal
54:57
influences and I looked at dudas priest
55:00
and Iron Maiden and Motley Crue and all
55:02
these kinds of people and then somebody
55:03
said have you thought about Microsoft
55:05
consumer products 1980 to 1982 and I was
55:09
like that is exactly what I want that
55:11
logo type is perfect so thank you
55:13
Microsoft for letting me recycle your
55:15
old logo be green now I do have some
55:18
certified Rockstar developer stickers to
55:21
give away here at NBC so come up
55:23
afterwards with your code with Rockstar
55:24
comm code on your phone and I will
55:26
certify you you will become a member of
55:28
the world's most prestigious developer
55:30
program but to end the talk today I'd
55:33
like your help in something now I showed
55:35
you some examples in there of like hello
55:37
world and Pete that just looks like a
55:39
painting and the chef hello world
55:41
chocolate cake that could just be a cake
55:43
and if you like the the test of whether
55:46
Rockstar really succeeds as a language
55:48
is can you perform a rock star program
55:53
and have people just think it's a bad
55:55
heavy metal song from the 1980s and so
55:58
with your indulgence I'd like to close
56:00
NBC and this talk by performing live
56:03
fizzbuzz in rock star
56:08
[Music]
56:46
takes your heart and your soul while
56:52
your heart is as high as your soon put
57:01
your heart without your soul into your
57:08
[Music]
57:12
give back your heart you remember the
57:18
fizzbuzz riff
57:19
[Music]
59:33
[Music]
59:44
[Music]
59:46
[Applause]
59:49
[Music]
60:05
[Applause]
60:10
[Music]
60:11
thank you very much in DC thank you for
60:20
coming thank you for your time thank you
60:21
for listening
60:22
who's going to pub gun if you thought
60:25
that was silly we got way more stuff in
60:27
store if you don't if you're coming to
60:29
pub gun I will be emceeing tonight we
60:31
got 12 amazing speakers lined up with
60:33
five-minute funny talks there are still
60:35
tickets on sale if anyone doesn't have
60:36
plans tonight
60:37
Pupkin oh if you are not coming to
60:39
PubCon thank you very much I will see
60:41
you somewhere out on the road have a
60:43
wonderful weekend
60:44
see you soon bye-bye
60:47
[Applause] 
```

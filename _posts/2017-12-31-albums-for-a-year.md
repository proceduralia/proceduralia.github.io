---
layout: post
title: "Albums For A Year: towards introspecive data science"
categories:
  - Home
tags:
  - machine learning
  - data science
  - spotify
  - music
  - literature
---
![pirandello](/assets/images/pirandello2.png){:class="img-responsive"}
Luigi Pirandello was an outstanding author, whose writings shine in the history of European literature.
Apart from a considerable number of plays and novels, he wrote also many _novelle_, (not too) short stories
gathered in the collection _Novelle per un anno_ ("Novelle for a year").

_Novelle per un anno_ is a masterpiece: some 250 stories written in more than 50 years 
compose a wonderful exploration of human nature through umorism, sadness and deep thoughts.

Pirandello's original idea was to write a short story for each day of the year,
but this ambitious aim was stopped by his death, in 1926.
Last year I was reading _Ciaula scopre la Luna_, one of the most famous stories
from the collection and at some point I have suddenly understood a glimpse of the true
meaning of such a huge work. It's not about being a virtuoso of writing,
showing abilities on a range of different fictional scenarios or different
styles; it's not even about telling stories _per se_.
Pirandello gave us his collection in order to experience __exo-thought__.

# Exo-thought through art
---
Assume you read a new short story more or less every day. Initially, you just
enjoy the interesting plots and the wonderful writing style. Day after day, story after story,
you will start to experiment your reading on a new level. Indeed, you will start to discover a new kind
of thinking, and you will be able to experience the stories in a different way: the book will likely start to behave as
an extension of yourself.
All of the values, evocative powers, existential insights contained in the stories will be considered
by your thinking process in the same way as the original content of your mind.
This perceptual experience is similar to a new pair of special glasses, that you can use to see
the world differently.

Perspective augmentation phenomena can be probably generalized as being part of many experiences,
for example related to any other kind of art:
once you become familiar with a particular art form, you acquire a new set of thinking tools that
you can use during your interactions with that kind of pieces of art.

We can call it _exo-thought_, or thinking outside of youself. In some way, we
delegate part of our thinking process to the tools provided by an external medium.
In the case of reading, for example, we are in general delegating part of our ethical thinking to the one infused by
the writer in the written words,
or part of our sensorial processing to the descriptions contained in the text.

One of the best ways to become familiar with a tool, or with an art form, 
is to experience it as often as you can.
From this follows the outstanding augmentation power that Pirandello's _Novelle per un anno_
can have on its reader.

# Algorithms and exo-thought
---
We are all familiar with _exo-thought_, as it happens in our daily life.

For instance, a rather modern way to experiment it comes from the use of
our favorite user interfaces.
This concept is amazingly explained in these outstanding articles about 
[thought as a technology](http://cognitivemedium.com/tat/){:target="_blank"} and
[intelligence augmentation using artificial intelligence](https://distill.pub/2017/aia/){:target="_blank"}.
To align my terminology with the one used by Michael Nielsen, 
an _exo-thought_ can be said to be the use of a _cognitive technology_, that is

> an external artifact, designed by humans, which can be internalized, and used as a substrate for cognition.

In other words, 
once we become familiar with a new _cognitive technology_, we unlock
the power of a wonderful symbiosis between our own thinking and an external process, 
and human intelligence augmentation kicks in.

Astonished by this kind of symbiosis, I wanted to replicate the experience I had
reading _Novelle per un anno_.
Thus, I started thinking about one of the most fascinating and efficient symbiosis
of the modern world, the one occurring between humans and machine
learning algorithms.

I chose a domain -- music -- and a platform -- Spotify -- to perform my experiments.
Spotify offers a series of services to discover new music: useful tools
like _Discover Weekly_ -- a playlist that recommends to you new songs
that you are likely to enjoy - or _Release Radar_ - another
playlist containing new releases apt to your musical tastes.
If you look at them without proper attention, it doesn't seem like
a viable strategy for _intelligence augmentation_:
recommendation engines like this, after all, are widely used in many
websites and services we are well accustomed to.

Here came an idea: what if instead of using this powerful tools
in an absent and passive way, we try instead to integrate as deep as we can our human domain knowledge
and sensibility with them?

A realization of this intent was inspired by the work
of Pirandello: trying to listen to a new music album _(almost)_ every day for a whole year.
With this project in mind, codenamed _Albums for a year_,
I tried to exploit both the art-based _exo-thought_ and the
algorithmic _exo-thought_, in order to perform a new kind of intelligence augmentation.

The procedure that I used weekly in this process was the following:
- Listen to the new songs in _Discover Weekly_ and _Release Radar_
- Find the ones that I enjoyed the most and follow them as pointers to music albums
- Listen to the full albums from which the songs are taken
- Listen to other albums by the artists that made the albums I enjoyed the most
- Find new albums independently from the suggested tracks

# Introspective data science
---
Altough akin to the experience of reading
the collection of stories written by Pirandello, the
possibilities offered by modern technologies are even greater.
We likewise navigate, discover and meditate on novel information through our new perspective,
using both our art-based and algorithm-based _exo-thought_, but we
can also perform a new kind of operation, powered by software.
We can easily collect, display and analyze our own data.
To some extent, we can perform __introspection__, 
the self analysis of a thinking process.
In doing so, we exploit the wonderful toolbox offered by data science.

The first step is data collection:
I created a playlist and added each new album to this playlist
when I started listening to it.

# An year of listening habits
---
A first way to perform introspection is to look at the frequencies
and patterns in my musical routine.
Spotify automatically saves the time a song is added to a playlist;
in other words, I can retrieve the time 
I started listening to each one of the albums.

{% include graphs/frequency_scatter.html %}

Looking at the representation, I can basically track my listening
habits throughout the year.
They are both conditioned by mood and life events.
For instance, I initially used to listen
to my daily album early in the morning; but after summer
I began to find some other spaces for music, for
example during the evening.
Another observation I can make on my own habits is the
sparsity of albums we can observe in the right part of the graph,
due mainly to the imminent graduation and subsequent distractions.

# Representation matters
---
Apart from thinking on metadata like the listening date,
one can also reason on the content of the albums itself.
In order to do that, we need to find a suitable representation
for an album: for example, we could represent it using solely
its name and artist, but that wouldn't be enough for some kinds of analysis.
Therefore, it's better to choose a numeric representation, leveraging some of
the data offered by Spotify. I basically worked with two representation models,
each of them representing an album in a way related to:
- The genres of the artist that recorded it
- The musical features of the songs included in it

For the genres representation I considered the whole set of genres given by Spotify
to all the artists in _Album for a year_ and I transformed each album into a one-hot vector,
i.e. a vector full of zeros, with a one only in the positions associated to genres
of the album artist.

The total set of genres has a size of 212, but each album commonly has 4-5 genres.
In other words, this is a very sparse representation.
For example, among the 212 elements of the vector representing 
_Recomposed By Max Richter: Vivaldi, The Four Seasons_, only
the spots associated to _compositional ambient_, _focus_, _minimal_,
_modern classical_ and _soundtrack_ are set to one.

# Albums as a graph
---

We can't directly visualize all of this data:
the only visual way to get some insights is to reduce its 
dimensionality.

We can, for instance, represent our data as an undirected graph,
with each node being an album and each arc existing between two nodes
if the corresponding albums share at least one genre.
The weigth on the arcs is equal to the exact number of shared genres.

Once obtained this graph, we can visualize it using the
Fruchterman-Reingold force-directed algorithm,
a physics based method that produces very good visual layouts.
You can click on a node to highlight its neighbours.

{% include graphs/albums_graph.html %}

Although no explicit clustering technique is used, some
groups are clearly visible. 
The one on the right, for example, is mainly formed of
renditions of classical music works from composers
such as Bach, Chopin and Brahms.
Going towards the center, modern classical music arises,
in the form of soundtrack and neoclassical albums. To be honest,
I didn't realize this was the genre I listened to the most
during the whole examined period until I noticed
this is by far the densest
area in the graph.
The remaining albums are mainly grouped in the jazz cluster in the lower-left corner
and in the rock cluster on the upper-left.

# Embedded albums
---

Another way to visualize the genre representation of the albums is to use some
statistical technique to go from 212 to 2 dimensions.
This process is usually called _dimensionality reduction_ and can be carried out
by means of several methods.
I obtained satisfying results on my sparse data
with the one called _laplacian eigenmaps_,
or _spectral embedding_. Under the hood, it works constructing a graph from the data
and decomposing it using _eigendecomposition_.

{% include graphs/binary_repr_se.html %}

This 2-dimensional view of the data has an interesting shape, that immediately leads me to another
_introspective insight_: the classic jazz from Miles Davis, Thelonious Monk and friends
is maybe the most different category, in genre, from  my main listenings of _neoclassical_ and
_alternative rock_.

Albeit one can visually infer the existence of some clusters,
it can be also done algorithmically. For example, we can use _k-means_,
and find _k_ clusters associated with our reduced data. Moreover, we can use the so called
_elbow heuristic_ to select a proper value for _k_.

{% include graphs/elbow_kmeans_se.html %}

We aim at finding the best tradeoff between the number of clusters and the
error in the assignment of points to clusters. In practice, a good point is the one in the elbow
of the curve obtained plotting the total error with different _k_ values: in our case, it is between
2 and 3.
Let's use 3 clusters and update our plot.

{% include graphs/binary_repr_se_kmeans.html %}

Unfortunately, the genre binary representation doesn't discriminate
albums of the same artist,
because only artists, and not albums, have associated genres retrievable from Spotify:
this results in several
overlapping albums in the plot.
But _every model represents only a view of a real problem_.

# Audio features and T-SNE
---
Another way to represent the albums uses some audio features that Spotify offers for songs.
They are very descriptive quantities, indicating, for example, the degree of confidence
with which you can say a song is acoustic, or its tempo.
A straightforward way to extend this representation from songs to albums is to
consider an album as the mean of the vectors containing the features of its songs.
In this way, we obtain 12-dimensional description of the albums from the playlist, again,
impossible to visualize as is.

We can use a different method to perform dimensionality reduction, for example _t-sne_.
Guided by the _Distill_ article on 
[how to use t-SNE effectively](https://distill.pub/2016/misread-tsne/){:target="_blank"}, I searched for
the better _perplexity_ to visualize the data.

{% include graphs/encoded_se.html %}


The result is quite different from the previous ones. Looking solely at the audio
features of an album and forgetting about its declared genres, many musical styles
become near in the visual representation. For example, the distinction between _classical_
and _neoclassical_ almost
disappears. Moreover, jazz albums can be found in the neighbourhood 
either of the rock or of the classical ones,
depending on their type of musical contamination.

The insight I can get from this is that, despite the abundance of genres in my
_Album for a year_ playlist, the diversity in musical features is probably not
likewise evident.

It's rather intuitive that the _musical language_ of a genre is encoded in some way in the
musical features of its songs. Nonetheless, the similarity among songs strongly
traverses the genre barrier, and, don't considering for a moment aspects such as melodies and timbres,
the general appeal that a song has on our personal tastes
is given by a combination of its musical features and our bias towards its genre.

# Conclusions
---
The analysis I've conducted so far is really far from extensive, but
I think it's useful to visually dive into some of the material we use daily.
It can easily give us an intuition on how we perceive and think,
leveraging data analysis and visualization for a different purpose than the
usual ones related to business or research.

During the year, I learned to interact in a profound way with a part of
the recommendation engine of Spotify.
For my final analysis I chose not to distinguish between the albums I selected by myself and the
ones indirectly suggested by the automated playlists, simply because
this distinction slowly disappeared, as my degree of confidence with the whole
system became higher and higher. _This_ seems to be
the essence of _exo-thought_ and _intelligence augmentation_.

{% include bokeh_includes.html %}

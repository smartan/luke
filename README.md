luke
====

![Luke, the Lucene Toolbox Project](src/main/resources/img/luke-big.gif)

Luke is the GUI tool for introspecting your Lucene / Solr / Elasticsearch index. It allows:

* Viewing your documents and analyzing their field contents (for stored fields)
* Searching in the index
* Performing index maintenance: index sanity checking, index optimization (take a backup before running this!)
* Reading index from hdfs
* Exporting the index or portion of it into an xml format
* Testing your custom Lucene analyzers
 
Recent Changes
====
See [CHANGES.txt](CHANGES.txt)

Luke discussion group
====
[Luke google group](https://groups.google.com/forum/#!forum/luke-discuss)

Intro video about features
====
This lightning talk was delivered by Dmitry Kan on ApacheCon 2015 in Austin, Texas.
[![ScreenShot](https://github.com/DmitryKey/luke/blob/master/docs/img/ApacheCon_Luke_lightning_talk.png)](https://www.youtube.com/watch?list=PLGeM09tlguZTaS5FNoJGYEohaubtIvErS&v=fQAAzpk4oQ4#t=392)

Brief project history
====

* The original author is [Andrzej Bialecki](https://code.google.com/p/luke)
* The project has been mavenized by Neil Ireson (see google group discussion [here](http://bit.ly/16Y8utO))
* The project has been ported to Lucene trunk (marked as 5.0 at the time) by Dmitry Kan
* The project has been back-ported to Lucene 4.3 by sonarname, who later decided not to continue supporting the project
* There are updates to the (non-mavenized) project done by [tarzanek](https://github.com/tarzanek/luke)

This project's goal
====

0. Keep the project mavenized (compatible with Apache Lucene and Solr style)
1. To port the thinlet UI to an ASL compliant license framework so that it can be contributed back to Apache Lucene.
   Current work is done with Apache Pivot (https://github.com/dmitrykey/luke/tree/pivot-luke). Grab a released version of pivoted luke for lucene 5.2.1 here: https://github.com/DmitryKey/luke/releases/tag/pivot-luke-5.2.1
2. Maintain a single point of trust for the development and updates of the tool. That said,
   everyone is welcome to join.

Committers
====
* [Dmitry Kan](https://github.com/DmitryKey)
* [Tomoko Uchida](https://github.com/mocobeta)

Launching luke
====
1. Clone the repository.
2. Run `mvn install` from the project directory. (Make sure you have Java and Maven installed before doing this)
3. Use [luke.sh](luke.sh) or [luke.bat](luke.bat) for launching luke from the command line based on the OS you are in.

(Alternatively, for older verions of luke you can directly download the jar file from the [releases](https://github.com/DmitryKey/luke/releases) page and run it with the command `java -jar luke-with-deps.jar`)

Running luke with a custom analyzer or codec
====

See [luke.sh](luke.sh) for an example of launching luke with custom components.

Documentation
====
The documentation is being written along the way of discovering the luke's usage scenarios.

https://github.com/DmitryKey/luke/wiki

You are free and welcome to contribute you findings!

Feature / bug fix requests
====
Found bug? Missing a useful feature? Raise an issue here:

https://github.com/DmitryKey/luke/issues

Or, and btw, the pull requests are welcome as well!

Releases
====

All of the releases you find under the "releases" link above are versioned after the Lucene's version they use.

Usually we don't do releases for minor version upgrades, because the major release usually can read the index of the next
minor release.

An example: lucene 4.8.0 can read the index generated by lucene 4.8.1. Hence the luke 4.8.0 can read too.

Conclusion: in order to find a luke release that can read an index of your version of Lucene, pick the closest major version
and download the luke for that from the releases page above.

Where is luke 4.4.0 ?
===

There is no separate luke 4.4.0 release, but luke 4.5.0 should open the Lucene 4.4.0 index just fine.

Licensing
===

The license for the code is [ALv2](http://www.apache.org/licenses/LICENSE-2.0.html), excluding the license of the
thinlet library that is used for the UI.

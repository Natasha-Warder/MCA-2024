                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                           
                                                                                                 # MCA Labs 2660237w
# Week 1: Basics of Music Data
##  Task 1 
Cloning the MCA Github Repository.

##  Task 2 - Identifying a theme for your dataset
+ Title: All of the lights
- Producers: Kanye West
* writers: Kanye West, Emile, Jeffrey Basker, Warren Trotter, Malik Jones
+ Performer: Kanye West
- Album: My Beautiful Dark Twisted Fantasy
* Larger Work: samples; Expo'83 - The Backyard Heavies 1971, Mary Jane (Live) - Rick James 2001, Introduction to Star Time! - James Brown 1968
+ Time Period: 2009-10
- Genre: HipHop / Rap

Click here to access [All of The Lights Original Sheet Music](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/allofthelights.pdf)

## Task 3 - Challenges 
1. Working With Music & Music-Related Data 
   - Access to Music-related data is common as digitised files require proper accreditation. Curating copyrighted music (audio files, sheet music) becomes more challenging as works may be harder to access.
   - Music data distribution can become inaccurate through secondary sources, therefore it is important to source metadata from reliable sources. 

2. Theme & Emphasised Challenges
   - Discussing sound beyond structured melodies: reverb, synth and bass.
   - deconstructing authourship and proper accreditation.
   - defining ownership and gathering concise information.
   - plotting notes accurately based on proximity and scale.
     
3. Theme & Manifestations of Data 
   - Present curation takes many forms: sheet music, vocal covers, instrumental covers and thematic analysis. The lyricism and sampling of contrasting sounds have been discussed extensively by journalists over Kanye's acceptance of the media's perception of him.
   - As there is a lot of avaiable information for this dataset, it is important to ensure data is factually correct when utilising a scope of sources.




# Week 2: Music as Notation

## Task 1 - Selecting Music Related to Theme
Selected Piece: All Of The Lights: Interlude (My Beautiful Dark Twisted Fantasy)

## Task 2 - Convert to Musescore
Original PDF 
<img title="a title" alt="Alt text" src="/images/interlude.png">

## Task 3 - Editing on MuseScore
Edited .mscz file Click here to access [.mscz File](https://github.com/Natasha-Warder/MCA-2024/blob/master/All%20Of%20The%20Lights.mscz)

## Task 4 - Evaluating transcription by the OMR engine

Dotted half notes had to be fixed as the computer mistook the shape of dots as artefacts. 
The scale of the PDF is accurate, therefore poor photo quality did not impact machine ability to identify straight lines. 
When playing the song, bar lines had to be adjusted as rests were misplaced, which created inaccuracies in rhythm. 
Elements remained fairly consistent as the piece does not specify expression or dynamics but the metronome marking 70 beats per minute remained the same. As the piece of music has been adapted as an interlude, lyrics are excluded from the piece but this could have contributed to poor transcription. 

During the group activity on tuesday, inaccuracies were found in performance methods. The piece is structured using a two staff format, whereas All of The Lights uses a bass clef for violin to accompany a treble clef and bass clef for piano. Although less instrumentation was notated, QMR engine completely removed vital information like fingerings, time signature, the composer and title. This was an unexpected outcome as accompaniment involves ensuring the cohesive nature accross different instruments. 


  
  
# Week 3: Encoding Basics for Notation

## Task 1 - Rendering MEI and MusiXML files

Click here to access [MEI File](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/All%20Of%20The%20Lights.mei)
Click here to access [MusicXML File](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/All%20Of%20The%20Lights.musicxml)



## Task 2 - Comparing MusicXML and MEI elements 

#### Note element
for MusicXML the <note> element includes attributes like pitch, duration, type, and accidental. It is designed to represent musical notes, specifying pitch and rhythmic values clearly. Whereas, for MEI The <note> element in MEI is more flexible, using attributes like pname, oct, and dur. MEI also supports richer metadata for notational details.

#### Part element
for MusicXML the part element contains a sequence of measures and is used to delineate different voices or instruments in a score. Whereas, the staff element in MEI may have multiple measures and can include additional context about the performance, instrumentation, and more.

#### Measure element
for Music XML the measure element contains attributes and note elements, clearly outlining the structure of the music, including time signatures and key signatures. Whereas for MEI, a measure is also a container for note elements and can include attributes. However, it uses a more abstract approach for structural elements, allowing for varied representations.


#### Attributes Employed in Each Standard
- Music XML Parent-Child Relationships Structure:
part → measure → note
measure can contain attributes, note, and other musical elements (like rest).
- MEI Parent-Child Relationships Structure:
staff → measure → note
measure can contain attr, note, rest, and other elements.


#### Implications of Differences 
MusicXML Implications
- Simplicity: MusicXML's straightforward structure makes it easy to parse and understand for developers and music notation software.
- Limited Flexibility: While it covers basic musical notation well, it may struggle with more complex scenarios (like extended techniques, and unconventional notations).

MEI Implications
- Richness and Complexity: MEI's flexibility allows for detailed representations, including extended techniques, performance instructions, and complex musical structures.
- Interoperability Challenges: The complexity of MEI can make it harder for some software to implement, potentially limiting its use outside academic or specialized contexts.



# Week 4: Computational Analytics of Music Notation

## Task 1 - jSymbolic Analysis
In generating a jSymbolic of my piece, this displayed Range, Mean Pitch, Last Pitch and Most Common Rhythm Value: 

Click here to access [CSV](https://gla-my.sharepoint.com/:x:/g/personal/2660237w_student_gla_ac_uk/ETfVh-M5mLZFieKaiBAY_70Bsck6uImZJC8uzZxk_JUgjg?e=UGzkkF
)

## Task 2 - Generating a piano roll and a pitch histogram
Click here to view [Jupyter Notebook](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/Intro%20to%20music21.ipynb
)

### The Piano Roll of pitches measures the pitch, length, and velocity of notes, seen below:
  <img title="Piano Roll" alt="Plotted pitches" src="/images/pianoroll.png">

  ### The Histogram, documents the distribution of a set of pitches from  the piano roll, seen below:
 <img title="Histogram" alt="Documenting most and least used pitches" src="/images/histogram1.png">




# Week 5: Standards in Curation
## Task 1 - MEI Metadata Schema
title, artist, publisher, and at least two others of your choice. 

| All of The Lights Metdata| Specifications |
| ------------- | ---------------------- | 
| Title        | All of The Lights Interlude        |
|  Artist      | Kanye West |
| Publisher      | Musescore |
| Lyricist       | Ayden Lake  |
| Date Encoded   | 22.10.2024       |

## Task 2 - Modifying MEI Metadata

Click here to access the updated [MEI File](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/All%20Of%20The%20Lights%20(5).mei) using MEI Friend.

#### The following Metadata was updated

The Title of the piece: <title>All Of The Lights Interlude </title>
                        <respStmt>
              Composer: <persNamerole="composer">Kanye West</persName>
              Lyricist: <persNamerole="lyricist">Ayden Lake</persName>
              Publisher: <persNamerole="publisher">Musescore</persName>
                         </respStmt>
                         </titleStmt>
                         <pubStmt xml:id="ps1odls*>
 Updated encoding date:  <dateisodate="2024-10-22" type="encoding-date">2024-10-22</date>
                         </pubStmt>





# Week 7: Challenges in Curation 

## Task 1 - Updating MEI Elements

## Task 2 - Revised MEI Metadata


# Week 8: Music as Sound 

## Task 1 - Audio tracks related to theme
Important technical and non-technical metadata:

| Title         | Drunk Piano            | Andante                | Our Own Melody        |
| ------------- | ---------------------- | ---------------------- | ----------------------| 
| Artist        | Shadow Priest          | Jean Toba              | Blue Dot Sessions     |
| Composer      | Content Cell           | Content Cell           | Content Cell          |
| Copyright     | Creative Commons       | Creative Commons       | Creative Commons      |
| Genre         | Electronic, Experimental, Downtempo | Jazz, soul, RnB | Minimalism, soul |
| Source        | Free Music Archive | Free Music Archive | Free Music Archive |
| File format   | VLC.wav | VLC.wav | VLC.wav |
| Channels      | Content Cell          | Content Cell           | Content Cell          |
| Sample Rate   | Content Cell          | Content Cell           | Content Cell          |
| Bits/sec      | 1411kbps          | 1411kbps           | 1411kbps           |
| Duration      | 1.57         | 5.35           | 3.06       |





## Task 2 - Analysis using SonicVisualiser
### Rendering Spectograms
#### Drunk Piano
(https://github.com/Natasha-Warder/MCA-2024/blob/master/images/drunkpiano.png)

The following images show wavforms (1st layer) and spectograms per audio track (2nd layer) with log spcace frequencies that have been extracted as CSV files. 

<img title="a title" alt="Alt text" src="/images/drunkpianocsv.png">

#### Andante
(https://github.com/Natasha-Warder/MCA-2024/blob/master/images/andante.png)

<img title="a title" alt="Alt text" src="/images/andantecsv.png">

#### Our Own Melody
(https://github.com/Natasha-Warder/MCA-2024/blob/master/images/melody.png)

Spectrograms with log-spaced frequencies 

<img title="a title" alt="Alt text" src="/images/melodycsv.png">



### CSV Files 
link to folder with csv


Time-frequency analysis has an advantage over waveform-based analysis by providing a simultaneous view of both time and frequency information. While waveform analysis typically focuses on either time or frequency domains separately, time-frequency methods reveal how a signal's frequency components evolve. This could be useful for analysing non-stationary signals, such as speech, music, or biological data, where frequency content changes over time. Time-frequency analysis is better suited for understanding dynamic and complex signals by capturing both temporal and spectral details.


# Week 9: Analysing and Extracting Audio from Data
## Extracting Data From Audio
### Task 1 - Extracting Features
The Track 'All of The Lights Interlude' was split into three sections beginning, middle and end of the interlude for this exercise. 



### Task 2 - Compute and Visualise Features with Histograms
For either the MFCC or Chroma feature, compare the histograms for the 3 tracks and highlight/discuss if the histograms capture significant differences between the tracks and if you expected this difference based on listening to the tracks (max 300 words)


# Week 10: Audio Similarity and Transcription 

# MCA Labs 2660237w
##  Week 1
###  Task 2 - Identifying a theme for your dataset
+ Title: All of the lights
- Producers: Kanye West
* writers: Kanye West, Emile, Jeffrey Basker, Warren Trotter, Malik Jones
+ Performer: Kanye West, Rihanna, Kid Cudi
- Album: My Beautiful Dark Twisted Fantasy
* Larger Work: samples; Expo'83 - The Backyard Heavies 1971, Mary Jane (Live) - Rick James 2001, Introduction to Star Time! - James Brown 1968
+ Time Period: 2009-10
- Genre: HipHop / Rap

  

### Task 3 - Challenges 

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


# Week 2

Selected Piece: All Of The Lights: Interlude (My Beautiful Dark Twisted Fantasy)

Evaluating transcription by the OMR engine: 
Dotted half notes had to be fixed as the computer mistook the shape of dots as artefacts. 
The scale of the PDF is accurate, therefore poor photo quality did not impact machine ability to identify straight lines. 
When playing the song, bar lines had to be adjusted as rests were misplaced, which created inaccuracies in rhythm. 
Elements remained fairly consistent as the piece does not specify expression or dynamics but the metronome marking 70 beats per minute remained the same. As the piece of music has been adapted as an interlude, lyrics are excluded from the piece but this could have contributed to poor transcription. 

During the group activity on tuesday, inaccuracies were found in performance methods. The piece is structured using a two staff format, whereas All of The Lights uses a bass clef for violin to accompany a treble clef and bass clef for piano. Although less instrumentation was notated, QMR engine completely removed vital information like fingerings, time signature, the composer and title. This was an unexpected outcome as accompaniment involves ensuring the cohesive nature accross different instruments. 


# Week 3

### Comparing MusicXML and MEI elements 

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
- Limited Flexibility: While it covers basic musical notation well, it may struggle with more complex scenarios (like extended techniques, unconventional notations).

MEI Implications
- Richness and Complexity: MEI's flexibility allows for detailed representations, including extended techniques, performance instructions, and complex musical structures.
- Interoperability Challenges: The complexity of MEI can make it harder for some software to implement, potentially limiting its use outside academic or specialized contexts.



# Week 4

### jSymbolic Analysis & Music21 Piano Roll and Histogram




# Week 5

### MEI Metadata Schema

# Week 7

### Updating MEI Elements




# Week 8

### Task 1 
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

#### Drunk Piano
(https://github.com/Natasha-Warder/MCA-2024/blob/master/images/andante.png)


#### Andante


#### Our Own Melody




### Task 2
Time-frequency analysis has an advantage over waveform-based analysis by providing a simultaneous view of both time and frequency information. While waveform analysis typically focuses on either time or frequency domains separately, time-frequency methods reveal how a signal's frequency components evolve. This could be useful for analysing non-stationary signals, such as speech, music, or biological data, where frequency content changes over time. Time-frequency analysis is better suited for understanding dynamic and complex signals by capturing both temporal and spectral details.


# Week 9
## Extracting Data From Audio
### Task 1 - Extracting Features
### Task 2 - Compute and Visualise Features with Histograms


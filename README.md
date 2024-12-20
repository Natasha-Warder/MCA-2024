                                                                                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                

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
<img title="a title" alt="Alt text" src="images/interlude.png">

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

Click here to access (view raw to open in MuseScore) [MEI File](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/All%20Of%20The%20Lights.mei)
Click here to access [MusicXML File](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/All%20Of%20The%20Lights.musicxml)

# All of The Lights Interlude in Verovio
<img title="a title" alt="Alt text" src="images/verovio.png">


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

1. Range: 41
2. Mean Pitch: 61.66
3. Most Common Pitch Class: 5
4. Last Pitch: 46
5. Most Common Rhythm Value: 0.25

This metadata was then used in Python to generate a piano roll and pitch histogram.

## Task 2 - Generating a piano roll and a pitch histogram
Click here to view [Jupyter Notebook](https://github.com/Natasha-Warder/MCA-2024/blob/master/tasks/Intro%20to%20music21.ipynb
)

The audio has a broad pitch range of 41 semitones, with a central focus around F (pitch class 5) and an average pitch of C#4 (61.66). The rhythm is predominantly structured around quarter notes, indicating a moderate tempo. The final pitch, A♭3, may indicate a sense of resolution or closure, with the music potentially ending in a stable tonal context.


### The Piano Roll of pitches measures the pitch, length, and velocity of notes, seen below:

  <img title="Piano Roll" alt="Plotted pitches" src="images/pianoroll.png">

### The Histogram, documents the distribution of a set of pitches from  the piano roll, seen below:

 <img title="Histogram" alt="Documenting most and least used pitches" src="images/histogram1.png">

- A histogram based on the piano roll shows the distribution of pitches, with a higher frequency around F (pitch class 5), reflecting its prominence in the audio.
- It illustrates the 41-semitone pitch range, showing the spread from the lowest to the highest pitch.
- Rhythmic values highlight quarter notes (0.25) as the most frequent rhythmic value (emphasising a steady tempo).


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


<img title="a title" alt="Alt text" src="images/meifriend.png">


# Week 7: Challenges in Curation 

## Task 1 - Updating MEI Elements

The following MEI Elements were updated:
 .<publisher>Universal Music Group</publisher>
 .<availability><useRestrict>"https://creativecommons.org/licenses/by/4.0/"</useRestrict></availability>
  .</pubStmt>https://mei-friend.mdw.ac.at/#<notesStmt>
 .<annot> Genres: Hip Hop, Classical Piano, Classical Alternative</annot></notesStmt>
   .</fileDesc>
   
The publisher Universal Music Group was included to establish ownership of audio. 
The Creative Commons license CC BY 4.0, Attribution 4.0 International emphasises the materials published can be shared and adapted when properly credited. 
The notes statement which specifies genre emphasises the piece incorporates different classical styles. 
   


## Task 2 - Revised MEI Metadata
<img title="a title" alt="Alt text" src="images/updatemeifriend.png">

To improve the appearance of metadata I have formatted it with clear indentation and correctly closed tags. To ensure the useRestrict tag is correctly placed within the availability tag and to maintain consistency, clearer naming conventions are required for better comprehension.

# Week 8: Music as Sound 

## Task 1 - Audio tracks related to theme
Three alternative classical piano audio tracks were downloaded using FMA (Free Music Archive):

Important technical and non-technical metadata:

| Title         | Drunk Piano            | Andante                | Our Own Melody        |
| ------------- | ---------------------- | ---------------------- | ----------------------| 
| Artist        | Shadow Priest          | Jean Toba              | Blue Dot Sessions     |
| Composer      | Content Cell           | Content Cell           | Content Cell          |
| Copyright     | Creative Commons       | Creative Commons       | Creative Commons      |
| Genre         | Electronic, Experimental, Downtempo | Jazz, soul, RnB | Minimalism, soul |
| Source        | Free Music Archive | Free Music Archive | Free Music Archive |
| File format   | VLC.wav | VLC.wav | VLC.wav |
| Channels      | 2          | 2       | 2    |
| Sample Rate   | 44100Hz          | 44100Hz         | 44100Hz-        |
| Bits/sec      | 1411kbps          | 1411kbps           | 1411kbps           |
| Duration      | 1.57         | 5.35           | 3.06       |





## Task 2 - Analysis using SonicVisualiser
### Rendering Spectrograms
The following images show waveforms (1st layer) and spectrograms per audio track (2nd layer) with log space frequencies that have been extracted as CSV files. 

### Drunk Piano 
<img title="a title" alt="Alt text" src="images/drunkpianoweek8.png">

### Andante
<img title="a title" alt="Alt text" src="images/andanteweek8.png">

### Our Own Melody
<img title="a title" alt="Alt text" src="images/ourownmelodyweek8.png">


Time-frequency analysis has an advantage over waveform-based analysis by providing a simultaneous view of both time and frequency information. While waveform analysis typically focuses on either time or frequency domains separately, time-frequency methods reveal how a signal's frequency components evolve. This could be useful for analysing non-stationary signals, such as speech, music, or biological data, where frequency content changes over time. Time-frequency analysis is better suited for understanding dynamic and complex signals by capturing both temporal and spectral details.


### CSV Files 
link to folder with [csv files](https://gla-my.sharepoint.com/my?id=%2Fpersonal%2F2660237w%5Fstudent%5Fgla%5Fac%5Fuk%2FDocuments%2FMA%20FILES%2FWEEK%208%20CSV&ct=1733493944870&or=OWA%2DNT%2DMail&cid=b413a9ec%2D575d%2D96a1%2Df8c7%2Daed9b6efa1e1&ga=1)



# Week 9: Analysing and Extracting Audio from Data
## Extracting Data From Audio
### Task 1 - Extracting Features
The Track 'All of The Lights Interlude' was split into three 15 second sections beginning, middle and end (presented top to bottom) of the interlude for this exercise. The images below feature a Spectrogram, a Mel Frequency Cepstral Coefficients, and a Chromagram for each segment of the interlude. 


### Beginning Segment 
Panes top to bottom are: Chromagram then Spectrogram then MFCC then the audio Waveform
<img title="a title" alt="Alt text" src="images/aotl1.png">

### Middle Segment 
Panes top to bottom are: Chromagram then Spectrogram then MFCC then the audio Waveform
<img title="a title" alt="Alt text" src="images/aotl2.png">

### End Segment 
Panes top to bottom are: MFCC then Spectrogram then Chromagram then audio Waveform
<img title="a title" alt="Alt text" src="images/aotl3.png">



### Task 2 - Compute and Visualise Features with Histograms
The sections beginning, middle and end (presented left to right) were transformed into Histograms. 

## Histograms Computed From Spectrograms
By transforming Spectrograms into Histograms this shows a more limtied distribution of frequences and their intensities over time than anticipated. 
<img title="a title" alt="Alt text" src="images/spect hist.png">

## Histograms Computed From MFCCs
The ability to view the distribution of energy across different frequency bands emphasises how sound is being heard.
<img title="a title" alt="Alt text" src="images/mel hist.png">

## Histograms Computed From Chromagrams
The distribution of pitch classes: C,D,E etc., highlights the occurence of different pitches and chords helping to visualise harmonic content. 
<img title="a title" alt="Alt text" src="images/chrom hist.png">

## Comparison of Histograms
Histograms highlight the interlude is a cohesive piece which remains fairly similar from start to finish as it functions as a bridge. This similarity was expected due to the function of the audio being transitional within a larger piece of music (All of The Lights). 

# Week 10: Audio Similarity and Transcription 
### Task 1 - Similarity, generating a similarity matrix 

Using the Python Notebook a similarity matrix (left) of the beginning, middle and end of the interlude. All tracks were identified as classical pieces and the symmetry of darker cool tones in the similarity matrix emphasises the consistency of violin and piano across the piece. 

<img title="a title" alt="Alt text" src="images/week 10 task 1.png">


### Task 2 - Transcription
For this task I transcribed the week two All Of The Lights Interlude file (left) intially generated using MuseScore. By exporting this file to a WAV file and transcribing it in SonicVisualiser a new MIDI file (right) was generated of the original piece. The Transcription is extremely inaccurate by include a multitude of slurs and legato lines this would greatly impact the fluidity of the piece in performance and make notes less distinct, also 3 by 4 beats are introduced changing the timing of the piece, placement of notes are wrong and rests are inserted in random places. 

<img title="a title" alt="Alt text" src="images/week 10 task 2.png">

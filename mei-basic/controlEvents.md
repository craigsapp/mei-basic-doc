---
title: Slurs, Dynamics and other "Control Events"
verovio: true
author: Johannes Kepper
creation_date: 9 May 2017
last_updated: 6 Oct 2017
tags: [all, events]
keywords: introduction
summary: 
github:    mei-basic/controlEvents.md
permalink: /controlEvents.html
---

{% include page-title.html %}

With <span class="soCalled">events</span>, MEI encodes the individual notes etc. that compose a score. However, music notation has various "features" that tell us something about those notes, that control how we need to understand them. Those features are called <span class="soCalled">control events</span> in MEI.

#### Slurs and Ties

<div part="N" org="uniform" sample="complete">


One of the most prominent and frequently used control events in 18th and 19th century music are slurs. They are encoded as follows:

<div class="meiSample">

<div class="btn-group"><button class="btn btn-sm active" id="s16d434ee-c73f-47d6-8afc-9a25c35c4133_excerpt_link" onclick="showCode('excerpt','s16d434ee-c73f-47d6-8afc-9a25c35c4133')">Relevant Excerpt</button> <button class="btn btn-sm" id="s16d434ee-c73f-47d6-8afc-9a25c35c4133_full_link" onclick="showCode('full','s16d434ee-c73f-47d6-8afc-9a25c35c4133')">Full Encoding</button></div>

<div class="excerpt" id="s16d434ee-c73f-47d6-8afc-9a25c35c4133_excerpt_container">

<div class="excerptEditor" id="s16d434ee-c73f-47d6-8afc-9a25c35c4133_excerpt">

<div xml:space="preserve" class="pre">

<div class="indent1"><span data-indentation="1" class="element"><slur <span class="attribute">staff=</span><span class="attributevalue">"1"</span> <span class="attribute">startid=</span><span class="attributevalue">"#note1"</span> <span class="attribute">endid=</span><span class="attributevalue">"#note2"</span>/></span></div>

</div>

</div>

</div>




<script>loadMEI('s16d434ee-c73f-47d6-8afc-9a25c35c4133','basic_slur1.mei');</script></div>

This example introduces quite a number of important concepts. Let's have a close look: The <span class="att" scheme="TEI">staff</span> attribute attaches the slur to a specific staff in the score. The assignment to specific notes is dones through the <span class="att" scheme="TEI">startid</span> and <span class="att" scheme="TEI">endid</span> attributes. Both attributes use a specific datatype called <span class="soCalled">anyURI</span>, so it's basically a URI as you use your internet browser to point to a specific webpage. What we see over here is a <span class="soCalled">fragment identifier</span>, as we can see from the trailing hash symbol (#). The text following this hash refers to an <span class="soCalled">xml:id</span> of an element in the same file. This means we have to look at the encoding of the notes of our example:

<div class="meiSample">

<div class="btn-group"><button class="btn btn-sm active" id="s4612b9d5-0033-4c29-a1ac-3a1d9685364b_excerpt_link" onclick="showCode('excerpt','s4612b9d5-0033-4c29-a1ac-3a1d9685364b')">Relevant Excerpt</button> <button class="btn btn-sm" id="s4612b9d5-0033-4c29-a1ac-3a1d9685364b_full_link" onclick="showCode('full','s4612b9d5-0033-4c29-a1ac-3a1d9685364b')">Full Encoding</button></div>

<div class="excerpt" id="s4612b9d5-0033-4c29-a1ac-3a1d9685364b_excerpt_container">

<div class="excerptEditor" id="s4612b9d5-0033-4c29-a1ac-3a1d9685364b_excerpt">

<div xml:space="preserve" class="pre">

<div class="indent1"><span data-indentation="1" class="element"><note <span class="attribute">xml:id=</span><span class="attributevalue">"note1"</span> <span class="attribute">pname=</span><span class="attributevalue">"c"</span> <span class="attribute">oct=</span><span class="attributevalue">"4"</span> <span class="attribute">dur=</span><span class="attributevalue">"2"</span> <span class="attribute">dots=</span><span class="attributevalue">"1"</span>/></span></div>

<div class="indent1"><span data-indentation="1" class="element"><note <span class="attribute">xml:id=</span><span class="attributevalue">"note2"</span> <span class="attribute">pname=</span><span class="attributevalue">"g"</span> <span class="attribute">oct=</span><span class="attributevalue">"4"</span> <span class="attribute">dur=</span><span class="attributevalue">"4"</span>/></span></div>

</div>

</div>

</div>




<script>loadMEI('s4612b9d5-0033-4c29-a1ac-3a1d9685364b','basic_slur1.mei');</script></div>

As we can see there, our notes have an additional attribute <span class="att" scheme="TEI">xml:id</span>. This attribute is actually allowed on every element in MEI. The value must conform to the rules of XML IDs, which basically allows most common ASCII characters, but requires to start with a letter. However, the most important thing about XML IDs is that they need to be unique within a file, that is, there must not be any other element with the same value for <span class="att" scheme="TEI">xml:id</span> in the file. Only by this limitation, XML IDs can serve their purpose, that is, inambiguously identify elements within a file. As a side note, even though we used "note1" and "note2" as XML IDs for this example, we don't actually recommend to use so-called <span class="soCalled">predictable IDs</span>, that is, XML IDs which can be guessed by their position in the file. As soon as you start to apply modifications to your file, it's quite likely that this will require you to change your IDs, and that this endeavor will lead to inconsistency and problems – believe us, we've been through this.

Now that we understand the mechanism of <span class="att" scheme="TEI">xml:id</span> and <span class="soCalled">anyURI</span>, what does it mean? It attaches the two ends of the slur firmly to the notes referenced (just for the record: chords can be equally well referenced). This means that when you change your encoding by adding or deleting notes, moving things around etc., the slur will stay attached to that note, no matter what.

Sometimes, however, you don't want to attach a <span class="soCalled">control event</span> like a slur to a specific note.

</div>

#### Dynamics of all kinds

#### Other controlEvents

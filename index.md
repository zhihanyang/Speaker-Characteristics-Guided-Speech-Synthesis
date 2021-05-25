**Abstract:**
Nowadays, talking head techniques are widely researched. Most of the previous works pay attention to the association between tones, prosody, and visual cues, such as head motion, lip movement, and gestures. However, it is also important to concern with the timbre, matching the voice with the speaker identity, since people obtain speaker-specific information from both the auditory and visual modalities.
Thus in this paper, we aim to generate proper voice characteristics in accordance with the speaker characteristics we set up.
To address the problem, we first select 6 speaker characteristics related to the voice qualities: gender, age, race, body mass index, face shape, and personality. We then train a Conditional Variational AutoEncoder with attention (attentionCVAE) model to inference speaker embeddings from speaker characteristics and employ a multi-speaker text-to-speech system to generate speeches of nonexistent speakers we set.
The subjective tests indicate that our method can reconstruct real-world speaker embedding, and generate meaningful fake embeddings from speaker characteristics. The further analysis uncovers how and to what extent the speaker characteristics influence the voice qualities of speakers.

## Comparison with Baselines(Section 5.5)
These samples as corresponding to Section 5.5 in our paper. **LibriTTS** is the original TTS training dataset; **Voxceleb2** is unseen during TTS training and we train the next two models on this dataset; we train **MAF** and **attentionCVAE** to generate embedding from fake characteristic labels. We randomly select 4 samples for each respectively.

### LibriTTS
<audio controls>
  <source src="./audio/baselines/2532_157475.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/5126_34483.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/7777_106366.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/8677_246948.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

### VoxCeleb2
<audio controls>
  <source src="./audio/baselines/id00053.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/id03784.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/id05354.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/id07232.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

### MAF
<audio controls>
  <source src="./audio/baselines/maf_sample1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/maf_sample2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/maf_sample3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/maf_sample4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

### attentionCVAE(ours)
<audio controls>
  <source src="./audio/baselines/cvae_sample1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/cvae_sample2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/cvae_sample3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/cvae_sample4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

## Face Matching Test(Section 5.7)
We randomly select 3 seen speakers and 3 unseen speakers during training from VoxCeleb2 respectively. We respectively generate speech from their speaker embedding extracted from their audio and the embedding predicted from our model, and compare to what extent these speech match the speaker's face.

### seen speakers
id05663

![Branching](./image/5663.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id05663.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id05663_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

id07017

![Branching](./image/07017.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id07017.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id07017_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

id07254

![Branching](./image/07254.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id07254.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id07254_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>


### unseen speakers
id00425

![Branching](./image/00425.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id00425.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id00425_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

id00467

![Branching](./image/00467.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id00467.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id00467_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>


id01590

![Branching](./image/01590.jpg)

ground truth:
<audio controls>
  <source src="./audio/faceMatch/id01590.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
ours:
<audio controls>
  <source src="./audio/faceMatch/id01590_fake.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

### Characteristic Matching Test(Section 5.7)
We select 3 attributes: **gender, age, and BMI** to evaluate the influence of speaker characteristics tovoice qualities. We choose two opposite characteristics of one attributes to generate speech from.

#### gender
male:

<audio controls>
  <source src="./audio/attrMatch_s/male1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/male2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

female:

<audio controls>
  <source src="./audio/attrMatch_s/female1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/female2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

#### age
young:

<audio controls>
  <source src="./audio/attrMatch_s/young1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/young2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

elderly:

<audio controls>
  <source src="./audio/attrMatch_s/old1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/old2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

#### BMI
underweight:

<audio controls>
  <source src="./audio/attrMatch_s/slim1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/slim2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

overweight:

<audio controls>
  <source src="./audio/attrMatch_s/fat1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./audio/attrMatch_s/fat2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>


### Relationship between Characteristic and Voice(Section 5.8)
We give some examples to illustrate how voice change as the characteristic change.

#### BMI

![Branching](./image/middleweight_m.png width=60%)

<audio controls>
  <source src="./audio/attrMatch/m_middleage.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

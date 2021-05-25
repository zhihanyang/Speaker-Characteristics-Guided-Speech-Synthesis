**Abstract:**
Nowadays, talking head techniques are widely researched. Most of the previous works pay attention to the association between tones, prosody, and visual cues, such as head motion, lip movement, and gestures. However, it is also important to concern with the timbre, matching the voice with the speaker identity, since people obtain speaker-specific information from both the auditory and visual modalities.
Thus in this paper, we aim to generate proper voice characteristics in accordance with the speaker characteristics we set up.
To address the problem, we first select 6 speaker characteristics related to the voice qualities: gender, age, race, body mass index, face shape, and personality. We then train a Conditional Variational AutoEncoder with attention (attentionCVAE) model to inference speaker embeddings from speaker characteristics and employ a multi-speaker text-to-speech system to generate speeches of nonexistent speakers we set.
The subjective tests indicate that our method can reconstruct real-world speaker embedding, and generate meaningful fake embeddings from speaker characteristics. The further analysis uncovers how and to what extent the speaker characteristics influence the voice qualities of speakers.

# Comparison with Baselines(Section 5.5)

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

### LibriTTS
<audio controls>
  <source src="./audio/baselines/5126_34483.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/5126_34483.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./audio/baselines/5126_34483.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.
<audio controls>
  <source src="./assets/images/f_<30_<25.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>
<audio controls>
  <source src="./assets/images/f_<30_<25.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="./assets/images/f_<30_<25.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```

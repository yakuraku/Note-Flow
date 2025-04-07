# Note Flow: AI-Powered Music Composition with LSTM


![Music Generation](https://img.shields.io/badge/Type-Music_Generation-blue) ![PyTorch](https://img.shields.io/badge/Framework-PyTorch-orange) ![LSTM](https://img.shields.io/badge/Architecture-LSTM-green) ![ABC_Notation](https://img.shields.io/badge/Format-ABC_Notation-yellow)

An end-to-end system for generating musical compositions in ABC notation using deep learning.

## Features

- 🎵 **LSTM-based architecture** trained on Irish folk music dataset
- 🎼 **ABC notation processing** with text-to-music conversion
- 🔊 **Real-time audio playback** of generated compositions
- ⚙️ **Customizable generation** parameters (temperature, sequence length)
- 🚀 **HuggingFace-ready** model for easy deployment

## Quick Start

### Installation

```bash
git clone https://github.com/yakuraku/note-flow.git
```

### Basic Usage

```python
from note_flow import generate_music, play_song

# Generate a musical composition
composition = generate_music(
    start_string="X:1\nT:Generated\nM:4/4\nK:D\n",
    temperature=0.7,
    length=500
)

# Play the generated music
play_song(composition)
```

### Generation Parameters

| Parameter      | Description                          | Recommended Value |
|---------------|--------------------------------------|------------------|
| `temperature` | Controls randomness (lower = more conservative) | 0.5-1.2 |
| `length`      | Number of characters to generate     | 300-1000         |
| `start_string`| Initial musical seed                 | ABC header format|

## Dataset

The model is trained on the [Irish Folk Music ABC Notation Dataset](https://huggingface.co/datasets/sander-wood/irishman) from HuggingFace, containing traditional Irish tunes in ABC format.

## Examples

Sample generated output:
```abc
X:1
T:Generated
M:4/4
L:1/8
K:D
(DEF) \| (F2G) (B>A) (B2A) | (c2A) (A2 (F>A) (E>D) C2 | (CD).D EDC c2 (.d2) .F2(DF) | (DFA) (B2d) \| (A2F2) (AG) F2A | (G2E) (DF).F | (cd).d (ed/c/B/) | A2 A2 (AB) | (AG).G (TA2 F2) | G4 G2 || (A2 G2) (AB) | F4 (D (ED) | G2 E | D2 D2 (D2 D2 | .E2) (TE2) | (TE>D) | (D2 G) | F (F>D) {A}(G (GF) z (D/E/2F/4) (G/4E/4F/4G/4A3/2) | G4 ((3EFE) | D4 z2 (A/2B/2) (AB/2c/2) | d4 ((3BAG) A3 (B>c) | (.c.B.B) (AA) | G2 (g>B)(cB) (TA2 | F2 D2 D2 (G>A) | (B>A) (B>c) |  .D(AG) F>G (TA2 | G4 G2) | (A2B) (d2 (gb)
```

## Inspiration

Note Flow builds upon the foundational concepts from [MIT's Introduction to Deep Learning Lab](http://introtodeeplearning.com/) music generation project. While retaining the core LSTM architecture for sequence modeling, this implementation introduces several key enhancements to better suit my needs.


## License

This project is licensed under the [MIT License](LICENSE).

## Credits

**Created and maintained by** [Yashwanth Kumar Kurakula](https://github.com/yakuraku).  
**Contact:** yashwanth.415@gmail.com | [Linkedin](https://www.linkedin.com/in/yashwanth-kumar-kurakula/)  


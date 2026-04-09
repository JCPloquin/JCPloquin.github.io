---
title: "Sonification: From Image to Sound - Experience Report on Manual and Automated Approaches"
date: 2025-08-04T10:00:00+02:00
author: "Jean-Christophe Ploquin"
draft: false
excerpt: "Sonification, this fascinating technique that transforms visual data into sonic experiences, plays a central role in my transmedia projects. Having had the opportunity to experiment with this approach through **Fluctus Planetarium** and its interactive adaptation **Fluctus Planetarium: The Game**, I wish to share my experience with two complementary methodologies: manual sonification with ARGOPd/PureData for the original work and custom automation with Godot Engine for the interactive adaptation."
tags: ["sonification", "electroacoustic", "ARGOPd", "Godot", "Pure Data", "transmedia"]
categories: ["Sound Creation", "Technology"]
description: "Experience report on two sonification approaches: manual vectorization with ARGOPd for Fluctus Planetarium and algorithmic automation with Godot Engine for the interactive adaptation."
---

# Sonification: From Image to Sound - Experience Report on Manual and Automated Approaches

Sonification, this fascinating technique that transforms visual data into sonic experiences, plays a central role in my transmedia projects. Having had the opportunity to experiment with this approach through **Fluctus Planetarium** and its interactive adaptation **Fluctus Planetarium: The Game**, I wish to share my experience with two complementary methodologies: manual sonification with ARGOPd/PureData for the original work and custom automation with Godot Engine for the interactive adaptation.

## Sonification in My Creative Projects

As an electroacoustic composer, I have always been intrigued by the bridges between visual arts and sound creation. Sonification offers the unique possibility to make heard what is seen, to reveal the hidden musicality of shapes and colors. It was this curiosity that led me to integrate these techniques into **Fluctus Planetarium**, then to completely rethink the approach during its adaptation to an interactive game.

## Manual Approach: Fluctus Planetarium and ARGOPd

### Original Creative Context

For **Fluctus Planetarium**, my acousmatic project, I needed to translate the **planetary textures created by Louis Jeanne** into sound material. These visual works, resulting from the deconstruction of portraits into abstract and organic textures, constitute the base material for my sonic creation.

### Manual Vectorization Process for ARGOPd

The particularity of the **ARGOPd Theme8 sonification module** (developed by Gérard Paresys) that I used is that it requires **vector graphic scores** specifically formatted to function. The "Score/Graphic Score" module uses Pure Data's "data structures" and requires meticulous preparation of the visual material.

I therefore developed a **manual vectorization** process of Louis Jeanne's textures:
1. **Analysis** of the organic textures of the planets
2. **Extraction** of significant graphic elements  
3. **Manual vectorization** into geometric shapes compatible with Pd data structures
4. **Creation** of graphic scores exploitable by the Theme8 module

<div style="display: flex; gap: 20px; margin: 20px 0;">
  <div style="flex: 1;">
    <img src="/img/matis_texture.png" alt="Organic texture by Louis Jeanne" style="width: 100%; height: auto;" />
    <p style="text-align: center; font-style: italic; margin-top: 10px;">Organic texture by Louis Jeanne</p>
  </div>
  <div style="flex: 1;">
    <img src="/img/matis_partition.png" alt="Vectorized score for ARGOPd" style="width: 100%; height: auto;" />
    <p style="text-align: center; font-style: italic; margin-top: 10px;">Vectorized score for ARGOPd</p>
  </div>
</div>

*Visual comparison: The original organic texture by Louis Jeanne (gray and blue organic tones) and its manual vectorization into a colorful graphic score (bright geometric shapes) - same structural framework, different vectorial interpretation*

This vectorization step is **crucial**: it transforms the fluid and organic textures into discrete geometric elements that the ARGOPd module can interpret as sound instructions.

### ARGOPd Theme8: An Exceptional Tool for Interpretation

Once the vectorized scores are created according to Theme8 specifications, **ARGOPd** reveals all its power. This suite of over 200 modules and 300 patches for PureData, co-winner of the 2014 AFIM International Musical Software Competition, offers particularly sophisticated **sonification patches**.

The Theme8 "Score/Graphic Score" module uses Pure Data's "data structures" and allows:
- **Sequential reading** of the vectorized elements of the score
- **Transformation** of each geometric shape into sound parameters
- **Artistic control** of playback speed and rendering quality
- **Generation** of real-time audio streams from visual data

Using vectorized scores in ARGOPd Theme8 allowed me to:
- **Artistically control** every aspect of the visual-to-sound transposition
- **Musically interpret** Louis Jeanne's textures
- **Compose** customized processing chains
- **Create** an authentic dialogue between visual arts and electroacoustic composition

### Results of Manual Sonification

The graphic scores I created reveal the **creative mediation** necessary between the original visual art and its sonification. The colorful geometric shapes - triangles, rectangles and polygons - combine with audio signal representations in the ARGOPd interface, creating a true **contemporary score** where each color and shape corresponds to specific sound parameters.

This manual approach offers exceptional **creative flexibility**. Each parameter can be adjusted intuitively, allowing exploration of different sonic interpretations of the original textures until the desired artistic result is achieved.

## Automated Approach: Fluctus Planetarium: The Game and Godot Engine

### Interactive Adaptation Challenge

When adapting **Fluctus Planetarium** into the interactive version **Fluctus Planetarium: The Game**, the constraints were entirely different: I had to automate sonification to allow players to progressively discover musical creation. The goal was to develop an algorithm capable of automatically generating interesting sonic material from any image, without going through the manual vectorization step.

This transition from acousmatic work to interactive experience forced me to **completely rethink** the sonification approach, moving from manual artistic interpretation to direct pedagogical automation.

### Custom Algorithmic Innovation

I developed an original sonification system that directly analyzes pixels without prior vectorization:

#### RGB to Harmonics Mapping
```gdscript
var r_freq = lerp(110.0, 440.0, color.r)    # Red: 110-440 Hz
var g_freq = lerp(880.0, 2200.0, color.g)   # Green: 880-2200 Hz  
var b_freq = lerp(4400.0, 8800.0, color.b)  # Blue: 4400-8800 Hz
```

#### Progressive Revelation in 5 Temporal Phases
The algorithm progressively reveals sonic complexity over 10 seconds:
- **0-2s**: Red only
- **2-4s**: Blue only  
- **4-6s**: Green only
- **6-8s**: Red + Blue
- **8-10s**: Complete RGB

This pedagogical approach allows players to progressively understand how each color component contributes to the final sonic result, creating a **bridge** between the original work and its appropriation by users.

#### Professional Audio Quality
- **Bilinear interpolation** for smooth image traversal
- **Temporal smoothing** (factor 0.95) to reduce granularity
- **Normalization to -1dB** for optimal audio level
- **Anti-click envelopes** with fade in/out of 2000 samples

### Real-Time Effects Chain

The algorithm generates a **AudioStreamWAV** 44.1kHz 16-bit which is then processed by a complete effects chain:
- **6-band Equalizer** (Bass/Medium/Treble)
- **Pitch Shift**, **Reverb**, **Delay**, **Chorus**, **Distortion**
- **Real-time spectrum analyzer** with 16-band VU meters
- **Integrated oscilloscope** with 512-sample buffer
- **User-editable volume curve**

This architecture transforms the sound workshop into a true **virtual studio** accessible to non-musician players, democratizing access to techniques used in the original work.

## Comparison of Both Approaches

| **Aspect** | **ARGOPd Theme8 (Manual)** | **Godot (Automated)** |
|------------|----------------------------|------------------------|
| **Preparation** | Mandatory manual vectorization | Direct pixel analysis |
| **Interface** | Pure Data data structures | Structured GDScript code |
| **Control** | Artistic interpretation | Reproducible algorithm |
| **Real-time** | Yes, via PureData | Yes, with spectral analysis |
| **Source format** | Specific vector scores | Any raster images |
| **Target audience** | Electroacoustic composers | General public via gaming |
| **Creativity** | Subjective interpretation | Objective logic |

## Work Evolution: From Creation to Adaptation

This experience showed me how a **single work** can require radically different technical approaches depending on its dissemination context:

### Original Work (Fluctus Planetarium)
- **Creative interpretation** of Louis Jeanne's textures via vectorization for ARGOPd Theme8
- **Total artistic control** by the composer with Pure Data data structures
- **Sonification** as collaborative creative process and creative mediation

### Interactive Adaptation (Fluctus Planetarium: The Game)
- **Automated algorithm** for universal accessibility without preparation
- **Progressive pedagogy** of direct pixel-by-pixel sonification
- **Democratization** without prior creative mediation or technical skills

## Complementary Methods

These two approaches reveal the richness of the sonification process:

### Manual approach (ARGOPd Theme8) favors:
- **Creative interpretation** of visual material via vectorization
- **Artistic collaboration** between visual and sonic creators
- **In-depth aesthetic research** with meticulous preparation
- **Dialogue** between visual arts and electroacoustic composition

### Automated approach (Godot) promotes:
- **Universal accessibility** to techniques without preparation
- **Reproducibility** of results with any image
- **Progressive learning** through direct experience
- **Personal appropriation** of concepts without technical barriers

## Future Prospects

This adaptation experience opens fascinating perspectives for the future of electroacoustic works. One can imagine **transmedia ecosystems** where:
- **Manual interpretation** (ARGOPd) maintains its collaborative artistic dimension
- **Automated algorithms** (Godot) broaden the audience without mediation
- **Artificial intelligence** assists the transition between creative approaches
- The **community** explores and extends the work via diversified tools

## Conclusion

**Fluctus Planetarium** and its adaptation perfectly illustrate the richness of sonification approaches. From manual vectorization of Louis Jeanne's textures for the ARGOPd Theme8 module to the direct algorithm on Godot, each method reveals different aspects of the creative process.

My experience with this dual approach has convinced me that the future of sonification lies in complementarity: manual creative interpretation for aesthetic research with specialized tools like ARGOPd, intelligent automation for transmission and appropriation via custom solutions.

Sonification thus becomes a **mediation language** with multiple facets, capable of revealing the hidden musicality of our visual environment according to different levels of reading and interaction, from in-depth artistic collaboration requiring creative vectorization to accessible playful experience with direct pixel analysis.

*This article explores sonification techniques in the context of Fluctus Planetarium transmedia projects. To learn more about my other research in electroacoustic sound creation, check out [my other articles](/posts/).*

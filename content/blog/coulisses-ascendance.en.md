---
title: "Behind the Scenes: Creating Ascendance"
date: 2025-07-05T15:00:00+02:00
slug: "behind-the-scenes-creation-dascendance"
draft: false
categories: ["Music", "Development", "Creation"]
tags: ["ascendance", "behind the scenes", "composition", "development", "genealogy"]
description: "Dive into the behind-the-scenes of Ascendance's creation: from initial idea to technical challenges, discover the creative process behind this interactive acousmatic work."
---

Three weeks after the launch of *Ascendance*, it's time to lift the veil on the behind-the-scenes of this creation. How do you transform an artistic idea into an interactive work? A look back at a creative process that blends electroacoustic composition and software development.

## The Creative Spark: When Genealogy Meets Acousmatic Music

The idea for *Ascendance* was born from a simple observation: **our family trees resemble musical scores**. Each branch evokes a melodic line, each generation suggests a tessitura, each ancestor carries within them a unique sonic story.

This revelation came to me while exploring my own family archives. Contemplating the birth and death dates of my ancestors, I could already hear the bells, choirs, and trumpets that would become the fundamental sound objects of the work.

## The Technical Challenge: Making GEDCOM and Audio Dialogue

**First major obstacle:** how to make a GEDCOM file "speak"? These genealogy files contain a wealth of information, but in a purely textual format. I needed to create a **parser** capable of extracting relevant data and transforming it into musical parameters.

## What is a Parser?

A **parser** is a computer program that analyzes a character string and breaks it down into elements understandable by the machine. Etymologically, the term comes from the Latin "pars" (part): the parser identifies the different parts of a text according to precise rules.

In the context of *Ascendance*, my GEDCOM parser must:
- **Identify** each individual in the family tree
- **Extract** their birth and death dates
- **Understand** family relationships
- **Convert** this information into spatial and temporal coordinates for composition

## The Parallel with Xenakis and Stochastic Music

This approach recalls the revolutionary work of Iannis Xenakis in the 1950s. The Greek composer used **stochastic mathematics** - based on probability calculations - to transform abstract data into concrete musical material.

**Xenakis transformed:**
- **Laws of physics** (gas kinetics, Markov chains) into **compositional rules**
- **Natural phenomena** (cicada songs, crowd demonstrations) into **sound masses**
- **Probabilistic equations** into **musical events**

**In Ascendance, I transform:**
- **Genealogical data** into **spatialized sound objects**
- **Family links** into **harmonic relationships**
- **Historical dates** into **temporal progressions**

Like Xenakis who "parsed" natural phenomena to extract compositional laws, my GEDCOM parser extracts the musical structure hidden in our family histories.

## The Sound Architecture: Three Universes, Three Aesthetics

*Ascendance* is structured in three distinct movements, each requiring a specific compositional approach:

## The Warm-up: Journey Through Musical History

**Artistic challenge:** How to represent the passage of historical time through music? I chose to superimpose samples from different eras - Pierre Henry, Léo Delibes, Gregorian chant, ancient music - in random order. This controlled cacophony prepares the listener for the temporal journey ahead.

## The Outward Journey: Each Ancestor, a Sound Signature

**Technical innovation:** Each ancestor automatically generates three symbolic sound objects. Birth dates trigger trumpets, life periods activate choirs, death dates resonate bells. Quadraphonic spatialization allows perception of only "nearby" ancestors in the tree.

## The Return Journey: The Temporal Avalanche

**Radical aesthetic choice:** Abandoning individual melody for a descending global texture. This "chromatic avalanche" symbolizes the cascade of generations, creating a striking dramatic effect.

## The Challenges of Interactive Spatialization

**Complex problem:** How to navigate a sound space too vast to be grasped globally? The solution lay in creating a "sonic horizon" - only ancestors within a 4-generation radius remain audible.

This technical limitation becomes an artistic choice: it mimics our natural perception of family history, where only "close" ancestors are truly accessible to us.

## Harmonic Evolution: The Comma as Temporal Guide

**Compositional discovery:** Rather than progression by semitones (too brutal), I opted for ascending by commas (ninth of a tone). This micro-interval creates a subtle harmonic progression that accompanies genealogical exploration without dominating it.

Each generation ascended slightly raises the overall pitch, creating a sensation of spiritual elevation toward origins.

## Creation Tools: Between Tradition and Innovation

**Software palette:**
- **Ardour**: Main sequencer for assembly and multichannel mixing
- **Pure Data**: Programming musical algorithms and real-time processing
- **Godot Engine**: Game engine for interactivity and interface
- **Custom audio libraries**: Sound objects composed specifically for the project
- **GEDCOM parsing scripts**: Developed custom for genealogical analysis

**Pure Data** plays a central role in my creations. This visual programming language allows me to develop the complex musical algorithms that transform genealogical data into sound objects. Each ancestor, each date, each family link passes through Pure Data patches that calculate spatialization, pitch, and timbre parameters in real time.

## User Experience: When Art Meets Its Audience

Since launch, feedback reveals unexpected uses. Some users explore *Ascendance* as a family meditation tool, others find a new way to understand their heritage. This diversity of approaches confirms the richness of the interactive medium.

**Notable testimonials:**
- "I finally 'heard' my great-grandfather"
- "An overwhelming experience that gives a sonic dimension to my genealogy"
- "More than a game, it's an inner journey"

## Toward New Creative Horizons

*Ascendance* opens the way to other experiments. The idea of adapting this approach to other types of data - geographical, historical, scientific - is already germinating. The principle remains the same: transform information into immersive artistic experience.

## Lessons Learned

**Artistically:** Interactivity must never dominate the aesthetic dimension. Every technical choice must serve the musical intention.

**Technically:** Simplicity of use often hides development complexity. Three clicks to load a GEDCOM represent hundreds of hours of programming.

**Humanly:** Interactive art creates unique links between creator and audience. Each user becomes co-creator of their own experience.

*Ascendance* demonstrates that it's possible to rethink the boundaries between composition, programming, and user experience. This hybrid work opens new perspectives for 21st-century sound art, following in the footsteps of Xenakis's innovations that already transformed mathematics into music.

---

*Discover Ascendance for free on [jcploquin.itch.io/ascendance](https://jcploquin.itch.io/ascendance) and explore your own musical genealogical journey.*


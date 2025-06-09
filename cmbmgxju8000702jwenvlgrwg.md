---
title: "[AI #3] John McCarthy's "Programs with Common Sense": The 1959 Paper That Predicted Modern AI"
seoTitle: "John McCarthy's Vision: AI's Future Foretold"
seoDescription: "Discover how John McCarthy's 1959 paper predicted today's AI advancements in common sense reasoning and declarative programming"
datePublished: Sat Jun 07 2025 16:48:30 GMT+0000 (Coordinated Universal Time)
cuid: cmbmgxju8000702jwenvlgrwg
slug: ai-3-john-mccarthys-programs-with-common-sense-the-1959-paper-that-predicted-modern-ai
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/eGGFZ5X2LnA/upload/5855bd72f877057fa34a4dfcbc41d4d9.jpeg
tags: ai, artificial-intelligence, paper-review

---

*How the father of AI envisioned machines with common sense reasoning 65 years ago*

---

## Abstract

This comprehensive review analyzes John McCarthy's groundbreaking 1959 paper ["Programs with Common Sense"](http://jmc.stanford.edu/articles/mcc59/mcc59.pdf), examining the revolutionary Advice Taker system, declarative programming concepts, and common sense reasoning that laid the foundation for modern artificial intelligence. We explore how McCarthy's 65-year-old vision has materialized in today's AI systems and identify the prescient ideas that continue to shape AI development.

**Keywords:** Artificial Intelligence, John McCarthy, Advice Taker, Common Sense Reasoning, Declarative Programming, AI History

---

## Introduction: The Visionary's Dream

In 1959, when computers were glorified calculators filling entire rooms, one man dared to imagine machines that could think like humans. That man was John McCarthy, and his paper "Programs with Common Sense" became the blueprint for artificial intelligence as we know it today.

McCarthy's central insight was revolutionary for its time: while computers excelled at chess and mathematical calculations, they completely failed at basic common sense reasoning like "if it's raining, take an umbrella." This seemingly simple observation would spark a 65-year journey toward creating truly intelligent machines.

The paper introduced the **Advice Taker**, a theoretical system that could accept advice in natural language and use logical reasoning to solve problems—a concept that sounds remarkably similar to modern large language models like GPT-4 and Claude.

---

## The 1959 Problem : Computers Without Common Sense

### The Paradox of Intelligent Machines

McCarthy identified a fundamental paradox in early computing: machines that could solve complex mathematical proofs were completely stumped by everyday reasoning that any child could handle.

**What computers could do in 1959:**

* Play chess at expert levels
    
* Solve complex mathematical equations
    
* Perform geometric proofs
    
* Process large datasets
    

**What computers couldn't do:**

* Understand that "hungry" implies "need food"
    
* Reason that "rain" suggests "bring umbrella"
    
* Plan a route from home to airport
    
* Make common sense inferences
    

### McCarthy's Core Insight: HOW vs. WHAT

The revolutionary idea was shifting from **imperative programming** (telling computers *how* to do something step-by-step) to **declarative programming** (telling computers *what* you want and letting them figure out how).

**Traditional Imperative Approach:**

```bash
Step 1: Stand up from chair
Step 2: Walk to door
Step 3: Turn door handle
Step 4: Open door
```

**McCarthy's Declarative Vision:**

```bash
Facts:
- "The door is available"
- "You are in the room"
- "You want to go outside"

Computer reasoning: "I can go through the door to get outside"
```

This shift represented a fundamental change in how we think about programming and artificial intelligence.

---

## The Advice Taker: Revolutionary System Design {#advice-taker}

### System Architecture

The Advice Taker was designed as an intelligent system that could:

1. Accept advice and facts in natural language
    
2. Store knowledge in a logical framework
    
3. Perform reasoning to reach conclusions
    
4. Plan and execute actions
    
5. Learn from experience
    

### Six Core Components

#### 1\. Expression System

A flexible representation method for storing information, similar to modern knowledge graphs:

```python
at(me, desk)     % I am at the desk
at(desk, home)   % The desk is at home
```

#### 2\. Logic System

Rule-based reasoning using if-then relationships:

```python
if raining(X) then take(umbrella)
if at(X,Y) and at(Y,Z) then at(X,Z)  % Transitivity rule
```

#### 3\. Immediate Deduction Engine

Real-time inference as new information becomes available—similar to how modern AI systems process context.

#### 4\. Object-Property System

Structured representation of entities and their attributes:

```bash
Car: [color=red, size=medium, location=home]
Phone: [color=blue, size=small, location=pocket]
```

#### 5\. Individuals, Functions, and Programs

The system could represent not just facts but also functions and executable programs as logical formulas.

#### 6\. Cyclic Processing

Continuous loop of reasoning → action → new information → reasoning, mirroring modern reinforcement learning cycles.

---

## Airport Example: Reasoning in Action {#airport-example}

Let's examine how the Advice Taker would solve a practical problem: getting from home to the airport.

### Initial Setup

**Given Facts:**

```python
at(I, desk)           % I am at the desk - (1)
at(desk, home)        % Desk is at home - (2)  
at(car, home)         % Car is at home - (3)
at(home, county)      % Home is in county - (4)
at(airport, county)   % Airport is in county - (5)
want(at(I, airport))  % I want to be at airport - (14)
```

### Logical Rules

**Transitivity Rule:**

```python
at(A,B) ∧ at(B,C) → at(A,C)
```

**Movement Rules:**

```python
% Walking within same location
same_location(X,Y) → can_walk(X,Y)

% Driving with car access
at(car,L) && at(I,L) → can_drive(car, anywhere_in_county)
```

### Reasoning Process

1. **Location Analysis:** From (1) and (2): `at(I, home)` via transitivity
    
2. **Resource Assessment:** Car is available at home (3)
    
3. **Goal Analysis:** Need to reach airport in same county (4,5)
    
4. **Plan Generation:**
    
    * `do(walk(desk, car))` - Walk to car
        
    * `do(drive(car, airport))` - Drive to airport
        

This example demonstrates sophisticated spatial reasoning and planning that was revolutionary for 1959 but mirrors how modern AI systems approach problem-solving.

---

## Academic Debates and Criticism {#debates}

### Bar-Hillel's Critique

Professor Bar-Hillel raised significant concerns about McCarthy's approach:

**Logical Inconsistency:**

> "If I am in the immediate spatial neighborhood of the car, and the car is at home, does that necessarily mean I am at home?"

```python
at(I, near(car)) && at(car, home) → at(I, home) ?
```

**Practical Limitations:**

* Why drive when you could take a taxi?
    
* What about flight schedules, traffic conditions, fuel costs?
    
* How does the system handle real-world complexity?
    

### McCarthy's Response

McCarthy defended his work by emphasizing the **epistemological foundation** of AI:

> "To make computers learn, we need epistemology. While current methods are ambiguous, they will eventually become as precise as mathematics. I'm not proposing a practical solution but demonstrating the *types* and *methods* of reasoning required."

This response highlighted McCarthy's focus on fundamental AI principles rather than immediate practical applications—a vision that proved remarkably prescient.

---

## McCarthy's Five Revolutionary Ideas {#five-ideas}

### 1\. Learning Prerequisites

**Principle:** "For a program to learn something, it must first be able to 'hear' it."

**Modern Equivalent:** Prompt engineering and natural language interfaces in current AI systems.

### 2\. Representational Generality

**Principle:** "All actions must be representable within the system."

**Modern Equivalent:** Multimodal AI systems that can process text, images, audio, and video.

### 3\. Incremental Improvement

**Principle:** "Small changes should lead to significant improvements."

**Modern Equivalent:** Fine-tuning, reinforcement learning from human feedback (RLHF), and continuous learning.

### 4\. Partial Success Recognition

**Principle:** "Systems must recognize partial success, not just complete success or failure."

**Modern Equivalent:** Reward shaping in reinforcement learning and graduated scoring systems.

### 5\. Subroutine Learning

**Principle:** "Systems should create reusable functional units independently."

**Modern Equivalent:** Modular neural networks, API compositions, and tool-using AI systems.

---

## From 1959 to 2024: Prophecy Becomes Reality {#modern-ai}

### McCarthy's Vision vs. Modern AI

| McCarthy's 1959 Vision | 2024 Reality | Status |
| --- | --- | --- |
| Natural language knowledge input | Prompt-based interaction | ✅ **Achieved** |
| Logical reasoning | Chain-of-thought prompting | ✅ **Achieved** |
| Common sense judgment | Conversational AI | ✅ **Achieved** |
| Planning and problem-solving | Step-by-step problem solving | ✅ **Achieved** |
| Learning and improvement | Fine-tuning, RLHF | ✅ **Achieved** |

### Unsolved Challenges

#### The Relevance Problem

How do we select relevant information from millions of data points?

**Current Solutions:**

* Attention mechanisms in transformers
    
* Retrieval-Augmented Generation (RAG)
    
* Vector databases and semantic search
    

#### Common Sense Boundaries

How do we define the scope of "common sense"?

**Status:** Still an active research area in AI safety and alignment.

#### Real-time Learning

Can AI systems learn and adapt during conversations?

**Current Limitation:** Most AI systems are fixed after training, though some experimental systems show promise.

---

## Modern Implications and Applications

### Large Language Models as Advice Takers

Modern LLMs like GPT-4, Claude, and Gemini embody many aspects of McCarthy's Advice Taker:

* **Natural Language Interface:** Users provide instructions in plain English
    
* **Contextual Reasoning:** Models maintain conversation context and make inferences
    
* **Planning Capabilities:** Breaking down complex tasks into steps
    
* **Knowledge Integration:** Combining information from training data with user input
    

### Remaining Challenges

1. **Hallucination Control:** Ensuring AI systems don't generate false information
    
2. **Causal Reasoning:** Understanding cause-and-effect relationships
    
3. **World Model Consistency:** Maintaining coherent understanding of reality
    
4. **Ethical Reasoning:** Making moral and ethical judgments
    

---

## Technical Implementation Insights

### From Logic Programming to Neural Networks

McCarthy's logical approach influenced several AI paradigms:

**Prolog and Logic Programming:**

```python
parent(tom, bob).
parent(bob, ann).
grandparent(X, Z) :- parent(X, Y), parent(Y, Z).
```

**Modern Neural Approaches:**

* Transformer attention mechanisms
    
* Memory-augmented networks
    
* Neuro-symbolic AI combining logic and neural networks
    

### The Knowledge Representation Challenge

McCarthy emphasized the importance of knowledge representation—a challenge that modern AI addresses through:

* **Vector Embeddings:** Dense representations of concepts
    
* **Knowledge Graphs:** Structured relationship networks
    
* **Ontologies:** Formal concept hierarchies
    
* **Large-scale Pre-training:** Implicit knowledge in neural weights
    

---

## Conclusion and Modern Significance {#conclusion}

John McCarthy's "Programs with Common Sense" stands as one of the most prescient documents in AI history. Written when computers occupied entire floors and performed simple calculations, it envisioned machines capable of human-like reasoning, natural language understanding, and common sense judgment.

### Key Contributions

1. **Declarative Programming Paradigm:** Shifting focus from "how" to "what"
    
2. **Common Sense Reasoning:** Identifying the importance of everyday knowledge
    
3. **Natural Language Interfaces:** Envisioning human-computer interaction in plain language
    
4. **Learning Systems:** Designing AI that improves through experience
    
5. **Logical Foundation:** Providing formal framework for AI reasoning
    

### Modern Relevance

The principles McCarthy outlined in 1959 continue to guide AI development:

* **Prompt Engineering** mirrors advice-giving to the Advice Taker
    
* **Chain-of-Thought Reasoning** implements McCarthy's logical inference
    
* **Constitutional AI** addresses McCarthy's concerns about AI behavior
    
* **Multimodal Systems** realize his vision of comprehensive representation
    

### Future Directions

As we advance toward Artificial General Intelligence (AGI), McCarthy's insights remain relevant:

* **Interpretability:** Understanding how AI systems reason
    
* **Robustness:** Building systems that handle edge cases gracefully
    
* **Alignment:** Ensuring AI systems pursue intended goals
    
* **Integration:** Combining symbolic reasoning with neural approaches
    

McCarthy's 1959 vision of machines with common sense has largely become reality, yet his deeper insights about the nature of intelligence, learning, and reasoning continue to challenge and inspire AI researchers today.

The journey from room-sized calculators to conversational AI assistants validates McCarthy's fundamental belief: intelligence is not about computational power alone, but about the ability to reason, learn, and apply common sense to novel situations.

---

## References

1. McCarthy, John (1959). ["Programs with Common Sense"](http://jmc.stanford.edu/articles/mcc59/mcc59.pdf). Computer Science Department, Stanford University.
    
2. Russell, Stuart J., and Peter Norvig. *Artificial Intelligence: A Modern Approach*. 4th ed., Pearson, 2020.
    
3. Minsky, Marvin. *The Society of Mind*. Simon & Schuster, 1986.
    
4. Nilsson, Nils J. *The Quest for Artificial Intelligence*. Cambridge University Press, 2009.
    
5. McCorduck, Pamela. *Machines Who Think*. A.K. Peters/CRC Press, 2004.
    

---

*This analysis was prepared to commemorate the 65th anniversary of McCarthy's seminal work and its continuing influence on modern artificial intelligence development.*
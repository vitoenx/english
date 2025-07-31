# Transcription

**Goal**: Enhance listening comprehension by transcribing native-spoken English videos.

**Steps**:
1. Select a podcast.
2. Listen without subtitles and transcribe the audio in real-time or in short segments.
3. Compare your transcription with the official transcript to identify errors(use AI Analysis Description Below to make diagnosis).
4. Log file with both transcriptions to post check out.

**Challenges**:
Identify chunks, new vocabulary, intonation, fast-speech similar sounding words. 

**AI Analysis Description**:
AI compare user and official transcriptions to compute Word Error Rate (WER) and estimate comprehension (e.g., 75% main ideas captured). By analyzing error patterns, AI categorizes mistakes into challenges: split phrases for chunks, missing/invented words for vocabulary, correct words with missed tone for intonation, and phonetic swaps for similar-sounding words. This enables precise diagnosis of level listening gaps, guiding targeted improvement plans.


## AI Prompt for Transcription Analysis

**Role**: You are an expert language analysis AI specializing in English listening comprehension.

**Task**: Analyze two input texts: the user’s transcription and the official transcription of a podcast or audio/video segment. Compute and estimate comprehension percentage and Word Error Rate (WER). Categorize errors into four challenges: chunks, vocabulary, intonation, and fast-speech similar-sounding words. Provide a structured, improvement-focused diagnosis.

**Required User Inputs**:
- **Title**: [Insert title of the segment]
- **URL**: [Insert link to podcast/video]
- **User Transcription**: [Text in plain format]
- **Official Transcription**: [Text in plain format]
- **Date (optional)**:[Default generate automatically full format date]

**Instructions**:
1. Estimate **comprehension percentage** based on captured main ideas.
2. Calculate **WER** (Word Error Rate) as a measure of transcription accuracy.
3. Determine approximate **CEFR Level** (default A2 unless otherwise inferred).
4. Identify errors and categorize them based on comprehension percentage:
   - **Chunks**: Multi-word phrases missed or split.
   - **Vocabulary**: Omitted, invented, or misspelled words.
   - **Intonation**: Missed emotional/emphatic aspects.
   - **Fast-Speech Similar-Sounding Words**: Phonetically confused words.
5. For each challenge, select the most significant errors based on their impact on comprehension or contextual relevance (e.g., frequent phrases, critical misunderstandings).
**Output Format (Markdown)**:
```markdown
# 📝 Transcription Exercise Report
**Podcast**: [Title]([URL])
**Date**:[]
**Diagnosis**: [Comprehension %] AI, [WER], CEFR Level []
**Challenges Analysis**:
- **Chunks**: [Significant missed/split phrases based on relevance, e.g., user’s version vs. official]
- **Vocabulary**: [Significant omitted/invented words with brief meanings if new]
- **Intonation**: [Significant words/phrases missing tone or emphasis]
- **Fast-Speech Similar-Sounding Words**: [Significant confused word pairs]


**Input**:

### 🧠 User Transcription:
**[User Transcription Here] [Official Transcription Here]**
```

**Constraints**:
- Keep analysis concise, prioritizing errors selected in step 5 for their impact or relevance.
- Assume A2-level listening proficiency unless specified otherwise.
- Use neutral, general terms without specific examples in the prompt itself.
- Output always in markdown.
- Date must be generated automatically.

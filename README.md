# README: Mexican Spanish Frequency Vocabulary Game

## 1. Introduction

This application is a gamified language learning tool designed to take users from absolute beginner (**Level 0**) to an intermediate proficiency (**B1**) in **Mexican Spanish**.

Unlike traditional apps that group words by arbitrary themes (e.g., "The Zoo," "Kitchen Items"), this application utilizes **Frequency-Based Learning**. Users learn words in the order of their statistical usage in real-world Mexican Spanish. This ensures that each level adds vocabulary that is statistically the most useful for everyday conversation.

### Key Features:
* **Target Dialect:** Mexican Spanish (LatAm standard with Mexican lexical preferences).
* **Total Vocabulary:** 3,000 distinct words (plus a survival set).
* **Progression:** 10 Levels (300 words each) + Level 0 (Survival).
* **Gamification:** Specifics TBD. The gamified app will be heavily focused on vocabulary rather than grammar. It strives to prevent the "Duolingo clone" feel and avoids reliance on "streaks" as a primary retention mechanic.

---

## 2. Level Breakdown & Progression

The course moves through **11 distinct stages**. The difficulty curve is logarithmic; early levels provide massive comprehension gains, while later levels refine nuance.

| Level | CEFR Mapping | Word Count | Focus Description |
| :--- | :--- | :--- | :--- |
| **Lvl 0** | **Pre-A1** | ~80 words | **Survival Mode:** Essential fixed phrases, numbers, and basics to function immediately. |
| **Lvl 1** | **A1** | 300 words | **The Core:** The absolute most frequent words (verbs *ser/estar*, articles, basic pronouns). |
| **Lvl 2** | **A1** | 300 words | **Daily Life:** High-usage verbs (*ir, comer*), question words, and common objects. |
| **Lvl 3** | **A1** | 300 words | **Foundational:** Connecting sentences, describing immediate surroundings, time frames. |
| **Lvl 4** | **A2** | 300 words | **Expansion:** Past tense triggers, movement verbs, describing people and routine. |
| **Lvl 5** | **A2** | 300 words | **Interaction:** Transactional vocabulary (shopping, banking), frequency adverbs. |
| **Lvl 6** | **A2** | 300 words | **Expression:** Opinions, feelings, describing events, "Mexicanisms" (e.g., *ahorita*). |
| **Lvl 7** | **B1** | 300 words | **Nuance:** Abstract nouns, complex prepositions, professional/work vocabulary (*chamba* context). |
| **Lvl 8** | **B1** | 300 words | **Storytelling:** Narrative verbs, connectors (*sin embargo*), detailed descriptions. |
| **Lvl 9** | **B1** | 300 words | **Society:** Media, news, health, technology (Mexican standard terms). |
| **Lvl 10** | **B1** | 300 words | **Fluency Bridge:** Idiomatic verbs, subjunctive triggers, colloquial intensity. |

---

## 3. Level 0: Survival Spanish (The "Emergency Kit")
*Note: These words do not count toward the 3,000 frequency algorithm but are prerequisites for the game mechanics.*

**Goal:** Enable the user to learn the basic and neccessary words that would likely be taught in a "Spanish 101" class. These words will not neccessarily be frequency based, but should be words one would be expected to learn when first encountering a language.

### Content Checklist:
* **Numbers:** 1-25, 30, 40, 50, ... 100, 1000.
* **Time:** Days of the week, Months, "Today/Tomorrow/Yesterday."
* **Colors:** Colors of the rainbow, black, white, etc.
* **Greetings & Farewells (Mexican Context):**
    * *Hola, Buenos días/tardes/noches.*
    * *¿Qué onda?* (Casual Mexican greeting).
    * *¿Cómo estás? / ¿Mande?* (Polite "What?").
* **Survival Phrases:**
    * *¿Dónde está el baño?* (Where is the bathroom?)
    * *La cuenta, por favor.* (The check, please.)
    * *No hablo español.* (I don't speak Spanish.)
    * *¿Cuánto cuesta?* (How much is it?)
    * *Ayuda.* (Help.)

---

## 4. Vocabulary Distribution (The Math)

The core game (Levels 1–10) contains **3,000 words**. To maintain grammatical balance, every level of 300 words must adhere to the following Part of Speech (POS) ratios.

### Target Ratios per Level (300 Words)

| Part of Speech | Percentage | Word Count (Per Level) | Notes for Content Team |
| :--- | :--- | :--- | :--- |
| **Nouns** | **40%** | **120** | Prioritize concrete objects first, then abstract concepts. |
| **Verbs** | **20%** | **60** | *Mexican Usage Note:* Use *tomar* or *agarrar*, avoid *coger*. |
| **Adjectives** | **16%** | **48** | Pairs of opposites (big/small, hot/cold). |
| **Adverbs** | **8%** | **24** | Time (*ya, todavía*) and manner (*bien, mal*). |
| **Prepositions** | **6%** | **18** | High frequency (*de, en, a, por, para*). |
| **Conjunctions** | **4%** | **12** | Connectors (*y, pero, que, o*). |
| **Pronouns** | **4%** | **12** | *Note:* Exclude "Vosotros" (Spain); focus on "Ustedes". |
| **Interjections** | **2%** | **6** | Conversational fillers (*pues, ay, órale, bueno*). |
| **TOTAL** | **100%** | **300 Words** | |

---

## 5. CEFR Level Mapping Strategy

### Levels 1–3: A1 (The Beginner)
* **Goal:** Basic discovery.
* **Grammar Context:** Present tense indicative.
* **Mexican Lexicon:** Use *carro* (not *coche*), *celular* (not *móvil*), *computadora* (not *ordenador*).

### Levels 4–6: A2 (The Elementary)
* **Goal:** Describe experiences and immediate environment.
* **Grammar Context:** Introduction of Past Tense (Preterite vs. Imperfect).
* **Mexican Lexicon:** *Boleto* (ticket), *chamarra* (jacket), *camión* (bus), *platicar* (to chat).

### Levels 7–10: B1 (The Intermediate)
* **Goal:** Deal with most situations while traveling; abstract thought.
* **Grammar Context:** Future tense, Conditionals, and Introduction to Subjunctive.
* **Mexican Lexicon:** *Estacionarse* (to park), *rentar* (to rent), *checar* (to check).

---

## 6. Technical & Content Guidelines

### For the Data Team (JSON/Database Structure)

The vocabulary data is structured as arrays of objects. Please ensure strict adherence to the schema below.

**Adjectives Example:**
```json
{
  "region": "MX",
  "partOfSpeech": "adjectives",
  "level": 1,
  "words": [
    {
      "id": 1,
      "spanish": "bueno",
      "english": "good",
      "masculine": "bueno",
      "feminine": "buena",
      "pluralMasculine": "buenos",
      "pluralFeminine": "buenas"
    }
  ]
}

**Adverbs Example:**
{
  "region": "MX",
  "partOfSpeech": "adverbs",
  "level": 1,
  "words": [
    {
      "id": 2,
      "spanish": "también",
      "english": "also, too"
    }
  ]
}
**Nouns Example:**
{
  "region": "MX",
  "partOfSpeech": "nouns",
  "level": 1,
  "words": [
    {
      "id": 4,
      "spanish": "hombre",
      "english": "man",
      "gender": "masculine",
      "plural": "hombres"
    }
  ]
}
**Verbs Example (Note: Conjugation Object):**
{
  "region": "MX",
  "partOfSpeech": "verbs",
  "level": 1,
  "words": [
    {
      "id": 7,
      "spanish": "ser",
      "english": "to be (permanent)",
      "conjugations": {
        "present": {
          "yo": "soy",
          "tú": "eres",
          "él/ella/usted": "es",
          "nosotros/nosotras": "somos",
          "ellos/ellas/ustedes": "son"
        },
        "preterite": {
          "yo": "fui",
          "tú": "fuiste",
          "él/ella/usted": "fue",
          "nosotros/nosotras": "fuimos",
          "ellos/ellas/ustedes": "fueron"
        }
      }
    }
  ]
}
```

Strict "No-Go" List:

> NO Vosotros conjugations (strictly Ustedes for plural 'you').

> NO Coger (vulgar in Mexico; replace with tomar or agarrar).

> NO Zumo (use Jugo).

> NO Ordenador (use Computadora).

In short, avoid Spain-specific words, with a focus on Mexican words (but not slang or subregion-specific).

## 7. Conclusion

This application aims to be the most efficient path to intermediate CEFR B1 (in regards to simple vocabulary) for learners targeting the Americas. By strictly adhering to a 3,000-word frequency list distributed across 10 gamified levels, we ensure that users are not just "playing a game," but acquiring the statistical building blocks of the language.

    "Upon completing Level 10, a user will recognize approximately 94% of the vocabulary in daily Mexican conversation and 90% in general texts. This coverage is widely considered the threshold for independent functioning in the language."
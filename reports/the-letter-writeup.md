# TryHackMe – The Letter
## OSINT Investigation Write-up

**Platform:** TryHackMe  
**Room:** The Letter  
**Category:** OSINT / Historical Investigation  
**Status:** Completed  
**Country:** France  
**Techniques:** Postal code decoding, historical newspaper research, digital archives, historical investigation, information correlation.

---

## 1. Introduction

The objective of this challenge was to identify an individual mentioned indirectly in a historical letter by analysing several documents and correlating information from different sources.

The initial evidence consisted of:

- `letter.png` – An old French postal envelope.
- `Newspaper_clipping.png` – A historical newspaper clipping from *L'Ouest-Éclair*.
- `Note.txt` – A personal message written by Audette to Édouard.

The investigation followed a progressive OSINT approach, starting with geographical identification and ending with the identification of a historical maritime rescue crew member.

## 2. Postal Code Identification

### 2.1 Envelope Analysis

The first step was to examine the postal envelope.

At the bottom of the envelope, I noticed a sequence of orange dots and vertical bars.

Instead of treating this sequence as a conventional barcode, I investigated its structure and discovered that it corresponded to a French postal code substitution system.

### 2.2 Decoding the Postal Code

I found a decoding table explaining how each digit is represented by a specific combination of dots and vertical bars.

Using this substitution table, I decoded the sequence printed on the envelope.

**Decoded postal code: 29760**

This postal code corresponds to Penmarc'h, in the Finistère department, France.

This discovery provided the first geographical lead for the investigation.

**Evidence:** 
- Original postal envelope.
- French postal code substitution table.
- Decoded postal code.

## 3. Historical Newspaper Identification

### 3.1 Analysing the Newspaper Clipping

The second step was to examine the historical newspaper clipping.

The newspaper was identified as *L'Ouest-Éclair*.

One of the visible headlines mentioned Édouard Herriot declaring his solidarity with Paul Painlevé.

This reference became the starting point for a historical search.

### 3.2 Searching for the Publication Date

I searched online using the historical reference:

"Quand M. Herriot se déclare solidaire de M. Painlevé"

The search results provided a chronological indication pointing towards the newspaper editions published around 24–25 May 1925.

To verify this information, I used Gallica, the digital library of the Bibliothèque nationale de France.

I searched the historical editions of *L'Ouest-Éclair* around the identified dates.

This research led me to the edition dated:

**24 May 1925**

The identification of the newspaper edition established a connection with the historical events occurring during that period.

## 4. Historical Event Investigation

After identifying the geographical location and the newspaper publication date, I continued researching the historical events associated with Penmarc'h.

I discovered a dedicated historical archive:

**Source:**  
https://www.kbcpenmarch.franceserv.com/la-catastrophe-du-23-mai-1925-selon-la-presse-locale.html

The website documented the maritime disaster of **23 May 1925**.

The incident involved two fishing boats:

- Berceau de Saint-Pierre
- Saint-Louis

The historical records also described the rescue operations conducted by several crews.

This discovery provided an important direction for the next stage of the investigation.

## 5. Analysing the Personal Note

I returned to the original message written by Audette to Édouard.

Two sentences were particularly important:

> "Ton arrière-grand-père n'avait même pas l'âge de passer le permis quand il s'est distingué ce jour-là."

> "Le benjamin de l'équipe, et certainement pas le moins courageux."

These statements provided two important clues:

1. The individual was younger than 18 years old.
2. He was the youngest member of his team.

The reference to being proud to see Édouard on the water also reinforced the maritime connection.

The objective was now to identify a young member of one of the rescue crews involved in the historical event.

## 6. Rescue Crew Investigation

While exploring the historical archive, I discovered a section documenting the medals awarded to the rescue crews.

Two crews were particularly relevant:

- Gérald-Samuel
- Arche-d'Alliance

The records provided the names, ages, positions and distinctions of their members.

I examined the information and compared the ages with the clue contained in Audette's letter.

Among the listed crew members, one individual matched the age-related clue:

**Yves GOURLAOUEN – 15 years old – Mousse**

He was a member of the rescue crew of the *Arche-d'Alliance*.

His age was particularly significant because he was only 15 years old, considerably younger than the legal driving age mentioned indirectly in the letter.

This discovery established the final identification.

## 7. Final Identification

**Identified individual: Yves Gourlaouen**

| Attribute | Information |
|---|---|
| Full name | Yves Gourlaouen |
| Age | 15 years |
| Position | Mousse |
| Rescue crew | Arche-d'Alliance |
| Historical event | Maritime disaster of 23 May 1925 |

The identification was established by correlating the information contained in the original letter with the historical rescue crew records.

The age of 15 years matched the central clue in Audette's message.

## 8. Investigation Methodology

The challenge was solved through the following sequence:

1. Examine the postal envelope and identify the coded sequence.
2. Use the French postal code substitution table to decode the postal code.
3. Identify Penmarc'h as the geographical location.
4. Analyse the newspaper clipping and identify its historical reference.
5. Search for the publication date using the reference to Édouard Herriot and Paul Painlevé.
6. Consult Gallica to locate the original edition of *L'Ouest-Éclair* dated 24 May 1925.
7. Research the maritime disaster of 23 May 1925.
8. Examine historical rescue crew records and their awarded medals.
9. Compare the recorded ages with the clues in Audette's letter.
10. Identify Yves Gourlaouen, aged 15, as the individual matching the clues.

## 9. Tools and Resources

| Tool / Resource | Purpose |
|---|---|
| French postal code substitution table | Decode the envelope |
| dCode | Postal code decoding reference |
| Google Search | Historical reference investigation |
| Gallica – BnF | Historical newspaper archives |
| KBC Penmarc'h | Maritime disaster and rescue crew records |
| Manual OSINT analysis | Information correlation |

### References

- [dCode – French Postal Barcode](https://www.dcode.fr/french-postal-barcode)
- [Gallica – Bibliothèque nationale de France](https://gallica.bnf.fr/)
- [KBC Penmarc'h – La catastrophe du 23 mai 1925](https://www.kbcpenmarch.franceserv.com/la-catastrophe-du-23-mai-1925-selon-la-presse-locale.html)

## 10. Evidence Collection

The screenshots collected during the investigation are organised as follows:

```text
screenshots/
├── 01-original-envelope.png
├── 02-postal-code-decoding-table.png
├── 03-historical-search-herriot.png
├── 04-gallica-newspaper-edition.png
├── 05-maritime-disaster-records.png
├── 06-rescue-crew-medals.png
└── 07-final-identification.png
```

Original evidence was preserved to maintain the integrity of the investigation.

## 11. Conclusion

This challenge demonstrated how different OSINT techniques can be combined to solve a historical investigation.

Starting from a coded postal sequence, the investigation progressively uncovered a geographical location, a historical newspaper edition, a maritime disaster and the records of its rescue crews.

By correlating the historical records with the clues contained in Audette's personal letter, I identified Yves Gourlaouen, aged 15, as the individual matching the description.

**Key takeaway:** Effective OSINT is not limited to searching for information. It involves identifying connections between independent sources, validating evidence and building a logical investigation from small clues.

## Pitch
The university of Bern provides its members with free access to a high performance computing cluster (UBELIX) and generative AI tools. The challeng we faced in our project at the Data Science Lab was to use these resources programmatically. Our talk will shine a light on how we manage the different processing steps on client-devices, Server, the university's GPUStack and UBELIX.

## Overview
- The application
- Challenges
- The solutions we came up with

## Challenges
### Liste
- audio extraction im browser
- matadaten aus Video
    - muss schnell gehen
    - idealerweise ohne provider subscription
- UBELIX batch job aus code, keine API (nobody did this before us)

### Lösungen
- *Browser*: failover to backend
- *Metadaten aus Video*:
    - GPUStack existiert! -> GUI DEMO
    - Zweiteilige Lösung: a) audio transkript mit whisper b) metadaten extrahieren und json formen, prompts zeigen, traffic zeigen
- Für UBELIX existiert keine API
    - Wie wird UBELIX derzeit verwendet?
    - Lösung: Dedizierter Account auf UBELIX, dedizierter SSH key, python library (paramiko) für SSH traffic, UBELIX commands haben json output

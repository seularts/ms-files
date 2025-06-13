:::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Top 10 Privacy Risks](#div-topprivacy){#topprivacy-link .tab-link
  role="tab" aria-selected="false" aria-controls="topprivacy"}
- [Participate](#div-participate){#participate-link .tab-link role="tab"
  aria-selected="false" aria-controls="participate"}
- [Acknowledgements](#div-acknowledgements){#acknowledgements-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgements"}
- [Translation](#div-translation){#translation-link .tab-link role="tab"
  aria-selected="false" aria-controls="translation"}
- [FAQs](#div-faqs){#faqs-link .tab-link role="tab"
  aria-selected="false" aria-controls="faqs"}

# OWASP Top 10 Privacy Risks {#owasp-top-10-privacy-risks .page-title}

::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
![Version 2.0](https://img.shields.io/badge/version-2.0-brightgreen)
![OWASP Lab Project](https://img.shields.io/badge/OWASP-Lab-yellow)

The OWASP Top 10 Privacy Risks Project provides a top 10 list for
privacy risks in web applications and related countermeasures. It covers
technological and organizational aspects that focus on real-life risks,
not just legal issues. The Project provides tips on how to implement
privacy by design in web applications with the aim of helping developers
and web application providers to better understand and improve privacy.
The list uses the OECD Privacy Guidelines as a framework and can also be
used to assess privacy risks associated with specific web applications.

## Top 10 Privacy Risks

The following table shows version 2.0 of the OWASP Top 10 Privacy Risks
and compares it to the ranking of 2014.

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
 2021  2014  Title 
 P1    1     Web Application Vulnerabilities 
 P2    2     Operator-sided Data Leakage 
 P3    3     Insufficient Data Breach Response 
 P4    New   Consent on Everything 
 P5    5     Non-transparent Policies, Terms and Conditions 
 P6    4     Insufficient Deletion of User Data 
 P7    New   Insufficient Data Quality
 P8    9     Missing or Insufficient Session Expiration 
 P9    13    Inability of Users to Access and Modify Data 
 P10   6     Collection of Data Not Required for the User-Consented Purpose
```
:::
::::

Detailed information is provided in the Top 10 Privacy Risks tab.

## Quick Download

- [Top 10 Privacy Risks Countermeasures v2.0
  (PDF)](OWASP_Top_10_Privacy_Risks_Countermeasures_v2.0.pdf)
- [Top 10 Privacy Risks Presentation v2.0
  (PPTX)](assets/OWASPTop10PrivacyRisks_v2.pptx)
- [Presentation from OWASP Roundtable "Stammtisch" Hamburg 2021
  (PDF)](../www-chapter-germany/stammtische/hamburg/assets/slides/2021-08-05_OWASP%20Top%2010%20Privacy%20Risks%20v2.0.pdf)

## Licensing

OWASP Top 10 Privacy Risks Project is free to use. It is licensed under
the [Creative Commons CC-BY-SA v3.0
License](https://creativecommons.org/licenses/by-sa/3.0/).
:::::

::: {#sec-topprivacy .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Top 10 Privacy Risks {#top-10-privacy-risks}

Version 2.0 of the OWASP Top 10 Privacy Risks list from 2021. Further
information and related countermeasures will be provided soon.

The type shows if a risk is rather
![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji
height="20" width="20"} organizational,
![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji
height="20" width="20"} technical, or both.

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------- --------------- ------------ -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Type**                                                                                                                                                                                                                                                                                                       **Title**                                                        **Frequency**   **Impact**   **Description**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Web Application Vulnerabilities                                  High            Very high    Vulnerability is a key problem in any system that guards or operates on sensitive user data. Failure to suitably design and implement an application, detect a problem or promptly apply a fix (patch) is likely to result in a privacy breach. This risk also encompasses the OWASP Top 10 List of web application vulnerabilities and the risks resulting from them.
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Operator-sided Data Leakage                                      High            Very high    Failure to prevent the leakage of any information containing or related to user data, or the data itself, to any unauthorized party resulting in loss of data confidentiality. Introduced either due to intentional malicious breach or unintentional mistake e.g. caused by insufficient access management controls, insecure storage, duplication of data or a lack of awareness.
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Insufficient Data Breach Response                                High            Very high    Not informing the affected persons (data subjects) about a possible breach or data leak, resulting either from intentional or unintentional events; failure to remedy the situation by fixing the cause; not attempting to limit the leaks.
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Consent on Everything                                            Very high       High         Aggregation or inappropriate use of consent to legitimate processing. Consent is \"on everything\" and not collected separately for each purpose (e.g. use of website and profiling for advertising).
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Non-transparent Policies, Terms and Conditions                   Very high       High         Not providing sufficient information to describing how data is processed, such as its collection, storage, and processing. Failure to make this information easily-accessible and understandable for non-lawyers.
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Insufficient Deletion of Personal Data                           High            High         Failure to effectively and/or timely delete personal data after termination of the specified purpose or upon request.
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Insufficient Data Quality                                        Medium          Very high    The use of outdated, incorrect or bogus user data. Failure to update or correct the data.
  P8       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Missing or insufficient Session Expiration                       Medium          Very high    Failure to effectively enforce session termination. May result in collection of additional user-data without the user's consent or awareness.
  P9       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Inability of users to access and modify data                     High            High         Users do not have the ability to access, change or delete data related to them.
  P10      ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Collection of data not required for the user-consented purpose   High            High         Collecting descriptive, demographic or any other user-related data that are not needed for the purposes of the system. Applies also to data for which the user did not provide consent.
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------- --------------- ------------ -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Note: The values between 0 to 3 used for frequency and impact rating
were replaced by a textual description: 0-1.5: Low, 1.5-1.9: Medium,
1.9-2.3: High, \> 2.3: Very high
:::

::: {#sec-participate .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Participate

Some ways you can help:

- Discuss with us in the mailing list or Google docs
- Tell your colleagues and friends about the project
- Provide feedback (feel free to contact us)
- Apply the results in practice to improve web application privacy

Sign up to our [mailing
list](https://groups.google.com/a/owasp.org/forum/#!forum/top-10-privacy-risks-project/join)
to stay informed.

## Discussions and Documentation

To avoid overwriting issues we use Google Docs for our discussions.

### Ongoing

[Countermeasures
v2.1](https://docs.google.com/document/d/1s6RLhyLi02-3LMOxC8lBQEGhVrqKT0QZYN1X4aBqSsM/edit?usp=sharing)\

### Closed discussions and documents

[Calculation of the complete Privacy Risks list
v2.0](https://docs.google.com/spreadsheets/d/1GstkaCzO7_ok1p4rr1drq0SuPLjg5MlkshG5oS58vAY/edit?usp=sharing)\
[Impact Rating
2020](https://docs.google.com/document/d/1VuusvZnhHpWvmPFeAovM68iB_Do3XFZCH2EsITGuAKg/edit)\
[Privacy Risk Candidate List
2020](https://docs.google.com/document/d/1eEU7TsoaPG56-zhJi4bi1SD53Jto84GQ8dDGTajL8TY/edit)\
[Method Update
2019](https://docs.google.com/document/d/1AlAg2cybvo5VX-frzF5uHeAcib3X2rTAA2p97XH8fHw/edit)\
[Countermeasures
v1.0](https://docs.google.com/document/d/1GaoJDPtyXMv09wIw9xXTVPYTR_6fQROlptszPhxVc1s/edit?usp=sharing)\
[Method
description](https://docs.google.com/document/d/1nHM9LH2rP6ac3DvJ7lehDNb9qVP5YADOQGNEuiy5okg/edit)\
[Privacy Risk list
2014](https://docs.google.com/document/d/1ufAuGtW42gUHtJF-9_VOzNZEegZJnMyqDcyfzmsjJeQ/edit)\
[Draft
list](https://docs.google.com/document/d/1WMljvy09nulPnzv5XkFc2uxn1bSR-ftKqx5VoayTzW8/edit)\
[Impact rating
2014](https://docs.google.com/a/owasp.org/document/d/1Gjd5XVJyGWHryUA2WyPSRQ0gQuaD5zWUCHU76_FHMKU/edit)\
[Calculation of the complete Privacy Risks list
v1.0](https://docs.google.com/spreadsheets/d/1q7Xh4gclSieXNpVbdvyFwsZMENo2r3BoN2S3ww_W5-M/edit)\
:::

::: {#sec-acknowledgements .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Volunteers

The Top 10 Privacy Risk list was developed by a team of volunteers. The
primary contributors have been:

### Version 2.0 {#version-20}

- Florian Stahl
- Abraham Kang
- Fernando Galves
- Edward Delaporte
- Angel Camacho
- Stefan Burgmair
- Ramón Salado
- Tetsuya Nihonmatsu
- Shoichi Nakata
- Eyal Estrin

### Version 1.0 {#version-10}

- Stefan Burgmair
- R. Jason Cronk
- Edward Delaporte
- Tim Gough
- Prof. Hans-Joachim Hof
- Lukasz Olejnik
- Guillaume Simard
- Florian Stahl

## Sponsors

Please contact us if you are interested to support the OWASP Top 10
Privacy Risks project. Your company logo will be displayed on the
project website and you will receive an individual web-based training on
the project content for free.
:::

::: {#sec-translation .section .page-body .tab-hidden}

------------------------------------------------------------------------

Currently project documentation is available in English, German,
Spanish, Japanese and French. Translation to Portuguese and Arabic is
ongoing. If you are interested in helping to translate to any other
language, please contact the project leaders.

## German

### Top 10 Datenschutzrisiken

Der Typ gibt an, ob ein Risiko eher
![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji
height="20" width="20"} organisatorisch,
![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji
height="20" width="20"} technisch oder beides ist.

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------- ---------------- ------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Typ**                                                                                                                                                                                                                                                                                                        **Titel**                                                         **Häufigkeit**   **Schaden**   **Beschreibung**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Schwachstellen in Web-Anwendungen                                 Hoch             Sehr hoch     Schwachstellen sind ein zentrales Problem in jedem System, mit dem sensible Nutzerdaten erhoben, verarbeitet und genutzt werden. Bestehen Fehler im Design oder in der Implementierung der Applikation, werden Probleme nicht entdeckt oder Sicherheitspatches nicht unverzüglich eingespielt, führt dies mit hoher Wahrscheinlichkeit zu einer Verletzung des Persönlichkeitsrechts. Dieses Risiko wird bereits in anderen Projekten behandelt, wie der OWASP Top 10 Liste der häufigsten Sicherheitsrisiken für Webanwendungen.
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Datenabfluss beim Betreiber                                       Hoch             Sehr hoch     Wird die unerwünschte Preisgabe personenbezogener oder personenbeziehbarer Daten an nicht autorisierte Personen nicht wirksam verhindert, ist dies ein Verlust der Vertraulichkeit. Ursachen sind entweder ein vorsätzlich durchgeführter Datenabzug oder unbeabsichtigte Fehler wie beispielsweise unzureichendes Zugriffsmanagement, unsichere Datenablage, Datendopplung oder fehlendes Problembewusstsein (Awareness).
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Unzureichende Reaktion bei einer Datenpanne                       Hoch             Sehr hoch     Betroffene werden nicht über mögliche Pannen oder Datenlecks benachrichtigt, die durch Angriffe oder unbeabsichtigte Ereignisse entstehen. Angemessene Abhilfemaßnahmen zum Schließen der Lücken und Beseitigung der Ursache fehlen.
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Einwilligung für alles                                            Sehr hoch        Hoch          Das aggregierte oder unangemessene Einholen der Einwilligung vom Benutzer zur Legitimierung der Datenverarbeitung. Die Einwilligung wird kollektiv für alles eingeholt und nicht separat für jeden Zweck wie z.B. Nutzung der Webseite und Analyse für Werbung.
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Intransparente Nutzungs-bedingungen                               Sehr hoch        Hoch          Informationen zur Datenverarbeitung wie Erhebung, Speicherung und Nutzung personenbezogener Daten sind unzureichend. Diese Informationen sind nicht leicht zugänglich oder für juristische Laien nicht verständlich aufbereitet.
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Unzureichende Löschung personen-bezogener Daten                   Hoch             Hoch          Personenbezogene Daten werden nicht termingerecht oder nicht effektiv nach Zweckablauf bzw. aufgrund einer Löschanfrage gelöscht.
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Unzureichende Datenqualität                                       Mittel           Sehr hoch     Es werden veraltete, inkorrekte oder gefälschte personenbezogene Daten genutzt. Datenaktualisierungen oder -korrekturen finden nicht in ausreichendem Maße statt.
  P8       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Fehlendes oder unzureichendes Session-Ende                        Mittel           Sehr hoch     Unzureichendes Beenden von Sessions. Dies kann dazu führen, dass zusätzliche Nutzerdaten ohne Einverständnis oder Wissen des Nutzers gesammelt werden.
  P9       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Zugriff auf oder Änderungen von Benutzerdaten nicht möglich       Hoch             Hoch          Benutzer können auf ihre Daten nicht zugreifen, diese ändern oder löschen.
  P10      ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Sammeln von Daten, die über den eigentlichen Zweck hinaus gehen   Hoch             Hoch          Es werden Beschreibungsdaten, demographische Daten oder sonstige personenbezogene Daten gesammelt, die nicht für den vereinbarten Zweck der Anwendung benötigt werden. Ebenso werden Daten gesammelt, für deren Erhebung der Nutzer keine Einverständniserklärung abgegeben hat.
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------- ---------------- ------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## French

### Top 10 des risques pour la vie privée (1.0) {#top-10-des-risques-pour-la-vie-privée-10}

Le type détermine si un risque est
![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji
height="20" width="20"} organisationnel,
![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji
height="20" width="20"} technique ou les deux.

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------- --------------- ------------ ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Type**                                                                                                                                                                                                                                                                                                       **Titre**                                           **Fréquence**   **Impact**   **Description**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Application avec vulnérabilités                     Élevé           Très élevé   Une application contenant des vulnérabilités logicielles est un problème clé pour des systèmes qui traitent des données personnelles sensibles. Un manque dans la conception, dans l'implémentation, une détection de failles insuffisante, une incapacité à appliquer une solution (patch) à une faille mènent à une fuite de données personnelles.
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Fuite de données par l'opérateur                    Élevé           Très élevé   L'impossibilité de prévenir la fuite de données concernant ou pas des données personnelles à des groupes non autorisés mène à une perte de confidentialité. Que ce soit intentionnel ou une erreur (mauvaise gestion des accès, stockage non sécuritaire, duplication de données ou manque de réactivité).
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Mauvaise réponse suite à une fuite de données       Élevé           Très élevé   Ne pas informer les gens affectés à propos d'une fuite de données. Ne pas remédier à la situation en identifiant et en réparant la cause. Ne pas tenter de limiter la fuite.
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Suppression insuffisante des données personnelles   Très élevé      Élevé        Ne pas supprimer les données personnelles convenablement à la fin de l'utilisation précisée à l'utilisateur.
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Conditions d'utilisation opaques                    Très élevé      Élevé        Ne pas fournir suffisamment d'information sur la collecte, le stockage et le traitement de vos données. Ne pas fournir l'information claire et facilement accessible. Information seulement compréhensible par des avocats.
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Collecte de données excessive                       Très élevé      Élevé        Collecter de l'information descriptive, géographique, démographique ou toute autre information qui n'est pas nécessaire pour le système. S'applique aussi pour les données qui n'ont pas fait le consentement de l'utilisateur.
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Partage de données                                  Élevé           Élevé        Partager des données à des tiers sans obtenir le consentement de l'utilisateur. Partager des données en échange d'argent ou via des widgets : maps, réseau social, boutons et analytiques.
  P8       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Données personnelles périmées                       Élevé           Très élevé   L'utilisation de données incorrectes ou en lien avec des utilisateurs fictifs. Impossibilité de mettre à jour ces données.
  P9       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Expiration de session manquante ou insuffisante     Moyen           Très élevé   Échec à mettre fin convenablement à une session. Cela permet de collecter de l'information supplémentaire sur l'utilisateur sans son consentement ou sa connaissance.
  P10      ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Transmission de données non sécurisée               Moyen           Très élevé   Ne pas sécuriser le transfert de données permettant la fuite de ces dernières. Ne pas renforcer les mécanismes qui pourraient limiter les fuites. Permettre de sortir des données d'utilisateur à l'extérieur des limites de l'opération de l'application.
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------- --------------- ------------ ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Vidéo

[Top 10 des risques pour la vie privée en français
(Youtube)](https://youtu.be/babi0T0xQ2Y)

### Flyer

[Infoflyer in French](Top_10_Privacy_Risks_French.html)

## Japanese

### トップ10 プライバシーリスク バージョン2.0 日本語訳 {#トップ10-プライバシーリスク-バージョン20-日本語訳}

タイプはリスクが組織的![：man_office_worker：](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png){loading="lazy"
height="20"
width="20"}、技術的![：woman_technologist：](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png){loading="lazy"
height="20" width="20"}、またはその両方であるかどうかを示しています。

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------- ------------ ------------ ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **タイプ**                                                                                                                                                                                                                                                                                                     **タイトル**                                   **頻度**     **影響**     **説明**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Webアプリケーションの脆弱性                    高い         非常に高い   脆弱性は、機密性の高い個人データを保護または操作する上でシステムの重大な問題です。アプリケーションの適切な設計と実装、問題の検出、または修正（パッチ）の迅速な適用を怠ると、プライバシーが侵害される可能性があります。このリスクには、[Webアプリケーションの脆弱性のOWASPトップ10リスト](../www-project-top-ten/index.html){target="_blank" rel="noopener"}とそれらに起因するリスクも含まれます。
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   オペレーター側のデータ漏えい                   高い         非常に高い   個人データを含むまたは個人データに関連する情報が許可されていない第三者に漏洩し、データの機密性が失われます。意図的な悪意のある違反または意図しないミスのいずれかが原因で引き起こされました。たとえば、不十分なアクセス管理制御、安全でないストレージ、データの重複、または認識の欠如が原因です。
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   不十分なデータ侵害対応                         高い         非常に高い   意図的または意図的でないイベントのいずれかが原因で発生する侵害またはデータ漏洩について、影響を受ける人（データ主体）に通知しないこと。原因を修正することによって状況を改善することに失敗すること。漏洩を制限することを怠ることです。
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          すべてに同意する                               非常に高い   高い         処理を正当化するための同意を集約する、または同意を不適切に使用することです。同意の対象は「すべて」であり、目的ごとに収集していません（たとえば、Webサイトの使用や広告のプロファイリング）。
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          不透明なポリシー、利用規約                     非常に高い   高い         データの収集、保存、処理など、データの処理方法を説明するための十分な情報が提供されていません。例えば弁護士以外の人でも簡単に理解できるようにしなければなりません。
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   個人データの削除が不十分                       高い         高い         指定された目的の終了後または要求に応じて、個人データを効果的および/またはタイムリーに削除しないことです。
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   不十分なデータ品質                             中           非常に高い   古い、正しくない、または偽の個人データを使用すること、または、データの更新または修正の誤りがあることです。
  P8       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        セッションの有効期限がないか不十分             中           非常に高い   セッションの終了が確実ではないことによって、ユーザーの同意または認識なしに、追加の個人データが収集される可能性があります。
  P9       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   ユーザーがデータにアクセスして変更できない     高い         高い         ユーザーが自分に関連するデータにアクセス、変更、または削除することができません。
  P10      ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          ユーザーの同意を得た目的と異なるデータの収集   高い         高い         システムの目的に関係のない、分析データ、統計データ、またはその他の個人の関連データの収集することや、ユーザーが同意しなかったデータを収集することです。
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------- ------------ ------------ ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Spanish

### Top 10 Riesgos de privacidad (2.0) {#top-10-riesgos-de-privacidad-20}

El tipo determina si un riesgo es
![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji
height="20" width="20"} organizacional ,
![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji
height="20" width="20"} técnico, o ambos.

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------- ---------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Tipo**                                                                                                                                                                                                                                                                                                       **Título**                                                                        **Frecuencia**   **Impacto**   **Descripción**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Vulnerabilidades en aplicaciones web                                              Alto             Muy Alto      La vulnerabilidad es un problema clave en cualquier sistema que protege u opera con datos confidenciales del usuario. Si no se diseña e implementa adecuadamente una aplicación, se detecta un problema o se aplica rápidamente una solución (parche), es probable que se produzca una violación de la privacidad. Este riesgo también abarca la lista de las 10 principales vulnerabilidades de aplicaciones web de OWASP y los riesgos que se derivan de ellas.
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Fuga de datos del lado del operador                                               Alto             Muy Alto      No impedir la filtración de cualquier información que contenga o esté relacionada con los datos del usuario, o los datos en sí, a ninguna parte no autorizada que resulte en la pérdida de confidencialidad de los datos. Introducido ya sea debido a una violación maliciosa intencional o error involuntario, por ejemplo, causado por controles de administración de acceso insuficientes, almacenamiento inseguro, duplicación de datos o falta de conciencia.
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Respuesta insuficiente por filtración de datos                                    Alto             Muy Alto      No informar a las personas afectadas (interesados) sobre una posible violación o fuga de datos, como resultado de eventos intencionales o no intencionales; no remediar la situación arreglando la causa; sin intentar limitar las fugas.
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Consentimiento en todo                                                            Muy Alto         Alto          uso inapropiado del consentimiento para el procesamiento legítimo. El consentimiento está \"en todo\" y no se recopila por separado para cada propósito (por ejemplo, el uso del sitio web y la elaboración de perfiles para publicidad).
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Políticas, términos y condiciones opacas                                          Muy Alto         Alto          No proporcionar suficiente información para describir cómo se procesan los datos, como su recopilación, almacenamiento y procesamiento. No hacer que esta información sea fácilmente accesible y comprensible para las personas que no son abogados.
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Eliminación insuficiente de datos personales                                      Alto             Alto          No eliminar datos personales de manera efectiva y/o oportuna tras la finalización del propósito especificado o previa solicitud.
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Calidad de datos insuficiente                                                     Medio            Muy Alto      El uso de datos de usuario desactualizados, incorrectos o falsos. No actualizar o corregir los datos.
  P8       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Falta o insuficiente mecanismo de expiración de sesión                            Medio            Muy Alto      No cerrar eficazmente la sesión. Puede dar lugar a la recopilación de datos de usuario adicionales sin el consentimiento o el conocimiento del usuario.
  P9       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Imposibilidad de los usuarios para acceder y modificar datos                      Alto             Alto          Los usuarios no tienen la capacidad de acceder, cambiar o eliminar datos relacionados con ellos.
  P10      ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Recopilación de datos no requeridos para el propósito consentido por el usuario   Alto             Alto          Recopilación de datos descriptivos, demográficos o cualquier otro dato relacionado con el usuario que no sean necesarios para los fines de la operación. Se aplica también a los datos para los que el usuario no proporcionó su consentimiento.
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------- ---------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Brazilian Portuguese

### Top 10 riscos de privacidade (2.0) {#top-10-riscos-de-privacidade-20}

O tipo determina se um risco é
![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji
height="20" width="20"} organizacional ,
![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji
height="20" width="20"} técnico ou ambos.

  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------- ---------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Tipo**                                                                                                                                                                                                                                                                                                       **Título**                                                                  **Frequência**   **Impacto**   **Descrição**
  P1       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Vulnerabilidades em aplicações web                                          Alto             Muito Alto    A vulnerabilidade é um problema importante em qualquer sistema que protege ou opera com dados confidenciais do usuário. A falha em projetar e implementar adequadamente um aplicativo, detectar um problema ou aplicar imediatamente uma correção (patch) provavelmente resultará em uma violação de privacidade. Esse risco também abrange a lista do OWASP Top 10 e os seus riscos resultantes.
  P2       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Vazamento de dados pelo lado do operador                                    Alto             Muito Alto    Falha em evitar o vazamento de qualquer informação que contenha ou esteja relacionada aos dados do usuário, ou os próprios dados, para qualquer parte não autorizada, resultando na perda da confidencialidade dos dados. Introduzido devido a violação maliciosa intencional ou erro não intencional, por exemplo causados por controles de gerenciamento de acesso insuficientes, armazenamento inseguro, duplicação de dados ou falta de conscientização.
  P3       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Resposta insuficiente devido ao vazamento de dados                          Alto             Muito Alto    Não informar as pessoas afetadas (titulares dos dados) sobre uma possível violação ou vazamento de dados, resultante de eventos intencionais ou não; falha em remediar a situação corrigindo a causa; não tentando limitar os vazamentos.
  P4       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Consentimento em tudo                                                       Muito Alto       Alto          Agrega��o ou uso impr�prio de consentimento para processamento leg�timo. O consentimento � \"sobre tudo\" e n�o � coletado separadamente para cada finalidade (por exemplo, uso do site e cria��o de perfil para publicidade).
  P5       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          Pol�ticas, termos e condi��es n�o transparentes                             Muito Alto       Alto          N�o fornecendo informa��es suficientes para descrever como os dados s�o processados, como sua coleta, armazenamento e processamento. Falha em tornar essas informa��es facilmente acess�veis e compreens�veis para n�o advogados.
  P6       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Exclus�o insuficiente de dados pessoais                                     Alto             Alto          Falha na exclus�o efetiva e/ou oportuna de dados pessoais ap�s o t�rmino da finalidade especificada ou mediante solicita��o.
  P7       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Qualidade dos dados insuficiente                                            M�dio            Muito Alto    O uso de dados do usu�rio desatualizados, incorretos ou falsos. Falha ao atualizar ou corrigir os dados.
  P8       ![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}                                                                                                                                                        Expira��o de sess�o ausente ou insuficiente                                 M�dio            Muito Alto    Falha em impor o encerramento da sess�o de forma eficaz. Pode resultar na coleta de dados adicionais do usu�rio sem o consentimento ou conhecimento do usu�rio.
  P9       ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}![:woman_technologist:](../../github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bb.png ":woman_technologist:"){.emoji height="20" width="20"}   Incapacidade dos usu�rios de acessar e modificar seus dados                 Alto             Alto          Os usu�rios n�o t�m a capacidade de acessar, alterar ou excluir dados relacionados a eles.
  P10      ![:man_office_worker:](../../github.githubassets.com/images/icons/emoji/unicode/1f468-1f4bc.png ":man_office_worker:"){.emoji height="20" width="20"}                                                                                                                                                          A coleta de dados n�o requeridos para o prop�sito consentido pelo usu�rio   Alto             Alto          Coletar dados descritivos, demogr�ficos ou quaisquer outros dados relacionados ao usu�rio que n�o sejam necess�rios para os prop�sitos do sistema. Aplica-se tamb�m a dados para os quais o usu�rio n�o deu consentimento.
  -------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------- ---------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: {#sec-faqs .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Frequently Asked Questions

### Why is this project only about web applications and not about any kind of software?

Web applications can easily collect data from users without their
permission or without adequately informing them how their data is used.
Cookies, and other trackers, enable the monitoring of user's behaviour,
and this information may be used for a variety of commercial purposes,
including targeted advertising, profiling, and the sale of aggregated
data. Thus, the topic is very important, especially for web
applications.

### Are the Top 10 Privacy Risks applicable for mobile apps as well?

Privacy risks for mobile apps are very similar. The rating might be
slightly different and there might be some additional risks related to
the loss of devices and the use of location data, but in general the Top
10 Privacy Risks are applicable for mobile apps as well.

### What is the difference between this project and the OWASP Top 10?

There are two main differences. First, the OWASP Top 10 describes
technical security risks that are not primarily affecting privacy.
Second, the OWASP Top 10 do not address organisational issues like
privacy notices, profiling, or the sharing of data with third parties.

### Why should companies and other organisations be concerned about privacy risks?

Privacy risks may have serious consequences for an organisation, such
as:

- perceived harm to privacy;
- a failure to meet public expectations on both the use and protection
  of personal information;
- retrospective imposition of regulatory conditions;
- low adoption rates or poor participation in the scheme from both the
  public and partner organisations;
- the costs of redesigning the system or retro-fitting solutions;
- failure of a project or completed system;
- withdrawal of support from key supporting organisations due to
  perceived privacy harms; and/ or
- failure to comply with the law, leading to enforcement action from the
  regulator or compensation claims from individuals.

Source of privacy risks: ICO Handbook on Privacy Impact Assessment (PIA)
:::
:::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-privacy-risks/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-privacy-risks){.github-button
icon="octicon-star" data-size="large" show-count="true"
aria-label="Star on GitHub"}
:::

:::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

### Project Information

- Version 2.0
-  Lab Project
-  Documentation

### Mailing List

- [Join Google
  Group](https://groups.google.com/a/owasp.org/forum/#!forum/top-10-privacy-risks-project/join)

### Timeline

- \[2022\] Countermeasures v2.0 published
- \[2021\] Release of version 2.0
- \[2020\] French Translation available
- \[2015\] German Translation available
- \[2014\] Top 10 Privacy Risks v1.0 published

### External Links

- [Video from OWASP 20th Anniversary Conference (Version
  2.0)](https://youtu.be/MtDHjHiERo8)\
- [Video from panel discussion at CPDP
  2015](https://www.youtube.com/watch?v=6SEdnWlSZyk)\
- [OECD Privacy
  Guidelines](http://www.oecd.org/sti/ieconomy/2013-oecd-privacy-guidelines.pdf)\
- [Internet Privacy Engineering Network -
  IPEN](https://edps.europa.eu/data-protection/ipen-internet-privacy-engineering-network_en)\
- [Check your website with PRIVACYSCORE](https://privacyscore.org/)

### Leaders

- [Florian
  Stahl](../cdn-cgi/l/email-protection.html#ea8c868598838b84c4999e8b8286aa859d8b999ac485988d)
- [Stefan
  Burgmair](../cdn-cgi/l/email-protection.html#3447405152555a1a5641465359555d46745b435547441a5b4653)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::

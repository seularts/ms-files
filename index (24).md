:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Translation
  Efforts](#div-translation_efforts){#translation_efforts-link .tab-link
  role="tab" aria-selected="false" aria-controls="translation_efforts"}
- [Sponsors](#div-sponsors){#sponsors-link .tab-link role="tab"
  aria-selected="false" aria-controls="sponsors"}
- [Data 2025](#div-data_2025){#data_2025-link .tab-link role="tab"
  aria-selected="false" aria-controls="data_2025"}

# OWASP Top Ten {#owasp-top-ten .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## Important note:

### OWASP Top Ten 2025

Current project status as of September 2024:

- We are planning to announce the release of the **OWASP Top 10:2025**
  in the first half of 2025.
- **Data Collection (Now - December 2024)**: Please donate your
  application penetration testing statistics.

[Stay Tuned!](https://www.owasptopten.org/)

------------------------------------------------------------------------

The OWASP Top 10 is a standard awareness document for developers and web
application security. It represents a broad consensus about the most
critical security risks to web applications.

Globally recognized by developers as the first step towards more secure
coding.

Companies should adopt this document and start the process of ensuring
that their web applications minimize these risks. Using the OWASP Top 10
is perhaps the most effective first step towards changing the software
development culture within your organization into one that produces more
secure code.\
\

## Top 10 Web Application Security Risks

There are three new categories, four categories with naming and scoping
changes, and some consolidation in the Top 10 for 2021.

![Mapping](assets/images/mapping.png)

- [**A01:2021-Broken Access
  Control**](../Top10/A01_2021-Broken_Access_Control/index.html) moves
  up from the fifth position; 94% of applications were tested for some
  form of broken access control. The 34 Common Weakness Enumerations
  (CWEs) mapped to Broken Access Control had more occurrences in
  applications than any other category.
- [**A02:2021-Cryptographic
  Failures**](../Top10/A02_2021-Cryptographic_Failures/index.html)
  shifts up one position to #2, previously known as Sensitive Data
  Exposure, which was broad symptom rather than a root cause. The
  renewed focus here is on failures related to cryptography which often
  leads to sensitive data exposure or system compromise.
- [**A03:2021-Injection**](../Top10/A03_2021-Injection/index.html)
  slides down to the third position. 94% of the applications were tested
  for some form of injection, and the 33 CWEs mapped into this category
  have the second most occurrences in applications. Cross-site Scripting
  is now part of this category in this edition.
- [**A04:2021-Insecure
  Design**](../Top10/A04_2021-Insecure_Design/index.html) is a new
  category for 2021, with a focus on risks related to design flaws. If
  we genuinely want to "move left" as an industry, it calls for more use
  of threat modeling, secure design patterns and principles, and
  reference architectures.
- [**A05:2021-Security
  Misconfiguration**](../Top10/A05_2021-Security_Misconfiguration/index.html)
  moves up from #6 in the previous edition; 90% of applications were
  tested for some form of misconfiguration. With more shifts into highly
  configurable software, it's not surprising to see this category move
  up. The former category for XML External Entities (XXE) is now part of
  this category.
- [**A06:2021-Vulnerable and Outdated
  Components**](../Top10/A06_2021-Vulnerable_and_Outdated_Components/index.html)
  was previously titled Using Components with Known Vulnerabilities and
  is #2 in the Top 10 community survey, but also had enough data to make
  the Top 10 via data analysis. This category moves up from #9 in 2017
  and is a known issue that we struggle to test and assess risk. It is
  the only category not to have any Common Vulnerability and Exposures
  (CVEs) mapped to the included CWEs, so a default exploit and impact
  weights of 5.0 are factored into their scores.
- [**A07:2021-Identification and Authentication
  Failures**](../Top10/A07_2021-Identification_and_Authentication_Failures/index.html)
  was previously Broken Authentication and is sliding down from the
  second position, and now includes CWEs that are more related to
  identification failures. This category is still an integral part of
  the Top 10, but the increased availability of standardized frameworks
  seems to be helping.
- [**A08:2021-Software and Data Integrity
  Failures**](../Top10/A08_2021-Software_and_Data_Integrity_Failures/index.html)
  is a new category for 2021, focusing on making assumptions related to
  software updates, critical data, and CI/CD pipelines without verifying
  integrity. One of the highest weighted impacts from Common
  Vulnerability and Exposures/Common Vulnerability Scoring System
  (CVE/CVSS) data mapped to the 10 CWEs in this category. Insecure
  Deserialization from 2017 is now a part of this larger category.
- [**A09:2021-Security Logging and Monitoring
  Failures**](../Top10/A09_2021-Security_Logging_and_Monitoring_Failures/index.html)
  was previously Insufficient Logging & Monitoring and is added from the
  industry survey (#3), moving up from #10 previously. This category is
  expanded to include more types of failures, is challenging to test
  for, and isn't well represented in the CVE/CVSS data. However,
  failures in this category can directly impact visibility, incident
  alerting, and forensics.
- [**A10:2021-Server-Side Request
  Forgery**](../Top10/A10_2021-Server-Side_Request_Forgery_(SSRF)/index.html)
  is added from the Top 10 community survey (#1). The data shows a
  relatively low incidence rate with above average testing coverage,
  along with above-average ratings for Exploit and Impact potential.
  This category represents the scenario where the security community
  members are telling us this is important, even though it's not
  illustrated in the data at this time.
:::

::: {#sec-translation_efforts .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Translation Efforts

Efforts have been made in numerous languages to translate the OWASP Top
10 - 2021. If you are interested in helping, please contact the members
of the team for the language you are interested in contributing to, or
if you don't see your language listed (neither here nor at
[github](https://github.com/OWASP/Top10/issues?utf8=%E2%9C%93&q=is%3Aissue)),
please email
[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
cfemail="711e061002015c051e0105141f311d180205025f1e061002015f1e0316"} to
let us know that you want to help and we'll form a volunteer group for
your language. We have compiled this
[readme](https://github.com/OWASP/Top10/tree/master/2021#translating-the-owasp-top-10-2021)
with some hints to help you with your translation.

### Top10:2021 Completed Translations:

- [**ar - العربية**](../Top10/ar/index.html)
- [**es - Español**](../Top10/es/index.html)
- [**fr - Français**](../Top10/fr/index.html)
- [**id - Indonesian**](../Top10/id/index.html)
- [**it - Italiano**](../Top10/it/index.html)
- [**ja - 日本語\]**](../Top10/ja/index.html)
- [**pt_BR - Português (Brasil)**](../Top10/pt_BR/index.html)
- [**zh_CN - 简体中文**](../Top10/zh_CN/index.html)
- [**zh_TW - 繁體中文**](../Top10/zh_TW/index.html)

## Historic:

### Top10:2017 Completed Translations:

- **Chinese:** [OWASP Top 10-2017 -
  中文版（PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10_2017_%E4%B8%AD%E6%96%87%E7%89%88v1.3.pdf)\
  - 项目组长：[王颉](https://wiki.owasp.org/index.php/User:Jie_Wang)（[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
    cfemail="2255434c4548624d554351520c4d50450c414c"}）
  - 翻译人员：陈亮、王厚奎、王颉、王文君、王晓飞、吴楠、徐瑞祝、夏天泽、杨璐、张剑钟、赵学文（排名不分先后，按姓氏拼音排列）
  - 审查人员：Rip、包悦忠、李旭勤、杨天识、张家银（排名不分先后，按姓氏拼音排列）
  - 汇编人员：赵学文
- **French:** [OWASP Top 10 2017 in French
  (Git/Markdown)](https://github.com/OWASP/Top10/tree/master/2017/fr)
- **German:** [OWASP Top 10 2017 in German V1.0
  (Pdf)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10-2017_de_V1.0.pdf)
  [(web pages)](2017/de/index.html)\
  compiled by Christian Dresen, Alexios Fakos, Louisa Frick, Torsten
  Gigler, Tobias Glemser, Dr. Frank Gut, Dr. Ingo Hanke, Dr. Thomas
  Herzog, Dr. Markus Koegel, Sebastian Klipper, Jens Liebau, Ralf
  Reinhardt, Martin Riedel, Michael Schaefer
- **Hebrew:** [OWASP Top 10-2017 - Hebrew
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP-Top-10-2017-he.pdf) 
  [(PPTX)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP-Top-10-2017-he.pptx)\
  translated by Eyal Estrin (Twitter: \@eyalestrin) and Omer Levi
  Hevroni (Twitter: \@omerlh).
- **Japanese:** [OWASP Top 10-2017 - 日本語版
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10-2017%28ja%29.pdf)\
  translated and reviewed by Akitsugu ITO, Albert Hsieh, Chie TAZAWA,
  Hideko IGARASHI, Hiroshi TOKUMARU, Naoto KATSUMI, Riotaro OKADA,
  Robert DRACEA, Satoru TAKAHASHI, Sen UENO, Shoichi NAKATA, Takanori
  NAKANOWATARI ,Takanori ANDO, Tomohiro SANAE.
- **Korean:** [OWASP Top 10-2017 - 한글
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10-2017-ko.pdf) 
  [(PPTX)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10-2017-ko.pptx)\
  번역 프로젝트 관리 및 감수 : 박형근(Hyungkeun Park) / 감수(ㄱㄴㄷ순) :
  강용석(YongSeok Kang), 박창렴(Park Changryum), 조민재(Johnny Cho) /
  편집 및 감수 : 신상원(Shin Sangwon) / 번역(ㄱㄴㄷ순) : 김영하(Youngha
  Kim), 박상영(Sangyoung Park), 이민욱(MinWook Lee), 정초아(JUNG CHOAH),
  조광렬(CHO KWANG YULL), 최한동(Handong Choi)
- **Portuguese:** [OWASP Top 10 2017 - Portuguese
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10-2017-pt_pt.pdf) [(ODP)](https://github.com/OWASP/Top10/raw/master/2017/OWASP%20Top%2010-2017-pt_pt.odp)\
  translated by Anabela Nogueira, Carlos Serrão, Guillaume Lopes, João
  Pinto, João Samouco, Kembolle A. Oliveira, Paulo A. Silva, Ricardo
  Mourato, Rui Silva, Sérgio Domingues, Tiago Reis, Vítor Magano.
- **Russian:** [OWASP Top 10-2017 - на русском языке
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP%20Top%2010-2017-ru.pdf)\
  translated and reviewed by JZDLin
  ([\@JZDLin](https://github.com/JZDLin)), Oleksii Skachkov
  ([\@hamster4n](https://github.com/hamster4n)), Ivan Kochurkin
  ([\@KvanTTT](https://github.com/KvanTTT)) and [Taras
  Ivashchenko](https://wiki.owasp.org/index.php/User:Taras_Ivashchenko)
- **Spanish:** [OWASP Top 10-2017 - Español
  (PDF)](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP-Top-10-2017-es.pdf)\
  - [Gerardo
    Canedo](https://wiki.owasp.org/index.php/User:Gerardo_Canedo)（[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
    cfemail="66210314071402094825070803020926091107151648091401"} -
    \[Twitter: \@GerardoMCanedo\])
  - [Cristian
    Borghello](https://wiki.owasp.org/index.php/User:Cristian_Borghello)（[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
    cfemail="f2b1809b81869b939cdcb09d80959a979e9e9db29d85938182dc9d8095"} -
    \[Twitter: \@seguinfo\])

### Top10:2017 Release Candidate Translation Teams:

- Azerbaijanian: Rashad Aliyev
  ([\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="3c4e5d4f545d587c5d5055594a1255525a53"})
- Chinese
  RC2:Rip、包悦忠、李旭勤、王颉、王厚奎、吴楠、徐瑞祝、夏天泽、张家银、张剑钟、赵学文(排名不分先后，按姓氏拼音排列)
  [OWASP Top10 2017 RC2 - Chinese
  PDF](https://www.owasp.org/images/d/d6/OWASP_Top_10_2017（RC2）中文版（发布版）.pdf)
- French: Ludovic Petit:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="9cd0e9f8f3eaf5ffb2ccf9e8f5e8dcf3ebfdefecb2f3eefb"}, Sébastien
  Gioria:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="a1f2c4c3c0d2d5c8c4cf8fe6c8ced3c8c0e1ced6c0d2d18fced3c6"}.
- Others to be listed.

### Top10:2013 Completed Translations:

- Arabic: [OWASP Top 10 2013 - Arabic
  PDF](https://www.owasp.org/images/6/6a/OWASP_TOP_10_2013_Arabic.pdf)\
  Translated by: Mohannad Shahat:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="25684a4d444b4b44410b764d444d4451654a524456550b4a5742"},
  Fahad: \@SecurityArk, Abdulellah Alsaheel:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="85e6f6abf6e4ede0e0e9c5e2e8e4ece9abe6eae8"}, Khalifa Alshamsi:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e0ab8893d1d6d1d8a0878d81898cce838f8d"} and Sabri(KING SABRI):
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="6d0604030a431e0c0f1f042d0a000c0401430e0200"}, Mohammed
  Aldossary:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="127f7d7a737f7f77763c737e767d616173606b527d657361623c7d6075"}
- Chinese 2013：中文版2013 [OWASP Top 10 2013 - Chinese
  (PDF)](https://www.owasp.org/images/5/51/OWASP_Top_10_2013-Chinese-V1.2.pdf).\
  项目组长： Rip、王颉， 参与人员： 陈亮、 顾庆林、 胡晓斌、 李建蒙、
  王文君、 杨天识、 张在峰
- Czech 2013: [OWASP Top 10 2013 - Czech
  (PDF)](https://www.owasp.org/images/f/f3/OWASP_Top_10_-_2013_Final_-_Czech_V1.1.pdf)
  [OWASP Top 10 2013 - Czech
  (PPTX)](https://www.owasp.org/images/0/02/OWASP_Top_10_-_2013_Final_-_Czech_V1.1.pptx)\
  CSIRT.CZ - CZ.NIC, z.s.p.o. (.cz domain registry): Petr Zavodsky:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1b6b7e6f6935617a6d747f6870625b746c7a686b3574697c"}, Vaclav
  Klimes, Zuzana Duracinska, Michal Prokop, Edvard Rejthar, Pavel Basta
- French 2013: [OWASP Top 10 2013 - French
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202013%20-%20French.pdf)\
  Ludovic Petit:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="cc80b9a8a3baa5afe29ca9b8a5b88ca3bbadbfbce2a3beab"}, Sébastien
  Gioria:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="570432353624233e323979103e38253e3617382036242779382530"},
  Erwan Abgrall:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1770237b2373657e7a57707a767e7b3974787a"}, Benjamin Avet:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e183848f8b808c888fcf80978495a1868c80888dcf828e8c"}, Jocelyn
  Aubert:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e983868a8c859087c7889c8b8c9b9da9869e889a99c7869b8e"}, Damien
  Azambour:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5b3f3a36323e35753a213a3639342e293c1b342c3a282b7534293c"},
  Aline Barthelemy:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="6b0a0702050e45090a191f030e070e06122b0d19450a090945080406"},
  Moulay Abdsamad Belghiti:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5b3a393f283a363a3f75393e373c33322f321b3c363a323775383436"},
  Gregory Blanc:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="375045525058454e19555b56595477505a565e5b1954585a"}, Clément
  Capel:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="71121d141c141f055f121001141d310217035f121e1c"}, Etienne
  Capgras:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="90d5e4f9f5fefef5bef3f1e0f7e2f1e3d0e3fffce5f3fffdbef6e2"},
  Julien Cayssol:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="6208170e0b070c22031315184c010d0f"}, Antonio Fontes:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e687889289888f89c8808988928395a68991879596c8899481"}, Ely de
  Travieso:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="6520091c4b0100111704130c00160a250a120416154b0a1702"}, Nicolas
  Grégoire:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d0beb9b3bfbcb1a3feb7a2b5b7bfb9a2b590b1b7b1a2a2b9feb6a2"},
  Valérie Lasserre:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d3a5b2bfb6a1bab6fdbfb2a0a0b6a1a1b693b4beabfdb5a1"}, Antoine
  Laureau:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1a7b746e7573747f34767b6f687f7b6f5a756d7b696a3475687d"},
  Guillaume Lopes:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="c7aba8b7a2b4e9a0b2aeababa6b2aaa287a1b5a2a2e9a1b5"}, Gilles
  Morain:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="0b6c6267676e78256664796a62654b6c666a626725686466"},
  Christophe Pekar:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5b38332932282f342b333e752b3e303a291b342c3a282b7534293c"},
  Olivier Perret:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="29594c5b5b4c5d5a694f5b4c4c074f5b"}, Michel Prunet:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="4e23272d262b22603e3c3b202b3a0e21392f3d3e60213c29"}, Olivier
  Revollat:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="621007140d0e0e031622050f030b0e4c010d0f"}, Aymeric Tabourin:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="3a5b43575f485359144e5b58554f4853547a55485b545d5f14595557"}
- German 2013: [OWASP Top 10 2013 - German
  PDF](https://wiki.owasp.org/?title=Special:Redirect/file/OWASP_Top_10_2013_DE_Version_1_0.pdf)\
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="13677c632223537c647260633d7776"} which is Frank Dölitzscher,
  Torsten Gigler, Tobias Glemser, Dr. Ingo Hanke, Thomas Herzog, [Kai
  Jendrian](https://wiki.owasp.org/index.php/User:Kai_Jendrian), [Ralf
  Reinhardt](https://wiki.owasp.org/index.php/User:Ralf_Reinhardt),
  Michael Schäfer
- Hebrew 2013: [OWASP Top 10 2013 -
  Hebrew](https://wiki.owasp.org/index.php/OWASP_Top10_Hebrew)
  [PDF](https://www.owasp.org/images/1/1b/OWASP_Top_10_2013-Hebrew.pdf)\
  Translated by: Or Katz, Eyal Estrin, Oran Yitzhak, Dan Peled, Shay
  Sivan.
- Italian 2013: [OWASP Top 10 2013 - Italian
  PDF](https://www.owasp.org/images/c/c9/OWASP_Top_10_-_2013_-_Italiano.pdf)\
  Translated by: Michele Saporito:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="44296a3725342b362d302b73042329252d286a272b29"}, Paolo Perego:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="ccb8a4a9bfbcfca2aba98ca3bbadbfbce2a3beab"}, Matteo Meucci:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="7815190c0c1d1756151d0d1b1b1138170f190b0856170a1f"}, Sara
  Gallo:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="84f7e5f6e5aae3e5e8e8ebc4e3e9e5ede8aae7ebe9"}, Alessandro
  Guido:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2b4a474e536b584e485e59425f524a4f4f42485f4e4f05484446"}, Mirko
  Guido Spezie:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="deb3b7acb5b19ebabfa7abf0b7aa"}, Giuseppe Di Cesare:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2b4c425e584e5b5b4e054f42484e584a594e6b4a4742484e05425f"},
  Paco Schiaffella:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="7407171c1d15121211181815341319151d185a171b19"}, Gianluca
  Grasso:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="cfa8a6aea1aba0ba8fa8a2aea6a3e1aca0a2"}, Alessio D'Ospina:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5a3b363f292933353e35291a3d373b333674393537"}, Loredana
  Mancini:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="7c10130e19181d121d52111d121f1512153c1e090f1512190f0f5119521508"},
  Alessio Petracca:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="bddcd1d8ceced4d293cdd8c9cfdcdededcfddad0dcd4d193ded2d0"},
  Giuseppe Trotta:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="187f716d6c6a776c6c79587f75797174367b7775"}, Simone Onofri:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d8abb1b5b7b6bdf6b7b6b7beaab198bfb5b9b1b4f6bbb7b5"}, Francesco
  Cossu:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e98188848b9c8a828c9ba98e84888085c78a8684"}, Marco Lancini:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="6e030f1c0d0140020f000d0700074003022e09030f0702400d0103"},
  Stefano Zanero:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d0aab1beb5a2bf90b5bcb5a4fea0bfbcb9bdb9feb9a4"}, Giovanni
  Schmid:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="dabdb3b5acbbb4b4b3f4a9b9b2b7b3be9ab4bbf4b3b9bba8f4b9b4a8f4b3ae"},
  Igor Falcomata':
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="93f8fcf1f2d3e0faf8e6e1f6e9e9f2bdfce1f4"}
- Japanese 2013: [OWASP Top 10 2013 - Japanese
  PDF](https://www.owasp.org/images/7/79/OWASP_Top_10_2013_JPN.pdf)\
  Translated by: Chia-Lung Hsieh: ryusuke.tw(at)gmail.com, Reviewed by:
  Hiroshi Tokumaru, Takanori Nakanowatari
- Korean 2013: [OWASP Top 10 2013 - Korean
  PDF](https://www.owasp.org/images/2/2c/OWASP_Top_10_-_2013_Final_-_Korean.pdf)
  (이름가나다순)\
  김병효:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2a4853455f444d425345044143476a455d4b595a0445584d"},
  김지원:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="167c7f617978387d7f7b567961776566387964387d64"},
  김효근:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2e454f5a5b5c476e454f5a5b5c4700455c"},
  박정훈:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5129343d383e3f11363c30383d7f323e3c"},
  성영모:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2e57415b40494341005d4b4140496e41594f5d5e00415c00455c"},
  성윤기:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="84fdf1eae1aaf7f1eae3c4ebf3e5f7f4aaebf6e3"},
  송보영:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d5b7baacbaa0bbb2fba6babbb295baa2b4a6a5fbbaa7fbbea7"},
  송창기:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e0868183948f92d7a08e81968592ce838f8d"},
  유정호:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="dabda8b3aab2b3a9eded9abdb7bbb3b6f4b9b5b7"},
  장상민:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2d5e4c434a40444303474c434a6d425a4c5e5d03425f03465f"},
  전영재:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="ef96809a8188858e8ac1858a8081af80988e9c9fc1809d88"},
  정가람:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="790d1e1a180b0b160d391e14181015571a1614"},
  정홍순:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="adc7c5de9a9f95edcac0ccc4c183cec2c0"},
  조민재:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="88e2e7e0e6e6f1a6ebe0e7c8e7ffe9fbf8a6e7faef"},허성무:[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="ee879d9d87839e828b808b9aae89838f8782c08d8183"}
- Brazilian Portuguese 2013: [OWASP Top 10 2013 - Brazilian Portuguese
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP_Top_10_-_2013_Brazilian_Portuguese.pdf)\
  Translated by: Carlos Serrão, Marcio Machry, Ícaro Evangelista de
  Torres, Carlo Marcelo Revoredo da Silva, Luiz Vieira, Suely Ramalho de
  Mello, Jorge Olímpia, Daniel Quintão, Mauro Risonho de Paula
  Assumpção, Marcelo Lopes, Caio Dias, Rodrigo Gularte
- Spanish 2013: [OWASP Top 10 2013 - Spanish
  PDF](https://www.owasp.org/images/5/5f/OWASP_Top_10_-_2013_Final_-_Español.pdf)\
  Gerardo Canedo:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e58280978497818acb86848b80818aa58a92849695cb8a9782"}, Jorge
  Correa:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2c464d4f435e5e494d416c4b414d4540024f4341"}, Fabien Spychiger:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d6b0b7b4bfb3b8f8a5a6afb5bebfb1b3a496b2a4b3b7bbbab7b4f8b8b3a2"},
  Alberto Hill:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="23424f414651574c0d47424d4a464f0d4b4a4f4f63444e424a4f0d404c4e"},
  Johnatan Stanley:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5933363137382d38372a2d193e34383035773a3634"}, Maximiliano
  Alonzo:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1875797477766277586c717a367b7775366d61"}, Mateo Martinez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="4e232f3a2b2160232f3c3a27202b340e21392f3d3e60213c29"}, David
  Montero:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="4e2a2f38272a602321203a2b3c210e21392f3d3e60213c29"}, Rodrigo
  Martinez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d5a7bab1b8b4a7a195b3bcbbb2fbb0b1a0fba0ac"}, Guillermo
  Skrilec:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="b9deccd0d5d5dccbd4d697cad2cbd0d5dcdaf9d6ced8cac997d6cbde"},
  Felipe Zipitria:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="7016151c1900155e0a19001904021911301f071103005e1f0217"},
  Fabien Spychiger:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="9dfbfcfff4f8f3b3eeede4fef5f4faf8efddf9eff8fcf0f1fcffb3f3f8e9"},
  Rafael Gil:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="7301121512161f5d141a1f1f12011a1c00331c041200035d1c0114"},
  Christian Lopez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="56353e243f25223f3738783a3926332c783b3724223f3816392137252678392431"},
  jonathan fernandez
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="d3b9bcbdb2a7bbb2bdfdb5b6a1bdb2bdb7b6a9e3e793b4beb2babffdb0bcbe"},
  Paola Rodriguez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="5000313f3c310f02611026352239363f3e357e333f3d"}, Hector
  Aguirre:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="0e666b6d7a617c206f607a61606761206f697b677c7c6b4e61796f7d7e20617c69"},
  Roger Carhuatocto:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="aedccdcfdcc6dbcfdac1cddac1eec7c0dac7d680c7c0c8c1"}, Juan
  Carlos Calderon:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="402a2f282e232332003921282f2f6e232f2d"}, Marc Rivero López:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="c7aab5aeb1a2b5a8aba8b7a2bd87a0aaa6aeabe9a4a8aa"}, Carlos
  Allendes:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e5868497898a96cb848989808b818096a58a92849695cb8a9782"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="badedbd4d3dfd6fad9dbc8c8dfc8d594d9d6"}:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="3a5e5b54535f567a595b48485f4855145956"}, Manuel Ramírez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="472a262932222b6935262a2e35223d693407202a262e2b6924282a"},
  Marco Miranda:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="076a66756468296a6e756669636647687066747729687560"},
  Mauricio D. Papaleo Mayada:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2b465b4a5b4a474e446b4c464a424705484446"}, Felipe Sanchez:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="92f4f7fefbe2f7bce1f3fcf1faf7e8d2e2f7e0fbe6f3f8f7e1fbfcf4fde0fff3e6fbf1fde1bcf1fe"},
  Juan Manuel Bahamonde:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="4e243b2f20232f203b2b22602c2f262f2321202a2b0e29232f2722602d2123"},
  Adrià Massanet:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1f7e7b6d767e727e6c6c7e717a6b5f78727e7673317c7072"}, Jorge
  Correa:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="345e55575b4646515559745359555d581a575b59"}, Ramiro Pulgar:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="354754585c475a1b454059525447755a425446451b5a4752"}, German
  Alonso Suárez Guerrero:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="0a6d6f78676b6424797f6b786f704a657d6b797a2465786d"}, Jose A.
  Guasch:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="62080305170311010a22050f030b0e4c010d0f"}, Edgar Salazar:
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="bcd9d8dbddce92cfddd0ddc6ddcefcd3cbddcfcc92d3cedb"}
- Ukrainian 2013: [OWASP Top 10 2013 - Ukrainian
  PDF](https://www.owasp.org/images/e/e3/OWASP_Top_10_-_2013_Final_Ukrainian.pdf)\
  Kateryna Ovechenko, Yuriy Fedko, Gleb Paharenko, Yevgeniya Maskayeva,
  Sergiy Shabashkevich, Bohdan Serednytsky

### 2010 Completed Translations: {#2010-completed-translations}

- Korean 2010: [OWASP Top 10 2010 - Korean
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202010%20Korean.pdf)\
  Hyungkeun Park,
  ([\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="b1dcd8c3c3da80f1d6dcd0d8dd9fd2dedc"})
- Spanish 2010: [OWASP Top 10 2010 - Spanish
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202010%20Spanish.pdf)\
  Daniel Cabezas Molina, Edgar Sanchez, Juan Carlos Calderon, Jose
  Antonio Guasch, Paulo Coronado, Rodrigo Marcos, Vicente Aguilera
- French 2010: [OWASP Top 10 2010 - French
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202010%20French.pdf)\
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="ea869f8e859c8389c49a8f9e839eaa859d8b999ac485988d"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="1162747370626578747f3f76787e637870517e667062613f7e6376"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="e988879d86878086c78f86879d8c9aa9869e889a99c7869b8e"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="3e5c5b5051574a10594b5b4c5b4a4a5b7e51495f4d4e10514c59"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="a5efcac6c0c9dccb8bc4d0c7c0d7d1e5cad2c4d6d58bcad7c2"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="2267504b410c654350504743576245474f434e564d0c414d4f"},
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="ebac9e8287878a9e868ec5a39e9298868a8598ab8c8e868a879f84c5888486"}
- German 2010: [OWASP Top 10 2010 - German
  PDF](https://wiki.owasp.org/?title=Special:Redirect/file/OWASPTop10_2010_DE_Version_1_0.pdf)\
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="50243f206160103f273123207e3435"} which is Frank Dölitzscher,
  Tobias Glemser, Dr. Ingo Hanke, [Kai
  Jendrian](https://wiki.owasp.org/index.php/User:Kai_Jendrian), [Ralf
  Reinhardt](https://wiki.owasp.org/index.php/https://wiki.owasp.org/index.php/User:Ralf_Reinhardt),
  Michael Schäfer
- Indonesian 2010: [OWASP Top 10 2010 - Indonesian
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202010%20Indonesian.pdf)\
  Tedi Heriyanto (coordinator), Lathifah Arief, Tri A Sundara, Zaki
  Akhmad
- Italian 2010: [OWASP Top 10 2010 - Italian
  PDF](https://www.owasp.org/images/f/f9/OWASP_Top_10_-_2010_ITA.pdf)\
  Simone Onofri, Paolo Perego, Massimo Biagiotti, Edoardo Viscosi,
  Salvatore Fiorillo, Roberto Battistoni, Loredana Mancini, Michele
  Nesta, Paco Schiaffella, Lucilla Mancini, Gerardo Di Giacomo,
  Valentino Squilloni
- Japanese 2010: [OWASP Top 10 2010 - Japanese
  PDF](https://torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASP%20Top%2010%20-%202010%20Japanese-A4.pdf)\
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="630006000a0f4d1016230c140210134d0c1104"}, Dr. Masayuki
  Hisada, Yoshimasa Kawamoto, Ryusuke Sakamoto, Keisuke Seki, Shin
  Umemoto, Takashi Arima
- Chinese 2010: [OWASP Top 10 2010 - Chinese
  PDF](https://www.owasp.org/images/a/a9/OWASP_Top_10_2010_Chinese_V1.0_Released.pdf)\
  感谢以下为中文版本做出贡献的翻译人员和审核人员: Rip Torn, 钟卫林,
  高雯, 王颉, 于振东
- Vietnamese 2010: [OWASP Top 10 2010 - Vietnamese
  PDF](torage.googleapis.com/google-code-archive-downloads/v2/code.google.com/owasptop10/OWASPTop%2010%20-%202010%20Vietnamese.html)\
  Translation lead by Cecil Su - Translation Team: Dang Hoang Vu, Nguyen
  Ba Tien, Nguyen Tang Hung, Luong Dieu Phuong, Huynh Thien Tam
- Hebrew 2010: [OWASP Top 10 Hebrew
  Project](https://wiki.owasp.org/index.php/OWASP_Top10_Hebrew) --
  [OWASP Top 10 2010 - Hebrew
  PDF](https://www.owasp.org/images/c/cd/OWASP_Top_10_Heb.pdf).\
  Lead by Or Katz, see translation page for list of contributors.
:::

::: {#sec-sponsors .section .page-body .tab-hidden}

------------------------------------------------------------------------

## 2021 Project Sponsors {#2021-project-sponsors}

The OWASP Top 10:2021 is sponsored by Secure Code Warrior.

[![Secure Code
Warrior](assets/images/securecodewarrior.png)](https://securecodewarrior.com/)

## 2017 Project Sponsors {#2017-project-sponsors}

The OWASP Top 10 - 2017 project was sponsored by Autodesk, and supported
by the [OWASP NoVA
Chapter](../www-chapter-northern-virginia/index.html).

![Autodesk](assets/images/autodesk.png)

## 2003-2013 Project Sponsors {#2003-2013-project-sponsors}

Thanks to [Aspect
Security](https://www.aspectsecurity.com/){target="_blank"} for
sponsoring earlier versions.
:::

::: {#sec-data_2025 .section .page-body .tab-hidden}

------------------------------------------------------------------------

# OWASP Top 10 2025 Data Analysis Plan

## Goals

To collect the most comprehensive dataset related to identified
application vulnerabilities to-date to enable analysis for the Top 10
and other future research as well. This data should come from a variety
of sources; security vendors and consultancies, bug bounties, along with
company/organizational contributions. Data will be normalized to allow
for level comparison between Human assisted Tooling and Tooling assisted
Humans.

\

## Analysis Infrastructure

Plan to leverage the OWASP Azure Cloud Infrastructure to collect,
analyze, and store the data contributed.

\

## Contributions

We plan to support both known and pseudo-anonymous contributions. The
preference is for contributions to be known; this immensely helps with
the validation/quality/confidence of the data submitted. If the
submitter prefers to have their data stored anonymously and even go as
far as submitting the data anonymously, then it will have to be
classified as "unverified" vs. "verified".

### Verified Data Contribution

Scenario 1: The submitter is known and has agreed to be identified as a
contributing party.\
Scenario 2: The submitter is known but would rather not be publicly
identified.\
Scenario 3: The submitter is known but does not want it recorded in the
dataset.\

### Unverified Data Contribution

Scenario 4: The submitter is anonymous. (Should we support?)

The analysis of the data will be conducted with a careful distinction
when the unverified data is part of the dataset that was analyzed.

\

## Contribution Process

There are a few ways that data can be contributed:

1.  Email a CSV/Excel file with the dataset(s) to
    [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
    cfemail="5436263d353a7a33383527143b233527247a3b2633"}
2.  Upload a CSV/Excel file to <https://bit.ly/OWASPTop10Data>

Template examples can be found in GitHub:
<https://github.com/OWASP/Top10/tree/master/2024/Data>

\

## Contribution Period

We plan to accept contributions to the new Top 10 until Dec 31, 2024 for
data dating from 2021 to current.

\

## Data Structure

The following data elements are **required** or optional.\
The more information provided the more accurate our analysis can be.\
At a bare minimum, we need the time period, total number of applications
tested in the dataset, and the list of CWEs and counts of how many
applications contained that CWE.\
If at all possible, please provide the additional metadata, because that
will greatly help us gain more insights into the current state of
testing and vulnerabilities.\

### Metadata

- Contributor Name (org or anon)\
- Contributor Contact Email\
- **Time period (2024, 2023, 2022, 2021)**\
- **Number of applications tested**\
- Type of testing (TaH, HaT, Tools)\
- Primary Language (code)\
- Geographic Region (Global, North America, EU, Asia, other)\
- Primary Industry (Multiple, Financial, Industrial, Software, ??)\
- Whether or not data contains retests or the same applications multiple
  times (T/F)\

### CWE Data

- **A list of CWEs w/ count of applications found to contain that CWE**\

*If at all possible, please provide core CWEs in the data, not CWE
categories.*\
*This will help with the analysis, any normalization/aggregation done as
a part of this analysis will be well documented.*

#### Note:

If a contributor has two types of datasets, one from HaT and one from
TaH sources, then it is recommended to submit them as two separate
datasets.\
*HaT = Human assisted Tools (higher volume/frequency, primarily from
tooling)*\
*TaH = Tool assisted Human (lower volume/frequency, primarily from human
testing)*\

\

## Survey

Similarly to the Top Ten 2021, we plan to conduct a survey to identify
up to two categories of the Top Ten that the community believes are
important, but may not be reflected in the data yet. We plan to conduct
the survey in early 2025, and will be utilizing Google forms in a
similar manner as last time. The CWEs on the survey will come from
current trending findings, CWEs that are outside the Top Ten in data,
and other potential sources.

\

## Process

At a high level, we plan to perform a level of data normalization;
however, we will keep a version of the raw data contributed for future
analysis. We will analyze the CWE distribution of the datasets and
potentially reclassify some CWEs to consolidate them into larger
buckets. We will carefully document all normalization actions taken so
it is clear what has been done.

We plan to calculate likelihood following the model we continued in 2021
to determine incidence rate instead of frequency to rate how likely a
given app may contain at least one instance of a CWE. This means we
aren't looking for the frequency rate (number of findings) in an app,
rather, we are looking for the number of applications that had one or
more instances of a CWE. We can calculate the incidence rate based on
the total number of applications tested in the dataset compared to how
many applications each CWE was found in.

In addition, we will be developing base CWSS scores for the top 20-30
CWEs and include potential impact into the Top 10 weighting.

Also, would like to explore additional insights that could be gleaned
from the contributed dataset to see what else can be learned that could
be of use to the security and development communities.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-ten/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-ten){.github-button
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

- • [OWASP Top 10:2021](../Top10/index.html)
- • [Making of OWASP Top 10](https://www.owasptopten.org/)
- • [OWASP Top 10:2021 - 20th Anniversary Presentation
  (PPTX)](https://github.com/OWASP/Top10/raw/master/2021/Presentations/20th%20Anniversary%20-%20OWASP%20Top%2010%202021.pptx)
- [Flagship Project]{style="font-size:1.0em;padding-left:12px;"}
- [Documentation]{style="font-size:1.0em;padding-left:12px;"}
- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}
- • [Previous Version (2017)](2017/index.html)

### Downloads or Social Links

- • [OWASP Top 10
  2017](https://ubiquitous-adventure-gnwnz4m.pages.github.io/OWASP_Top_10-2017_(en).pdf.pdf){target="_blank"
  rel="noopener"}
- • [Other languages → tab 'Translation
  Efforts'](index.html#div-translation_efforts)

### Social

- [Twitter](https://twitter.com/owasptop10)

### Code Repository

- [repo](https://github.com/OWASP/Top10){target="_blank" rel="noopener"}

### Leaders

- [Andrew van der
  Stock](../cdn-cgi/l/email-protection.html#acdacdc2c8c9decdc6ecc3dbcddfdc82c3decb)
- [Brian
  Glas](../cdn-cgi/l/email-protection.html#4e2c3c272f206029222f3d0e21392f3d3e60213c29)
- [Neil
  Smithline](../cdn-cgi/l/email-protection.html#adc3c8c4c183dec0c4d9c5c1c4c3c8edc2daccdedd83c2dfca)
- [Torsten
  Gigler](../cdn-cgi/l/email-protection.html#e2968d909196878ccc858b858e8790a28d95839192cc8d9085)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::

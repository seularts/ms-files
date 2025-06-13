::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Acknowledgements](#div-acknowledgements){#acknowledgements-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgements"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [OWASP-2023](#div-owasp_archive){#owasp_archive-link .tab-link
  role="tab" aria-selected="false" aria-controls="owasp_archive"}

# OWASP Smart Contract Top 10 {#owasp-smart-contract-top-10 .page-title}

:::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![OWASP Smart Contract Logo](assets/images/owasp-sctop10.png)

## About the Smart Contract Top 10

The OWASP Smart Contract Top 10 (2025) is a standard awareness document
providing Web3 developers and security teams with insights into the top
10 vulnerabilities found in smart contracts.

It serves as a reference to ensure that smart contracts are secured
against the most critical weaknesses exploited or discovered in recent
years. The **Smart Contract Top 10** can be used alongside other smart
contract security projects to ensure comprehensive risk coverage. Visit
[scs.owasp.org](https://scs.owasp.org/) for more details on OWASP Smart
Contract Security Projects.

## Changes

![OWASP 2023 to 2025 Changes](assets/images/Mapping2023-2025.png)

### Top 10

- SC01:2025 - [Access Control
  Vulnerabilities](2025/en/src/SC01-access-control.html)
- SC02:2025 - [Price Oracle
  Manipulation](2025/en/src/SC02-price-oracle-manipulation.html)
- SC03:2025 - [Logic Errors](2025/en/src/SC03-logic-errors.html)
- SC04:2025 - [Lack of Input
  Validation](2025/en/src/SC04-lack-of-input-validation.html)
- SC05:2025 - [Reentrancy
  Attacks](2025/en/src/SC05-reentrancy-attacks.html)
- SC06:2025 - [Unchecked External
  Calls](2025/en/src/SC06-unchecked-external-calls.html)
- SC07:2025 - [Flash Loan
  Attacks](2025/en/src/SC07-flash-loan-attacks.html)
- SC08:2025 - [Integer Overflow and
  Underflow](2025/en/src/SC08-integer-overflow-underflow.html)
- SC09:2025 - [Insecure
  Randomness](2025/en/src/SC09-insecure-randomness.html)
- SC10:2025 - [Denial of Service (DoS)
  Attacks](2025/en/src/SC10-denial-of-service.html)

### Overview

  Title                                    Description
  ---------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  SC01 - Access Control Vulnerabilities    Access control flaws allow unauthorized users to access or modify a contract's data or functions. These vulnerabilities arise when the code fails to enforce proper permission checks, potentially leading to severe security breaches.
  SC02 - Price Oracle Manipulation         Price Oracle Manipulation exploits vulnerabilities in how smart contracts fetch external data. By tampering with or controlling oracle feeds, attackers can affect contract logic, leading to financial losses or system instability.
  SC03 - Logic Errors                      Logic errors, or business logic vulnerabilities, occur when a contract's behavior deviates from its intended functionality. Examples include incorrect reward distribution, token minting issues, or flawed lending/borrowing logic.
  SC04 - Lack of Input Validation          Insufficient input validation can lead to vulnerabilities where an attacker may manipulate the contract by providing harmful or unexpected inputs, potentially breaking logic or causing unexpected behaviors.
  SC05 - Reentrancy Attacks                Reentrancy attacks exploit the ability to reenter a vulnerable function before its execution is complete. This can lead to repeated state changes, often resulting in drained contract funds or broken logic.
  SC06 - Unchecked External Calls          Failing to verify the success of external function calls can result in unintended consequences. When a called contract fails, the calling contract may incorrectly proceed, risking integrity and functionality.
  SC07 - Flash Loan Attacks                Flash loans, while useful, can be exploited to manipulate protocols by executing multiple actions in a single transaction. These attacks often result in drained liquidity, altered prices, or exploited business logic.
  SC08 - Integer Overflow and Underflow    Arithmetic errors due to exceeding the limits of fixed-size integers can lead to serious vulnerabilities, such as incorrect calculations or token theft. Unsigned integers wrap around on underflow, while signed integers flip between extremes.
  SC09 - Insecure Randomness               Due to the deterministic nature of blockchain networks, generating secure randomness is challenging. Predictable or manipulable randomness can lead to exploitation in lotteries, token distributions, or other randomness-dependent functionalities.
  SC10 - Denial of Service (DoS) Attacks   DoS attacks exploit vulnerabilities to exhaust contract resources, rendering it non-functional. Examples include excessive gas consumption in loops or function calls designed to disrupt normal contract operation.

## Data Sources

### SolidityScan's Web3HackHub:

To identify and validate the OWASP Smart Contract Top 10
vulnerabilities, we incorporated insights from multiple authoritative
sources, with a notable focus on **[SolidityScan's
Web3HackHub](https://solidityscan.com/web3hackhub?year=2024) (2024)**.
This resource provides a comprehensive database of blockchain-related
incidents, offering valuable data on attack vectors, financial losses,
and trends.

Web3HackHub documents breaches from 2011 onward, enabling analysis of
evolving attack methods, the increasing sophistication of exploits, and
lessons learned from each incident.

**Key highlights from Web3HackHub for 2024 include:**

- Total Financial Impact: \$1.42 billion lost across 149 documented
  incidents in 2024.

- Top Attack Vectors (by frequency, total losses):

  - Access Control Vulnerabilities: \$953.2M in losses.
  - Logic Errors: \$63.8M in losses.
  - Reentrancy Attacks: \$35.7M in losses.
  - Flash Loan Attacks: \$33.8M in losses.
  - Lack of Input Validation: \$14.6M in losses.
  - Price Oracle Manipulation: \$8.8M in losses.
  - Unchecked External Calls: \$550.7K in losses.

[![web3hackhub](assets/images/web3hackhub-snap.png)](https://solidityscan.com/web3hackhub)

### Other Sources:

In addition to SolidityScan's Web3HackHub, incorporating insights from
[Peter Kacherginsky's "Top 10 DeFi Attack Vectors -
2024"](https://x.com/_iphelix/status/1855855006219690233) provides
valuable data for creating the OWASP Smart Contract Top 10 for 2025.
Peter's analysis is instrumental in understanding the evolving threat
landscape and aligning the OWASP Smart Contract Top 10 with real-world
observations.

By integrating data from both SolidityScan's Web3HackHub and
Kacherginsky's "Top 10 DeFi Attack Vectors - 2024," we were able to
provide a well-rounded justification for the 2025 rankings.

After analyzing **149 security incidents from SolidityScan's Web3HackHub
(2024)**, **Peter Kacherginsky's "Top 10 DeFi Attack Vectors - 2024"**,
and the **[Immunefi Crypto Losses in 2024
Report](https://downloads.ctfassets.net/t3wqy70tc3bv/2LqNkvjajiCS5sPJmWLakc/9715af967dd95a55da05d2ad373edb0d/Immunefi_Crypto_Losses_in_2024_Report.pdf)**,
which collectively document over **\$1.42 billion in financial losses
across decentralized ecosystems**, the **OWASP Smart Contract Top 10 for
2025** was created to address the most critical vulnerabilities in the
blockchain and smart contract ecosystem.

## Licensing

The OWASP Smart Contract Top 10 (2025) is
[licensed](https://github.com/OWASP/www-project-smart-contract-top-10/blob/8083e976d6d18013dce2d5e6e62f98e632151a09/LICENSE.md)
under the [CC BY-NC-SA
4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/), the Creative
Commons Attribution-ShareAlike 4.0 license. Some rights reserved.

![license](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc-sa.svg)

## Project Leaders

- [Jinson Varghese
  Behanan](../cdn-cgi/l/email-protection.html#107a797e637f7e507f677163603e7f6277)
  (Twitter: [\@JinsonCyberSec](https://x.com/JinsonCyberSec))
- [Shashank](../cdn-cgi/l/email-protection.html#e99a81889a81888782a98a9b8c8d9a81808c858d9ac78a8684)
  (Twitter: [\@cyberboyIndia](https://x.com/cyberboyIndia))
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::: {#sec-acknowledgements .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Project Lead

  Name                      Affiliation                                   Personal Links
  ------------------------- --------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------
  Jinson Varghese Behanan   [Astra Security](https://www.getastra.com/)   [Website](https://www.jinsonvarghese.com/), [Twitter](https://twitter.com/JinsonCyberSec), [LinkedIn](https://www.linkedin.com/in/JinsonVarghese/)
  Shashank                  [CredShields](https://credshields.com/)       [Twitter](https://x.com/cyberboyIndia), [LinkedIn](https://www.linkedin.com/in/shashank-in/)

## Contributors

Individuals that provided a significant contribution to the project:

  Name               Affiliation                                                 Personal Links
  ------------------ ----------------------------------------------------------- -------------------------------------------------------------------------------------------------
  Moises Ruiz Diaz   [Web3 Security Latam](https://www.web3securitylatam.com/)   [Twitter](https://twitter.com/bunturx), [LinkedIn](https://www.linkedin.com/in/bunturx)
  Hansen Wong        \-                                                          [Twitter](https://twitter.com/hansen_wong)
  Pratik Lagaskar    [CredShields](https://credshields.com/)                     [LinkedIn](https://www.linkedin.com/in/pratik-lagaskar), [Twitter](https://x.com/warlordsam077)
  Nehal Pillai       [CredShields](https://credshields.com/)                     [LinkedIn](https://www.linkedin.com/in/nehal-pillai), [Twitter](https://x.com/nehal_10_0)
  Sobhan Shokri      \-                                                          [LinkedIn](https://www.linkedin.com/in/xdevman/), [Twitter](https://x.com/xdevman)
:::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

All discussions take place on the the OWASP Smart Contract Top Ten
[GitHub
repository](https://github.com/OWASP/www-project-smart-contract-top-10)
or [Slack Channel](https://owasp.slack.com/archives/C07MNDE6TPZ).

We welcome all community members to actively participate and help
enhance this project. If you have any suggestions, feedback or want to
help improve the list, we invite you to kickstart a dialogue by raising
an issue or submitting a pull request.

You can read our contributing guidelines
[here](https://github.com/OWASP/www-project-smart-contract-top-10/blob/main/CONTRIBUTING.md).
:::

::: {#sec-owasp_archive .section .page-body .tab-hidden}

------------------------------------------------------------------------

## About the Smart Contract Top 10 {#about-the-smart-contract-top-10}

The OWASP Smart Contract Top 10 is a standard awareness document that
intends to provide Web3 developers and security teams with insight into
the top 10 vulnerabilities found in smart contracts.

It will serve as a reference to ensure that smart contracts are secured
against the top 10 weaknesses exploited/discovered over the last couple
of years.

### Top 10 {#top-10}

- SC01:2023 - [Reentrancy
  Attacks](2023/en/src/SC01-reentrancy-attacks.md)
- SC02:2023 - [Integer Overflow and
  Underflow](2023/en/src/SC02-integer-overflow-underflow.md)
- SC03:2023 - [Timestamp
  Dependence](2023/en/src/SC03-timestamp-dependence.md)
- SC04:2023 - [Access Control
  Vulnerabilities](2023/en/src/SC04-access-control-vulnerabilities.md)
- SC05:2023 - [Front-running
  Attacks](2023/en/src/SC05-front-running-attacks.md)
- SC06:2023 - [Denial of Service (DoS)
  Attacks](2023/en/src/SC06-denial-of-service-attacks.md)
- SC07:2023 - [Logic Errors](2023/en/src/SC07-logic-errors.md)
- SC08:2023 - [Insecure
  Randomness](2023/en/src/SC08-insecure-randomness.md)
- SC09:2023 - [Gas Limit
  Vulnerabilities](2023/en/src/SC09-gas-limit-vulnerabilities.md)
- SC10:2023 - [Unchecked External
  Calls](2023/en/src/SC10-unchecked-external-calls.md)

### Overview {#overview}

  Title                                    Description
  ---------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  SC01 - Reentrancy Attacks                A reentrancy attack exploits the vulnerability in smart contracts when a function makes an external call to another contract before updating its own state. This allows the external contract, possibly malicious, to reenter the original function and repeat certain actions, like withdrawals, using the same state. Through such attacks, an attacker can possibly drain all the funds from a contract.
  SC02 - Integer Overflow and Underflow    The Ethereum Virtual Machine (EVM) defines fixed-size data types for integers, which limits the range of values they can represent. Overflow occurs when an arithmetic operation exceeds the maximum value a data type can hold, while underflow happens when an operation goes below the minimum value. For unsigned integers, underflow results in the maximum value, and for signed integers, exceeding the minimum value wraps around to the maximum positive value.
  SC03 - Timestamp Dependence              Smart contracts often use block.timestamp for time-sensitive functions. However, miners can slightly adjust this timestamp, creating a vulnerability where they can manipulate the timing to gain an unfair advantage.
  SC04 - Access Control Vulnerabilities    An access control vulnerability is a security flaw that allows unauthorized users to access or modify a contract's data or functions. These vulnerabilities occur when the contract's code fails to properly restrict access based on user permissions.
  SC05 - Front-running Attacks             Front-running is an attack where a malicious actor exploits knowledge of pending transactions to gain an unfair advantage. Attackers observe the mempool and place their own transactions with higher gas fees to be processed before the target transaction, leading to potential financial losses and disruption of smart contract functionality.
  SC06 - Denial of Service (DoS) Attacks   A Denial of Service (DoS) attack in Solidity targets vulnerabilities within smart contracts to exhaust critical resources such as gas, CPU cycles, or storage. These attacks aim to render the contract non-functional, disrupting its intended operation and potentially causing financial harm.
  SC07 - Logic Errors                      Logic errors, or business logic vulnerabilities, are subtle flaws found in smart contracts where the code deviates from its intended behavior. These errors can be challenging to detect as they reside within the contract's logic, potentially leading to unintended outcomes or exploitable conditions.
  SC08 - Insecure Randomness               Generating true randomness in smart contracts on blockchain networks is challenging due to their deterministic nature. Predictability or influence over a supposedly random number can allow attackers to exploit contracts for their benefit, undermining fairness and security measures.
  SC09 - Gas Limit Vulnerabilities         Gas limits on blockchain platforms like Ethereum impose constraints on smart contract computations per transaction. Functions exceeding the block gas limit, particularly those involving loops over dynamic data structures such as arrays, risk transaction failure due to resource exhaustion, highlighting a common vulnerability in contract design.
  SC10 - Unchecked External Calls          In Ethereum smart contracts, failing to properly verify the outcome of external function calls can lead to unintended consequences. If the called function fails and the calling contract does not check for this, it may incorrectly proceed under the assumption of success, potentially compromising contract integrity and functionality.

## Licensing {#licensing}

The OWASP Smart Contract Top 10 document is licensed under the [CC
BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/), the
Creative Commons Attribution-ShareAlike 4.0 license. Some rights
reserved.

[![license](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc-sa.svg)](https://github.com/OWASP/www-project-smart-contract-top-10/blob/8083e976d6d18013dce2d5e6e62f98e632151a09/LICENSE.md)

## Project Leaders {#project-leaders}

- [Jinson Varghese
  Behanan](../cdn-cgi/l/email-protection.html#3d5754534e52537d524a5c4e4d13524f5a)
  (Twitter: [\@JinsonCyberSec](https://x.com/JinsonCyberSec))
- [Shashank](../cdn-cgi/l/email-protection.html#8af9e2ebf9e2ebe4e1cae9f8efeef9e2e3efe6eef9a4e9e5e7)
  (Twitter: [\@cyberboyIndia](https://x.com/cyberboyIndia))
:::
::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-smart-contract-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-smart-contract-top-10){.github-button
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

### Smart Contract Top 10 Information

- [Incubator Project](../projects/index.html)

- [Version
  0.1.0](https://github.com/OWASP/www-project-smart-contract-top-10/tree/main/2025/en/src)

- [Documentation]{style="font-size:1.0em;padding-left:12px;"}

- [Builder]{style="font-size:1.0em;padding-left:12px;"}

- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Code Repository

- [Github
  Repository](https://github.com/OWASP/www-project-smart-contract-top-10)

### Translations

- [Spanish](https://github.com/OWASP/www-project-smart-contract-top-10/tree/main/2025/es/src)
- [Chinese](https://github.com/OWASP/www-project-smart-contract-top-10/tree/main/2025/zh-cn/src)
- [Persian
  (Farsi)](https://github.com/OWASP/www-project-smart-contract-top-10/tree/main/2025/FA/src)

### License

- [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

### Leaders

- [Jinson Varghese
  Behanan](../cdn-cgi/l/email-protection.html#9ef4f7f0edf1f0def1e9ffedeeb0f1ecf9)
- [Shashank](https://x.com/cyberboyIndia)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::

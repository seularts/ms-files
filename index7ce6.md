::::::::::::::::::::::::::::::::::::: main-wrapper
:::::::::::::::::::::::::::::::::::: {#donate-app style="margin: 0px;" v-cloak=""}
::::::::::::::::::::::::::::::::::: col-sidebar
:::::::::::::::::::::::::::::::::: {.main-wrapper style="padding: 0px;"}
<div>

# Donate to the OWASP Foundation

The Open Worldwide Application Security Project (OWASP) is a nonprofit
foundation that works to improve the security of software. Through
community-led open source software projects and hundreds of local
chapters worldwide, your gift\* will support the Foundation and its many
activities around the world to secure the web. Existing donors can
[Modify Recurring Gifts](https://owasp.glueup.com/).

::: {#error-message .error-text style="font-size: 90%; margin-bottom: 16px" v-if="Object.keys(errors).length"}
Please correct the errors below before proceeding.
:::

::::::::::::::::::: gift-amount
:::::::: gift-amount-header
::: amount-title
Amount of your Gift
:::

:::::: gift-currency
::: {v-bind:class="currency === 'usd' ? 'selected' : ''" v-on:click="changeCurrency('usd')"}
USD \$
:::

::: {v-bind:class="currency === 'eur' ? 'selected' : ''" v-on:click="changeCurrency('eur')"}
EUR €
:::

::: {v-bind:class="currency === 'gbp' ? 'selected' : ''" v-on:click="changeCurrency('gbp')"}
GBP £
:::
::::::
::::::::

::::::::::: donation-amounts
:::::: donation-amount-row
::: {v-on:click="setAmount(10)" v-bind:class="amount === 10 &&
              !isCustomAmount ? 'selected' : ''"}
[]{v-html="currencySymbol"}10
:::

::: {v-on:click="setAmount(25)" v-bind:class="amount === 25 &&
              !isCustomAmount ? 'selected' : ''"}
[]{v-html="currencySymbol"}25
:::

::: {v-on:click="setAmount(50)" v-bind:class="amount === 50 &&
              !isCustomAmount ? 'selected' : ''"}
[]{v-html="currencySymbol"}50
:::
::::::

:::::: donation-amount-row
::: {v-on:click="setAmount(100)" v-bind:class="amount === 100 &&
              !isCustomAmount ? 'selected' : ''"}
[]{v-html="currencySymbol"}100
:::

::: {v-on:click="setAmount(500)" v-bind:class="amount === 500 &&
              !isCustomAmount ? 'selected' : ''"}
[]{v-html="currencySymbol"}500
:::

::: {v-on:click="setCustomAmount" v-bind:class="isCustomAmount ? 'selected' : ''"}
[Other]{v-if="!isCustomAmount"}
[[]{v-html="currencySymbol"}]{.currencyinput v-else=""}
:::
::::::
:::::::::::

::: {.error-text v-if="errors.amount"}
{{ errors.amount\[0\] }}
:::
:::::::::::::::::::

::: donation-options
Make this a monthly recurring gift

[]{.checkmark} Join the OWASP Mailing List

[]{.checkmark} Publicly list me as a supporter of [{{ projectName
}}]{style="font-weight: 900; color: #233e81"}

[]{.checkmark}
:::

::::::::: donor-fields
### Your Information

<div>

::: {.error-text v-if="errors.email"}
{{ errors.email\[0\] }}
:::

</div>

<div>

::: {.error-text v-if="errors.email_confirm"}
{{ errors.email_confirm\[0\] }}
:::

</div>

<div>

::: {.error-text v-if="errors.name"}
{{ errors.name\[0\] }}
:::

</div>
:::::::::

::: {.donation-options v-if="showRestrictedOption"}
Please restrict this gift[ for [{{ projectName
}}]{style="font-weight: 900; color: #233e81"}]{v-if="projectName"}. In
doing so, I understand this gift amount is net 10% administration costs
and unspent restricted gift balances become unrestricted after one year.

[]{.checkmark}
:::

:::: {style="margin-bottom: 30px;"}
::: {.error-text v-if="errors.recaptcha"}
{{ errors.recaptcha\[0\] }}
:::
::::

::: submit-container
Donate
:::

\* Unless otherwise noted your gift to the OWASP Foundation, net credit
card processing fees, is unrestricted and will be used at the sole
discretion of the organization to fulfill its mission and objectives.
Read more about our [Donation
Policy](../www-policy/operational/donations.html){target="_blank"
rel="noopener"}. You do have the option to be listed as a Supporter of a
Project or Chapter; however, this option does not restrict your gift in
anyway whatsoever. The OWASP Foundation is a 501(c)3 therefore in some
cases your gift may be tax-deductible and you should consult with a tax
professional for more details. Additionally you can elect to receive
marketing mails from us by selecting \"Join the OWASP Marketing Mail
List.\" Marketing mails include information and special offers for
upcoming conferences, meetings, and other opportunities offered to you.
You can revoke your consent to receive Marketing Mail List emails at any
time by using the Unsubscribe link found at the bottom of these emails.

</div>
::::::::::::::::::::::::::::::::::
:::::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::
:::::::::::::::::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

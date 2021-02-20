# Public transport in Germany during COVID-19

This repository contains data regarding the estimated usage of public transport in Germany during the COVID-19 pandemic in 2020. The data is extracted from the public transport companion [Abfahrt](https://play.google.com/store/apps/details?id=de.andary.abfahrt), which is an Android app that can be used to retrieve the next departures for a specific bus stop or a train station.

Abfahrt supports multiple public transport providers in Germany and is used by over a 1,000 active users throughout the country. It logs the amount of requests by endusers for departures per station and publishes them in the Abfahrt Livemap (retired as of Q1 2021).

The amount of requests for information on departures is likely correlated to how many people are actually using public transportation. The amount of requests per week in 2020 can be found inside of `2020.csv`. The amount of requests per week is relative to the maximum amount of requests per week.

## Findings

The following diagram displays the data of `2020.csv`:

![Amount of requests per week in 2020](https://andary.de/io/oepnv-covid19.jpg)

- The highest estimated usage of public transportation can be observed in **February 2020** (Week 7).
- On **March 17** (Week 12), [the Robert-Koch-Institut classifies the infection risk in Germany as high](https://www.tagesschau.de/inland/coronavirus-deutschland-rki-101.html). In the same week, [Angela Merkel addresses the public and calls for strict actions](https://www.tagesschau.de/inland/merkel-rede-109.html). The estimated usage of public transportation **drops to 35%** of the maximum in Week 7.
- On **March 22**, [Germany goes into lockdown](https://www.tagesschau.de/inland/kontaktverbot-coronavirus-101.html).
- On **April 17** (Week 16), [the reproduction rate R falls below 1](https://www.tagesschau.de/inland/wieler-spahn-pressekonferenz-101.html). The estimated usage of public transportation **drops to just 25%**.
- On **May 4** (Week 19), [the first schools reopen](https://www.tagesschau.de/inland/schulen-coronavirus-101.html), and a week later, [in most states restaurants are allowed to open again](https://www.tagesschau.de/inland/corona-lockerung-bundeslaender-101.html). The estimated usage of public transporation **rises to around 35%**.
- In **July** (Week 28), you can observe a peak in the estimated usage of public transportation **of 46%**. No significant events occured in this week.
- Due to more and more relaxed restrictions over the next few months, the estimated usage of public transportation climbs **up to 69% in September and October**.
- On **October 28** (Week 44), [the government announced a second light lockdown due to rising infections](https://www.tagesschau.de/inland/corona-regeln-november-101.html). The estimated usage of public transportation drops **to 32%**.
- With [even more restrictive measurements announced to start on **December 1**](https://www.tagesschau.de/inland/corona-plan-bundeslaender-101.html) (Week 49), you can observe a **peak of 52%** estimated public transportation usage in Week 48.
- With [Angela Merkel appealing to the population and calling for even more restrictions](https://www.tagesschau.de/inland/merkel-corona-generaldebatte-101.html) on **December 9** (Week 50) and [the government anncouncing a full lockdown](https://www.tagesschau.de/inland/corona-massnahmen-145.html) on **December 13**, estimated usage of public transportation **drops to 20%**.
- At the **end of the year**, the estimated usage of public transportation is at **just 15%** of the maximum estimated usage in February.

## Accuracy of the data

Abfahrt logs every time an enduser requests departures for a specific stop or station. Obviously, the amount of requests does therefore not necessarily translate to the amount of public transport journeys of this user, but is likely correlated.

As Abfahrt does not track any personal data, it has no way of differentating between single users and there is no information on how many users were responsible for how many of the performed requests. This may result in volatility in the dataset due to a changing amount of people using the app. According to the Google Play Developers Console, the amount of devices that Abfahrt was installed on in 2020 actually somewhat relates to the data seen above. The peak of users was reached in May 2020 with around 1,100 unqiue active devices and then dropped to just around 850 at the end of year. Over the whole year, the user base of Abfahrt has grown 10,2%.

Additionally, please keep in mind that this is just a hobby project. I'm not an expert on this field and it is not my intention to publish anything of scientfic value. I just think that it's interesting to see the key events of this year mirror in my own data. :pray:

## Related resources

In April 2020, [Deutsche Bahn said](https://www.tagesschau.de/wirtschaft/coronavirus-bahn-101.html) that its current amount of passengers is around 10 to 15 percent of the usual amount. Additionally, they reduced the amount of trains in service to around 65% and were using their weekend schedules. This was reversed in May 2020, when [Deutsche Bahn decided](https://www.tagesschau.de/wirtschaft/bahn-app-auslastung-angebot-101.html) to keep up the normal schedules to reduce the amount of passengers per single train.

[According to Deutsche Bahn](https://www.deutschebahn.com/de/presse/pressestart_zentrales_uebersicht/Fragen-und-Antworten-zum-Bahnverkehr-in-Zeiten-von-Corona-4966788), the amount of bookings in September were about 75% and in October about 50% of the usual demand. This vaguely relates to the data shown above. Unfortunately, I wasn't able to find any more accurate data.

**Made with :two_hearts: in Heidelberg.**

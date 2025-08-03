Here’s what each of those columns represents in the GDELT 1.0 Event schema:

- **Cameo**  
  The CAMEO (Conflict and Mediation Event Observations) code for the event, usually a 4-digit string. It encodes both the high-level category (first two digits, the “base code”) and the more specific action (last two digits).

- **Cameo_full**  
  The human-readable description of that CAMEO code (e.g. “14 – Protest,” “181 – Violent demonstration”).

- **GLOBALEVENTID**  
  A unique identifier for each distinct event in the database. Every row with the same GLOBALEVENTID refers to the same underlying event, even if mentioned multiple times.

- **SQLDATE**  
  The date on which the event occurred, in YYYYMMDD format (e.g. `20240415` for April 15, 2024).

- **Actor1Name**  
  The name of the primary actor initiating the action (e.g. “ISRAELI GOVERNMENT,” “HAMAS”).

- **Actor1Geo_FullName**  
  The full geographic name (city, province/state, country) associated with Actor 1, where that actor is based or acting from.

- **Actor2Name**  
  The name of the secondary (target) actor in the event (e.g. “PALESTINIAN CIVILIANS,” “UN”).

- **Actor2Geo_FullName**  
  The full geographic name for Actor 2, analogous to Actor1Geo_FullName.

- **IsRootEvent**  
  A binary flag (“1” or “0”) indicating whether this row represents the root record for that GLOBALEVENTID (i.e. the primary, canonical mention).

- **EventCode**  
  Same as **Cameo**, the full 4-digit CAMEO code for the event.

- **EventBaseCode**  
  The 2-digit “base” portion of the CAMEO code (e.g. “14” for all protest-related events).

- **QuadClass**  
  A high-level grouping of event types into one of four “quadrants”:  
  1 = Verbal Cooperation  
  2 = Material Cooperation  
  3 = Verbal Conflict  
  4 = Material Conflict  

- **GoldsteinScale**  
  A numerical score (typically between –10 and +10) estimating the event’s likely impact on stability—negative for conflict/violence, positive for cooperation.

- **NumMentions**  
  How many times this event was referenced across all monitored news/sources.

- **NumSources**  
  The number of distinct media outlets or feeds that mentioned this event.

- **NumArticles**  
  The count of unique articles in which the event appears.

- **AvgTone**  
  The average “tone” of all mentions (a sentiment measure where negative values = more negative coverage, positive = more positive).

- **ActionGeo_Type**  
  A numeric code for the geographic granularity of the event location:  
  - 1 = Country  
  - 2 = Province/State  
  - 3 = Admin2 (district/county)  
  - 4 = City  
  - 5 = Unknown  

- **ActionGeo_FullName**  
  The full place name (city, province, country) where the event actually took place.

- **ActionGeo_CountryCode**  
  The 2-letter ISO country code for the event location (e.g. “IL” for Israel, “PS” for Palestine).

- **SOURCEURL**  
  The URL of the article or feed item from which this particular mention of the event was extracted.
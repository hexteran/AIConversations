# Passive Personal Metabolism and Cognitive Energy Observation

## Objective

The goal of this 30-day N-of-1 study is to understand **how I normally feel and function in everyday life** and how those changes relate to glucose, sleep, physical activity, training, heart rate, meals, caffeine, and other naturally occurring factors.

This is an **observational study, not an intervention study**. I should not deliberately change my diet, meal order, walking habits, caffeine intake, sleep schedule, training schedule, hydration, or other routines for the purpose of the study.

The useful question is:

> When I live normally, which naturally occurring physiological and behavioral patterns are associated with feeling energetic, focused, sleepy, hungry, stressed, mentally tired, or physically tired?

Glucose is treated as one possible explanatory variable rather than as the assumed cause of changes in energy or cognition.

## Main design principle: minimum overhead

The study is only useful if logging does not itself substantially change normal behavior. Therefore:

1. Prefer measurements collected automatically by devices and apps.
2. Keep manual check-ins short enough to complete in a few taps.
3. Do not weigh food or calculate macronutrients unless that is already part of normal routine.
4. Do not perform pre/post-training weighing or special hydration measurements.
5. Do not add special walks, standardized meals, fasting periods, or training sessions.
6. Prefer fewer consistently recorded variables over many inconsistently recorded variables.

## Duration

Observe normal life for approximately **30 days**.

The same protocol is used throughout the period. There are no experimental phases and no prescribed interventions.

The first 3–5 days can be treated as a familiarization period for the apps and optional cognitive test, but normal habits should remain unchanged.

## Recommended low-overhead app setup on Android

### 1. Google Health Connect — automatic data hub

Use **Health Connect** as the background aggregation layer whenever the wearable and other apps support it.

Health Connect can store many useful categories, including activity, exercise, sleep, heart rate, resting heart rate, HRV, weight, nutrition, hydration, and blood glucose. Whether a particular metric appears there depends on whether the source app actually writes that data to Health Connect.

Official documentation:
https://developer.android.com/health-and-fitness/health-connect/data-types

The intention is that data such as steps, workouts, sleep, heart rate, and HRV should be collected automatically rather than entered manually.

### 2. Bearable — primary subjective journal

**Bearable** is a good candidate for the main manual journal because it is designed for quick repeated tracking of energy, mood, symptoms, lifestyle factors, and custom ratings. On Android it can read supported data from Health Connect.

Useful things to configure in Bearable:

- Energy
- Focus / concentration as a custom rating
- Sleepiness or mental fatigue
- Stress
- Mood
- Hunger, if useful
- Training as a Factor
- Coffee / caffeine as a Factor
- Alcohol as a Factor, when applicable
- unusually large or unusual meals as optional Factors

Bearable supports multiple energy entries during a day and allows their times to be adjusted. Its Factors and custom ratings can also be used to record events and states without writing journal text.

Official information:
https://bearable.app/
https://bearable.app/support/howto/sync-with-google-health-connect-apple-health/

Bearable can export tracked data later for analysis.

### 3. CGM manufacturer app — glucose source

Use the normal application supplied by the CGM manufacturer for continuous glucose measurement.

There is no need to manually copy individual glucose readings into the journal. Export the CGM data after the observation period and align it with the other data by timestamp.

If the CGM app happens to write glucose into Health Connect, that can simplify aggregation, but this should not be assumed in advance.

### 4. Wearable app — passive physiology

Keep using the wearable's normal application. Prefer automatic collection of:

- steps
- workouts
- heart rate
- resting heart rate
- HRV
- sleep start / end
- sleep duration

If possible, let the wearable app synchronize these measurements to Health Connect and let Bearable read the supported subset.

## Minimal manual protocol

### Regular check-ins

Do only **three short subjective check-ins per day**:

- morning
- middle of the day
- evening

Exact clock times are less important than consistency. If the schedule varies, preserve the actual timestamp rather than forcing an artificial measurement time.

Each check-in should take roughly 10–20 seconds.

Record only:

- **Energy**: 1–5
- **Focus / concentration**: 1–5
- **Sleepiness / mental fatigue**: 1–5
- **Stress**: 1–5

Optional if they are useful and still low-overhead:

- hunger: 1–5
- mood: 1–5

Using a 1–5 scale fits Bearable's existing energy workflow and reduces friction compared with entering precise 0–10 numbers.

### Event logging

Log only events whose timestamps are useful for later interpretation.

The minimum useful event set is:

- meals
- caffeine
- training

Do not attempt to describe everything that happened during the day.

## Meals and food

Detailed food weighing is intentionally excluded from the core protocol because it creates substantial overhead and can change eating behavior.

For a meal, the minimum useful information is simply:

- approximate timestamp

If it takes only a few extra seconds, optionally add a broad description such as:

- normal meal
- large meal
- carb-heavy meal
- snack
- dessert / sugary food

If a nutrition app is already part of normal routine and writes nutrition data to Health Connect, keep using it. Do not start meticulous calorie or macro tracking solely for this study unless that is genuinely desired independently of the experiment.

The CGM trace can later be used to derive post-meal glucose responses automatically from these timestamps.

## Caffeine

Record caffeine with minimal detail:

- timestamp
- type or rough quantity only if easy (for example, coffee / energy drink)

Exact milligrams are optional.

The main reason to record caffeine is that it is an important confounder for perceived energy and cognitive performance.

## Intensive training

Training remains part of normal life and should not be modified for the study.

Do **not** perform special pre/post measurements.

The wearable should automatically capture the workout duration and cardiovascular measurements where possible.

Manually log only:

- training timestamp / type
- **cardiovascular fatigue after training**: 1–5
- **muscular fatigue after training**: 1–5
- **overall fatigue after training**: 1–5

Optionally record perceived session intensity (RPE 1–10) if it takes only one additional tap.

There is no need to manually enter average HR, maximum HR, HR zones, or session duration if the wearable already stores them.

The analysis can later derive relationships such as:

`training → glucose pattern → evening energy → sleep → next-day energy / focus`

and:

`training intensity → subjective muscular/cardio fatigue → recovery`

## Hydration

Hydration is **not a core manual metric** in this low-overhead version.

Pre/post-training body-weight measurements, sweat-loss calculations, and urine measurements are removed.

If water intake is already naturally recorded by an app, keep it. Otherwise, do not add detailed hydration logging solely for the experiment.

A simple subjective signal such as unusually thirsty / dehydrated can be added as a Bearable Factor when it is noticeable, but it should not become another mandatory task.

## Optional objective cognitive measurement

### What is PVT?

**PVT means Psychomotor Vigilance Test.** It is a simple reaction-time test: a stimulus appears after an unpredictable delay and the user responds as quickly as possible. Repeated trials provide measures of alertness, reaction speed, variability, and attentional lapses.

It is useful because performance can deteriorate with sleepiness or fatigue even when subjective ratings do not change much.

### Keep it optional and infrequent

A cognitive test adds much more overhead than passive sensor collection. Therefore it should **not** be performed several times every day in the core protocol.

Suggested options:

- one brief PVT at roughly the same time once per day, or
- one brief PVT 3–4 days per week

Use the same phone and the same app throughout the study.

If even this becomes annoying, remove PVT completely. Subjective energy and focus are more important to this study's primary goal than maximizing laboratory-style measurement density.

## What should be automatic vs manual?

### Automatic whenever possible

- CGM glucose
- steps
- workout timestamps and duration
- heart rate
- resting heart rate
- HRV
- sleep timing and duration
- weight, if already coming from a connected scale
- existing nutrition data, if already logged elsewhere

### Manual — three times per day

- energy
- focus
- sleepiness / mental fatigue
- stress

### Manual — only when the event occurs

- meal timestamp
- caffeine timestamp
- training type / timestamp
- post-training cardio fatigue
- post-training muscular fatigue
- post-training overall fatigue

### Optional

- hunger
- mood
- PVT
- broad meal category
- RPE
- alcohol
- subjective dehydration / unusual thirst

## Expected daily overhead

A realistic target is:

- three subjective check-ins: about 30–60 seconds total
- meal/caffeine event taps: about 30–60 seconds total
- training rating on training days: about 10–20 seconds
- optional PVT: about 3 minutes when performed

Without PVT, manual overhead should usually remain around **1–2 minutes per day**.

## Data to export after the observation period

Rather than constructing a manual spreadsheet every day, export raw data at the end.

Potential sources:

- CGM export
- wearable / Health Connect data
- Bearable export
- optional PVT results

Align the datasets by timestamp during analysis.

A simplified merged dataset could contain:

```text
timestamp
energy
focus
sleepiness
stress
hunger
mood

glucose

glucose_change_30m
glucose_change_60m
glucose_slope

meal_event
meal_category
caffeine_event

steps
heart_rate
resting_hr
hrv
sleep_duration
sleep_start
sleep_end

training_event
training_type
training_duration
training_rpe
post_training_cardio_fatigue
post_training_muscular_fatigue
post_training_overall_fatigue

pvt_median_rt
pvt_lapses
```

Not every row needs every field. The analysis pipeline can combine time-series measurements and event data after collection.

## Analysis plan

The first analysis should stay descriptive rather than trying to prove causality.

### 1. Build timelines

Overlay:

- glucose
- meals
- caffeine
- training
- sleep
- energy
- focus
- sleepiness

This should reveal obvious repeated patterns before statistical modeling.

### 2. Examine natural associations

Examples:

- sleep duration vs next-day energy
- HRV vs next-day energy / focus
- resting HR vs fatigue
- training vs evening and next-day fatigue
- meal events vs glucose excursions
- glucose excursions vs later sleepiness
- caffeine timing vs energy / sleep

### 3. Use lagged relationships

A particularly useful question is not just whether glucose and energy are correlated at the same time, but whether glucose behavior precedes a change in how I feel.

For example:

- glucose now → energy 30 minutes later
- glucose now → energy 60 minutes later
- glucose slope → sleepiness 60–120 minutes later
- training → energy later that evening
- sleep → next-morning focus

### 4. Control obvious confounders

When enough data are available, regression models can include:

- time of day
- sleep duration
- caffeine
- meal timing
- recent training
- recent activity
- stress

For example:

`Energy = β0 + β1·Glucose + β2·Sleep + β3·Caffeine + β4·TimeOfDay + β5·Training + error`

This is still observational evidence and should not be interpreted as proof of causation.

## Questions this study may answer

- What does my normal daily energy pattern look like?
- What times of day am I normally most and least focused?
- Does poor sleep predict lower energy or focus the following day?
- Do some naturally occurring meals produce reproducible glucose patterns?
- Are larger or faster glucose changes associated with later sleepiness or lower focus?
- Does caffeine timing explain some apparent glucose/energy relationships?
- How do intensive training sessions affect evening and next-day energy?
- Do cardiovascular and muscular fatigue behave differently after training?
- Does HRV or resting HR correlate with how recovered I feel?
- Do objective PVT results, when available, agree with subjective energy and focus?

## Interpretation principles

1. **Do not change habits to create cleaner data.** Normal life is the object of study.
2. Correlation is not causation.
3. A glucose spike is not automatically harmful or responsible for fatigue.
4. CGM values measure interstitial glucose and should not be treated as perfectly timed blood-glucose measurements.
5. Passive measurements are preferred to manual ones.
6. Missing occasional subjective entries are preferable to making the protocol burdensome enough to change behavior or abandon it.
7. Look for patterns that repeat across many normal days rather than interpreting single events.

## Recommended practical setup

For Android, the lowest-overhead starting configuration is:

**CGM app + wearable → Health Connect → Bearable for subjective journaling**

with CGM data exported separately if it cannot be synchronized into the same ecosystem.

The core manual task is therefore only:

> three quick state check-ins per day + timestamps for meals/caffeine/training + a few fatigue taps after training.

Everything else should be automated where possible.
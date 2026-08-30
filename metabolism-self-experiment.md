# Personal Metabolism and Cognitive Energy Experiment

## Objective

This 30-day N-of-1 experiment is designed to identify which measurable physiological and behavioral variables are associated with changes in subjective energy, concentration, sleepiness, hunger, mood, and objective cognitive performance.

The study treats glucose as one possible explanatory variable rather than assuming that glucose fluctuations directly determine cognitive energy. It combines continuous glucose monitoring with sleep, training load, heart-rate and HRV, hydration, food intake, caffeine, and repeated cognitive testing.

A second objective is to move beyond passive correlation. After an initial observation phase, the protocol introduces repeated controlled interventions so that potentially causal effects can be tested within the same individual.

## Core model

The experiment follows this causal structure:

> context and behavior → physiological response → cognitive / subjective outcome

Examples:

- meal composition → glucose response → later sleepiness or concentration
- training load → recovery and sleep → next-day cognitive performance
- dehydration → post-training fatigue → cognitive-test performance
- poor sleep → altered glucose response + lower energy

Because these variables influence one another, the experiment records major confounders instead of interpreting any single correlation in isolation.

## Duration and phases

### Days 1–10: Observation

Live normally. Do not deliberately change diet, exercise, caffeine, or sleep habits.

The purpose is to establish natural variation and learn the data-collection routine.

### Days 11–18: Post-meal walking experiment

Choose one standardized lunch and repeat it across eight test days.

Randomize between:

- **Control:** eat the meal and do not exercise immediately afterward.
- **Intervention:** eat the same meal and take a 15-minute walk immediately afterward.

Avoid doing all control days first and all intervention days second. Alternate or randomize conditions.

When practical, record subjective and cognitive outcomes before the meal and at approximately +30, +60, +90, +120, and +180 minutes.

### Days 19–26: Meal-order experiment

Use another standardized meal.

Randomize between:

- carbohydrate first, then protein / vegetables
- protein / vegetables first, then carbohydrate

Keep ingredients, portion size, meal time, caffeine, and post-meal activity as similar as reasonably possible.

### Days 27–30: Replication

Choose the strongest apparent effect from the preceding phases and repeat the comparison.

The purpose is to determine whether the effect reproduces instead of relying on a single unusually good or bad day.

## Core measurements

Record:

- continuous glucose using a CGM
- heart rate and HRV
- steps and activity
- sleep timing and duration
- meal timestamps and approximate macronutrients
- caffeine timing and dose
- morning body weight
- subjective energy, concentration, sleepiness, hunger, mood, stress, and motivation using stable 0–10 scales

For meals, derive:

- pre-meal glucose
- post-meal peak
- change from baseline
- time to peak
- glucose at +60, +120, and +180 minutes
- incremental area under the curve (iAUC)
- approximate return-to-baseline time

For whole days, derive:

- mean glucose
- standard deviation
- coefficient of variation
- minimum and maximum
- overnight mean
- overnight variability

CGM values represent interstitial glucose rather than direct blood glucose, so small timing differences should not be overinterpreted.

## Subjective state

Use fixed measurement times rather than recording only when feeling unusually good or bad.

Suggested checkpoints:

- after waking
- 10:00
- 13:00
- 16:00
- 19:00
- before bed

Rate each from 0–10:

- mental energy
- concentration
- sleepiness
- hunger
- mood
- stress
- motivation to work

Keep the meaning of each scale stable throughout the experiment.

## Cognitive-performance battery

Use the same device, test implementation, input method, and environment whenever possible.

Practice the tests for 3–5 days before treating results as experimental data to reduce learning effects.

### Primary test: 3-minute Psychomotor Vigilance Test (PVT)

Record:

- median reaction time
- 90th-percentile reaction time
- reaction-time variability
- number of lapses

PVT is the main objective alertness measure.

### Secondary test: Digit-Symbol Substitution

Use a 1–2 minute digital version to measure processing speed.

### Optional: 2-back

Use a short 1–2 minute test to measure working memory and sustained attention.

A practical core battery is:

1. subjective ratings — ~15 seconds
2. PVT — 3 minutes
3. digit-symbol — 2 minutes

This is short enough to repeat regularly without the testing itself becoming a major burden.

## Intensive training

Training is treated as a major explanatory variable rather than something to remove from the dataset.

For every intensive session, record:

- training type
- start time
- duration
- session structure when useful: warm-up, technique, pads / bag, intervals, sparring, cooldown
- overall RPE, 0–10
- cardiovascular RPE, 0–10
- muscular RPE, 0–10
- average heart rate
- maximum heart rate
- minutes above 80% of HRmax
- minutes above 90% of HRmax

### Session load

Calculate:

`session load = duration in minutes × overall RPE`

Examples:

- 90 min × RPE 3 = 270 AU
- 90 min × RPE 8 = 720 AU
- 30 min × RPE 10 = 300 AU

The short interval session may be more intense, while the longer hard session may have greater total load.

### Glucose around training

Record or derive:

- glucose at −60 min
- glucose immediately before training
- minimum during training
- maximum during training
- glucose immediately after
- glucose at +30, +60, +120, and +180 min

Do not assume hard exercise must lower glucose. High-intensity exercise can temporarily raise glucose because counter-regulatory hormones stimulate glucose release from the liver.

## Hydration and dehydration

Dehydration should be treated as a training-stress and recovery variable.

Measure body mass immediately before and after hard sessions under similar conditions, ideally after using the toilet, with similar or minimal clothing, and after toweling off sweat.

### Percentage body-mass loss

`body mass loss % = (pre-training weight − post-training weight) / pre-training weight × 100`

### Estimated sweat loss

Approximately:

`sweat loss (L) = pre-weight − post-weight + fluid consumed − urine produced`

For short exercise periods, approximately 1 kg of acute mass loss can be treated as about 1 L of fluid.

### Sweat rate

`sweat rate = estimated sweat loss / training duration in hours`

Record:

- pre-training weight
- post-training weight
- body-mass loss %
- fluid consumed
- urine during training if applicable
- estimated sweat loss
- sweat rate

These metrics can later be tested against RPE, post-training fatigue, cognitive performance, heart rate, and next-day HRV.

## Post-training recovery

Immediately after training, rate from 0–10:

- overall fatigue
- mental fatigue
- muscular fatigue

Approximately two hours later, record:

- energy
- hunger
- sleepiness

The next morning, record:

- muscle soreness
- general fatigue
- sleep quality
- resting heart rate
- HRV
- subjective energy
- cognitive battery when scheduled

This supports analyses such as:

`training load → sleep / recovery → next-day cognitive performance`

## Suggested data structure

Use one row per subjective or cognitive measurement rather than one row per day.

Suggested columns:

```text
timestamp
energy
concentration
sleepiness
hunger
mood
stress
motivation

pvt_median_rt
pvt_p90_rt
pvt_rt_variability
pvt_lapses
digit_symbol_score

glucose_now
glucose_15m_ago
glucose_30m_ago
glucose_60m_ago
glucose_slope_30m

last_meal_time
minutes_since_meal
meal_kcal
meal_carbs
meal_protein
meal_fat
meal_fiber

caffeine_last_6h
steps_last_hour
exercise_last_6h

sleep_duration
sleep_quality
resting_hr
hrv
body_weight

experiment_condition

training_duration
training_rpe
training_cardio_rpe
training_muscular_rpe
training_load
training_avg_hr
training_max_hr
minutes_above_80pct_hrmax
minutes_above_90pct_hrmax

dehydration_pct
sweat_loss_l
sweat_rate_l_per_h
```

## Analysis plan

### 1. Visual analysis

Overlay on synchronized timelines:

- glucose
- meals
- caffeine
- activity / training
- sleep
- cognitive-test results
- subjective energy and sleepiness

### 2. Correlation analysis

Test associations such as:

- sleep duration vs morning PVT
- meal carbohydrate vs glucose peak
- training load vs next-day energy
- dehydration % vs post-training cognitive performance
- HRV vs subjective energy

### 3. Lagged analysis

Do not only compare glucose and energy measured at the same instant.

Test whether physiological changes precede subjective changes:

- glucose now → energy +30 min
- glucose now → energy +60 min
- glucose now → energy +90 min
- glucose now → energy +120 min

Repeat with:

- glucose change from baseline
- glucose slope
- glucose peak
- glucose iAUC

This may reveal, for example, that rapid glucose decline is associated with sleepiness even when absolute glucose concentration is not.

### 4. Regression and confounder control

A simple model might be:

`Energy = β0 + β1·Glucose + β2·Sleep + β3·Caffeine + β4·TimeOfDay + β5·Exercise + error`

Important confounders include:

- sleep duration and quality
- time since waking
- time of day
- time since last meal
- total meal calories
- carbohydrate / protein / fat / fiber
- caffeine
- recent exercise
- recent steps / activity
- training load
- hydration / dehydration
- stress

If glucose peak correlates with sleepiness but the relationship disappears after controlling for meal size, the evidence points more toward the meal as a whole than glucose itself.

## Questions this experiment should be able to address

- Do larger post-meal glucose excursions predict lower cognitive performance later?
- Is the rate of glucose decline more informative than the glucose peak?
- Does post-meal walking improve both glucose response and subjective or cognitive outcomes?
- Does meal order change glucose response, and does that change how I feel?
- How strongly does previous-night sleep predict glucose response and cognitive performance?
- Does training load predict next-day fatigue, HRV, or PVT performance?
- Does dehydration during training independently predict post-training cognitive fatigue?
- Does pre-training carbohydrate availability predict RPE or late-session fatigue?
- Do subjective fatigue and objective cognitive performance agree?

## Interpretation principles

1. Correlation is not causation.
2. A smaller glucose spike is not automatically better.
3. Isolated CGM readings should not be overinterpreted.
4. Repeated within-person comparisons are more useful than one-off observations.
5. Consistency of measurement is more important than collecting every possible metric.
6. Treat training, sleep, meals, hydration, caffeine, and circadian timing as interacting variables.

## Practical setup

The highest-value setup is:

- CGM
- smartwatch or heart-rate monitor
- food log
- sleep tracking
- daily weight
- fixed subjective ratings
- short PVT + Digit-Symbol battery
- pre/post-training weight and fluid log on hard-training days

This provides a rich dataset without making data collection so burdensome that adherence collapses.

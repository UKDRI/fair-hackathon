# TIHM dataset

This hosted copy contains the same tabular records as the reference `TIHM_Dataset`
package, exposed here with explicit `.csv` filenames and dataset-level
documentation so the files are easier to identify and reuse.

## Provenance

- Original dataset title: *TIHM: An open dataset for remote healthcare monitoring in dementia*
- Original DOI: <https://doi.org/10.5281/zenodo.7622128>
- Coverage: 2019-04-01 to 2019-06-30
- Resource type: tabular time-series dataset

## Files

| File | Rows | Columns | Description |
| --- | ---: | --- | --- |
| `data/Activity.csv` | 1,030,559 | `patient_id`, `location_name`, `date` | Room-level activity events per patient. |
| `data/Demographics.csv` | 56 | `patient_id`, `age`, `sex` | Patient sex and age band. |
| `data/Labels.csv` | 608 | `patient_id`, `date`, `type` | Clinical labels such as agitation and blood pressure. |
| `data/Physiology.csv` | 17,679 | `patient_id`, `date`, `device_type`, `value`, `unit` | Physiology measurements including blood pressure, heart rate, and temperature. |
| `data/Sleep.csv` | 461,423 | `patient_id`, `date`, `state`, `heart_rate`, `respiratory_rate`, `snoring` | Sleep stage observations with associated vital signs. |

## Column dictionary

### Activity

| Column | Type | Description |
| --- | --- | --- |
| `patient_id` | categorical | Participant hash code. |
| `location_name` | categorical | Room or sensor location, for example `Hallway`, `Lounge`, `Fridge Door`, `Bedroom`, or `Kitchen`. |
| `date` | datetime | Event timestamp from 2019-04-01 to 2019-06-30. |

### Labels

| Column | Type | Description |
| --- | --- | --- |
| `patient_id` | categorical | Participant hash code. |
| `date` | datetime | Label timestamp from 2019-04-04 to 2019-06-30. |
| `type` | categorical | Clinical label type, including `Agitation`, `Blood pressure`, and related observations. |

### Physiology

| Column | Type | Description |
| --- | --- | --- |
| `patient_id` | categorical | Participant hash code. |
| `date` | datetime | Measurement timestamp from 2019-04-01 to 2019-06-30. |
| `device_type` | categorical | Measurement source or modality, for example `Body Temperature`, `Heart rate`, or blood pressure devices. |
| `value` | float | Numeric measurement value. |
| `unit` | categorical | Measurement unit, for example `Cel`, `beats/min`, `%`, `kg`, or `mm[Hg]`. |

### Sleep

| Column | Type | Description |
| --- | --- | --- |
| `patient_id` | categorical | Participant hash code. |
| `date` | datetime | Sleep observation timestamp from 2019-04-01 to 2019-06-30. |
| `state` | categorical | Sleep state: `LIGHT`, `AWAKE`, `DEEP`, or `REM`. |
| `heart_rate` | float | Heart rate during the sleep observation. |
| `respiratory_rate` | float | Respiratory rate during the sleep observation. |
| `snoring` | boolean | Whether snoring was detected. |

### Demographics

| Column | Type | Description |
| --- | --- | --- |
| `patient_id` | categorical | Participant hash code. |
| `sex` | categorical | `Male` or `Female`. |
| `age` | categorical | Age band: `(70, 80]`, `(80, 90]`, or `(90, 110]`. |



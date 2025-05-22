Each folder contains skeleton data corresponding to the dataset divisions in the paper’s table “Details of HRC-OaSA dataset division, where xfre represents cross-frequency division and xsub represents cross-subject division.”

* **SBIT(hand)** refers to the hand-joint subset of the SBIT dataset. It retains all 17 hand joints without any averaging or preprocessing, so users must apply their own filtering or normalization. To assemble the complete SBIT dataset, merge these files with the corresponding ones in the `DepthProjection` folder.

#### File Naming in `Original`, `DepthProjection`, and `SBIT`

All files use the pattern:

```
P###A###R###_depth.json
```

* `P###` = subject ID (e.g., `P001` = Subject 1)
* `A###` = action ID (e.g., `A001` = Action 1)
* `R###` = repetition number (e.g., `R001` = first recording)

> **Example:** `P001A001R001_depth.json` is Subject 1 performing Action 1, first trial.

#### File Naming in `ProSSA`

Files in `ProSSA` encode both the motion vector source and the skeleton-length donor:

```
PabA###R###_depth.json
```

* **`Pa b`**:

  * `a` = subject whose motion vector is used
  * `b` = subject whose bone lengths are used
* `A###` = action ID
* `R###` = repetition number

> **Example 1:** `P013A005R002_depth.json`
> – Motion vector from Subject 1, performing Action 5 on the second trial
> – Bone lengths replaced by those of Subject 3

> **Example 2:** `PX10A00YR00Z_depth.json`
> – Motion vector from Subject X, Action Y, Trial Z
> – Bone lengths from Subject 10

> **Example 3:** `P10XA00YR00Z_depth.json`
> – Motion vector from Subject 10, Action Y, Trial Z
> – Bone lengths from Subject X

You can contact me at lbjctxz@126.com

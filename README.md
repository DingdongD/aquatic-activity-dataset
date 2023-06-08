### Write in front

We hope that readers will acknowledge our work by citing it when using our datasets or code.

Our related work based on this dataset currently has one formal published work (`ICARCV2022`), one minor revision work in review (`IEEE GRSL`) and one work in submission(`IEEE Sensor Journal`). The reader can cite our current published work as follows:

​	[1] X. Yu, Z. Cao, Z. Wu, C. Song, J. Zhu and Z. Xu, "A Novel Potential Drowning Detection System Based on Millimeter-Wave Radar," 2022 17th International Conference on Control, Automation, Robotics and Vision (ICARCV), Singapore, Singapore, 2022, pp. 659-664, doi: 10.1109/ICARCV57592.2022.10004245.

​	[2] X. Yu, Z. Cao, Z. Wu, C. Song, J. Zhu and Z. Xu, "Sample Intercorrelation Based Multi-domain Fusion Network for Aquatic Human Activity Recognition Using Millimeter-wave Radar", in IEEE Geoscience and Remote Sensing Letters, 2023, doi: 10.1109/LGRS.2023.3284395.

​	[3] Z. Wu, Z. Cao, X. Yu, C. Song, J. Zhu and Z. Xu, "A Novel Multi-Person Activity Recognition Algorithm Based on Point Clouds Measured by Millimeter-Wave MIMO Radar", in IEEE Sensor Journal.

 If you have problems running the code incompletely during the run, please feel free to contact us by 2222134033@zju.edu.cn.
 
### AHAR TASK

#### AHAR-I

​	Based on the TI AWR1243BOOST millimeter-wave radar, we completed the first version of the aquatic human activity recognition (AHAR-I) dataset, in which the millimeter wave radar parameters are configured as shown in the following table.

|           Patrameter Name           | Accurate Value |
| :---------------------------------: | :------------: |
|       Starting Frequency(GHZ)       |       77       |
|    Frequency Slope (MHZ/ $\mu$s)    |     46.397     |
|         Idel Time ($\mu$s)          |     30.00      |
|       Ramp End Time ($\mu$s)        |     80.00      |
|          Sample Rate(ksps)          |      6847      |
|     Periodicity Per Frame (ms)      |     100.00     |
|   Number of ADC Points Per Chirp    |      256       |
|        Number of Chirp Loops        |      128       |
| Valid Azimuth Field of View (VAFOV) |    -60°~60°    |

​	In AHAR-I dataset, we collected nine classes of aquatic human activities, including struggling, drowning, floating with a ring, swimming with a ring, pulling a ring, backstroke, breaststroke, freestyle and waving for help, and the number and duration of raw data files for each acitivty are shown in the table below. Among them, three swimming-like activities and lap-pulling activities were adopted in a continuous 400-frame acquisition mode, and the other five aquatic human activities were adopted in a continuous 200-frame acquisition mode.

|   Activity Type    | # of data files | Total duration (sec) |
| :----------------: | :-------------: | :------------------: |
| Distress(Struggle) |       32        |         600          |
|      Drowning      |       40        |         799          |
| Float with a ring  |       30        |         600          |
|  Swim with a ring  |       30        |         501          |
|    Pull a ring     |       13        |         516          |
|     Backstroke     |       20        |         655          |
|     Breastroke     |       18        |         639          |
|     Freestyle      |       18        |         635          |
|   Wave for help    |       30        |         600          |

​	In order to better promote the research and development in the topic/field of aquatic humanactivity recognition, we now make the relevant millimeter wave radar raw dataset publicly available. 

```
AHAR-I download link：https://pan.baidu.com/s/1r1EoYE4SxeX-yP5mz0Co-A 
link password：2l34 
```

​	In addition to this, we will further share our work based on AHAR-I (Two-Stage-Fusion Network, TSFNet), which was published in the international computer conference `ICARCV 2022`.  We sincerely hope that readers or users using our dataset and codes can cite our work,

​	We sincerely hope that readers or users who use our datasets and code will cite our work, as we consider it a sign of recognition and respect for our work.

​	[1] X. Yu, Z. Cao, Z. Wu, C. Song, J. Zhu and Z. Xu, "A Novel Potential Drowning Detection System Based on Millimeter-Wave Radar," 2022 17th International Conference on Control, Automation, Robotics and Vision (ICARCV), Singapore, Singapore, 2022, pp. 659-664, doi: 10.1109/ICARCV57592.2022.10004245.

#### AHAR-II

​	In the second version of the aquatic human activity recognition (AHAR-II) dataset, we added an aquatic human activity, namely frolicking, based on the AHAR-I. We then investigated the effects of covariances in different background environments (deep water, shallow water), different users (user 1, user 2) and different aspect-angles (radial and non-radial) on the recognition of aquatic human activities, respectively.

​	We divided the radar data collected based on the above covariances into six different variable domains, as shown in the following table.

|      Index      |             Domain Setting              |
| :-------------: | :-------------------------------------: |
| $\mathcal{D}_1$ |   subject 1,radial,shallow water area   |
| $\mathcal{D}_2$ |   subject 2,radial,shallow water area   |
| $\mathcal{D}_3$ | subject 1,non-radial,shallow water area |
| $\mathcal{D}_4$ | subject 2,non-radial,shallow water area |
| $\mathcal{D}_5$ |    subject 1,radial,deep water area     |
| $\mathcal{D}_6$ |    subject 2,radial,deep water area     |

​	Information on the number of radar raw data files acquired for different aquatic human activities under each variable domain is shown below, where 300 consecutive frames (30s) were acquired for each file. 

|                 | $A_1$ | $A_2$ | $A_3$ | $A_4$ | $A_5$ | $A_6$ | $A_7$ | $A_8$ | $A_9$ | $A_{10}$ | ALL  |
| :-------------: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :------: | :--: |
| $\mathcal{D}_1$ |  10   |  10   |  10   |  11   |  11   |  12   |  13   |  13   |  10   |    10    | 110  |
| $\mathcal{D}_2$ |  12   |  11   |  11   |  10   |  12   |  10   |  10   |  11   |  10   |    11    | 108  |
| $\mathcal{D}_3$ |   7   |   6   |   8   |   8   |   8   |   6   |   8   |   8   |  11   |    7     |  77  |
| $\mathcal{D}_4$ |   7   |   6   |   8   |   8   |   8   |   6   |   7   |   8   |  10   |    7     |  75  |
| $\mathcal{D}_5$ |   7   |   7   |   8   |   8   |   8   |   7   |  10   |   8   |   6   |    6     |  75  |
| $\mathcal{D}_6$ |   7   |   7   |   9   |   8   |   7   |   7   |   7   |   8   |   7   |    7     |  74  |

​	Note: The aquatic human activities corresponding to `A1-A10` are: struggling(distressing), drowning, freestyle, breaststroke backstroke, floating with a ring, swimming with a ring, pulling a ring, frolicking, and waving.

​	In addition,  we also provide a partial two-person aquatic human activity recognition dataset and a single-person continuous different aquatic human activity flow dataset, which can be used for testing the algorithm performance.

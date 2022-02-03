# Kinect-Database ![immagine](https://user-images.githubusercontent.com/26774553/152373922-8e54e0e6-b5b3-4f39-8808-169b7452cd37.png)

Data collection from four Kinect One (K1, K2, K3 K4) acquisition. The four devices acquired the data, independently recording with different viewpoints:

![Kinect_1_2_3_4](https://user-images.githubusercontent.com/26774553/152374188-16a82388-3be3-44a0-b2fb-97f402bd8d84.svg)

Experimental acquisitions were performed in a prototype room. In this setting, we decided to record each experimental trial using four Kinect One devices.Two are positioned to sense the whole room (K1 and K4), while the remaining two are placed to specifically acquire two areas of the room, such as the bed (K2) and the desk (K3).

We performed a set of experimental acquisitions on a group of 12 normal subjects (7 females and 5 males; age ranging 25 and 60 years old; height ranging 1.55 and 1.90 m). In the database the 12 different subjects are rappresented by the following abbreviation 'Sn', where n = 1,..12.

The acquisitions were structured as four separate sessions, for a total of about 13 min:
  - subject starts walking from standing position in front of K1 (identified as 'PATH1', in the dataset), then grabs a chair near the desk, placing it infront of the camera, and     finally sits on it. While sitting, the subject first moves the head backward and then leans the trunk forward, while simultaneously pitching the head as an unconscious           person. The subject then returns to the normal sitting position and finally gets up and brings the chair back to its original location. Each pose was maintained for 10 s.       The sequence was then repeated in front of the other cameras (K2 - 'PATH2', K3 - 'PATH3', K4 - 'PATH4');
  - subject starts sitting on the bed, then lies down on the back, turns on the right side, then returns sitting on the bed ('PATH5');
  - subject starts sitting on the bed, then lies down on the back, turns on the right side, then returns on the back and turns to the other side ('PATH6');
  - subject starts lying on the ground on the back, then turns on the left side ('PATH7');
  - subject starts sitting on the bed, then lies down. The action is repeated three times ('PATH8').

Each row of the dataset is labelled with one of the following classes:
  - Class 1: standing pose;
  - Class 2: sitting pose;
  - Class 3: lying down pose;
  - Class 4: “dangerous sitting” pose (in which the subject is sitting on a chair with the head forward or backward as if unconscious);
  - Class 5: trasitions between between two successive postures, e.g. when subject passes from the standing to the sitting pose or from the sitting to lying pose).

![omino](https://user-images.githubusercontent.com/26774553/152379873-27446217-7c26-4951-b632-7083d9d5fef1.svg)

In the file database.mat, you will fine the following column (joint angles between two body segments are computed in the space and absolute joint angles calculated between a body segment and the horizontal plane passing through the two hips and the two shoulders):
1) Datatime
2) Subjets (Sn, where n = 1,..12)
3) Kinect (K1, K2, K3 and K4)
4) Pathway (PATH1, PATH2, PATH3, and PATH4)
5) A_pitch (head pitch angle) 
6) A_roll (head roll angle)
7) B_pitch (trunk pitch angle)
8) B_roll (trunk roll angle)
9) ξ
10) µ2
11) δ2
12) Z_1
13) Z_c7
14) Z_hc
15) Labels (1, 2, 3, 4 and 5)

**All missing data (temporal holes between data frames) were filled in with the value ‘999’.**

**All Kinect Data are roto-translated to obtain data referred to an absolute reference system.**
![rotoT](https://user-images.githubusercontent.com/26774553/152385224-dc1a0633-fa70-4a13-b85a-4d9768d42396.svg)

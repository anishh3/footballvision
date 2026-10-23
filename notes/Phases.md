phase 1 - detection

Roboflow dataset
        ↓
TensorFlow model
        ↓
Evaluate
        ↓
Independent match video
        ↓
Annotated video


phase2 - tracking

Detector
   ↓
ByteTrack / BoT-SORT
   ↓
Persistent player IDs

phase 3 - team identification 

Player crops
      ↓
Team A / Team B


phase4 - Pitch Understanding
Pitch lines / keypoints
       ↓
Homography
       ↓
Player → pitch coordinates



Phase 5 — Tactical Analytics
2D player coordinates
        ↓
heatmaps
team shape
formation
movement
distance


Phase 6 — Football Events
ball trajectory
      ↓
passes
shots
possession
goals


Phase 7 — Deployment
Video
 ↓
Complete CV pipeline
 ↓
FastAPI
 ↓
Dashboard



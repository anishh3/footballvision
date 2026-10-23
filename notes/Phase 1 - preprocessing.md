                    FOOTBALLVISION
                         │
                         ▼
              ┌─────────────────────┐
              │ Choose Phase 1 goal │
              │ Object Detection    │
              └──────────┬──────────┘
                         │
                         ▼
              Find football dataset
                         │                                                
                         ▼
              Roboflow Football
              Detection Dataset
                         │
                         ▼
                 Download as COCO
                         │
                         ▼
        ┌────────────────────────────────┐
        │ Dataset structure               │
        │ train / valid / test            │
        └───────────────┬────────────────┘
                        │
                        ▼
              Inspect COCO JSON
                        │
             ┌──────────┴──────────┐
             ▼                     ▼
       images section         annotations section
             │                     │
             │                bbox + category_id
             │                     │
             └──────────┬──────────┘
                        ▼
                 Dataset analysis
                        │
           ┌───────────────┼────────────────┐
           ▼               ▼                ▼
        Class counts     Image sizes    Ball sizes
        │                 │                  │
        ▼                 ▼                  ▼
 
     player: 25161    1920 × 1080      median 11.8×12 px
     referee: 2694
     ball: 1323
     goalkeeper: 1017
                        │
                        ▼
              Check dataset quality
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
       Bounding boxes        Split overlap
        look correct          0 exact overlap
              │                   │
              └─────────┬─────────┘
                        ▼
                Define our classes
                        │
            ┌───────────┼───────────┐
            ▼           ▼           ▼
          ball      goalkeeper    player
                        │
                        ▼
                     referee
                        │
                        ▼
              Ignore unused class
              "players-ball-referee"
                        │
                        ▼
               Build COCO parser
                        │
                        ▼
         COCO [x,y,width,height]
                        │
                        ▼
          Convert to [y1,x1,y2,x2]
                        │
                        ▼
             Convert to TensorFlow
                  tensors
                        │
                        ▼
             Image + boxes + labels
                        │
                        ▼
             Visualize converted data
                        │
                        ▼
                 ✅ VERIFIED
 ![[Pasted image 20261008213550.png]]
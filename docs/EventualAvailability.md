```mermaid
flowchart BT
  subgraph iPhone1
    c1(STCiOSXDataCollector)
  end
  
  subgraph Linux1
    c2(STCX11DataCollector)
  end
  subgraph Android1
    c3(STCDroneDataCollector)
  end
  subgraph Cloud
    s[(STCDataServer)]
  end
    c1 & c2 & c3 -.->|NO CONNECTION| s
```

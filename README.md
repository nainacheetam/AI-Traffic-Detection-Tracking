## Traffic Analytics Dashboard

The dashboard presents the preliminary results of the vehicle detection and traffic volume analysis.

![Traffic Analytics Dashboard](Final_Traffic_Analytics_Dashboard.png)

### Key Results

- Total AI-recorded vehicle crossings: 29
- Cars: 25
- Buses: 4
- Observed traffic flow: 1.805 vehicles/second

*Note: Results are preliminary and have not yet been independently validated against manual counts.*
## Methodology

The project follows a computer vision-based traffic monitoring pipeline.

1. **Video Input:** Traffic footage is uploaded into Google Colab.
2. **Frame Processing:** OpenCV extracts individual frames from the video.
3. **Vehicle Detection:** YOLO11n detects vehicles and generates bounding boxes.
4. **Vehicle Classification:** Detected vehicles are classified into cars, motorcycles, buses and trucks.
5. **Object Tracking:** ByteTrack associates vehicle detections across successive frames using tracking IDs.
6. **Virtual Counting Line:** A predefined horizontal line is used to identify vehicle crossings.
7. **Event Recording:** Vehicle IDs, predicted categories, crossing times and directions are recorded.
8. **Traffic Analysis:** Pandas processes the event dataset, while Matplotlib generates the analytics dashboard.
9. ## Limitations
10. ## Future Improvements

The project can be extended through the following improvements:

1. **Manual Ground-Truth Validation:** Compare AI-generated vehicle counts with manually verified vehicle crossings.
2. **Longer Video Analysis:** Test the system on longer traffic recordings to study traffic patterns more reliably.
3. **Improved Detection:** Experiment with detection confidence thresholds and model configurations.
4. **Tracking Optimisation:** Improve tracking consistency and reduce ID fragmentation.
5. **Direction-Wise Analysis:** Analyse traffic volume separately for different movement directions.
6. **PCU-Based Analysis:** Extend vehicle composition analysis using Passenger Car Unit (PCU) factors.
7. **Traffic Density Estimation:** Explore vehicle density and congestion monitoring.
8. **Real-Time Monitoring:** Develop a system for processing live traffic camera feeds.

The current prototype has the following limitations:

1. **Short Video Duration:** The analysis uses approximately 16.07 seconds of traffic footage, which is insufficient for long-duration traffic studies.
2. **Detection Errors:** Some vehicles may be missed or incorrectly classified by the YOLO model.
3. **Tracking Fragmentation:** A vehicle may receive a different tracking ID if tracking is interrupted.
4. **Counting Uncertainty:** The AI-generated crossing count has not yet been independently validated against manual ground-truth counts.
5. **Limited Traffic Analysis:** Peak-hour traffic, hourly variation and congestion cannot be reliably determined from this short sample.
6. **Camera Dependency:** Detection performance may vary with camera angle, lighting, vehicle overlap and video quality.

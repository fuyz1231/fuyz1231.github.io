# In situ monitoring for laser based additive manufacturing
This project is about anomaly detection for metal laser-based additive manufacturing. The current main strategy is plotting the splatter contour on the optical images and then extracting the related information from the contour area to detect anomalies. The information we can get by tracking the splatter from the optical image is mean intensity, radius, area, center X moving path, and center Y moving path.

## Project Structure

```angular2html
📁 Dataset/                                                           # Datasets collected on the machine (LBAM system at the UofSC).
    📁 dataset1
        📁 Gcode_whole_product_with_same_power                        # Generated laser path for the whole product printed with the same power from G-code
            📄 Gcode_Whole_part.csv
            📄 whole part laser path.png
        📄 README.md
    📁 dataset2                                                       # laser path for the product inner and outring printed with different power from G-code
            📄 Gcode_Inner_outter_different.csv
            📄 Inner outter different power laser path.png
        📄 README.md

📁 LBAM_hardware/
    📁 buildplate/                                                    # Custom hardware setup developed for in-situ monitoring
    📁 buildplate/
    📁 custom_top_plate/
    📁 FLIR_optical/
    📁 laser_safety_lockout/
    📁 NIT_thermal/
    📁 Workswell_thermal/                                                
    📄 README.md
📁 Software/                                                          # Exploration code developed for this project
    📁 Feature tracking frames/                                       # Generated frames with outline through the code 
        📁 smallest_125w150mms_powder_frames/
        📄 Frames.png
        📄 README.md
    📁 Python code                                                    # python code for this project
        📄 get_frames_from_video.py
        📄 plot_area_intensity_radius.py
        📄 track_pool_from_images.py
        📄 README.md
📄 .gitignore                                                         # Files to ignore
```

## [Hardware setup for the LBAM system at the UofSC](LBAM_hardware)
Files related to the custom hardware developed for in situ monitoring
1. A building plate to fit the experimental needs is designed. The new plate can satisfy the setting up with the thermal and optical cameras.
2. The holders for the thermal cameras. There are two thermal cameras that will be used in the future: Workswell (WIC-336-DFUW) and NIT (WiDy SWIR 320). 
3. The holder for the optical camera (FLIR BFS-U3-16S2M-CS).

![Picture1](https://user-images.githubusercontent.com/48246423/157728697-24c5dc51-bab8-452f-adae-7da4745e3534.png)

![image](https://user-images.githubusercontent.com/48246423/157718688-0deab753-d56d-46ab-80b3-152ff86c0736.jpg)


## [Datasets](Datasets)
Datasets collected on the machine.

## [Software](Software)
Software Developed for this project.

## [References](References)
Related references for the project. You can also find the pdf format in the References folder.

[1] Berumen_2010_QualityControlLaser: Quality control of laser and powder bed-based additive manufacturing technologies

[2] Clijsters_2014_SituQualityControl: In situ quality control of the selective laser melting process using a high-speed, real-time melt pool monitoring system

[3] Everton_2016_ReviewSituProcess: Review of in-situ process monitoring and in-situ metrology for metal additive manufacturing

[4] FU_2022_MLAlgorithm: Machine learning algorithms for defect detection in metal laser-based additive manufacturing: A review

[5] Furumoto_2012_MonitoringLaserConsolidation: Monitoring of laser consolidation process of metal powder with high speed video camera

[6] Ye_2021_InSituAM: Deep Learning for Inter-Layer Classification During In-situ Quality Control of Additive Manufactured Parts



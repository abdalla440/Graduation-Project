

# Graduation project (ODM)

## What is ODM

Orbit Determination manager (ODM): a full orbit calculation software package.

**ODM** provides the data needed for the ground station's **Flight Control Center (FCC)** which is the main control and satellite data provider system in the ground station.

#### Flight Control Center (FCC):

The **FCC** Consists of many subsystems the most important is the _"orbit subsystem"_ because it is the one responsible for providing the data about satellite position, tracking, possible contacts

#### Orbit determination process:

As mentioned the orbit subsystem is responsible for satellite tracking so we could say it is the eye of the station in the sky and it is the one who:

-   tells the ground station's antenna where to point and when.
-   when the satellite is above a certain area or where it will be in x time.
-   and more...

## Functionality

The application provides the following main functionality:

-   Fined satellite position, velocity in the orbit at an exact moment
-   Predict satellite orbit for a period: which is the satellite position in space relative to earth’s ITRS reference frame.
-   Calculate and visualize the satellite Ground track: which is the satellite path projection on the earth, the surface considering the earth's rotation.
-   Calculate and visualize satellite RVZ (radio visibility zones): in which satellite is available to connect with the ground station’s antenna.
-   Real-Time satellite ground track tracking

## Data Accuracy

the accuracy of data provided with the application is 99.999% compared to real trusted standard data (provided from [STK](https://www.agi.com/products/stk) ). the following figures show data comparison of 360,000 rows for 4 days of data calculation between "ODM", "STK" :

### satellite orbit prediction (data sample & error average)

![orbit](https://user-images.githubusercontent.com/58492759/185061500-9a53028a-b085-4262-badb-282b3f3850fc.png)

![orbiterror](https://user-images.githubusercontent.com/58492759/185061505-5df3b270-1101-428d-af65-c87970d053cc.png)


### satellite Ground tracking (data sample & error average)

![ground](https://user-images.githubusercontent.com/58492759/185061440-f52a64d0-638f-437c-8df0-74d72c6bbb45.png)

![grounderror](https://user-images.githubusercontent.com/58492759/185061447-ba8d97a0-36f1-419e-9ac9-3ce7eda93697.png)


### satellite radio visibility zones (data sample & error average)

![rvz](https://user-images.githubusercontent.com/58492759/185061543-4df56676-87b9-401a-b409-891d3ad5b029.png)

![rvzerror](https://user-images.githubusercontent.com/58492759/185061548-cfff68d3-6561-4945-9aeb-450c2bed6a20.png)


## Demo

[Orbit Determenation Manager (Demo)](https://drive.google.com/file/d/1YbNZPa-mL91QArUInBbEiQdZCrOgMUHa/view?usp=sharing)

## ODM's Maniual

### **Login**

![login](https://user-images.githubusercontent.com/58492759/185058080-86887fb9-1a29-44f3-9173-256f314e0523.png)

### **Home page**

![home](https://user-images.githubusercontent.com/58492759/185058099-e4839ff6-7ee2-4389-b06b-31a812f92621.jpg)

### **Admin dashboard**
This page for admin to control all data in the system (Add, Update, delete users and to view all users)  

in our case the user is an admin, so the admin menu is available for him In admin dashboard:  
1. Add button to add new user.  
2. Update button to update existing users.  
3. Delete button to delete users.  
4. User info panel to get data for new users or change data of  existing users.  
5. Users table to view all users in database.

![admin](https://user-images.githubusercontent.com/58492759/185058128-54ea7242-558c-41b5-9c16-a7fdbd4f17db.png)

### **Satellite TLE**
This page to show which TLE is selected from database giveing the following insights:  
1. Satellite selection input panel.  
2. TLE page.  
3. Active TLE three lines.  
4. Active TLE initial position and velocity.  
5. Active TLE details.  
6. Selected satellite available TLE sets. 
 
![tle](https://user-images.githubusercontent.com/58492759/185058160-ee73e7ae-a249-4783-a9d5-13f7a3792b43.png)

### **Ground-track**
This page shows the map world, satellite position, satellite orbit, all information panels and all reports panels.  
When doing Ground track for a satellite the Ground tab is opened and gives the following insights:  
1. Ground track input panel.  
2. Map of the world that show:  
• Satellite position on the earth (denoted by red point).  
• satellite orbit which the selected point is part of (denoted by red  curve).  
3. Animation control panel (timeline).  
17. information panel:  
• ground track calculation starts and end time.  
• Total number of orbit satellite do in this calculation period.  
• Current orbit displayed on the map (of the selected point).  
. • Longitude, latitude, time (of the currently selected point).  
18. Ground track pointes table (time, longitude, latitude).  
19. Reports panel:  
• Get report button to report a .word file.  
• Export csv button to report a .csv file of the propagation.  
• Search by position button.  
• Search by time button.  
20. Options panel that has two modes:  
• Animation mode and you can optimize:  
• number of orbits to display.  
• Point-time mode in it you can search with:  
• Position (search to know when satellite pass on a certain  position).  
• Position (search to know where satellite will be in a specific  time).

![groundpage](https://user-images.githubusercontent.com/58492759/185058191-dce251d5-ccb1-4da8-997b-83baa351ef0b.png)

### **RVZ**
This page shows session visualization figure, session acquisition time (AOS), session lose time (LOS), session duration insights, reports panel  
When doing RVZ for a satellite the RVZ tab is opened and gives the following insights:  
1. RVZ input panel.  
2. Session visualization figure.  
3. Elevation visualization figure.  
4. Available sessions table.  
5. Information panel:  
• Session Acquisition time (AOS).  
• Session Lose time (LOS).  
• Session Duration.  
• Session maximum Elevation angle (Max-Elv).  
6. insights panel:  
• session duration progress bar.  
• maximum Elevation angle progress bar.  
• how much this session is recommended to connect satellite at.  
7. Reports panel:  
• Get the report button to report a .word file.  
• Export csv button to report a .csv file of the propagation

![rvzpage](https://user-images.githubusercontent.com/58492759/185058232-00a49ad7-79cc-420d-a49c-97fdb9b3aa3c.png)

### **Orbit propagation**

This page shows propagation pointes table and orbit propagation input panel. 

When doing Orbit propagation for a satellite the Orbit  tab is opened and give the following insights: 
1.  Orbit propagation input panel. 
2.  Propagation pointes table (time, position: x y z, velocity: x y z). 
3.  Information panel show details of the selected point. 
4.  Reports panel: 
-   Get the report button to report a .word file.
-   Export csv button to report a .csv file of the propagation.
5.  Satellite orbit display area and its control panel (reserved for future work).

![orbitpage](https://user-images.githubusercontent.com/58492759/185058733-6d50639d-f0e1-4ee9-aa00-a548ba21a95f.png)

### **Database dashboard**

![databasecity](https://user-images.githubusercontent.com/58492759/185058824-f65948e6-e6d9-4d27-98c5-f755e485ceb6.jpg)

![databasesatellite ](https://user-images.githubusercontent.com/58492759/185058828-771cc876-53d1-4a10-bb7c-397837888aa1.jpg)

![databasestation](https://user-images.githubusercontent.com/58492759/185058830-8e216a93-6e72-4305-b4ac-ca2580b9f2a2.jpg)


### **Session countdown**

![counter](https://user-images.githubusercontent.com/58492759/185058872-abd673bc-86af-420c-8c32-5053dba241e7.jpg)

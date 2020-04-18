# iLectureOnline-01-Kalman-Filter
Kalman Filter topic on iLectureOnline

### Lecture 2: Flowchart Of A Simple Example (Single Measured Value)

- Tree main calculation
  - Calculate the kalman gain
    - Need error in estimate
    - Nedd error in data input (measurement)
  - Calculate current estimate
    - Need previous estimate (calulated before)
    - Need data input (measurement)
  - Calculate new error in estimate
  
### Lecture 4: The 3 Calculations Of The Kalman Filter

- Kalman gain = error of estimate / (error of measuremenf + eror)
- Current estimate = previous estimate + KG * (new measurement - previous estimate)
- Current error of estimate = (error of measurement * previous error of estimate) / (error of measurement + previous error of estimate) = (1 - KG) * previous error of estimate


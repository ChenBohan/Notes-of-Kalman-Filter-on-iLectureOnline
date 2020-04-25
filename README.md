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

### Lecture 18: What Is A Covariance Matrix?

```
P[k] = A * P[k-1] * A[-1] + Q
K[k] = P[k] * H[T] / H * P[k] * H[T] + R
```

- P
  - State covariance matrix
  - Errro in estimate
- Q
  - Process noise covariance matrix
  - Keeps the state covariance matrix from becoming too small or going to zero
- R
  - Measurement covariance matrix
  - Error in measurement
- K
  - KG
  - Weight factor based on comparing the error in the estimate to the error in the measurement

### Lecture 23: Finding The Covariance Matrix, Numerical Example

- Deviation matrix: a = A - I * A * 1 / num

- Covariance matrix = a[T] * a

### Lecture 26: Flow Chart Of 2-D Kalman Filter - Tracking Airplane

- Process errors in process covariance matrix
  - usually we start out by simply giving them some initial reasonable value
- Transformation matrix H
  - Transform the format of matrix P to the format of KG matrix

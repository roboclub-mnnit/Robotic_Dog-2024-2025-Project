# Robotic Dog
### Manipulator diagram

![manipulator diagram](https://github.com/user-attachments/assets/9b4d97b2-c81c-4415-b9cb-c7aa37436ce1)


### Rotation matrices
    R0_1 = np.array([[-np.sin(T1), 0, np.cos(T1)],
                     [np.cos(T1),  0, np.sin(T1)],
                     [0,           1,          0]])

    R1_2 = np.array([[np.cos(T2), -np.sin(T2), 0],
                     [np.sin(T2),  np.cos(T2), 0],
                     [0,           0,          1]])

    R2_3 = np.array([[1, 0, 0],
                     [0, 0, 1],
                     [0, -1, 0]])

### Displacement vectors
    D0_1 = np.array([[a1 * np.cos(T1)], [a1 * np.sin(T1)], [0]])
    D1_2 = np.array([[a2 * np.cos(T2)], [a2 * np.sin(T2)], [0]])
    D2_3 = np.array([[a3 * np.cos(T3)], [a3 * np.sin(T3)], [0]])

### Homogeneous transformation matrices
    H0_1 = np.concatenate((R0_1, D0_1), axis=1)
    H0_1 = np.concatenate((H0_1, [[0, 0, 0, 1]]), axis=0)

    H1_2 = np.concatenate((R1_2, D1_2), axis=1)
    H1_2 = np.concatenate((H1_2, [[0, 0, 0, 1]]), axis=0)

    H2_3 = np.concatenate((R2_3, D2_3), axis=1)
    H2_3 = np.concatenate((H2_3, [[0, 0, 0, 1]]), axis=0)
    

    H0_2 = np.dot(H0_1, H1_2)
    H0_3 = np.dot(H0_2, H2_3)

### Angles
For right leg, T1 varies from -90 to +90; T2 and T3 vary from 0 to 180

For left leg, T1 varies from 90 to 270; T2 and T3 vary from 0 to 180

### Other Information
The front of the bot coincides with XY plane.

Offset - 1 cm in x direction and 8.5 cm in z direction

## Photo Gallery
![Robotic Dog 1](https://github.com/user-attachments/assets/4d83a174-1096-4905-bac9-b160f455b128)

For Right front leg,
float x = x_centre - 1;
float y = y_centre;
float z = z_centre - 8.5;

For Right rear leg,
float x = x_centre - 1;
float y = y_centre;
float z = z_centre + 8.5;

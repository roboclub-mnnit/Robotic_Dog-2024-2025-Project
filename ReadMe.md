### Manipulator Diagram
![Manipulator diagram (2)](https://github.com/user-attachments/assets/9a57f824-aab2-4efb-a61f-38d54a75ae4b)


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


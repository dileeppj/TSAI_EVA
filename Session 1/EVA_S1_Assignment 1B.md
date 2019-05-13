## EVA-S1_Assignment 1B

**Q1. What is Channels and Kernels?**
**A1.**
**<u>Kernels</u>**
Filters/ Kernels are feature extractors which help to extract the features in an image, the features may be different types of edges (horizontal, vertical, curved etc.). Filters are used to extract these features from an image by convolution. When the filters are convoluted over an image, we will get a collection of similar features from the image.

​	![Image result for edge detection neural network](https://s3.amazonaws.com/quantstart/media/images/qs-deep-learning-alex-net-kernels.jpeg)

**<u>Channels</u>**
When the Filters / Kernels are convoluted over an image, we will get a collection of similar features from the image, this bag of similar feature is called channel. Channel is the similar feature bag. If we have 40 kernels we will have 40 channels, each channel will have only that feature



**Q2. Why do we only (well mostly) use 3x3 kernels ?**
**A2**. We mostly use 3x3 kernels because of many reasons described below:

* We can do any other odd convolution (we use odd as it has a central line of distinction) using 3x3 kernel such as 5x5, 7x7 etc. 5x5 is two times of 3x3. Using 5x5 or above is not preferred as it is lot slower and uses more memory than 3x3.

* Most of the GPU are optimized for working on 3x3 kernels



**Q3. How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations).**
**A3.** We need to perform 99 3x3 convolution operation to reach 1x1 from 199x199.
<u>**Calculation**</u>
Count #1 : (199x199) * (3x3) -> (197x197)
Count #2 : (197x197) * (3x3) -> (195x195)
Count #3 : (195x195) * (3x3) -> (193x193)
Count #4 : (193x193) * (3x3) -> (191x191)
Count #5 : (191x191) * (3x3) -> (189x189)
Count #6 : (189x189) * (3x3) -> (187x187)
Count #7 : (187x187) * (3x3) -> (185x185)
Count #8 : (185x185) * (3x3) -> (183x183)
Count #9 : (183x183) * (3x3) -> (181x181)
Count #10 : (181x181) * (3x3) -> (179x179)
Count #11 : (179x179) * (3x3) -> (177x177)
Count #12 : (177x177) * (3x3) -> (175x175)
Count #13 : (175x175) * (3x3) -> (173x173)
Count #14 : (173x173) * (3x3) -> (171x171)
Count #15 : (171x171) * (3x3) -> (169x169)
Count #16 : (169x169) * (3x3) -> (167x167)
Count #17 : (167x167) * (3x3) -> (165x165)
Count #18 : (165x165) * (3x3) -> (163x163)
Count #19 : (163x163) * (3x3) -> (161x161)
Count #20 : (161x161) * (3x3) -> (159x159)
Count #21 : (159x159) * (3x3) -> (157x157)
Count #22 : (157x157) * (3x3) -> (155x155)
Count #23 : (155x155) * (3x3) -> (153x153)
Count #24 : (153x153) * (3x3) -> (151x151)
Count #25 : (151x151) * (3x3) -> (149x149)
Count #26 : (149x149) * (3x3) -> (147x147)
Count #27 : (147x147) * (3x3) -> (145x145)
Count #28 : (145x145) * (3x3) -> (143x143)
Count #29 : (143x143) * (3x3) -> (141x141)
Count #30 : (141x141) * (3x3) -> (139x139)
Count #31 : (139x139) * (3x3) -> (137x137)
Count #32 : (137x137) * (3x3) -> (135x135)
Count #33 : (135x135) * (3x3) -> (133x133)
Count #34 : (133x133) * (3x3) -> (131x131)
Count #35 : (131x131) * (3x3) -> (129x129)
Count #36 : (129x129) * (3x3) -> (127x127)
Count #37 : (127x127) * (3x3) -> (125x125)
Count #38 : (125x125) * (3x3) -> (123x123)
Count #39 : (123x123) * (3x3) -> (121x121)
Count #40 : (121x121) * (3x3) -> (119x119)
Count #41 : (119x119) * (3x3) -> (117x117)
Count #42 : (117x117) * (3x3) -> (115x115)
Count #43 : (115x115) * (3x3) -> (113x113)
Count #44 : (113x113) * (3x3) -> (111x111)
Count #45 : (111x111) * (3x3) -> (109x109)
Count #46 : (109x109) * (3x3) -> (107x107)
Count #47 : (107x107) * (3x3) -> (105x105)
Count #48 : (105x105) * (3x3) -> (103x103)
Count #49 : (103x103) * (3x3) -> (101x101)
Count #50 : (101x101) * (3x3) -> (99x99)
Count #51 : (99x99) * (3x3) -> (97x97)
Count #52 : (97x97) * (3x3) -> (95x95)
Count #53 : (95x95) * (3x3) -> (93x93)
Count #54 : (93x93) * (3x3) -> (91x91)
Count #55 : (91x91) * (3x3) -> (89x89)
Count #56 : (89x89) * (3x3) -> (87x87)
Count #57 : (87x87) * (3x3) -> (85x85)
Count #58 : (85x85) * (3x3) -> (83x83)
Count #59 : (83x83) * (3x3) -> (81x81)
Count #60 : (81x81) * (3x3) -> (79x79)
Count #61 : (79x79) * (3x3) -> (77x77)
Count #62 : (77x77) * (3x3) -> (75x75)
Count #63 : (75x75) * (3x3) -> (73x73)
Count #64 : (73x73) * (3x3) -> (71x71)
Count #65 : (71x71) * (3x3) -> (69x69)
Count #66 : (69x69) * (3x3) -> (67x67)
Count #67 : (67x67) * (3x3) -> (65x65)
Count #68 : (65x65) * (3x3) -> (63x63)
Count #69 : (63x63) * (3x3) -> (61x61)
Count #70 : (61x61) * (3x3) -> (59x59)
Count #71 : (59x59) * (3x3) -> (57x57)
Count #72 : (57x57) * (3x3) -> (55x55)
Count #73 : (55x55) * (3x3) -> (53x53)
Count #74 : (53x53) * (3x3) -> (51x51)
Count #75 : (51x51) * (3x3) -> (49x49)
Count #76 : (49x49) * (3x3) -> (47x47)
Count #77 : (47x47) * (3x3) -> (45x45)
Count #78 : (45x45) * (3x3) -> (43x43)
Count #79 : (43x43) * (3x3) -> (41x41)
Count #80 : (41x41) * (3x3) -> (39x39)
Count #81 : (39x39) * (3x3) -> (37x37)
Count #82 : (37x37) * (3x3) -> (35x35)
Count #83 : (35x35) * (3x3) -> (33x33)
Count #84 : (33x33) * (3x3) -> (31x31)
Count #85 : (31x31) * (3x3) -> (29x29)
Count #86 : (29x29) * (3x3) -> (27x27)
Count #87 : (27x27) * (3x3) -> (25x25)
Count #88 : (25x25) * (3x3) -> (23x23)
Count #89 : (23x23) * (3x3) -> (21x21)
Count #90 : (21x21) * (3x3) -> (19x19)
Count #91 : (19x19) * (3x3) -> (17x17)
Count #92 : (17x17) * (3x3) -> (15x15)
Count #93 : (15x15) * (3x3) -> (13x13)
Count #94 : (13x13) * (3x3) -> (11x11)
Count #95 : (11x11) * (3x3) -> (9x9)
Count #96 : (9x9) * (3x3) -> (7x7)
Count #97 : (7x7) * (3x3) -> (5x5)
Count #98 : (5x5) * (3x3) -> (3x3)
Count #99 : (3x3) * (3x3) -> (1x1)
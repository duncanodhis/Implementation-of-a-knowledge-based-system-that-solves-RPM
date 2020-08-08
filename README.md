# Implementation-of-a-knowledge-based-system-that-solves-RPM
This  agent solves ravens progressive matrices using pillow and not any other third party library in python
Logical transformation were performed in the first two images in a row or a column then it is compared with the third image for similarity for example XOR(A,B) was compared against C and XOR(D,E) was compared against F.Incase the first two logical operation were similar then my agent assumes an answer has been found but first it is checked for match with XOR(G,H)
I decided to use the following equation as a way of determine the percentage difference for similarity check .
[(a+b)*½]\(a-b) 
I decided to set a similarity threshold for pixels of identical image to reduce time used in checking for this similarity.
For problems D-02,D-03 had ordered patterns in 3 shapes for example D-02 my agent takes pixels in row and column then compares them.That is ABC is compared to DEF and DEF to GH# .The patterns obtained should be maintained in all cases so that # can match with what it has suggested.A second check is done to correct any shape mistake that might occur when a diagonal comparison is done.
For problems like D-07 my agent was capable of identifying a diagonal symmetry in GEC then a pattern was generated ,this pattern is was also identified and used in AE#  ,when checked diagonally BD ,HF had a diagonal symmetry too.This prompted my agent to give an answer based on that symmetry.
For problem D-08 a diamond shape was the object of interest in pattern identification ,it showed me that there was just a single filled shape diagonally.
Problems with consistent diagonal images such as D-06,D-07,D-09,D-10,D-12
For example D-06 my agent was capable of measuring pixel difference e.g A-E had a similarity difference when compared to E-#.This created some difficulty since outward shapes of A and E interfered with differences in pixel so I was prompted to add pixel for each row and column then result of this difference is compared .That is row one is compared against row 2 two then second row is compared against the third one .This would create an alternation that will eventually give out an answer.
For problems like E-13 my agent tried doing a logical operation at first but found that it was not feasible approach to solving this problem.So I decided that it will do pixel subtraction specifically black pixels in ABC ,a pattern difference from ABC was identified in DEF.Now based on this my agent did a black pixels subtraction in GH#  to identify an answer.




<!-- INTRODUCTION -->
<br />

![SLAM (Simultaneous Location and Mapping) - Gem Finder Project](/assets/title.jpg?raw=true "Index")

  <p align="center">
    An implementation of the online SLAM algorithm to find a path through an unknown map using only measurements between landmarks (gems) and the craft, and our sense of movement, to find our way to each landmark.
  </p>
</p>

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Slam in Practice](#slam-in-practice)
* [Powered by Python](#built-with)
* [License](#license)
* [Contact](#contact)

<!-- ABOUT THE PROJECT -->
## About The Project

This is a really cool implementation of a SLAM (Simultaneous Location and Mapping) algorithm. Our robot is armed without a map of the environment but with sensors that indicate the distance to any gems within a certain distance (our radar can only see so far!)

We are tasked by our commander to retrieve a list of gems, which can be collected in any order and only one of each type needs to be collected. Wasting time extracting dirt can be deadly, so the craft needs to be precise. The craft can also only rotate up to 90 degrees at a time so we have to be careful not to overshoot!

But what about when we don't see any of the gems? Then, I have implemented an outward spiral search from the robot's current location, which loops outward until it sees a new gem.

Due to proprietary code restrictions, I cannot publicly share the code other than a short overview!


## SLAM in Practice

We are tasked with finding and retrieving gems A, M, and D without a map. There are several other gems in the map but we only need to extract these three. 

The little dot in a box indicates when that gem has been seen, and the letter is "ticked off" the top when one is successfully extracted. I've also printed some output at each step so we can see what the robot is currently trying to achieve. 

![Craft Navigation to Each Gem](/assets/navigation.gif?raw=true "Craft Navigation to Each Gem")

We can see the robot head to the first gem it sees, then spiral until it sees the next available gem. It extracts the next gem before it heads to the final one in the sequence. 

We can also see that at first, the only gem the robot can see is the gem "A", and as soon as it sees the next gem, "M" it heads there. Once M is extracted, it heads to D. 

Once it's found all three gems, we exit out of the simulation!

## Built With
This project was built in Python version 3.8.3 and using a proprietary matrix class which allows us to compute Cholesky factorization and expand and contract matrices as needed for online SLAM.

<!-- LICENSE -->
## License
Not distributed for public use.

<!-- CONTACT -->
## Contact
Jasmine Sondhi - [LinkedIn](https://www.linkedin.com/in/jasmine-sondhi/) - jsondhi@outlook.com

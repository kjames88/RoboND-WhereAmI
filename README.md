# RoboND-WhereAmI

### Moment of inertia for wheels
link: https://en.wikipedia.org/wiki/List_of_moments_of_inertia
Solid cylinder model with radius 0.2 and height 0.1

Prior to adjusting the inertia values from the udacity_bot defaults, the large-wheeled robot had a pronounced dive periodically as the robot presumably reduced its velocity.  Some hint remains but is much less apparent.

### Localization accuracy

Using diff_corrected the parameters alpha1 - alpha5 must be updated.  The fact that the default values correspond to the uncorrected algorighm is mentioned in the ROS documentation.  Link:  https://answers.ros.org/question/227811/tuning-amcls-diff-corrected-and-omni-corrected-odom-models/

The values used are only slightly tuned but show a clear improvement in localization performance.  In retrospect, it is clear that the particle filter performance must depend on the platform odometry calculations since the measurement probabilities are computed using the pose of the robot.  Several hours of frustration preceded this realization.


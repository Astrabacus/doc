Specific Plugins
=======================

Over the time, many components have been implemented in SOFA. 
Some of these components are specific and allows for a particular functionality.
They have been repackaged into plugins that can be activated / deactivated in the compilation of SOFA.

In this documentation, you will find a brief description of these plugins

### Specific Boundary Conditions
This plugin gathers components that inherit from Forcefields and Projective Constraints.
Here is the list of the components and their function:

- **AffineMovementConstraint** no description available: copy of PatchTestMovementConstraint (deprecated)
- **ConicalForceField** creates conical walls using penalty forces
- **DiagonalVelocityDampingForceField** creates damping forces. It allows to set specific coefficient of damping for each node and in each direction.
- **EdgePressureForceField** spread a pressure force on edges
- **EllipsoidForceField** creates ellipsoid walls using penalty forces
- **FixedPlaneConstraint** Specific implementation of partialFixedConstraint to fix a plane
- **FixedRotationConstraint** Specific implementation of partialFixedConstraint to fix the rotation on rigidtypes
- **FixedTranslationConstraint** Specific implementation of partialFixedConstraint  ot fix the translation on rigidtypes
- **HermiteSplineConstraint** Impose a trajectory to given Dofs following a Hermite cubic spline constraint.
- **LinearForceField** Apply forces changing to given degres of freedom. Some keyTimes are given and the force to be applied is linearly interpolated between keyTimes
- **LinearMovementConstraint** impose a displacement to given DOFs (translation and rotation). The motion between 2 key times is linearly interpolated
- **LinearVelocityConstraint** impose a velocity to given DOFs (translation and rotation)	The motion between 2 key times is linearly interpolated
- **OscillatingTorsionPressureForceField** was developped for creating an oscillating torsion (used in the [paper](http://www-sop.inria.fr/asclepios/Publications/Stephanie.Marchesseau/PBMB-Marchesseau-2010.pdf) )
- **OscillatorConstraint** Apply sinusoidal trajectories to particles.
- **ParabolicConstraint** Apply a parabolic trajectory to particles going through 3 points specified by the user.
- **PartialLinearMovementConstraint** impose a motion to given DOFs (translation and rotation) in some directions only.
- **PatchTestMovementConstraint** Impose a motion to all the boundary points of a mesh. The motion of the 4 corners are given in the data cornerMovements and the movements of the edge points are computed by linear interpolation.
- **PointConstraint** Attach given particles to their initial positions. This is a temporary class, somehow redundant with FixedConstraint, simplified to avoid the memory leak issue.
- **PositionBasedDynamicsConstraint** Position-based dynamics as described in [Muller06]: input: target positions X  ( x(t) <- x(t) + stiffness.( X - x(t) )    v(t) = v(t) + stiffness.( X - x(t) ) /dt )
- **ProjectDirectionConstraint** Project particles to an affine straight line going through the particle original position.
- **ProjectToLineConstraint** Project particles to an affine straight line.
- **ProjectToPlaneConstraint** Project particles to an affine plane.
- **ProjectToPointConstraint** Attach given particles to their initial positions. Contrary to FixedConstraint, this one stops the particles even if they have a non-null initial velocity.
- **QuadPressureForceField** Implements a pressure force applied on a quad surface. (Redundant with SurfacePressureForceField). Does not implement AddKToMatrix (so it doesn't work with direct solvers.
- **SkeletalMotionConstraint** impose a specific motion (translation and rotation) for each DOFs of a MechanicalObject based on a skeletal motion description
- **SphereForceField** creates sphere walls using penalty forces
- **TorsionForceField**   This forcefield applies a torque to a set of selected nodes. The force is applied from a specified axis (origin and direction) and a torque value.
- **UniformVelocityDampingForceField** creates damping forces. Contrary to DiagonalVelocityDampingForceField the damping coefficient is uniform for each node and in each direction.


### Specific User Interaction
This plugin gathers some components that are used to define some specific interaction using the mouse

- **AddRecordedCameraPerformer** Save the current camera's position and orientation in the appropriate Data of Recorded Camera for navigation
- **FixParticlePerformer** Fix the points that are grabbed by the mouse 
- **InciseAlongPathPerformer** Incise along the path defined by cliking on the mouse. It works only with triangles.
- **RemovePrimitivePerforme** Remove the primitives picked by the mouse.
- **StartNavigationPerformer** 
- **SuturePointPerformer** create a spring between simulated object picked by the mouse


### SOFA LM Constraint
This plugin gathers the following LM components :
- **BarycentricDistanceLMConstraintContact**
- **DOFBlockerLMConstraint**
- **FixedLMConstraint**
- **DistanceLMContactConstraint**
- **DistanceLMConstraint**
- **LMConstraintSolver**
- **LMConstraintDirectSolver**






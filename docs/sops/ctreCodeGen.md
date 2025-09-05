# CTRE Code Gen Steps

This is a step-by-step guide to generating swerve code for a new robot.

***Assumptions:***
- Robot is built and fully wired, but not IDed
- Rio and radio are configured
- Battery is in place and securely attached

## **Step 1 - Devices**
- Place robot on blocks or a cart where the wheels are freely moving but not touching the floor
- Open Phoenix Tuner X and establish connection to the robot
- Make a decision on which side will be the "front" (it is recommended to label this)
- For each device:
  - Blink the device and identify where it is on the robot
  - Follow the guide below for the ID:
    - All IDs are **two digit numbers**
    - First digit (tens place) is the swerve module
      - Front left = 1
      - Front right = 2
      - Back left = 3
      - Back right = 4
      - Not on swerve module = 0 or 5
    - Second digit (ones place)
      - Drive motor = 1
      - Angle motor = 2
      - CANcoder = 3
      - Other = 4-9 as needed
  - Follow the naming scheme below for the name:
      - All words in camelCase, except for CAN which is all caps
      - Module is first
      - Then "Drive" for drive motors, "Angle" for the steering/angle motors, or "CAN" for CANcoders
        - Other devices can be named up to preference
      - Example: The drive motor on the front left module would be "frontLeftDrive"
- Make any firmware updates if needed
- (Apply licenses?)

## **Step 2 - Generate Swerve Code**
- Navigate to the "Mechanisms" tab on Phoenix Tuner X
- Make appropriate measurements:
  - If not already known, talk to Mr. Rivera/Build team for the swerve module manufacturer and type
  - For wheel radius and gear ratio, check the specific spec sheets for the swerve modules found on the WCP/SDS website
    - Example: Spec sheet for WCP X2i found [here](https://wcproducts.com/products/swerve-x2i)
  - Use a ruler or measuring tape to measure the module distances, measuring using the centers of the CANcoders as endpoints
- Click "New Project"
- Be sure to have drive station open 
- From this point on, carefully follow all instructions
  - Notes: When aligning wheels for zeroing CANcoders, use either a meter/yard stick or an aluminum bar

## **Step 3 - Modify Code** 
- Go to the `TunerConstants.java` file (Inside `src\main > java\frc\robot > generated`) and comment out the KS, KV, and KA value assignments

  **Original (values may differ):**
  
  ```java
  private static final Slot0Configs steerGains = new Slot0Configs()
    .withKP(100).withKI(0).withKD(0.5)
    .withKS(0.1).withKV(2.66).withKA(0)
    .withStaticFeedforwardSign(StaticFeedforwardSignValue.UseClosedLoopSign);
  // When using closed-loop control, the drive motor uses the control
  // output type specified by SwerveModuleConstants.DriveMotorClosedLoopOutput
  private static final Slot0Configs driveGains = new Slot0Configs()
    .withKP(0.1).withKI(0).withKD(0);
    .withKS(0).withKV(0.124);
  ```

  **Changed:**

  ```java
  private static final Slot0Configs steerGains = new Slot0Configs()
    .withKP(100).withKI(0).withKD(0.5)
    // .withKS(0.1).withKV(2.66).withKA(0)
    .withStaticFeedforwardSign(StaticFeedforwardSignValue.UseClosedLoopSign);
  // When using closed-loop control, the drive motor uses the control
  // output type specified by SwerveModuleConstants.DriveMotorClosedLoopOutput
  private static final Slot0Configs driveGains = new Slot0Configs()
    .withKP(0.1).withKI(0).withKD(0);
    // .withKS(0).withKV(0.124);
  ```

- Go to the `RobotContainer.java` file (Inside `src\main > java\frc\robot`) and add deadzones and smooth joystick movement

  **Original:**
  
  ```java
  drivetrain.applyRequest(() ->
    drive.withVelocityX(-joystick.getLeftY() * MaxSpeed) // Drive forward with negative Y (forward)
       .withVelocityY(-joystick.getLeftX() * MaxSpeed) // Drive left with negative X (left)
       .withRotationalRate(-joystick.getRightX() * MaxAngularRate) // Drive counterclockwise with negative X (left)
  )
  ```
  
  **Changed:**
  
  ```java
  drivetrain.applyRequest(() ->
    drive.withVelocityX(Math.abs(joystick.getLeftY()) < 0.075 ? 0 : Math.pow(joystick.getLeftY(), 3) * MaxSpeed) // Drive forward with negative X (forward)
      .withVelocityY(Math.abs(joystick.getLeftX()) < 0.075 ? 0 : Math.pow(joystick.getLeftX(), 3) * MaxAngularRate) // Drive left with negative Y (left)
      .withRotationalRate(Math.abs(joystick.getRightX()) < 0.075 ? 0 : -1 * Math.pow(joystick.getRightX(), 3) * MaxSpeed) // Drive counterclockwise with negative X (right)
  )
  ```

- Make changes to deadzone values as needed (the `0.075` number)

## **Step 4 - Test and Make Adjustments**
- Test drive
  - Connect your controller and enable the robot
  - Press the B button to orient the robot in the direction you are facing
  - Push the left joystick up very slightly and check that all of the wheels are slowly driving in the forward direction
  - Place robot on the floor and use the right joystick to test that the robot rotates in the correct directions
  - Do a quick test drive using both joysticks and adjust driving speed, deadzones, and PIDs to you or the drive team's liking
- Troubleshooting
  - If the robot's driving is inverted, go into the previous code block and add/remove `-1 *` before the `Math.pow()`
  - If the robot is jittery/moving without joystick input, increase the deadzone values







  
    

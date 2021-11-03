/*
        Josiah Taylor
        Arjun Krishna
*/

//1- Gyro, 2 - US, 3 - Colour
// 5 is red; 2 is blue; white is 6

task main()
{
        displayString(3,"Tues 12:00 16");

        int numOfBlueTiles= 0;
        double widthOfLongestRedTile = 0;
        double totalTravelTime = 0;

        SensorType[S1] = sensorEV3_Gyro;
        SensorType[S2] = sensorEV3_Ultrasonic;
        SensorType[S3] = sensorEV3_Color;

        wait1Msec(50)
        SensorMode[S3] = modeEV3Color_Color;



        //Wait for button press
        while(!getButtonPress(buttonEnter))
        {}

        while(getButtonPress(buttonEnter))
        {}
        time1[T1] = 0;

        //Get starting colour (should be white):
        int initialColour = (int)SensorValue[S3];
        motor[motorA] = motor[motorD] = 40;

        //While we are on the white tile:
        while(SensorValue[S3] == initialColour)
        {}

        wait1Msec(50);

        //If tile is blue and Ganondorf is closer than 40 cm go into loop:
        do
        {
                int tileColour = (int)SensorValue[S3];
                double widthOfThisRedTile = 0;

                nMotorEncoder[motorA] = 0;
                //While the tile is red stay at 40:
                while(  tileColour == 5 )
                {}

                widthOfThisRedTile = nmotorEncoder[motorA]*(PI*2.75)/180;

                if(widthOfThisRedTile > widthOfLongestRedTile)
                {
                        widthOfLongestRedTile = widthOfThisRedTile;
                }

                motor[motorA] = motor[motorD] = 10;

                int tileColour = (int)SensorValue[S3];

                //While the tile is blue stay at 10:
                int thisBlue = numOfBlueTiles;
                while(tileColour == 2)
                {
                        if(numOfBlueTiles == thisBlue)
                                numOfBlueTiles += 1;
                }

                //Once the tile is no longer blue
                motor[motorA] = motor[motorD] = 40;
        } while((int)SensorValue[S3] != 6);


        displayString(4, "%d", numOfBlueTiles );
        displayString(5, "%d", widthOfLongestRedTile);
        displayString(5, "%d", timer1[T1]);

        for(int i = 0; i<8 ; i++)

                motor[motorA] = -30;
                motor[motorD] = 30;

                while(getGyroDegrees(S1) < 45*(i+1))
                {}

                motor[MotorA] = motor[motorD] = 0;
                wait1Msec(500);
                )

}

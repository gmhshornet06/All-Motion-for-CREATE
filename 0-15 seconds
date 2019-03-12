#include <kipr/botball.h>

int main()
{
    //wait_for_light(3);
    //shut_down_in(30);
    create_connect();
    
    //turn left 90°
    set_create_total_angle(0);
    while(abs(get_create_total_angle())<48)
    {
        create_drive_direct(-100,100);
        msleep(10);
    }
    set_create_total_angle(0);
    
    //turn left 20 ticks
    while(abs(get_create_total_angle())<20)
    {
        create_drive_direct(-100,100);
        msleep(10);
    }
    
    //drive forward for 2.3 seconds
    create_drive_direct(100,100);
    msleep(2300);
    
    //turn right 20 ticks
    set_create_total_angle(0);
    while(abs(get_create_total_angle())<20)
    {
        create_drive_direct(100,-100);
        msleep(10);
    }      
    
    //drive forward to PVC pipe
    while(analog(1)<1950)
    {
        create_drive_direct(100,100);
        msleep(10);
    }
    
    //turn left 90°
    set_create_total_angle(0);
    while(abs(get_create_total_angle())<45)
    {
        create_drive_direct(-100,100);
        msleep(10);
    }
    
    //drive forward to black line / electrical line
    while(get_create_rfcliff_amt()>1900)
    {
        create_drive_direct(100,100);
        msleep(10);
    }
    create_stop();
    create_disconnect();
    return 0;
}

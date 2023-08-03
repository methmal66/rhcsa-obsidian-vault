#linux  #flashcards #rhcsa/rh124/Ch11_Logs  #rhcsa 

Why correctly synchronised system time is critical?::To analyse log files across multiple systems
<!--SR:!2023-08-02,3,258-->

What is the most widely used protocol to provide and obtain correct time information on the internet?::NTP (Network)
<!--SR:!2023-08-03,4,284-->

How to identify the correct timezone hame of our correct location?::Using `tzselect` interactive prompt
<!--SR:!2023-08-03,4,284-->

How to display the current time details?::`timedatectl`
<!--SR:!2023-08-03,4,284-->

How to permanently set the timezone?::`timedatectl set-timezone Asia/Colombo`
<!--SR:!2023-08-03,4,284-->

How to permanently set the system's current time?::`timedatectl set-time 17:30:00`
<!--SR:!2023-08-03,4,278-->

How to permanently activate the NTP service to enable synchronisation for automatic time adjustment?::`timedatectl set-ntp true`
<!--SR:!2023-08-03,4,284-->

Which service keeps the usually-inaccurate local hardware clock (RTC) on track by synchronizing it to the configured NTP servers?::chronyd

What is the main configuration file of chronyd?::/etc/chrony.conf
<!--SR:!2023-08-03,4,284-->

What are the default NTP servers used by chronyd?::Servers from the pool.ntp.org project
<!--SR:!2023-08-03,4,284-->

How to display the clock sources of chronyd?::`chrocyc sources -v`
<!--SR:!2023-08-03,4,278-->

How to update time when clock has been frizzed due to inactive?::Restart chronyd
<!--SR:!2023-08-03,4,284-->

References:
- [Chapter11, Section4, Maintaining accurate time](rh124-8.0-student-guide.pdf#pageno=382)
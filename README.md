WiringPi on OrangePi
-----------------------------------------------

The Open source project of WiringPi on OrangePi. maintain from www.orangepi.org

### Usage

  * Download

    ```
      On OrangePi 2G-IOT:
        env GIT_SSL_NO_VERIFY=true git clone https://github.com/OrangePiLibra/WiringPi.git 
      On Other board:
        git clone https://github.com/OrangePiLibra/WiringPi.git
    ```
  * Compile and install wiringPi
   
    On OrangePi 2G-IOT

    ```
      cd WiringPi
      sudo ./build OrangePi_2G-IOT
      sudo ./build OrangePi_2G-IOT install
    ```
    On OrangePi PC2

    ```
      cd WiringPi
      sudo ./build OrangePi_PC2
      sudo ./build OrangePi_PC2 install
    ```
    On OrangePi Win/Win plus

    ```
      cd WiringPi
      sudo ./build OrangePi_A64
      sudo ./build OrangePi_A64 install
    ```
    On OrangePi PC/PC plus/One/Lite/PC plus

    ```
      cd WiringPi
      sudo ./build OrangePi_H3
      sudo ./build OrangePi_H3 install
    ```
    On OrangePi Zero

    ```
      cd WiringPi
      sudo ./build OrangePi_ZERO
      sudo ./build OrangePi_ZERO install
    ```
  * Utilze WiringPi

    The location of demo code for WiringPi on OrangePi as follow:
    ```
      cd WiringPi/example/OrangePi
      make OrangePi
      ./OrangePi
    ```
  
  * More information

    More information about WiringPi on OrangePi, please refer:
    ```
      cd  WiringPi/example/OrangePi
      cat README.md
    ```
  * Gpio readall
   
    Use command `gpio readall`.

    ```
       orangepi@orangepi:~$ gpio readall
       +-----+-----+----------+------+---+--OrangePi+---+------+---------+-----+--+
       | BCM | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | BCM |
       +-----+-----+----------+------+---+----++----+---+------+----------+-----+-----+
       |     |     |     3.3v |      |   |  1 || 2  |   |      | 5v       |     |     |
       |   2 |  -1 |    SDA.0 |      |   |  3 || 4  |   |      | 5V       |     |     |
       |   3 |  -1 |    SCL.0 |      |   |  5 || 6  |   |      | 0v       |     |     |
       |   4 |   6 | IO6 PA06 |  OUT | 0 |  7 || 8  |   |      | TxD3     |     |     |
       |     |     |       0v |      |   |  9 || 10 |   |      | RxD3     |     |     |
       |  17 |  -1 |     RxD2 |      |   | 11 || 12 | 0 | OUT  | IO1 PD14 | 1   | 18  |
       |  27 |  -1 |     TxD2 |      |   | 13 || 14 |   |      | 0v       |     |     |
       |  22 |  -1 |     CTS2 |      |   | 15 || 16 | 0 | OUT  | IO4 PC04 | 4   | 23  |
       |     |     |     3.3v |      |   | 17 || 18 | 0 | OUT  | IO5 PC07 | 5   | 24  |
       |  10 |  -1 |     MOSI |      |   | 19 || 20 |   |      | 0v       |     |     |
       |   9 |  -1 |     MISO |      |   | 21 || 22 |   |      | RTS2     |     |     |
       |  11 |  -1 |     SCLK |      |   | 23 || 24 |   |      | SPI-CE0  |     |     |
       |     |     |       0v |      |   | 25 || 26 |   |      | CE1      |     |     |
       |   0 |  -1 |    SDA.1 |      |   | 27 || 28 |   |      | SCL.1    |     |     |
       |   5 |   7 |  IO7 PA7 |  OUT | 0 | 29 || 30 |   |      | 0v       |     |     |
       |   6 |   8 |  IO8 PA8 |  OUT | 0 | 31 || 32 | 0 | OUT  | IO9 PG08 | 9   | 12  |
       |  13 |  10 | IO10 PA9 |  OUT | 0 | 33 || 34 |   |      | 0v       |     |     |
       |  19 |  12 | IO12PA10 |  OUT | 0 | 35 || 36 | 0 | OUT  | IO13PG09 | 13  | 16  |
       |  26 |  14 | IO14PA20 |  OUT | 0 | 37 || 38 | 0 | OUT  | IO15PG06 | 15  | 20  |
       |     |     |       0v |      |   | 39 || 40 | 0 | OUT  | IO16PG07 | 16  | 21  |
       +-----+-----+----------+------+---+----++----+---+------+----------+-----+-----+
       | BCM | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | BCM |
       +-----+-----+----------+------+---+--OrangePi+------+----------+-----+-----+
      ```
      * Gpio watch readall
      Use command `watch -n 0.1 gpio readall `
                   
                  Every 0.1s: gpio readall                               orangepiwin: Wed Dec 25 17:24:14 2019

 +-----+-----+----------+------+---+-Orange Pi Win/Win+ +---+---+------+---------+-----+--+
 | BCM | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | BCM |
 +-----+-----+----------+------+---+----++----+---+------+----------+-----+-----+
 |     |     |     3.3v |      |   |  1 || 2  |   |      | 5v       |     |     |
 | 227 |   8 |    SDA.1 |   IN | 0 |  3 || 4  |   |      | 5V       |     |     |
 | 226 |   9 |    SCL.1 |   IN | 0 |  5 || 6  |   |      | 0v       |     |     |
 | 362 |   7 |   GPIO.7 |   IN | 0 |  7 || 8  | 0 | OUT  | S_TX     | 15  | 354 |
 |     |     |       0v |      |   |  9 || 10 | 0 | OUT  | S_RX     | 16  | 355 |
 | 229 |   0 |     RxD3 |   IN | 0 | 11 || 12 | 0 | OUT  | GPIO.1   | 1   | 100 |
 | 228 |   2 |     TxD3 |   IN | 0 | 13 || 14 |   |      | 0v       |     |     |
 | 231 |   3 |     CTS3 |   IN | 0 | 15 || 16 | 0 | IN   | GPIO.4   | 4   | 361 |
 |     |     |     3.3v |      |   | 17 || 18 | 0 | IN   | GPIO.5   | 5   | 68  |
 |  98 |  12 |     MOSI |   IN | 0 | 19 || 20 |   |      | 0v       |     |     |
 |  99 |  13 |     MISO |   IN | 0 | 21 || 22 | 0 | IN   | RTS3     | 6   | 230 |
 |  97 |  14 |     SCLK |   IN | 0 | 23 || 24 | 0 | IN   | CE0      | 10  | 96  |
 |     |     |       0v |      |   | 25 || 26 | 0 | IN   | GPIO.11  | 11  | 102 |
 | 143 |  30 |    SDA.2 |   IN | 0 | 27 || 28 | 0 | IN   | SCL.2    | 31  | 142 |
 |  36 |  21 |  GPIO.21 |   IN | 0 | 29 || 30 |   |      | 0v       |     |     |
 |  37 |  22 |  GPIO.22 |   IN | 0 | 31 || 32 | 0 | IN   | RTS2     | 26  | 34  |
 |  38 |  23 |  GPIO.23 |   IN | 0 | 33 || 34 |   |      | 0v       |     |     |
 |  39 |  24 |  GPIO.24 |   IN | 0 | 35 || 36 | 0 | IN   | CTS2     | 27  | 35  |
 | 101 |  25 |  GPIO.25 |   IN | 0 | 37 || 38 | 0 | IN   | TxD2     | 28  | 32  |
 |     |     |       0v |      |   | 39 || 40 | 0 | IN   | RxD2     | 29  | 33  |
 +-----+-----+----------+------+---+----++----+---+------+----------+-----+-----+
 | BCM | wPi |   Name   | Mode | V | Physical | V | Mode | Name     | wPi | BCM |
 +-----+-----+----------+------+---+-Orange Pi Win/Win+ +---+------+----------+-----+-----+
 
 Or
 Use command `watch -n 0.1 cat /sys/kernel/debug/gpio `

 

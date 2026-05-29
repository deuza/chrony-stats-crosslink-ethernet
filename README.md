# chrony-stats-crosslink-ethernet

My configuration :


            [Internet]
                |
        [Set-top box NAT]
                |
              [Wi-Fi]
              /     \
        wlan0       wlan0 + NAT port 123 UDP ntppool.org
          |           |
       [time1]     [time2]
       eth0 ←──────→ eth0
          \   PTP    /
           \  10G   /     (direct copper, IP 10.0.0.1/30 et 10.0.0.2/30)
            \      /
       GPS/PPS    GPS/PPS
       (HAT)      (HAT)

A big thank you to TheHuman00 for the original idea
His repository for more “standard” use is available here: [https://github.com/TheHuman00/chrony-stats/](https://github.com/TheHuman00/chrony-stats/)

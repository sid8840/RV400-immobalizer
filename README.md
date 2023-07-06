# RV400-immobalizer
This is one stop repository for getting knowledge of Revolt RV400 immobilizer.

the basic idea of this immobalizer is
Convert 85V to usable 5V for RF reciever and immobalizer ICC and 12 volts for DC to DC converter i.e., for Key switch and LED.
then RF reciever recieves 4 signals from key., start,lock,unlock and locate.
those signals are then forwarded to Immobalizer IC according to press of button.
1) when power button is pressed on keyfob, the RF reciver recieves the signal, forward it to IC and ic then latches that signal to 2 MOSFETs, one to BMS controller and one to Signal wire.
2) when lock  button is pressed on keyfob, the RF reciver recieves the signal, forward it to IC and ic then breaks that signal to 2 MOSFETs,  one to BMS controller and one to Signal wire.(but maintains supply for PCB ) activates the motion sensor within ic.
3) when unlock button is pressed on keyfob, the RF reciver recieves the signal, forward it to IC and ic then beaks that signal from motion sensor within ic so that bike can be moved without alarm.
4) when locate button is pressed on keyfob, the RF reciver recieves the signal, forward it to IC and ic then latches that signal to speaker and key led so that alarm and flash indiaction can be provided.

the failing of immobalizer can be split into two parts, The RF Reciver and Main board.
the RF reciever is very rare to fail, but Main board can.
more about RF reciver used in Immobalizer with circuit diagram: [MICRF229.pdf](https://github.com/sid8840/RV400-immobalizer/files/11966820/MICRF229.pdf).
i dont find the any info regarding Immobalizer ic used in main PCB.


![06-07-2023 (14 46 08)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/158cc7fd-3c00-4427-aa0d-755b4e64cdb1)
![06-07-2023 (14 45 56)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/7479f229-dce4-4906-8176-ca6d9159fedc)
![06-07-2023 (14 45 25)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/4e9ac10c-11da-494e-9f76-57f24f659624)
![06-07-2023 (14 44 51)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/e241f3c8-56ba-4fa2-a1bb-6d0771b2f683)
![06-07-2023 (14 44 32)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/7648bd6f-3a03-4416-89ef-4e690efdd924)
![06-07-2023 (14 44 03)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/bd4de678-f635-4c35-b3b3-c88c1a52b879)
![06-07-2023 (14 43 44)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/40c35041-5682-47d4-9a82-55435da6c2f6)
![06-07-2023 (13 12 48)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/60d52995-a2af-445b-86a0-1f2d1fa4d7dd)
![06-07-2023 (14 46 58)](https://github.com/sid8840/RV400-immobalizer/assets/83544106/64650259-959e-44f8-9d3d-af307db1652d)

I want to make the similar design with the help of Aurdino code , esp32 and amazon available parts so that anyone can troubleshoot instaed of depending on Revolt service center.
any help is useful.

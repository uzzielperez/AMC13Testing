# AMC13 Testing

To know more about the backend.

https://indico.cern.ch/event/1056810/contributions/4441368/attachments/2277431/3869413/cooper_daqOnCallTraining_uTCA_uHTR_jul2021.pdf

To ignore certain slots see `HcalCfg/uTCA/Global.cfg`

## Familiarization
```
[ciperez@pc-e1a02-34-01 ~]$ ~hcalsw/bin/AMC13Tool2.sh 52
No address table path specified.
Using .xml connection file...
Using AMC13 software ver:0
Read firmware versions 0x6064 0x31
flavor = 4  features = 0x000000ba
```

Currently the firmware version:

>list
Connected AMC13s
*0: SN: 189 T1v: 6064 T2v: 0031 cf: /nfshome0/hcalsw/bin/connections.xml


## log-in
```
# SSH Tunnel to 904 machine 
# Or check how it is set up in your pac file
ssh hcal904daq04
source ~hcalsw/bin/env.sh
source /opt/rh/devtoolset-8/enable # for xdaq15
~hcalsw/bin/ngFEC.exe -p 64400

```

## AMC13 steps

* Getting Familiar with Crate 52 AMC13
* Request for permission to power ON ( FIN )
* Ask to reprogram AMC13 on Wednesday (plug-in into one of the powered crates and see if they are working) and get some fakedata readouts http://bucms.bu.edu/twiki/bin/view/BUCMSPublic/AMC13Tool2Recipes#FakeDataReadout

## MAC Address

```
$ wget http://physics.bu.edu/~cosbyc/AMC13/addressCalc.py
$ python addressCalc.py -s 415
    T2 IP Address: 192.168.4.192
    T1 IP Address: 192.168.4.193
    T2 MAC Address: 08-00-30-F3-05-20
    T1 MAC Address: 08-00-30-F3-05-60
```

## MiniDAQ Stress Testing

For miniDAQ: https://indico.cern.ch/event/1056810/contributions/4441338/attachments/2277433/3869179/HCALFM_forDAQ_2021.pdf

For the MiniDAQ stress testing: https://twiki.cern.ch/twiki/bin/view/CMS/HCALMiniDAQ

# DS3231

The DS3231 is a low-cost, extremely accurate I2C real-time clock (RTC) with an integrated emperaturecompensated crystal oscillator (TCXO) and crystal.

Plugin for [DoT](https://github.com/bondrogeen/DoT)

![Logo](https://raw.githubusercontent.com/bondrogeen/DS3231/master/doc/Screenshot_2.jpg)


or manual

```lua

-- init 
dofile("DS3231.lua")({init={sda=4,scl=3}})

-- setting the time and date {"sec","min","hour","day","date","month","year"} 
dofile("DS3231.lua")({set={0,0,15,3,10,4,18}}) 

-- get temperature
print(dofile("DS3231.lua")({temp=true}))

-- tablet {"min"=0,"day"=3,"month"=4,"date"=10,"sec"=1,"hour"=15,"year"=18}
t=dofile("DS3231.lua")({get=true})

-- 2018-04-10T15:00
t=dofile("DS3231.lua")({getStr=true})
print(t)


```

![schematic](https://raw.githubusercontent.com/bondrogeen/DS3231/master/doc/Screenshot_1.jpg)

## Changelog

### 0.0.2 (2018-08-12)
* (bondrogeen) minor fix.
### 0.0.1 (2018-04-10)
* (bondrogeen) init.
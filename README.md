# DS3231

The DS3231 is a low-cost, extremely accurate I2C real-time clock (RTC) with an integrated emperaturecompensated crystal oscillator (TCXO) and crystal.

Plugin for [DoT](https://github.com/bondrogeen/DoT)

or 

```lua

sda=4
scl=3
i2c.setup(0,sda or 4,scl or 3,i2c.SLOW)

dofile("DS3231.lua")({set={0,0,15,3,10,4,18}}) 
-- setting the time and date {"sec","min","hour","day","date","month","year"} 

print(dofile("DS3231.lua")({temp=true}))
-- temperature

t=dofile("DS3231.lua")({get=true})
-- tablet {"min"=0,"day"=3,"month"=4,"date"=10,"sec"=1,"hour"=15,"year"=18}

t=dofile("DS3231.lua")({getStr=true})
print(t)
-- 2018-04-10T15:00

```

## Changelog

### 0.0.1 (2018-04-10)
* (bondrogeen) init.
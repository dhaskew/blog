---
layout: post
title: Temperature Monitoring
date: 2019-01-01 18:46:57 -0400
---

I have an XPS 9360 and I wanted to monitor my cpu temps.

note: "-j" is for json and "-f" is for fahrenheit. I jut like the json output more.

```bash
$> sensors -j -f
{
   "coretemp-isa-0000":{
      "Adapter": "ISA adapter",
      "Package id 0":{
         "temp1_input": 48.000,
         "temp1_max": 100.000,
         "temp1_crit": 100.000,
         "temp1_crit_alarm": 0.000
      },
      "Core 0":{
         "temp2_input": 47.000,
         "temp2_max": 100.000,
         "temp2_crit": 100.000,
         "temp2_crit_alarm": 0.000
      },
      "Core 1":{
         "temp3_input": 46.000,
         "temp3_max": 100.000,
         "temp3_crit": 100.000,
         "temp3_crit_alarm": 0.000
      }
   },
   "pch_skylake-virtual-0":{
      "Adapter": "Virtual device",
      "temp1":{
         "temp1_input": 44.000
      }
   },
   "acpitz-virtual-0":{
      "Adapter": "Virtual device",
      "temp1":{
         "temp1_input": 25.000,
         "temp1_crit": 107.000
      }
   }
}
```

If you want to monitor this output for a while and have the terminal automatically update the output, use the 'watch' command.

```bash
$> watch -n 1 sensors -j -f
```


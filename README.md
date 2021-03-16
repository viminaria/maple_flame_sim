# maple_flame_sim
simple python script to test equal probability line flame outputs in maple
### Notable changes:
- Changed all stat value to 9
- Addition of secondary stats for flame score evaluation (default 0.08)
- Weightings for line count on non-boss items using experimental data
- Support for Kanna and Demon Avenger flame scores

## Examples:

$ python flame.py --trials 1000000 --level 160-169 --threshold 120\
\
settings: level: 160-169, threshold: 120, type: pflame, noboss: False\
\
best score: 165.40\
stats: {'dex': 30, 'att': 0, 'mp': 0, 'str': 109, 'int': 0, 'hp': 0, 'luk': 25, 'matt': 0, 'as': 6}\
\
score above 120: 1991 out of 1000000 trials\
average flames: 502\
average meso cost: 4.578b\
\
time: 12.504 seconds

default options: --type=pflame, --stat=str, default item gets boss flame

### Full options:

$ python flame.py --trials 1000000 --level 160-169 --threshold 240 --stat as --type eflame\
\
settings: level: 160-169, threshold: 240, type: eflame, noboss: False\
\
best score: 315.00\
stats: {'dex': 80, 'att': 0, 'mp': 0, 'str': 65, 'int': 0, 'hp': 0, 'luk': 30, 'matt': 0, 'as': 7}\
\
score above 240: 5037 out of 1000000 trials\
average flames: 198\
\
time: 11.996 seconds

### Non-boss flame (will take longer to calculate due to line weightings):
$ python flame.py --trials 1000000 --level 140-149 --threshold 60 --noboss\
settings: level: 140-149, threshold: 60, type: pflame, noboss: True\
\
best score: 90.00\
stats: {'dex': 0, 'att': 2, 'mp': 0, 'str': 48, 'int': 16, 'hp': 0, 'luk': 0, 'matt': 0, 'as': 4}\
\
score above 60: 594 out of 1000000 trials\
average flames: 1683\
average meso cost: 15.349b\
\
time: 35.603 seconds

### For option values:
$ python flame.py  --help

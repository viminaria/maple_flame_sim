# maple_flame_sim
simple python script to test equal probability line flame outputs in maple

## Examples:

$ python flame.py --trials 1000000 --level 160-169 --threshold 120\
best score: 162\
stats: {'dex': 30, 'att': 0, 'mp': 0, 'str': 114, 'int': 0, 'hp': 0, 'luk': 30, 'matt': 0, 'as': 6}\
score above 120: 1002 out of 1000000 trials

default options: --type=pflame, --stat=str, default item gets boss flame

### Full options:

$ python flame.py --trials 100 --level 160-169 --threshold 120 --stat dex --type eflame\
best score: 124\
stats: {'dex': 84, 'att': 0, 'mp': 0, 'str': 0, 'int': 30, 'hp': 0, 'luk': 0, 'matt': 5, 'as': 5}\
score above 120: 1 out of 100 trials

### No boss flame:
$ python flame.py --trials 1000000 --level 160-169 --threshold 80 --stat dex --type eflame --noboss\
best score: 108\
stats: {'dex': 76, 'att': 0, 'mp': 0, 'str': 20, 'int': 0, 'hp': 0, 'luk': 20, 'matt': 0, 'as': 4}\
score above 80: 353 out of 1000000 trials

### For option values:
$ python flame.py  --help

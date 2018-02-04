# gimme-stat

The toll for git repositories to generate a simple progress statistic.

```
$ npm -g install gimme-stat
$ cd /home/your_git_project_name
$ gimme-stat
```

# Available arguments
 - `--since=[date]` `--until=[date]` you can use any `git log` valid formats for the options, as a rule in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)
   - examplse of use:
     - --since="2014-02-12T16:36:00-07:00"
   - Note: you can also use:
     - --since="2.years"
     - --since="3.months"
     - --since="2014-02-12T16:36:00-07:00"
     - --since="1 month ago"
     - --since="2 weeks 3 days 2 hours 30 minutes 59 seconds ago"
 - `--short` the flag to generate short statistic without details by files extensions.
 - `--cwd` you can use the argument to specify repository path in your local system if you run the commnad not from the repository or you want to specefy a few repositories.
   - single rep example: `--cwd="/home/project"`
   - You can use a few rep splitted by comma: `--cwd="/home/project1,/home/project2,/home/project3"`
- `--lmargin=19` - the space between progress line and a left edge of the window

# Examples
```
$ gimme-stat --since=3.months --cwd="/home/project1,/home/project2,/home/project3"

Dat Ding  [===================================                                                       ] 34.62%
├── js    [=====================================================================                     ] 68.80%
├── html  [=======================                                                                   ] 22.98%
└── less  [=========                                                                                 ] 8.22%
Ilya Mokin[===================                                                                       ] 18.46%
├── js    [====================================================================================      ] 86.74%
├── other [=========                                                                                 ] 8.06%
├── json  [===                                                                                       ] 2.69%
└── html  [===                                                                                       ] 2.51%
Some Man1 [================                                                                          ] 15.89%
├── html  [===========================================================                               ] 58.17%
├── js    [=========================================                                                 ] 40.37%
└── less  [==                                                                                        ] 1.46%
Some Man2 [=============                                                                             ] 12.27%
├── js    [=======================================================================================   ] 93.13%
├── html  [=====                                                                                     ] 4.58%
└── less  [===                                                                                       ] 2.29%
Oh My Goog[==========                                                                                ] 9.41%
├── js    [====================================                                                      ] 35.85%
├── html  [===============================                                                           ] 30.76%
├── ts    [=======================                                                                   ] 22.32%
├── scss  [===========                                                                               ] 10.37%
└── json  [=                                                                                         ] 0.70%
```

```
$ gimme-stat --since=3.months --short

Dat Ding  [===================================                                                       ] 34.62%
Ilya Mokin[===================                                                                       ] 18.46%
Some Man1 [================                                                                          ] 15.89%
Some Man2 [=============                                                                             ] 12.27%
Oh My Goog[==========                                                                                ] 9.41%
```
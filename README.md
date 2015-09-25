# tw-tod-sh
(taskwarrior time-of-day shell script)

is a taskwarrior extension designed to filter-out tasks that are not appropriate for the current (now) time of day. Using the extension is as easy as adding +morn +aft +day +eve +night tags to any tasks that would be best performed at those times. 


### Features

#### Planned

- a cron-job runs ToD.sh, changes rc.tod and applies tod filters 
- on-add and on-modify hooks act on any date-change, adding "+8hrs" (or whatever) to any task with a +morn tag (for example), if no hours were specified.

### Advantages

### Benefits

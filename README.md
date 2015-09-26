# tw-tod-sh
(taskwarrior time-of-day shell script)

is a taskwarrior extension designed to filter-out tasks that are not appropriate for the current (now) time of day, for 2 selected reports. Using the extension is as easy as adding +morn +aft +day +eve +night tags to any tasks that would be best performed at those times. 


### Features

- easily set preferred time-of-day for a task by adding a +morn +aft +day +eve +night tag
- easily re-set time-of-day with 'ToD [morn|aft|day|eve|night|none]'
- does not use or interfere with task context
- designed to work with tw-needs-hook (another persistent filter tw-extension)
- view help with 'ToD help'

#### Planned

- a cron-job runs ToD.sh, changes rc.tod and applies tod filters.
- more easily customized times and hours
- applies to any number of reports, not just 2 (ready and ls by default)
- on-add and on-modify hooks act on any date-change, adding "+8hrs" (or whatever) to any task with a +morn tag (for example), if no hours were specified.

### Advantages

You could easily filter for all "evening tasks" with 'task +eve ready' but that over-simplification would hide any task without an +eve tag. That's potentially a problem, because many of the hidden tasks might well be actionable any time, including the evening, unless you were _meticulous_ with your tags.

Instead, what this extension does, is to apply the _iverse_ of the tod tag. Instead of +eve, it's ( -morn -aft -day ), eliminating tasks specified for some other time, but not concealing anything else. 

### Benefits

De-selecting reports that are not actionable "now" can reduce a large list by half, dramatically improving the signal-to-noise ratio, and making it clearer what tasks can be done immediately.

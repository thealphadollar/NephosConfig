# NephosConfig
The repository contains configuration files for [Nephos](https://github.com/thealphadollar/Nephos).

You can add channels, jobs and share entities using these files. The effect of the change may take upto 10 minutes to reflect.

## Adding a channel
To add a channel, edit the add_data.yaml file, under the channels section, in the below format.

```yaml
[Next Index]:
    name: "[Name of the channel]"  # name, mandatory, WITHIN QUOTES
    ip: "[IP]"  # address eg. "0.0.0.0:8080", mandatory, WITHIN QUOTES
    country_code: "[COUNTRY CODES]"  # country code. eg "IND", optional, multiple entries separated by single whitespace
    lang: "spa"  # language codes eg. [ENG RUS], optional, multiple entries separated by whitespace.
    timezone: "spa"  # timezone, mandatory
```

## Adding a job
To add a job, edit the add_job.yaml file in the below format.
```yaml
[Next Index]:
    name: "[Job Name]" # name, mandatory, WITHIN QUOTES
    channel_name: "[Channel Name]" # channel (must be already added to nephos)
    start_time: "04:10"  # "HH:MM" eg. "15:45", WITHIN QUOTES
    duration: 135 # in minutes
    repetition: "1111111"  # eg. "1000000" for every monday, WITHIN QUOTES
```
## Adding a sharing entity
To add a share entity, edit the add_data.yaml file, under the sharing_entity section, in the below format.
```yaml
[Next Index]:
    email: "[EMail Addresses]"  # email address of the entities inside quotes, mandatory, multiple values separated by space
    tags: "[TAGS]"  # add tags inside quotes, separating multiple by space. Any tags can be used, channel name (
                         # replace whitespace in channel name by '_'), languages, timezone etc.
```

# Effect
All changes take time to effect the running Nephos and there is no need to restart the module.

In case the updation fails, admin (and all email address enlisted in Nephos notification file) will be notified through mail stating
if the updation was successful or failure given there was any change in the file.
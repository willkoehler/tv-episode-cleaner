# TV Episode Cleaner

This script cleans old episodes of TV shows from my Media/ folder.

I use [EyeTV](https://www.elgato.com/en/eyetv/eyetv-3) to record shows and
<https://github.com/corykim/eyetv-export-scripts> to export the shows to a Media/ folder,
where they are managed by [Plex](https://plex.tv)

The only problem with this system is that episodes collect over time and there's no convenient way to
delete them from the Plex client (I use [Plex Connect](https://github.com/iBaa/PlexConnect) on the Apple TV).
I wrote this script to clean old episodes of shows.

Clone this repository to your /Applications folder

    git clone git@github.com:willkoehler/tv_episode_cleaner.git /Applications/TVEpisodeCleaner

Run the script manually:

    /Applications/TVEpisodeCleaner/tv_episode_cleaner

Set up the script to run nightly

    cp /Applications/TVEpisodeCleaner/net.willkoehler.tv-episode-cleaner.plist ~/Library/LaunchAgents
    launchctl load ~/Library/LaunchAgents/net.willkoehler.tv-episode-cleaner.plist

Unload and stop the nightly job

    launchctl unload ~/Library/LaunchAgents/net.willkoehler.tv-episode-cleaner.plist
    rm ~/Library/LaunchAgents/net.willkoehler.tv-episode-cleaner.plist

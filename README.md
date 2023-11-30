# fetchtitlesong.py

function fetchDate() {
  echo -e "$(date '+%A, %B %d, %Y at %H:%M')" | lolcat # motd sederhana
}


function musik() {
echo -e "$(fetchDate)\n-----------------------------------" | lolcat

echo -n "Music's Today :" | lolcat
brandomusicx shuffle > /dev/null 2>&1;
python3 ~/.scripts/automations/fetchSongTitle_animation.py
}
musik;

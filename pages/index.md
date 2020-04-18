---
layout: default
post_list: "date"
toc: false
home_btn: true
btn_text: true
footer: true
title: "Jayasurya Obbu"
author: ""
encrypted_text: true
permalink: /
---

# **😎Jayasurya Obbu😎**

> M.Sc, Sensor Systems Technology 👨🏻‍🎓👨🏻‍🎓
>
> Karlsruhe University of Applied Sciences 🏫
>
> Karlsruhe, BW, Germany 🇩🇪

##  Who I Am?
* A Masters Student in Sensors 👨🏻‍🎓👨🏻‍🎓
* An Entrepreneur at ImmortalElectronics LLP 👨‍💼
* An Electronics and Communication Engineering Graduate 👨🏻‍🎓
* An Indian 🇮🇳
* An Organ Donor ❤️
* A Programmer rather than A Coder 👨‍💻
* A Musicophile 🎧

## Without music, life would be a mistake. Here you can see what I'm listening

<ul id="tracklist" ></ul>

<script>
            var url = 'https://ws.audioscrobbler.com/2.0?method=user.getRecentTracks&user=jayasuryaobbu&limit=6&api_key=33cdaddff9d11f6c16bc9c015757bec9&format=json';
            var getJSON = function (url, callback) {
              var xhr = new XMLHttpRequest();
              xhr.open('GET', url, true);
              xhr.responseType = 'json';
              xhr.onload = function () {
                var status = xhr.status;
                if (status === 200) {
                  callback(null, xhr.response);
                } else {
                  callback(status, xhr.response);
                }
              };
              xhr.send();
            };
            
            function timeAgo(time) {
              var units = [{
                  name: "second",
                  limit: 60,
                  in_seconds: 1
                },
                {
                  name: "minute",
                  limit: 3600,
                  in_seconds: 60
                },
                {
                  name: "hour",
                  limit: 86400,
                  in_seconds: 3600
                },
                {
                  name: "day",
                  limit: 604800,
                  in_seconds: 86400
                },
                {
                  name: "week",
                  limit: 2629743,
                  in_seconds: 604800
                },
                {
                  name: "month",
                  limit: 31556926,
                  in_seconds: 2629743
                },
                {
                  name: "year",
                  limit: null,
                  in_seconds: 31556926
                }
              ];
            
              var diff = (new Date() - new Date(time * 1000)) / 1000;
              if (diff < 5) return "now";
            
              var i = 0,
                unit;
              while (unit = units[i++]) {
                if (diff < unit.limit || !unit.limit) {
                  var diff = Math.floor(diff / unit.in_seconds);
                  return diff + " " + unit.name + (diff > 1 ? "s" : "") + ' ago';
                }
              };
            }
            
            getJSON(url,
              function (err, data) {
                if (err !== null) {
                  console.log('Something went wrong: ' + data.message);
                } else {
                  var nowplaying = '';
                  var info = data.recenttracks.track[0];
                  var recent = data.recenttracks.track[1];
                  var track = info.name;
                  var artist = info.artist["#text"];
                  var album = info.album["#text"];
                  var cover = info.image[3]["#text"];
                  var url = info.url;
                  var listening = info["@attr"];
                  var headphones = '<li><img src="/assets/img/headphones.emoji.svg" class="emoji-big"> <span>Listening to</span> ';
                  nowplaying += headphones + '<em><strong>' + track + '</strong> by <strong>' + artist + '</strong></em>';
            
                  if (listening)
                    nowplaying += ' <small>right now</small></li>';
                  else
                    nowplaying += ' <small>' + timeAgo(info.date['uts']) + '</small></li>';
            
                  nowplaying += headphones + '<em><strong>' + recent.name + '</strong> by <strong>' + recent.artist['#text'] + '</strong></em>';
                  nowplaying += ' <small>' + timeAgo(recent.date['uts']) + '</small></li>';
            
                  document.getElementById('tracklist').innerHTML = nowplaying;
                }
              });
            </script>

## Tabs

[Education📖](education.md) [Work Experience💼](work-experience.md) [Skills🤹🏼](skills.md) [Portfolio🖥️](portfolio.md) [More Info😉](additional_info.md)

## Social Connectivity

[Facebook](https://www.facebook.com/jayasurya.obbu/) [LinkedIn](https://www.linkedin.com/in/jayasurya-obbu/) [Instagram](https://www.instagram.com/mr__circuit/) [Twitter](https://twitter.com/JayasuryaObbu) [Xing](https://www.xing.com/profile/Jayasurya_Obbu/) [GitHub](https://github.com/mr-circuit) [E-Mail]( mailto:hello@jayasurya.me)
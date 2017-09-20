---
layout: post
title:  "Plastic Tracking App"
date:   2017-09-18 08:51:39 +0200
categories: project
tags: [project, plastic, past]
excerpt_separator: <!--more-->
img: /assets/plastic_tracker.png
---
![PlasticTracker](/assets/plastic_tracker.png){:class="img-responsive"}

A quick request from our friends over in Investigations had Turbo and King mock up a tool to track plastic based on brand, location and amount. This was a 3-day turnaround and the project was completed with iOS/Android app and admin web-panel. Ultimately the project was shelved for unknown reasons but the code remains for future reference. See links below for more.

[Plastic Tracking App](https://github.com/gptechlab/plastic-tracking-app)

The "magic":
```
function postTrash() {
    typeoftrash = $("#typeoftrash").val();
    brand = $("#brand").val();
    console.log("\nts: " + ts + "\nlat: " + lat + "\nlong: " + long + "\ntypeoftrash: " + typeoftrash + "\nbrand: " + brand);

    $("#tagbox").fadeOut(200, function() { $("#myImage").fadeOut(200, function() { $("#myImage").removeAttr('src'); }) });

    //Add Push to DB here: ;
    var rootRef = firebase.database().ref();
    var storesRef = rootRef.child('rubbish');
    var newStoreRef = storesRef.push();
    var tosend = {
        ts: ts,
        lat: lat,
        long: long,
        typeoftrash: typeoftrash,
        brand: brand,
        url: "/rubbish/" + newStoreRef.key + ".jpeg"
    }
    newStoreRef.set(tosend);

    storageRef = firebase.storage().ref().child("/rubbish/" + newStoreRef.key + ".jpeg");
    storageRef.putString(base64, 'base64');
    $("#buttonbox").animate({ "top": "50%" }, function() { $("#logopng").animate({ "opacity": 1 }) })

    //Push to Storage

}
```
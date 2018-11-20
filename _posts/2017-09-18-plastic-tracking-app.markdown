---
layout: post
title:  "Plastic Tracking App"
date:   2017-09-18 08:51:39 +0200
categories: project
tags: [project, plastic, past, kiho, tzetterl]
excerpt_separator: <!--more-->
img: /assets/plastic_tracker.png
---
![PlasticTracker](/assets/plastic_tracker.png)

A quick request from our friends over in Investigations had Turbo and King mock up a tool to track plastic based on brand, location and amount. This was a 3-day turnaround and the project was completed with iOS/Android app and admin web-panel. Ultimately the project was shelved for unknown reasons but the code remains for future reference. See links below for more.

[Plastic Tracking App](https://github.com/gptechlab/plastic-tracking-app)

The "magic":
```
function postTrash() {
	//get the type of trash from the UI dropdown list
    typeoftrash = $("#typeoftrash").val();

    //get the brand of the trash from the UI dropdown list
    brand = $("#brand").val();

    //debug line cause, why the hell not, is why?!
    console.log("\nts: " + ts + "\nlat: " + lat + "\nlong: " + long + "\ntypeoftrash: " + typeoftrash + "\nbrand: " + brand);

    //get rid of the form UI and string it together to make it nearly unintelligible in the code.
    $("#tagbox").fadeOut(200, function() { $("#myImage").fadeOut(200, function() { $("#myImage").removeAttr('src'); }) });

    //construct DB reference
    var rootRef = firebase.database().ref();
    var storesRef = rootRef.child('rubbish');
    var newStoreRef = storesRef.push();

    //construct object to send to db
    var tosend = {
        ts: ts,
        lat: lat,
        long: long,
        typeoftrash: typeoftrash,
        brand: brand,
        url: "/rubbish/" + newStoreRef.key + ".jpeg"
    }

    //get DB object reference ID
    newStoreRef.set(tosend);

    //construct image reference to send to storage
    storageRef = firebase.storage().ref().child("/rubbish/" + newStoreRef.key + ".jpeg");
    storageRef.putString(base64, 'base64');

    //bring back the starting UI like a boss
    $("#buttonbox").animate({ "top": "50%" }, function() { $("#logopng").animate({ "opacity": 1 }) })
}
```

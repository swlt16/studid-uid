# Student Id Card Serial Number Reader
(this is a very unhandy title)

## Overview
This web application gives access to the unique serial number
of the integrated NFC tag in a student ID card from the University of Tübingen (and many others).
This serial number can be used for some payment related features
like [autoload](https://www.my-stuwe.de/mensa/bezahlung/autoload/).

## Technical Details
The application uses the [NDEFReader API](https://developer.mozilla.org/de/docs/Web/API/NDEFReader),
which is currently (January 2026) only available on Google Chrome or Opera on Android.
Altought this API is constructed to read all (unencrypted) datasets from the tag, 
at this time it is limited to the unique serial number. This application just reads this
number and brings it to the necessary shape (reverse byte order and decimal format).
All other scripts are just for usability, the core functionality is very simple. 

## Data Privacy
The provided source code will be executed on the user's device only.
There is absolutely no server side code. In addition, the read results are 
not stored in any way on the user's device, not even in a cookie. 
If the user reloads the page, the results are gone.
So there should be no privacy related issues with this application.

## Authors
See the file AUTHORS in the repository root.
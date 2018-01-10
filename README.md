# Demo of analyzing machine audio sounds in Python

by <a href='mailto:Dattaraj.Rao@ge.com'>Dattaraj J Rao</a>

Every Machine vibrates during operation and this vibration creates sound – which is basically pressure waves traveling through a medium like air. Different modes of operation on the machine can generate different sounds and a way to distinguish these can tell us how the machine is operating. For example a Locomotive Engine running in notch 0 will create a very different sound signature than when its running in notch 8. Another example – many times you can tell from the sound your car makes that something is wrong. Expert mechanics can listen to your car Engine sounds and even diagnose some major issues even without opening the hood. What is happening here is our ears are trained to distinguish frequencies in sounds and are able to distinguish frequencies that may be causing problem. This is what we will try to do through our Analytics.

This application is hosted on Predix and developed using Python. We use Predix blob store to save files that are uploaded by users. The audio frequency Analytic is written in Python and packaged as a micro-service using Predix Analytics Framework. Currently we have a standard Analytic that extracts frequency signals from audio – but plan is to expand fpor more complicated tasks. Also – would like to give a shout-out to the new predix Python SDK from Jayson DeLancey – this has been extensively used to configure spaces and create and manage micro-services like BLOB store.
The working demo we created is available on Predix at the link below. Try this out on new WAV audio files from your vibrating components and do share your findings. 

https://mc-audio-dattaraj.run.aws-usw02-pr.ice.predix.io/ 

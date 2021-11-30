# Microsoft's MFA 

Microsoft's MFA system will allow the use of a whole slew of other authenticator apps besides their own. This could pave the way for some creative solutions for those of us with differing abilities and restrictions, physically, etc.  I just received an email from an emeritus professor (who at 90+ years of age still regularly bicycles in from Glendale all the way to our Great Lakes facility in the 3rd ward) who only ever really does email on his laptop and doesn't want to have to go hunt down his phone to authenticate.  I told him about the first alternative below and I'm sure he'll be stopping by my office in the next couple of weeks to learn more. I was about to say he'll probably be driving this time, but he was still cycling this time last year as I recall.

## Authy
First, there is an actual open-source authenticator called [Authy](www.authy.com) that has downloadable releases for Windows, MacOS, and Linux. ( `sudo snap install authy` on Ubuntu!); there's even someone who hacked a CLI version, using an Authy Python module, and I believe there's a Raspberry PI version out there. I've tested out the desktop version one of my Ubuntu laptops, and it works just as well as anything else.

The one tricky thing to get Authy working (it only uses 6-digit OTPs) is that the very first code that the Authy app shows times out after only 8 or 10 seconds, and that first code is the only one that Microsoft will accept as the right one. You can take all the time you want to enter that first code into the Microsoft end of things, long after it is expired off the Authy display, but you gotta write down or screenshot that first 6-digit OTP.  I tried it a few times, and unless you give it that first OTP, you must delete the account in Authy and start over.

Secondly, you can use other more well-known apps to authenticate, such as Google Authenticator, and even the Duo authenticator can be configured!!  It looks like they all can only use the 6-digit time-based OTP method; push-type alerts seem to only be available for Microsoft MFA using the Microsoft Authenticator.

Since the Raspberry PI Zero costs $10, technically you can run an authenticator on $10 worth of hardware (although with no display, all you could really do is blink the authentication code in morse code using the one user-programmable LED on it)

## Recent discoveries
### The `libvirt` PHP module



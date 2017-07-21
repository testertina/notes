# Steps

1. Create a main user on DRINKI 2 - ties main user to DRINKI 2
	* Referral Test, referral@test.com, password, female
	* Drinki promo code: RTEST1
	
2. Run tests on DRINKI 3 - this will tie a user to DRINKI 3
	* This doesn't work.  Even on a new device, main user (R. Test) is linked to Drinki 3 device, maybe because I signed in with him in the tests firstly.
	
3. Recreate a main user on DRINKI 4 - ties main user to DRINKI 4
 	* Referral Test, referral@test.com, password, female
	* Drinki promo code: RTEST2
	
4. Create a new user on DRINKI 5 - this should tie new user to DRINKI 5
	
	**Create New User**
	
	* Create new user on DRINKI 5 using random info. (promo code is NTEST1)
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Sign in with R.Test**
	
	* Sign in with R. Test details
	* Succesful sign in with R. Test
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Sign in with N.Test**
	
	* Sign in with N. Test user
	* Sucessful sign in with N. Test
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Create Third User**
	
	* Create a new user on DRINKI 5: un:Third Test
	* Can create user but it overwrites first user logged in on device RTEST2 (Referral Test user does not exist)
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Create Fourth User**
	
	* Create a new user on DRINKI 5: un:Fourth Test
	* Can create user but it overwrites first user logged in on device RTEST2 (Referral Test user does not exist)
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Sign in with N.Test**
	
	* Log in with N. Test details
	* Successful: Drinki promo code is NTEST1
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Sign in with Third Test User**
	
	* Log in with Third Test details
	* Unsuccessful: User does not exist
	* Restart app/emulator DRINKI 5 (waited 4 min with no emulator running before restarting for app to reset)
	
	**Sign in with Fourth Test User**
	
	* Log in with Fourth test details
	* Sucessful: Drinki promo code is RTEST2

I think the solution will be to create all users at the beginning of the test and log in with them as needed.
  # Dendrophobia
  
  > Creator: N00D135  
  Difficulty: Hard  
  Origin: SpookyCTF 2026  
  
  ## Challenge Description:
  ```
  OUCH! I was taking some pictures and then a tree branch fell on my head and now I'm scared of trees!
  I blacked out and I don't know where I ended up but I want revenge on this tree... looks like I find the unique ID of this tree!
  
  Yknow what, I really hate this tree species! I want to mess with the tree of the same species that was last watered in this same city and cleared of litter/waste.
  I think it's in a well known area but I think I forgot its name!
  
  Flag format is spookyctf{FirstTreeID_SpecificLocationWhereSecondTreeIs}
  ```
  
  ## Challenge Steps:
  ## First Part:
  Within the challenge there are two images that are shown.
  In the first image is an airplane that is soaring through the sky, in order to get more information on the plane,
  using an Reverse Image Searcher is advised.
  For this, I used Google Lens and got this information from it.  
  <img width="687" height="418" alt="image" src="https://github.com/user-attachments/assets/64959726-2973-4447-8ff0-064fdc6afd21" />
  
  ### Key Information from First Image:
  - Aircraft Type:
  Airbus A380-861  
  *This will be used later!*
  
  Now for the Second Image, running it through Google Lens yields no conclusive information except stating what the Aircraft type is.
  However, asking the AI for where the image is taken, gives the user a narrower search field.  
  <img width="687" height="496" alt="image" src="https://github.com/user-attachments/assets/165c98c4-f41b-4817-88bd-aec41f501c6f" />
  
  ### Key Information from Second Image:
  - Search Field:
  Near John F. Kennedy International Airport | Queens, New York!
  
  **Gathering the information is incredibly valuable for answering what the challenge wants!**
  Now for going back to the challenge, the user is asked to provide the TreeID of the First Tree for the first part.
  Using the information given from both images.
  
  ---
  ### First Image - Aircraft Type: Airbus A380-861
  ### Second Image - Search Field: Near John F. Kennedy International Airport | Queens, New York
  ---
  
  The first thing to check is the Flight History of the Aircraft that is landing at the JFK Airport.
  When searching for past flight history of the A6-EEU (Registration Tail Number for the Aircraft) plane, we see there was a flight on October 25th, 2026. Which goes from Dubai to JFK Airport.  
  <img width="1347" height="22" alt="image" src="https://github.com/user-attachments/assets/75e651b5-952b-4a9f-88ed-0548c5e9c063" />  
    
  ***Using the flight path, we can make a rough estimate of where the picture was taken!***  
  Heading over to [FlightRadar](https://www.flightaware.com/live/flight/A6EEU/history/20261026/0310Z/KJFK/OMDB), we see a clear flight path the aircraft took, which helps us locate where the photo was taken.
  This is the image of the path that was taken on October 25th.
  
  <img width="915" height="596" alt="image" src="https://github.com/user-attachments/assets/e9f40cc6-0e74-4404-9494-02c274ac00ef" />  
    
  Now for the fun part, out of the large space **where can the tree be located?**
  If referencing the two original images, we see that;
  1) The tree is located close to a building.
  2) The tree is located in a space with heavy greenery.
  3) The tree is to the left and at an angle from the plane.
  4) The tree has some distance from the airplane as the author is not directly underneath it.
  
  This cuts down our area of searching a significant amount, which I have made a rough searching area of where it could be:
  <img width="915" height="596" alt="Screenshot_20261112_131750" src="https://github.com/user-attachments/assets/aec94fa3-695d-4610-8846-9fe165459f92" />  
  (Areas underneath shadow indicate area where the picture **cannot** be taken.)  
  
  Using point 2, this immediately brings the search area down to one area,  
  <img width="84" height="101" alt="image" src="https://github.com/user-attachments/assets/dac6cfa7-18fc-465a-852a-deea7d36d211" />
  
  Now that there is a pretty small search area, how can we find a specific Tree ID?
  Managed by NYC, there is a [Tree Map](https://www.nycgovparks.org/tree-map) of all trees located in NYC.
  Navigating to the search area, shows many trees that have unique IDs;
  <img width="634" height="732" alt="image" src="https://github.com/user-attachments/assets/40872869-64d6-4b51-b733-3414819c43d7" />
  
  However, this can be simplified more by remembering the photo being taken very close to a building, and additionally, the second image showing **no buildings** and **full greenery**, east of the tree.
  This brings it down to only **three** trees that could be the answer to the first part.
  <img width="1408" height="735" alt="Screenshot_20261112_140517" src="https://github.com/user-attachments/assets/62dd4aa3-a6c4-49d9-a33d-ce7c446cb599" />  
  (Trees with red blips are considered viable options for the correct tree.)  
  
  Now to confirm which tree is correct, using Google Earth to give a perspective of where the trees are, and what view they would give, would grant us the correct one.
  After navigating to the location it is easily shown to us that two of the three trees that were viable options quickly become unviable due to it being a heavily wooded area.  
  <img width="1002" height="744" alt="GoogleEarth" src="https://github.com/user-attachments/assets/22ae55ee-59df-45ad-9d6b-be7cd09a0dfd" />
  
  This leaves only one option, which is the tree found on the lower right of the image with the trees marked, furthermore, heading to street view of where the tree would be located shows the rooftops that are on the first image.  
  <img width="1078" height="814" alt="StreetView" src="https://github.com/user-attachments/assets/e2064e66-a901-471b-9748-4811ee7ffc82" />
  Therefore, the correct tree is:
  <img width="1291" height="458" alt="image" src="https://github.com/user-attachments/assets/b34f3861-e778-492b-bad5-86ffd1f12667" />  
  Giving us the first part of the flag, "spooky{5597069_????}"  

  ## Second Part:
  Beginning the second part of the flag, the second statement mentions specifically hating the specific species of tree, indicating to focus on the "Willow Oak" tree.  
  Additionally, the narrator also wants to find the tree that was last watered and cleaned of litter/waste, which is oddly specific, therefore pointing the user on trying to find this specific statement somewhere.  
  These two points will lead to a well-known location which will be the second part of the flag.  

  Since the NYC Tree Map contained extensive information on specific trees, the user should remain on the website in order to find additional, more niche information, underneath the Tree ID, there is a button to view all Willow Oak trees, 
  which follows what the narrator mentioned within the second statement.  
  <img width="266" height="60" alt="image" src="https://github.com/user-attachments/assets/ba919548-7860-4252-8957-a75377fb6968" />

  After interacting with the button, the NYC Tree Map gathers more information on the specific tree species, and scrolling down brings a subsection for **Recent Tree Care Activities**, which heavily suggests falling under the 
  statement of cleaning litter/waste. Once checking the subsection, there are two events for when this happened;  
  <img width="494" height="279" alt="image" src="https://github.com/user-attachments/assets/6cffeaa0-bdf1-44b1-9263-61953b53e222" />
 
  However, the November 7th tree care had been done on the last day of the event, proving to be impossible to be on the challenge. Additionally, there are no remarks for the tree being watered. Leaving the only option of *October 25th, 2026*,
  where the user can interact with the location of tree to see where it was done. Leading to where the tree is located, and the well-known location, **Tompkins Square Park**.  
  <img width="734" height="706" alt="image" src="https://github.com/user-attachments/assets/10ac8969-0e33-40f5-bc4b-66d88a3596ae" />  
  *Combining both parts of the flag finishes the challenge!*
    
  &nbsp;  
  &nbsp;  

  # Flag:
  ### ``` spooky{5597069_TompkinsSquarePark} ```

  
  

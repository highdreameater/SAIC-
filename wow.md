

---

**WORKFLOW**

1. **User Input:** 📝  
   The user provides details such as the date, time, and route for the booking. The script also asks for the date and time when it should attempt to make the booking.

2. **Login & Navigation:** 🔐  
   The script opens the bus booking website using Selenium. It enters the login credentials and submits the form.

3. **Selecting Booking Details:** 🎟️  
   The script selects the desired date, time, and route from dropdown menus. It picks a bus, checks the seat selection box, and submits the form.

4. **Email Confirmation:** 📧  
   Once the booking is made, an email is sent to confirm success or failure. If there’s an error, the email will contain details about the issue encountered.

5. **Automated Scheduling:** ⏳  
   The script waits until the specified time and then attempts to book the seat, ensuring that the booking occurs as soon as slots become available.

---

**MY LOG**

Initially, I encountered errors because the process would halt at certain points. I suspected issues with my laptop, but after completing the booking code, I tried to use a third-party API for emails (Yagmail). Unfortunately, I discovered that logging in through less secure apps had been restricted in my Google account for a long time. Only institutional accounts have the feature to allow less secure apps to sign in, so I resolved the email issue.

To navigate through the booking process, I needed to obtain the IDs of each element to use `find_element_by_id`. At first, I thought about clicking on the three-line menu, but I later realized I could directly use the reservation link (womp womp).

Then, I implemented a scheduling API to automate the program. I added a feature that automatically sets the booking date to 15 days prior to the desired travel date. I set the time for the booking attempt to 12:01 AM, which is when most buses are likely to have empty seats.

The whole purpose of this code is to input the desired travel date and ask the user for the time. As soon as the booking opens (which is 15 days prior, as per the rules), the code attempts to make the reservation. By default, I set the seat number to 27, anticipating that it would typically be available at 12:01 AM. time. As soon as the booking opens (which is 15 days prior, as per the rules), the code attempts to make the reservation. By default, I set the seat number to 27, anticipating that it would typically be available at 12:01 AM.

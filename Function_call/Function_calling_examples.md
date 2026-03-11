
Function Calling Examples
A.	Correct tool usage

1.	Will it snow in New York next Sunday?

Json 
{ 
"name": "get_weather",
"arguments": {
"location": "New York",
"date": "next Sunday "
}
}
2.	Book a cab from Indiranagar to the airport at 6:30 AM tomorrow.

Json
{
               "name": "book_ride",
                "arguments": {
                "pickup": "Indiranagar",
                "destination": "airport",
                "time": "6.30 AM tomorrow"
                  }
                  }
3.	Set a reminder to take medicine every day at 9 PM.

Json
{
               "name": "set_reminder",
                "arguments": {
                "event": "take medicine",
                "date": "every day",
                "time": "9 PM"

                  }
                  }
B.	Wrong tool Correction

1.	What’s the weather like in Dubai right now?

Wrong call

Json
{
"name": "get_weather",
"arguments": {
"location": "Dubai",
"date": "right now"
}
}

Corrected Call

Json
{
"name": "get_weather",
"arguments": {
"location": "Dubai",
"date": "today"
}
}



Corrections:
In the function-calling benchmark, right now should be mapped to today. Most LLM tasks use today as the safe default 

2.	Send an email to Rahul reminding him about the meeting.

Wrong tool

Json
{
"name": "send_email",
"arguments": {
"to": "Rahul",
"subject": "meeting",
"message": "Reminding him about the meeting"
}
}

Corrected call
           {
                 "name": "send_email",
                 "arguments": {
                 "to": "Rahul",
                 "subject": "Meeting Reminder",
                 "message": "Hi Rahul, this is a reminder about the upcoming          meeting."
                 }
                 }

Correction
Subject and message should be natural, not robotic.

3.	I am at MG Road right now. How do I get to Lalbagh?
Wrong call

Json
{ 
"name": "get_direction",
"arguments": {
"origin": "MG Road",
"destination": "Lalbagh"
}
}

Corrected tool

Json
{ 
"name": "get_directions",
"arguments": {
"origin": "MG Road",
"destination": "Lalbagh"
}
}

Corrections: Wrong tool name instead of get_directions it was get_direction.

4.	Add Diwali celebration to my calendar on November 1st at 8 PM.

Wrong call

Json
{
  "name": "add_to_calendar",
  "arguments" {
    "event": "Diwali celebration",
    "date": "November 1st",
    "time": "8 PM"
  }
}

Correct call

Json
{
  "name": "add_to_calendar",
  "arguments": {
    "event": "Diwali celebration",
    "date": "November 1st",
    "time": "8 PM"
  }
}

Correction: a semicolon was missing after the arguments

C.	Clarifying Questions

1.	Set a reminder for my dentist appointment.

Sure! When is your dentist appointment, and what time should I set the reminder for?

2.	Find Italian restaurants.

Sure, could you please provide the location?


D.	No tool 

1.	What are some healthy dinner ideas

Some healthy dinner ideas include:
•	Grilled vegetables with paneer or tofu
•	A bowl of vegetable soup with whole-grain bread
•	Stir-fried veggies with lean protein like chicken or sprouts
•	Quinoa salad with cucumbers, tomatoes, and chickpeas
•	Dal, brown rice, and a side of steamed vegetables











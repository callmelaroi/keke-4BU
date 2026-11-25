course: BU-COS-209 week 4
group1: kernel panic
membes: Iromenu leroy 25/0149
        Isiguzoro Ekeledilichuckwu 25/1643
        Godwin Esther 25/0820
        ikedigwe wisdom 25/0107
        Nwosu Chibubem 25/0968
        Mosaka Tioluwani 25/1875
        
date: 21st of November 2026
 1. Poblem Statement: On campus, students regularly struggle to find keke (tricyle) on time

Executive Summary
On our campus, students regularly struggle to find a keke (tricycle) on time, especially during peak hours, rain, or late evenings. Drivers also struggle because they waste fuel driving around looking for passengers, and often reject trips because they don't know the destination or fare in advance.

2. our solution is a campus-only hailing app that connects students (riders) with the nearest available keke driver in real-time. A rider enters pickup and destination, the app notifies nearby online drivers, and the first driver to accept gets the ride. The rider can track the keke on a map.

We are NOT building another Bolt. We are building a small, campus-specific solution for a problem we can observe every day.

3. Core Problem:Getting a keke on campus is unpredictable, time-consuming, and frustrating for both riders and drivers.

For Riders:
.Long, unpredictable waiting times, especially at 8am, 12pm, and 5pm, and during rain.
. Drivers refuse to go to certain hostels / faculties because they consider the road bad or the trip too short.
. No way to know if a keke is coming or how much it will cost before boarding.
. Safety concern at night - boarding an unknown keke with no record of the trip.

For Drivers:
. Waste time and fuel cruising empty looking for passengers.
. Lose passengers to other drivers while waiting at a park.
. Arguments over price because fare is negotiated verbally after the trip.
. No record of trips or earnings.

4. Why This Matters:
If a student misses a 8am lecture because they waited 25 minutes for keke, that's an academic problem, not just a transport problem.

5. Research Methodology
We did not assume this problem. We observed and asked.

Methods Used:
Interviews: 8 students and 2 keke drivers 

Interview Questions We Asked:
. Riders: "have you ever gone late to a class only because you coulndt fink keke on time"
. Riders: "Tell me about the last time you struggled to find keke. What happened?"
. Riders: "as a student in samuel akande hall having a class in SAT, how long would it take you to find keke"
. Riders: "Have you ever had a driver refuse your location? Why?"
. Drivers: "How do you find passenger"
. Drivers: "Why do you sometimes reject a passenger?"


 Research Findings (What We Found)

6. Quantitative Findings

Finding from Our Observation

Average Wait Time (Peak): 18-25 minutes at Main Gate between 7:30-8:30am 
 Average Wait Time (Off-Peak): 5-8 minutes 
 Rejection Rate: 4 out of 10 students we watched were rejected for Havila gold, samuel akande SAT, BUTH and Bethel splendor route

Insight: The problem is NOT lack of keke. It's lack of matching. Keke and passengers are in the same area but cannot find each other efficiently.

 Target Users: students, keke drivers, staff and even visistors

How People Cope Today

Trekking: Students trek 15-20 mins and arrive late/sweaty.
Standing at juntions: Students walk to junctions instead of waiting at their hostel.
Calling a Known Driver: Students save 1-2 driver numbers and call them. If driver is busy, they are stuck.


Why These Fail: They depend on luck, personal connections, or physical walking. No system.

7. Proposed Solution: 
A mobile app with two modes in one app: Rider Mode and Driver Mode.

Core Flow:
1. Rider opens app, allows location
2. Rider enters: Pickup (auto-filled from GPS) + Destination (from campus list)
3. App shows estimated fare (e.g., ₦200/ ₦300 fixed price + service fee)
4. Rider taps "Request Keke"
5. App finds 3 nearest ONLINE drivers within 1.5km and sends push notification
6. First driver to tap ACCEPT gets the ride. Others see "Ride Taken"
7. Rider sees: Driver name, photo, keke plate number, ETA, live map
8. Driver arrives, rider boards, ride starts
9. On arrival, rider pays cash, taps "Complete", rates driver 1-5 stars

What We Will Build First
We will ONLY build what is needed to prove matching works.

8. IN SCOPE for MVP:
.  Sign up / Login (Phone number + OTP or Email + Password)
.  Choose Role: Rider or Driver
.  Driver Profile: Name, Photo, Keke Plate Number, Phone
.  Go Online / Offline toggle for drivers
.  Live Location (GPS) for both
.  Request Ride: Pickup + Destination from campus location list
.  Fixed Fare Display (Zone-based, not dynamic)
.  Driver Matching: Notify nearest drivers
.  Accept / Reject Ride
.  Live Tracking on Map (Rider sees driver moving)
.  Trip Complete + Cash Payment Confirmation
.  Rating (1-5 stars) after ride
.  Ride History (Simple list)

OUT OF SCOPE (NOT in MVP):
.  Card / Online Payment (Cash only for MVP)
.  In-app Chat (Use phone call button)
.  Dynamic Surge Pricing
.  Multiple stops / Shared rides
.  Admin Dashboard (Will be added in V2)
.  iOS App (Android first, because 90% of campus uses Android)

Why This MVP?: If we can prove that 1 rider can request and 1 driver can accept and arrive, we have solved the core problem. Everything else is decoration.


9.  Functional Requirements
. System must allow user to create account as Rider or Driver.
. System must capture and update driver live location every 10 seconds when Online.
. System must calculate distance between rider and available drivers.
. System must send push notification to drivers within 1.5km radius.
. System must lock a ride to the first driver who accepts.
. System must display fare based on pre-defined campus zones.
. System must allow rider to view driver details before boarding.
. System must record trip: rider, driver, pickup, destination, fare, time, rating.

 Non-Functional Requirements

. Performance: Request should reach drivers in < 5 seconds. Map should load in < 3 seconds on 3G.
. Usability: A new user should be able to request a keke in < 2 minutes without tutorial. Big buttons for drivers.
. Reliability: App must work with low internet. If GPS fails, allow manual pickup entry.
. Security:Phone numbers hidden. Rider sees driver number only after ride is accepted. No sharing of personal data.
. Privacy: Location is only shared during an active ride, not when app is closed.
. Scalability:* MVP designed for 100 users (50 riders, 20 drivers) on one campus. 

10.  Success Metrics - How Will We Know It Works?

If we test for 1 week with 20 drivers and 50 students:
. Average wait time drops from 20 mins to < 7 mins
. 80% of requests get accepted within 2 minutes
. Driver empty cruising time drops by 30%
. 70% of riders say they feel safer than boarding random keke

11.  Risks & Assumptions

Risk/How We Will Handle It 

1. Drivers don't want to use app (low tech literacy): Keep UI super simple, do 1-on-1 onboarding at keke park, use big buttons.
2. No internet / Low data: Optimize for low data, allow SMS fallback in V2, use lightweight maps.
3. Drivers reject low-fare trips anyway: Show fare upfront, allow driver to set minimum fare / preferred zones.
4.Safety / Fake Drivers: Require plate number + student ID verification for drivers in pilot 
5. GPS inaccurate on campus: Allow manual pin drop + campus location list (Library, Hostel A, Main Gate, etc.),

Assumptions:
. Most students have Iphone + mobile data
. Campus has at least 20 keke drivers willing to try pilot
. University allows keke operation on campus

12. Roadmap

. (This PRD): Research + PRD + Figma Prototype
. Backend setup + Login + Maps
. Matching + Accept/Reject + Live Tracking
. Testing with 5 real drivers on campus + Demo Video
. Presentation + Feedback

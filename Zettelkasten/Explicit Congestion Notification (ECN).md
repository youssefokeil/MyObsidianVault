Created on: 18-08-2024 12:31
Status: #idea
Tags: #networks 
# Explicit Congestion Notification
> ECN messages, is a message sent from congested router back to previous routers until it reaches receiver and notify it that there is congested ahead. Meaning the sender doesn't wait for duplicate ACKs or timeout.

### Implementation:
- Two bits in IP header (ToS field) marked by network router to indicate congestion
- Congestion indication is carried back to receiving host
- Receiver notifies sender of congestion, by setting the ECE bit in ACK message

-----------------
# References
[[Computer Networks]]
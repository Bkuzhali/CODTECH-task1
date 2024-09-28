# CODTECH-task1
**NAME1** B KUZHALI
**COMPANY1** CODTECH IT SOLUTIONS
**ID1** CT08DS7287
**DOMAIN1** CYBER SECURITY&ETHICAL HACKING
**DURATION1** AUGUST 30th, 2024 to SEPTEMBER 30th, 2024
**MENTOR1** NEELA SANTHOSH KUMAR 


##Overview of the project

##Project:PASSWORD STRENGTH CHECKER

##Objective
Develop a tool to assess the strength of passwords entered by users, providing feedback on password strength based on factors such as length, complexity, and uniqueness.

##about the program

**Function Definition**
def password_strength_checker(password):

This defines a function password_strength_checker that takes a single argument password, which is the password to be checked.

**Initialization**
strength = 0
feedback = []

Two variables are initialized:

- strength: an integer that keeps track of the password's strength level (0-4)
- feedback: a list that stores feedback messages for improving the password

**Length Check**

if len(password) >= 8:
    strength += 1
else:
    feedback.append("Password is too short.")

Checks if the password length is at least 8 characters. If true, increments strength by 1. Otherwise, adds a feedback message.

**Case Check**

if re.search(r'[a-z]', password) and re.search(r'[A-Z]', password):
    strength += 1
else:
    feedback.append("Password should include both uppercase and lowercase letters.")

Uses regular expressions to check if the password contains:

- At least one lowercase letter ([a-z])
- At least one uppercase letter ([A-Z])

If both conditions are true, increments strength by 1. Otherwise, adds a feedback message.

**Number Check**

if re.search(r'[0-9]', password):
    strength += 1
else:
    feedback.append("Password should include at least one digit.")

Checks if the password contains at least one digit ([0-9]). If true, increments strength by 1. Otherwise, adds a feedback message.

**Special Character Check**

if re.search(r'[@#$%^&*()_+!]', password):
    strength += 1
else:
    feedback.append("Password should include at least one special character (@#$%^&*()_+!).")

Checks if the password contains at least one special character ([@#$%^&*()_+!]). If true, increments strength by 1. Otherwise, adds a feedback message.

**Feedback and Strength Level**

if strength == 4:
    return "Strong", feedback
elif strength == 3:
    return "Moderate", feedback
else:
    return "Weak", feedback

Based on the strength value, returns:

- "Strong" if all checks pass (strength == 4)
- "Moderate" if three checks pass (strength == 3)
- "Weak" otherwise



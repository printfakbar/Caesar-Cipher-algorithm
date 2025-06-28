import re

def check_password_strength(password):
    score = 0
    feedback = []

    # Check length
    if len(password) >= 8:
        score += 1
    else:
        feedback.append("Password should be at least 8 characters long.")

    # Check lowercase
    if re.search(r"[a-z]", password):
        score += 1
    else:
        feedback.append("Include at least one lowercase letter.")

    # Check uppercase
    if re.search(r"[A-Z]", password):
        score += 1
    else:
        feedback.append("Include at least one uppercase letter.")

    # Check digits
    if re.search(r"\d", password):
        score += 1
    else:
        feedback.append("Include at least one number.")

    # Check special characters
    if re.search(r"[!@#$%^&*(),.?\":{}|<>]", password):
        score += 1
    else:
        feedback.append("Include at least one special character.")

    # Determine strength
    if score == 5:
        strength = "Strong"
    elif score >= 3:
        strength = "Moderate"
    else:
        strength = "Weak"

    return strength, feedback


# Example usage
if __name__ == "__main__":
    password = input("Enter your password: ")
    strength, feedback = check_password_strength(password)
    print(f"\nPassword Strength: {strength}")
    if feedback:
        print("Suggestions:")
        for f in feedback:
            print(f"- {f}")
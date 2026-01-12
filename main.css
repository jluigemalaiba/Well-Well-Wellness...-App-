#include <iostream>
#include <string>
using namespace std;

// Add days to a date
void addDays(int &day, int &month, int &year, int howManyDays) {
    day = day + howManyDays;
    
    int daysInMonth[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
    
    while (day > daysInMonth[month - 1]) {
        day = day - daysInMonth[month - 1];
        month = month + 1;
        
        if (month > 12) { 
            month = 1; 
            year = year + 1; 
        }
    }
}

// Check if string has only numbers
bool isNumber(string text) {
    if (text == "") return false;
    
    for (int i = 0; i < text.length(); i++) {
        if (text[i] < '0' || text[i] > '9') {
            return false;
        }
    }
    return true;
}

// Check if string has only letters (and spaces)
bool isLetters(string text) {
    if (text == "") return false;
    
    bool hasLetter = false;
    for (int i = 0; i < text.length(); i++) {
        char letter = text[i];
        
        // Check if it's A-Z or a-z or space
        bool isAtoZ = (letter >= 'A' && letter <= 'Z');
        bool isatoz = (letter >= 'a' && letter <= 'z');
        bool isSpace = (letter == ' ');
        
        if (isAtoZ || isatoz || isSpace) {
            if (!isSpace) hasLetter = true;
        } else {
            return false;
        }
    }
    return hasLetter;
}

// Clear bad input
void clearBadInput() {
    cin.clear();
    while (cin.get() != '\n');
}

int main() {
    int choice;
    string goBack;
    
    cout << "========================================\n";
    cout << "      WELL, WELL, WELLNESS... APP!\n";
    cout << "========================================\n\n";
    
    while (true) {
        cout << "\n=== Main Menu ===\n";
        cout << "1. BMI Calculator\n";
        cout << "2. Sleep Status Checker\n";
        cout << "3. Water Intake Checker\n";
        cout << "4. Step Progress Tracker\n";
        cout << "5. Calorie Tracker\n";
        cout << "6. Body Workout Program\n";
        cout << "7. Screen Time Checker\n";
        cout << "8. Mood Checker\n";
        cout << "9. Study Time Optimizer\n";
        cout << "10. Estimated Period Tracker\n";
        cout << "0. Exit\n";
        cout << "\nChoose (0-10): ";
        
        if (!(cin >> choice)) {
            clearBadInput();
            cout << "\nInvalid! Please enter numbers only (0-10).\n";
            continue;
        }
        
        if (choice < 0 || choice > 10) {
            cout << "\nInvalid! Please choose 0-10 only.\n";
            continue;
        }
        
        if (choice == 0) {
            cout << "\nThank you for using Well, Well, Wellness... App!\n";
            cout << "Stay healthy! Goodbye!\n";
            break;
        }
        
        cout << "\n";
        
        // === 1. BMI CALCULATOR ===
        if (choice == 1) {
            float weight, height, bmi;
            
            cout << "=== BMI Calculator ===\n\n";
            
            // Get weight
            while (true) {
                cout << "Your weight (kg): ";
                if (cin >> weight && weight > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            // Get height
            while (true) {
                cout << "Your height (cm, example 165): ";
                if (cin >> height && height > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            // Calculate BMI
            height = height / 100;  // convert cm to meters
            bmi = weight / (height * height);
            bmi = (int)(bmi * 10) / 10.0;  // round to 1 decimal
            
            // Show result
            cout << "\n=== Result ===\n";
            cout << "Your BMI is: " << bmi << "\n\n";
            
            if (bmi < 18.5) {
                cout << "Category: Underweight\n";
                cout << "Tip: Eat healthy and nutritious food!\n";
            } else if (bmi < 25) {
                cout << "Category: Normal Weight\n";
                cout << "Tip: Good job! Keep it up!\n";
            } else if (bmi < 30) {
                cout << "Category: Overweight\n";
                cout << "Tip: Do exercise and healthy eating.\n";
            } else {
                cout << "Category: Obese\n";
                cout << "Tip: Consult a doctor for guidance.\n";
            }
        }
        
        // === 2. SLEEP STATUS ===
        else if (choice == 2) {
            int hours;
            
            cout << "=== Sleep Status Checker ===\n";
            
            while (true) {
                cout << "Enter hours of sleep: ";
                if (cin >> hours && hours >= 0 && hours <= 24) break;
                clearBadInput();
                cout << "Invalid! Enter 0-24 only.\n";
            }
            
            if (hours < 6) {
                cout << "Sleep Status: Not enough sleep. Try to sleep 6-8 hours!\n";
            } else if (hours <= 8) {
                cout << "Sleep Status: Good sleep.\n";
            } else {
                cout << "Sleep Status: Too much sleep. Try to sleep 6-8 hours!\n";
            }
        }
        
        // === 3. WATER INTAKE ===
        else if (choice == 3) {
            int glasses;
            
            cout << "=== Water Intake Checker ===\n";
            
            while (true) {
                cout << "Enter number of glasses of water drank today: ";
                if (cin >> glasses && glasses >= 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            if (glasses < 8) {
                cout << "Hydration Status: Low! Try drinking 8-12 glasses.\n";
            } else if (glasses <= 12) {
                cout << "Hydration Status: Good water intake.\n";
            } else {
                cout << "Hydration Status: More than enough! Try drinking 8-12 glasses.\n";
            }
        }
        
        // === 4. STEP TRACKER ===
        else if (choice == 4) {
            int steps = 0, goal, add;
            char cont = 'y';
            
            cout << "=== Step Progress Tracker ===\n";
            
            // Get step goal
            while (true) {
                cout << "Enter your step goal: ";
                if (cin >> goal && goal > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            cout << "Step goal set to: " << goal << " steps\n\n";
            
            // Main loop
            while (cont == 'y' || cont == 'Y') {
                cout << "Current Steps: " << steps << "\n";
                
                // Calculate progress
                int percent = (steps * 100) / goal;
                if (percent > 100) percent = 100;
                cout << "Progress: " << percent << "%\n";
                
                // Check if goal reached
                if (steps >= goal) {
                    cout << "Goal Reached! Congratulations!\n";
                    cout << "You exceeded by " << (steps - goal) << " steps!\n\n";
                    
                    // Ask for new goal
                    char newGoal;
                    while (true) {
                        cout << "Do you want a new goal? (y/n): ";
                        cin >> newGoal;
                        if (newGoal == 'y' || newGoal == 'Y' || newGoal == 'n' || newGoal == 'N') break;
                        cout << "Invalid! Type y or n.\n";
                    }
                    
                    if (newGoal == 'y' || newGoal == 'Y') {
                        steps = 0;
                        while (true) {
                            cout << "Enter your new step goal: ";
                            if (cin >> goal && goal > 0) break;
                            clearBadInput();
                            cout << "Invalid! Enter a positive number.\n";
                        }
                        cout << "New goal: " << goal << " steps\n\n";
                    } else {
                        cout << "\nThank you for using this feature!\n";
                        cout << "Keep up the great work!\n";
                        break;
                    }
                } else {
                    cout << "Remaining: " << (goal - steps) << " steps\n";
                    
                    // Add steps
                    while (true) {
                        cout << "\nAdd steps: ";
                        if (cin >> add && add >= 0) break;
                        clearBadInput();
                        cout << "Invalid! Enter a positive number.\n";
                    }
                    
                    steps = steps + add;
                    
                    // Continue?
                    while (true) {
                        cout << "Continue? (y/n): ";
                        cin >> cont;
                        if (cont == 'y' || cont == 'Y' || cont == 'n' || cont == 'N') break;
                        cout << "Invalid! Type y or n.\n";
                    }
                    cout << "\n";
                }
            }
            
            // Show summary if stopped early
            if (steps < goal && (cont == 'n' || cont == 'N')) {
                cout << "\n=== Summary ===\n";
                cout << "Total Steps: " << steps << "\n";
                cout << "Progress: " << ((steps * 100) / goal) << "%\n";
                cout << "Keep going!\n";
            }
        }
        
        // === 5. CALORIE TRACKER ===
        else if (choice == 5) {
            string name, food;
            int target, calories, total = 0, count = 0;
            char more;
            
            cout << "=== Calorie Tracker ===\n";
            
            // Get name
            cin.ignore();
            while (true) {
                cout << "Your name: ";
                getline(cin, name);
                if (isLetters(name)) break;
                cout << "Invalid! Letters only.\n";
            }
            
            // Get target
            while (true) {
                cout << "Daily calorie target: ";
                if (cin >> target && target > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            // Add foods
            cin.ignore();
            while (true) {
                cout << "\n=== Food #" << (count + 1) << " ===\n";
                
                // Get food name
                while (true) {
                    cout << "Food name: ";
                    getline(cin, food);
                    if (isLetters(food)) break;
                    cout << "Invalid! Letters only.\n";
                }
                
                // Get calories
                while (true) {
                    cout << "Calories: ";
                    if (cin >> calories && calories >= 0) break;
                    clearBadInput();
                    cout << "Invalid! Enter a positive number.\n";
                }
                
                total = total + calories;
                count = count + 1;
                
                cout << "Added: " << food << " (" << calories << " cal)\n";
                cout << "Total: " << total << " cal\n";
                
                // Add more?
                while (true) {
                    cout << "\nAdd more? (y/n): ";
                    cin >> more;
                    if (more == 'y' || more == 'Y' || more == 'n' || more == 'N') break;
                    cout << "Invalid! Type y or n.\n";
                }
                
                cin.ignore();
                if (more == 'n' || more == 'N') break;
            }
            
            // Show summary
            cout << "\n=== Summary ===\n";
            cout << "Name: " << name << "\n";
            cout << "Food Count: " << count << "\n";
            cout << "Total Calories: " << total << " cal\n";
            cout << "Target Calories: " << target << " cal\n";
            
            if (total < target) {
                cout << "\nNeed " << (target - total) << " more calories!\n";
            } else if (total > target) {
                cout << "\nOver by " << (total - target) << " calories!\n";
            } else {
                cout << "\nPerfect! Right on target!\n";
            }
        }
        
        // === 6. WORKOUT PROGRAM ===
        else if (choice == 6) {
            int pick;
            
            cout << "=== Full Body Workout Program ===\n\n";
            cout << "1. Warm Up\n";
            cout << "2. Upper Body\n";
            cout << "3. Lower Body\n";
            cout << "4. Core\n";
            cout << "5. Full Routine\n";
            
            while (true) {
                cout << "Choice: ";
                if (cin >> pick && pick >= 1 && pick <= 5) break;
                clearBadInput();
                cout << "Invalid! Enter 1-5.\n";
            }
            
            if (pick == 1) {
                cout << "\n=== Warm Up (5-10 mins) ===\n";
                cout << "1. Jumping Jacks - 30 seconds\n";
                cout << "2. Arm Circles - 20 reps each direction\n";
                cout << "3. High Knees - 30 seconds\n";
                cout << "4. Leg Swings - 10 each leg\n";
                cout << "5. Torso Twists - 20 reps\n\n";
            } else if (pick == 2) {
                cout << "\n=== Upper Body ===\n";
                cout << "1. Push-ups - 3 sets x 10-15 reps\n";
                cout << "2. Tricep Dips - 3 sets x 10 reps\n";
                cout << "3. Pike Push-ups - 3 sets x 8 reps\n";
                cout << "4. Arm Pulses - 2 sets x 20 reps\n";
                cout << "5. Wall Push-ups - 2 sets x 15 reps\n\n";
            } else if (pick == 3) {
                cout << "\n=== Lower Body ===\n";
                cout << "1. Squats - 3 sets x 15 reps\n";
                cout << "2. Lunges - 3 sets x 10 each leg\n";
                cout << "3. Glute Bridges - 3 sets x 15 reps\n";
                cout << "4. Calf Raises - 3 sets x 20 reps\n";
                cout << "5. Wall Sit - 3 sets x 30 seconds\n\n";
            } else if (pick == 4) {
                cout << "\n=== Core Workout ===\n";
                cout << "1. Plank - 3 sets x 30-60 seconds\n";
                cout << "2. Crunches - 3 sets x 15 reps\n";
                cout << "3. Bicycle Crunches - 3 sets x 20 reps\n";
                cout << "4. Leg Raises - 3 sets x 10 reps\n";
                cout << "5. Russian Twists - 3 sets x 20 reps\n\n";
            } else {
                cout << "\n=== Complete Full Body Routine ===\n\n";
                cout << "Warm Up:\n";
                cout << "- Jumping Jacks: 30 sec\n";
                cout << "- Arm Circles: 20 reps\n\n";
                cout << "Upper Body:\n";
                cout << "- Push-ups: 3x10\n";
                cout << "- Tricep Dips: 3x10\n\n";
                cout << "Lower Body:\n";
                cout << "- Squats: 3x15\n";
                cout << "- Lunges: 3x10 each\n\n";
                cout << "Core Workout:\n";
                cout << "- Plank: 3x30sec\n";
                cout << "- Crunches: 3x15\n\n";
                cout << "Cool Down:\n";
                cout << "- Stretch all muscles: 5-10 mins\n\n";
            }
            
            cout << "\nGreat workout! Stay healthy!\n";
        }
        
        // === 7. SCREEN TIME ===
        else if (choice == 7) {
            int hours;
            
            cout << "=== Screen Time Checker ===\n\n";
            
            while (true) {
                cout << "How many hours on screen today? ";
                if (cin >> hours && hours >= 0 && hours <= 24) break;
                clearBadInput();
                cout << "Invalid! Enter 0-24 only.\n";
            }
            
            cout << "\n=== Result ===\n";
            cout << "Your screen time: " << hours << " hours\n\n";
            
            if (hours <= 2) {
                cout << "Status: Excellent!\n";
                cout << "Tip: Keep it up! Perfect screen time!\n";
            } else if (hours <= 4) {
                cout << "Status: Good\n";
                cout << "Tip: Still okay, but don't increase it!\n";
            } else if (hours <= 6) {
                cout << "Status: Moderate\n";
                cout << "Tip: A bit high, try to reduce it!\n";
            } else {
                cout << "Status: Too much!\n";
                cout << "Tip: Way too much! Take a break.\n";
            }
        }
        
        // === 8. MOOD CHECKER ===
        else if (choice == 8) {
            int mood;
            
            cout << "=== Mood Checker ===\n\n";
            
            while (true) {
                cout << "Rate your mood today (1-5): ";
                
                if (cin >> mood) {
                    if (mood == 1) {
                        cout << "Mood: Very sad. Take a rest and be kind to yourself.\n";
                        break;
                    } else if (mood == 2) {
                        cout << "Mood: Sad. Maybe talk to someone you trust.\n";
                        break;
                    } else if (mood == 3) {
                        cout << "Mood: Okay. Just an average day.\n";
                        break;
                    } else if (mood == 4) {
                        cout << "Mood: Happy! Keep doing what you're doing!\n";
                        break;
                    } else if (mood == 5) {
                        cout << "Mood: Very happy! Spread the good vibes!\n";
                        break;
                    } else {
                        cout << "Invalid! Enter 1-5 only.\n";
                    }
                } else {
                    clearBadInput();
                    cout << "Invalid! Enter 1-5 only.\n";
                }
            }
        }
        
        // === 9. STUDY OPTIMIZER ===
        else if (choice == 9) {
            int numSubjects;
            
            cout << "=== Study Time Optimizer ===\n";
            
            // Get number of subjects
            while (true) {
                cout << "How many subjects? ";
                if (cin >> numSubjects && numSubjects > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            string subjects[numSubjects];
            int difficulty[numSubjects];
            
            // Get each subject info
            cin.ignore();
            for (int i = 0; i < numSubjects; i++) {
                // Get subject name
                while (true) {
                    cout << "\nSubject " << (i + 1) << ": ";
                    getline(cin, subjects[i]);
                    if (isLetters(subjects[i])) break;
                    cout << "Invalid! Letters only.\n";
                }
                
                // Get difficulty
                while (true) {
                    cout << "Difficulty (1-Easy, 2-Medium, 3-Hard): ";
                    if (cin >> difficulty[i] && difficulty[i] >= 1 && difficulty[i] <= 3) break;
                    clearBadInput();
                    cout << "Invalid! Enter 1, 2, or 3.\n";
                }
                cin.ignore();
            }
            
            // Get total hours
            int totalHours;
            while (true) {
                cout << "\nTotal hours available: ";
                if (cin >> totalHours && totalHours > 0) break;
                clearBadInput();
                cout << "Invalid! Enter a positive number.\n";
            }
            
            // Calculate total difficulty points
            int totalPoints = 0;
            for (int i = 0; i < numSubjects; i++) {
                totalPoints = totalPoints + difficulty[i];
            }
            
            // Show schedule
            cout << "\n=== Optimized Schedule ===\n";
            for (int i = 0; i < numSubjects; i++) {
                float time = (float)difficulty[i] / totalPoints * totalHours;
                cout << subjects[i] << ": " << time << " hours";
                if (difficulty[i] == 3) {
                    cout << " (Priority!)";
                }
                cout << "\n";
            }
            
            // Show recommendations
            cout << "\n=== Recommendations ===\n";
            for (int i = 0; i < numSubjects; i++) {
                if (difficulty[i] == 3) {
                    cout << "Study " << subjects[i] << " first\n";
                    break;
                }
            }
            cout << "Take 10-min breaks every hour\n";
            if (totalHours > 8) {
                cout << "Warning: Too many hours. Split across days!\n";
            }
        }
        
        // === 10. ESTIMATED PERIOD TRACKER ===
        else if (choice == 10) {
            int day, month, year, duration;
            
            cout << "\n=== Estimated Period Tracker ===\n";
            cout << "\nEnter the date of your last period:\n\n";
            
            // Get month
            while (true) {
                cout << "Month (1-12): ";
                if (cin >> month && month >= 1 && month <= 12) break;
                clearBadInput();
                cout << "Invalid! Enter 1-12 only.\n";
            }
            
            // Get year first (needed to check leap year)
            while (true) {
                cout << "Year (example 2024): ";
                if (cin >> year && year > 2000 && year < 2027) break;
                clearBadInput();
                cout << "Invalid! Enter valid year.\n";
            }
            
            // Figure out max days for this month
            int maxDays;
            
            // Months with 31 days: Jan, Mar, May, Jul, Aug, Oct, Dec
            if (month == 1 || month == 3 || month == 5 || month == 7 || 
                month == 8 || month == 10 || month == 12) {
                maxDays = 31;
            }
            // February - check if leap year
            else if (month == 2) {
                // Leap year if divisible by 4
                if (year % 4 == 0) {
                    maxDays = 29;  // leap year
                } else {
                    maxDays = 28;  // normal year
                }
            }
            // Months with 30 days: Apr, Jun, Sep, Nov
            else {
                maxDays = 30;
            }
            
            // Get day
            while (true) {
                cout << "Day (1-" << maxDays << "): ";
                if (cin >> day && day >= 1 && day <= maxDays) break;
                clearBadInput();
                cout << "Invalid! Enter 1-" << maxDays << " only.\n";
            }
            
            // Get duration
            while (true) {
                cout << "How many days did it last?: ";
                if (cin >> duration && duration > 0 && duration <= 10) break;
                clearBadInput();
                cout << "Invalid! Enter 1-10 only.\n";
            }
            
            // Calculate end date
            int endDay = day, endMonth = month, endYear = year;
            addDays(endDay, endMonth, endYear, duration - 1);
            
            // Calculate next period
            int nextDay = day, nextMonth = month, nextYear = year;
            addDays(nextDay, nextMonth, nextYear, 28);
            
            // Show results
            cout << "\n=== Results ===\n";
            cout << "Started: " << month << "/" << day << "/" << year << "\n";
            cout << "Ended: " << endMonth << "/" << endDay << "/" << endYear << "\n\n";
            cout << "Your period might start on this date: " << nextMonth << "/" << nextDay << "/" << nextYear << "\n";
            cout << "(Based on 28-day cycle)\n";
        }        
        // Go back to menu
        while (true) {
            cout << "\n\nType 'back' to return to menu: ";
            cin >> goBack;
            if (goBack == "back" || goBack == "BACK" || goBack == "Back") break;
            cout << "Invalid! Type 'back' to continue.\n";
        }
    }
    return 0;
}

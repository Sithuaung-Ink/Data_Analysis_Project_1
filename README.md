# Data_Analysis_Project_1
#calculate the calories for exercise
class ExerciseSession:
    def __init__(self,exercise_name,exercise_intensity="[Low, Moderate, High]",duration = 0):
        self.exercise_name = exercise_name
        self.exercise_intensity = exercise_intensity
        self.duration = duration
    def calories_burned(self):
        if self.exercise_intensity == "Low":
            self.duration *= 4
        elif self.exercise_intensity == "Moderate":
            self.duration *= 8
        elif self.exercise_intensity == "High":
            self.duration *= 12   
        return self.duration
        
       
    def get_exercise(self):
        return self.exercise_name 
    
    def get_intensity(self):
        return self.exercise_intensity
    
    def get_duration(self):
        return self.duration
    
    def set_exercise(self,new_exercise):
        self.exercise_name = new_exercise
        
    def set_intensity(self, new_intensity):
        self.exercise_intensity=new_intensity
        
    def set_duration(self, new_duration):
        self.duration = new_duration
        
new_exercise = ExerciseSession("Running", "Low", 60)
print(new_exercise.calories_burned())
new_exercise.set_exercise("Swimming")
new_exercise.set_intensity("High")
new_exercise.set_duration(30)
print(new_exercise.calories_burned())
new_exercise.set_exercise("Tennis")
new_exercise.set_intensity("Moderate")
new_exercise.set_duration(10)
print(new_exercise.calories_burned())

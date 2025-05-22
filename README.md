def calculate_gpa():
    students = {}  
    while True:
        name = input('student name:(for ending sendfinish')
        if name.lower() == 'finish':
            break
        
        num_courses = int(input("send lossons: "))
        
        total_units = 0
        total_weighted_scores = 0
        
        for i in range(num_courses):
            units = int(input(f"everylosso {i + 1}add this: "))
            score = float(input(f"{i + 1}send this score: "))
            
            total_units += units
            total_weighted_scores += score * units
        
        if total_units > 0:
            gpa = total_weighted_scores / total_units
        else:
            gpa = 0
        
        students[name] = gpa 

    print("\n score students:")
    for student, gpa in students.items():
        print(f"{student}: {gpa:.2f}")


calculate_gpa()

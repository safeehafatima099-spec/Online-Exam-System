1. Register User
FUNCTION RegisterUser(name, pass):
    newNode = CREATE_NODE(name, pass)
    IF head == NULL:
        head = newNode
    ELSE:
        temp = head
        WHILE temp.next != NULL:
            temp = temp.next
        temp.next = newNode
    PRINT "User Registered"
END FUNCTION
________________________________________
2. Login User
FUNCTION LoginUser(name, pass):
    temp = head
    WHILE temp != NULL:
        IF temp.name == name AND temp.pass == pass:
            RETURN TRUE
        temp = temp.next
    RETURN FALSE
END FUNCTION
________________________________________
3. Add Question
FUNCTION AddQuestion(statement, optA, optB, optC, optD, correct):
    q = CREATE_NODE(statement, optA, optB, optC, optD, correct)
    IF qHead == NULL:
        qHead = q
    ELSE:
        temp = qHead
        WHILE temp.next != NULL:
            temp = temp.next
        temp.next = q
END FUNCTION
________________________________________
4. Start Exam & Evaluate
FUNCTION StartExam():
    score = 0
    temp = qHead
    WHILE temp != NULL:
        DISPLAY temp.question
        ans = INPUT()
        IF ans == temp.correct:
            score = score + 1
        temp = temp.next
    PRINT "Your Score: ", score
END FUNCTION
________________________________________
5. Delete Student (Queue)
FUNCTION DeleteStudent():
    IF front == NULL:
        PRINT "Queue Empty"
    ELSE:
        PRINT "Deleted: ", front.name
        front = front.next
END FUNCTION
________________________________________


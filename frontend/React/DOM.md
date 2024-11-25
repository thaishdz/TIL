
# TIL : Change detection in the DOM


#### 1. Initial render

![image](https://github.com/user-attachments/assets/4464dbf0-92d0-4896-a808-8b074696c51a)


#### 2. Change (state, props, etc.):
A new Virtual DOM __is generated__ (with the changes)

![image](https://github.com/user-attachments/assets/5c0acc74-bd5d-448f-8771-99c303628bea)


#### 3. Comparison (diffing):
React compares the current Virtual DOM with the previous one (in memory)


![image](https://github.com/user-attachments/assets/d4b0f3f1-055b-4472-ab33-9ce4811141cf)



#### 4. Apply changes to the real DOM:
Only the differences are applied to the real DOM, without re-rendering everything.

![image](https://github.com/user-attachments/assets/92c03b4d-fb9e-4e6c-80ce-de0daf2c58fd)




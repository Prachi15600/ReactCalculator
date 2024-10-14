**Overview**<br/>
This project is a simple calculator application built using React. It allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division. The calculator has a clean, responsive UI and features digit buttons, operation buttons, and additional functionalities like clearing inputs and deleting individual digits.

**Features**<br/>
Basic Arithmetic Operations: Supports addition, subtraction, multiplication, and division.
Responsive Layout: The calculator UI adjusts gracefully to different screen sizes.
Clear and Delete Functions: Users can clear the entire input or delete the last entered digit.
Decimal Support: The calculator supports decimal point inputs.
Real-time Display: The current operand and operation are displayed dynamically as the user interacts with the calculator.

**File Structure**<br/>
├── public/<br/>
├── src/<br/>
│   ├── App.js                 # Main component of the calculator<br/>
│   ├── DigitButton.js          # Component for digit buttons (0-9 and .)<br/>
│   ├── OperationButton.js      # Component for operation buttons (+, -, *, /)<br/>
│   ├── styles.css              # Styling for the calculator's layout and buttons<br/>
│   └── index.js                # Entry point for the React app<br/>
├── README.md                   # Documentation file<br/>
└── package.json                # Project dependencies and metadata<br/>

**Components**<br/>
1. App.js: Contains the main calculator logic, reducer function to handle the app's state, and UI layout.
2. DigitButton.js: Renders digit buttons and dispatches the ADD_DIGIT action when clicked.
3. OperationButton.js: Renders operation buttons and dispatches the CHOOSE_OPERATION action when clicked.

**How to Run the Project**<br/>

**Prerequisites**<br/>
Ensure that you have Node.js and npm installed. You can download them from Node.js Official Website.

**Installation Steps**<br/>
1. Clone the Repository -
   git clone https://github.com/your-username/react-calculator.git
   cd react-calculator
   
3. Install Dependencies
   Use npm to install the required packages.
   npm install

4. Run the Application
   Start the development server using the following command:
   npm start

5. View in Browser
   Once the server is running, open your browser and go to:
   http://localhost:3000

**Application Logic**<br/>
The calculator's logic is handled by a useReducer hook in the App.js component. This reducer manages state transitions based on the following actions:

1. ADD_DIGIT: Appends a digit to the current operand.
2. CHOOSE_OPERATION: Selects an operation (+, -, *, /) to be performed.
3. CLEAR: Resets the calculator to its initial state.
4. DELETE_DIGIT: Deletes the last entered digit.
5. EVALUATE: Performs the calculation based on the selected operation and operands.
   
**Reducer Function**<br/>
The reducer function handles these actions to update the state, which includes the currentOperand, previousOperand, and the chosen operation.

**Formatting Numbers**<br/>
The project uses the Intl.NumberFormat object to properly format numbers for better readability, especially when handling large numbers or decimals.

**Future Improvements**<br/>
1. Add keyboard support for easier input.
2. Enhance error handling (e.g., dividing by zero).
3. Implement advanced operations like square root or percentage.
4. Add animations for button presses.

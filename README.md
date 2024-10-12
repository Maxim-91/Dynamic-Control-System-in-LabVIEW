# Dynamic VI Control System

This LabVIEW project, **Dynamic VI Control System**, demonstrates how to handle multiple VI states such as start, stop, open, close, and exit using an event-driven approach. The program listens for user actions and dynamically changes states based on those inputs, making it flexible for controlling different VI behaviors.

## Key Features

1. **State Machine Architecture**:
   - The program uses a state machine architecture, where each state (Start, Stop, Open, Close, Exit) is controlled independently.
   - User actions are mapped to these states, providing clear and efficient control of the system.

2. **Event-Driven Execution**:
   - User events such as "Start", "Stop", "Open", "Close", and "Exit" trigger the transitions between states.
   - Each event is captured and processed, ensuring the program responds dynamically to user inputs.

3. **Dynamic VI Management**:
   - The program dynamically loads and unloads subVIs (like opening and closing windows or starting and stopping processes) based on user commands.
   - It ensures that the appropriate VI is active and running at any given time, optimizing resource use.

4. **Modular and Scalable**:
   - The architecture is designed to be modular, allowing for easy scaling if more states or functionalities are needed in the future.
   - Each process (Start, Open, Close, etc.) is neatly encapsulated in its respective state, making the program easy to modify or expand.

## Program Workflow

1. **Initialization**:
   - The program begins by initializing and registering the user events.
   - The state machine is set to its default state, awaiting user input to transition between different states.

2. **State Transitions**:
   - The user can trigger the following states via the UI:
     - **Start**: Launches the `Start.vi` and begins the execution of the associated task.
     - **Open**: Opens a new VI window (`Open.vi`) for additional processes or display.
     - **Close**: Closes the currently opened VI window and returns to the main state.
     - **Stop**: Terminates the current process, halting any active operations.
     - **Exit**: Safely stops all processes and closes the program.

3. **User-Controlled Events**:
   - Each button press on the front panel (Start, Stop, Open, Close, Exit) corresponds to a value change event that triggers the transition to the corresponding state.
   - The state machine manages these transitions smoothly, ensuring proper resource handling (e.g., closing open VIs).

4. **Termination**:
   - The program can be exited at any time by clicking the "Exit" button, which stops any running processes and closes the main VI.

## Inputs and Outputs

- **Inputs**:
  - User-triggered events (Start, Stop, Open, Close, Exit).
  
- **Outputs**:
  - The states of the VI (such as running, open, closed, or stopped) are visually updated on the front panel, and windows corresponding to subVIs (e.g., `Open.vi`) are dynamically displayed.

## How to Use

1. Launch the main program in LabVIEW.
2. Use the buttons on the front panel to:
   - Start a process.
   - Open additional windows (subVIs).
   - Stop the current process.
   - Close any open windows.
   - Exit the program safely.
3. Observe the VI behavior dynamically updating based on your actions.

## Requirements

- **LabVIEW** version XX.X or later.
- Understanding of event-driven programming and state machines in LabVIEW.

## Notes

- The **Dynamic VI Control System** is designed to demonstrate efficient VI control and modularity, offering a flexible framework for managing multiple processes in LabVIEW.
- This example can be expanded with additional states and functionalities, adapting to a wide range of VI management tasks.

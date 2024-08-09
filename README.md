# Scicomp2'

The Quantum Simulator code which could be find the Python ipynb os pretty much incomplete but for now it works for n by n qubit states. 
The Gate functions  labelled with Sigma, X,Y,Z are and Hadamard are acting on single quibits and CNOT gate for multiple qubits. 
The state is initiaiized in the computation basis where initial_states = [0 ,1]  represents the state |01>
The functions appply single qubit gate generates a full gate based on the dimensionlality of hilber space that is 2**n where n is the number of qubits.
Apply CNOT gate takes in the initial state, the control and target qubits along with the number of qubits and returns the new states as a unitary operation on the iniial state. 
The simulate_circuit functions utilizes a conditional argument where if the gate operation has a shape (2,2) it runs the apply single gate function otherwise if the gate has dimensionality(4,4) whihc in the codes scope is only CNOT gate than it calls the function for apply_CNOT gate.
This function returns the final state after series of uniary operations operated one after the another in order using the for loop.

The gate operations are called using a tuple where the respective gate and the intended qubit where the gate has to be operated can be directed in for example    gate_operations = [    (Hadamard(), [0]),    
(sigma_X(), [0]),    where the Hadamard gate is acting on the first qubit and the sigma X as well. 
]

The code is yet to be completed which will incorporate more complex gates and correct normalization of the initial states.The code has to be checked for initial superpostion states and etc. 
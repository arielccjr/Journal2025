~MODERN COMPUTER STACK: Transistor - Web Browser
~HARDWARE: 
    : Infrastructure: InternetDeepSeaCables, CopperWire/EthernetCable/RadioWaves/WiFi/Signals
	: In-Output Devices/Peripherals:
		: See/Camera      = Show/Screen, GUI, CRTs>Scanning>Pixels, DesktopMetaphor, 3DProjection,
		: Hear/Microphone = Speak/Speaker
		: Feel/Keyb/Mouse = Move/Animation/Events
		: Inhale/Cooler   = Exhale/Exhaust
		: Eat/Power       = Create/Heat/PowerSupply
        : Router+Swtich, 
    : Computer:
        : More Bits for more Instruction/Memory Length:
            : Parallelization > Instruction Pipelining > Pipelined Superscalar > Multi-core CPU's
        : Central/Graphical Processing Unit (C/GPU): 
            : Clock
            : Temporary Memory Registers:
                : Instruction Address Register >>> Address Input >>> Address = Data in RandomAccessMemory (RAM) >>> Instruction Register: FETCH PHASE
                    : Multiplexer: MUX = (a AND NOTsel) OR (sel AND b)
                        : NOT (in=sel, out=NOTsel)
                        : AND (in=a, in=NOTsel, out=aANDNOTsel)
                        : AND (in=sel, in=b, out=selANDb)
                        : OR (in=aANDNOTsel, in=selANDb, out=out)
                    : Matrix >>> Gate >>> AND-OR Latch: Memory Address
                        : AND (in=column, in=row, out=columnANDrow)
                            : AND (in=data, in=write-enable, out=set)
                            : NOT (in=data, out=NOTdata)
                            : AND (in=NOTdata, in=write-enable, out=reset)
                                : OR (in=set, in=outLOOP, out=setORoutLoop)
                                : NOT (in=reset, out=NOTreset)
                                : AND (in=setORoutLOOP, in=NOTreset, out=out)
                    : Memory Register/Bit: Flip Flops: out[t] = in[t-1]
                        : OR-LOOP (in=a, in=b, out=1)
                        : AND-LOOP (in=a, in=b, out=0) 
                : Instruction Register decodes Data into OperationsCode (OPCODE): DECODE PHASE
                    : Load 
                    : Arithmetic = Half>Full>Multi-bit Adder:
                        : XOR (in=a, in=b, out=abSUM)
                            : AND (in=a, in=b, out=aANDb); 
                            : NOT (in=aANDb, out=NOTaANDb); 
                            : OR (in=a, in=b, out=aORb); 
                            : AND (in=NOTaANDb, in=aORb, out=out);
                        : AND (in=a, in=b, out=abCARRY)	
                            : >XOR (in=abSUM, in=c, out=abcSUM)
                            : >AND (in=abSUM, in=c, out=abcCARRY)
                                ; >OR (in=abCARRY, in=abcBARRY, out=out)
                        : Flags of Bits: Overflow(>), Zero(=), Negative(<)...    
                    : Logic: Mux/DMux >>> Xor >>> Or >>> And/Nand >>> Not
        : ControlWire: Transistor>IntegratedCircuit>PrintedCircuitBoards>Semiconductor 

~SOFTWARE: OPERATING SYSTEM: Automation/Learning, Optimization/Multi-Tasking, Device Driver
    : LAYERS OF THE OPEN SYSTEM INTERCONNECTION (OSI) MODEL: 
        : 1. Physical Layer:
            Transistors convert digital signals (0s and 1s) into electrical, light, or radio waves
            These signals represent raw binary data
            Electrical pulses are transmitted through various media like copper wires, fiber optic cables, or wireless signals
        : 2. Data Link Layer: The frames are reassembled and validated for any transmission errors.
            Organizes raw bits into frames
            Adds error detection and correction mechanisms
            Manages how devices on the same network communicate
            Transistor-based circuits ensure accurate signal interpretation
        : 3. Network Layer: 
            The packets are reassembled, and IP addresses are used to confirm the data arrived at the correct destination.
            Handles routing of data packets between different networks
            Uses IP addresses to determine destination
            Breaks large data into smaller, manageable packets
            Transistor-based routers and switches make routing decisions
            : Internet Protocol (IP) Header: InternetServiceProvider(ISP)>Wide>LocalAreaNetwork>MAC Address
        : 4. Transport Layer: Segments are reassembled, and any lost data is retransmitted.
            Ensures reliable data transfer
            Manages data segmentation and reassembly
            Provides error checking and flow control
            TCP/UDP protocols govern how data is packaged and transmitted
            : Transmission Control Protocol (TCP): Sequence Switching/Routing Packets, Acknowledging
                : TCP Header: Software Port + Checksum
            : Data Payload (UDP): 
                : Data 
        : 5. Application Layer: 
            The data is handed off to the application that requested it, such as a web browser displaying a webpage.
            Interfaces with user applications
            Protocols like HTTP, FTP define how applications communicate
            Translates user requests into network commands 
            : Domain Name System (DNS) + Web-Server Address
            : Web-Browser/Search Engine: Hypertext Transfer Protocol (HTTP)
                : Web-Address/Page: Universal Resource Locator (URL) + Hyperlinks
                : Hypertext Markup Language (HTML) + CSS
                : Index: Frequency of Words + Backlinks
    : MACHINE-CODE = OPERATION CODE (OPCODE): INSTRUCTION + MEMORY ADDRESS:
        : Memory Size/Length: (4/8(byte)/16(word)/32/64/128)
        : Memory Bit: BinaryStates: 0, 1 (Base-2 Notation)
    : INSTRUCTION/ALGORITHM: Function>Algorithm/Sort>Compression: 
        : LOAD + MEMORY ADDRESS
            : Read (Enable) DATA in MEMORY ADDRESS (RAM)
            : Write (Enable) DATA in Temporary Memory Register
        : ADD/SUBTRACT + MEMORY ADDRESS(ES)
        : STORE
            : Write (Enable) DATA in MEMORY ADDRESS 
            : Read (Enable) DATA in Temporary Memory Register
        : JUMP / JUMP-NEGATIVE + MEMORY ADDRESS
        : HALT   
        : Brute Force, Selection, Merge, Dijkstra... 
        : ControlFlow: Conditional Statement: If/While/For... function(input1, 2)
            : Triggers: Automatically executes actions in response to table events. To enforce rules and maintain data integrity.
            : Conditionals: Enables decision-making in code. To perform actions based on conditions.
                : If/Else If/Else: Executes code based on logical conditions. To handle multiple outcomes.
                : Switch: Simplifies multi-condition branching. To streamline complex conditional logic.
                : Exception Handling: Manages runtime errors. To handle errors gracefully and ensure program stability.
            : Loops: Repeats code execution based on conditions. To perform repetitive tasks.
                : While: Repeats while a condition is true. To handle indefinite iteration.
                : Do-While: Executes at least once before checking conditions. To ensure at least one iteration.
                : For: Iterates a specific number of times. To handle definite iteration.
                : Continue Statement: Skips to the next iteration. To bypass unnecessary code in specific cases.
                : Break Statement: Exits a loop or switch statement early. To terminate iterations based on conditions.	
        : Execute: Return Statement: Then/Else/Next... 
            : Return: Exits a function and optionally returns a value. To end execution and provide a result.
        : Console Input/Output: Reads from and writes to the console. To interact with the user.
        : Search/Queries: a sequence of actions that leads from initial state to a goal state
            : Data Querying: Retrieves specific data from the database. To access and analyze stored information.
            : Sub-Query: Uses the result of one query within another query. To filter or derive conditions dynamically.
            : GROUP BY/HAVING: Groups data and filters results based on aggregate conditions. To summarize and analyze grouped data.
            : Joins: Combines rows from multiple tables. To retrieve related data from different tables.
            : Unions: Merges result sets of multiple SELECT queries. To consolidate data into one result set.
        : Initialization: Assignment Statement: A = 1
            : Import/Include: Brings in external libraries or namespaces. To use classes and methods from other libraries.
            : Declarations: Allocates memory space for storing data. To store data that can be used and manipulated in a program.
            : Assignments: Initializes or updates the value of a variable. To give variables usable values.
            : Comparison: Less Than, Greater Than, Equal
        : List: Queue/Stack, Create-Read-Update-Delete, Normalize
            : String and Date Functions: Manipulates string and date values. To format and extract meaningful information.
            : Data Insertion: Adds new records to a table. To populate the database.
            : Data Update: Modifies existing records in a table. To correct or update information.
            : Data Deletion: Removes records from a table. To delete obsolete or incorrect data.
        : Arithmetic: XOR+ANDCarry/Half, Full, Multi-bit Adder
            : Aggregate Functions: Performs calculations like sum, average, and count. To derive summary statistics.
        : Logic: NOT, AND, OR
    : MEMORY/DATA-STRUCTURE: Read-Write, Management/Data Structure: Allocation/Virtualization, Protection, De+Fragmentation
        : Read-Only Memory (ROM) & Access Control: Defines visibility and accessibility of members. To enforce encapsulation and protect data.
        : Class Definitions: Encapsulates data and behavior in a blueprint for objects. To create reusable structures for organizing data and logic.
            : Functions: Encapsulates reusable blocks of code. To simplify and modularize tasks.
        : Transactions: Groups operations as a single unit of work. To ensure data consistency and integrity.
            : Views: Creates virtual tables based on SQL queries. To simplify complex queries and enhance security.
            : Stored Procedures: Encapsulates SQL statements for reuse. To standardize and simplify repetitive tasks.
        : Database Creation: Creates a new database. To systematically organize and store application data.
            : Table Creation: Defines a structured format for storing data in rows and columns. To organize data with specific attributes.
        : File System: Directory = Name, Type, Root>Sub, Hierarchical/Flat, Metadata: Length, 
            : FILE TYPES: Array, Libraries, Node/Tree, Graph/Web/Forest, 3D Matrix: A fixed-size collection of items of the same type stored in contiguous memory. To efficiently store and access multiple values in a single variable.
                : Wave/Audio: Amplitude, Spectogram
                : Bitmap: GraphicsGenerator>ScreenBuffer(ImageWidthxHeight)
                : Character/Text/List/String = ASCII>UNICODE
                : Number/Integer/Float= 
                    : Scientific Notation; Negative Bit= 2^N-x
                    : Null Value			
        : Pointer: Next Address Reference
            : Primary Key Constraint: Ensures unique identification for each table record. To prevent duplicate records and establish a reliable reference point.
            : Foreign Key Constraint: Links two tables to maintain referential integrity. To model relationships between tables.
        : Indexes(References): Improves the speed of data retrieval. To optimize query performance.

~AUTHORIZATION/SECURITY: Session: The session is maintained or closed as necessary.
    : DIVIDE/UNCERTAINTY: Random variable 
        : NOT-IN-NOT-OUT:
            Hide	| Block
            Mute	| Deafen
            Pause	| Detach
            Choke	| Mask
            Break	| Fast
        : Error/Flags     
            Collision/Network Congestion= conflict with transfer in carrier
                Routine Problem, Hop Limit
                Scrambled Packets
                Growing Wait-Time
            Kernel Panic/Crash, Overflow= not enough memory bit 
            Dirty Bit= Mismatch between Cache and RAM, Bugs, Worm, Malware 
        : Cybersecurity:
            : Threat Model, 
                : Attack vector
                : Brute Force Attack
            : Questions: 
                : Who are you?
                : What should you have access to?
                : What you have?
                : What you are?
            : Authentication
                : Passwords
                : 2/Multi-Factor
            : Premission:
                : Read = Allows a user to see the contents of a file
                : Write = Allows a user to modify the contents
                : Execute = Allows user to run a file
            : Malware:
                : 
            : Security Kernel =
                : Independent Verification & Validation
            : Isolation/Sandbox
            : Virtual Machine
        : Hackers: 
            : White Hats
            : Black Hats
            : Social Engineering
                : Phishing
                : Pre-texting
            : NAND Mirroring 
            : Malware:
                : Trojan Horse
            : Bug Exploits:
                : Buffer Overflow
                : Bounds Checking
                : Canaries
                : Code Injections
            : Zero Day Vulnerability
            : Security Patches 
            : DDos Attacks
        : Cryptography: Defense
            : Encription 
                : Symmetric
                : Asymmetric
                    : Public
                    : Private
            : Decryption
            : Ceasar Cipher
            : Cryptoanalyst
            : Subsctitution Cipher
            : Columnar Transposition Cipher
                : Enigma Rotor
                : The Bombe
            : Data Encryption Standard
                : Advanced Encryption Standard
            : Key Exchange
                : Diffie-Hellman
            : Modular Exponentiation
        
    ~ENGINEERING/COLLABORATION:
        : DEVELOPMENT LIFECYCLE:
            : Planning + Design: Survey-Prove Investors
            : Prototyping (Testing) Development: FAIL FAST!
            : Deployment: Proven Product
            : Maintenance/Warranty
        : Source Control
            : Quality Assurance
            ; Roll Back
        : Repository:
            : Check in vs out
            : Committing

###########################################################################################################
: NOTES: ARTIFICIAL INTELLIGENCE NOTES
: SEARCH
    : Uninformed: 
        : Depth-First (Stack)
            : Start with a frontier that contains the intitial state.
            : Start with an empty explored set.
            : Repeat:
                : If the frontier is empty, then no solution.
                : Remove a node from the frontier.
                : If node contains goal state, return the solution.
                : Add the node to the explored set.
                : Expand node, add resulting nodes to the frontier, if they are NOT already in the frontier or the explored set.
        : Breadth-First (Queue)
    : Informed: with Heuristic Function
        : Greedy Best-First
        : A*: g(n) + h(n)
            : g(n) = cost to reach node
            : h(n) = estimated cost to goal 
            : optimal if:
                : h(n) is admissible (never overestimates the true cost)
                : and h(n) is consistent (for every node n and successor n' with step cost c, h(n) < h(n') + c) 
    : Adversarial: with Adversary
        : Minimax: Win-Lose Goal-State
            : Set Agents:
                : MAX aims to maximize score
                : MIN aim to minimize score
            : Set Outcomes: 
                : -1 = Lose
                : 0 = Tie
                : +1 = Win
            : Given a state s:
                : MAX picks action a in ACTIONS(s) that produces highest value of MIN-VALUE(RESULTS(s, a))
                : MIN picks action a in ACTION(s) that produces smallest value of MAX-VALUE(RESULTS(s, a))
            : Pseudocode:
                function MAX-VALUE(state):
                    if TERMINAL(state):
                        return UTILITY(state)
                    v = -infinity
                    for action in ACTIONS(state):
                        v = MAX(v, MIN-VALUE(RESULT(state, action)))
                    return v
                
                function MIN-VALUE(state):
                    if TERMINAL(state):
                        return UTILITY(state)
                    v = infinity
                    for action in ACTIONS(state):
                        v = MIN(v, MAX-VALUE(RESULT(state, action)))
                    return v
        : Alpha-Beta Pruning
        : Depth-Limited Minimax: with Evaluation function

: LOGIC: 
    : Logical Connectives: 
        : not ¬, 
        : and ∧, 
        : or ∨,
        : implication →
        : biconditional ↔
    : Entailment Algorithm: Does KB ⊨ α ?
    : Model Checking: (logic.py)
        : To determine if KB ⊨ α:
            : Enumerate all possible models.
            : If in every model where KB is true, α is true, then KB entals α.
            : Otherwise, KB does not entail α.
    : Knowledge Engineering:
    : Inference Rules:
        : Modus Ponens: α → β
        : And Elimination: α ⊨ β
        : Double Negation Elimination:
        : Implication Elimination
        : Biconditional Elimination
        : De Morgan's Law
        : Distributive Property/Law
        : Unit Resolution
    : Conversion to conjunctive normal form (CNF)
        : Eliminate biconditionals
        : Eliminate implications
        : Move not inwards using De Morgan's laws
        : Use distributive law to distribute or wherever possible
    : Inference by Resolution
        : To determine if KB ⊨ α:
            : Convert (KB and not alpha) to Conjunctive Normal Form.
            : Keep checking to see if we can use resolution to produce a new clause.
                : If ever we produce the empty clause (equivalent to false), we have a contradiction, and KB ⊨ α.
                : Otherwise, if we cannot add new clauses, no entailment.
    : First-Order Logic
        : Universal Quantificationa
        : Existential Quantification
: PROBABILITY: 
    : Bayes' Rule: P(b | a) = P(a | b) P(b) / P(a)
    : Probability Rules:
        : Negation
        : Inclusion-Exclusion
        : Marginalization
        : Conditioning
    : Inference by Enumeration
    : Approximate Inference:
    : Sampling
        : Rejection Sampling
        : Likelihood Weighting
    : hidden Markov Model: Task:
        : Filtering = given objservations from start until now, calculate distribution for current state
        : prediction = given observations from start until now, calculate distribution for a future state
        : smoothing = given observations from start until now, calculate distribution for past state
        : most likely explanation = given observatinos from start until now, calculate most likely sequence of states
: OPTIMIZATION:
    : Local Search = search algorithms that maintain a single node and searches by moving to a neighboring node
        : Hill Climbing
            : function HILL-CLIMB(problem):
                : current = initial state of problem
                : repeat:
                    neighbor = highest valued neighbor of current
                    if neighbor not better than current:
                        return current
                    current = neighbor
            : steepest-ascene = choose the highest-valued neighbor
            : stochastic = choose randomly from higher-valued neighbors
            : first-choice = choose the first higher-valued neighbor
            : random-restart = conduct hill climbing multiple times
            : local beam search = chooses the k highest-valued neighbors
        : Simulated Annealing =
            function SIMULATED-ANNEALING(problem, max):
                current = initiate state of problem 
                for t = 1 to max:
                    T = TEMPERATURE(t)
                    neighbor = random neighbor of current 
                    deltaE = how much better neigh is than current
                    if deltaE > 0:
                        current = neighbor
                    with probability e^deltaE/T set current = neighbor
                return current
        : Linear Programming:
            : Simplex
            : Interior-Point
        : arc consistency = when all the values in a variable's domain satisfy the variable's binary constraints
            : function REVISE(csp, X, Y):
                revised = false
                for x in X.domain:
                    if no y in Y.domain satisfies constrain for (x, Y):
                        delete x from X.domain
                        revised = true
                    return revised
            : function AC-3(csp)
                queue = all arcs in csp
                while queue non-empty:
                    (X, Y) = DEQUEUE(queue)
                    if REVISE(csp, X, Y):
                        if size of X.domain == 0:
                            return false
                        for each Z in X.neighbors - {Y}:
                            ENQUEUE(queue, (Z, X))
                    return true 
        : Backtracking Search:
            : function BACKTRACKING(assignment, csp):
                if assignment complete: return assignment
                var = SELECT-UNASSIGNED-VAR(assignment, csp)
                for value in DOMAIN-VALUES(var, assignment, csp):
                    if value consistent with assignment:
                        add {var = value} to assignment
                        result = BACKTRACK(assignment, csp)
                        if result not= failure: return result
                    remove {var = value} from assignment
                return failure
        : maintaining arc consistency = algorithm for enforcing arc-consistency every time we make a new assignment 
            : function BACKTRACKING(assignment, csp):
                if assignment complete: return assignment
                var = SELECT-UNASSIGNED-VAR(assignment, csp)
                for value in DOMAIN-VALUES(var, assignment, csp):
                    if value consistent with assignment:
                        add {var = value} to assignment
                        inferences = INFERENCES(assignment, csp)
                        if inferences not= failure: add inferences to assignment
                        result = BACKTRACK(assignment, csp)
                        if result not= failure: return result
                    remove {var = value} and inferences from assignment
                return failure
: LEARNING:
    : supervised learning = given a data set of input-output pairs, learn a function to map inputs to outputs
        : classification = supervised learning task of learning a function mapping an input point to a discrete category
            : nearest-neighbor classification = algorithm that, given an input, chooses the class of the nearest data point to that input
            : k-nearest-neighbor classification = algorithm that, given an input, chooses the most common class out of the k nearest data points to that input
        : hypothesis hw(x) = 1 if w * x > 0; 0 otherwise
        : perceptron learning rule = given data point (x, y), update each weight according to: 
            : wi = wi + a(y - hw(x)) * xi
            : wi = wi + a(actual value - estimate) * xi
            : Only capable of learning linearly separable decision boundary.
        : Support Vector Machine
            : boundary that maximizes the distance between any of the data points 
        : regression = supervised learning task of learning a function mapping an input point to a continuous value
        : regularization = penalizing hypotheses that are more complex to favor simpler, more general hypotheses
        : holdout cross-validation = splitting data into a training set and a test set, such that learning happens on the training set and is evaluated on the test set
        : k-fold cross-validation = splitting data into k sets, and experimenting k times, using each set as a test set once, and using remaining data as training set
    : reinforcement learning = given a set of rewards or punishments, learn what actions to take in the future
        : Q-learning = method for learning a function Q(s,a), estimate of the value of performing action a in state s
            : Start with Q(s,a)=0 for all s,a
            : When we take an action and receive a reward:
                : Estimate the value of Q(s,a) based on current reward and expected future rewards
                : Update Q(s,a) to take into account old estimate as well as our new estimate
        : Greedy Decision-Making
            : When in state s, choose action a with the highest Q(s,a)
        : Explore vs Exploit 
            : Epsilon-Greedy:
                : Set epsilon equal to how often we want to move randomly.
                : With probability 1 - epsilon, choose estimated best move.
                : With probability epsilon, choose random move.
        : function approximation = approximating Q(s,a) often by a function combining various features, rather than storing one value for every state-action pair
    : unsupervised learning = given input data without any additional feedback, learn patterns
        : clustering = organizing a set of objects into groups in such a way that similar objects tend to be in the same group
            : k-means clustering = algorithm for clustering data based on repeatedly assigning points to clusters and updating those clusters' centers
            :  
: NEURAL NETWORKS:
    : Neurons are connected to and receive electrical signals from other neurons.
    : Neurons process input signals and can be activated.
    : artificial neural network = mathematical model for learning inspired by biological neural networks
        : Model mathematical function from inputs to outputs based on the structure and parameteres of the network.
        : Allows for learning the network's parameters based on data.
        : Functions:
            : step function: g(x) = 1 if x > 0, else 0
            : logic sigmoid
            : rectified linear unit (relu)
        : h(x1, x2) = g(w0 + w1x1 + w2x2)
        : h(x1, x2, xn-1, xn) = g(n sigma i=1 xiwi + w0)
    : supervised neural network: 
        : gradient descent = algorithm for minimizing loss when training neural network
            : Start with a random choice of weights.
            : Repeat: 
                : Calculate the gradient based on ALL DATA POINTS: direction that will lead to decreasing loss.
                : Update weights according to the gradient.
        : Stochastic gradient descent
            : Start with a random choice of weights.
            : Repeat: 
                : Calculate the gradient based on ONE DATA POINTS: direction that will lead to decreasing loss.
                : Update weights according to the gradient.
        : Mini-Batch gradient descent
            : Start with a random choice of weights.
            : Repeat: 
                : Calculate the gradient based on ONE SMALL BATCH: direction that will lead to decreasing loss.
                : Update weights according to the gradient.
    : multilayer neural network = artificial neural network with an input layer, an output layer, and at least one hidden layer 
    : backpropagation = algorithm for training neural netowrks with hidden layers
        : Start with a random choice of weights.
        : Repeat:
            : Calculate error for output layer.
            : For each layer, starting with output layer, and moving inwards towards earliest hidden layer:
                : Propagate error back one layer.
                : Update weights.
    : deep neural networks = neural network with multiple hidden layers
    : dropout = temporarily removing units - selected at random - from a neural network to prevent over-reliance on certain units
    : computer vision = computational methods for analyzing and understanding digital images
    : image convolution = applying a kernel/filter that adds each pixel value of an image to its neighbors, weighted according to a kernel matrix
    : pooling = reducing the size of an input by sampling from regions in the input
        : max-pooling = pooling by choosing the maximum value in each region
    : convolutional neural network = neural networks that use convolution, usually for analyzing images
        : Apply convolution
        : Apply pooling
        : Apply Flattening
        : Apply Deep Neural Networks
    : feed-forward neural network = neural network that has connections only in one direction
        : input >>> network >>> output
    : recurrent neural network: input >>> network (loop) >>> output
        : Relationships:
            : one-to-many 
            : many-to-one
            : many-to-many
: NATURAL LANGUAGE PROCESSING:
    : tokenization = the task of splitting a sequence of characters into pieces (tokens)
    : text classification =
    : Naive-Bayes classifier = 
    : additive smoothing = adding a value a to each value in our distribution to smooth the data  
        : Laplace smoothing = adding 1 to each value in ou r distribution: pretending we've seen each value one more time than we actually have
    : Word Representation
    : Question "What is that?" >>> Recurrent Network >>> Answer "This is apple."
    : Encoder >>> Hidden State >>> Decoder
    : Attention = letting us decide which values are important to pay attention to when generating, in this case, the next word in our sequence.
    : Machine Translation 
    : Transformers Architecture
        : Encoder: input word + positional encoding >>> (multi-head self attention >>> neural network) * Number >>> encoded representation
        : Decoder: previous output word + positional encoding >>> (multi-head self attention >>> (encoded representations) attention >>> neural network) * Number >>> encoded representation

######################################################################################################
~ATTENTION IS ALL YOU NEED:
1. Encoder-Decoder Architecture Overview
	Goal: Convert an input sequence into an output sequence (e.g., translating English to German).
	Components:
		Encoder: Processes the input sequence to produce an intermediate representation.
		Decoder: Uses the intermediate representation to generate the output sequence.
2. Input Representation: 
	Input tokens (words) are converted into fixed-size vectors using embedding layers:
		𝑋embed = Embedding(𝑋input)
	Add positional encodings to include order information:
		𝑋 = 𝑋embed +PositionalEncoding
3. Encoder Steps
	Each encoder layer has two sub-layers:
	Multi-Head Self-Attention: Each position in the sequence attends to every other position:
		Attention(𝑄,𝐾,𝑉)=softmax(𝑄𝐾𝑇𝑑𝑘)𝑉
	where:
		𝑄=𝑋𝑊𝑄,𝐾=𝑋𝑊𝐾,𝑉=𝑋𝑊𝑉
		𝑊𝑄,𝑊𝐾,𝑊𝑉 are learned projection matrices.
	Use multiple attention heads (ℎ) to attend to different representation subspaces:
		MultiHead(𝑄,𝐾,𝑉)=Concat(head1,…,headℎ)𝑊𝑂
    MultiHead(Q,K,V)=Concat(head 
    Feed-Forward Network (FFN):
    Applies a pointwise transformation to each position independently:
    Add residual connections and layer normalization:
4. Decoder Steps
    Similar to the encoder, but with an additional attention step:
    Masked Multi-Head Self-Attention:
    Prevents attending to future tokens by masking out invalid positions.
    Encoder-Decoder Attention:
    The decoder attends to the encoder’s output:
    Feed-Forward Network (FFN):
    Same as in the encoder layers.
    Add residual connections and layer normalization after each sub-layer.
5. Output Prediction
    The final decoder output is passed through a linear layer to map it back to the size of the vocabulary.
    Apply a softmax function to get probabilities for each token:
6. Training and Optimization
    Use the Adam optimizer with a custom learning rate schedule:
Summary of Logical Steps
    Embed Input: Represent tokens as vectors and add positional encoding.
    Encode Input: Pass through 
    𝑁
    N-layer encoder using self-attention and feed-forward steps.
    Decode Output: Pass through 
    𝑁
    N-layer decoder using masked self-attention, encoder-decoder attention, and feed-forward layers.
    Generate Prediction: Map decoder outputs to probabilities via softmax.
    Optimize: Train the model using Adam and a dynamic learning rate schedule.
    This structured approach ensures efficient learning and high-quality sequence transduction.

###########################################################################################################
~MEMORY HIERARCHY LEVELS: Focuses on hierarchy by speed and cost efficiency, supporting temporary and volatile storage.
    1. REGISTERS = 
    2. CACHE MEMORY = 
    3. MAIN MEMORY (RAM) = 
    4. SECONDARY STORAGE = 
    5. TERTIARY STORAGE
    6. CLOUD STORAGE

~FILE SYSTEM MEMORY HIERARCHY: Deals with directory structures, access permissions, and long-term storage management.
    1. PHYSICAL STORAGE LAYER
    2. CLOCK STORAGE LAYER
    3. FILE SYSTEMN METADATA LAYER
    4. DIRECTORY TREE STRUCTURE
    5. FILE-LEVEL ABSTRACTION
    6. ACCESS CONTROL AND PERMISSIONS LAYER.
    7. LOGICAL FILE ORGANIZATION (INDEXING/ALLOCATION)
    8. NETWORKING AND DISTRIBUTED FILE SYSTEMS

~DATA NORMALIZATION: Emphasizes redundancy reduction, relational design, and ensuring data integrity.
    1. UNNORMALIZED FORM (UNF)
    2. FIRST NORMAL FORM (1NF)
    3. SECOND NORMAL FORM (2NF)
    4. THIRD NORMAL FORM (3NF)
    5. BOYCE-CODD NORMAL FORM (BCNF)
    7. FIFTH NORMAL FORM (5NF)
    8. SIXTH NORMAL FORM (6NF)

#########################################################################################################
~ESP:
~Customer Detail View:
    : 0NF: INITIAL TABLE:
        CustomerDetails
        CustomerNumber(PK),
            Name
            Address
            City
            Province
            PostalCode
            HomePhone
    : 1NF: Composite >>> Atomic
        CustomerDetails
        CustomerNumber(PK),
            Name >>> LastName, FirstName
            Address
            City
            Province
            PostalCode
            HomePhone
    : 2NF:
        CustomerDetails
        CustomerNumber(PK),
            LastName, FirstName
            Address
            City
            Province
            PostalCode
            HomePhone
    : 3NF:
        CustomerDetails
        CustomerNumber(PK),
            LastName, FirstName
            Address
            City
            Province
            PostalCode
            HomePhone
    : ERD:
        CUSTOMER
        ---------------------
        |   CustomerNumber  |
        |-------------------| 
        |   FirstName       |
        |   LastName        |
        |   Address         |
        |   City            |
        |   Province        |
        |   PostalCode      |
        |   Phone           |
        ---------------------    

~Customer Orders View:
    : 0NF:
        Order
            CustomerName = Fred Smith
            Address = 123 SomeWhere St. Edmonton, Ab, T5H 2J9
            Phone = 436-7867
            CustomerNumber = 137
            Date = Jan 16, 2000
            OrderNumber(PK) = 219
            ItemNumber =
                H23
                H319
                M24
            Description = 
                Heater Fan Belt - 23 Degrees
                Heater Fan Belt Support Brackets
                Bolts - 24mm
            Quantity =
                1
                2
                8
            Price =
                11.99
                4.99
                0.29
            Amount =
                11.99
                9.98
                2.32
            Subtotal = 24.29
            GST = 1.70
            Total = 25.99

        Order
        OrderNumber(PK), CustomerNumber, CustomerName, Address, Phone, Date,
        (ItemNumber, Description, Quantity, CurrentPrice, SellingPrice, Amount), Subtotal, GST, Total

    : 1NF:
        Order
            OrderNumber(PK) = 219
                CustomerNumber = 137
                    CustomerName = Fred Smith
                        FirstName = Fred
                        LastName = Smith 
                    Address = 123 SomeWhere St. Edmonton, Ab, T5H 2J9
                        Street = 123 SomeWhere St.
                        City = Edmonton
                        Province = AB
                        Postal Code = T5H2J9
                    Phone = 436-7867
                Date = Jan 16, 2000
                Subtotal = 24.29
                GST = 1.70
                Total = 25.99
        OrderItem 
            OrderNumber(FK)(PK)
                ItemNumber(PK) =
                    H23
                    H319
                    M24
                    Description = 
                        Heater Fan Belt - 23 Degrees
                        Heater Fan Belt Support Brackets
                        Bolts - 24mm
                    Quantity =
                        1
                        2
                        8
                    CurrentPrice=
                    SellingPrice=
                        11.99
                        4.99
                        0.29
                    Amount =
                        11.99
                        9.98
                    2.32
        Order
        OrderNumber(PK), CustomerNumber, LastName, FirstName, Street, City, Province, PostalCode, Phone, Date, Subtotal, GST, Total

        OrderItem
        OrderNumber(FK)(PK), ItemNumber(PK), Description, Quantity, CurrentPrice, SellingPrice, Amount

    : 2NF:
        Order
            OrderNumber(PK) = 219
                CustomerNumber = 137
                    CustomerName = Fred Smith
                        FirstName = Fred
                        LastName = Smith 
                    Address = 123 SomeWhere St. Edmonton, Ab, T5H 2J9
                        Street = 123 SomeWhere St.
                        City = Edmonton
                        Province = AB
                        Postal Code = T5H2J9
                    Phone = 436-7867
                Date = Jan 16, 2000
                Subtotal = 24.29
                GST = 1.70
                Total = 25.99
        OrderItem 
            OrderNumber(FK)(PK)
                ItemNumber(FK)(PK) =
                    H23
                    H319
                    M24
                Quantity =
                    1
                    2
                    8        
                SellingPrice=
                    11.99
                    4.99
                    0.29
                Amount =
                    11.99
                    9.98
                    2.32        
        Item 
            ItemNumber(PK)
            Description = 
                Heater Fan Belt - 23 Degrees
                Heater Fan Belt Support Brackets
                Bolts - 24mm
            CurrentPrice=

        Order
        OrderNumber(PK), CustomerNumber, LastName, FirstName, Street, City, Province, PostalCode, Phone, Date, Subtotal, GST, Total

        OrderItem
        OrderNumber(FK)(PK), ItemNumber(FK)(PK), Quantity, SellingPrice, Amount

        Item
        ItemNumber(PK), Description, CurrentPrice

    : 3NF:
        Order
            OrderNumber(PK) = 219
                CustomerNumber(FK) = 137
                    CustomerName = Fred Smith
                        FirstName = Fred
                        LastName = Smith 
                    Address = 123 SomeWhere St. Edmonton, Ab, T5H 2J9
                        Street = 123 SomeWhere St.
                        City = Edmonton
                        Province = AB
                        Postal Code = T5H2J9
                    Phone = 436-7867
                Date = Jan 16, 2000
                Subtotal = 24.29
                GST = 1.70
                Total = 25.99
        Customer
            CustomerNumber(PK)
                FirstName
                LastName
            Address 
                Street
                City
                Province
                PostalCode
            Phone
        OrderItem 
            OrderNumber(FK)(PK)
                ItemNumber(FK)(PK) =
                    H23
                    H319
                    M24
                Quantity =
                    1
                    2
                    8        
                SellingPrice=
                    11.99
                    4.99
                    0.29
                Amount =
                    11.99
                    9.98
                    2.32        
        Item 
            ItemNumber(PK)
            Description = 
                Heater Fan Belt - 23 Degrees
                Heater Fan Belt Support Brackets
                Bolts - 24mm
            CurrentPrice=

        Order
        OrderNumber(PK), CustomerNumber(FK), Date, Subtotal, GST, Total

        Customer
        CustomerNumber(PK), FirstName, LastName, Address, City, Province, PostalCode, Phone

        OrderItem
        OrderNumber(FK)(PK), ItemNumber(FK)(PK), Quantity, SellingPrice, Amount

        Item
        ItemNumber(PK), Description, CurrentPrice

~ESP2:
    : 0NF:
        PaymentLog
            CustomerName    = David Williams
            CustomerNumber  = 78
            OrderNumber     = 123
            OrderDate       = Jan 11/2029
            OrderTotal      = $145.18
            Date            =
                            Jan 11/99
                            Jan 18/99
            PaymentAmount   =
                            100.00
                            45.18
            PaymentNumber   =
                            1
                            2
            BalanceOwing    =
                            45.18
                            0.00
            PaymentType     =
                            Cheque
                            Cash
            DepositBranch#  =
                            118
                            118
    : 1-2-3NF: PaymentLog
        OrderTable
        OrderNumber(FK)(PK) = 123
            OrderDate           = Jan 11/2029
            OrderTotal          = $145.18
            CustomerNumber(FK)
            
            CustomerTable
            CustomerNumber(PK) = 78
                CustomerName
                    FirstName   = David
                    LastName    = Williams
        
            PaymentTable
            PaymentNumber(PK)=
                                1
                                2                
                    PaymentDate     =
                                    Jan 11/99
                                    Jan 18/99
                    PaymentAmount   =
                                    100.00
                                    45.18
                    BalanceOwing    =
                                    45.18
                                    0.00
                    PaymentType     =
                                    Cheque
                                    Cash
                    DepositBranch#  =
                                    118
                                    118
    Initial Table:
        Order
        OrderNumber(PK), OrderDate, OrderTotal, CustomerName, CustomerNumber, 
        (PaymentDate, PaymentAmount, PaymentNumber, BalanceOwing, PaymentType, DepositBranchNumber)
    
    1-2NF Table:
        Order
        OrderNumber(PK), OrderDate, OrderTotal, FirstName, LastName, CustomerNumber
        
        Payment
        OrderNumber(PK)(FK), PaymentDate, PaymentAmount, PaymentNumber(PK), BalanceOwing, PaymentType, DepositBranchNumber

    3NF Table:
        Order
        OrderNumber(FK)(PK), OrderDate, OrderTotal, CustomerName, CustomerNumber(FK), 

        Customer
        CustomerNumber(PK) FistName, LastName

        Payment
        OrderNumber(PK)(FK), PaymentNumber(PK), PaymentDate, PaymentAmount, BalanceOwing, PaymentType, DepositBranchNumber




~DATABASE FUNDAMENTALS:
    1. The complexities of database design, optimization, and operation are not visible to the end users.
        Why: To ensure smooth functionality and efficiency without exposing users to technical complexities.
        How: By using tools like DBMS software to manage and optimize the database engine and underlying schema.
    2. Databases and DBMS: Databases store data, and a DBMS is used to manage and interact with the database.
        Why: To efficiently store, retrieve, and manage data while enforcing rules and relationships.
        How: Using features like:
            DDL: Define the database schema.
            DML: Manipulate data (insert, update, delete).
            DCL: Enforce security and user access.
            Query Language: Retrieve specific data.
    3. Relational DBMS: A type of DBMS that organizes data into tables with rows and columns.
        Why: To store related data (e.g., customers and orders) and enforce relationships between them.
        How:
            Use tables for structured storage.
            Link tables using primary and foreign keys.
            Follow business rules to define relationships.
    4. Database Design Process: The structured process of creating a database schema that supports application requirements.
        Why: To ensure the database meets business needs, enforces rules, and avoids redundancy.
        How:
            Understand requirements by talking to users and reviewing documents.
            Define the purpose and functions of the database.
            Use tools like ERD for logical design.
            Normalize the schema to minimize redundancy and ensure consistency.
            Create a physical design for performance optimization.
    5. Normalization: A process for organizing data to reduce redundancy and ensure consistency.
        Why: To create efficient and reliable databases that avoid data duplication and inconsistencies.
        How:
            1NF: Ensure atomic attributes and no repeating groups.
            2NF: Eliminate partial dependencies on composite primary keys.
            3NF: Remove transitive dependencies (non-key attributes depending on other non-key attributes).
    6. Entity-Relationship Diagram (ERD): A graphical representation of entities and their relationships.
        Why: To visually represent business rules, relationships, and data structures.
        How:
            Identify entities (e.g., customers, orders).
            Define relationships (e.g., one-to-many between customers and orders).
            Use ERD notations (e.g., IDEF1X) to depict the schema.
    7. The Database Engine: The core set of programs in a DBMS that handles all database operations.
        Why: To execute database operations efficiently.
        How:
            Users submit DML or query statements via applications.
            The DBMS processes the request and interacts with the database engine.
            The engine executes the request and interacts directly with the database.

Entities and Relationships: A relationship defines a business association between two entities (e.g., Customer and Order). Entities represent real-world objects like customers, orders, or items.
    Types of Relationships:
        One-to-One (1:1): One instance of an entity is linked to one instance of another entity.
        One-to-Many (1:N): One instance of an entity is linked to many instances of another entity.
        Many-to-Many (M:N): Multiple instances of one entity are linked to multiple instances of another entity.
    Defining Relationships: Relationships are implemented using foreign keys, which connect the primary key of one entity to a field in another.
    Entity-Relationship Diagram (ERD): A graphical representation showing entities, attributes, and their relationships.
Why: Purpose of Relationships:
    To model real-world associations between entities, such as orders being placed by customers.
    To ensure data integrity (e.g., preventing orphaned orders without customers).
    To enforce business rules (e.g., ensuring each order is tied to one and only one customer).
    To enable querying across related tables for meaningful insights.
How:
    Identify Business Rules:
        Example: "Each customer can place multiple orders."
    Define Cardinality:
        Determine whether the relationship is one-to-one, one-to-many, or many-to-many.
    Implement Foreign Keys:
        In a one-to-many relationship, the primary key of the parent table is added as a foreign key in the child table.
        Example: In the Customer-Order relationship, add CustomerId as a foreign key in the Order table.
    Handle Many-to-Many Relationships:
        Break them into two one-to-many relationships by creating an associative entity.
        Example: For the Employee-Project relationship, create a WorksOn table with EmployeeId and ProjectId as its composite primary key.
    Create ERD:
        Use graphical notations like IDEF1X to visualize entities, attributes, and relationships.
        Include relationship labels and cardinality symbols for clarity.
    Iteratively Refine the Design:
        Ensure the relationships meet business requirements and minimize data redundancy.
    Visualization Using ERD
        Entities: Represented as boxes with attributes inside.
        Attributes:
            Primary keys are listed above the line in an entity box.
            Foreign keys are suffixed with "FK."
        Relationships:
            Dashed lines for non-identifying relationships.
            Solid lines for identifying relationships.

Normalization is a systematic process of organizing data in a relational database to reduce redundancy and ensure data integrity.
    Goal: To determine:
        How many tables are needed.
        Which attributes (data items) belong in which table.
Why is Normalization Important?
    Reduces Redundancy:
        Ensures that data is not duplicated across tables, saving storage and making updates easier.
        Example: Instead of storing a customer’s address in multiple tables, normalize the database by creating a single table for customers.
    Minimizes Anomalies:
        Anomalies are inconsistencies or issues that arise when managing data in a poorly designed database:
            Update Anomaly: If data is repeated, updating one instance and forgetting others creates inconsistencies.
            Insert Anomaly: Missing data prevents new rows from being added (e.g., trying to add an employee but having no department data available).
            Delete Anomaly: Deleting a record unintentionally removes essential data (e.g., deleting an order may also delete customer information if stored in the same table).
    Improves Data Integrity and Flexibility:
        Ensures that relationships between tables are clear and properly enforced.
        Makes it easier to update, retrieve, and analyze data.
    Establishes Industry Standards:
        Based on E.F. Codd's rules for relational database design, normalization has become the industry standard.
Steps in Normalization
    Normalization is typically carried out in steps called "Normal Forms," each addressing specific issues:
        First Normal Form (1NF):
            Ensures that each column contains atomic (indivisible) values.
            Eliminates repeating groups or arrays within a table.
            Example: Splitting a table with multiple phone numbers in a single column into separate rows.
        Second Normal Form (2NF):
            Builds on 1NF.
            Ensures that all non-key attributes are fully dependent on the primary key.
            Eliminates partial dependency (attributes that depend on part of a composite primary key).
        Third Normal Form (3NF):
            Builds on 2NF.
            Ensures that all attributes are only dependent on the primary key and not on other non-key attributes (removes transitive dependency).
        Beyond 3NF:
            Higher normal forms like Boyce-Codd Normal Form (BCNF) or Fourth and Fifth Normal Forms address even more specific design issues.
    The Role of Codd’s Rules
        E.F. Codd: The father of relational databases, who formalized the rules of normalization.
        Purpose of Rules:
            Provide a structured approach to database design.
            Help designers systematically decide the number of tables and their attributes.
    Evaluation Criteria for Database Design
        Minimizing Redundancy:
            A well-normalized design avoids duplication of data, ensuring storage efficiency.
        Avoiding Anomalies:
            Anomalies are minimized, resulting in reliable and consistent data management.

Normalization: How

Why Normalize?
Large tables with many columns can:
    Be hard to interpret and manage.
    Increase redundancy (duplicate data) within the database.
    Raise the risk of anomalies (e.g., update, insert, or delete inconsistencies).
Normalization solves these problems by systematically breaking large tables into smaller, related tables. The resulting design:
    Simplifies understanding.
    Minimizes redundancy.
    Reduces the likelihood of anomalies.

Normal Forms: Normalization involves organizing a database into one of several normal forms, each based on specific rules. The main normal forms are:
    First Normal Form (1NF):
        Ensures that all columns contain atomic (indivisible) values.
        Eliminates repeating groups or arrays within a table.
    Second Normal Form (2NF):
        Builds on 1NF.
        Ensures all non-key attributes are fully dependent on the primary key.
        Eliminates partial dependencies (dependencies on part of a composite primary key).
    Third Normal Form (3NF):
        Builds on 2NF.
        Ensures no non-key attribute is dependent on another non-key attribute (removes transitive dependencies).
    Boyce-Codd Normal Form (BCNF):
        A stricter version of 3NF.
        Ensures every determinant is a candidate key (i.e., no attribute can determine another unless it is part of a candidate key).
    Fourth Normal Form (4NF):
        Eliminates multi-valued dependencies.
        Ensures that one column's value is not dependent on multiple values of another column.
    Domain-Key Normal Form (DKNF):
        Theoretical "ultimate" form of normalization.
        Ensures no constraints exist other than key constraints and domain constraints.
        Rarely implemented due to its complexity.
Trade-offs in Normalization
    Advantages:
        Fewer redundancies.
        Lower risk of anomalies.
        Easier to maintain and update.
    Disadvantages:
        More tables increase the complexity of queries.
        Potential performance degradation, especially with high volumes of rows and joins.
    Best Practice:
        Most databases are normalized up to Third Normal Form (3NF) as it provides the best balance between performance and maintenance for most applications.
Denormalization is the process of intentionally introducing violations to a normal form after normalization has been applied. This is often done to:
    Improve performance.
    Simplify queries and reduce the number of joins.
    However, denormalization can lead to:
        Increased redundancy.
        Higher risk of anomalies.
    Example: Adding derived or duplicate data to speed up read queries.
Key Concepts in Normalization
    Primary Key:
        A unique identifier for each row in a table.
        Must be correctly selected to ensure proper normalization.
    Business Rules:
        Database design must reflect the organization’s policies and rules.
        A clear understanding of these rules is critical to effective normalization.

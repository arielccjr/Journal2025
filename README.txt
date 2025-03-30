# **~QUESTION-PLAN (RHETORIC)**
# **~FLOW: IN:SEE/HEAR/FEEL/SMELL/TASTE(STIMULUS) = OUT:BE(SEEN/HEARD/FELT/SMELLED/TASTED), GRATIFICATION**
    : Motion is the transition of the potentiality (what something could be (+/-)) for the actuality (what it is (0)).
    ~LAYERS OF THE OPEN SYSTEM INTERCONNECTION (OSI) MODEL: INFRASTRUCTURE & I/O PERIPHERALS:
        ~1: PHYSICAL: Data is sent as electrical/optical signals through the wire.
        ~2: DATA LINK: Packets are framed with Media Access Control (MAC) addresses. 
        ~3: NETWORK: Packets are assigned IP addresses and routed. Internet Protocol (IP)?
        ~4: TRANSPORT: Data is split into packets. Transmission Control Protocol (TCP): TCP Header = Software Port + Checksum?
        ~5: SESSION: A session is established. DomainNameSystem (DNS) + UniformResourceLocator(URL), HypertextMarkUpLanguage(HTML)?
        ~6: PRESENTATION: Data is encrypted. Data Payload (UDP): Data?
        ~7: APPLICATION: Data is created in a format users can understand. HypertextTransferProtocol(HTTP)+CSS?
    ~COMPUTER-HARDWARE: Central/Graphical Processing Unit (C/GPU)
        : CLOCK
        : TEMPORARY MEMORY REGISTERS:
            : INSTRUCTION-ADDRESS REGISTER & MEMORY ADDRESS: Pointer(Next Address Reference) -> Index
                : MULTIPLEXER: MUX = (a AND NOTsel) OR (sel AND b)
                    : NOT (in=sel, out=NOTsel)
                    : AND (in=a, in=NOTsel, out=aANDNOTsel)
                    : AND (in=sel, in=b, out=selANDb)
                    : OR (in=aANDNOTsel, in=selANDb, out=out)
                : MATRIX >>> GATES:
                    : AND (in=column, in=row, out=columnANDrow)
                        : AND (in=data, in=write-enable, out=set)
                        : NOT (in=data, out=NOTdata)
                        : AND (in=NOTdata, in=write-enable, out=reset)
                            : OR (in=set, in=outLOOP, out=setORoutLoop)
                            : NOT (in=reset, out=NOTreset)
                            : AND (in=setORoutLOOP, in=NOTreset, out=out)
                : AND-OR LATCH/MEMORY REGISTER & MEMORY BIT(0/1): 
                    : OR-LOOP (in=a, in=b, out=1)
                    : AND-LOOP (in=a, in=b, out=0)
            : INSTRUCTION REGISTER & OPERATIONS CODE (OPCODE): Algorithms= BruteForce, Selection, Merge, Dijkstra, Divide&Conquer
                : ARITHMETIC UNIT = Half>Full>Multi-bit Adder:
                    : XOR (in=a, in=b, out=abSUM)
                        : AND (in=a, in=b, out=aANDb);
                        : NOT (in=aANDb, out=NOTaANDb);
                        : OR (in=a, in=b, out=aORb);
                        : AND (in=NOTaANDb, in=aORb, out=out);
                    : AND (in=a, in=b, out=abCARRY)
                        : >XOR (in=abSUM, in=c, out=abcSUM)
                        : >AND (in=abSUM, in=c, out=abcCARRY)
                            ; >OR (in=abCARRY, in=abcBARRY, out=out)
                : LOGIC UNIT: Mux/DMux >>> Xor >>> Or/Nor >>> And/Nand >>> Not
            : REGISTERS A, B, C... for holding values temporarily. 
        : FLAGS OF BITS:
            : OVERFLOW(>)
            : NEGATIVE(<)
            : ZERO(=)

# **~STOP-&-CORRECT = NOT-IN:BLINK/DEAFEN/FLEE/MASK/FAST() - NOT-OUT:HIDE/MUTE/PAUSE/BLOW/SPIT(), TheLeastCommonDenominatorOf1**
## **~DECODE(UNKNOWN), KNOWN**
    ~NATURAL-LANGUAGE:
        : Fallacy Type – Determine whether the error is linguistic or conceptual.
            : For fallacies in language, clarifying ambiguous terms, sentence structure, or assumptions usually suffices. 
                : Equivocation: Using a word with multiple meanings ambiguously in an argument.
                : Amphiboly: Ambiguity arising from poor sentence structure or unclear phrasing.
                : Accent: Changing the meaning of a statement by emphasizing different words.
                : Composition: Assuming what is true of parts is true for the whole.
                : Division: Assuming what is true of the whole is true for each part.
            : Fallacies Outside Language: focusing on the logical structure, causation, or evidentiary support is essential. 
                : Begging the Question (Petitio Principii): Assuming the truth of what the argument is supposed to prove.
                : False Cause (Post Hoc Ergo Propter Hoc): Assuming that because one event follows another, the first caused the second.
                : Accident: Misapplying a general rule to an exception or specific case.
                : Converse Accident (Hasty Generalization): Drawing a broad conclusion from a limited sample.
                : False Analogy: Comparing two things that aren’t sufficiently similar in relevant aspects.
                : Slippery Slope: Assuming a small first step will lead to a chain of extreme events.
                : Ad Hominem: Attacking the person instead of the argument itself.
                : Appeal to Authority (Ad Verecundiam): Relying on an authority figure outside their area of expertise.
        : Invalid syllogisms: A logical error occurs (e.g., fallacies, undistributed middle). Undistributed Middle Fallacy, Incorrect reasoning
                All dogs are animals. All cats are animals. Therefore, all dogs are cats.
        : Uncertainty: inability to have perfect knowledge about the world, 
            
    : Induction (Epagōgē): We observe patterns in nature. Example: Seeing multiple instances of fire being hot.
    : INFERENCE BY RESOLUTION:
        ~1: Convert all knowledge into Conjunctive Normal Form (CNF):
            : Remove biconditionals (↔) and implications (→).
            : Apply De Morgan’s Laws to push NOT operators inward.
            : Distribute OR over AND to standardize logical clauses.
        ~2: Assume the negation of the query (¬Q).
        ~3: Use Resolution Inference:
            : Find clauses with complementary literals (P and ¬P).
            : Resolve them to create new clauses.
            : Repeat until empty clause (∅) is derived (indicating a contradiction).
        ~4: If an empty clause is found, the query is true; otherwise, it's false.
    : Using Reduction & Proofs: Aristotle reduced complex arguments to basic valid forms using:
        : Direct reduction: Rearranging premises to match known valid syllogisms.
        : Indirect proof (reductio ad absurdum) to disprove invalid reasoning.  
 
    : TRANSFORMERS ARCHITECTURE: "Attention is all needed." 
        : Encoder: input word + positional encoding >>> (multi-head self attention >>> neural network) * Number >>> encoded representation
        : Decoder: previous output word + positional encoding >>> (multi-head self attention >>> (encoded representations) attention >>> neural network) * Number >>> encoded representation
        ~1: Encoder-Decoder Architecture
            : Encoder: Processes the input sentence into a fixed representation.
            : Decoder: Generates the output sequence, one word at a time.
        ~2: Self-Attention Mechanism
            Instead of using RNNs, the Transformer calculates attention scores for all words in a sentence simultaneously.
            Multi-Head Attention enables different aspects of word relationships to be captured.
        ~3: Positional Encoding: Since Transformers do not process sequences sequentially, positional encoding is added to retain information about word order.
        ~4: Feed-Forward Layers: Each word's representation is passed through fully connected layers to extract deeper features.
        ~5: Masked Self-Attention in the Decoder: Prevents words from attending to future words (maintains causality).
        ~6: Output Prediction: The decoder predicts the next word using a softmax function, generating the final output.
        ~7: Optimization and Training
            Uses the Adam optimizer with learning rate scheduling.
            Dropout and Label Smoothing are applied for regularization.
            Beam Search is used for better sentence generation.
                ~SEARCH/Queries: Retrieves specific data from the database. To access and analyze stored information.
                    ~1: Define Initial State: Start with a known state.
                    ~2: Check Goal State: Verify if the current state meets the goal criteria.
                    ~3: Expand Nodes: Generate possible next states from the current state.
                    ~4: Store in Frontier: Maintain a list of unexplored nodes.
                    ~5: Use Search Strategy: Choose the next state based on the algorithm.
                    ~6: Avoid Infinite Loops: Track visited states to prevent redundant exploration.
   
    ~SYLLOGISM/DEMONSTRATION(Apodeixis): Deduction (Syllogismos): From these first principles, we derive further necessary truths using logical reasoning.
        : Defining the Syllogism: A syllogism is a logical argument where a conclusion follows necessarily from two premises. It has three parts:
            : Term 1 (Major term) – Found in the major premise and conclusion. "All mammals (Middle Term) are warm-blooded. (Major Premise)"
                All humans are mortal. (Universal and necessary premise)
            : Term 2 (Minor term) – Found in the minor premise and conclusion. "Whales are mammals. (Minor Premise)"
                Socrates is a human. (Particular known fact)
            : Term 3 (Middle term) – Links the two premises but does not appear in the conclusion. "Therefore, whales are warm-blooded. (Conclusion)"
                Therefore, Socrates is mortal. (Demonstrated conclusion)
        : Identifying Syllogistic Figures & Moods: Aristotle categorized syllogisms into different figures and moods based on how terms are positioned.
            : Figure 1: Middle term is subject in one premise, predicate in another.
            : Figure 2: Middle term is predicate in both premises.
            : Figure 3: Middle term is subject in both premises.
            : Figure 4: Middle term switches placement.
        : Each figure contains valid or invalid moods, which define how premises are arranged using:
            : A (Universal Affirmative: "All A are B")
            : E (Universal Negative: "No A are B")
            : I (Particular Affirmative: "Some A are B")
            : O (Particular Negative: "Some A are not B")
        
    : STATEMENT: ADVERB, VERB, ADJECTIVE, PRONOUN, PAST-FUTURE TENSES (1, 2, 3, 4, 8, 9): Propositions (statements) are combinations of words that express truth or falsity.
        : Affirmation & Negation: Every proposition affirms or denies something. A proposition and its negation cannot both be true at the same time (Law of Non-Contradiction).
            : Affirmation: “Socrates is wise.”
            : Negation: “Socrates is not wise.”
        : Contradictions & Opposites (Square of Opposition)
            : Contradictory statements: One must be true, the other false. “It is day.” vs. “It is not day.”
            : Contrary statements: Both cannot be true, but both can be false. “All men are wise.” vs. “No man is wise.”
        : Modal Logic (Necessity vs. Possibility): Implication: Modal logic helps in predicting future truths without contradiction.
            : Necessity: Something must be true. “The sun must rise.”
            : Possibility: Something may or may not be true. “It may rain tomorrow.”
    
    : WORD: Etymology: Words are symbols of mental concepts: Identify the Subject, the Primary substance, that is the individual entities (e.g., Socrates, this particular tree).
        : FIXES: Know its Attributes, Accidental properties, the Characteristics that vary without changing substance, Using the Remaining Nine Categories
            : HOW: POSITIVE (+1/Vice of Excess) & NEGATIVE (-1/Vice of Deficiency)
                : Quality – What kind of thing it is (e.g., "red," "brave," "intelligent").
                : Quantity – How much or how big something is (e.g., "five feet tall," "three liters").
            : WHY: CAUSE, EFFECT
                : Prime Mover (God), a being that causes motion without itself being moved. To avoid infinite regress, there must be a first, unmoved mover.
                : Material – What something is made of (e.g., a statue is made of marble).
                : Formal – The essence or shape of something (e.g., the design of the statue).
                : Efficient – What brings something into being (e.g., the sculptor carving the statue).
                : Final – The purpose or goal of something (e.g., the statue exists to honor someone).
            : WHEN: Time, SCHEDULE= BirthStart*DeathFinish... ClockCycle/Hertz/Second/Minute/Hour/Day/Month/Season/Year...: CHRONOLOGY, measure of motion in relation to before and after.
            : WHERE: Space, HOME= Earth*Heaven... Point/Index/DomainNameSystem/FileDirectory/Position/Location/Continent/Sea/Climate...: ASTRONOMY (PTOLEMY), GEOGRAPHY
            : WHO: Relations, FAMILIAR= Mother*Father... Blood/Tribe/Race/Specie/Genus/Status...: Personality, Community (Polis), (e.g., "bigger than," "father of").
            : WHAT: State, FORM, Weights&Measures, Metals/Conductors, Flags, Letters/Spells, File Types: Array, Libraries, Node/Tree, Graph/Web/Forest, 3D Matrix... 
                : State/Condition – What condition it is in (e.g., "armed," "healthy," "wet").
                : Passion (Being Acted Upon) – What is being done to it (e.g., "being burned," "being pushed").
                : Action – What it is doing (e.g., "running," "writing").
                : Position – How it is arranged (e.g., "sitting," "lying down").
                : SEEING/EYES: Light: GEOMETRY (EUCLID): Bitmap: GraphicsGenerator>ScreenBuffer(ImageWidthxHeight): Character/Text/List/String = ASCII>UNICODE
                    +SEE-SHOW: Eyes, Camera, Optical/Ocular System, Photoreceptor, Display: DellMonitor, WacomTablet, 
                    -BLIND-HIDE: SHADOW(Terminator, Core, Occlusion, Cast), BLINK(Epilepsy, Autism), Void, Cover, Opacity(Clear-Opaque), Absorption, Refraction/Distortion (Water, Mirage), Blur
                    : Web, Letter, Flag, Media: Comics, Shows, Movies, Physique+Beauty, Portrait/Figure, Character, Concept/Sequential, GUI/DesktopMetaphor, 3DProjection,    
                    : VIEW: 1st, 2nd (Possession), 3rd-Person (God View)
                    : SHOT: Close-up, Medium, Long/Wide... 
                    : ANGLE: Up-Down,  Right-Left
                    : FORM: Dot(), Line(Straight, Curve), Shape(), Size(Proportion, Ratio), 
                    : LIGHT: SOURCE(Sun, Moon, Stars, Lamp...), White(High, Center, Halftone, Reflected(Shine, Matte)), COLOR(Red/Magenta, Green/Yellow, Blue/Cyan)
                : HEARING/EARS: Sound: MUSIC (BOETHIUS), Rode Mic, INSTRUMENT, Throat, RealtekSpeakers: Wave/Audio: Amplitude, Spectogram... 
                    ~MUTE-DEAFEN: SILENCE, Ambience, NOISE, Mumble, Stutter, Cry, Explode, Whisper, Introversion
                    ~HEAR-SOUND:
                    : Amp, Volume
                    : Length
                    : GENRES: Alt, Post-Rock, Country, Gregorian Chant, Foreign
                    : RHYTHM: Beat, SOUND EFFECTS
                : FEELING/SKINS: Motion: PHYSICS (ARISTOTLE), SKINS:	Hands, Feet, Skin, Mouse, Keyboard, Controller
                    ~AVOID-PAUSE: STILLNESS, Rest: EVASION, Clothes, Armour, Fear, Shyness, Rejection, 
                    ~FEEL-MOVE: MOTION: MartialArts, eSports, Dance, Animation/GUI, Robotics, Driving, Pokemon, Counter-Strike, BattleRealms, OnePiece, BannerSaga, Transistor
                    : EMOTION: Reaction, INERTIA, Love, Hate
                    : TEXTURE: Rough, Smooth
                    : MASS: Light, Heavy
                    : SPEED: Slow, Fast, 
                    : DISTANCE/ZOOM: In, Out
                    : TEMPERATURE: Cold, Warm, Hot, Weather:  Humidity, Pressure
                : SMELLING/NOSE: Air, Diffusion
                    : Inhaled: Smells(Floral, Fruity, Earthy, Spicy, Woody, Musky, Sweet...), Yawn, 
                    : Emitted/Exhaled: EXHAUST, Sigh, Sneeze/Cough, Burp, Fart, Vent/Purifyer, Cig, CarbonDioxide
                    : CHOKE: Suffocate, Hiccup, Cold, Asthma, Breath-Holding, 
                    : MASK/FILTER, BLOW: Fan, 
                : TASTING/TONGUE: Energy, Power, Heat
                    : EATEN: Throat, Stomach, Intestine, Flavors(Bitter, Salty, Sour, Sweet, Savory...) HautCuisin
                    : CREATED: BODY/Flesh/Blood, Physique/Health(CAFBasicTraining), Seed(TaoistNoNut)
                    : FAST: Hunger, Thirst, Starvation, 
                    : SOIL: Spit, Shit, Piss, Poison/Pollution, Disease, Waste Elimination
                    : Ingestion (Chewing & Swallowing), Enzyme Activity in the Small Intestine, Absorption of Nutrients
                    : GnRH (Gonadotropin-releasing hormone) from the hypothalamus triggers the release of LH (luteinizing hormone) and FSH (follicle-stimulating hormone), 
                    : Spermatogenesis(Testes) & Oogenesis(Ovaries)
        : ROOTS: FACT/KNOWN/AXIOMS: Know the Subject’s Substance (substantiam, οὐσία), that refers to the core identity or essence of things, answering "What?"
            : NEUTRAL (0): Golden Means
            : SEEN/HEARD/FELT/SMELLED/TASTED
            : Recognition of First Principles (Nous/Axioms): Through repeated observation, the intellect grasps universal truths. Must be:
                    : True (not subject to doubt).
                    : Primary (not derived from anything else).
                    : Immediate (not requiring proof).
                    ; More knowable than conclusions.
                Example in Geometry: Axioms like "The whole is greater than the part" must be accepted without proof.
                Example: Realizing "Fire is always hot" is a universal principle.

## **~CODE(), REASON:**
    : LOGIC-ARITHMETIC = -1, 0, +1
    : NOW-SPACE: Same Plane/Continuance of Evidence
    : HAPPINESS & THE GOLDEN MEAN: Deficiency (too little of a trait) vs Excess (too much of a trait). Example: Courage is the mean between cowardice (deficiency) and recklessness (excess).
        : The Highest Good is Happiness (Eudaimonia), worth pursuing for its own sake, contemplative, and is lived within a 
        : Virtue (arete): Moral Virtues developed through habit. needs Practical Wisdom (Phronesis), the ability to judge what is virtuous in different situations.
    : COMMUNITY (polis).
        : PUBLIC-SAFETY, 
    : POSTAL MECHANICS, MARITIME LAW, SEE-PASS, SEA-TREATY, DRYDOCK, DROGUE LAW: Flags, International Beaureau of Weights and Measures in France, Stamps, Autograph
    : ROBERT'S RULE OF ORDER provides a standardized structure for conducting meetings efficiently and fairly.
        ~1: Call to Order: The chairperson calls the meeting to order, marking the official start.
        ~2: Quorum Check: A record of who is present and absent is taken (optional for smaller meetings).
        ~3: Reading and Approval of Minutes: The minutes from the last meeting are read & proved by members.
        ~4: Reports of Officers, Boards, and Standing Committees: Matters carried over from previous meetings are discussed.
        ~7: New Business: New topics, proposals, or motions are introduced for discussion and decision-making.
        ~8: Announcements: Members share relevant updates, reminders, or upcoming events.
        ~9: Adjournment: The meeting is formally closed after a motion to adjourn is passed.
    : CORRECT-PARSE-SYNTAX-GRAMMAR: POSITION-LODIAL-FACT
        : FOR THE CAUSE: START-STATE = UNKNOWING|UNBEING(DIVIDE): starting knowledge base | empty assignment
        : OF THE EFFECT: GOAL-STATE = FOR THE KNOWING-BEING(ONENESS/NEUTRALITY): Eudaimonia
        : IS/ARE-THINKING:
        : WITH THE DUTY/PERFORMANCE: Moral & Intellectual Virtues, Phronesis
        : OF THE TERMS:
        : WITH THE CONTRACT:
        : BY THE AUTHORITY: ~AGENT/PLAYER/CORPORATION: BODY/I/HERE/NOW: knowledge-based agent(s) that reason by operating on knowledge        
            : JoeHisaishi, Rivermaya/Bamboo, LanaDR, ZackB, MidwestPenPals, Locomotora, KidC, RyX, X, Rivermaya, Bamboo, JuanKarlos, LanadelRey, ZackBryan, MidwestPenPals, Hillsong
            : DavidF, WesA, DenisV, TinaF, DanH, MatthewW, EiichiroO, HajimeI, Urusawa
            : Dusk&Dawn, Nerdwriter, MrMorj, Sawyer7mage, Werb
            : Proko, Steve H, Norman R, Alex R, Rene G, J.C. Leyendecker, Takeshi Obata, Jiraiya, MILO Y, Wurze, George H, Dusk&Dawn, Nerdwriter, Mr. Morj
    : COMPUTER LANGUAGES: MACHINE CODE
        : FETCH / INPUT STATEMENTS: 
            : IMPORT Library/Package
            : DECLARE/INITIALIZE Variables
            : Queries (SELECT, WHERE, JOIN, AGGREGATE functions): Extract insights and support decision-making.
        : DECODE: MEMEORY-ADDRESS + OPERATION
            : DATA DEFINITION LANGUAGE (CREATE, ALTER, DROP commands): Sets up the database structure for efficient storage.
            : DATA MANIPULATION LANGUAGE (INSERT, UPDATE, DELETE statements): Keep datacase data updated and accurate.
            : STORED PROCEDURES (CREATE, PROCEDURE, parameters, transactions, and error handling): Improve performance and handle business logic efficiently.
            : TRIGGERS (CREATE TIGGER for INSERT, UPDATE, DELETE): Enforce rules and log/audit changes automatically.
        : EXECUTE / OUTPUT STATEMENTS:
            : TRIGGERS/CONDITIONALS: Perform actions based on conditions.
                : If/ElseIf/Else: Executes code based on logical conditions. To handle multiple outcomes.
                : Switch: Simplifies multi-condition branching. To streamline complex conditional logic.
                : Exception Handling: Manages runtime errors. To handle errors gracefully and ensure program stability.        
            : LOOPS: Repeats code execution based on conditions. To perform repetitive tasks.
                : While: Repeats while a condition is true. To handle indefinite iteration.
                : Do-While: Executes at least once before checking conditions. To ensure at least one iteration.
                : For: Iterates a specific number of times. To handle definite iteration.
            : RETURN: Exits a function and optionally returns a value. To end execution and provide a result.
                : Then/Else/Next...  
                : Continue: Skips to the next iteration. To bypass unnecessary code in specific cases.
                : Break: Exits a loop or switch statement early. To terminate iterations based on conditions.        
    : RHETORIC: systematic study of persuasion, analyzing how language, logic, and emotion influence an audience. 
        ~TITLE:                         How do we know each other? How do we find closure?
        ~1: INTRODUCTION (Exordium): Establishes credibility (ethos) and engages the audience.
            : Ethos (Character & Credibility): Achieved through expertise, moral character, and goodwill toward the audience.
            : HOOK QUESTION:            Have you ever cursed, like that? Is this by instinct, or by choice?
            : MEANING:                  Let me ask a bigger question: Are we bound by our habits or do we act out of our free will?
            : THESIS:                   This speech shares that we have free will — the ability to choose.”
                                        The Three Kinds of Rhetoric (Based on Purpose)
                                            : Deliberative (Political) Rhetoric – Concerned with future actions (e.g., laws, policies).
                                            : Forensic (Judicial) Rhetoric – Concerned with past actions (e.g., guilt or innocence in legal cases).
                                            : Epideictic (Ceremonial) Rhetoric – Concerned with praise or blame (e.g., speeches at events, eulogies).  
            : TRANSITION:               First: why are we slaves of our passions? 
        ~2: NARRATION (Narratio): Presents background information and context.
            : Pathos (Emotional Appeal): Uses vivid storytelling, analogies, and emotional triggers to influence perception.
            : Support:                  You are right: SLEEPING FOR-BY DREAM: MADNESS, NIGHTMARE, Worst Case, FALLACIES: DIVISION, LACKING, [HIERARCHY = EAT AND BE EATEN. FORGET-ERASE NATURAL-ENGLISH.]
                                        SPOIL FOR-BY SOILVOID(-): Disruptions, Damages, Uncontrolled Elements (Dice), Expenses, taxes, and liabilities, Low Health, Resource Scarcity/Finity, Bankruptcy
                                        BAIT/SACRIFICE FOR-BY MOTHERBEAST.": NPCs/Requests/Puzzles, Alone/LowPopulation, WildEncounters + EnemyRaids/Ambush, Rivals, SocialLadder
                                        TRAP FOR-BY WILDWORLD: The Rat Race, 
                                        WAIT FOR-BY BIRTHSTART: Initial State, Beginning Again
            : TRANSITION:               But what if this is only half-true?
            : Introduction:             AWAKENING FOR-BY REALITY. "I KNOW! THAT'S RIGHT!": REASON: ARITHMETIC+LOGIC, REALIZATION OF THE DREAM, ONENESS, COMPLETENESS/FULFILLMENT!
                                        [FAIRNESS = KNOW AND BE KNOWN. READ-WRITE ARITHMETIC-&-LOGIC, SENSES IN LATIN-&-GREEK]
                                            : Win Condition: players must fulfill their dream on the Fast Track or reach a certain level of passive income.
                                            : Winning rounds builds your team’s momentum, giving you both an economic and psychological edge in the match.
                                        FRUIT FOR-BY SEEDWORD(+)
                                            : Mental Library, pokedex, Map, Contact List,
                                            : Skills / Experience Points, Abilities/Stats, New Moves, Karma, 
                                            : Art & Design: Color, Logo, Web, Comics, Video, Audio, Game, Store Set Up
                                            : Opportunities: Resources: Money, Income, Investments, Passive Income, Items, Badges/Priviledges
                                            : Testimonials, Reviews
                                        SON FOR-BY FATHERGOD: Team: Accountant/ComputerScientist, Investors, Publishers, Fathers, Brotherhoods, Gentlemen, the “New Rich”
                                        WAY FOR-BY KINGDOMHEAVEN: Creative Directing Studio: Channels/Web/Store
                                            : Build Structures/LEVELS: Balance scope budget, and schedule  
                                                : NAVIGATION, Maps, Atmosphere, Weather,
                                                : Progressing the game storyline and accessing new areas.
                                                : better positioning on the map, better territory
                                        CHANCE FOR-BY DEATHEND
                                            : Timeline: Every time the player passes "Payday" on the board, they receive their paycheck.
                                            : Incorporation/Fiscal Year: December 1, 2024... 1-2 days per project
                                            : PROGRESS = Tutorials, Saves, Updates: Journal?
                                            : Battle Cycle: 1 move/turn at a time: Best of 7 Rounds: Round-Time: 3 minutes
                                            : DEADLINE: Goal State, Completion
                                            : Fast Track, Here, they focus on making larger investments and fulfilling their dream, which is a personal goal they select at the start of the game.       
        ~3: PROOF (Confirmatio): Develops logical (logos) arguments with supporting evidence.
            : Logos (Logical Argument): Uses deductive (enthymeme) and inductive reasoning (example-based proof).
                                        : Finding a Commonplace (Topos) for Argument
                                        : Forming Premises from Endoxa (Common Opinions)
            : TRANSITION:               How don’t they entirely negate free will
        ~4: REFUTATION (Refutatio): Anticipates counterarguments and disproves them. Primarily focusing on eristic (contentious) arguments used in debate 
            : For fallacies in language, clarifying ambiguous terms, sentence structure, or assumptions usually suffices. 
                : For Equivocation: “The law should be followed because it is the ‘law of nature,’” 
                    clarify that legal law and natural law are distinct concepts, thus invalidating the argument’s logic.
                : For Amphiboly: If someone says, “Flying planes can be dangerous,” 
                    clarify whether they mean that piloting planes is dangerous or that planes in flight are hazardous.
                : For Accent: “I didn’t say she stole the money,” 
                    show how different emphases change the implied meaning and that no conclusion can be reliably drawn.
                : For Composition: “All parts of the car are lightweight, so the whole car must be lightweight,” 
                    show that a car’s total weight differs from its individual parts.
                : For Division: “The team is successful, so every team member is successful,” 
                    point out that team success doesn’t imply each member’s personal success.
            : Fallacies Outside Language: focusing on the logical structure, causation, or evidentiary support is essential. 
                : For Begging the Question (Petitio Principii): “Reading is beneficial because it’s good for you,” 
                    explain that “good for you” is simply restating “beneficial” without further evidence.
                : For False Cause (Post Hoc Ergo Propter Hoc): “I started wearing my lucky charm, and my grades improved,” 
                    explain that improved grades may be due to other factors, like studying harder.
                : For Accident: “Cutting people is wrong, so surgeons are immoral,” 
                    clarify that surgery is a controlled, beneficial exception to the general rule against cutting.
                : For Converse Accident (Hasty Generalization): “One politician lied, so all politicians are liars,” 
                    explain that one instance doesn’t justify generalizing about all politicians.
                : For False Analogy: “Employees are like nails; you have to hit them on the head to make them work,” 
                    explain that employees and nails are different and shouldn’t be treated the same way.
                : For Slippery Slope: “If we let students redo assignments, they’ll expect to retake exams,” 
                    explain that allowing assignment revisions doesn’t logically lead to redoing all assessments.
                : For Ad Hominem: “You shouldn’t listen to her because she’s not a scientist,” 
                    clarify that the person’s background doesn’t inherently disprove their argument’s validity.
                : For Appeal to Authority (Ad Verecundiam): If a celebrity endorses a health product, 
                    explain that fame does not qualify them as a medical expert, and scientific evidence is required for credibility.
            : TRANSITION:
        ~5: CONCLUSION (Peroratio): Reinforces key points and leaves a lasting impression, often with pathos.
            : QUESTION:                 So, are we simply animals flowing along the current of passion, or do we have free will? 
            : THESIS:                   We are capable of both — of habits, but empowered to rise above them.
            : MEANING:                  This question matters because it shows how If we believe we have no choice, 
            : REVIEW POINTS:
                Point 1:                Habits and instincts strongly influence our behavior.
                Point 2:                Self-awareness, delayed gratification, and cultural evolution prove our capacity for free will.
                Point 3:                Addressing counterarguments reveals the balance between instinct and choice.
            : CLOSING:                  Ultimately, the power to choose defines what it means to be human.

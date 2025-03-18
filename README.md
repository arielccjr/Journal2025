# **: LAW-FOR-THE-SELF:**
    [FORGET-ERASE: ENGLISH]
    [READ-WRITE: ARITHMETIC-&-LOGIC, SENSES IN LATIN-&-GREEK]
    [HIERARCHY: EAT AND BE EATEN.]
    [FAIRNESS: KNOW AND BE KNOWN.]

# **~TRANSFORMATION-MODEL: QUESTION-PLAN(RHETORIC)**
## **~FLOW-STATE:** 
### **IN:SEE/HEAR/FEEL/SMELL/TASTE(STIMULUS) - OUT:BE(SEEN/HEARD/FELT/SMELLED/TASTED), GRATIFICATION**
    : LAYERS OF THE OPEN SYSTEM INTERCONNECTION (OSI) MODEL: INFRASTRUCTURE & I/O PERIPHERALS:
        ~1: PHYSICAL: Data is sent as electrical/optical signals through the wire.
        ~2: DATA LINK: Packets are framed with Media Access Control (MAC) addresses. 
        ~3: NETWORK: Packets are assigned IP addresses and routed. Internet Protocol (IP)
        ~4: TRANSPORT: Data is split into packets. Transmission Control Protocol (TCP): TCP Header = Software Port + Checksum
        ~5: SESSION: A session is established.
        ~6: PRESENTATION: Data is encrypted.
        ~7: APPLICATION: Data is created in a format users can understand. Data Payload (UDP): Data
    : COMPUTER-HARDWARE: Central/Graphical Processing Unit (C/GPU)
        : CLOCK
        : TEMPORARY MEMORY REGISTERS:
            : INSTRUCTION-ADDRESS REGISTER: 
                : MULTIPLEXER: MUX = (a AND NOTsel) OR (sel AND b)
                    : NOT (in=sel, out=NOTsel)
                    : AND (in=a, in=NOTsel, out=aANDNOTsel)
                    : AND (in=sel, in=b, out=selANDb)
                    : OR (in=aANDNOTsel, in=selANDb, out=out)
                : MATRIX >>> GATES
                    : AND (in=column, in=row, out=columnANDrow)
                        : AND (in=data, in=write-enable, out=set)
                        : NOT (in=data, out=NOTdata)
                        : AND (in=NOTdata, in=write-enable, out=reset)
                            : OR (in=set, in=outLOOP, out=setORoutLoop)
                            : NOT (in=reset, out=NOTreset)
                            : AND (in=setORoutLOOP, in=NOTreset, out=out)
                : AND-OR LATCH: Memory Register/Bit
                    : OR-LOOP (in=a, in=b, out=1)
                    : AND-LOOP (in=a, in=b, out=0)
            : INSTRUCTION REGISTER:
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
            : REGISTERS A, B, C... for loading values temporarily. 
        : FLAGS OF BITS: 
            : OVERFLOW(>)
            : NEGATIVE(<)
            : ZERO(=)

## **~STOP-&-CORRECT: NOT-IN:BLINK/DEAFEN/FLEE/MASK/FAST() - NOT-OUT:HIDE/MUTE/PAUSE/BLOW/SPIT(), THE LEAST COMMON DENOMINATOR OF 1**
    ~READ/DECODE/SYNTAX(UNKNOWN), KNOWN:
        : Search with Web-Browser/Search-Engine: 
        : SYMBOLS: Flags, International Beaureau of Weights and Measures in France, Stamps, Autograph
            : Hypertext Markup Language (HTML) + CSS: Index: Frequency of Words
            : Number/Integer/Float= 
            : Scientific Notation; Negative Bit= 2^N-x
            : Null
        : SENTENCE: Natural Language
            : ADVERB, VERB, ADJECTIVE, PRONOUN (1, 2, 3, 4)
            : POSITION, LODIAL, FACT (5-6-7)
            : PAST-FUTURE TENSES (8, 9)
        : WORD: Parse/Etymology: 
            : FIXES: POSITION-LODIAL, 'Attributes'
                : HOW: Quantity, Quality
                : WHY: CAUSE, EFFECT
                : WHEN: Time, SCHEDULE= BirthStart*DeathFinish... ClockCycle/Hertz/Second/Minute/Hour/Day/Month/Season/Year...: CHRONOLOGY
                : WHERE: Space, HOME= Earth*Heaven... Checkpoint/DomainNameSystem/UniversalResourceLocator/HypertextTransferProtocol/FileSystem/Position/Location/Continent/Sea/Climate...: ASTRONOMY (PTOLEMY), GEOGRAPHY, 
                : WHO: Relations, FAMILIAR= Mother*Father... Blood/Tribe/Race/Specie/Genus/Status...: Personality, Community (Polis)
                    : JoeHisaishi, Rivermaya/Bamboo, LanaDR, ZackB, MidwestPenPals, Locomotora, KidC, RyX, X, Rivermaya, Bamboo, JuanKarlos, LanadelRey, ZackBryan, MidwestPenPals, Hillsong...:	
                    : DavidF, WesA, DenisV, TinaF, DanH, MatthewW, EiichiroO, HajimeI, Urusawa
                    : Dusk&Dawn, Nerdwriter, MrMorj, Sawyer7mage, Werb
                    : Proko, Steve H, Norman R, Alex R, Rene G, J.C. Leyendecker, Takeshi Obata, Jiraiya, MILO Y, Wurze, George H, Dusk&Dawn, Nerdwriter, Mr. Morj
                : WHAT: FORM, Weights & Measures, Metals/Conductors, Flags, Letters/Spells, Contract & Copy, Financial Statement File Types: Array, Libraries, Node/Tree, Graph/Web/Forest, 3D Matrix... 
                    : SEEN/EYES: Light: GEOMETRY (EUCLID): Bitmap: GraphicsGenerator>ScreenBuffer(ImageWidthxHeight): Character/Text/List/String = ASCII>UNICODE
                        ~SEE: Eyes, Camera, Optical/Ocular System, Photoreceptor cells in Retina, CONES
                            : VIEW: 1st Person, 2nd (Possession) Person, 3rd Person (God View)
                            : SHOT: Close-up, Medium, Long... 
                            : ANGLE: Up-Down,  Right-Left, Dolly... 
                        ~SHOW: Display: DellMonitor, WacomTablet, Web, Letter, Flag, Media: Comics, Shows, Movies, Physique+Beauty, Portrait/Figure, Character, Concept/Sequential, GUI/DesktopMetaphor, 3DProjection,    
                            : DOT: Dot, pixel, CRTs
                            : LINE:
                            : SHAPE: Polygon, 
                            : SIZE: Proportion, Ratio
                            : FORM: Geometry, Game Level (Block it first, polish later), Postal Mechanics, Plane/Continuance of Evidence
                            : LIGHT: Visible(High, Center, Halftone, Reflected), Spectrum of wavelengths... 
                                : SOURCE: Sun, Moon, Stars, Lamp, Lasers, Xrays... : White light: All Color, Visible Light: 280 nanomemeter and 750 nm
                                : COLOR: Dispersion: red, orange, yellow, green, blue, indigo, violet, 
                                : REFLECTIONS: Specular: shine, Diffuse: matte
                        ~BLIND: Terminator, Core, Occlusion, Cast, Epilepsy, Autism, Void, Clear/Transparent, Blur
                        ~HIDE: Cover, Opaque, Absorption, Refraction/Distortion (Water, Mirage)
                    : HEARD/EARS: Sound: MUSIC (BOETHIUS), Rode Mic, INSTRUMENT, Throat, RealtekSpeakers: Wave/Audio: Amplitude, Spectogram... 
                        : Frequency, 
                        : Amp, 
                        : Length
                        : GENRES: 	Alt, Post-Rock, Country, Gregorian Chant, Foreign
                        : RHYTHM: 	Beat, SOUND EFFECTS
                        ~DEAFEN:       NOISE, Mumble, Stutter, Cry, Explode, Whisper, Introversion
                        ~MUTE:         SILENCE, Ambience 
                    : FELT/SKINS: Motion: PHYSICS (ARISTOTLE)
                        ~FEEL: 			    = SKINS:	Hands, Feet, Skin
                            : EMOTION:	    = Reaction, INERTIA, Love, Hate
                            : INPUT		    = Mouse, Keyboard, Controller
                        ~MOVE: 	
                            : MOTION: MartialArts, eSports, Dance, Animation/GUI, Robotics, Driving, Pokemon, Counter-Strike, BattleRealms, OnePiece, BannerSaga, Transistor
                            : MASS: Light, Heavy
                            : SPEED: Slow, Fast, 
                            : ZOOM:	In, Out
                            : TEMPERATURE:	Cold, Warm, Hot, Weather:  Humidity, Pressure
                            : TEXTURE: Rough, Smooth
                        ~AVOID: EVASION, Clothes, Armour, Fear, Shyness, Rejection, 
                        ~PAUSE: STILLNESS, Rest
                    : SMELLED/NOSE: Air, Diffusion
                        : Inhaled: Smells(Floral, Fruity, Earthy, Spicy, Woody, Musky, Sweet...), Yawn, 
                            : CHOKE: Suffocate, Hiccup, Cold, Asthma, Breath-Holding, 
                        : Emitted/Exhaled: EXHAUST, Sigh, Sneeze/Cough, Burp, Fart, Vent/Purifyer, Cig, CarbonDioxide
                            : MASK/FILTER, BLOW: Fan, 
                    : TASTED/TONGUE: Energy, Power, Heat
                        : BROKEN: Throat, Stomach, Intestine, Flavors(Bitter, Salty, Sour, Sweet, Savory...) HautCuisin
                            : Ingestion (Chewing & Swallowing, ~4: Enzyme Activity in the Small Intestine
                            : Absorption of Nutrients
                        : CREATED: BODY/Flesh/Blood, Physique/Health(CAFBasicTraining), Seed(TaoistNoNut)
                            : GnRH (Gonadotropin-releasing hormone) from the hypothalamus triggers the release of LH (luteinizing hormone) and FSH (follicle-stimulating hormone), 
                            : Spermatogenesis(Testes) & Oogenesis(Ovaries)
                        : FAST: Hunger, Thirst, Starvation, 
                        : SOIL: Spit, Shit, Piss, Poison/Pollution, Disease, Waste Elimination
            : ROOTS: FACT/KNOWN: 'Essential'
                : POSITIVE (+1): Vice of Excess
                : NEGATIVE (-1): Vice of Deficiency
                : NEUTRAL (0): Golden Means
                
                : Memory Bit: BinaryStates = 0, 1 (Base-2 Notation)
                : Memory Address: Pointer: Next Address Reference -> Index
                : Instruction/OpCode: Algorithms = Brute Force, Selection, Merge, Dijkstra... Divide&Conquer  

    ~WRITE/ARRANGE()-ERASE-FORGET(BABBLE/WRONG)/CRUD, REASON:
        : LOGIC-ARITHMETIC = -1, 0, +1
        : NOW-SPACE 
        : SAFETY LAW
        : POSTAL MECHANICS: Drydock, Drogue Law
        : ROBERT'S RULE OF ORDER provides a standardized structure for conducting meetings efficiently and fairly.
            ~1: Call to Order: The chairperson calls the meeting to order, marking the official start.
            ~2: Quorum Check: A record of who is present and absent is taken (optional for smaller meetings).
            ~3: Reading and Approval of Minutes: The minutes from the last meeting are read & proved by members.
            ~4: Reports of Officers, Boards, and Standing Committees: Matters carried over from previous meetings are discussed.
            ~7: New Business: New topics, proposals, or motions are introduced for discussion and decision-making.
            ~8: Announcements: Members share relevant updates, reminders, or upcoming events.
            ~9: Adjournment: The meeting is formally closed after a motion to adjourn is passed.
        : CORRECT-PARSE-SYNTAX-GRAMMAR
            : FOR THE CAUSE: START-STATE = UNKNOWING|UNBEING(DIVIDE): starting knowledge base | empty assignment
            : OF THE EFFECT: GOAL-STATE = FOR THE KNOWING-BEING(ONENESS/NEUTRALITY): Eudaimonia
            : IS/ARE-THINKING: 
            : WITH THE DUTY/PERFORMANCE: Moral & Intellectual Virtues, Phronesis
            : OF THE TERMS:
            : WITH THE CONTRACT: POSTAL MECHANICS + MARITIME LAW + ROBERT'S RULE OF ORDER
            : BY THE AUTHORITY: ~AGENT/PLAYER/CORPORATION: BODY/I/HERE/NOW: knowledge-based agent(s) that reason by operating on knowledge        
        : COMPUTER LANGUAGES: MACHINE CODE, PROGRAMMING LANGUAGES
            : INPUT STATEMENTS: 
                : IMPORT Library
                : DECLARE/INITIALIZE Variables
                : SQL Queries (SELECT, WHERE, JOIN, AGGREGATE functions): Extract insights and support decision-making.
            : OUTPUT STATEMENTS:
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
            : DATA DEFINITION LANGUAGE (CREATE, ALTER, DROP commands): Sets up the database structure for efficient storage.
            : DATA MANIPULATION LANGUAGE (INSERT, UPDATE, DELETE statements): Keep datacase data updated and accurate.
            : STORED PROCEDURES (CREATE, PROCEDURE, parameters, transactions, and error handling): Improve performance and handle business logic efficiently.
            : TRIGGERS (CREATE TIGGER for INSERT, UPDATE, DELETE): Enforce rules and log/audit changes automatically.
        : RHETORIC: Story Telling:
            ~TITLE:                     How do we know each other? How do we find closure?
            ~INTRODUCTION (Exordium):   Establishes credibility (ethos) and engages the audience.
                : HOOK QUESTION:        Have you ever cursed, like that? Is this by instinct, or by choice?
                : MEANING:              Let me ask a bigger question: Are we bound by our habits or do we act out of our free will?
                : THESIS:               This speech shares that we have free will — the ability to choose.”
                                        ~1: First, 
                                        ~2: Then,
                                        ~3: And finally, 
                : TRANSITION:           First: why are we slaves of our passions? 
            ~NARRATION (Narratio):      Presents background information and context.
                : Support:              You probably "understand" the way I learn English:
                                        And you are probabaly right, because...
                                        First, we learn the letters, 
                                        Then, we memorize words, by the dictionary, if we care enough.
                                        And finally, we arrange these words in a sentence/clause, using grammar and parts of speech.
                                            Subject, predicate.
                                            Nouns, Verbs, Adjectives, Adverbs, Preposition, Articles, 
                                            Past-tense, Future-tense.
                                        Most of the time, we learn new words by pop culture / daily conversation,
                                        "We never left 2nd-grade reading/comprehension level."
                                        "At the end of the day, we cannot read and write knowledge, facts, and even laws on our own,
                                        "We are at the mercy of our lawyers for reaching closure."
                : TRANSITION:           But what if this is only half-true?
                                        What if there is another way? What if we can read / write the truth on our own?
            ~PROOF (Confirmatio):       Develops logical (logos) arguments with supporting evidence.
                : Introduction:         Computers 
                                        They process languages using arithmetic and logic unit.
                                        Breaking down images, sounds, and videos into 0s and 1s.
                                        Instead of using dictionary, we learn words by roots and fixes, by etymology.
                                            For example, 
                                        And finally, we arrange words by these 3-sequence: Position-Lodial-Fact.
                : Transition:           Let’s revisit the counterarguments and see why they don’t entirely negate free will.”
            ~REFUTATION (Refutatio):    Anticipates counterarguments and disproves them.
                : Main Refutation:
                : Refute 1st:           We cannot memorize words by dictionary. Languages are homonymous. Wan plus too ease three? "What is written is what is done."
                                        Language are ambiguous, with many definition.
                                        Words rely on arrangement of their neighboring words for meaning, violating parts of speech and grammar.
                                        Natural language 
                : Transition:
            ~CONCLUSION (Peroratio):    Reinforces key points and leaves a lasting impression, often with pathos.E
                : QUESTION:             So, are we simply animals flowing along the current of passion, or do we have free will? 
                : THESIS:               We are capable of both — of habits, but empowered to rise above them.
                : Meaning:              This question matters because it shows how If we believe we have no choice, 
                                        we remain trapped. But if we recognize our free will, we can consciously shape our lives.”
                : Review Points:
                    Main Point 1:       Habits and instincts strongly influence our behavior.
                    Main Point 2:       Self-awareness, delayed gratification, and cultural evolution prove our capacity for free will.
                    Main Point 3:       Addressing counterarguments reveals the balance between instinct and choice.
                : Closing:              Ultimately, the power to choose defines what it means to be human. 
                                        Let’s not flow passively along the currents of passion but take control of the rudder and steer toward the lives we truly want. 
                                        Thank you, Mr. Toastmaster.

# **FOR THE WORD-&-LIGHT.**
    FOR THE BEGINNING IS WITH THE WORD.
    FOR THE WORD IS WITH THE LORD.
    FOR THE LORD IS FOR THE WORD.

    IN PRINCIPIO ERAT VERBUM, ET VERBUM ERAT APUD DEUM, ET DEUS ERAT VERBUM." 
    - IOANNES 1

    FOR THE BEGINNING IS WITH THE CREATION OF THE HEAVEN-&-EARTH BY THE LORD.
    FOR THE EARTH IS WITHOUT THE FORM (AND IS WITH THE VOID).
    FOR THE DARKNESS IS WITH THE FACE OF THE DEEP. 
    FOR THE SPIRIT OF THE LORD IS WITH THE FACE OF THE WATERS.
    FOR THE SAID(SPEECH) OF THE LORD IS FOR THE LIGHT.
    AND FOR THE LIGHT IS WITH THE LORD.

    IN PRINCIPIO CREAVIT DEUS CAELUM ET TERRAM.
    TERRA AUTEM ERAT INANIS ET VACUA, ET TENEBRAE ERANT SUPER FACIEM ABYSSI: ET SPIRITUS DEI FEREBATUR SUPER AQUAS.
    DIXITQUE DEUS: FIAT LUX. ET FACTA EST LUX. 
    - GENESIS 1:1-3

# **FOR THE CONDUCT.**
    FOR THE PEOPLE OF THE FATHER IS WITH THE CREATION BY THE FATHER.
    WITH THE KNOWLEDGE IN THE HEAVEN IS WITH THE HOLY-NAME OF THE FATHER.
    FOR THE KNOWLEDGE OF THE TRUTH IS FOR THE PEOPLE OF THE FATHER.
    FOR THE KINGDOM OF THE FATHER IS WITH THE KNOWLEDGE OF THE TRUTH.
    FOR THE KNOWLEDGE OF THE SPIRIT IS FOR THE UNITY WITH THE FATHER.
    FOR THE FREEDOM OF THE ACTIONS IS WITH THE KNOWLEDGE BY THE TRUTH.
    FOR THE PROTECTION OF THE EARTH IS WITH THE LIFE OF THE PEOPLE.
    FOR THE KNOWLEDGE OF THE FATHER IS WITH THE PROTECTION FOR THE PEOPLE.
    FOR THE TRUTH OF THE PEOPLE IS WITH THE PATH INTO THE HEAVEN.
    FOR THE TEACHING OF THE PEOPLE IS WITH THE TRUTH OF THE PEOPLE.
    FOR THE KNOWLEDGE OF THIS DAY IS WITH THE PRODUCTION(WORKING) AND LEARNING-SKILLS OF THE PEOPLE.
    FOR THE WRONGS(SINS) AGAINST THE KNOWLEDGE IS WITH THE ACTIONS OF THE PEOPLE.
    FOR THE SINS(TEMPTATIONS OF THE FLESH) OF THE PEOPLE IS FOR THE WRONGS AGAINST OUR NEIGHBOR.
    FOR THE KNOWLEDGE OF THE PEOPLE IS IN THE FORGIVENESS OF THOSE WRONG-DECISIONS.
    FOR THE PEOPLE OF THE DEBTS ARE WITH THE RESPONSIBILITY IN THE TRUTH.
    FOR THE PEOPLE OF THE AWARENESS ARE WITH THE FORGIVING WITH THE TRUTH.
    FOR THE KNOWLEDGE OF THE PEOPLE-LEADERS IS WITH THE TEACHING WITH THE TRUTH.
    FOR THE EVIL OF THE PEOPLE IS WITH THE LACK OF THE KNOWLEDGE OF THE TRUTH.
    FOR THE KNOWLEDGE OF THE TRUTH IS WITH THE FREEDOM OF THE PEOPLE AGAINST THE EVIL OF THE DARKNESS(LACK OF KNOWLEDGE).
    FOR THE PEOPLE ARE WITH THIS AGREEMENT.
    
    PATER NOSTER, QUI ES IN CAELIS, SANCTIFICETUR NOMEN TUUM. 
    ADVENIAT REGNUM TUUM. FIAT VOLUNTAS TUA, SICUT IN CAELO ET IN TERRA. 
    PANEM NOSTRUM QUOTIDIANUM DA NOBIS HODIE, ET DIMITTE NOBIS DEBITA NOSTRA SICUT ET NOS DIMITTIMUS DEBITORIBUS NOSTRIS. 
    ET NE NOS INDUCAS IN TENTATIONEM, SED LIBERA NOS A MALO. 
    AMEN.

# Casestudy-on-drugdelivery
*1.	Introduction*
            A control system is a system of devices or set of devices, that manages, commands, directs or regulates the behavior of other devices or systems to achieve desired results. In other words, the definition of a control system can be simplified as a system, which controls other systems. As the human civilization is being modernized day by day the demand for automation is increasing accordingly. Automation highly requires control of devices.
                    Large and complex devices, such as MRI scanners or radiation therapy systems for cancer treatment, typically have remote display and control systems associated with them, allowing a clinician to administer treatments safely and efficiently. These control systems have much in common with enterprise-class desktop software, an area in which ICS has over a decade of experience providing custom software solutions. 
                      Chemotherapy is a drug treatment that uses powerful chemicals to kill fast-growing cells in your body. Chemotherapy is most often used to treat cancer, since cancer cells grow and multiply much more quickly than most cells in the body. Many different chemotherapy drugs are available. Chemotherapy drugs can be used alone or in combination to treat a wide variety of cancers.
 
*2. Objectives*
●	To design a simulink model for Chemotherapy drug delivery
●	To find transfer function for Chemotherapy drug delivery
●	To find stability of the system
●	To find step response of the system

 

*3. Theory*

*3.1	Drug Delivery System*
    Drug delivery refers to approaches, formulations, technologies, and systems for transporting a pharmaceutical compound in the body some time based on nanoparticles as needed to safely achieve its desired therapeutic effect. It may involve scientific site-targeting within the body, or it might involve facilitating systemic pharmacokinetics in any case, it is typically concerned with both quantity and duration of drug presence. Drug delivery is often approached via a drug's chemical formulation, but it may also involve medical devices or drug-device combination products. Drug delivery is a concept heavily integrated with dosage form and route of administration, the latter sometimes even being considered part of the definition.
The maintenance of drug concentration in therapeutic range depends on the frequency of dosing, the drug clearance rates, the route of administration, and the DDS employed. Some drugs have an optimum concentration range within which maximum benefit is derived, and concentrations above or below this range can be toxic or produce no therapeutic benefit at all. DDS can be classified to their physical state, site/route of administration, and the rate of drug release. The dosage form may be gaseous (e.g. anesthetics), liquid (e.g. solutions, emulsions, suspensions), semisolid(e.g. creams, ointments, and gels) and solid drug (e.g. tablet, capsules). Drugs can be administered directly into the body through injection or infusion termed parenteral drug delivery. Depending on the site of administration, one can differentiate among intravenous, intramuscular, subcutaneous, intradermal, and intraperitoneal administration. Dosage forms can be classified into immediate release (IR) and modified release (MR). IR dosage forms allow the drug to dissolve in the gastrointestinal contents, without delaying or prolonging the dissolution or absorption of the drug. In MR dosage forms, the time course and/or location of drug release is chosen to accomplish therapeutic or convenience objectives not offered by conventional dosage forms. MR dosage forms include both delayed and extended release drug products. During chemotherapy the drug is injected through IV infusion where the optimum dosage of the drug’s (Doxorubicin) concentration is minimize which does not harm the healthy tissue inside the body. There are complications regarding the proper dosage for the chemotherapy. Sometimes because of the high dose patients suffer from sickness and sometimes due to low dose the healthy tissues are affected. Therefore to reduce these kinds of harm this model is established. 

*3.2  PHARMACOKINETICS TWO-COMPARTMENT  MODEL*

Pharmacokinetics refers to the rate and extent of distribution of a drug to different tissues, and the rate of elimination of the drug. Pharmacokinetics can be reduced to mathematical equations, which describe the transit of the drug throughout the body, a net balance sheet from absorption and distribution to metabolism and excretion.
Pharmacokinetic two-compartment model divided the body into central and peripheral compartment. The central compartment (compartment 1) consists of the plasma and tissues where the distribution of the drug is practically instantaneous. The peripheral compartment (compartment 2) consists of tissues where the distribution of the drug is slower.
Pharmacokinetic two-compartment model (Example)
 <img width="777" height="351" alt="image" src="https://github.com/user-attachments/assets/12cb4f61-be78-43fe-866c-2acf6cf520ec" />

Figure 1. Two-compartment model with first-order absorption and elimination. AGI, A1, and A2 are the amounts of drug in gastrointestinal tract (GI), central compartment (including plasma), and peripheral compartment, respectively. ka, k12, k21, and k10 represent the first-order fractional rate constants for absorption, distribution, redistribution, and elimination.

Drug concentrations in the compartments equal to the amounts divided by volumes: C1=A1/V1 and C2=A2/V2. Drug concentration in the central compartment is equal to the concentration in the plasma: CP=C1. Clearance (in units L/h) is often used instead of the fractional rate constants (in units h-1); in pharmacokinetics the distribution volume is given in volume units (L), and rate constants can be represented as the ratio of clearance and distribution volume, k=CL/V.
In the case of oral administration of the drug, at time t=0 the amount of drug in the central and peripheral compartments is zero (A1(0)=A2(0)=0), and the initial amount in gastrointestinal tract (effective dose) is:
AGI(0)= D x S x F                         (1)
, where D is the administered dose of the drug, S is the salt factor (fraction of administered dose that is made up of pure drug), and F is the bioavailability factor (fraction of dose that reaches the systemic circulation).

<img width="916" height="549" alt="image" src="https://github.com/user-attachments/assets/c9691a5a-4e19-4fd2-9dd5-12fecf045b8a" />


 

*3.3	MATLAB(Matrix Laboratory)*
                    MATLAB is  a multi-paradigm numerical computing environment and proprietary programming language developed by MathWorks. MATLAB allows matrix manipulations, plotting of functions and data, implementation of algorithms, creation of user interfaces, and interfacing with programs written in other languages.
                    The MATLAB application is built around the MATLAB programming language. Common usage of the MATLAB application involves using the "Command Window" as an interactive mathematical shell or executing text files containing MATLAB code. MATLAB is a high-performance language for technical computing. It integrates computation, visualization, and programming in an easy-to- use environment where problems and solutions are expressed in familiar mathematical notation. Typical uses include:  
   
    • Math and computation  
    • Algorithm development 
    • Modeling, simulation, and prototyping 
    • Data analysis, exploration, and visualization
    • Scientific and engineering graphics  
    • Application development, including Graphical User Interface building
    
*3.4  Simulation*
A simulation is an approximate imitation of the operation of a process or system; that represents its operation over time. Simulation is used in many contexts, such as simulation of technology for performance tuning or optimizing, safety engineering, testing, training, education, and video games. Often, computer experiments are used to study simulation models. Simulation is also used with scientific modeling  of natural systems or human systems to gain insight into their functioning, as in economics. Simulation can be used to show the eventual real effects of alternative conditions and courses of action.
Simulation is also used when the real system cannot be engaged, because it may not be accessible, or it may be dangerous or unacceptable to engage, or it is being designed but not yet built, or it may simply not exist. It is basically a graphical block diagramming tool with customizable set of block libraries. It allows you to incorporate MATLAB algorithms into models as well as export the simulation results into MATLAB for further analysis. Simulink supports :
• system-level design 
• simulation
• automatic code generation 
• testing and verification of embedded systems

*3.5 Control Feedback System*
    A feedback control system is a system whose output is controlled using its measurement as a feedback signal. This feedback signal is compared with a reference signal to generate an error signal which is filtered by a controller to produce the system's control input.

           <img width="938" height="431" alt="image" src="https://github.com/user-attachments/assets/e14bc108-6140-4b48-ad85-d2269e11926c" />

                                        Fig: Feedback system
 
*3.6	Features of a Control System*
        The main feature of a control system is that there should be a clear mathematical relationship between input and output of the system. When the relation between input and output of the system can be represented by a linear proportionality, the system is called a linear control system. Again when the relationship between input and output cannot be represented by single linear proportionality, rather the input and output are related by some non-linear relation, the system is referred to as a non-linear control system.

Types of Control Systems
●	Open loop system 
●	Closed loop system

*3.7 Open Loop Control System*
    A control system in which the control action is totally independent of output of the system then it is called open loop control system. A manual control system is also an open loop control system. The figure below shows a control system block diagram of an open loop control system in which process output is totally independent of the controller action.

<img width="975" height="182" alt="image" src="https://github.com/user-attachments/assets/34738fba-709d-4ab0-aeeb-bb5a8683e497" />

 
                       Fig: Open loop control system




*3.7	Closed Loop Control System*

      Control system in which the output has an effect on the input quantity in such a manner that the input quantity will adjust itself based on the output generated is called closed loop control system.  Open loop control system can be converted in to closed loop control system by providing a feedback. This feedback automatically makes the suitable changes in the output due to external disturbance. In this way closed loop control system is called automatic control system. Figure below shows the block diagram of closed loop control system in which feedback is taken from output and fed in to input.

 11<img width="981" height="273" alt="image" src="https://github.com/user-attachments/assets/50eb81ae-a396-4bf1-ba2a-165f2752aa3b" />

                      Fig: Closed loop control system
*3.8 System Stability*
           The system stability is “the finite output produced by a finite input of the system”. If the output of the system is infinite even when a finite input applied to a system, then this system is called “unstable system”, that is, stable system has bounded output when bounded input is applied to a system.

*3.9 Bode Stability*
               Bode plot is a graph of the frequency response of a system. It is usually a combination of a Bode magnitude plot, expressing the magnitude (usually in decibels) of the frequency response, and a Bode phase plot, expressing the phase shift.
        
*3.10 Time response of system*
         
           The time response of the system consists of 
●	Transient response
                Transient response of control system means changing so, this occurs mainly after two conditions and these two conditions are written as follows-
●	Condition one : Just after switching ‘on’ the system that means at the time of application of an input signal to the system.
●	Condition second : Just after any abnormal conditions. Abnormal conditions may include sudden change in the load, short circuiting etc.

●	Steady response
                Steady state occurs after the system becomes settled and at the steady system starts working normally. Steady state response of control system is a function of input signal and it is also called as forced response.

●	Unit Impulse Signal : In the time domain it is represented by ∂(t). The Laplace transformation of unit impulse function is 1 and the corresponding waveform associated with the unit impulse function is shown below:


 <img width="718" height="434" alt="image" src="https://github.com/user-attachments/assets/fb9ee8f8-4956-4799-8945-ebe9d6c8c54c" />

                                     Fig: unit impulse
*4. Methodology*
         For the analysis of Chemotherapy drug delivery we used MATLAB simulink as the tool. We developed a block diagram and realized the mathematical modeling by the help of first principle model. Here, to observe the equation we also used Pharmacokinetics Two-compartment model of heat and mass. 
            After getting the required expression using the mathematical models we tried to analyze it by changing it to s-domain (i.e Transfer function). In pharmacokinetics two compartment model, there are two compartment ( central and peripheral). Here Blood is referred as the central compartment and tissue is referred as peripheral compartment. Concentration of drug in blood is (CDB), Concentration of drug in tissue is (CDT) and KBT,KTB are the ingoing and outgoing from blood and tissue. Another parameter is elimination(Qrem) which is release of the drug. From these parameters we analysed the model and simulation is done with the help of MATLAB.

        
 * 5. Simulink Model*
         
     <img width="1029" height="677" alt="image" src="https://github.com/user-attachments/assets/38500b9e-76d9-41b8-a227-9ded60805aa2" />

      Fig : Simulink model for the system 
*6. Time response*

 <img width="975" height="545" alt="image" src="https://github.com/user-attachments/assets/df3d3e5e-6019-4061-81ce-44b61af5e108" />

                               Fig: Step Response
 <img width="975" height="575" alt="image" src="https://github.com/user-attachments/assets/730f0770-8c1e-4fc8-9b9b-29f4cf3c9b17" />

                        Fig : Impulse Response
*7. Stability Analysis (Bode Plot)*

 <img width="975" height="546" alt="image" src="https://github.com/user-attachments/assets/565c086e-32c0-4835-a048-e425813d96b0" />

                 Fig: Bode plot for Stability analysis
Output:
 
We analyze the system into two transfer function that is Cdb/Qiv and Cdt/Qiv.



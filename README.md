# LEDESMA_PURISIMA.cpp
Project/ Pre-final: C++ Visual Novel - Dispatch Decision Engine

This C++ application is a text-based graphic novel. It represents the first episode of a story-driven game in which the player takes control of Robert and makes choices that impact the plot, character interactions, and resolution. Player decisions are saved in global variables so they can affect next scenes, and each scene is implemented as a distinct function.

The application illustrates fundamental C++ ideas like:

Global variables
Boolean logic
Counters with integers
void functions
Conditional statements with if and else
Input and output from users

The Function of Global Variables

bool gameFailed
keeps track of the player's performance in the street fight. Later sequences are omitted if this is the case.

bool choseMercy
preserves the moral decision made by the player throughout the interrogation scenario. choose if Robert takes a path of mercy or brutality.

bool romanceActive
shows whether Blonde Blazer's romance route is active.

int blazerReputation
shows how vividly the public and Blonde Blazer recall Robert's deeds. Stronger impressions are associated with higher values.

bool streetFightSurvived
keeps track of whether Robert makes it through street combat.

string toxicResolution
contains a brief account of the resolution of the last battle with Toxic.

These variables function as memory, enabling choices made in previous scenes to influence results in subsequent ones.

Function Breakdown and Decision Paths

Scene 1: sceneApartmentInterrogation()

Goal: presents the story's central moral choice.

Options for Decision-Making:

Catch the offender → Mercy

Let the criminal go → Ruthlessness

Impact on the Story: 
Updates isMerciful.
Later fight scenes' words and actions are influenced by this choice.
Robert's underlying character becomes apparent in this scene.

Scene 2: sceneStreetF()

Goal: shows how tactical choices have quick effects.

 Options for Decision-Making:

 Punch with the right hand ⇒ Failure result
 Punch with the left hand ⇒ Successful result

 Impact on the Story: 
doesn't alter global variables
 emphasizes that decisions can have immediate effects
 Instead of long-term branching, this scene emphasizes gameplay logic.

Scene 3: sceneBarFlambae()

Goal: demonstrates how relationships and reputation are impacted by public activities.

Options for Decision-Making:

Throw water: less memorable but safer
Throw alcohol → Risky, disorderly, and unforgettable

Impact on the Story: 
Blazer_Impression_Score is updated.
Alcohol preference raises the score higher, indicating a more favorable public perception.
Blonde Blazer's memories of Robert in the epilogue are influenced by this scene.

Scene 4: sceneBillboardMoment()

Goal: introduces romantic and emotional decision-making.

Options for Decision-Making:

Kiss Blonde Blazer → The romance starts
Let the moment pass. Tension still exists.

Impact on the Story: 

isRomanticTensionActive is updated.
assesses the possibility of a romantic conclusion.
Vulnerability and emotional intelligence are highlighted in this situation.

Scene 5: sceneFightToxic()

Goal: reflects Robert's well-known fighting style.

Options for Decision-Making:

Punt Toxic → creative and showy
Stomp Toxic → Effective and brutal

Impact on the Story:

uses isMerciful to change the conversation a little.
demonstrates agreement or disagreement with past moral decisions
The scene here illustrates how decisions made in the past affect narrative in the present.

epilogue_summary()

Goal:
gives a concluding synopsis of the narrative based on collective selections.

Use of Logic:

Whether Robert is remembered as kind or cruel depends on how kind he is.

Blonde Blazer's recall of Robert is determined by Blazer_Impression_Score.

Whether a romance starts depends on isRomanticTensionActive.

Robert's move from front-line hero to dispatcher behind the scenes is completed by this function, which completes the Pivot.

main()

Goal:
regulates the program's flow.

Behavior:

calls the functions of each scene sequentially.

calls epilogue_summary() at the end.

The scenes play in order since the main() function serves as the plot driver.

This program shows how to use fundamental C++ ideas to generate branching narratives.  Global variables serve as memory that stores player choices, and each scene function represents a story node.  Based on user input, the computer generates various story pathways and endings using straightforward if/else logic.


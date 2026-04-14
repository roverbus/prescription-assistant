# User Flow Description - AI-Assisted Prescribing Access Assistant

## Narrative User Flow

The clinician walks into the room and begins a discussion with a patient about obesity treatment. The patient says they have been trying diet and exercise for months, feel discouraged, and want to start a medication soon. During the conversation, the clinician mentions a `GLP-1 receptor agonist` such as semaglutide. The assistant, listening through live recording and transcript detection, recognizes that the medication is being seriously considered and quickly checks the likely access barriers in the background.

Within a few seconds, the clinician sees: `Medium: covered, but prior auth and step therapy may delay start.` The assistant also suggests a more accessible alternative, such as `generic phentermine`, which is often easier for plans to cover than semaglutide when clinically appropriate. Knowing the patient is eager to start soon and may get discouraged by a long approval process, the clinician decides it is better to talk through both options before the visit ends.

Using the assistant's communication guidance, the clinician says, `"The medication we first talked about is still a good option, but your insurance may require extra approval steps and may ask us to try another treatment first, which could slow things down. One option, if it is a safe fit for you, is to start generic phentermine for the next three months. That may help you begin treatment sooner, and it may also improve our chances of getting a GLP-1 approved later if we still need it. Let me walk you through both options so we can choose the best next step for you."` The clinician remains the final decision-maker, and the recommendation and supporting reasoning are saved so the logic is not lost after the visit.


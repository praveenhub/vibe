Untitled-1                                   app_flow_document.mdc U X
.cursor > rules > app_flow_document.mdc

Rule Type
Always                       This rule attached to every chat and command+k request

Update this rule if user requested changes to the project requirement, etc.
# Braindump App Flow Document

## Onboarding and Sign-In/Sign-Up

When users first visit the Braindump web application, they are greeted by a calming, minimalist landing page with soothing colors like light blue and lavender that immediately sets a tranquil tone. Users quickly understand the concept of using the app as an AI-powered journaling and productivity tool designed to transform raw thoughts into structured insights, to-dos, daily reflections, and weekly productivity reports. The sign-up process is streamlined with a single-click option to sign in using Google through the Clerk authentication provider, meaning users can instantly create an account without the need for a lengthy form. In addition, if a user forgets their password, a clearly marked recovery option is available, sending a reset email so that they can easily regain access. Logging out is also straightforward, with a logout option accessible from the profile section on any page of the application.

## Main Dashboard or Home Page

After a successful sign-in, the user is taken to a central dashboard that acts as the heart of the app. This dashboard is designed with simplicity and clarity in mind. The primary view includes a modern, clean interface featuring a sidebar and a top navigation menu that clearly indicate the main modules of Braindump. These modules include Brain Dump for journal entries, Daily Review for end-of-day summaries, Weekly Report for overarching productivity insights, and Focus Mode for deep work sessions. The layout is intuitive, ensuring that users can navigate easily between reviewing previous entries, starting a new brain dump, or entering a focused work mode without feeling overwhelmed by too many options at once.

## Detailed Feature Flows and Page Transitions

The journey within Braindump is carefully designed to flow naturally from one key feature to the next. In the Brain Dump section, users can either type their thoughts directly or choose to speak them using the integrated voice-to-text functionality powered by the Deepgram API. When opting for voice input, the app captures and transcribes the spoken words with only a short delay to maintain a natural workflow. The raw input collected is automatically processed in the background using the OpenAI API with the GPT4 model, which organizes the content into clear insights, actionable to-dos, and reflective comments. Once the processing is complete, users are taken to a dedicated review page where they can see the AI-generated outputs alongside their original entry. This page allows for manual edits, ensuring that users can customize the insights to match their own understanding and requirements. Transitioning further, if a user decides to work on their tasks, they can easily switch to the Focus Mode page. Here, the app provides a customizable timer, break reminders, and notifications related to upcoming tasks, ensuring a seamless movement between planning, execution, and review. The design of each page supports quick navigation back to the dashboard or to other sections, ensuring a cohesive and connected experience throughout the entire app.

## Settings and Account Management

Users have access to a comprehensive account management section that is accessible from a prominent profile icon on the main dashboard. In this area, the app allows users to update their personal information, configure their notification settings, and manage linked services such as Google Calendar, Trello, and Outlook. The settings also include options for exporting data, enabling users to download logs, journal entries, and reports as PDF files or sync them with cloud storage services like Google Drive or Dropbox. Additionally, the billing and subscription details are seamlessly integrated into the account management area for those features that might require a premium upgrade. Once users update their settings, a clear navigation option enables them to return directly to their previous workflow, ensuring that they can easily continue managing their journaling and productivity tasks without disruption.

## Error States and Alternate Paths

Braindump is built with the user experience in mind, even when unexpected situations occur. When users input invalid data, such as an incomplete voice recording or a corrupted journal entry, the app responds with clear and informative error messages that explain the issue and offer guidance for correction. Connectivity issues or temporary failures in external services like Deepgram or the OpenAI API are handled gracefully by notifying users through contextual pop-ups or inline messages, along with options to retry the process. If a user attempts to access a restricted area without proper permissions, a fallback page appears that explains the situation and provides a path to return to a secure area of the application. These message ensure that users never feel lost and are always guided back to the normal flow of the application.

## Conclusion and Overall App Journey

The journey through Braindump is designed to be smooth, efficient, and reassuring. It begins with a calm and friendly onboarding process that builds trust and sets the tone for clarity and productivity. Once users are signed in, the main dashboard offers an intuitive gateway into the myriad features of the app, from voice-to-text journaling to AI-generated insights and actionable to-dos. Users can easily switch between creating entries, reviewing insightful summaries, and focusing on deep work with customizable timer settings and distraction blockers. The account management section allows for personalized adjustments and integration with other productivity tools, while error handling maintains seamless continuity in the user experience. Overall, every component of the Braindump app is interconnected, ensuring that whether a user is journaling a fleeting thought, reflecting on a day's progress, or planning the next focused work session, the journey remains cohesive, supportive, and in tune with the goal of enhancing mental clarity and productivity.

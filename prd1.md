Untitled-1                                   project_requirements_document.mdc U X
.cursor > rules > project_requirements_document.mdc

Rule Type
Always                       This rule attached to every chat and command+k request

Update this rule if user requested changes to the project requirement, etc.
# Project Requirements Document (PRD)

## 1. Project Overview

Braindump is an AI-powered journaling and productivity web application built to help users transform their raw thoughts
into clear insights and actionable steps. It offers a unique way to capture ideas, emotions, and reflections using both
text and voice input. The AI engine then organizes the raw input into structured insights, tailored to-do items, daily
summaries, and comprehensive weekly reports. This design not only aids in mental clarity by tracking emotional and
productivity patterns but also helps users stay on top of their goals with a streamlined workflow.

The purpose of Braindump is to simplify the process of self-reflection and productivity management. By converting a
brain-dump of ideas into clear outputs like action steps and reflective summaries, users can more easily understand and
act upon their thoughts. Key objectives include ensuring an effortless journaling experience, delivering quick and
accurate transcriptions with short delays, providing editable AI-generated insights, and integrating seamlessly with
third-party productivity tools such as Google Calendar, Trello, and Dropbox. Success will be measured by user engagement,
improved productivity tracking, and overall satisfaction with the clarity of insights provided.

## 2. In-Scope vs. Out-of-Scope

**In-Scope:**

*   Voice-to-Text Journaling that leverages Deepgram API for accurate and near-real-time transcription.
*   AI-Powered Insights & Reflections generated through OpenAI's GPT-4 model, organizing raw journal entries.
*   Actionable To-Dos Generation derived from each journal entry.
*   Daily Review Summary that compiles the day's entries and completed tasks.
*   Weekly Productivity Report showcasing user progress and consistency.
*   Focus Mode with customizable deep work session timers, break reminders, distraction blockers, and notifications.
*   Integration with third-party services such as Google Calendar, Trello, Asana, Google Drive, Dropbox, and Outlook for
    task management and calendar syncing.
*   User account management using Clerk (with Google sign-in) to manage authentication and data privacy.
*   Manual editing capabilities for AI-generated insights, to-dos, and reports.

**Out-of-Scope:**

*   Native mobile application support; Braindump is a web application only.
*   Real-time transcription perfection; short delays are acceptable as long as accuracy is maintained.
*   Advanced analytics beyond daily summaries and weekly reports in the initial version.
*   Integrations with other productivity tools or calendar apps not mentioned, unless added in a future phase.
*   Offline functionality or local data storage beyond browser sessions.

## 3. User Flow

A new user visiting Braindump is greeted by a minimalist and calming welcome screen designed with soothing colors (light
blue, green, lavender) and modern sans-serif fonts. The user signs up or logs in using Google through Clerk
authentication. After a smooth onboarding process, the user lands on a clean dashboard that serves as the central
navigation hub, where they can select a brain-dump session, view their to-dos, or check the day's summary.

Once on the dashboard, the user can either type in or use the voice-to-text feature to record a journal entry. After
speaking or typing, the app processes the input through AI, displaying structured insights, action items, and reflective
points in an intuitive review page. The user can then manually adjust the generated content. Finally, depending on the
day's progress, the user can enter Focus Mode to work through their to-dos using customizable timer settings or review
the daily summary and weekly report to track progress and sync tasks with integrated third-party tools like Google
Calendar or Trello.

## 4. Core Features

**Voice-to-Text Journaling:**
Seamless transcription of spoken thoughts via Deepgram API, ensuring short delays and high accuracy.
**AI-Powered Insights & Reflections:**
AI-driven organization of journal entries using OpenAI's GPT-4 model to generate clear insights, takeaways, and
reflections.
**Actionable To-Dos Generation:**
Creation of clear and tailored to-do items based on user entries, designed to be completed by the end of the day.
**Daily Review Summary:**
End-of-day summaries that compile journal entries and track completed tasks to help users reflect on their
productivity.

**Weekly Productivity Report:**
Aggregated report of daily entries and tasks that showcases trends in productivity and consistency over a week.
**Focus Mode with Integrated Task Management:**
Customizable focus sessions with adjustable timers, break reminders, distraction blockers, and notifications for
upcoming tasks.
**Third-Party Integrations:**
Integration with calendar apps (Google Calendar, Outlook) and task management tools (Trello, Asana), along with data
export options (PDF, Google Drive, Dropbox).
**Manual Editing Capabilities:**
Allow users to edit AI-generated insights, to-dos, and reports to personalize outputs.

## 5. Tech Stack & Tools

**Frontend Frameworks & Languages:**

*   Next.js for building the web application.
*   Tailwind CSS for modern and minimalist styling.
*   Typescript for a robust type system and improved code quality.
*   Shadcn UI for pre-built UI components ensuring consistency in design.

**Backend & Services:**

*   Supabase for database management and backend-as-a-service.
*   Clerk for third-party authentication, specifically enabling Google sign-in.
*   OpenAI API (using GPT-4 model) for processing journal entries and generating insights.
*   Deepgram API for voice-to-text functionality.

**Additional Tools & Integrations:**

*   Integration with Google Calendar, Trello, Asana, Google Drive, Dropbox, and Outlook for task and calendar management.
*   Cursor and Claude 3.5 Sonnet for advanced AI-powered code assistance to maintain high productivity during development.

**Starter Kit Reference:**

*   CodeGuide Starter Pro (GitHub repository: <https://github.com/codeguide-dev/codeguide-starter-pro>) is used for project structure and initial setup.

## 6. Non-Functional Requirements

**Performance:**

*   Ensure fast response times for voice-to-text transcription (short delays are acceptable).
*   Rapid generation of AI insights and summaries without noticeable lag.

**Security:**

*   Secure management of user data and journal entries.
*   Use secure third-party authentication via Clerk.
*   Implement HTTPS for data transmission and stringent access controls on sensitive data.

**Compliance & Usability:**

*   Adherence to data privacy standards and regulations.
*   Intuitive and accessible UI design that prioritizes ease of navigation and minimal distraction.
*   Responsive design to cater to various screen sizes in a web environment (desktop-focused).

**Reliability:**

*   System should gracefully handle API interruptions or rate limits from OpenAI and Deepgram.
*   Maintain data integrity during user sessions and background tasks.

## 7. Constraints & Assumptions

The application is built as a web-only tool with no native mobile support initially.
Third-party services such as OpenAI API, Deepgram API, and Clerk must be available and functional.
The design assumes that users prefer a minimalist, distraction-free interface that conveys calmness and clarity.
Users are expected to have basic internet connectivity and the latest browser support for modern web applications.
Integration with calendar apps and task managers relies on external API availability, and any outages may affect seamless sync capabilities.
The project uses a pre-defined starter kit (CodeGuide Starter Pro) which informs the overall file structure and development patterns.

## 8. Known Issues & Potential Pitfalls

**API Rate Limits and Service Downtime:**
The app relies on multiple external APIs (OpenAI, Deepgram, Clerk), which may have rate limits or service interruptions. A fallback mechanism or rate limiting strategy should be implemented to handle temporary outages.
**Transcription Accuracy & Delays:**
While short delays in transcription are acceptable, ensuring high accuracy especially with varied speech patterns or accents could be challenging. Continuous testing with diverse voice samples is required.
**User Data Security:**
Handling sensitive journal entries means security is critical. Ensure that all integrations are secured and comply with relevant data privacy laws.
**Third-Party Integration Dependencies:**
The seamless integration with calendar apps and task managers might be affected by changes or deprecations in external APIs. Keep an eye on updates from Google Calendar, Trello, Asana, and cloud storage services.
**Manual Editing Clarity:**
Allowing users to edit AI-generated outputs introduces the risk of accidental data loss or formatting issues. Precise version control or "undo" features should be considered.
**UI/UX Complexity:**
Balancing a minimalist design with rich functionality may lead to usability challenges, especially for first-time users. Regular user testing and iterative design reviews are advised to mitigate this risk.

This document serves as the definitive reference for the Braindump AI Journaling and productivity tool. All subsequent technical documents--including Tech Stack Document, Frontend Guidelines, Backend Structure, App Flow, and IDE rules--should be developed in alignment with this PRD to ensure clarity and consistency in implementation.

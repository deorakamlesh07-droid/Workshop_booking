# Workshop Booking Documentation

This file explains the ideas behind the UI changes, how to run the project on your system, and how the mobile experience looks after the redesign.

## Setup Instructions

If you want to run the project locally, follow these steps:

1. Clone the repository:
   `git clone https://github.com/FOSSEE/workshop_booking.git`
2. Open the project folder:
   `cd workshop_booking`
3. Install the required packages using a Python version that works with this project:
   `py -3.7 -m pip install -r requirements.txt`
4. Check that `local_settings.py` contains valid local email configuration values.
5. Create the local database and tables:
   `py -3.7 manage.py migrate --run-syncdb`
6. Start the Django development server:
   `py -3.7 manage.py runserver 127.0.0.1:8000`
7. Open the project in your browser:
   `http://127.0.0.1:8000/`

## What Design Principles Guided The Improvements?

The main goal was to make the website easier for students to use, especially on mobile devices. I focused on clarity first, so the interface feels less crowded and important actions are easier to notice. Better spacing, clearer headings, and card-based sections were used to make the pages feel simpler and less overwhelming.

Another important principle was consistency. Instead of making one page look good and leaving the others unchanged, I tried to make the overall experience feel connected. Forms, workshop status screens, and detail pages now follow a more similar style, which makes the site easier to understand as you move from one page to another.

## How Did You Ensure Responsiveness Across Devices?

Responsiveness was handled by improving the shared layout and styles so the same pages work well on both phones and larger screens. The spacing, containers, and navigation were adjusted to fit smaller screens more naturally.

For pages with a lot of information, especially tables, I changed the layout so the content stacks better on mobile instead of forcing horizontal scrolling. I also made buttons and form fields larger and easier to tap, which helps a lot for students using the site on their phones.

## What Trade-Offs Did You Make Between The Design And Performance?

I tried to improve the look and usability without making the project heavy. Most of the redesign was done with HTML and CSS, which keeps the experience fast and avoids adding extra JavaScript just for visual changes.

I also worked with the existing Django template setup instead of trying to rebuild the frontend from scratch. That means the redesign stays practical and safer for the current project, even if it limits some bigger architectural changes. I did add a lightweight Google font to improve the typography, which adds a small extra request, but the visual improvement felt worth it.

## What Was The Most Challenging Part Of The Task And How Did You Approach It?

The hardest part was improving the UI in a noticeable way without affecting the existing backend logic. Since this project already had an older Django template structure, the challenge was to make it feel modern and mobile-friendly while still respecting how the project already works.

I approached this by focusing on the pages that matter most in the coordinator journey, such as login, workshop status, workshop types, workshop details, and profile pages. That made it possible to improve the overall experience in a focused and practical way without making unnecessary changes elsewhere.

## Before And After Screenshots

### Before

#### Login

<img src="docs/screenshots/before changes/login.png" alt="Before login screen" width="250">

#### Register

<img src="docs/screenshots/before changes/register.png" alt="Before register screen" width="250">

#### Coordinator Dashboard

<img src="docs/screenshots/before changes/dashboard-coordinator.png" alt="Before coordinator dashboard screen" width="250">

#### Workshop Types

<img src="docs/screenshots/before changes/workshop-types.png" alt="Before workshop types screen" width="250">

#### Propose Workshop

<img src="docs/screenshots/before changes/propose-workshop.png" alt="Before propose workshop screen" width="250">

#### Profile

<img src="docs/screenshots/before changes/profile.png" alt="Before profile screen" width="250">

### After

<img src="docs/screenshots/after changes/after-login.png" alt="After mobile login screen" width="250">

### More Mobile Screens

#### Workshop Status

<img src="docs/screenshots/after changes/coordinator-03-status.png" alt="Coordinator mobile workshop status" width="250">

#### Workshop Types List

<img src="docs/screenshots/after changes/coordinator-04-types-list.png" alt="Coordinator mobile workshop types list" width="250">

#### Workshop Type Details

<img src="docs/screenshots/after changes/coordinator-05-type-details.png" alt="Coordinator mobile workshop type details" width="250">

#### Propose Workshop

<img src="docs/screenshots/after changes/coordinator-06-propose.png" alt="Coordinator mobile propose workshop" width="250">

#### Workshop Details And Comments

<img src="docs/screenshots/after changes/coordinator-07-workshop-details.png" alt="Coordinator mobile workshop details and comments" width="250">

#### Profile

<img src="docs/screenshots/after changes/coordinator-08-profile.png" alt="Coordinator mobile profile" width="250">

This is a simple expense tracker app.This app is made with flutter.

This is a personal skill improvements project.I am devided these into 8 phases.Below given details of 8 phases in 18 days.

Phases in Detail
Phase 1 — Foundation & Git
Discipline Day 1 (1 day)
Goal: Get a working repo and a real git workflow before writing any feature code.
● Create a new Flutter project (flutter create expense_tracker)
● Initialize a git repo and push it to GitHub
● Create your first feature branch: feature/setup
● Write a short README.md describing the app and your 8-phase plan
● Commit and merge feature/setup into main via a pull request
● Deliberately create a merge conflict: edit the same line of a file on two branches, then merge and
resolve it manually

Phase 2 — State Management —
Riverpod Day 2–4 (3 days)
Goal: Learn Riverpod by building it yourself, using only the official docs — no AI, no copying old project code.
● Add flutter_riverpod to pubspec.yaml and wrap the app in ProviderScope
● Create an Expense model class: amount, category, title, date, note
● Build a Notifier (or StateNotifier) that holds a List with add/remove/update methods
● Build a derived provider that computes the running total from the list
● Connect the list provider to a simple UI (even a plain ListView) just to confirm it works
● Commit each piece separately, writing WHY in the commit message, not just what changed

Phase 3 — Navigation — GoRouter Day 5–7 (3 days)
Goal: Wire up the 3 real screens (see UI section) with proper routing between them.
● Add go_router and configure it with 3 routes: Home, Add Expense, Expense Detail
● Build the Home screen UI (see UI spec) and connect it to your list + total providers
● Build the Add Expense screen UI and wire the Save button to your Notifier's add method
● Build the Expense Detail screen, passing the expense ID as a route parameter
● Make sure back navigation works correctly from every screen

Phase 4 — Persistence — Hive or Drift Day 8–10 (3 days)
Goal: Make expenses survive an app restart. Pick one storage option and set it up from scratch.
● Choose Hive (simpler, NoSQL-style) or Drift (SQL, closer to what many companies use)
● Set up the package and generate any required adapters/tables from the official docs
● Implement Create, Read, Update, Delete for expenses using your chosen storage
● Wire storage into your Riverpod providers so the list loads from disk on app start
● Test it by adding an expense, fully closing the app, and reopening it

Phase 5 — Async & Real API (optional
stretch) Day 11–12 (2 days)
Goal: Practice real async/await with a live network call, since this was a named weak spot.
● Pick a free public API (e.g. a currency exchange rate API)
● Write an async function that fetches the current rate using http or dio
● Show a loading indicator while the request is in flight
● Handle the error case (no internet, failed request) with a visible message
● Use the rate to optionally show each expense converted to USD
● Out loud, explain to yourself why each await is placed where it is

Phase 6 — Native & Platform Basics Day 13–15 (3 days)
Goal: Touch the native side of Flutter at least once, since this was a total blind spot.
● Generate an Android signing keystore using keytool
● Configure key.properties and build.gradle to use it
● Build a signed release APK or App Bundle (flutter build appbundle)
● Add one simple MethodChannel call from Dart to native Android (e.g. read the device battery level)
● Confirm the native call returns a real value into your Flutter UI

Phase 7 — Testing Day 16–17 (2 days)
Goal: Write and understand two real tests yourself — no AI-generated test code.
● Write one unit test for your total provider (e.g. adding two expenses gives the correct sum)
● Write one widget test for the Add Expense form (e.g. empty amount shows a validation error)
● Run flutter test and make sure both pass
● Go through each line of both tests and be able to explain what it checks and why

Phase 8 — Explain It (README) Day 18 (1 day)
Goal: Turn the finished project into something you can defend confidently in an interview.
● Write a README section: why Riverpod over GetX for this app
● Write a section: why you chose Hive or Drift
● Describe your folder structure and why you organized it that way
● Add a short 'what I'd change at scale' section
● Practice explaining the whole project out loud in under 3 minutes
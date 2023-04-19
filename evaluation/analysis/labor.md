* Qi
	* Initial work / foundation
		* The language was designed
		* The initial implementation was written
	* Promotion / getting the word out / community
		* The initial author was invited to give a talk at RacketCon
		* The initial author received feedback on drafts of the talk
		* The initial author gave a talk at RacketCon
		* A Q&A was held after the talk
		* An early adopter advocated for the project
		* An early adopter advocated for the project
		* An early adopter advocated for the project
		* Advent of Code was solved using Qi
		* The idea of a Qi-themed event was suggested
		* The Qi design challenge was organized
		* A weekly meetup for the project was started
		* The first library extending Qi functionality was written
		* The first application leveraging Qi was written
		* There was a suggestion to write a tutorial
		* An interactive tutorial was written using racket templates
		* A theoretical connection between Qi and Arrows in category theory was drawn
	* Documentation
		* A quickscript for interactive evaluation in DrRacket was added to support the Qi tutorial
		* Improvements were made to a Vim plugin to better support the Qi tutorial
		* A broken link in the documentation was reported
		* There was a suggestion to create a wiki for Qi
		* The wiki was created
		* A Developer's Guide containing developer documentation was written
		* Documentation was written for Qi
		* Some formatting and typos in the docs were fixed
	* Improving usability / ease of adoption:
		* Distribution
			* There was a suggestion to distribute a Qi template using racket templates
			* There was a suggestion to decompose the package into lib/test/doc packages for more flexible development and distribution
			* The package was decomposed into lib/test/doc packages
			* An installation issue was reported
		* IDE support
			* A quickscript for entering unicode in DrRacket was written
			* A flow-oriented debugger was added
		* The package config was modified so that Qi appears in the languages section of the docs
		* A recipe for hosting backup documentation in case the package index is unavailable was provided
		* The backup docs workflow following the recipe was added
		* The repo was migrated to an organization account
		* Technical support was provided to Qi users
	* Implementation
		* The core macro was refactored into separate expansion and compilation stages
		* Macro extensibility
			* A simple macro extensibility based on prefix matching was designed, to allow users to extend the syntax of the language in a rudimentary way
			* An implementation for the prefix matching macro extensibility scheme was provided
			* Many options for proper macro extensibility were suggested
			* "First class" macro extensibility was implemented, allowing users to seamlessly extend the syntax of the language
		* Form improvements
			* Switch form
				* Improvements to the switch form were suggested
				* Improvements to switch were implemented
				* Some bugs in switch were fixed
			* Clos form
				* A design example was provided to motivate adding closures (the clos form) to Qi
				* The name clos was suggested for this form
			* Threading form error message
				* A confusing error message in the threading form was reported and a way to handle it was suggested
				* The suggested error message fix was implemented
				* Threading form bug
				* An elusive bug was identified that was causing performance degradation in the threading form
				* A hygiene issue related to the same bug was identified that could have caused other bugs in the future
			* Feedback form design improvements
				* An illustrative example to motivate design improvements to the `feedback` form of the language was provided
				* The design of `feedback` was improved
				* The PR improving the design of `feedback` was reviewed
			* Restricting fancy-app
				* There was a suggestion to restrict fancy-app's (a templatized function application library) scope in Qi to avoid tricky bugs in handling user input
				* fancy-app was restricted to just the fine-grained application form
				* The fancy-app PR was reviewed
			* Optimizing fanout
				* It was pointed out that fanout does not accept arbitrary Racket expressions for N
				* An optimized implementation was suggested for fanout
				* fanout was modified to support arbitrary expressions for N and have an optimized implementation
				* The fanout PR was reviewed
			* Partition
				* partition was added, which is a generalized version of the sieve form
				* The partition PR was reviewed
			* The ability to support the _ template in the function position was added
			* Support for keyword arguments to add bindings in lambda forms of the language was added
		* Reducing tech debt
			* Uses of deprecated macro form ~or were updated to ~or*
			* The unused let/flow and let/switch macros were removed
			* The organization of some tests was improved
	* Operational excellence
		* Performance
			* The partition implementation was optimized
			* Benchmarking scripts were added
			* The performance benchmarks were audited for accuracy
			* The benchmarks were fixed according to the audit
			* The number of dependencies was reduced
			* These tools were used to identify and remove all heavy dependencies and dramatically reduce load-time latency
			* The performance of any?, all?, and none? were significantly improved
			* There was a suggestion to use indirect documentation links to reduce build times
			* Some improvements were suggested to reduce memory consumption in building docs
		* Dev Tools
			* CI was set up for the project repository
			* Performance benchmarking was added to CI
			* A dependency profiler tool was written to identify heavy dependencies
			* A way to measure load-time latency was suggested
			* A script to measure load-time latency following that approach was written
			* The load-time latency PR was reviewed
			* The benchmarks runner config was modified to avoid reporting success when it failed

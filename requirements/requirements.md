# Project Requirements
This section is (as the name implies) a specification of requirements the product will need to achieve in order be classified as "complete"
these specs are posed as psuedo-acceptance tests that are User-centric (focusing on features visible strictly from a user's point of view)
These have been written using the GIVEN WHEN THEN FROMULA, since I intend to use them to write real acceptance tests in the same format, using Catch2 (and likely cmake).

The reason I chose to write acceptance tests is to avoid **scope-creep**, an everlong enemy of mine. having acceptance tests to tell me when I'm "done" helps me ship out a release faster, and keep other features i thought of for a different release of the project. Can't spend my whole live developing one thing, after all.
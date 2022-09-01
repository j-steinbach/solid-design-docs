Normative (WIP)

## Task-List (formerly Todo-List)

At the core of the Todo-app is a Task-List (TL). It MUST hold a collection of Tasks (T), which COULD be empty -- it is possible that the user hasn't created any Tasks yet.

The list MUST inform about who created it and when, whom the list is shared with, who is allowed to edit the list and when it was last changed.

The list SHOULD have a name, which gets displayed in the GUI and the browser window. Otherwise a name gets generated based on the Creator's name ("Jonas' Todolist"). In case of multiple lists with the same name a number gets appended ("Jonas' Todolist #1").

The list SHOULD also have a description, to give context about it's purpose. The description can contain text and media, similar to a Github Readme.

The list by default MUST be "private", ie. only the logged-in creator can access it. It further MUST provide access controls (AC) to give the owner granular control over who can access it and/or edit it. A private list MUST allow to invite other people to also access it ("share-able"), ie. to either see or also edit the list. Sharing COULD send a notification. Finally the list MUST be able to made public, which means that anyone can access it via URL.

---

Optional:

The list SHOULD also inform about the amount of items it contains in the GUI, and what their status is -- how many tasks remain to to and how many are done. This information MIGHT be stored in the TL or aggregated from the items in the collection.

The list SHOULD be filterable and searchable. The list SHOULD be reorder-able, which means that the user (anyone with edit-rights) can rearrange the list to his or her liking. The list SHOULD be export-able, e.g. print-able or be exported as plaintext. It SHOULD also be possible to share or export a filtered subset (a "view") of the list, either as parametrized link or as download.

## Task (formerly Todo-Item)

A Task --the atomic unit of the TL-- describes a single thing to be done by someone. One or more TI form a TL.

A task MUST be described in a single sentence. If that is not enough, the task CAN have a description with more information, data and media. [EN: I am not sure what to call the 'task'.. I am not a fan of "heading", "title" or "content". Maybe "name"? Or simply "task"?] E: "label" it is

A task MUST contain information about who created it and the date of its creation and last modification.

A task MUST have a state of TODO or DONE, although it COULD also have more states (e.g. PENDING, BLOCKED, OBSOLETE, CANCELLED, REVIEW, ARCHIEVED, ...). If the task is done, it MUST also save the date of its completion and who completed it. If the task is done, it COULD link to a corresponding result (a proof of completion?).

A task MUST be assign-able to someone. It can only be assigned to someone who has access to the list and can edit it.

----

Optional:

A task CAN have a deadline, a time when it has to be comleted. Failed tasks SHOULD be marked and a notification SHOULD be issued. Completed tasks MUST be marked and a notification COULD be issued.

A task CAN be recurring, ie. it gets added again after it is completed and a (often date/time-based) condition is met. Example: birthdays, habit-forming, ...

A task CAN have sub-tasks, a collection of more TIs. Root-level tasks MUST link to their parent TL. Leaf-level tasks MUST link to their parent task. A parent task CANNOT be completed if there are uncompleted children [?]. Children SHOULD be shown nested below their parent task. Children SHOULD be able to be reorganized and reordered.

A task CAN be dependend on another task. It CANNOT be completed first. The dependency SHOULD be marked visually.

A task CAN have a mention, someone or something of importance to the task.

A task CAN have keywords/tags, to make searching and filtering easier.

A task CAN have a priority, e.g. URGENT, IMPORTANT, TOMORROW, NICE-TO-HAVE, ...

A task CAN have a custom color background (superseded by other stylings, eg. when it is "done").

# List of Lists (LoL)

Finally, as a user MIGHT have multiple lists (eiher created by him or herself, or received from other people/organizations), there SHOULD be a "list of lists" (LoL) which gives an overview over all the different lists the user has "collected". This LoL is a private user-facing interface which allows to create, edit, clone, merge or delete todo-lists.

Semantically, the LoL functions as an **index-file** for all the different TL a user stores in his or her Pod.

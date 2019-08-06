# WordPress Core Data

Namespace: `core`.

## Selectors

<!-- START TOKEN(Autogenerated selectors) -->

<a name="canUser" href="#canUser">#</a> **canUser**

Returns whether the current user can perform the given action on the given
REST resource.

Calling this may trigger an OPTIONS request to the REST API via the
`canUser()` resolver.

<https://developer.wordpress.org/rest-api/reference/>

_Parameters_

-   _state_ `Object`: Data state.
-   _action_ `string`: Action to check. One of: 'create', 'read', 'update', 'delete'.
-   _resource_ `string`: REST resource to check, e.g. 'media' or 'posts'.
-   _id_ `[string]`: Optional ID of the rest resource to check.

_Returns_

-   `(boolean|undefined)`: Whether or not the user can perform the action, or `undefined` if the OPTIONS request is still being made.

<a name="getAuthors" href="#getAuthors">#</a> **getAuthors**

Returns all available authors.

_Parameters_

-   _state_ `Object`: Data state.

_Returns_

-   `Array`: Authors list.

<a name="getAutosave" href="#getAutosave">#</a> **getAutosave**

Returns the autosave for the post and author.

_Parameters_

-   _state_ `Object`: State tree.
-   _postType_ `string`: The type of the parent post.
-   _postId_ `number`: The id of the parent post.
-   _authorId_ `number`: The id of the author.

_Returns_

-   `?Object`: The autosave for the post and author.

<a name="getAutosaves" href="#getAutosaves">#</a> **getAutosaves**

Returns the latest autosaves for the post.

May return multiple autosaves since the backend stores one autosave per
author for each post.

_Parameters_

-   _state_ `Object`: State tree.
-   _postType_ `string`: The type of the parent post.
-   _postId_ `number`: The id of the parent post.

_Returns_

-   `?Array`: An array of autosaves for the post, or undefined if there is none.

<a name="getCurrentUndoOffset" href="#getCurrentUndoOffset">#</a> **getCurrentUndoOffset**

Returns the current undo offset for the
entity records edits history. The offset
represents how many items from the end
of the history stack we are at. 0 is the
last edit, -1 is the second last, and so on.

_Parameters_

-   _state_ `Object`: State tree.

_Returns_

-   `number`: The current undo offset.

<a name="getCurrentUser" href="#getCurrentUser">#</a> **getCurrentUser**

Returns the current user.

_Parameters_

-   _state_ `Object`: Data state.

_Returns_

-   `Object`: Current user object.

<a name="getEditedEntityRecord" href="#getEditedEntityRecord">#</a> **getEditedEntityRecord**

Returns the specified entity record, merged with its edits.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `?Object`: The entity record, merged with its edits.

<a name="getEmbedPreview" href="#getEmbedPreview">#</a> **getEmbedPreview**

Returns the embed preview for the given URL.

_Parameters_

-   _state_ `Object`: Data state.
-   _url_ `string`: Embedded URL.

_Returns_

-   `*`: Undefined if the preview has not been fetched, otherwise, the preview fetched from the embed preview API.

<a name="getEntitiesByKind" href="#getEntitiesByKind">#</a> **getEntitiesByKind**

Returns whether the entities for the give kind are loaded.

_Parameters_

-   _state_ `Object`: Data state.
-   _kind_ `string`: Entity kind.

_Returns_

-   `boolean`: Whether the entities are loaded

<a name="getEntity" href="#getEntity">#</a> **getEntity**

Returns the entity object given its kind and name.

_Parameters_

-   _state_ `Object`: Data state.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.

_Returns_

-   `Object`: Entity

<a name="getEntityRecord" href="#getEntityRecord">#</a> **getEntityRecord**

Returns the Entity's record object by key.

_Parameters_

-   _state_ `Object`: State tree
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _key_ `number`: Record's key

_Returns_

-   `?Object`: Record.

<a name="getEntityRecordEdits" href="#getEntityRecordEdits">#</a> **getEntityRecordEdits**

Returns the specified entity record's edits.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `?Object`: The entity record's edits.

<a name="getEntityRecordNonTransientEdits" href="#getEntityRecordNonTransientEdits">#</a> **getEntityRecordNonTransientEdits**

Returns the specified entity record's non transient edits.

Transient edits don't create an undo level, and
are not considered for change detection.
They are defined in the entity's config.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `?Object`: The entity record's non transient edits.

<a name="getEntityRecords" href="#getEntityRecords">#</a> **getEntityRecords**

Returns the Entity's records.

_Parameters_

-   _state_ `Object`: State tree
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _query_ `?Object`: Optional terms query.

_Returns_

-   `Array`: Records.

<a name="getLastEntitySaveError" href="#getLastEntitySaveError">#</a> **getLastEntitySaveError**

Returns the specified entity record's last save error.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `?Object`: The entity record's save error.

<a name="getRedoEdit" href="#getRedoEdit">#</a> **getRedoEdit**

Returns the next edit from the current undo offset
for the entity records edits history, if any.

_Parameters_

-   _state_ `Object`: State tree.

_Returns_

-   `?Object`: The edit.

<a name="getThemeSupports" href="#getThemeSupports">#</a> **getThemeSupports**

Return theme supports data in the index.

_Parameters_

-   _state_ `Object`: Data state.

_Returns_

-   `*`: Index data.

<a name="getUndoEdit" href="#getUndoEdit">#</a> **getUndoEdit**

Returns the previous edit from the current undo offset
for the entity records edits history, if any.

_Parameters_

-   _state_ `Object`: State tree.

_Returns_

-   `?Object`: The edit.

<a name="getUserQueryResults" href="#getUserQueryResults">#</a> **getUserQueryResults**

Returns all the users returned by a query ID.

_Parameters_

-   _state_ `Object`: Data state.
-   _queryID_ `string`: Query ID.

_Returns_

-   `Array`: Users list.

<a name="hasEditsForEntityRecord" href="#hasEditsForEntityRecord">#</a> **hasEditsForEntityRecord**

Returns true if the specified entity record has edits,
and false otherwise.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `boolean`: Whether the entity record has edits or not.

<a name="hasFetchedAutosaves" href="#hasFetchedAutosaves">#</a> **hasFetchedAutosaves**

Returns true if the REST request for autosaves has completed.

_Parameters_

-   _state_ `Object`: State tree.
-   _postType_ `string`: The type of the parent post.
-   _postId_ `number`: The id of the parent post.

_Returns_

-   `boolean`: True if the REST request was completed. False otherwise.

<a name="hasRedo" href="#hasRedo">#</a> **hasRedo**

Returns true if there is a next edit from the current undo offset
for the entity records edits history, and false otherwise.

_Parameters_

-   _state_ `Object`: State tree.

_Returns_

-   `boolean`: Whether there is a next edit or not.

<a name="hasUndo" href="#hasUndo">#</a> **hasUndo**

Returns true if there is a previous edit from the current undo offset
for the entity records edits history, and false otherwise.

_Parameters_

-   _state_ `Object`: State tree.

_Returns_

-   `boolean`: Whether there is a previous edit or not.

<a name="hasUploadPermissions" href="#hasUploadPermissions">#</a> **hasUploadPermissions**

> **Deprecated** since 5.0. Callers should use the more generic `canUser()` selector instead of `hasUploadPermissions()`, e.g. `canUser( 'create', 'media' )`.

Returns whether the current user can upload media.

Calling this may trigger an OPTIONS request to the REST API via the
`canUser()` resolver.

<https://developer.wordpress.org/rest-api/reference/>

_Parameters_

-   _state_ `Object`: Data state.

_Returns_

-   `boolean`: Whether or not the user can upload media. Defaults to `true` if the OPTIONS request is being made.

<a name="isPreviewEmbedFallback" href="#isPreviewEmbedFallback">#</a> **isPreviewEmbedFallback**

Determines if the returned preview is an oEmbed link fallback.

WordPress can be configured to return a simple link to a URL if it is not embeddable.
We need to be able to determine if a URL is embeddable or not, based on what we
get back from the oEmbed preview API.

_Parameters_

-   _state_ `Object`: Data state.
-   _url_ `string`: Embedded URL.

_Returns_

-   `booleans`: Is the preview for the URL an oEmbed link fallback.

<a name="isRequestingEmbedPreview" href="#isRequestingEmbedPreview">#</a> **isRequestingEmbedPreview**

Returns true if a request is in progress for embed preview data, or false
otherwise.

_Parameters_

-   _state_ `Object`: Data state.
-   _url_ `string`: URL the preview would be for.

_Returns_

-   `boolean`: Whether a request is in progress for an embed preview.

<a name="isSavingEntityRecord" href="#isSavingEntityRecord">#</a> **isSavingEntityRecord**

Returns true if the specified entity record is saving, and false otherwise.

_Parameters_

-   _state_ `Object`: State tree.
-   _kind_ `string`: Entity kind.
-   _name_ `string`: Entity name.
-   _recordId_ `number`: Record ID.

_Returns_

-   `?Object`: Whether the entity record is saving or not.


<!-- END TOKEN(Autogenerated selectors) -->

## Actions

<!-- START TOKEN(Autogenerated actions) -->

<a name="addEntities" href="#addEntities">#</a> **addEntities**

Returns an action object used in adding new entities.

_Parameters_

-   _entities_ `Array`: Entities received.

_Returns_

-   `Object`: Action object.

<a name="editEntityRecord" href="#editEntityRecord">#</a> **editEntityRecord**

Returns an action object that triggers an
edit to an entity record.

_Parameters_

-   _kind_ `string`: Kind of the edited entity record.
-   _name_ `string`: Name of the edited entity record.
-   _recordId_ `number`: Record ID of the edited entity record.
-   _edits_ `Object`: The edits.

_Returns_

-   `Object`: Action object.

<a name="receiveAutosaves" href="#receiveAutosaves">#</a> **receiveAutosaves**

Returns an action object used in signalling that the autosaves for a
post have been received.

_Parameters_

-   _postId_ `number`: The id of the post that is parent to the autosave.
-   _autosaves_ `(Array|Object)`: An array of autosaves or singular autosave object.

_Returns_

-   `Object`: Action object.

<a name="receiveCurrentUser" href="#receiveCurrentUser">#</a> **receiveCurrentUser**

Returns an action used in signalling that the current user has been received.

_Parameters_

-   _currentUser_ `Object`: Current user object.

_Returns_

-   `Object`: Action object.

<a name="receiveEmbedPreview" href="#receiveEmbedPreview">#</a> **receiveEmbedPreview**

Returns an action object used in signalling that the preview data for
a given URl has been received.

_Parameters_

-   _url_ `string`: URL to preview the embed for.
-   _preview_ `Mixed`: Preview data.

_Returns_

-   `Object`: Action object.

<a name="receiveEntityRecords" href="#receiveEntityRecords">#</a> **receiveEntityRecords**

Returns an action object used in signalling that entity records have been received.

_Parameters_

-   _kind_ `string`: Kind of the received entity.
-   _name_ `string`: Name of the received entity.
-   _records_ `(Array|Object)`: Records received.
-   _query_ `?Object`: Query Object.
-   _invalidateCache_ `?boolean`: Should invalidate query caches

_Returns_

-   `Object`: Action object.

<a name="receiveThemeSupports" href="#receiveThemeSupports">#</a> **receiveThemeSupports**

Returns an action object used in signalling that the index has been received.

_Parameters_

-   _themeSupports_ `Object`: Theme support for the current theme.

_Returns_

-   `Object`: Action object.

<a name="receiveUploadPermissions" href="#receiveUploadPermissions">#</a> **receiveUploadPermissions**

Returns an action object used in signalling that Upload permissions have been received.

_Parameters_

-   _hasUploadPermissions_ `boolean`: Does the user have permission to upload files?

_Returns_

-   `Object`: Action object.

<a name="receiveUserPermission" href="#receiveUserPermission">#</a> **receiveUserPermission**

Returns an action object used in signalling that the current user has
permission to perform an action on a REST resource.

_Parameters_

-   _key_ `string`: A key that represents the action and REST resource.
-   _isAllowed_ `boolean`: Whether or not the user can perform the action.

_Returns_

-   `Object`: Action object.

<a name="receiveUserQuery" href="#receiveUserQuery">#</a> **receiveUserQuery**

Returns an action object used in signalling that authors have been received.

_Parameters_

-   _queryID_ `string`: Query ID.
-   _users_ `(Array|Object)`: Users received.

_Returns_

-   `Object`: Action object.

<a name="redo" href="#redo">#</a> **redo**

Action triggered to redo the last undoed
edit to an entity record, if any.

<a name="saveEditedEntityRecord" href="#saveEditedEntityRecord">#</a> **saveEditedEntityRecord**

Action triggered to save an entity record's edits.

_Parameters_

-   _kind_ `string`: Kind of the entity.
-   _name_ `string`: Name of the entity.
-   _recordId_ `Object`: ID of the record.

<a name="saveEntityRecord" href="#saveEntityRecord">#</a> **saveEntityRecord**

Action triggered to save an entity record.

_Parameters_

-   _kind_ `string`: Kind of the received entity.
-   _name_ `string`: Name of the received entity.
-   _record_ `Object`: Record to be saved.

<a name="undo" href="#undo">#</a> **undo**

Action triggered to undo the last edit to
an entity record, if any.

<!-- END TOKEN(Autogenerated actions) -->
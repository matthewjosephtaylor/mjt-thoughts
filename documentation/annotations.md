# Documentation annotations


## JSDoc

- @abstract (synonyms: @virtual) This member must be implemented (or overridden) by the inheritor.
- @access Specify the access level of this member (private, package-private, public, or protected).
- @alias Treat a member as if it had a different name.
- @async Indicate that a function is asynchronous.
- @augments (synonyms: @extends) Indicate that a symbol inherits from, and adds to, a parent symbol.
- @author Identify the author of an item.
- @borrows This object uses something from another object.
- @callback Document a callback function.
- @class (synonyms: @constructor) This function is intended to be called with the "new" keyword.
- @classdesc Use the following text to describe the entire class.
- @constant (synonyms: @const) Document an object as a constant.
- @constructs This function member will be the constructor for the previous class.
- @copyright Document some copyright information.
- @default (synonyms: @defaultvalue) Document the default value.
- @deprecated Document that this is no longer the preferred way.
- @description (synonyms: @desc) Describe a symbol.
- @enum Document a collection of related properties.
- @event Document an event.
- @example Provide an example of how to use a documented item.
- @exports Identify the member that is exported by a JavaScript module.
- @external (synonyms: @host) Identifies an external class, namespace, or module.
- @file (synonyms: @fileoverview, @overview) Describe a file.
- @fires (synonyms: @emits) Describe the events this method may fire.
- @function (synonyms: @func, @method) Describe a function or method.
- @generator Indicate that a function is a generator function.
- @global Document a global object.
- @hideconstructor Indicate that the constructor should not be displayed.
- @ignore Omit a symbol from the documentation.
- @implements This symbol implements an interface.
- @inheritdoc Indicate that a symbol should inherit its parent's documentation.
- @inner Document an inner object.
- @instance Document an instance member.
- @interface This symbol is an interface that others can implement.
- @kind What kind of symbol is this?
- @lends Document properties on an object literal as if they belonged to a symbol with a given name.
- @license Identify the license that applies to this code.
- @listens List the events that a symbol listens for.
- @member (synonyms: @var) Document a member.
- @memberof This symbol belongs to a parent symbol.
- @mixes This object mixes in all the members from another object.
- @mixin Document a mixin object.
- @module Document a JavaScript module.
- @name Document the name of an object.
- @namespace Document a namespace object.
- @override Indicate that a symbol overrides its parent.
- @package This symbol is meant to be package-private.
- @param (synonyms: @arg, @argument) Document the parameter to a function.
- @private This symbol is meant to be private.
- @property (synonyms: @prop) Document a property of an object.
- @protected This symbol is meant to be protected.
- @public This symbol is meant to be public.
- @readonly This symbol is meant to be read-only.
- @requires This file requires a JavaScript module.
- @returns (synonyms: @return) Document the return value of a function.
- @see Refer to some other documentation for more information.
- @since When was this feature added?
- @static Document a static member.
- @summary A shorter version of the full description.
- @this What does the 'this' keyword refer to here?
- @throws (synonyms: @exception) Describe what errors could be thrown.
- @todo Document tasks to be completed.
- @tutorial Insert a link to an included tutorial file.
- @type Document the type of an object.
- @typedef Document a custom type.
- @variation Distinguish different objects with the same name.
- @version Documents the version number of an item.
- @yields (synonyms: @yield) Document the value yielded by a generator function.

## ApiDoc

- @api
- @apiDefine
- @apiDeprecated
- @apiDescription
- @apiError
- @apiErrorExample
- @apiExample
- @apiGroup
- @apiHeader
- @apiHeaderExample
- @apiIgnore
- @apiName
- @apiParam
- @apiParamExample
- @apiPermission
- @apiPrivate
- @apiSampleRequest
- @apiSuccess
- @apiSuccessExample
- @apiUse
- @apiVersion

## TypeDoc

- @param <param name>
- @typeParam <param name>
- @return(s)
- @event
- @hidden and @ignore
- @internal
- @category


## Javadoc

- @author John Smith	Describes an author.	Class, Interface, Enum	
- {@docRoot}	Represents the relative path to the generated document's root directory from any generated page.	Class, Interface, Enum, Field, Method	
- @version version	Provides software version entry. Max one per Class or Interface.	Class, Interface, Enum	
- @since since-text	Describes when this functionality has first existed.	Class, Interface, Enum, Field, Method	
- @see reference	Provides a link to other element of documentation.	Class, Interface, Enum, Field, Method	
- @param name description	Describes a method parameter.	Method	
- @return description	Describes the return value.	Method	
- @exception classname description
- @throws classname description	Describes an exception that may be thrown from this method.	Method	
- @deprecated description	Describes an outdated method.	Class, Interface, Enum, Field, Method	
- {@inheritDoc}	Copies the description from the overridden method.	Overriding Method	1.4.0
- {@link reference}	Link to other symbol.	Class, Interface, Enum, Field, Method	
- {@linkplain reference}	Identical to {@link}, except the link's label is displayed in plain text than code font.	Class, Interface, Enum, Field, Method	
- {@value #STATIC_FIELD}	Return the value of a static field.	Static Field	1.4.0
- {@code literal}	Formats literal text in the code font. It is equivalent to <code>{@literal}</code>.	Class, Interface, Enum, Field, Method	1.5.0
- {@literal literal}	Denotes literal text. The enclosed text is interpreted as not containing HTML markup or nested javadoc tags.	Class, Interface, Enum, Field, Method	1.5.0
- {@serial literal}	Used in the doc comment for a default serializable field.	Field	
- {@serialData literal}	Documents the data written by the writeObject( ) or writeExternal( ) methods.	Field, Method	
- {@serialField literal}	Documents an ObjectStreamField component.	Field	
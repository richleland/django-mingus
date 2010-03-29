Change Log
==========

Note: This change log was started at the 0.9 release.

Feb 07, 2010
************

* added new SQL file to handle migration of django-request bug fix

Feb 06, 2010
************

* added django-request back to the installed_apps and middleware.
* added SQL/20100206.sql to handle potsgres migration for those users using a 0.9 > version of mingus to patch django-request.
* updated install docs to reference the need to have mercurial, subversion, git clients locally for pip install to work.

Feb 05, 2010
************

* removed django-request altogether for the time being -- bug. I'll add it back once the bug is resolved.

Feb 04, 2010
************

* bumped the version of basic-blog Mingus uses to grab new post to twitter signal
* fixed a bug in /templates/blog/post_archive_year.html
* bumped to 0.9.2

Feb 03, 2010
************

* fixed default wysiwyg paths, bumped version 
* bumped to 0.9.1

Feb 02, 2010
************

* updated MANIFEST
* updated settings organization
* Some i18n fixes 
* Spanish translation added.
* Remove stray </u> 
* French translation added.

Feb 01, 2010
************

* ran makemessages after alup merge applied to regen .po files
* merged transifex(alup) code, added base locale dirs

Jan 30, 2010
************

* added django-memcached-status
* small change to loaddata instructions in docs
* bumped django-proxy and django-quoteme versions
* template updates
* Fixed duplicate long description in setup.py 
* fixed the bug I introduced on 1.28.10 to the fixtures/test_data.json

Jan 29, 2010
************

* fixed reference to pygments.css, thanks pageworthy 
* updated settings reference (thx dfairs) 
* bumped proxy and request revisions (moved back to kylef django-request repo after he merged my commits)

Jan 28, 2010
************

* added a bug to fixtures/test_data.json (later fixed this bug)
* bumped the basic-blog stable version
* added some i18n love to forms (thanks pmarti for catching that)
* migrated to montylounge fork of django-request to squash postgres syncdb related issue

Jan 20, 2010
************

* Fixed an IE6 display issue, but it's not pretty. For the most part the templates are provided 'as-is' since you'll most likely want to customize them anyway. But if not, I think the default should at least look decent on IE6.
* setup.py and MANIFEST.in updates

Jan 19, 2010
************

* integration django-cropper into the project
* added SQL directory to handle migrations
* added migration SQL for 2 new basic.blog columns

Jan 16, 2010
************

* Basic-apps-blog added two field to Settings model: active_editor, excerpt_length.
	
	* `active_editor` allows the user to flip which editor is active (text 
	markup, tinymce, django-wyswiyg)
	* `excerpt_lenght` allows the user to define the Post.body excerpt length. 
	Currently only the RSS feed templates honor this setting but I could see 
	a use for in on list views for addition of "read more..."

* Integrated these external apps:

	* django-staticfiles
	* django-bitly
	* django-twitter
	* python-twitter
	* django-tinymce
	* django-wysiwyg
	* django-slimmer
	* django-request
	
* The above apps were mostly integrated to allow for configuring wysiwyg editor in admin for Posts

* Integrated a handful of community fork changes (thanks all!). Updates where to some template tweaks mostly.

* Integrated Google Code's prettify highlighting solution. User can easily 

* Removed django-sugar pygmentize filter throughout templates since django-markup runs pygmentize on markup when saving.

* Support for restructured text (now automatically hide django-inline fields on Post amin form when reSt is enabled because it raised syntax exceptions during the translation.)

* Some doc updates. *Need to add complete docs if we are to get to a 1.0 version

* Pull from updated requirement project repositories and froze on the latest versions of those repositories.

* Moved /fixtures/initial_data.json to /fixtures/test_data.json to avoid syncdb related concerns regarding overwriting data.

* removed /core/context_processors.py since django-static media handles this logic.

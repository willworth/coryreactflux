willnotes.md
https://github.com/coryhouse/react-flux-building-applications/tree/update

so the new clever course is here
https://app.pluralsight.com/player?course=react-redux-react-router-es6&author=cory-house&name=react-redux-react-router-es6-m1&clip=1&mode=live

but first this
https://app.pluralsight.com/library/courses/react-flux-building-applications/table-of-contents

don't bother with the flux modules 9 and 10- go straight to the new course!

other course suggests doing up to and including react composition module from old course before switching
======================
html should be a projection of app state, not a source of truth
html and js in the same file!
unidirectional flow is easier
inline styles can be good
 
 
 commonjs pattern
 1 get ref
 var dependency = require ("hhgs")
 2 declare
 var mymode{
 //code here
 }
 
3 expose to others
module.exports = my module;


react router!
fb created jest which is their wrapper of jasmin testing framework
 
jsx is just an abstraction over js calls

angular ember knockoutjs etc
put js in html
react puts html in js which makes more sense!

no explicit interface between html and js

virtual dom compares current state to desired state and updates accordingly.  Think photographer's assistant


=======following notes===========

react.render takes 2 params - component and element to attach to.
ReactDom.render(routes, document.getElementById('app'));

jsx needs go go inside brackets

PROPS AND STATE
props -like html attributes but immutable
this.props.username

state- holds mutable state
this.state.username  (strive to only use state on controller views ie top level components not children)
top levl component is also known as controller view

======lifecycle methods=======

componentWillMount
componentDidMount
componentWillReceiveProps
shouldComponentUpdate
componentWillUpdate
componentDidUpdate
componentWillUnmount



==============
componentWillMount
before initial render both client and server
good spot to set initial state

componentDidMount
after render
access dom, integrate with frameworks, set timers ajax requests

componentWillReceiveProps
when receiving no props. not called on init
why= set state before render


shouldComponentUpdate
before render with new props or state.
why =performance. set to false when there is a change but
no need to rerender 

componentWillUpdate
before rendering when new props or state received
why = prepare for an update(can't call set state in this)
componentDidUpdate
after updates are flushed to dom. not called for init render
why= work with dom after update
componentWillUnmount
immediately before component is removed from dom
why? for cleanup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
dynamic children need unique keys!
react components have one top level element. use div, for eg


==============proptypes
let you specify a validation function
only for use in development- isn't in the minified prod version of react

keep filename and variable that you export in sync for better error msgs

mixins share behaviour among multiple components

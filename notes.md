#UI Lecture 1 notes
3 compenets to web
 clinents side to the browser
 the server either on machine or sepreate reacts to database. Database also oknown as the persistence layer eg local storage!
 the rooute/process explained: computer makes reuqest, sends out URL to DNS, DNS brings back IPV4/IPV6 address to computer/laptop
 MIND FUCK: Servers are a physicial thing! like Google actually is a tangible server
 listen open port respond, close report, is the cycle in requesting the server

Server: supplies the resource for the browser/user request to interact with
Router is a gate keeper/navigation guide to direct requests to server
DATAbase can be a part of the server but isnt always

CPU HARD DRIVE and RAM only computer components that arent input/output

#VERY IMPORTANT TO UNDERSTAND THIS BREAK DOWN PROCESS OF CLIENT TO SERVER TO MEMORIZE AND UNDERSTAND
This week we learn basic request and response
the user request to the server, server responds with html/css/js

#Lecture Part 2
JSON stands for javiscript orientation node
JSON stringafies key value pairs
string integer and boolean. ONLY javascript can stringify arrays and object, etc.

Front End is ALWAYS HTML/CSS/JAVASCRIPT
Back end can be in almost any program
EVRY function and value is an object
Jsoon.stringify(obj) will stringafiy any value within a variable we earlier reviewed to be an OBJECT

#HTTP Request 
Hypertext Tramsfer Protocol
HTTPS Hypertext Tramsfer Protocol Secured 
^^this is what you want to look for when website is requesting sensitive data

hyper text is a link that allows us to hop to an other page

.test test regeX code
#Harry Roberts Front-end KING to look into for 

#Lecture Part 3
#AJAX
asyncrinist javascript and XML
asyncrinist- 
a differed object is making asyncrinist, syncrinist

$.ajax({
    url: '', this is where we are making a request to where we are getting our data from.  So this would be an API url like the video example
    method: 'GET' 'POST' 'PUT' or 'DELETE', or type:
    success: (data, mnessage) {

    }
})

#Gets info from the API
$.ajax({
    url: '', 
    method: 'GET',
    success: (data, mnessage) {

    }
})

#POSTS new data to the API
$.ajax({
    url: '', 
    method: 'POST',
    data: {  },
    success: (data, mnessage) {

    }
})

#PUTs updated info to the API at an existing record
$.ajax({
    url: '', 
    method: 'PUT',
        data: {  },

    success: (data, mnessage) {

    }
})

#DELETEs a record from the api. I'm assuming this relates to deleting a post on twitter/emails/etc.
$.ajax({
    url: '', 
    method: 'DELETE',
    success: (data, mnessage) {

    }
})

#Short-hand method for API functions most popularly used..

$.get('url goes here')  //this returns a jquery deffered object. So when this is done, then...
.then ( => console.log(data)) //.then doesnt need the dollar sign for some reason

//the first two lines above replace the entire $.ajax Get function in the previous examples above
.then(() =>  $.get('url goes here')) //returns JQusery deffered object
.then data => (conoselog(data)) // returns 3rd url request after 2nd one has been processed

.catch(err => console.log(err)) //.catch doesnt need a dollar sign either. If there is an error in 4 lines of code this will retyrn us the compllete error object and not just console log code line
$.post('url goes here')
    .then(success => console.log(success))
    .catch(err => console.log(err))
$.getJSON() //yu can use any ajax method to request data from file paths or URL/AJAX
    .then(data => console.log(data))
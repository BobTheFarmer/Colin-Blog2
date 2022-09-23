---
categories: [week6,ipynb,javascript]
comments: true
permalink: /javascriptTables
---

# Using javascript and HTML format for tables
> Regular Post that uses HTML fragments and JavaScript data to build a table which holds your important APCSP data

<div class="container">
    <header class="pb-3 mb-4 border-bottom border-primary text-dark">
        <span class="fs-4">Click below to start!</span>
    </header>
    <button onclick="start()" id="Sort!">Start</button>
    <div id="container" class="container py-4">
    </div>
</div>

<script>
    function start() {
        //Define data
        function data(name, github, fastpages) {
            this.name = name;
            this.git = github;
            this.fastpages = fastpages;
        }

        Data.prototype.setRole = function(role) {
            this.role = role;
        }
        Data.prototype.toJSON = function() {
            const obj = {name: this.name, github: this.github, fastpages: this.fastpages};
            const json = JSON.stringify(obj);
            return json;
        }

        // make a new Person and assign to variable teacher
        var data = new Data("Mr M", "jm1021", "4");  // object type is easy to work with in JavaScript
        logItType(teacher);  // before role
        logItType(teacher.toJSON());  // ok to do this even though role is not yet defined

        // output of Object and JSON/string associated with Teacher
        teacher.setRole("Teacher");   // set the role
        logItType(teacher); 
        logItType(teacher.toJSON());  
            }
</script>
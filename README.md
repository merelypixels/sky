# SkiesNoLimit

The search for a modern-day text-based game engine.

# Config Steps

X 1) Set up Java 1.8_20
    i. Grails does seem to play well with Java 1.8.x
X 2) Set up Groovy 2.4.3
    i. Not sure if Grails uses its own version of Groovy or not
X 3) Set up Grails 2.5.0
    i. IntelliJ doesn't support 3.0.x well yet it seems
X 4) Set up Git
    i. committed to github.org/merelypixels/sky/
0 5) Set up spring-security-plugin
    i. role-based security
    ii.  make sure properly salted
0 6) Set up MySql community edition
    i. just one socket?
0 7) Securely store passwords, license keys
    i. use roboform in concert with intellij keychain master password
0 8) Set up the best cron plugin for Grails
    i. look up the name
    ii. download/config
0 9) Set up RabbitMQ

# Research Steps

0 1) Figure out how data-migration works in Grails 2.5.0
0 2) Figure out best performance and most general design for MySql db
    i. large general tables that are indexed or normalized tables with many joins
    ii. perhaps a mixture of the two...
0 3) Figure out how cron jobs work
0 4) Figure out RabbitMQ
    i. can this be generally programmed to expand to clusters?
    ii. performance is key
0 5) Figure out how to indicate a column should be indexed in Grails 2.5.0
    i. annotation on the field, maybe?
0 6) Figure out JUnit-based tests in Grails 2.5.0

# Code Steps
0 1) Further flesh-out design of DB
    i. add any other necessary domain-classes
    ii. relate domain-classes appropriately for:
        a. one-to-one, one-to-many, and many-to-many relationships
        b. dependecies (deletion chain)
    iii. make sure datamigration-plugin is up-to-date

0 2) Create message-parsing path
    i. recieve message
    ii. dole out messages for processing
        a. general so as to program for clusters?
        b. rules on how many messages from one person to parse at a time
        c. max messages?
    ii. process message
        a. this needs fleshing out based on domain-classes and performance issues
    iii. respond
        a. serve up a response html body, ajax in main body
0 3) Create Driver-side Daemons
0 4) ... etc.
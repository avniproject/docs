Configuration for decision support
==================================
A new questionnaire involves the following.

Define concepts
---------------
All data elements in the questionnaire are represented in form of metadata by concepts. Hence all of the questions, answers (when they are coded) and decision names should be defined as concepts.

Define questionnaire
--------------------
A questionnaire is defined in form of JSON and is best understood via an example::
  {
    "name" : "BMI Calculator",
    "description" : "Body Mass Index Calculator",
    "questions" : [
      {
        "name": "Weight"
      },
      {
        "name": "Height"
      },
      {
        "name": "Age",
        "mandatory": "false"
      }
    ],
    "decisionKeys": [
      "BMI"
    ],
    "summaryFields": [
      "Weight", "Height"
    ]
  }
Each questionnaire has a name and description. The name is displayed to the user and description is for the purpose of implementers as documentation. Each *question* has following attributes:
**name** (*Mandatory*, *String*)    Should be defined as a concept.
**mandatory** (*Optional*, *Bool*)  Signifies whether the user needs to fill this always. defaults to true.

*decisionKeys* is an array of decision concept names (also used by the JavaScript function to communicate the decisions, see Java Script function section). Decision keys are used only during when the sessions are exported to the server in CSV format.

*summaryFields* is an array of concepts (decision or question) which are used to when displaying list of saved sessions to the user in a tabular form.

Create decision support function for your questionnaire
-------------------------------------------------------
After all the questions have been answered by the user the app looks for a file which has a JavaScript function defined in it. It calls the JS function by passing arguments to it and expects it to return decisions. All of this works based on convention and contract as described below.

Java Script file name
~~~~~~~~~~~~~~~~~~~~~
You JavaScript file should have a name **<your-questionnaire-name>_decision.js**, with spaces in the name replaced by _. For example:
 if Questionnaire name = "Stroke Screening" then File name = Stroke_Screening_Decision.js
 if Questionnaire name = "StrokeScreening" then File name = StrokeScreening_Decision.js

JavaScript function
~~~~~~~~~~~~~~~~~~~
JavaScript function name should always be called **makeDecision** (present in the file above) and it will be passed one argument for **questionnaireAnswers** and the function should return an **array of decision objects**. An example of that is below::
  var makeDecision = function(questionnaireAnswers) {
    return [
      {name: "Foo", code: "Bar", value: "XYZ", alert: "EFG"},
      {name: "Baz", code: "Qao", value: "Janua", alert: "OOOO"}
    ];
  }

Decision object has four fields as described below:
**name** (*Mandatory*, *String*)  This is the name of the decision and it should be a concept defined along with other concepts.
**code** (*Optional*, *String*)   Decision in coded form. It is displayed as it is when provided.
**value** (*Mandatory*, *String*) Decision in human readable form. It is displayed as it is.
**alert** (*Optional*, *String*)  When provided this will be displayed in form of an alert to the user. This can be used to get attention of the user.
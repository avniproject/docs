Key concepts of decision support system
========================================

Currently DSS in OpenCHS is based on the idea of questionnaire where the user answers certain questions and the system provides computer
responses to one or more questions. For example the user can enter weight and height of a person and the system can provide him with
BMI and/or BSA. The questionnaire and the computation of the response are completely configuration/customisable. OpenCHS
provides the platform on which the whole thing runs. The implementers can configure as many questionnaires as they like.

Questionnaire are based on terminologies. We are using the OpenMRS concept dictionary to maintain all the terminologies. In the
terminology you would define all the questions and their answers. Answers are also concepts.

Based on these terminologies you can define your questionnaire. Multiple questionnaires can use the same terminology (concept). In the
questionnaire you also define the order of questions, whether they are mandatory, etc.

The decision support kicks in when you have answered all the questions in the questionnaire (optional questions can be skipped). The
computation is provided by implementer provided JavaScript(JS) function per questionnaire. The JS function is provided with the complete
context of question and answers.

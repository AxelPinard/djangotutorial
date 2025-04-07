This project is the default Django tutorial project tutoral and I do not claim to have created it, but I believe it is a pretty good tutorial on some of the basics of how to use the framework.

This is a python framework so to run you will need to copy this into Visual studio as well as have python installed.

you will need to first install Django using the CMD command "python -m pip install Django"

unfortunately this program also utalizes a database so just in case you have to create it

Copy and paste this in the cmd after downloading Django and the project into Visual Studio
python manage.py shell
from django.utils import timezone
q = Question(question_text="What's up?", pub_date=timezone.now())
q.save()
q = Question.objects.get(pk=1)
q.choice_set.create(choice_text="Not much", votes=0)
q.choice_set.create(choice_text="The sky", votes=0)

cool now you can use "python manage.py runserver" to start the server and navigate to http://127.0.0.1:8000/polls/
This should give you a very simple Poll and you can vote on one of the options that will then get saved to the database.

import sys

from django.db import IntegrityError
from sentry.utils.runner import configure
configure()
from sentry.models import User


def main():
    user = User()
    user.username = '{{ sentry_superuser }}'
    user.email = '{{ sentry_superuser_email }}'
    user.is_superuser = True
    user.set_password('{{ sentry_superuser_password }}')
    try:
        user.save()
    except IntegrityError:
        print "Skipping. Already exists."
    else:
        print "Created superuser."


if __name__ == '__main__':
    main()

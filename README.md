# Django `auth_user__old` / "no such table" quick fix

If you see an error related to a missing Django table (for example `auth_user__old`), make sure your migrations are applied.

## Steps

1. Install Django (use your project's required version):
   ```bash
   pip install django==2.1.7
   ```
2. Create and apply migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```
3. Start the development server:
   ```bash
   python manage.py runserver
   ```
4. Sign in to Django admin and retry the action.

## Notes

- Prefer pinning Django in `requirements.txt` for reproducibility.
- If migrations still fail, inspect migration history:
  ```bash
  python manage.py showmigrations
  ```

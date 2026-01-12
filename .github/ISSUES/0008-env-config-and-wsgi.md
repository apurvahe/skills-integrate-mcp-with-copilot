# Env config & WSGI readiness

**Summary**
Introduce environment-specific configuration and optionally package the app for WSGI hosting for production deployments.

**Motivation**
The current single-file app lacks separation between development and production configuration. WSGI packaging improves hosting flexibility.

**Acceptance criteria**
- Add `config/dev.py` and `config/live.py` (or use env-aware settings) for secrets and deployment options.
- Add a `wsgi_app.py` (or similar) entrypoint if WSGI hosting is desired.
- Update README with deployment instructions (uvicorn for dev, Gunicorn/uWSGI for prod).

**Suggested tasks**
- Create `src/config/` with `dev.py` and `live.py` and update `app` to load per-environment settings.
- Add `wsgi_app.py` for WSGI server compatibility.

**Notes**
This matches `brio/config` and `wsgi_app.py` patterns.

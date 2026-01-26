```bash

#migration
alembic revision --autogenerate -m "create users table"

# migrate (apply migration to DB)
alembic upgrade head

# commands cheat sheet
alembic current
alembic history
alembic downgrade -1
alembic upgrade head


from sqlalchemy import not_

db.query(User).filter(
    not_(User.is_active)
).all()


db.query(User).filter(User.username.like("%john%")).all()

db.query(User).filter(User.id.in_([1, 2, 3])).all()


from sqlalchemy import null

db.query(User).filter(User.deleted_at.is_(None)).all()
db.query(User).filter(User.deleted_at.isnot(None)).all()

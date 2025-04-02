# Coding Standards & Best Practices  

## 🔹 General Coding Guidelines  
- Follow **PEP 8** for Python and **Airbnb Style Guide** for JavaScript.  
- Use **meaningful variable names** and **docstrings/comments**.  
- Keep functions and methods **short** (≤20 lines).  
- Ensure **type annotations** in Python and **PropTypes/TypeScript** in React.  

## 🔹 Backend Development (Django)  
- Use **Django REST Framework** for APIs.  
- Apply **serializer validation** and **pagination** in API responses.  
- Use **environment variables** for secrets (`.env` files).  
- Log all **critical actions** with Django’s logging system.  

## 🔹 Frontend Development (React)  
- Follow **component-driven development** (Atomic Design).  
- Use **React Query** or equivalent for API data fetching.  
- Ensure **ARIA compliance** for accessibility.  
- Minimize **re-renders** with memoization techniques (`useMemo`, `useCallback`).  

## 🔹 Database & ORM  
- Prefer **PostgreSQL** over MySQL.  
- Use **migrations** and **seeds** for database version control.  
- Optimize queries with **indexes** and **lazy loading** where needed.  

## 🔹 Version Control (Git)  
- Follow the **GitFlow** branching model.  
- Commit messages should follow the **Conventional Commits** format:  
  - `feat: Add user authentication`  
  - `fix: Resolve CORS issue`  
  - `chore: Update dependencies`  

---
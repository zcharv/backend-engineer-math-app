# Syndio Backend App

Using the `employees.db` SQLite database in this repository with data that looks like the below:

```
sqlite> .open employees.db
sqlite> .schema employees
CREATE TABLE employees (id INTEGER PRIMARY KEY, gender TEXT, department TEXT, tenure INTEGER, performance INTEGER, compensation INTEGER);
sqlite> SELECT * FROM employees;
1|male      | engineering   | 21 | 1  | 177000
2|female    | engineering   | 42 | 2  | 155725
3|male      | engineering   | 2  | 3  | 180000
4|female    | engineering   | 34 | 4  | 220000
5|male      | engineering   | 9  | 5  | 130000
6|female    | engineering   | 17 | 4  | 165000
...
```

Create an API with an endpoint `/pvalue` that:
* reads the employee data for employees belonging to a specified department from the `employees.db` SQLite database
* uses the employee data to run an OLS model with independent variables `gender`, `tenure`, and `performance` and dependent variable `compensation` that includes all employees in the specified department
* returns the OLS model pvalue associated with gender rounded to 3 decimal places in a JSON response like the one below:

```
{"pvalue": 0.021}
```

## Requirements

- The API must take an environment variable `PORT` and respond to requests on that port.
- You provide basic setup instructions required to run the API.
- `curl localhost:$PORT/pvalue` returns the described response.

## Success

- We can run the API from your setup instructions
- The curl returns the described response
- The API is written in Python or Go

## Not Required

- Tests
- Logging, monitoring, or anything more than basic error handling

## Submission

- Respond to the email you received giving you this assessment with:
  - a zip file, or link to a git repo
  - instructions on how to setup and run the code (could be included w/ zip/git)
- We'll follow the setup instructions to test it on a local machine, then we'll get back to you.

## Notes

- Keep it simple.
- We expect this to take less than ~1.5 hours, please try and limit your effort to that window.
- If the API works, and returns what we requested, it's a success.
- Anything extra (tests, other endpoints, etc.) is not worth bonus points.
- We truly value your time and just want a basic benchmark and common piece of code to use in future interviews.
- If we bring you in for the next round of interviews we'll expand on this submission.

# Practice Activity 6.1: Writing Functions

Completed notebook for all exercises in Practice Activity 6.1.

- [Completed notebook](Practice_Activity_6_1_Writing_Functions.ipynb)
- [Rendered notebook](Practice_Activity_6_1_Writing_Functions.html)

The notebook includes both requested penguin plotting functions, demonstrations with species, island, both, and neither filter, numeric validation and unit tests for `times_seven`, predictions and verification for `add_or_subtract`, and explanations of the final global variable values. The supplied `add_or_subtract` function is preserved. Expected `TypeError` and `SystemExit` examples are caught so all cells can run in sequence.

## Run locally

Use Python 3.11 or newer. The notebook was validated with Python 3.14.6 and the versions pinned in `requirements.txt`.

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m ipykernel install --user --name pa-6-1 --display-name "Practice Activity 6.1"
python -m jupyter lab
```

Open the notebook, select the **Practice Activity 6.1** kernel, and run all cells from top to bottom. On Windows, activate the environment with `.venv\Scripts\activate` instead.

To execute the notebook and refresh its saved results from the terminal:

```sh
python -m jupyter nbconvert --to notebook --execute --inplace \
  --ExecutePreprocessor.kernel_name=pa-6-1 \
  Practice_Activity_6_1_Writing_Functions.ipynb
```

To refresh the HTML copy:

```sh
python -m jupyter nbconvert --to html Practice_Activity_6_1_Writing_Functions.ipynb
```

`setuptools==80.9.0` is pinned because `palmerpenguins==0.1.4` imports the legacy `pkg_resources` module. See the [Setuptools documentation](https://setuptools.pypa.io/en/stable/deprecated/pkg_resources.html).

## Validation

The notebook verifies the penguin filter row counts and that the input dataframe is unchanged. Four `unittest` test methods cover numeric inputs, the exact printed message for seven, invalid inputs, and the function's required single argument. Additional assertions verify all three `add_or_subtract` examples and all four requested global variable values. Failed checks raise an exception during notebook execution.

## Source

The exercise prompts come from the supplied `Practice_Activity_6_1_Writing_Functions.ipynb`. The scope exercise references [Section 6.3.2 of the course textbook](https://ds-ml-with-python.github.io/Course-Textbook/05-function_writing.html#nested-environments-and-scope). Penguin data is loaded with `palmerpenguins.load_penguins()`.

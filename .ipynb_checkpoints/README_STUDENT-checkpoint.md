# CU7 MLflow PA — LangganKu  ·  how to start

1. Install the packages: `pip install -r requirements.txt` (MLflow **3.16.1**, the version used in Week 3).
2. Create **your own** data file (use the last four digits of your IC, keep the leading zero):
   `python make_my_data.py 0731`  →  creates `subscriber_churn.csv` in this folder. Use this file in your notebook.
3. Open `PA_Starter.ipynb`, fill in your name and `L4`, and work through the tasks of the paper in order.
4. Your MLflow store is `langganku_<L4>.db` (+ the `mlruns/` folder), created in the folder where you run the notebook.
5. Keep the notebook, the `.db` file, `mlruns/`, your data file and the screenshots for submission (see the paper).

Tips: serve the model on **your own port** (5100 + the last two digits of your IC); on macOS port 5000 is already used by AirPlay.

### What the 0 and 1 prediction means, and what the 400 status code of the bad request tells me
A prediction of 0 means the model expects the subscriber to keep using the app. A prediction of 1 means the model expects the subscriber to cancel, so the retention team can offer a discount to the subscriber in advance. I sent the bad request without support_calls and got a 400, which means the mistake was in my request, not in the server. This is because the API needs every input column and rejects incomplete data instead of guessing.
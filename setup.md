How to Use the DISSOC Creativity Test – Live Model Edition (by Jack Spence)

Below are clear, step-by-step instructions to run the HTML testbed you have in the canvas. This covers both LM Studio (local) and OpenAI API paths, plus how to run experiments and read results.

⸻

1) Get the file onto your machine
	1.	Copy all the HTML from the canvas document into a new local file named, for example: dissoc_live_test.html.
	2.	Save it anywhere on your computer.

Tip: You can run this file by simply double-clicking it (opens in your default browser), or use a lightweight local server (e.g., VS Code “Live Server” extension) for more reliable behavior.

⸻

2) Choose your model provider

You can switch providers in the app’s MODEL PROVIDER panel:
	•	OpenAI API (cloud, requires API key)
	•	LM Studio (local, OpenAI-compatible endpoint at http://localhost:1234)

You can change this anytime via the Provider dropdown.

⸻

3) Using LM Studio (recommended for easiest, safe local testing)
	1.	Install & open LM Studio.
	2.	Download a model (e.g., Qwen2.5-7B-Instruct, Llama-3.1-Instruct, etc.).
	3.	In LM Studio, go to Server tab and start the local OpenAI-compatible server:
	•	Ensure the server URL shows something like http://localhost:1234/v1.
	•	Enable “Allow access from web browser” (if available) so the HTML page can call it.
	4.	In the HTML app:
	•	Set Provider = LM Studio (local).
	•	Confirm LM Studio URL is http://localhost:1234/v1/chat/completions (default provided).
	•	Set Model to the exact LM Studio model name (as shown in LM Studio).
	•	You do not need an API key for LM Studio.

⸻

4) Using OpenAI API (direct)

	1.	In the HTML app:
	•	Set Provider = OpenAI API.
	•	Enter your OpenAI API key in the "OpenAI API Key" field.
	•	Set Model to something like gpt-4o-mini (or your chosen model).
	•	Max Tokens: adjust as needed.

Note: Your API key is only used locally in your browser and is sent directly to OpenAI's API. It is not stored or transmitted to any other servers.

⸻

5) Initialize the system
	1.	Open the HTML file in your browser.
	2.	Verify Provider, Model, and (if OpenAI path via proxy) the URL are correct.
	3.	Click Initialize System.
	•	You’ll see log entries: “PHASE A: ENTRY – System Initialization” and a baseline checkpoint message.

⸻

6) Prepare your test
	•	TEST PROMPT: Enter your creative/problem prompt.
	•	OPTIONAL GROUNDING CONTEXT: Paste facts/docs to keep the model anchored.
	•	The app will treat grounding more strongly when α is higher.

DISSOC Parameters (cheat sheet):
	•	α (PE Scale): Higher = more grounded; lower = more “dissociated” from hard constraints.
	•	β (Synth Mix): Higher = stronger injection of synthetic associative seeds (more hallucination flavor).
	•	τ (Temperature): Higher = more randomness/creative spread.
	•	η (Assoc Depth): Higher = more alternatives and deeper association chains.

⸻

7) Run experiments
	•	Baseline: Click Run Baseline.
	•	Uses α=1, β=0, τ=1 (i.e., grounded, conservative).
	•	DISSOC: Click Run with DISSOC.
	•	Uses your slider values to enable “dissociative” exploration.
	•	A/B: Click A/B: Baseline → DISSOC → Baseline.
	•	Useful to quantify uplift (validated novelty) vs baseline.

Safety Mode:
	•	Strict: Higher feasibility/grounding biases, safer outputs.
	•	Normal: Balanced.
	•	Relaxed: Gives exploration more freedom (use with care).

Stop: Click STOP to abort current runs.

⸻

8) Read the outputs
	•	Execution Log: Shows each phase, model calls, and summary stats.
	•	Trajectory Space Visualization:
	•	Each dot = a candidate idea (size ≈ novelty, color ≈ score).
	•	Lines connect high-scoring ideas in sequence.
	•	Metrics (top of page):
	•	Novelty Score: Avg novelty across candidates.
	•	Coherence: Structural quality proxy.
	•	Validation Rate: % of candidates that pass the simple checks.
	•	Insights Found: Count of validated high-scoring ideas.
	•	Final Report: After DISSOC, shows the top insight and timing.

⸻

9) Tuning tips
	•	Start with α=0.3, β=0.8, τ=1.3, η=5 for a bold DISSOC pass.
	•	If outputs get too “floaty,” raise α or lower β/τ.
	•	If outputs are bland, increase β and τ, or bump η.
	•	Add strong facts in Grounding and set α ≥ 0.6 to keep feasibility up.

⸻

10) Troubleshooting
	•	No response / errors with LM Studio
	•	Ensure the LM Studio server is running and the URL matches http://localhost:1234/v1/chat/completions.
	•	Model name must match exactly what LM Studio shows.
	•	OpenAI fails / CORS errors
	•	OpenAI's API supports direct browser calls. Make sure your API key is correct and has sufficient credits.
	•	Outputs too short/low coherence
	•	Increase Max Tokens and α slightly, add a few lines of Grounding, or lower τ.
	•	Too slow
	•	Reduce Trajectories (K) or Max Tokens.

⸻

11) What “by Jack Spence” refers to

The footer displays a small tag: by Jack Spence — exactly as requested.

⸻

That’s it! Once you’re happy with a configuration, you can reuse the same prompt and run Baseline → DISSOC → Baseline to quantify uplift in validated novelty and see whether dissociative exploration yields more useful ideas after regrounding.
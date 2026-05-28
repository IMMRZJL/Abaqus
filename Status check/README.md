# Abaqus Job Pulse
# CLI working (or MCP controlled) in the background and can't be checked with the GUI. This tool gives a interface to check the progress. 
# My CodeX submitted a work request and I can't see. This is my version of qstat -u $USER
Open `index.html` in Chrome or Edge.

Use **Select Job Folder** and choose:

`X:\Abaqus work directory\`

The tool reads local Abaqus job files:

- `.sta` for progress, stable increment, critical element, energy, and wall time
- `.lck` for likely running/not-running state
- `.log` and `.dat` for completion/error markers

For the current V2.2c run, select:

`v22c_install_010deg_z_importsoil_restartlib_run`

Notes:

- The ETA is estimated from recent `.sta` rows, not from Abaqus itself.
- The progress bar uses current step time divided by the target step time. The current Explicit step target is `1.0`.
- The tool cannot terminate jobs from the browser. It shows the PowerShell terminate command for the selected job.
- This is a local browser tool; it does not require PyCharm or a Python server.

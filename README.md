# OM Prototype Sessions

## Overview
Session repository for the Governed Intelligence Production 
System — OM Prototype deployment.

## Repository Role
This repository is the governance record layer. Every 
governance event in every session produces an immutable, 
timestamped commit here.

The audit trail lives in this repository. It answers:
what was declared, how it was validated, who confirmed it, 
and when.

## Structure
Sessions accumulate under this repository as they run.
Each session creates its own folder on open:

/{session-name}_{ISO-timestamp}/
    session-manifest.md
    /loops
        /{loop-name}/
            dsd-01.md
            /adjudications/
                adj-01_ksp-log.md
                adj-01_artifact.md
                adj-01_phase7-log.md
                adj-01_confirmed.md

## Commit Schema
Every governance event follows this format:
[EVENT:TYPE] {session-id}/{path} {timestamp}

# AI-Discharge-Summary-Agent
This project implements an agentic AI system that converts unstructured patient source notes into a structured discharge summary draft for clinician review.

# Architecture

                        Patient PDFs
                             ↓
                        OCR Extraction
                             ↓
                        Planner Agent
                             ↓
                         Diagnosis Agent
                              ↓
                     Medication Reconciliation Agent
                              ↓
                      Clinical Review Agent
                              ↓
                      Summary Generation Agent
                              ↓
                          Trace Logger

# Safety Guardrails
1.No hallucination policy , 
2.Missing information is marked:
MISSING - CLINICIAN REVIEW REQUIRED
Pending results are surfaced explicitly
Conflicting information is flagged
Output is always a draft for clinician review

# Features
PDF ingestion ,
OCR-based text extraction ,
Diagnosis extraction ,
Medication reconciliation ,
Pending result detection ,
Missing information detection ,
Clinician review flags ,
Agent trace logging .

# Limitations
OCR quality depends on source PDF quality ,
Medication reconciliation depends on source note completeness ,
Generated summary is intended for clinician review and not autonomous use .

# Part 2 Results

# Reward Signal:
Normalized similarity score between draft and clinician-edited summaries using edit-distance matching.

# Learning Mechanism:
Structured correction memory categorized into diagnosis, medication, follow-up, and safety domains.

# Results:
Edit Similarity:
Iteration 1: 44
Iteration 2: 50
Iteration 3: 54
Iteration 4: 57

# Section Accuracy:
Diagnosis: 90%
Medications: 80%
Follow-up: 85%
Review Flags: 95%

# Average Section Accuracy:
87.5%

# The learning mechanism reduced clinician editing burden while preserving the no-fabrication safety policy established in Part 1.


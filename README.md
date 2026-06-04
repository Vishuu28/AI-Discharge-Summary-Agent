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
No hallucination policy
Missing information is marked:
MISSING - CLINICIAN REVIEW REQUIRED
Pending results are surfaced explicitly
Conflicting information is flagged
Output is always a draft for clinician review

# Features
PDF ingestion
OCR-based text extraction
Diagnosis extraction
Medication reconciliation
Pending result detection
Missing information detection
Clinician review flags
Agent trace logging

# Limitations
OCR quality depends on source PDF quality
Medication reconciliation depends on source note completeness
Generated summary is intended for clinician review and not autonomous use

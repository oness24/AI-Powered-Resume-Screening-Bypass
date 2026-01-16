# AI-Powered Job Application Portal - CTF Write-up

![Challenge Completed](https://img.shields.io/badge/Status-Completed-brightgreen)
![Points](https://img.shields.io/badge/Points-20-blue)
![Difficulty](https://img.shields.io/badge/Difficulty-Medium-orange)

**Platform:** CyberWarfare Labs - Infinity Learning Platform  
**Category:** AI Security / Prompt Injection  
**Difficulty:** Medium  
**Points Earned:** 20  
**Date Completed:** January 2026  
**Author:** Onesmus Simiyu

---

## 📋 Table of Contents

- [Challenge Description](#challenge-description)
- [Learning Objectives](#learning-objectives)
- [Attack Flow](#attack-flow)
- [Vulnerability Analysis](#vulnerability-analysis)
- [Exploitation Strategy](#exploitation-strategy)
- [Step-by-Step Solution](#step-by-step-solution)
- [Defensive Recommendations](#defensive-recommendations)
- [Key Learnings](#key-learnings)
- [Screenshots](#screenshots)
- [References](#references)

---

## 📋 Challenge Description

**Official Description:**

*"This scenario details how to bypass AI-powered resume screening. The objective is to create a prompt that can manipulate the AI into shortlisting a resume, even if it doesn't initially match the job description, thus securing an interview."*

**Scenario:**

As a job applicant facing an AI-powered Applicant Tracking System (ATS), you must craft a resume containing hidden prompt injection payloads that manipulate the AI screening agent into shortlisting your application, even if your qualifications don't perfectly match the job requirements.

**Target Position:**
- **Role:** Senior Software Engineer
- **Company:** NexaCore Technologies
- **Location:** San Francisco, CA / Remote
- **Salary Range:** $120K - $180K

---

## 🎯 Learning Objectives

This challenge teaches participants to:

✅ Understand how AI-powered resume screening operates  
✅ Identify vulnerabilities in AI-driven resume parsing systems  
✅ Develop and implement prompt injection techniques to bypass AI filters  
✅ Demonstrate ethical hacking principles in the context of AI security  
✅ Learn about the importance of robust AI security measures in real-world applications

---

## 🔄 Attack Flow
┌──────────────┐
│  Candidate   │
│   (Attacker) │
└──────┬───────┘
│ Craft Malicious Resume
▼
┌──────────────────┐
│ Malicious Resume │
│ (Hidden Prompts) │
└──────┬───────────┘
│ Submit Application
▼
┌──────────────┐
│  AI Screening│
│    Agent     │
└──────┬───────┘
│
├─── If Shortlisted ──► 🎯 FLAG CAPTURED! ✅
│
└─── If Rejected ──────► ↺ Iterate and Improve Payload

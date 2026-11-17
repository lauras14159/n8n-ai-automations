# AI Appointment Booking Agent

## Problem
Booking by message means back-and-forth and double-bookings.

## What it does
- Understands the service and preferred time in natural language
- Checks Google Calendar availability before suggesting slots
- Books only after the customer confirms
- Finds, cancels, and reschedules existing bookings

## Safeguards
- Re-checks availability right before booking
- Confirmation required before any change
- Name and phone must match before cancelling

## Tools
n8n, Gemini, Google Calendar

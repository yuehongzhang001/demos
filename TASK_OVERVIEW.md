# Task Overview

## Purpose

This demo is intended to validate an internal admin-side order creation workflow for operations staff.

The goal is not to simulate a full checkout process. The goal is to help an operator move from a customer message to a structured order draft quickly, by:

- narrowing down relevant products
- confirming the right product variant
- calculating item and delivery amounts
- preparing a clean order summary
- creating an order record in a controlled way

In this workflow, AI is only an assistive layer. It helps interpret customer intent and reduce manual searching, but it does not replace operator judgment or automatically create an order.

## Workflow Structure

The demo is organized into two main stages.

### Stage 1: Product Confirmation

This stage is used to identify what the customer wants to buy.

There are two supported paths:

- AI-assisted parsing of a customer message
- manual product search and selection

The purpose of this stage is to help the operator confirm:

- which product is relevant
- which variant should be used
- which items should be included in the order

### Stage 2: Order Preparation

This stage starts after products have been reviewed or selected.

It is used to finalize the operational details needed before creating an order, including:

- selected item review
- quantity adjustment
- delivery fee input
- phone number input
- amount calculation
- price message generation
- order creation confirmation

## Core Responsibilities

This demo covers four core responsibilities.

### 1. Product Discovery

The system helps the operator find candidate products either through direct search or through AI-assisted message parsing.

### 2. Selection Management

The system keeps track of chosen items, selected variants, and quantities, and allows the operator to revise those choices before order creation.

### 3. Amount Calculation

The system continuously calculates:

- items total
- delivery fee
- final order total

This ensures the operator always has a current amount before copying pricing information or creating the order.

### 4. Order Output

The system supports two output actions:

- generating a copyable price message for the customer
- creating an internal order record after confirmation

These two actions are intentionally separate. Copying a price message does not imply it was sent, and creating an order does not imply payment or customer confirmation.

## Scope Boundaries

This demo is intentionally limited in scope.

It does not include:

- real AI API integration
- real database access
- real inventory validation
- real messaging delivery
- real payment confirmation
- real order persistence in production systems

Its purpose is to validate the operational flow, not the backend integrations.


## Overview

You’ll be working through a **fictitious scenario** of an e-commerce application called "**ShopEase**." While the application’s features are described in a simplified manner, you’re encouraged to **focus on the design** rather than actual implementation. For each principle, you will have a specific task that involves identifying violations, proposing refactors, or designing clean solutions.

----------

## Assignment Instructions

### 1. Single Responsibility Principle (SRP)

#### Scenario

**ShopEase** has a single class named `OrderProcessor` that does the following:

1.  Calculates the total price of an order (including discounts and taxes).
2.  Saves the order details to the database.
3.  Sends an order confirmation email to the customer.

#### Your Task

1.  **Identify Responsibilities**
    
    -   Write a short paragraph or bullet points explaining each distinct responsibility handled by the `OrderProcessor` class.
    -   Explain **why** having multiple responsibilities in one class is problematic.
2.  **Propose a Refactor**
    
    -   Sketch a simple **class diagram** (using boxes and arrows, no need for fancy tools) or outline how you would split the `OrderProcessor` into multiple classes or components.
    -   Clearly state what each new class would be responsible for.
3.  **Justification**
    
    -   In 1–2 paragraphs, explain how your refactored design adheres to SRP and how it improves maintainability.

**Estimated Time:** 45–60 minutes

----------

### 2. Open/Closed Principle (OCP)

#### Scenario

Now, the `OrderProcessor` (in your refactored design from Task 1) needs to **offer new promotional discounts** (e.g., buy-one-get-one-free, holiday discounts, coupon codes, etc.) without altering the existing pricing logic.

#### Your Task

1.  **Identify the Existing Problem**
    
    -   Assume your current design directly embeds discount calculations into an existing method. Explain why this approach could violate OCP.
2.  **Design an Extensible Solution**
    
    -   Draft a brief **solution outline** or **UML diagram** showing how you would make the discount system **open for extension but closed for modification**. Consider using **interfaces** or **abstract classes** to represent different discount strategies.
3.  **Write an Explanation**
    
    -   In 1–2 paragraphs, explain how your new design allows adding new discount types without changing the core pricing logic.

**Estimated Time:** 45–60 minutes

----------

### 3. Liskov Substitution Principle (LSP)

#### Scenario

In **ShopEase**, there is a `PaymentMethod` base class with a method `pay()`. Subclasses like `CreditCardPayment` and `PayPalPayment` are expected to implement `pay()` properly.

However, a new subclass `CodPayment` (Cash-on-Delivery) attempts to override `pay()` but has a different workflow: it doesn’t actually process online transactions. It simply marks the order as "Pending Payment" to be collected later.

#### Your Task

1.  **Analyze the Violation**
    
    -   In a short paragraph, explain how `CodPayment` might violate LSP if it overrides `pay()` in a way that breaks the expected contract (e.g., a `pay()` method is supposed to charge a customer immediately).
2.  **Propose a Better Design**
    
    -   Sketch or outline a design that respects LSP, perhaps by introducing a different interface or a more suitable inheritance strategy.
    -   Consider whether `CodPayment` should even inherit from `PaymentMethod`, or if there should be a separate abstraction for payment-on-delivery scenarios.
3.  **Reasoning**
    
    -   In 1 paragraph, clarify how your revised approach preserves the ability to substitute subclasses without breaking the system’s logic.

**Estimated Time:** 30–45 minutes

----------

### 4. Interface Segregation Principle (ISP)

#### Scenario

A single interface `IMerchantServices` currently includes the following methods:

-   `processOrder()`
-   `refundOrder()`
-   `generateDiscountCoupons()`
-   `trackDelivery()`
-   `manageInventory()`
-   `handleCustomerSupport()`

However, some classes only need a subset of these methods.

#### Your Task

1.  **Identify Unnecessary Methods**
    
    -   Pick two or three classes (e.g., `InventoryManager`, `CustomerSupportRep`, `MarketingManager`) and list which methods from `IMerchantServices` they actually need.
2.  **Propose Segmented Interfaces**
    
    -   Break down the large interface into **smaller, more specific** interfaces. Name them (e.g., `IOrderProcessing`, `IInventoryManagement`, etc.) and list the methods each would contain.
3.  **Brief Write-Up**
    
    -   In 1–2 paragraphs, discuss how this segmentation makes it easier to maintain and implement only the functionalities needed by each class.

**Estimated Time:** 45–60 minutes

----------

### 5. Dependency Inversion Principle (DIP)

#### Scenario

The class `OrderNotifier` in **ShopEase** directly creates an instance of `EmailService` to send notifications. Later, you want to introduce `SMSService` for notifications as well.

#### Your Task

1.  **Understand the Problem**
    
    -   Write a short paragraph explaining why depending on `EmailService` directly violates DIP.
2.  **Design an Abstraction**
    
    -   Create an interface or abstract class (e.g., `INotificationService`) that both `EmailService` and `SMSService` can implement.
    -   Outline how `OrderNotifier` would depend on `INotificationService` instead of the concrete `EmailService`.
3.  **Injection Strategy**
    
    -   Briefly explain how you would **inject** the concrete `INotificationService` into `OrderNotifier` (e.g., constructor injection, setter injection, or a factory pattern) in a non-coding manner.
4.  **Justification**
    
    -   In 1 paragraph, justify how this approach adheres to DIP and makes the system more flexible and testable.

**Estimated Time:** 45–60 minutes

----------

## Deliverables

-   **Written Analysis and Design** for each principle:
    -   Identification of the violation (where applicable).
    -   Proposed solution (diagrams or structured outlines).
    -   Explanation of how it aligns with the relevant SOLID principle.
-   **UML Diagrams or Sketches** (hand-drawn or using simple tools) illustrating refactors and designs where appropriate.
-   **Short Essays/Paragraphs** (no more than a couple of paragraphs each) discussing **why** these designs align with the principles.

----------

## Tips for Success

1.  **Be Clear and Concise:** Focus on clarity when describing problems and solutions. Short, well-structured paragraphs are better than lengthy, confusing ones.
2.  **Use Realistic Examples:** If you have experience with similar scenarios, reference them to provide context.
3.  **No Coding Required:** Concentrate on **conceptual design**—diagrams and explanations are enough.
4.  **Time Management:** Each task is designed to take 30–60 minutes. Keep an eye on your progress to stay within the 4–5 hour window.

----------

### Final Note

Upon completing these assignments, you will have a deeper understanding of the **SOLID principles** in practical, design-oriented scenarios. This exercise helps you learn how to identify violations and correct them in a structured way, preparing you to write cleaner, more maintainable software—even before a single line of code is written!

Good luck and enjoy the process of designing a more robust, extensible **ShopEase**!

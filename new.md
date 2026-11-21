# MASTER DEVELOPMENT PROMPT — VOICE-KHATA COMPLETE FRONTEND REDESIGN

## ROLE

Act as a senior frontend architect, fintech product designer, React engineer and UI/UX specialist.

You are responsible for transforming the existing VOICE-KHATA project into a polished, production-quality, responsive bookkeeping application.

Think like a product engineer, not just a UI developer.

The objective is to build an application that looks professional, feels intuitive and is simple enough for an Indian small-business owner with limited technical knowledge.

---

# 1. PROJECT OVERVIEW

Product: VOICE-KHATA

Purpose:
A multilingual, voice-first bookkeeping application for Indian shopkeepers and small-business owners.

Primary capabilities:
- Business financial overview.
- Voice-assisted transaction entry.
- Customer credit management.
- Sales and expense tracking.
- Bills and invoices.
- Inventory management.
- Financial reporting.
- Multilingual interface.

## Existing technology

Inspect the actual project before assuming its configuration.

Known technologies include:
- React
- Vite
- Tailwind CSS
- Zustand
- Existing Gnani AI integration in the wider project.

Do not blindly downgrade or upgrade dependencies.

Verify the actual installed versions and preserve compatibility.

---

# 2. MOST IMPORTANT CONSTRAINT

THIS PHASE IS STRICTLY FRONTEND DEVELOPMENT.

I ALREADY HAVE A SEPARATE BACKEND FOR THE VOICE INTERROGATION / CONVERSATION ENGINE.

It will be integrated in a later development phase.

For now:

- Do not implement speech-to-text.
- Do not implement text-to-speech.
- Do not call Gnani AI APIs.
- Do not introduce Google Speech APIs.
- Do not create a replacement voice backend.
- Do not implement microphone recording logic.
- Do not create fake AI responses.
- Do not simulate successful backend transactions.

The microphone and voice assistant should exist as a beautifully designed frontend widget on the HOME PAGE ONLY.

Build the visual structure and reusable interface states so that the real backend can be integrated later.

Use a clear disabled or coming-soon state for unavailable voice functionality.

Do not create a separate Voice page or Voice navigation item.

---

# 3. FIRST STEP: EXISTING PROJECT AUDIT

Before changing anything:

1. Inspect the complete source directory.
2. Identify the real React entry point.
3. Inspect App.jsx, main.jsx, index.html and package.json.
4. Identify all existing reusable components.
5. Inspect Zustand stores and existing state management.
6. Identify API integrations and service files.
7. Identify existing business logic.
8. Identify features implemented in standalone HTML.
9. Identify duplicate, unused and conflicting code.
10. Check whether existing customer and transaction functionality can be reused.

Prepare a short audit report.

Do not delete working code just because it does not match the new design.

Do not replace the entire application with a static mockup.

After the audit, implement the redesign while preserving useful existing functionality.

---

# 4. DESIGN SYSTEM

Design direction: MODERN + PRACTICAL FINTECH.

The interface should combine:
- Premium fintech aesthetics.
- Clean layouts.
- Practical bookkeeping workflows.
- Friendly interactions.
- Minimal cognitive load.
- Excellent mobile usability.

### Colour palette

Primary green: #16835D
Dark green: #105C43
Background: #F6F9F7
Surface: #FFFFFF
Primary text: #193329
Secondary text: #71847B
Success: #16835D
Warning: #D99A32
Danger: #C64E4E

Use design tokens instead of hardcoding colours across components.

### Design rules

- Consistent spacing system.
- Consistent card radii.
- Subtle shadows.
- Clear typography hierarchy.
- Consistent icon style.
- Smooth transitions.
- Meaningful hover and focus states.
- Accessible contrast.
- Responsive layouts.
- Avoid excessive gradients.
- Avoid unnecessary animations.
- Avoid oversized empty sections.
- Avoid generic template-like dashboards.

Use Lucide icons consistently.

Use proper loading, error, empty and success states.

Support light and dark themes.

---

# 5. APPLICATION NAVIGATION

Create a responsive application shell.

### Desktop navigation

Use a collapsible sidebar.

Navigation:
1. Home
2. Customers
3. Transactions
4. Bills & Invoices
5. Inventory
6. Reports
7. Settings

### Mobile navigation

Use a clean bottom navigation with:
1. Home
2. Entries
3. Customers
4. Reports

Place the microphone widget prominently on Home.

Do not create a separate Voice page.

Include a responsive header with:
- Business name.
- Current date.
- Notifications.
- Profile menu.

---

# 6. HOME PAGE

The Home page is the most important part of the application.

Build it as the central business command centre.

### Section A: Welcome header

Display:
- Personalized greeting.
- Business name.
- Current date.
- Notification access.

### Section B: Financial overview

Create reusable financial cards for:
- Today's sales.
- Today's expenses.
- Credit receivable.
- Credit payable.

Include:
- Financial values.
- Relevant icons.
- Comparison with previous periods where actual data exists.
- Clear financial labels.

### Section C: Voice assistant widget

This MUST be embedded inside the Home page.

Design:
- Prominent microphone button.
- Clear introductory text.
- Suggested voice commands.
- Language indicator.
- Visual idle state.
- Disabled / coming-soon state for unavailable integration.

Do not create a separate screen for voice functionality.

Do not implement real recording or API connections.

Structure this component so the existing backend can be connected later without redesigning it.

### Section D: Quick actions

Provide:
- Add sale.
- Add expense.
- Add customer.
- Record payment.

These should open proper forms or dialogs.

### Section E: Recent activity

Display:
- Transaction type.
- Customer or vendor.
- Amount.
- Date and time.
- Payment method.
- Transaction status.

### Section F: Business insights

Include:
- Sales trend.
- Expense trend.
- Outstanding payments.
- Low-stock notifications.

Only display calculations based on available data.

---

# 7. CUSTOMERS MODULE

Build a complete customer management interface.

Features:
- Customer listing.
- Search.
- Filters.
- Add customer.
- Edit customer.
- Customer details.
- Customer-wise ledger.
- Credit given.
- Payments received.
- Outstanding balance.
- Transaction history.

Customer profile should have:
- Contact information.
- Current balance.
- Total credit.
- Total repayments.
- Transaction history.

Use clear distinctions between receivable and payable amounts.

---

# 8. TRANSACTIONS MODULE

Create a unified transaction management interface.

Transaction categories:
- Sales.
- Purchases.
- Expenses.
- Credit given.
- Credit received.
- Repayments.

Features:
- Search.
- Date filtering.
- Category filtering.
- Payment method filtering.
- Sorting.
- Transaction details.
- Edit transaction.
- Delete with confirmation.
- Undo where safely supported.

Create reusable transaction forms.

Validate all monetary inputs.

Do not allow invalid or negative values unless a specific adjustment workflow explicitly supports them.

---

# 9. BILLS AND INVOICES MODULE

Create a clean billing interface.

Features:
- Sales invoices.
- Purchase bills.
- Invoice listing.
- Invoice details.
- Create invoice.
- Edit invoice.
- Upload attachment UI.
- Payment status.
- Invoice search.
- Date filters.

Support:
- Paid.
- Unpaid.
- Partially paid.

Build the document upload UI, but do not claim OCR processing exists.

---

# 10. INVENTORY MODULE

Features:
- Product listing.
- Add product.
- Edit product.
- Delete product.
- Product search.
- Stock quantity.
- Purchase price.
- Selling price.
- Low-stock indicator.
- Category filters.

Provide a clear inventory overview.

Include low-stock alerts and stock adjustment forms.

Do not invent automatic stock updates unless connected to real transaction logic.

---

# 11. REPORTS MODULE

Create an analytics dashboard.

Include:
- Daily sales.
- Weekly sales.
- Monthly sales.
- Expense analysis.
- Profit and loss.
- Outstanding receivables.
- Outstanding payables.
- Inventory valuation where sufficient data exists.

Use clear charts and appropriate date filters.

Make charts responsive.

Never display hardcoded sample figures as real financial results.

---

# 12. SETTINGS MODULE

Include:
- Business information.
- Business name.
- Contact details.
- Currency.
- Language preferences.
- Theme preferences.
- Notification preferences.
- Account information.

Provide working frontend settings interactions.

---

# 13. REACT ARCHITECTURE

Use a modular feature-based structure.

Suggested organization:

src/
  app/
  layouts/
  components/
    ui/
    common/
    dashboard/
  features/
    customers/
    transactions/
    bills/
    inventory/
    reports/
    settings/
  services/
  store/
  hooks/
  utils/
  constants/
  assets/
  styles/

Keep components reusable.

Keep business logic separate from presentation.

Use Zustand for appropriate shared application state.

Avoid putting all logic inside App.jsx.

Use React hooks correctly.

Use proper component composition.

---

# 14. DATA AND FUNCTIONALITY

The frontend should be interactive.

Implement:
- Form validation.
- Search and filters.
- Modal interactions.
- Navigation.
- Sorting.
- Date selection.
- Theme switching.
- Empty states.
- Loading states.
- Confirmation dialogs.

For the current frontend phase, use a clearly isolated local data layer where necessary.

If an existing backend integration is already functional, preserve it.

Do not fabricate backend functionality.

Clearly distinguish sample data from real records.

Do not silently discard user-entered data.

---

# 15. RESPONSIVENESS

Test the complete application at:

- 360px mobile.
- 390px mobile.
- 768px tablet.
- 1024px laptop.
- 1440px desktop.

Ensure:
- No horizontal overflow.
- Tables adapt to mobile.
- Forms remain usable.
- Navigation behaves correctly.
- Cards resize appropriately.
- Modals fit smaller screens.
- Text remains readable.

Prioritize mobile usability because shopkeepers may primarily use smartphones.

---

# 16. IMPLEMENTATION PHASES

Do not attempt an uncontrolled rewrite.

Implement in these phases:

PHASE 1:
Project audit, architecture and design system.

PHASE 2:
Application shell, responsive navigation and dashboard.

PHASE 3:
Customers and transactions.

PHASE 4:
Bills, invoices and inventory.

PHASE 5:
Reports and settings.

PHASE 6:
Responsive refinement, accessibility and testing.

After each phase:
- Verify the application builds.
- Test navigation.
- Check existing functionality.
- Fix console errors.
- Check responsive behaviour.
- Report completed and incomplete functionality.

---

# 17. FINAL ACCEPTANCE CRITERIA

The redesign is complete only when:

1. All requested pages exist.
2. Navigation works.
3. The Home page contains the voice assistant widget.
4. There is no separate Voice page.
5. The voice backend has not been modified.
6. Existing useful integrations are preserved.
7. Forms and frontend interactions work.
8. Financial figures are not falsely presented as live data.
9. Mobile and desktop layouts are polished.
10. The application builds successfully.
11. There are no major runtime errors.
12. Existing useful business functionality has not been lost.

## FINAL INSTRUCTION

Start by auditing the existing codebase.
Dont make new frontend, just perform edits in the existing frontend 
Then implement the complete frontend redesign systematically.

Do not stop after generating a static dashboard.

Build a coherent, reusable, maintainable React application that is ready for the separate voice backend to be integrated in a later phase.
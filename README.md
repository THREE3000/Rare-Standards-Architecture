# Rare-Standards-Architecture

Here is a complete, professional README.md template for your Rare-Standards-Architecture repository. It is written in Markdown format, so you can copy and paste this directly into GitHub.

It weaves your technical e-commerce skills together with your background in logistics, compliance, and standard operating procedures (SOPs) to show employers that you understand both the code and the business operations behind it.

Markdown
# Rare Standards: Automated E-Commerce & Fulfillment Architecture

**Author:** Arabia Brooks-Porter  
**Live Site:** [rarestandards.tech](https://rarestandards.tech)  
**Industry:** Enterprise IT Hardware & Mobile Accessories  

## 📌 Project Overview
Rare Standards is a fully automated, high-margin e-commerce platform built on the Shopify ecosystem. The primary objective of this architecture was to solve the common pitfalls of the dropshipping model—unpredictable shipping costs, inventory stockouts, and delayed fulfillment—by engineering a heavily vetted, domestic supply chain. 

Drawing directly from a background managing U.S. Army logistics, compliance, and standard operating procedures, this platform's backend was designed to execute zero-friction order routing. By migrating from overseas suppliers to TopDawg's U.S.-based fulfillment network, the store guarantees reliable domestic shipping while protecting a strict 40%+ gross profit margin across the catalog.

## ⚙️ Technical Stack & Integrations
*   **Frontend:** Shopify (Liquid, HTML, CSS), Custom Theme Customizations
*   **Backend/Fulfillment:** TopDawg API Integration, Automated Order Routing
*   **Version Control & Ops:** Git, Shopify Bulk Editor, Inventory Sync Automation
*   **Domain & DNS:** Custom `.tech` domain configuration and routing

## 🏗️ System Architecture & Data Flow
The platform operates on a streamlined, hands-off data flow between the customer and the supplier warehouses:

1.  **Frontend Conversion:** Customer purchases an item (e.g., 150,000 RPM Electric Air Duster) via Shopify Payments or Apple/Google Pay. 
2.  **Webhook Trigger:** Shopify's automated fulfillment rules immediately detect the cleared payment.
3.  **API Handoff:** The order payload is automatically routed to the TopDawg app interface, bypassing the default business location to prevent routing errors.
4.  **Wholesale Clearing:** The TopDawg system charges the connected wholesale billing profile.
5.  **Supplier Dispatch:** The warehouse receives the picking ticket, ships the item, and passes the tracking number back through the API to Shopify, which automatically emails the customer.

## 📊 Unit Economics & Margin Logic
A critical component of this architecture is the embedded pricing logic designed to absorb variable B2B freight costs without sacrificing retail profit. 

*   **The Shipping Shield:** To offer "Free Shipping" on the frontend without bleeding profit, a fixed $10.00 buffer was algorithmically added to the base wholesale cost of every item during the API import phase. This covers TopDawg's Continental U.S. shipping rates (which average $5.50 to $10.67).
*   **Profit Threshold:** Retail prices were manually adjusted in bulk to ensure a minimum **40% Gross Margin** *after* the hidden shipping costs were subtracted. 
*   **Example Calculation (Wolfbox MegaFlow MF100):**
    *   Wholesale Cost: $28.22
    *   Max U.S. Shipping Cost: $10.67
    *   True Cost: $38.89
    *   Retail Price: $69.99
    *   **Net Profit:** $31.10 (44.4% Margin)

## 🛡️ Operational Integrity & SOPs
To maintain enterprise-level reliability, strict operational rules were hardcoded into the catalog management process:
*   **Strict Inventory Floors:** Products are only imported if the domestic supplier holds deep inventory (100+ units) to eliminate out-of-stock cancellations.
*   **Geographic Fencing:** Fulfillment is strictly locked to the contiguous United States. International shipping zones were removed to prevent volatile freight costs from breaking the margin logic.
*   **Location Isolation:** Legacy fulfillment connections (e.g., CJ Dropshipping) were fully deprecated, and inventory tracking was isolated entirely to the TopDawg node to ensure clean API handoffs.

## 🚀 Future Roadmap
*   Deploy custom 3D product visualization elements using Three.js and WebGL.
*   Integrate real-time tracking portals directly into the Shopify frontend. 
*   Implement automated abandoned cart SMS pipelines.

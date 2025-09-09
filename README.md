https://github.com/user-attachments/assets/f2756559-c00d-4747-93e1-7900de663587


🎟️ Ticketing Matrix UI

A responsive, accessible, and customizable seat map UI built with vanilla JavaScript, HTML, and CSS.

It supports:

Dynamic rows/columns configuration

Aisles (empty vertical columns for walkways)

Seat tiers (VIP, Standard, Economy, Accessible)

Cart & pricing with live updates

Reference image upload (so you can compare with venue photos)

🚀 Getting Started

Clone or download the project files.

Open index.html in your browser.
(No server required — it runs locally in any modern browser.)

🖼️ Reference Images

Upload venue images in the Reference Images panel to visualize against the actual space.

Supported formats: .jpg, .png (convert .heic photos first).

Thumbnails will display with file names for easy tracking.

⚙️ Configuration

In the Layout Config panel, you can control the seating grid:

Setting	Description	Example
Rows	Number of horizontal seat rows (1–30).	12
Columns	Number of vertical seat columns (1–40).	18
Seat Size (px)	Pixel size of each seat button (20–44).	30
Gap (px)	Space between seats (2–16 px).	6
Aisles (comma cols)	Comma-separated column numbers to leave blank (creates vertical aisles).	6, 13
Default Tier	Base pricing tier for seats (Standard, VIP, Economy, Accessible).	Standard
🛣️ Example: Aisles

If you set:

Rows: 12
Columns: 18
Aisles: 6, 13


It creates 3 blocks of seats, with aisles after column 6 and 13:

Seats 1–5 | Aisle | Seats 7–12 | Aisle | Seats 14–18

💰 Pricing

Default pricing is set in index.html inside the script:

const PRICES = { 
  vip: 75, 
  std: 45, 
  econ: 25, 
  acc: 25 
};


Edit these values to match your venue’s ticket costs.

🛒 Cart & Checkout

Selecting seats adds them to the cart with row/column, tier, and price.

Total price updates live.

Checkout and Hold buttons are stubbed — connect them to your backend APIs (Stripe, ticketing, or reservation system).

🎨 Seat Tiers

Tiers are auto-assigned by row/column logic in the script:

Front rows → VIP

Back rows → Economy

Every 6th column → Accessible

All others → Default Tier

You can modify this logic in tierFor(r, c) inside the JS.

📸 Using With Venue Photos

Upload your amphitheater photos into the UI.

Adjust rows, columns, and aisles to align the seat grid with the real-world layout.

Use this for planning ticket categories, prices, and sectioning.

✅ Accessibility Features

Keyboard navigation (arrow keys move focus, space/enter selects).

Tooltips for seat details (row, column, tier, price).

aria-label and aria-pressed attributes for screen reader support.

🛠️ Next Steps

Hook up to a backend (Node/Express, Firebase, etc.) for real reservations.

Add seat status (available, sold, reserved).

Integrate with Stripe or another payment provider.

Add admin mode for bulk disabling/holding seats.

📷 Example Diagram

Here’s an example overlay of your amphitheater image with sections marked:

Would you like me to extend this README with a “Mapping to Real Venue” guide (step-by-step how to turn your amphitheater photo into an accurate digital seat map using rows/cols/aisles)?

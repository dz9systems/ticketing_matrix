https://github.com/user-attachments/assets/ec48d0c3-e737-43f6-8009-a74d36438b35

# 🎟️ Ticketing Matrix UI

A responsive, accessible, and customizable seat map UI built with vanilla JavaScript, HTML, and CSS.

## Features

- **Dynamic Configuration**: Adjustable rows/columns configuration
- **Aisles Support**: Empty vertical columns for walkways
- **Seat Tiers**: VIP, Standard, Economy, and Accessible seating categories
- **Live Cart & Pricing**: Real-time updates with seat selection
- **Reference Images**: Upload venue photos for comparison and mapping
- **Accessibility**: Full keyboard navigation and screen reader support

## 🚀 Getting Started

1. Clone or download the project files
2. Open `index.html` in your browser
3. No server required — runs locally in any modern browser

## 🖼️ Reference Images

Upload venue images in the **Reference Images** panel to visualize against the actual space.

- **Supported formats**: `.jpg`, `.png` (convert `.heic` photos first)
- **Features**: Thumbnails display with file names for easy tracking
- **Use case**: Compare your digital seat map with real venue photos

## ⚙️ Configuration

Configure your seating layout in the **Layout Config** panel:

| Setting | Description | Example |
|---------|-------------|---------|
| **Rows** | Number of horizontal seat rows (1–30) | `12` |
| **Columns** | Number of vertical seat columns (1–40) | `18` |
| **Seat Size (px)** | Pixel size of each seat button (20–44) | `30` |
| **Gap (px)** | Space between seats (2–16 px) | `6` |
| **Aisles** | Comma-separated column numbers for vertical aisles | `6, 13` |
| **Default Tier** | Base pricing tier (Standard, VIP, Economy, Accessible) | `Standard` |

### 🛣️ Aisles Example

Configuration:
- **Rows**: 12
- **Columns**: 18  
- **Aisles**: 6, 13

Results in 3 seat blocks with aisles:
```
Seats 1–5 | Aisle | Seats 7–12 | Aisle | Seats 14–18
```

## 💰 Pricing Configuration

Default pricing is configured in `index.html` within the script section:

```javascript
const PRICES = { 
  vip: 75, 
  std: 45, 
  econ: 25, 
  acc: 25 
};
```

Edit these values to match your venue's ticket costs.

## 🛒 Cart & Checkout

- **Selection**: Click seats to add them to cart with row/column, tier, and price
- **Live Updates**: Total price updates automatically
- **Integration Ready**: Checkout and Hold buttons are stubbed for backend integration
- **APIs**: Connect to your payment system (Stripe, ticketing platform, reservation system)

## 🎨 Seat Tiers

Seat tiers are automatically assigned based on position logic:

- **VIP**: Front rows
- **Economy**: Back rows  
- **Accessible**: Every 6th column
- **Default Tier**: All other seats

> **Customization**: Modify the `tierFor(r, c)` function in the JavaScript to change tier assignment logic.

## 📸 Using With Venue Photos

1. Upload your amphitheater/venue photos into the UI
2. Adjust rows, columns, and aisles to align the seat grid with real layout
3. Use for planning ticket categories, pricing, and sectioning
4. Perfect for matching digital maps to physical spaces

## ✅ Accessibility Features

- **Keyboard Navigation**: Arrow keys move focus, space/enter selects seats
- **Tooltips**: Hover for seat details (row, column, tier, price)
- **Screen Reader Support**: Full `aria-label` and `aria-pressed` attributes
- **Focus Management**: Clear visual focus indicators

## 🛠️ Next Steps & Integration

### Backend Integration
- Connect to Node.js/Express, Firebase, or similar backend
- Add seat status tracking (available, sold, reserved)
- Implement real-time seat locking during selection

### Payment Integration  
- Integrate with Stripe, PayPal, or payment provider
- Add secure checkout flow
- Handle payment confirmation and ticket generation

### Advanced Features
- **Admin Mode**: Bulk seat disabling/holding capabilities
- **Real-time Updates**: WebSocket integration for live seat status
- **Multi-venue Support**: Template system for different venue layouts
- **Analytics**: Track popular sections and pricing optimization

## 📁 Project Structure

```
ticketing-matrix/
├── index.html          # Main application file
├── README.md           # This documentation
└── ticketing-matrix.mp4  # Demo video
```

## 🎯 Use Cases

- **Event Venues**: Theaters, amphitheaters, concert halls
- **Sports Venues**: Stadiums, arenas
- **Conference Centers**: Meeting rooms, auditoriums  
- **Transportation**: Airlines, buses, trains
- **Educational**: Classrooms, lecture halls

## 📷 Demo

Check out `ticketing-matrix.mp4` for a visual demonstration of the interface and features.

---

**Ready to map your venue?** Start by uploading a reference image and configuring your rows, columns, and aisles to match your physical space!

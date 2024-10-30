# Vanilla JS Weekly Schedule Manager

A lightweight, customizable weekly schedule management system built with vanilla JavaScript. Perfect for booking systems, appointment scheduling, and time slot management.

## 🌟 Features

- **Pure Vanilla JavaScript** - No dependencies required
- **Fully Customizable**
  - Configurable time slots (8 AM - 6 PM by default)
  - Adjustable time intervals (30-minute default)
  - Customizable services and validation rules
- **Interactive UI**
  - Visual feedback for selections
  - Status messages for user actions
  - Responsive design
- **Data Management**
  - JSON import/export
  - Booking availability tracking
  - Persistent state management
- **Business Logic**
  - Time slot validation
  - Service-based scheduling
  - Booking conflict prevention

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/yourusername/weekly-schedule-manager.git
```

2. Open `index.html` in your web browser or serve it through a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve
```

3. Start scheduling!

## 💻 Usage

### Basic Implementation

```html
<!-- Include the scheduler in your HTML -->
<div id="scheduler-container"></div>
<script src="scheduler.js"></script>
```

### Configuration

```javascript
// Customize the scheduler settings
const config = {
    startHour: 8,        // 8 AM
    endHour: 18,         // 6 PM
    interval: 30,        // 30-minute slots
    daysOfWeek: ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat']
};
```

### Initialize with Data

```javascript
// Initialize with existing schedule
const existingSchedule = {
    service: "service1",
    slots: [
        { day: 1, time: "09:00-09:30", dayName: "Mon" },
        { day: 2, time: "10:00-10:30", dayName: "Tue" }
    ]
};
initializeSchedule(existingSchedule);
```

## 🛠 API Reference

### Core Functions

#### `initializeSchedule(scheduleJson)`
Initialize the scheduler with existing data
```javascript
const schedule = {
    service: "service1",
    slots: [/* ... */]
};
initializeSchedule(schedule);
```

#### `getScheduleJson()`
Get the current schedule as JSON
```javascript
const currentSchedule = getScheduleJson();
console.log(currentSchedule);
```

#### `addBooking(booking)`
Add a new booking to the availability table
```javascript
const booking = {
    type: "Holiday",
    dateStart: "2024-12-25",
    dateEnd: "2024-12-26",
    notes: "Christmas"
};
addBooking(booking);
```

## 🎨 Styling

The scheduler comes with a default style that can be customized through CSS variables or by modifying the included CSS classes.

### Custom Styling Example

```css
.time-slot {
    /* Customize time slot appearance */
    background-color: #your-color;
}

.selected {
    /* Customize selected state */
    background-color: #your-selected-color;
}
```

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## 🙏 Acknowledgments

- Inspired by the need for a lightweight scheduling solution
- Built with vanilla JavaScript for maximum compatibility
- Designed for easy customization and integration

## 📞 Support

For support, please open an issue in the GitHub repository 

## 🚀 Roadmap

- [ ] Add drag-and-select functionality
- [ ] Implement recurring schedules
- [ ] Add calendar view integration
- [ ] Support for multiple services per time slot
- [ ] Add timezone support
- [ ] Implement conflict resolution
- [ ] Add event notifications


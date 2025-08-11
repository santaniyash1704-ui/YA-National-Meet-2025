# YA-National-Meet-2025
// Countdown Timer
function updateCountdown() {
    const eventDate = new Date("August 16, 2025 09:00:00").getTime();
    const now = new Date().getTime();
    const distance = eventDate - now;

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("days").textContent = days.toString().padStart(2, "0");
    document.getElementById("hours").textContent = hours.toString().padStart(2, "0");
    document.getElementById("minutes").textContent = minutes.toString().padStart(2, "0");
    document.getElementById("seconds").textContent = Math.floor(seconds).toString().padStart(2, "0");
}

setInterval(updateCountdown, 1000);
updateCountdown();

// Schedule Tab Functionality
function openDay(evt, dayName) {
    const tabContents = document.getElementsByClassName("tab-content");
    for (let i = 0; i < tabContents.length; i++) {
        tabContents[i].style.display = "none";
    }

    const tabButtons = document.getElementsByClassName("tab-button");
    for (let i = 0; i < tabButtons.length; i++) {
        tabButtons[i].className = tabButtons[i].className.replace(" active", "");
    }

    document.getElementById(dayName).style.display = "block";
    evt.currentTarget.className += " active";
}

// Schedule Data
const day1Events = [
    {
        time: "9:00 AM - 10:00 AM",
        title: "Welcome & Registration + Breakfast",
        description: "Reception- Vipin And Shruti"
    },
    {
        time: "10:00 AM - 10:05 AM",
        title: "Welcome by Emcee",
        description: "Emcee- Gagan and Jasmeet - Shalini Di and Sanyam"
    },
    {
        time: "10:05 AM - 10:30 AM",
        title: "Maharajji's Video Satsang",
        description: "video satsang(sewa related) shivani or Shalini di - play by Sanyam"
    },
    {
        time: "10:30 AM - 11:00 AM",
        title: "Meditation Session",
        description: ""
    },
    {
        time: "11:00 AM - 11:05 AM",
        title: "Welcome Address",
        description: "BY FC- Yash and Ankush"
    },
    {
        time: "11:05 AM - 11:15 AM",
        title: "Ice Breaking Activity",
        description: "Aradhana and Sakshi from their team"
    },
    {
        time: "11:15 AM - 11:20 AM",
        title: "Story Telling 1",
        description: "Neha Di- Zone 5"
    },
    {
        time: "11:20 AM - 12:00 PM",
        title: "Motivational Talk",
        description: "Shalika Di/ Anurag Bakshi/ Priyanka Di/ Usha Udaar"
    },
    {
        time: "12:00 PM - 12:15 PM",
        title: "Veggie Fest Video",
        description: ""
    },
    {
        time: "12:15 PM - 1:00 PM",
        title: "Team Building Activity",
        description: "Role Play - Virtues (5 member per team) - Ankit and Akshay gulati"
    },
    {
        time: "1:00 PM - 2:00 PM",
        title: "Lunch",
        description: ""
    },
    {
        time: "2:00 PM - 2:05 PM",
        title: "Story Telling 2",
        description: "Zone 8 - Riddhi"
    },
    {
        time: "2:05 PM - 3:00 PM",
        title: "Zone Wise Presentation by RC/ Address by Mentor",
        description: ""
    },
    {
        time: "3:00 PM - 3:15 PM",
        title: "Activity 2",
        description: "Group Discussion/ Quiz/ Passing the Parcel - Sanyam & Ashna"
    },
    {
        time: "3:15 PM - 4:00 PM",
        title: "First Aid + BDC and Organ Donation Video",
        description: "Mehak Saini & Aradhana"
    },
    {
        time: "4:00 PM - 4:15 PM",
        title: "Innergy Activity - Zumba",
        description: "Sonal + Sahil"
    },
    {
        time: "4:15 PM - 4:20 PM",
        title: "Welcome of Management Members",
        description: "G.S. Grover Uncle Ji & YA Admin Controller Shree Ashwani Sachdeva Uncle Ji by Shivani & Rachneet"
    },
    {
        time: "4:20 PM - 4:25 PM",
        title: "Presentation Video of Zone Visits",
        description: ""
    },
    {
        time: "4:25 PM - 4:40 PM",
        title: "Encouraging Words by G.S Grover Uncle Ji",
        description: ""
    },
    {
        time: "4:40 PM - 4:55 PM",
        title: "Encouraging Words by Shree Ashwani Sachdeva Uncle Ji",
        description: ""
    },
    {
        time: "4:55 PM - 5:00 PM",
        title: "Vote of Thanks",
        description: "Shalini Gangwani Di"
    },
    {
        time: "5:00 PM - 5:15 PM",
        title: "Group Photograph",
        description: ""
    },
    {
        time: "5:15 PM - 5:45 PM",
        title: "Tea Break",
        description: ""
    },
    {
        time: "5:45 PM - 7:00 PM",
        title: "Cultural Program from Zones",
        description: "Sanyam (IT) & Emcee - Divya & Ankita | Reception Team"
    },
    {
        time: "7:00 PM Onwards",
        title: "Dinner",
        description: ""
    },
    {
        time: "8:30 PM - 9:30 PM",
        title: "Grace Story Session in Sawan Ashram (Optional)",
        description: ""
    }
];

const day2Events = [
    {
        time: "7:00 AM - 8:00 AM",
        title: "Meditation Session in Sawan Ashram",
        description: ""
    },
    {
        time: "8:00 AM - 9:00 AM",
        title: "Breakfast",
        description: ""
    },
    {
        time: "9:00 AM",
        title: "Departure from Sawan Ashram",
        description: ""
    },
    {
        time: "10:30 AM - 11:00 AM",
        title: "Satsang & Meditation",
        description: ""
    },
    {
        time: "11:00 AM - 11:30 AM",
        title: "Address by National Council + Address by NFCs + Fruit Distribution",
        description: ""
    },
    {
        time: "11:30 AM - 12:30 PM",
        title: "Sant Darshan Singh Ji Dham Sewa Area Visit",
        description: ""
    },
    {
        time: "12:30 PM - 1:00 PM",
        title: "September Program Planning of Sewa Areas",
        description: "Group Discussion with NFCs & Zone FCs"
    },
    {
        time: "1:00 PM - 1:30 PM",
        title: "Meeting with NFCs, FCs, SC, and CC",
        description: "With Shivani, Rachneet & Shalini Di"
    },
    {
        time: "1:30 PM onwards",
        title: "Lunch",
        description: ""
    }
];

// Teams Data
const teams = [
    {
        name: "Reception (Welcome Kit)",
        tasks: [
            "Pen",
            "Notepad",
            "Eye mask & Earplugs",
            "Hand Made Greeting Card (welcome, MJ message, Virtue)",
            "Program Sheet",
            "my clear bag"
        ]
    },
    {
        name: "Creative Team",
        tasks: [
            "Design team create the design of different color - Ankit Juneja - Young Adults National Meet 2025, A new era to embrace",
            "Badge made at Home > RC + NFC badge will be of different Color",
            "Gratitude Wall Print",
            "Selfie Point"
        ]
    },
    {
        name: "Inreach & Beone",
        tasks: [
            "Decoration - in cosultation with Creative Team",
            "Mini Hand Made Cards"
        ]
    },
    {
        name: "Pandal + Admin Team + Cleaniness Team",
        tasks: [
            "Setup and windup"
        ]
    },
    {
        name: "Pandal Team",
        tasks: [
            "Matting outside DMH"
        ]
    },
    {
        name: "Reception + Traffic",
        tasks: [
            "List of Volunteers will be given to traffic team are coming from sawan Ashram to Kirpal Ashram + Sawan Ashram to Darshan Dham + Station to Sawan Ashram"
        ]
    },
    {
        name: "Wellness",
        tasks: [
            "Wellness team will drop Zone team to their rooms"
        ]
    },
    {
        name: "Admin",
        tasks: [
            "Parshad Packing and distribution"
        ]
    }
];

// Logistics Data
const logistics = [
    "Stay at Sawan Ashram for all the attendees those who are coming from different Zones from 15th Night",
    "Dinner - Langer prasad will be available for all the participants staying at Sawan Ashram",
    "FCs, SC, CC, TLs will be invited from Zones",
    "200 - 250 Count will be invited",
    "Railway Station to Sawan Ashram Transport",
    "Railway Station to Kirpal Ashram Transport",
    "Sawan Ashram to Burari Transport",
    "Sawan Ashram to Kirpal Ashram Transport",
    "Nimbu pani ki kirpal ashram & Burari",
    "Tea & Biscuit in Sawan Ashram",
    "Bands",
    "Selfie Booth",
    "Red Carpet Welcome",
    "Gratitude Tree (optional)/ Gratitude Wall",
    "Internet access in Darshan Meditation Hall"
];

// Render Schedule
function renderSchedule() {
    const day1Timeline = document.querySelector("#day1 .timeline");
    const day2Timeline = document.querySelector("#day2 .timeline");

    day1Events.forEach((event, index) => {
        const eventElement = document.createElement("div");
        eventElement.className = `event ${index % 2 === 0 ? 'left' : 'right'}`;
        eventElement.innerHTML = `
            <div class="event-time">${event.time}</div>
            <div class="event-title">${event.title}</div>
            ${event.description ? `<div class="event-description">${event.description}</div>` : ''}
        `;
        day1Timeline.appendChild(eventElement);
    });

    day2Events.forEach((event, index) => {
        const eventElement = document.createElement("div");
        eventElement.className = `event ${index % 2 === 0 ? 'left' : 'right'}`;
        eventElement.innerHTML = `
            <div class="event-time">${event.time}</div>
            <div class="event-title">${event.title}</div>
            ${event.description ? `<div class="event-description">${event.description}</div>` : ''}
        `;
        day2Timeline.appendChild(eventElement);
    });
}

// Render Teams
function renderTeams() {
    const teamsContainer = document.querySelector(".teams-container");

    teams.forEach(team => {
        const teamCard = document.createElement("div");
        teamCard.className = "team-card";
        teamCard.innerHTML = `
            <div class="team-name">${team.name}</div>
            <ul class="task-list">
                ${team.tasks.map(task => `<li>${task}</li>`).join('')}
            </ul>
        `;
        teamsContainer.appendChild(teamCard);
    });
}

// Render Logistics
function renderLogistics() {
    const logisticsContainer = document.querySelector(".logistics-container");

    logistics.forEach(item => {
        const logisticsItem = document.createElement("div");
        logisticsItem.className = "logistics-item";
        logisticsItem.innerHTML = `
            <p>${item}</p>
        `;
        logisticsContainer.appendChild(logisticsItem);
    });
}

// Initialize the page
document.addEventListener("DOMContentLoaded", function() {
    renderSchedule();
    renderTeams();
    renderLogistics();
    
    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });
});

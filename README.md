
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AcademeForge</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>AcademeForge</h1>
        <nav>
            <ul>
                <li><a href="#about">About Us</a></li>
                <li><a href="#ast">AST</a></li>
                <li><a href="#courses">Courses</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#contact">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <h2>Empowering India's Future, One Scholar at a Time</h2>
            <div class="cta-buttons">
                <a href="#register" class="cta">Register for AST</a>
                <a href="#telegram" class="cta">Join Telegram</a>
                <a href="#download" class="cta">Download App</a>
                <a href="#youtube" class="cta">Watch on YouTube</a>
            </div>
        </section>

        <section class="video">
            <h3>What is AcademeForge?</h3>
            <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" frameborder="0" allowfullscreen></iframe>
        </section>

        <section class="live-stats">
            <h3>Live Stats</h3>
            <p>Students Enrolled: <span id="students-enrolled">1000</span></p>
            <p>Cities Covered: <span id="cities-covered">50</span></p>
            <p>Scholarships Distributed: <span id="scholarships-distributed">200</span></p>
        </section>

        <section class="success-stories">
            <h3>Success Stories</h3>
            <div class="testimonials">
                <p>"AcademeForge changed my life!" - Student A</p>
                <p>"I achieved my dreams with their help!" - Student B</p>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 AcademeForge. All rights reserved.</p>
    </footer>

    <script src="script.js"></script> 
    body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: navy;
    color: white;
    padding: 20px;
    text-align: center;
}

.cta-buttons button {
    margin: 10px;
    padding: 10px 20px;
    background-color: orange;
    border: none;
    color: white;
    cursor: pointer;
}

.video-section {
    text-align: center;
    margin: 20px 0;
}

.live-stats {
    background-color: white;
    padding: 20px;
    margin: 20px;
    border-radius: 5px;
}

.success-stories {
    background-color: white;
    padding: 20px;
    margin: 20px;
    border-radius: 5px;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: navy;
    color: white;
    position: relative;
    bottom: 0;
    width: 100%;
         } 
// Simulated live stats update
document.addEventListener("DOMContentLoaded", function() {
    // Simulate fetching data
    const stats = {
        studentsEnrolled: 1200,
        citiesCovered: 50,
        scholarshipsDistributed: 300
    };

    document.getElementById("students-enrolled").innerText = stats.studentsEnrolled;
    document.getElementById("cities-covered").innerText = stats.citiesCovered;
    document.getElementById("scholarships-distributed").innerText = stats.scholarshipsDistributed;
}); 
import React from 'react';
import { StyleSheet, Text, View, Button } from 'react-native';

const App = () => {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>
</body>
</html>

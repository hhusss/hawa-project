        Rate A Spot Website
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rate This Spot</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>Rate This Spot</h1>
    </header>
    <main>
        <section id="form-section">
            <h2>Add New Location</h2>
            <form id="locationForm">
                <div class="form-group">
                    <label for="name">Location Name:</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="rating">Rating:</label>
                    <input type="number" id="rating" name="rating" min="1" max="5" required>
                </div>
                <div class="form-group">
                    <label for="review">Review:</label>
                    <textarea id="review" name="review" required></textarea>
                </div>
                <div class="form-group">
                    <label for="image">Image URL:</label>
                    <input type="text" id="image" name="image" required>
                </div>
                <button type="submit">Save Location</button>
            </form>
        </section>
        <section id="locations-section">
            <h2>Saved Locations</h2>
            <div class="locations-container" id="locationsContainer">
                
                <div class="location-card">
                    <img src="https://a.cdn-hotels.com/gdcs/production97/d1326/d94b74a4-8fc1-4b00-99b8-e6db53199ac8.jpg" alt="Hyde Park">
                    <h3>Hyde Park</h3>
                    <p>Rating: 4</p>
                    <p>A beautiful and spacious park in the heart of London.</p>
                </div>
                <div class="location-card">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6c/London_Eye_at_night_2.jpg" alt="London Eye">
                    <h3>London Eye</h3>
                    <p>Rating: 5</p>
                    <p>Amazing views of London from the top!</p>
                </div>
            </div>
        </section>
    </main>
    <script src="script.js"></script>
</body>
</html>
document.getElementById('locationForm').addEventListener('submit', function(event) {
    event.preventDefault();

 
    const name = document.getElementById('name').value;
    const rating = document.getElementById('rating').value;
    const review = document.getElementById('review').value;
    const image = document.getElementById('image').value;

    
    const locationCard = document.createElement('div');
    locationCard.className = 'location-card';

    locationCard.innerHTML = `
        <img src="${image}" alt="${name}">
        <h3>${name}</h3>
        <p>Rating: ${rating}</p>
        <p>${review}</p>
    `;

    
    const locationsContainer = document.getElementById('locationsContainer');
    locationsContainer.appendChild(locationCard);

    
    document.getElementById('locationForm').reset();
});
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f8ff; /* Alice Blue */
}

header {
    background-color: #1e90ff; /* Dodger Blue */
    color: #fff;
    padding: 1em;
    text-align: center;
    font-family: 'Poppins', sans-serif;
}

main {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 1em;
}

#form-section, #locations-section {
    background-color: #ffffff;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin: 1em;
    padding: 1em;
    width: 45%;
}

h2 {
    color: #1e90ff; /* Dodger Blue */
    font-family: 'Poppins', sans-serif;
}

.form-group {
    margin-bottom: 1em;
}

.form-group label {
    display: block;
    margin-bottom: 0.5em;
}

.form-group input, .form-group textarea {
    width: 100%;
    padding: 0.5em;
    border: 1px solid #ddd;
    border-radius: 5px;
}

button {
    background-color: #1e90ff; /* Dodger Blue */
    color: white;
    padding: 0.5em 1em;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #1565c0; /* Darker shade of Dodger Blue */
}

.locations-container {
    margin-top: 1em;
    display: flex;
    flex-wrap: wrap;
    gap: 1em;
}

.location-card {
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 1em;
    width: calc(45% - 1em);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.location-card img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
}

.location-card h3 {
    margin: 0;
    font-size: 1.2em;
}

.location-card p {
    margin: 0.5em 0 0;
}
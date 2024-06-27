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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>World Animal Encyclopedia</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom, #f0f8ff, #e6f7ff);
            color: #333;
        }
        .hero {
            background: url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center;
            background-size: cover;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
        }
        .hero h1 {
            font-size: 3rem;
        }
        .animal-card {
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .animal-card:hover {
            transform: scale(1.05);
        }
        .fact-box {
            background: #fff3cd;
            border-left: 5px solid #ffc107;
            padding: 10px;
            margin: 10px 0;
        }
        footer {
            background: #343a40;
            color: white;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>
<body>
    <header class="hero">
        <div class="container text-center">
            <h1>World Animal Encyclopedia</h1>
            <p>Discover facts, images, and wonders of every animal species!</p>
            <input type="text" id="search" class="form-control w-50 mx-auto" placeholder="Search for an animal...">
        </div>
    </header>

    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container">
            <a class="navbar-brand" href="#">Encyclopedia</a>
            <div class="collapse navbar-collapse">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item"><a class="nav-link" href="#mammals">Mammals</a></li>
                    <li class="nav-item"><a class="nav-link" href="#birds">Birds</a></li>
                    <li class="nav-item"><a class="nav-link" href="#reptiles">Reptiles</a></li>
                    <li class="nav-item"><a class="nav-link" href="#fish">Fish</a></li>
                    <li class="nav-item"><a class="nav-link" href="#insects">Insects</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <main class="container my-5">
        <section id="featured">
            <h2 class="text-center mb-4">Featured Animals</h2>
            <div class="row">
                <!-- Lion Example -->
                <div class="col-md-4 mb-4">
                    <div class="card animal-card">
                        <img src="https://images.unsplash.com/photo-1544568100-847a948585b9?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Lion">
                        <div class="card-body">
                            <h5 class="card-title">Lion (Panthera leo)</h5>
                            <p class="card-text">Lions are apex predators in the savannas of Africa and India.</p>
                            <button class="btn btn-primary" onclick="toggleDetails('lion')">Learn More</button>
                            <div id="lion-details" class="mt-3" style="display:none;">
                                <div class="fact-box">
                                    <strong>Fun Fact:</strong> A lion's roar can be heard up to 5 miles away!
                                </div>
                                <p><strong>Habitat:</strong> Grasslands, savannas.</p>
                                <p><strong>Diet:</strong> Carnivorous, preying on zebras, antelopes.</p>
                                <p><strong>Conservation:</strong> Vulnerable due to habitat loss.</p>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Penguin Example -->
                <div class="col-md-4 mb-4">
                    <div class="card animal-card">
                        <img src="https://images.unsplash.com/photo-1551986782-d0169b3f8fa7?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Penguin">
                        <div class="card-body">
                            <h5 class="card-title">Emperor Penguin (Aptenodytes forsteri)</h5>
                            <p class="card-text">The largest penguin species, thriving in Antarctica's icy waters.</p>
                            <button class="btn btn-primary" onclick="toggleDetails('penguin')">Learn More</button>
                            <div id="penguin-details" class="mt-3" style="display:none;">
                                <div class="fact-box">
                                    <strong>Fun Fact:</strong> They can dive up to 1,800 feet deep!
                                </div>
                                <p><strong>Habitat:</strong> Antarctic ice shelves.</p>
                                <p><strong>Diet:</strong> Fish, krill.</p>
                                <p><strong>Conservation:</strong> Near threatened due to climate change.</p>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Python Example -->
                <div class="col-md-4 mb-4">
                    <div class="card animal-card">
                        <img src="https://images.unsplash.com/photo-1520637836862-4d197d17c1a8?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Python">
                        <div class="card-body">
                            <h5 class="card-title">Burmese Python (Python bivittatus)</h5>
                            <p class="card-text">A large constrictor snake native to Southeast Asia.</p>
                            <button class="btn btn-primary" onclick="toggleDetails('python')">Learn More</button>
                            <div id="python-details" class="mt-3" style="display:none;">
                                <div class="fact-box">
                                    <strong>Fun Fact:</strong> They can grow up to 23 feet long!
                                </div>
                                <p><strong>Habitat:</strong> Tropical forests, grasslands.</p>
                                <p><strong>Diet:</strong> Rodents, birds, small mammals.</p>
                                <p><strong>Conservation:</strong> Least concern, but invasive in Florida.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Add more sections like #mammals, #birds, etc., with similar cards for other animals -->
        <section id="mammals">
            <h2>Mammals</h2>
            <p>Explore over 6,000 mammal species. (Add more cards here.)</p>
        </section>
        <!-- Repeat for other categories -->
    </main>

    <footer>
        <p>&copy; 2023 World Animal Encyclopedia. Data sourced from reliable sources like IUCN and National Geographic.</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        function toggleDetails(id) {
            const details = document.getElementById(id + '-details');
            details.style.display = details.style.display === 'none' ? 'block' : 'none';
        }

        // Simple search functionality
        document.getElementById('search').addEventListener('input', function() {
            const query = this.value.toLowerCase();
            const cards = document.querySelectorAll('.animal-card');
            cards.forEach(card => {
                const title = card.querySelector('.card-title').textContent.toLowerCase();
                card.style.display = title.includes(query) ? 'block' : 'none';
            });
        });
    </script>
</body>
</html>

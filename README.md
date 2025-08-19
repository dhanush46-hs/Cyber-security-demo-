# Cyber-security-demo-
Demo 
<!DOCTYPE html>
 <html lang="en">

 <head>
     <meta charset="UTF-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
     <title>Sunrise Avenue</title>

     <!-- Bootstrap CSS -->
     <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />

     <!-- CCBP UI Kit CSS (optional if available) -->
     <link rel="stylesheet" href="https://ccbp-assets.s3.ap-south-1.amazonaws.com/css/ui-kit.css" />

     <!-- Custom CSS -->
     <link rel="stylesheet" href="styles.css" />
 </head>

 <body>

     <!-- Hero Section -->
     <div class="hero d-flex flex-column justify-content-center align-items-center text-center" id="sectionHero">
         <h1 class="text-warning fw-bold">Sunrise Avenue</h1>
         <p class="text-white">Move to what moves you.</p>
         <div class="container mt-3">
             <button class="btn btn-warning" onclick="showFlats()">Book Flat</button>
         </div>
     </div>

     <!-- Flats List Section -->
     <div class="container d-none" id="sectionFlats">
         <h2 class="text-warning my-4">Sunrise Avenue</h2>

         <div class="d-flex flex-row flex-wrap gap-4">

             <!-- 3BHK Flat -->
             <div class="card" style="width: 18rem;">
                 <img src="https://assets.ccbp.in/frontend/static-website/flats-list-card1-img.png" class="card-img-top" alt="3BHK Flat">
                 <div class="card-body">
                     <h5 class="card-title">3BHK Flat</h5>
                     <p class="card-text">Fully furnished house with luxury en-suite, 1600sq.ft.</p>
                     <button class="btn btn-warning" onclick="showDetails('sectionDetails3bhk')">More Info</button>
                 </div>
             </div>

             <!-- 2BHK Flat -->
             <div class="card" style="width: 18rem;">
                 <img src="https://assets.ccbp.in/frontend/static-website/flats-list-card2-img.png" class="card-img-top" alt="2BHK Flat">
                 <div class="card-body">
                     <h5 class="card-title">2BHK Flat</h5>
                     <p class="card-text">Minimalist modern-day flat, 1200sq.ft.</p>
                     <button class="btn btn-warning" onclick="showDetails('sectionDetails2bhk')">More Info</button>
                 </div>
             </div>

             <!-- 4BHK Flat -->
             <div class="card" style="width: 18rem;">
                 <img src="https://assets.ccbp.in/frontend/static-website/flats-list-card3-img.png" class="card-img-top" alt="4BHK Flat">
                 <div class="card-body">
                     <h5 class="card-title">4BHK Flat</h5>
                     <p class="card-text">Colorful elegant home, 3600sq.ft.</p>
                     <button class="btn btn-warning" onclick="showDetails('sectionDetails4bhk')">More Info</button>
                 </div>
             </div>

         </div>
         <button class="btn btn-secondary mt-4" onclick="goBack()">Back</button>
     </div>

     <!-- 3BHK Flat Details -->
     <div class="container d-none" id="sectionDetails3bhk">
         <img src="https://assets.ccbp.in/frontend/static-website/flats-list-d1-img.png" class="img-fluid" alt="3BHK Flat Details">
         <h3 class="text-warning mt-3">Rs 3000/-</h3>
         <p><i class="bi bi-geo-alt-fill"></i> D/N 5-2, Food Street, Indore</p>
         <h4 class="text-warning">Description</h4>
         <p>This is a fully furnished house with handmade furniture including a luxury en-suite facilities pack. Its built-up area is about 1600sq.ft. A spacious home for you to live in.</p>
         <button class="btn btn-success">Confirm</button>
         <button class="btn btn-secondary" onclick="showFlats()">Back</button>
     </div>

     <!-- 2BHK Flat Details -->
     <div class="container d-none" id="sectionDetails2bhk">
         <img src="https://assets.ccbp.in/frontend/static-website/flats-list-d2-img.png" class="img-fluid" alt="2BHK Flat Details">
         <h3 class="text-warning mt-3">Rs 2000/-</h3>
         <p><i class="bi bi-geo-alt-fill"></i> D/N 6-2, Food Street, Indore</p>
         <h4 class="text-warning">Description</h4>
         <p>A minimalist house made for modern-day families. It is fully furnished with trending furniture. Its built-up area is about 1200sq.ft.</p>
         <button class="btn btn-success">Confirm</button>
         <button class="btn btn-secondary" onclick="showFlats()">Back</button>
     </div>

     <!-- 4BHK Flat Details -->
     <div class="container d-none" id="sectionDetails4bhk">
         <img src="https://assets.ccbp.in/frontend/static-website/flats-list-d3-img.png" class="img-fluid" alt="4BHK Flat Details">
         <h3 class="text-warning mt-3">Rs 4000/-</h3>
         <p><i class="bi bi-geo-alt-fill"></i> D/N 5-2, Food Street, Indore</p>
         <h4 class="text-warning">Description</h4>
         <p>A contemporary home with more color and vibrancy. It is fully furnished with elegant furniture. Its built-up area is about 3600sq.ft.</p>
         <button class="btn btn-success">Confirm</button>
         <button class="btn btn-secondary" onclick="showFlats()">Back</button>
     </div>

     <!-- JavaScript to switch views -->
     <script>
         function showFlats() {
             document.getElementById("sectionHero").classList.add("d-none");
             document.getElementById("sectionFlats").classList.remove("d-none");

             document.getElementById("sectionDetails3bhk").classList.add("d-none");
             document.getElementById("sectionDetails2bhk").classList.add("d-none");
             document.getElementById("sectionDetails4bhk").classList.add("d-none");
         }

         function goBack() {
             document.getElementById("sectionHero").classList.remove("d-none");
             document.getElementById("sectionFlats").classList.add("d-none");
         }

         function showDetails(sectionId) {
             document.getElementById("sectionFlats").classList.add("d-none");

             document.getElementById("sectionDetails3bhk").classList.add("d-none");
             document.getElementById("sectionDetails2bhk").classList.add("d-none");
             document.getElementById("sectionDetails4bhk").classList.add("d-none");

             document.getElementById(sectionId).classList.remove("d-none");
         }
     </script>
 </body>

 </html>

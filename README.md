<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Study Pathfinder - Find Your Learning Path</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #4361ee;
            --secondary: #3a0ca3;
            --accent: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4bb543;
        }
        
        body {
            background-color: #f5f7fb;
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 2rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--accent);
        }
        
        /* Hero Section */
        .hero {
            padding: 4rem 0;
            text-align: center;
            background-color: white;
            border-radius: 10px;
            margin: 2rem 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0,  ͦ0.1);
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            color: #555;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* Features Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        /* Assessment Section */
        .assessment {
            background: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin: 3rem 0;
        }
        
        .assessment h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--secondary);
        }
        
        .question {
            margin-bottom: 2rem;
            padding: 1.5rem;
            border-radius: 8px;
            background: #f8f9fa;
        }
        
        .question h3 {
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        .options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }
        
        .option {
            padding: 1rem;
            background: white;
            border: 2px solid #e9ecef;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .option:hover {
            border-color: var(--accent);
        }
        
        .option.selected {
            border-color: var(--primary);
            background: rgba(67, 97, 238, 0.1);
        }
        
        .hidden {
            display: none;
        }
        
        /* Results Section */
        .results {
            background: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin: 3rem 0;
        }
        
        .result-card {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
        }
        
        .result-card h3 {
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        .resources {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .resource-card {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
        }
        
        .resource-card h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
            margin-top: 3rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h3 {
            margin-bottom: 1.5rem;
            color: var(--accent);
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-section ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-section ul li a:hover {
            color: var(--accent);
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .assessment, .results {
                padding: 2rem 1rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-graduation-cap"></i>
                Study Pathfinder
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#assessment">Assessment</a></li>
                    <li><a href="#resources">Resources</a></li>
                    <li><a href="#about">About</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container">
        <!-- Hero Section -->
        <section id="home" class="hero">
            <h1>Discover Your Perfect Study Path</h1>
            <p>Take our assessment to find out which subjects and careers align with your interests and strengths. Get personalized study resources to help you succeed.</p>
            <a href="#assessment" class="btn">Start Assessment</a>
        </section>

        <!-- Features Section -->
        <section class="features">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-search"></i>
                </div>
                <h3>Interest Assessment</h3>
                <p>Discover your academic and career interests through our scientifically designed assessment.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-road"></i>
                </div>
                <h3>Personalized Path</h3>
                <p>Get a customized study plan based on your interests, strengths, and career goals.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-book-open"></i>
                </div>
                <h3>Study Resources</h3>
                <p>Access curated learning materials, courses, and tools to help you excel in your chosen field.</p>
            </div>
        </section>

        <!-- Assessment Section -->
        <section id="assessment" class="assessment">
            <h2>Discover Your Study Interests</h2>
            <p style="text-align: center; margin-bottom: 2rem;">Answer these questions to help us understand your interests and recommend the best study path for you.</p>
            
            <div id="question-container">
                <!-- Questions will be dynamically inserted here -->
            </div>
            
            <div style="text-align: center;">
                <button id="prev-btn" class="btn" style="background: #6c757d; margin-right: 10px;">Previous</button>
                <button id="next-btn" class="btn">Next</button>
                <button id="submit-btn" class="btn hidden" style="background: var(--success);">Get Results</button>
            </div>
        </section>

        <!-- Results Section -->
        <section id="results" class="results hidden">
            <h2>Your Personalized Study Path</h2>
            <div id="results-content">
                <!-- Results will be dynamically inserted here -->
            </div>
            
            <h3 style="margin-top: 2rem;">Recommended Resources</h3>
            <div class="resources" id="recommended-resources">
                <!-- Resources will be dynamically inserted here -->
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Study Pathfinder</h3>
                    <p>Helping students discover their passions and find the right educational path since 2023.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#assessment">Assessment</a></li>
                        <li><a href="#resources">Resources</a></li>
                        <li><a href="#about">About Us</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-envelope"></i> contact@studypathfinder.com</li>
                        <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Education St, Learn City</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Study Pathfinder. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Assessment questions and logic
        const questions = [
            {
                question: "Which of these activities do you enjoy the most?",
                options: [
                    { text: "Solving puzzles and logical problems", category: "analytical" },
                    { text: "Creating art, music, or writing stories", category: "creative" },
                    { text: "Helping others and working in teams", category: "social" },
                    { text: "Building or fixing things with your hands", category: "practical" }
                ]
            },
            {
                question: "What type of books or media do you prefer?",
                options: [
                    { text: "Science fiction or technology magazines", category: "analytical" },
                    { text: "Novels, poetry, or art books", category: "creative" },
                    { text: "Biographies or books about relationships", category: "social" },
                    { text: "How-to guides or DIY magazines", category: "practical" }
                ]
            },
            {
                question: "Which school subject interests you the most?",
                options: [
                    { text: "Mathematics or Computer Science", category: "analytical" },
                    { text: "Literature or Art", category: "creative" },
                    { text: "Psychology or Sociology", category: "social" },
                    { text: "Physical Education or Shop Class", category: "practical" }
                ]
            },
            {
                question: "How do you approach problem-solving?",
                options: [
                    { text: "Analyze data and look for patterns", category: "analytical" },
                    { text: "Think outside the box for creative solutions", category: "creative" },
                    { text: "Discuss with others to get different perspectives", category: "social" },
                    { text: "Try different approaches until something works", category: "practical" }
                ]
            },
            {
                question: "What kind of work environment do you prefer?",
                options: [
                    { text: "Quiet office with minimal distractions", category: "analytical" },
                    { text: "Flexible space that encourages innovation", category: "creative" },
                    { text: "Dynamic environment with lots of interaction", category: "social" },
                    { text: "Hands-on setting with tools and equipment", category: "practical" }
                ]
            }
        ];

        // Study paths based on interest categories
        const studyPaths = {
            analytical: {
                title: "Analytical & Technical Path",
                description: "Your answers suggest you have strong analytical thinking skills and enjoy solving complex problems. You might excel in fields that require logical reasoning and data analysis.",
                fields: ["Computer Science", "Engineering", "Mathematics", "Data Science", "Physics", "Economics"],
                resources: [
                    { title: "Khan Academy - Math & Science", description: "Free courses in mathematics, science, and computing.", url: "#" },
                    { title: "Codecademy", description: "Interactive coding lessons in various programming languages.", url: "#" },
                    { title: "Coursera - Data Science", description: "Specializations in data analysis and machine learning.", url: "#" }
                ]
            },
            creative: {
                title: "Creative & Artistic Path",
                description: "Your responses indicate a creative mindset and appreciation for artistic expression. You might thrive in fields that allow for innovation and self-expression.",
                fields: ["Graphic Design", "Creative Writing", "Film Production", "Music Composition", "Architecture", "Marketing"],
                resources: [
                    { title: "Skillshare - Creative Arts", description: "Thousands of classes in design, photography, and more.", url: "#" },
                    { title: "Adobe Creative Cloud Tutorials", description: "Learn industry-standard creative software.", url: "#" },
                    { title: "MasterClass - Writing & Design", description: "Learn from renowned artists and creators.", url: "#" }
                ]
            },
            social: {
                title: "Social & Helping Path",
                description: "Your answers show strong interpersonal skills and a desire to help others. You might find fulfillment in careers focused on people and communities.",
                fields: ["Psychology", "Education", "Social Work", "Healthcare", "Human Resources", "Counseling"],
                resources: [
                    { title: "Coursera - Psychology & Social Sciences", description: "Courses from top universities on human behavior.", url: "#" },
                    { title: "edX - Education & Teaching", description: "Professional development for educators.", url: "#" },
                    { title: "Mental Health First Aid", description: "Training to support people experiencing mental health crises.", url: "#" }
                ]
            },
            practical: {
                title: "Practical & Hands-On Path",
                description: "Your responses suggest you enjoy working with your hands and solving tangible problems. You might excel in fields that involve building, repairing, or creating physical objects.",
                fields: ["Mechanical Engineering", "Construction Management", "Culinary Arts", "Automotive Technology", "Electrical Work", "Fashion Design"],
                resources: [
                    { title: "Instructables DIY Projects", description: "Step-by-step guides for hands-on projects.", url: "#" },
                    { title: "YouTube Learning Channels", description: "Tutorials for various practical skills.", url: "#" },
                    { title: "Trade School Directory", description: "Find vocational programs in your area.", url: "#" }
                ]
            }
        };

        // DOM elements
        const questionContainer = document.getElementById('question-container');
        const prevBtn = document.getElementById('prev-btn');
        const nextBtn = document.getElementById('next-btn');
        const submitBtn = document.getElementById('submit-btn');
        const resultsSection = document.getElementById('results');
        const resultsContent = document.getElementById('results-content');
        const resourcesContainer = document.getElementById('recommended-resources');

        // State variables
        let currentQuestion = 0;
        const userAnswers = new Array(questions.length).fill(null);

        // Initialize assessment
        function initAssessment() {
            displayQuestion(currentQuestion);
            updateNavigationButtons();
        }

        // Display current question
        function displayQuestion(index) {
            const question = questions[index];
            
            let optionsHTML = '';
            question.options.forEach((option, i) => {
                const isSelected = userAnswers[index] === i;
                optionsHTML += `
                    <div class="option ${isSelected ? 'selected' : ''}" data-index="${i}">
                        ${option.text}
                    </div>
                `;
            });
            
            questionContainer.innerHTML = `
                <div class="question">
                    <h3>Question ${index + 1} of ${questions.length}</h3>
                    <p>${question.question}</p>
                    <div class="options">
                        ${optionsHTML}
                    </div>
                </div>
            `;
            
            // Add event listeners to options
            document.querySelectorAll('.option').forEach(option => {
                option.addEventListener('click', () => {
                    const optionIndex = parseInt(option.getAttribute('data-index'));
                    userAnswers[index] = optionIndex;
                    displayQuestion(index); // Refresh to show selection
                });
            });
        }

        // Update navigation buttons state
        function updateNavigationButtons() {
            prevBtn.classList.toggle('hidden', currentQuestion === 0);
            nextBtn.classList.toggle('hidden', currentQuestion === questions.length - 1);
            submitBtn.classList.toggle('hidden', currentQuestion !== questions.length - 1);
        }

        // Calculate results based on user answers
        function calculateResults() {
            const categoryCount = {
                analytical: 0,
                creative: 0,
                social: 0,
                practical: 0
            };
            
            // Count selections for each category
            userAnswers.forEach((answerIndex, questionIndex) => {
                if (answerIndex !== null) {
                    const category = questions[questionIndex].options[answerIndex].category;
                    categoryCount[category]++;
                }
            });
            
            // Find the dominant category
            let dominantCategory = 'analytical';
            let maxCount = categoryCount.analytical;
            
            for (const category in categoryCount) {
                if (categoryCount[category] > maxCount) {
                    maxCount = categoryCount[category];
                    dominantCategory = category;
                }
            }
            
            return dominantCategory;
        }

        // Display results
        function displayResults() {
            const dominantCategory = calculateResults();
            const studyPath = studyPaths[dominantCategory];
            
            let fieldsHTML = '';
            studyPath.fields.forEach(field => {
                fieldsHTML += `<li>${field}</li>`;
            });
            
            let resourcesHTML = '';
            studyPath.resources.forEach(resource => {
                resourcesHTML += `
                    <div class="resource-card">
                        <h4>${resource.title}</h4>
                        <p>${resource.description}</p>
                        <a href="${resource.url}" class="btn" style="padding: 8px 15px; margin-top: 10px; font-size: 0.9rem;">Explore</a>
                    </div>
                `;
            });
            
            resultsContent.innerHTML = `
                <div class="result-card">
                    <h3>${studyPath.title}</h3>
                    <p>${studyPath.description}</p>
                    <h4 style="margin-top: 1.5rem;">Recommended Fields of Study:</h4>
                    <ul style="margin-left: 1.5rem; margin-top: 0.5rem;">
                        ${fieldsHTML}
                    </ul>
                </div>
            `;
            
            resourcesContainer.innerHTML = resourcesHTML;
            resultsSection.classList.remove('hidden');
            
            // Scroll to results
            resultsSection.scrollIntoView({ behavior: 'smooth' });
        }

        // Event listeners for navigation
        prevBtn.addEventListener('click', () => {
            if (currentQuestion > 0) {
                currentQuestion--;
                displayQuestion(currentQuestion);
                updateNavigationButtons();
            }
        });

        nextBtn.addEventListener('click', () => {
            if (currentQuestion < questions.length - 1) {
                currentQuestion++;
                displayQuestion(currentQuestion);
                updateNavigationButtons();
            }
        });

        submitBtn.addEventListener('click', displayResults);

        // Initialize the assessment when page loads
        document.addEventListener('DOMContentLoaded', initAssessment);
    </script>
</body>
</html>

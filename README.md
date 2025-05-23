<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tyakkai Social - Social Media Management for Small Businesses</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --text: #333333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--text);
            line-height: 1.6;
            background-color: #f5f7ff;
        }
        
        a {
            text-decoration: none;
            color: var(--primary);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 24px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: white;
            border: 2px solid var(--primary);
        }
        
        .btn-primary:hover {
            background-color: var(--secondary);
            border-color: var(--secondary);
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-2px);
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            z-index: 100;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, #f5f7ff 0%, #e8ecff 100%);
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 50px;
        }
        
        .hero-text h1 {
            font-size: 48px;
            margin-bottom: 20px;
            color: var(--dark);
            line-height: 1.2;
        }
        
        .hero-text p {
            font-size: 18px;
            margin-bottom: 30px;
            color: #555;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
        }
        
        .hero-image {
            flex: 1;
            text-align: center;
        }
        
        .hero-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }
        
        /* Features Section */
        .features {
            padding: 100px 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: var(--dark);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: var(--light);
            border-radius: 10px;
            padding: 30px;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 40px;
            color: var(--accent);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* How It Works Section */
        .how-it-works {
            padding: 100px 0;
            background-color: #f9faff;
        }
        
        .steps {
            display: flex;
            justify-content: space-between;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        
        .step {
            flex: 1;
            min-width: 250px;
            text-align: center;
            padding: 0 20px;
            position: relative;
            margin-bottom: 30px;
        }
        
        .step-number {
            width: 60px;
            height: 60px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: 700;
            margin: 0 auto 20px;
        }
        
        .step h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .step:not(:last-child)::after {
            content: '';
            position: absolute;
            top: 30px;
            right: -50px;
            width: 100px;
            height: 2px;
            background-color: var(--accent);
            opacity: 0.3;
        }
        
        /* Testimonials Section */
        .testimonials {
            padding: 100px 0;
            background-color: white;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: var(--light);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: #ddd;
            margin-right: 15px;
            overflow: hidden;
        }
        
        .author-info h4 {
            margin-bottom: 5px;
            color: var(--dark);
        }
        
        .author-info p {
            color: #666;
            font-size: 14px;
        }
        
        /* CTA Section */
        .cta {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            text-align: center;
        }
        
        .cta h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }
        
        .cta p {
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        .cta .btn {
            background-color: white;
            color: var(--primary);
        }
        
        .cta .btn:hover {
            background-color: var(--light);
            transform: translateY(-2px);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            color: #fff;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #aaa;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 14px;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 50px;
                text-align: center;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .step:not(:last-child)::after {
                display: none;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-text h1 {
                font-size: 36px;
            }
            
            .section-title h2 {
                font-size: 30px;
            }
        }
		/* Sidebar Styles */
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100vh;
  background-color: white;
  box-shadow: 2px 0 10px rgba(0, 0, 0, 0.1);
  z-index: 99;
  display: flex;
  flex-direction: column;
  transition: all 0.3s ease;
}

.sidebar-header {
  padding: 20px;
  border-bottom: 1px solid var(--border-color);
}

.sidebar-header .logo {
  display: flex;
  align-items: center;
  font-size: 20px;
  font-weight: 700;
  color: var(--primary);
}

.sidebar-header .logo i {
  margin-right: 10px;
  font-size: 24px;
}

.sidebar-menu {
  flex: 1;
  overflow-y: auto;
  padding: 20px 0;
}

.menu-section {
  margin-bottom: 25px;
}

.menu-title {
  padding: 0 20px 10px;
  font-size: 12px;
  text-transform: uppercase;
  color: var(--light-text);
  letter-spacing: 1px;
  font-weight: 600;
}

.menu-item {
  display: flex;
  align-items: center;
  padding: 12px 20px;
  color: var(--dark);
  transition: all 0.3s ease;
}

.menu-item:hover {
  background-color: var(--light);
  color: var(--primary);
}

.menu-item.active {
  background-color: rgba(67, 97, 238, 0.1);
  color: var(--primary);
  border-left: 3px solid var(--primary);
}

.menu-item i {
  width: 24px;
  margin-right: 12px;
  font-size: 16px;
  text-align: center;
}

.sidebar-footer {
  padding: 15px;
  border-top: 1px solid var(--border-color);
}

.user-profile {
  display: flex;
  align-items: center;
  padding: 8px;
  border-radius: 6px;
  transition: all 0.3s ease;
}

.user-profile:hover {
  background-color: var(--light);
}

.user-profile img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 10px;
}

.user-info {
  flex: 1;
}

.user-name {
  display: block;
  font-weight: 600;
  font-size: 14px;
}

.user-email {
  display: block;
  font-size: 12px;
  color: var(--light-text);
}

.user-profile i {
  font-size: 12px;
  color: var(--light-text);
}

/* Main Content Wrapper */
.main-content-wrapper {
  margin-left: 250px;
  transition: all 0.3s ease;
}

/* Adjust header position */
header {
  left: 250px;
  width: calc(100% - 250px);
}

/* Responsive Adjustments */
@media (max-width: 992px) {
  .sidebar {
    transform: translateX(-100%);
  }
  
  .sidebar.active {
    transform: translateX(0);
  }
  
  .main-content-wrapper {
    margin-left: 0;
  }
  
  header {
    left: 0;
    width: 100%;
  }
  
  .mobile-menu-btn {
    display: block;
  }
}

    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-share-alt"></i>
                    <span>Tyakkai Social</span>
                </div>
                <ul class="nav-links">
                    <li><a href="#features">Features</a></li>
                    <li><a href="#how-it-works">How It Works</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#" class="btn btn-outline">Login</a></li>
                </ul>
            </nav>
        </div>
    </header>
	<!-- Sidebar -->
<div class="sidebar">
  <div class="sidebar-header">
    <div class="logo">
      <i class="fas fa-share-alt"></i>
      <span class="logo-text">Tyakkai</span>
    </div>
  </div>
  
  <div class="sidebar-menu">
    <div class="menu-section">
      <h4 class="menu-title">MAIN</h4>
      <a href="#" class="menu-item active">
        <i class="fas fa-home"></i>
        <span>Dashboard</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fas fa-calendar-alt"></i>
        <span>Calendar</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fas fa-chart-line"></i>
        <span>Analytics</span>
      </a>
    </div>
    
    <div class="menu-section">
      <h4 class="menu-title">SOCIAL ACCOUNTS</h4>
      <a href="#" class="menu-item">
        <i class="fab fa-facebook" style="color: #3b5998;"></i>
        <span>Facebook</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fab fa-twitter" style="color: #1da1f2;"></i>
        <span>Twitter</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fab fa-instagram" style="color: #e1306c;"></i>
        <span>Instagram</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fab fa-linkedin" style="color: #0077b5;"></i>
        <span>LinkedIn</span>
      </a>
    </div>
    
    <div class="menu-section">
      <h4 class="menu-title">TOOLS</h4>
      <a href="#" class="menu-item">
        <i class="fas fa-users"></i>
        <span>Team</span>
      </a>
      <a href="#" class="menu-item">
        <i class="fas fa-cog"></i>
        <span>Settings</span>
      </a>
    </div>
  </div>
  
  <div class="sidebar-footer">
    <div class="user-profile">
      <img src="https://via.placeholder.com/40" alt="User">
      <div class="user-info">
        <span class="user-name">John Doe</span>
        <span class="user-email">john@example.com</span>
      </div>
      <i class="fas fa-chevron-down"></i>
    </div>
  </div>
</div>
</section>

<!-- Main Content Wrapper -->
<div class="main-content-wrapper">

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Social Media Management Made Simple for Small Businesses</h1>
                    <p>Tyakkai Social helps you schedule posts, analyze engagement, and grow your audience—all from one affordable platform.</p>
                    <div class="hero-buttons">
                        <a href="#" class="btn btn-primary">Start Free Trial</a>
                        <a href="#" class="btn btn-outline">See Demo</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://via.placeholder.com/600x400" alt="Tyakkai Social Dashboard Preview">
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Powerful Features for Your Business</h2>
                <p>Everything you need to manage your social media presence efficiently and effectively.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3>Post Scheduling</h3>
                    <p>Schedule posts across multiple platforms in advance and maintain a consistent online presence.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Engagement Analytics</h3>
                    <p>Track likes, shares, comments, and impressions to understand what content resonates with your audience.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-calendar-check"></i>
                    </div>
                    <h3>Content Calendar</h3>
                    <p>Visualize your social media strategy with our intuitive drag-and-drop content calendar.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-hashtag"></i>
                    </div>
                    <h3>Hashtag Suggestions</h3>
                    <p>Our AI recommends trending hashtags to increase your post visibility and reach.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Team Collaboration</h3>
                    <p>Work with your team seamlessly with role-based access and approval workflows.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Mobile Friendly</h3>
                    <p>Manage your social media on the go with our responsive web app.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works Section -->
    <section class="how-it-works" id="how-it-works">
        <div class="container">
            <div class="section-title">
                <h2>How Tyakkai Social Works</h2>
                <p>Get started in just a few simple steps and transform your social media presence.</p>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Connect Your Accounts</h3>
                    <p>Link your Facebook, Instagram, and Twitter accounts securely with our platform.</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Plan Your Content</h3>
                    <p>Use our content calendar to organize and schedule your posts in advance.</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Analyze Performance</h3>
                    <p>Review engagement metrics to understand what content works best for your audience.</p>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <h3>Grow Your Audience</h3>
                    <p>Use our insights and suggestions to refine your strategy and expand your reach.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Customers Say</h2>
                <p>Don't just take our word for it—here's what small business owners like you are saying.</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "Tyakkai Social has saved me so much time! I can schedule a week's worth of posts in under an hour and focus on running my business."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">
                            <img src="https://via.placeholder.com/50" alt="Sarah J.">
                        </div>
                        <div class="author-info">
                            <h4>Sarah J.</h4>
                            <p>Owner, The Coffee Nook</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "The analytics dashboard helped me understand which posts perform best. Our engagement has increased by 75% since we started using Tyakkai."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">
                            <img src="https://via.placeholder.com/50" alt="Michael T.">
                        </div>
                        <div class="author-info">
                            <h4>Michael T.</h4>
                            <p>Marketing Director, Urban Fitness</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "As a small business owner, I can't afford expensive tools. Tyakkai gives me enterprise-level features at a fraction of the cost."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">
                            <img src="https://via.placeholder.com/50" alt="Lisa M.">
                        </div>
                        <div class="author-info">
                            <h4>Lisa M.</h4>
                            <p>Founder, Bloom Florist</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="cta">
        <div class="container">
            <h2>Ready to Transform Your Social Media Presence?</h2>
            <p>Join thousands of small businesses using Tyakkai Social to save time and grow their audience.</p>
            <a href="#" class="btn">Start Your 14-Day Free Trial</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <div class="logo">
                        <i class="fas fa-share-alt"></i>
                        <span>Tyakkai Social</span>
                    </div>
                    <p>Empowering small businesses with affordable social media management tools.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Product</h3>
                    <ul class="footer-links">
                        <li><a href="#">Features</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">Integrations</a></li>
                        <li><a href="#">Updates</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul class="footer-links">
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Help Center</a></li>
                        <li><a href="#">Tutorials</a></li>
                        <li><a href="#">Webinars</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Company</h3>
                    <ul class="footer-links">
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Tyakkai Social. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF Tools - Free Online PDF Merger, Splitter, Compressor & Converter</title>
    <meta name="description" content="Free online PDF tools to merge, split, compress and convert PDF files. Fast, secure and easy to use. No software installation required.">
    <meta name="keywords" content="PDF merger, PDF splitter, PDF compressor, PDF to Word, Word to PDF, PDF tools, online PDF editor">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: white;
        }

        .premium-btn {
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            color: white;
            padding: 8px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 500;
            transition: transform 0.2s;
        }

        .premium-btn:hover {
            transform: translateY(-2px);
        }

        /* Main Content */
        .main-content {
            background: white;
            margin: 30px 0;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 60px 40px;
            text-align: center;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 40px;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 32px;
            font-weight: bold;
            display: block;
        }

        .stat-label {
            font-size: 14px;
            opacity: 0.8;
        }

        /* Ad Space */
        .ad-space {
            background: #f8f9fa;
            border: 2px dashed #dee2e6;
            padding: 20px;
            text-align: center;
            color: #6c757d;
            margin: 20px 0;
            border-radius: 8px;
        }

        /* Tools Grid */
        .tools-section {
            padding: 60px 40px;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            margin-bottom: 50px;
            color: #333;
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .tool-card {
            background: #f8f9ff;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            cursor: pointer;
        }

        .tool-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(102, 126, 234, 0.15);
            border-color: #667eea;
        }

        .tool-card.active {
            border-color: #667eea;
            background: #f0f4ff;
        }

        .tool-icon {
            font-size: 48px;
            margin-bottom: 20px;
            display: block;
        }

        .tool-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #333;
        }

        .tool-card p {
            color: #666;
            margin-bottom: 20px;
        }

        .use-tool-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
        }

        .use-tool-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

        /* Tool Interface */
        .tool-interface {
            display: none;
            background: white;
            border-radius: 15px;
            padding: 40px;
            margin: 30px 0;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .tool-interface.active {
            display: block;
        }

        .interface-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .interface-header h2 {
            font-size: 32px;
            color: #333;
            margin-bottom: 10px;
        }

        .interface-header p {
            color: #666;
            font-size: 16px;
        }

        /* File Upload Area */
        .upload-area {
            border: 3px dashed #dee2e6;
            border-radius: 15px;
            padding: 60px 40px;
            text-align: center;
            margin-bottom: 30px;
            transition: all 0.3s;
            cursor: pointer;
        }

        .upload-area:hover, .upload-area.dragover {
            border-color: #667eea;
            background: #f8f9ff;
        }

        .upload-icon {
            font-size: 64px;
            color: #dee2e6;
            margin-bottom: 20px;
        }

        .upload-area.dragover .upload-icon {
            color: #667eea;
        }

        .upload-text {
            font-size: 18px;
            color: #666;
            margin-bottom: 15px;
        }

        .upload-subtext {
            color: #999;
            font-size: 14px;
        }

        .file-input {
            display: none;
        }

        .upload-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 20px;
            transition: all 0.3s;
        }

        .upload-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

        /* File List */
        .file-list {
            margin: 20px 0;
        }

        .file-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: #f8f9fa;
            padding: 15px 20px;
            border-radius: 10px;
            margin-bottom: 10px;
        }

        .file-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .file-icon {
            font-size: 24px;
            color: #dc3545;
        }

        .file-name {
            font-weight: 500;
            color: #333;
        }

        .file-size {
            color: #666;
            font-size: 14px;
        }

        .remove-file {
            color: #dc3545;
            cursor: pointer;
            font-size: 18px;
            padding: 5px;
        }

        /* Process Button */
        .process-btn {
            background: linear-gradient(135deg, #28a745, #20c997);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 25px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            margin: 30px 0;
            transition: all 0.3s;
        }

        .process-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(40, 167, 69, 0.3);
        }

        .process-btn:disabled {
            background: #6c757d;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        /* Processing Animation */
        .processing {
            text-align: center;
            padding: 40px;
            display: none;
        }

        .processing.active {
            display: block;
        }

        .spinner {
            border: 4px solid #f3f3f3;
            border-top: 4px solid #667eea;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: spin 1s linear infinite;
            margin: 0 auto 20px;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Usage Tracker */
        .usage-tracker {
            background: linear-gradient(135deg, #ffc107, #fd7e14);
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            margin: 20px 0;
        }

        .usage-count {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        /* Features Section */
        .features-section {
            background: #f8f9fa;
            padding: 60px 40px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature {
            text-align: center;
            padding: 20px;
        }

        .feature-icon {
            font-size: 40px;
            margin-bottom: 15px;
            display: block;
        }

        .feature h4 {
            font-size: 18px;
            margin-bottom: 10px;
            color: #333;
        }

        .feature p {
            color: #666;
            font-size: 14px;
        }

        /* Footer */
        .footer {
            background: #343a40;
            color: white;
            padding: 40px 0;
            margin-top: 60px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .footer-section h4 {
            margin-bottom: 20px;
            color: white;
        }

        .footer-section a {
            color: #adb5bd;
            text-decoration: none;
            display: block;
            margin-bottom: 8px;
        }

        .footer-section a:hover {
            color: white;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 32px;
            }
            
            .hero-stats {
                flex-direction: column;
                gap: 20px;
            }
            
            .tools-section,
            .hero {
                padding: 40px 20px;
            }
            
            .nav-links {
                display: none;
            }
        }

        /* Premium Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 1000;
        }

        .modal-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            border-radius: 20px;
            padding: 40px;
            max-width: 500px;
            width: 90%;
            text-align: center;
        }

        .close {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 30px;
            cursor: pointer;
            color: #999;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <nav class="nav">
                <a href="#" class="logo">📄 PDF Tools</a>
                <ul class="nav-links">
                    <li><a href="#tools">Tools</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <a href="#" class="premium-btn" onclick="showPremium()">Go Premium</a>
            </nav>
        </div>
    </header>

    <div class="container">
        <!-- Main Content -->
        <main class="main-content">
            <!-- Hero Section -->
            <section class="hero">
                <h1>Free Online PDF Tools</h1>
                <p>Merge, split, compress and convert PDF files with our powerful online tools. Fast, secure, and completely free to use.</p>
                
                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number">10M+</span>
                        <span class="stat-label">Files Processed</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">500K+</span>
                        <span class="stat-label">Happy Users</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">100%</span>
                        <span class="stat-label">Secure & Private</span>
                    </div>
                </div>
            </section>

            <!-- Ad Space -->
            <div class="ad-space">
                <strong>Advertisement</strong><br>
                Google AdSense Ad Space (728x90)
            </div>

            <!-- Usage Tracker -->
            <div class="usage-tracker">
                <div class="usage-count">
                    <span id="usageCount">0</span> / 3 free uses today
                </div>
                <div>Upgrade to Premium for unlimited usage</div>
            </div>

            <!-- Tools Section -->
            <section id="tools" class="tools-section">
                <h2 class="section-title">Choose Your PDF Tool</h2>
                
                <div class="tools-grid">
                    <!-- PDF Merger -->
                    <div class="tool-card" onclick="selectTool('merger')">
                        <span class="tool-icon">🔗</span>
                        <h3>Merge PDF</h3>
                        <p>Combine multiple PDF files into one document quickly and easily.</p>
                        <button class="use-tool-btn">Use Tool</button>
                    </div>

                    <!-- PDF Splitter -->
                    <div class="tool-card" onclick="selectTool('splitter')">
                        <span class="tool-icon">✂️</span>
                        <h3>Split PDF</h3>
                        <p>Extract pages from PDF files or split into multiple documents.</p>
                        <button class="use-tool-btn">Use Tool</button>
                    </div>

                    <!-- PDF Compressor -->
                    <div class="tool-card" onclick="selectTool('compressor')">
                        <span class="tool-icon">🗜️</span>
                        <h3>Compress PDF</h3>
                        <p>Reduce PDF file size while maintaining quality for easy sharing.</p>
                        <button class="use-tool-btn">Use Tool</button>
                    </div>

                    <!-- PDF to Word -->
                    <div class="tool-card" onclick="selectTool('pdfToWord')">
                        <span class="tool-icon">📝</span>
                        <h3>PDF to Word</h3>
                        <p>Convert PDF documents to editable Word format instantly.</p>
                        <button class="use-tool-btn">Use Tool</button>
                    </div>

                    <!-- Word to PDF -->
                    <div class="tool-card" onclick="selectTool('wordToPdf')">
                        <span class="tool-icon">📄</span>
                        <h3>Word to PDF</h3>
                        <p>Convert Word documents to PDF format with perfect formatting.</p>
                        <button class="use-tool-btn">Use Tool</button>
                    </div>
                </div>

                <!-- Ad Space -->
                <div class="ad-space">
                    <strong>Advertisement</strong><br>
                    Google AdSense Ad Space (336x280)
                </div>

                <!-- Tool Interfaces -->
                <div id="merger-interface" class="tool-interface">
                    <div class="interface-header">
                        <h2>🔗 Merge PDF Files</h2>
                        <p>Upload multiple PDF files and combine them into one document</p>
                    </div>
                    
                    <div class="upload-area" onclick="document.getElementById('mergerInput').click()">
                        <div class="upload-icon">📁</div>
                        <div class="upload-text">Drop PDF files here or click to browse</div>
                        <div class="upload-subtext">Support for multiple files, up to 10MB each</div>
                        <input type="file" id="mergerInput" class="file-input" accept=".pdf" multiple onchange="handleFileUpload(event, 'merger')">
                        <button class="upload-btn">Select Files</button>
                    </div>
                    
                    <div id="mergerFileList" class="file-list"></div>
                    
                    <button id="mergerProcess" class="process-btn" onclick="processFiles('merger')" disabled>
                        Merge PDF Files
                    </button>
                    
                    <div id="mergerProcessing" class="processing">
                        <div class="spinner"></div>
                        <p>Merging your PDF files...</p>
                    </div>
                </div>

                <div id="splitter-interface" class="tool-interface">
                    <div class="interface-header">
                        <h2>✂️ Split PDF Files</h2>
                        <p>Upload a PDF file and extract specific pages or split into multiple documents</p>
                    </div>
                    
                    <div class="upload-area" onclick="document.getElementById('splitterInput').click()">
                        <div class="upload-icon">📁</div>
                        <div class="upload-text">Drop PDF file here or click to browse</div>
                        <div class="upload-subtext">Single PDF file, up to 10MB</div>
                        <input type="file" id="splitterInput" class="file-input" accept=".pdf" onchange="handleFileUpload(event, 'splitter')">
                        <button class="upload-btn">Select File</button>
                    </div>
                    
                    <div id="splitterFileList" class="file-list"></div>
                    
                    <div style="margin: 20px 0; text-align: center;">
                        <label style="display: block; margin-bottom: 10px; font-weight: 500;">Page Range (e.g., 1-5, 7, 10-15):</label>
                        <input type="text" id="pageRange" placeholder="1-3, 5, 8-10" style="padding: 10px; border: 2px solid #dee2e6; border-radius: 8px; width: 300px; max-width: 100%;">
                    </div>
                    
                    <button id="splitterProcess" class="process-btn" onclick="processFiles('splitter')" disabled>
                        Split PDF File
                    </button>
                    
                    <div id="splitterProcessing" class="processing">
                        <div class="spinner"></div>
                        <p>Splitting your PDF file...</p>
                    </div>
                </div>

                <div id="compressor-interface" class="tool-interface">
                    <div class="interface-header">
                        <h2>🗜️ Compress PDF Files</h2>
                        <p>Reduce PDF file size while maintaining quality</p>
                    </div>
                    
                    <div class="upload-area" onclick="document.getElementById('compressorInput').click()">
                        <div class="upload-icon">📁</div>
                        <div class="upload-text">Drop PDF file here or click to browse</div>
                        <div class="upload-subtext">Single PDF file, up to 50MB</div>
                        <input type="file" id="compressorInput" class="file-input" accept=".pdf" onchange="handleFileUpload(event, 'compressor')">
                        <button class="upload-btn">Select File</button>
                    </div>
                    
                    <div id="compressorFileList" class="file-list"></div>
                    
                    <button id="compressorProcess" class="process-btn" onclick="processFiles('compressor')" disabled>
                        Compress PDF File
                    </button>
                    
                    <div id="compressorProcessing" class="processing">
                        <div class="spinner"></div>
                        <p>Compressing your PDF file...</p>
                    </div>
                </div>

                <div id="pdfToWord-interface" class="tool-interface">
                    <div class="interface-header">
                        <h2>📝 Convert PDF to Word</h2>
                        <p>Convert PDF documents to editable Word format</p>
                    </div>
                    
                    <div class="upload-area" onclick="document.getElementById('pdfToWordInput').click()">
                        <div class="upload-icon">📁</div>
                        <div class="upload-text">Drop PDF file here or click to browse</div>
                        <div class="upload-subtext">Single PDF file, up to 10MB</div>
                        <input type="file" id="pdfToWordInput" class="file-input" accept=".pdf" onchange="handleFileUpload(event, 'pdfToWord')">
                        <button class="upload-btn">Select File</button>
                    </div>
                    
                    <div id="pdfToWordFileList" class="file-list"></div>
                    
                    <button id="pdfToWordProcess" class="process-btn" onclick="processFiles('pdfToWord')" disabled>
                        Convert to Word
                    </button>
                    
                    <div id="pdfToWordProcessing" class="processing">
                        <div class="spinner"></div>
                        <p>Converting PDF to Word document...</p>
                    </div>
                </div>

                <div id="wordToPdf-interface" class="tool-interface">
                    <div class="interface-header">
                        <h2>📄 Convert Word to PDF</h2>
                        <p>Convert Word documents to PDF format</p>
                    </div>
                    
                    <div class="upload-area" onclick="document.getElementById('wordToPdfInput').click()">
                        <div class="upload-icon">📁</div>
                        <div class="upload-text">Drop Word file here or click to browse</div>
                        <div class="upload-subtext">Word files (.doc, .docx), up to 10MB</div>
                        <input type="file" id="wordToPdfInput" class="file-input" accept=".doc,.docx" onchange="handleFileUpload(event, 'wordToPdf')">
                        <button class="upload-btn">Select File</button>
                    </div>
                    
                    <div id="wordToPdfFileList" class="file-list"></div>
                    
                    <button id="wordToPdfProcess" class="process-btn" onclick="processFiles('wordToPdf')" disabled>
                        Convert to PDF
                    </button>
                    
                    <div id="wordToPdfProcessing" class="processing">
                        <div class="spinner"></div>
                        <p>Converting Word to PDF document...</p>
                    </div>
                </div>
            </section>

            <!-- Ad Space -->
            <div class="ad-space">
                <strong>Advertisement</strong><br>
                Google AdSense Ad Space (728x90)
            </div>

            <!-- Features Section -->
            <section id="features" class="features-section">
                <div class="container">
                    <h2 class="section-title">Why Choose Our PDF Tools?</h2>
                    
                    <div class="features-grid">
                        <div class="feature">
                            <span class="feature-icon">🚀</span>
                            <h4>Lightning Fast</h4>
                            <p>Process your PDF files in seconds with our optimized algorithms</p>
                        </div>
                        
                        <div class="feature">
                            <span class="feature-icon">🔒</span>
                            <h4>100% Secure</h4>
                            <p>Your files are processed securely and deleted automatically</p>
                        </div>
                        
                        <div class="feature">
                            <span class="feature-icon">💻</span>
                            <h4>No Software Required</h4>
                            <p>Works entirely in your browser - no downloads or installations</p>
                        </div>
                        
                        <div class="feature">
                            <span class="feature-icon">📱</span>
                            <h4>Mobile Friendly</h4>
                            <p>Use our tools on any device - desktop, tablet, or mobile</p>
                        </div>
                        
                        <div class="feature">
                            <span class="feature-icon">🌍</span>
                            <h4>Works Offline</h4>
                            <p>Once loaded, many features work without internet connection</p>
                        </div>
                        
                        <div class="feature">
                            <span class="feature-icon">💯</span>
                            <h4>High Quality</h4>
                            <p>Maintain original quality while processing your documents</p>
                        </div>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>PDF Tools</h4>
                    <a href="#">Merge PDF</a>
                    <a href="#">Split PDF</a>
                    <a href="#">Compress PDF</a>
                    <a href="#">PDF to Word</a>
                    <a href="#">Word to PDF</a>
                </div>
                
                <div class="footer-section">
                    <h4>Company</h4>
                    <a href="#">About Us</a>
                    <a href="#">Privacy Policy</a>
                    <a href="#">Terms of Service</a>
                    <a href="#">Contact</a>
                    <a href="#">FAQ</a>
                </div>
                
                <div class="footer-section">
                    <h4>Support</h4>
                    <a href="#">Help Center</a>
                    <a href="#">API Documentation</a>
                    <a href="#">System Status</a>
                    <a href="#">Report Bug</a>
                </div>
                
                <div class="footer-section">
                    <h4>Follow Us</h4>
                    <a href="#">Twitter</a>
                    <a href="#">Facebook</a>
                    <a href="#">LinkedIn</a>
                    <a href="#">Blog</a>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 30px; padding-top: 30px; border-top: 1px solid #495057;">
                <p>&copy; 2024 PDF Tools. All rights reserved. Made with ❤️ for productivity.</p>
            </div>
        </div>
    </footer>

    <!-- Premium Modal -->
    <div id="premiumModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closePremium()">&times;</span>
            <h2>🚀 Go Premium</h2>
            <div style="text-align: left; margin: 30px 0;">
                <h3 style="

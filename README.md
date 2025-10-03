<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hệ thống lọ - Thanh Phong Saygex AI</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset CSS */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo-icon {
            font-size: 2rem;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 5px 10px;
            border-radius: 4px;
        }

        nav a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        /* Hero Section */
        .hero {
            padding: 4rem 0;
            text-align: center;
            background-color: white;
            margin-bottom: 2rem;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }

        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            color: #7f8c8d;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(106, 17, 203, 0.3);
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(106, 17, 203, 0.4);
        }

        /* Main Content */
        .main-content {
            padding: 2rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
            color: #2c3e50;
            font-size: 2rem;
            position: relative;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            margin: 10px auto;
            border-radius: 2px;
        }

        /* Jar Grid */
        .jar-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 3rem;
        }

        .jar-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }

        .jar-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .jar-image {
            height: 200px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
        }

        .jar-content {
            padding: 1.5rem;
        }

        .jar-content h3 {
            margin-bottom: 0.8rem;
            color: #2c3e50;
        }

        .jar-content p {
            color: #7f8c8d;
            margin-bottom: 1.2rem;
        }

        .jar-stats {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid #eee;
        }

        .stat {
            text-align: center;
        }

        .stat-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #6a11cb;
        }

        .stat-label {
            font-size: 0.8rem;
            color: #7f8c8d;
        }

        /* AI Assistant Section */
        .ai-assistant {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: white;
            padding: 3rem 0;
            border-radius: 15px;
            margin-bottom: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .ai-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        .ai-text {
            flex: 1;
            min-width: 300px;
        }

        .ai-text h2 {
            font-size: 2.2rem;
            margin-bottom: 1.5rem;
        }

        .ai-text p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            opacity: 0.9;
        }

        .ai-features {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 2rem;
        }

        .ai-feature {
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 15px;
            border-radius: 50px;
        }

        .ai-visual {
            flex: 1;
            min-width: 300px;
            text-align: center;
            position: relative;
        }

        .assistant-avatar {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }

        .assistant-avatar::before {
            content: "";
            position: absolute;
            width: 150%;
            height: 150%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            transform: rotate(45deg);
            animation: shine 3s infinite;
        }

        @keyframes shine {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .assistant-name {
            margin-top: 20px;
            font-size: 1.5rem;
            font-weight: 600;
        }

        .assistant-title {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 20px;
        }

        .ai-controls {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }

        .control-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1.2rem;
        }

        .control-btn:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.1);
        }

        .control-btn.active {
            background: white;
            color: #6a11cb;
        }

        /* Camera Section */
        .camera-section {
            background: white;
            padding: 3rem 0;
            border-radius: 15px;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .camera-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            align-items: center;
        }

        .camera-preview {
            flex: 1;
            min-width: 300px;
            background: #2c3e50;
            border-radius: 10px;
            overflow: hidden;
            height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
        }

        .camera-info {
            flex: 1;
            min-width: 300px;
        }

        .camera-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: #2c3e50;
        }

        .camera-info p {
            color: #7f8c8d;
            margin-bottom: 1.5rem;
        }

        .camera-features {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .camera-feature {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .camera-feature i {
            color: #6a11cb;
            font-size: 1.2rem;
        }

        /* Features Section */
        .features {
            background-color: white;
            padding: 3rem 0;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 3rem;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .feature-item {
            text-align: center;
            padding: 1.5rem;
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #6a11cb;
        }

        .feature-item h3 {
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        .feature-item p {
            color: #7f8c8d;
        }

        /* Footer */
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 3rem 0 1.5rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 2rem;
        }

        .footer-column h3 {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 3px;
            background-color: #6a11cb;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column a {
            color: #bdc3c7;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-column a:hover {
            color: white;
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bdc3c7;
            font-size: 0.9rem;
        }

        /* Chatbot */
        .chatbot-container {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
        }

        .chatbot-toggle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .chatbot-toggle:hover {
            transform: scale(1.1);
        }

        .chatbot-window {
            position: absolute;
            bottom: 70px;
            right: 0;
            width: 350px;
            height: 450px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            display: none;
            flex-direction: column;
            overflow: hidden;
        }

        .chatbot-header {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .chatbot-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .chatbot-body {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .message {
            max-width: 80%;
            padding: 10px 15px;
            border-radius: 18px;
            font-size: 0.9rem;
        }

        .bot-message {
            align-self: flex-start;
            background: #f0f2f5;
            color: #333;
        }

        .user-message {
            align-self: flex-end;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
        }

        .chatbot-footer {
            padding: 15px;
            border-top: 1px solid #eee;
            display: flex;
            gap: 10px;
        }

        .chatbot-footer input {
            flex: 1;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
        }

        .chatbot-footer button {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            nav ul {
                gap: 15px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .chatbot-window {
                width: 300px;
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">🧪</div>
                    <h1>Thanh Phong Saygex AI</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#">Trang chủ</a></li>
                        <li><a href="#">Hệ thống lọ</a></li>
                        <li><a href="#">AI Tư vấn</a></li>
                        <li><a href="#">Liên hệ</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>Hệ thống lọ Thanh Phong Saygex với AI</h2>
            <p>Trải nghiệm công nghệ AI tiên tiến với trợ lý ảo, nhận diện giọng nói và camera thông minh để được tư vấn sản phẩm tốt nhất</p>
            <button class="btn" id="startAI">Kích hoạt AI ngay</button>
        </div>
    </section>

    <!-- AI Assistant Section -->
    <section class="ai-assistant">
        <div class="container">
            <div class="ai-content">
                <div class="ai-text">
                    <h2>Trợ lý AI "Em Mỹ Ruby"</h2>
                    <p>Trợ lý ảo thông minh của chúng tôi có thể tư vấn cho bạn về tất cả các loại lọ, giúp bạn lựa chọn sản phẩm phù hợp nhất với nhu cầu.</p>
                    <p>Với công nghệ nhận diện giọng nói tiên tiến, bạn có thể giao tiếp tự nhiên như đang nói chuyện với một chuyên gia thực thụ.</p>
                    
                    <div class="ai-features">
                        <div class="ai-feature">
                            <i class="fas fa-microphone"></i>
                            <span>Nhận diện giọng nói</span>
                        </div>
                        <div class="ai-feature">
                            <i class="fas fa-camera"></i>
                            <span>Hỗ trợ camera</span>
                        </div>
                        <div class="ai-feature">
                            <i class="fas fa-robot"></i>
                            <span>AI thông minh</span>
                        </div>
                        <div class="ai-feature">
                            <i class="fas fa-comments"></i>
                            <span>Tư vấn 24/7</span>
                        </div>
                    </div>
                </div>
                
                <div class="ai-visual">
                    <div class="assistant-avatar">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="assistant-name">Em Mỹ Ruby</div>
                    <div class="assistant-title">Trợ lý AI & Tư vấn viên ảo</div>
                    
                    <div class="ai-controls">
                        <button class="control-btn" id="voiceControl">
                            <i class="fas fa-microphone"></i>
                        </button>
                        <button class="control-btn" id="cameraControl">
                            <i class="fas fa-camera"></i>
                        </button>
                        <button class="control-btn" id="videoCall">
                            <i class="fas fa-video"></i>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Camera Section -->
    <section class="camera-section">
        <div class="container">
            <h2 class="section-title">Hệ thống Camera AI</h2>
            <div class="camera-container">
                <div class="camera-preview">
                    <div class="camera-placeholder">
                        <i class="fas fa-camera" style="font-size: 4rem;"></i>
                        <p>Camera đang tắt</p>
                        <button class="btn" style="margin-top: 15px;" id="toggleCamera">Bật Camera</button>
                    </div>
                </div>
                <div class="camera-info">
                    <h3>Nhận diện sản phẩm thông minh</h3>
                    <p>Hệ thống camera AI của chúng tôi có thể nhận diện các loại lọ và cung cấp thông tin chi tiết về sản phẩm ngay lập tức.</p>
                    
                    <div class="camera-features">
                        <div class="camera-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Nhận diện sản phẩm</span>
                        </div>
                        <div class="camera-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Phân tích kích thước</span>
                        </div>
                        <div class="camera-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Đề xuất sản phẩm tương tự</span>
                        </div>
                        <div class="camera-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Hướng dẫn sử dụng</span>
                        </div>
                    </div>
                    
                    <button class="btn" style="margin-top: 20px;">Trải nghiệm ngay</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Content -->
    <div class="container main-content">
        <!-- Jar System Section -->
        <h2 class="section-title">Hệ thống lọ của chúng tôi</h2>
        <div class="jar-grid">
            <!-- Jar 1 -->
            <div class="jar-card">
                <div class="jar-image">🧪</div>
                <div class="jar-content">
                    <h3>Lọ thủy tinh cao cấp</h3>
                    <p>Lọ thủy tinh chất lượng cao, chịu nhiệt tốt, phù hợp cho các phòng thí nghiệm và nghiên cứu khoa học.</p>
                    <div class="jar-stats">
                        <div class="stat">
                            <div class="stat-value">50ml</div>
                            <div class="stat-label">Dung tích</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">A+</div>
                            <div class="stat-label">Chất lượng</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Jar 2 -->
            <div class="jar-card">
                <div class="jar-image">🔬</div>
                <div class="jar-content">
                    <h3>Lọ nhựa PET</h3>
                    <p>Lọ nhựa PET chống va đập, nhẹ và bền, thích hợp cho đóng gói sản phẩm và vận chuyển.</p>
                    <div class="jar-stats">
                        <div class="stat">
                            <div class="stat-value">100ml</div>
                            <div class="stat-label">Dung tích</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">B+</div>
                            <div class="stat-label">Độ bền</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Jar 3 -->
            <div class="jar-card">
                <div class="jar-image">🌡️</div>
                <div class="jar-content">
                    <h3>Lọ chuyên dụng</h3>
                    <p>Lọ chuyên dụng cho các ứng dụng đặc biệt, có khả năng chống ăn mòn và chịu được hóa chất mạnh.</p>
                    <div class="jar-stats">
                        <div class="stat">
                            <div class="stat-value">250ml</div>
                            <div class="stat-label">Dung tích</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">A++</div>
                            <div class="stat-label">Đặc biệt</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Jar 4 -->
            <div class="jar-card">
                <div class="jar-image">🧴</div>
                <div class="jar-content">
                    <h3>Lọ mỹ phẩm</h3>
                    <p>Lọ chuyên dùng cho mỹ phẩm, thiết kế đẹp mắt, đa dạng màu sắc và kích thước.</p>
                    <div class="jar-stats">
                        <div class="stat">
                            <div class="stat-value">30ml</div>
                            <div class="stat-label">Dung tích</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">A</div>
                            <div class="stat-label">Thẩm mỹ</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Features Section -->
        <section class="features">
            <div class="container">
                <h2 class="section-title">Tính năng nổi bật</h2>
                <div class="feature-grid">
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-robot"></i></div>
                        <h3>AI Thông minh</h3>
                        <p>Trợ lý AI có khả năng học hỏi và cải thiện qua mỗi lần tương tác với khách hàng.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-microphone-alt"></i></div>
                        <h3>Nhận diện giọng nói</h3>
                        <p>Công nghệ nhận diện giọng nói tiên tiến, hỗ trợ tiếng Việt tự nhiên.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-video"></i></div>
                        <h3>Hỗ trợ Video Call</h3>
                        <p>Kết nối video trực tiếp với nhân viên tư vấn để được hỗ trợ tốt nhất.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-camera"></i></div>
                        <h3>Nhận diện hình ảnh</h3>
                        <p>Camera AI nhận diện sản phẩm và cung cấp thông tin chi tiết ngay lập tức.</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Chatbot -->
    <div class="chatbot-container">
        <div class="chatbot-toggle" id="chatbotToggle">
            <i class="fas fa-robot"></i>
        </div>
        <div class="chatbot-window" id="chatbotWindow">
            <div class="chatbot-header">
                <div class="chatbot-avatar">
                    <i class="fas fa-robot"></i>
                </div>
                <div>
                    <div class="assistant-name">Em Mỹ Ruby</div>
                    <div class="assistant-title">Đang trực tuyến</div>
                </div>
            </div>
            <div class="chatbot-body" id="chatbotBody">
                <div class="message bot-message">
                    Xin chào! Tôi là Em Mỹ Ruby, trợ lý AI của Thanh Phong Saygex. Tôi có thể giúp gì cho bạn?
                </div>
            </div>
            <div class="chatbot-footer">
                <input type="text" id="chatInput" placeholder="Nhập câu hỏi của bạn...">
                <button id="sendMessage"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Về chúng tôi</h3>
                    <ul>
                        <li><a href="#">Giới thiệu</a></li>
                        <li><a href="#">Lịch sử hình thành</a></li>
                        <li><a href="#">Tầm nhìn & Sứ mệnh</a></li>
                        <li><a href="#">Đội ngũ nhân sự</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Sản phẩm</h3>
                    <ul>
                        <li><a href="#">Lọ thủy tinh</a></li>
                        <li><a href="#">Lọ nhựa</a></li>
                        <li><a href="#">Lọ chuyên dụng</a></li>
                        <li><a href="#">Lọ theo yêu cầu</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Công nghệ AI</h3>
                    <ul>
                        <li><a href="#">Trợ lý ảo</a></li>
                        <li><a href="#">Nhận diện giọng nói</a></li>
                        <li><a href="#">Camera thông minh</a></li>
                        <li><a href="#">Hỗ trợ 24/7</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Liên hệ</h3>
                    <ul>
                        <li>Địa chỉ: 123 Đường ABC, Quận 1, TP.HCM</li>
                        <li>Điện thoại: 0123 456 789</li>
                        <li>Email: info@thanhphongsaygex.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2023 Thanh Phong Saygex AI. Tất cả các quyền được bảo lưu.
            </div>
        </div>
    </footer>

    <script>
        // Chatbot functionality
        document.getElementById('chatbotToggle').addEventListener('click', function() {
            const chatbotWindow = document.getElementById('chatbotWindow');
            chatbotWindow.style.display = chatbotWindow.style.display === 'flex' ? 'none' : 'flex';
        });

        document.getElementById('sendMessage').addEventListener('click', function() {
            sendMessage();
        });

        document.getElementById('chatInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });

        function sendMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (message) {
                // Add user message
                addMessage(message, 'user');
                
                // Clear input
                input.value = '';
                
                // Simulate AI response
                setTimeout(() => {
                    const responses = [
                        "Tôi có thể tư vấn cho bạn về các loại lọ thủy tinh, nhựa PET, lọ chuyên dụng và lọ mỹ phẩm. Bạn quan tâm đến loại nào?",
                        "Dựa trên nhu cầu của bạn, tôi đề xuất lọ thủy tinh cao cấp 50ml cho phòng thí nghiệm hoặc lọ nhựa PET 100ml cho đóng gói sản phẩm.",
                        "Chúng tôi có chính sách giao hàng nhanh trong 24h cho khu vực TP.HCM và 2-3 ngày cho các tỉnh thành khác.",
                        "Tất cả sản phẩm của chúng tôi đều được bảo hành 12 tháng và có chính sách đổi trả trong vòng 30 ngày.",
                        "Bạn có muốn kết nối với nhân viên tư vấn của chúng tôi qua video call không? Tôi có thể sắp xếp ngay bây giờ."
                    ];
                    
                    const randomResponse = responses[Math.floor(Math.random() * responses.length)];
                    addMessage(randomResponse, 'bot');
                }, 1000);
            }
        }

        function addMessage(text, sender) {
            const chatbotBody = document.getElementById('chatbotBody');
            const messageDiv = document.createElement('div');
            messageDiv.classList.add('message');
            messageDiv.classList.add(sender === 'user' ? 'user-message' : 'bot-message');
            messageDiv.textContent = text;
            
            chatbotBody.appendChild(messageDiv);
            chatbotBody.scrollTop = chatbotBody.scrollHeight;
        }

        // AI Controls
        document.getElementById('voiceControl').addEventListener('click', function() {
            this.classList.toggle('active');
            if (this.classList.contains('active')) {
                alert("Tính năng nhận diện giọng nói đã được kích hoạt. Bạn có thể nói chuyện với trợ lý AI.");
            } else {
                alert("Tính năng nhận diện giọng nói đã tắt.");
            }
        });

        document.getElementById('cameraControl').addEventListener('click', function() {
            this.classList.toggle('active');
            if (this.classList.contains('active')) {
                alert("Camera AI đã được kích hoạt. Bạn có thể sử dụng camera để nhận diện sản phẩm.");
            } else {
                alert("Camera AI đã tắt.");
            }
        });

        document.getElementById('videoCall').addEventListener('click', function() {
            alert("Kết nối với nhân viên tư vấn... Cuộc gọi video sẽ bắt đầu sau 3 giây.");
            // Simulate video call starting
            setTimeout(() => {
                alert("Cuộc gọi video đã được kết nối. Xin chào, tôi là Mỹ Ruby, tư vấn viên của Thanh Phong Saygex. Tôi có thể giúp gì cho bạn?");
            }, 3000);
        });

        document.getElementById('toggleCamera').addEventListener('click', function() {
            const cameraPlaceholder = document.querySelector('.camera-placeholder');
            if (cameraPlaceholder.innerHTML.includes('đang tắt')) {
                cameraPlaceholder.innerHTML = `
                    <div style="background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%); width: 100%; height: 100%; display: flex; align-items: center; justify-content: center; color: white;">
                        <div style="text-align: center;">
                            <i class="fas fa-eye" style="font-size: 4rem;"></i>
                            <p>Camera AI đang hoạt động</p>
                            <p style="font-size: 0.8rem; margin-top: 10px;">Đưa sản phẩm vào khung hình để nhận diện</p>
                        </div>
                    </div>
                `;
                this.textContent = "Tắt Camera";
                
                // Simulate product recognition after 2 seconds
                setTimeout(() => {
                    alert("Camera AI đã nhận diện được sản phẩm: Lọ thủy tinh cao cấp 50ml. Đang hiển thị thông tin chi tiết...");
                }, 2000);
            } else {
                cameraPlaceholder.innerHTML = `
                    <i class="fas fa-camera" style="font-size: 4rem;"></i>
                    <p>Camera đang tắt</p>
                    <button class="btn" style="margin-top: 15px;">Bật Camera</button>
                `;
                this.textContent = "Bật Camera";
                
                // Re-attach event listener to the new button
                document.querySelector('.camera-placeholder button').addEventListener('click', function() {
                    document.getElementById('toggleCamera').click();
                });
            }
        });

        document.getElementById('startAI').addEventListener('click', function() {
            alert("Hệ thống AI đang được khởi động...\n\nTrợ lý ảo Mỹ Ruby: 'Xin chào! Tôi là trợ lý AI của Thanh Phong Saygex. Tôi có thể giúp gì cho bạn hôm nay?'");
            
            // Auto-open chatbot
            document.getElementById('chatbotWindow').style.display = 'flex';
        });
    </script>
</body>
</html>

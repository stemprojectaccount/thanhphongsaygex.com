<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hệ thống lọ - Thanh Phong Saygex</title>
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
                    <h1>Thanh Phong Saygex</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#">Trang chủ</a></li>
                        <li><a href="#">Hệ thống lọ</a></li>
                        <li><a href="#">Dịch vụ</a></li>
                        <li><a href="#">Liên hệ</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>Hệ thống lọ Thanh Phong Saygex</h2>
            <p>Chuyên cung cấp các loại lọ chất lượng cao, đa dạng kích thước và mẫu mã phục vụ cho nghiên cứu và sản xuất</p>
            <a href="#" class="btn">Khám phá ngay</a>
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
                        <div class="feature-icon">✅</div>
                        <h3>Chất lượng đảm bảo</h3>
                        <p>Tất cả sản phẩm đều được kiểm tra chất lượng nghiêm ngặt trước khi giao đến tay khách hàng.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">🚚</div>
                        <h3>Giao hàng nhanh</h3>
                        <p>Hệ thống giao hàng toàn quốc với thời gian nhanh chóng, đảm bảo đúng hẹn.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">💲</div>
                        <h3>Giá cả cạnh tranh</h3>
                        <p>Giá thành hợp lý, cạnh tranh nhất thị trường với chất lượng đảm bảo.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">🛠️</div>
                        <h3>Hỗ trợ kỹ thuật</h3>
                        <p>Đội ngũ kỹ thuật viên chuyên nghiệp sẵn sàng hỗ trợ 24/7.</p>
                    </div>
                </div>
            </div>
        </section>
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
                    <h3>Hỗ trợ</h3>
                    <ul>
                        <li><a href="#">Hướng dẫn mua hàng</a></li>
                        <li><a href="#">Chính sách bảo hành</a></li>
                        <li><a href="#">Câu hỏi thường gặp</a></li>
                        <li><a href="#">Liên hệ</a></li>
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
                &copy; 2023 Thanh Phong Saygex. Tất cả các quyền được bảo lưu.
            </div>
        </div>
    </footer>
</body>
</html>

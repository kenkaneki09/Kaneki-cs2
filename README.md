# Kaneki-cs2
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Kaneki CS2 Free Skins</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 480px;
            margin: 0 auto;
            padding: 16px;
        }
        
        /* Header */
        .header {
            text-align: center;
            padding: 20px 0;
            border-bottom: 2px solid #e94560;
            margin-bottom: 20px;
            position: relative;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            background: linear-gradient(45deg, #e94560, #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 0 0 30px rgba(233, 69, 96, 0.5);
        }
        
        .admin-badge {
            display: inline-block;
            background: #e94560;
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            margin-top: 8px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        
        .admin-badge:active {
            transform: scale(0.95);
        }
        
        /* Stats Bar */
        .stats-bar {
            display: flex;
            justify-content: space-between;
            gap: 12px;
            margin-bottom: 20px;
        }
        
        .stat-card {
            flex: 1;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            padding: 16px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            transition: left 0.5s;
        }
        
        .stat-card:hover::before {
            left: 100%;
        }
        
        .stat-icon {
            font-size: 24px;
            margin-bottom: 4px;
        }
        
        .stat-value {
            font-size: 24px;
            font-weight: bold;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        
        .stat-label {
            font-size: 12px;
            color: #aaa;
            margin-top: 4px;
        }
        
        /* Daily Reward */
        .daily-reward {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }
        
        .daily-reward.claimed {
            background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
        }
        
        .daily-reward h3 {
            font-size: 18px;
            margin-bottom: 8px;
        }
        
        .reward-amount {
            font-size: 32px;
            font-weight: bold;
            margin: 10px 0;
        }
        
        .claim-btn {
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.3);
            color: white;
            padding: 12px 32px;
            border-radius: 25px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            backdrop-filter: blur(10px);
        }
        
        .claim-btn:active {
            transform: scale(0.95);
        }
        
        .claim-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }
        
        .streak-info {
            font-size: 12px;
            margin-top: 8px;
            opacity: 0.9;
        }
        
        /* Navigation */
        .nav-tabs {
            display: flex;
            gap: 8px;
            margin-bottom: 20px;
            overflow-x: auto;
            padding-bottom: 8px;
        }
        
        .nav-tab {
            flex: 1;
            min-width: 80px;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: #aaa;
            padding: 12px 8px;
            border-radius: 12px;
            font-size: 12px;
            cursor: pointer;
            transition: all 0.3s;
            white-space: nowrap;
        }
        
        .nav-tab.active {
            background: #e94560;
            color: white;
            box-shadow: 0 4px 15px rgba(233, 69, 96, 0.4);
        }
        
        /* Shop Grid */
        .shop-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 80px;
        }
        
        .skin-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }
        
        .skin-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(233, 69, 96, 0.3);
        }
        
        .skin-image {
            width: 100%;
            height: 120px;
            background: linear-gradient(135deg, #2d3561 0%, #1a1f3d 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            position: relative;
            overflow: hidden;
        }
        
        .skin-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .skin-rarity {
            position: absolute;
            top: 8px;
            right: 8px;
            padding: 4px 8px;
            border-radius: 8px;
            font-size: 10px;
            font-weight: bold;
            text-transform: uppercase;
        }
        
        .rarity-covert { background: #eb4b4b; color: white; }
        .rarity-classified { background: #d32ce6; color: white; }
        .rarity-restricted { background: #8847ff; color: white; }
        .rarity-mil-spec { background: #4b69ff; color: white; }
        
        .skin-info {
            padding: 12px;
        }
        
        .skin-name {
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 4px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .skin-weapon {
            font-size: 12px;
            color: #888;
            margin-bottom: 8px;
        }
        
        .skin-price {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .price-tag {
            display: flex;
            align-items: center;
            gap: 4px;
            color: #ffd700;
            font-weight: bold;
        }
        
        .buy-btn {
            background: #e94560;
            color: white;
            border: none;
            padding: 6px 16px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .buy-btn:active {
            transform: scale(0.95);
        }
        
        .buy-btn:disabled {
            background: #444;
            cursor: not-allowed;
        }
        
        /* Buy Coins Section */
        .buy-coins-section {
            display: none;
            text-align: center;
            padding: 20px 0;
        }
        
        .coin-package {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 24px;
            margin: 12px 0;
            border: 2px solid #ffd700;
            position: relative;
            overflow: hidden;
        }
        
        .coin-package::before {
            content: '⭐';
            position: absolute;
            top: -10px;
            right: -10px;
            font-size: 60px;
            opacity: 0.1;
        }
        
        .package-coins {
            font-size: 36px;
            color: #ffd700;
            font-weight: bold;
            margin-bottom: 8px;
        }
        
        .package-price {
            font-size: 24px;
            color: #fff;
            margin-bottom: 16px;
        }
        
        .buy-package-btn {
            background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
            color: #000;
            border: none;
            padding: 16px 48px;
            border-radius: 30px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s;
            box-shadow: 0 4px 20px rgba(255, 215, 0, 0.4);
        }
        
        .buy-package-btn:active {
            transform: scale(0.95);
        }
        
        /* Admin Panel */
        .admin-panel {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.95);
            z-index: 1000;
            overflow-y: auto;
            padding: 20px;
        }
        
        .admin-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 2px solid #e94560;
        }
        
        .close-admin {
            background: #e94560;
            border: none;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            font-size: 20px;
            cursor: pointer;
        }
        
        .admin-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            padding: 20px;
            margin-bottom: 20px;
        }
        
        .admin-section h3 {
            color: #e94560;
            margin-bottom: 16px;
        }
        
        .edit-item {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 12px;
        }
        
        .edit-item input, .edit-item select {
            width: 100%;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: white;
            padding: 10px;
            border-radius: 8px;
            margin-top: 8px;
            font-size: 14px;
        }
        
        .save-btn {
            background: #4CAF50;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            margin-top: 12px;
        }
        
        .add-ad-btn {
            background: #2196F3;
            color: white;
            border: none;
            padding: 16px;
            border-radius: 12px;
            width: 100%;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            margin-bottom: 12px;
        }
        
        /* Ad Banner */
        .ad-banner {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%);
            border-radius: 16px;
            padding: 16px;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            display: none;
        }
        
        .ad-banner.show {
            display: block;
            animation: slideIn 0.5s ease;
        }
        
        @keyframes slideIn {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        .ad-label {
            position: absolute;
            top: 8px;
            left: 8px;
            background: rgba(0,0,0,0.5);
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 10px;
        }
        
        .ad-content {
            font-weight: bold;
            font-size: 16px;
        }
        
        /* Bottom Nav */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(20px);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            justify-content: space-around;
            padding: 12px 0;
            z-index: 100;
        }
        
        .bottom-btn {
            background: none;
            border: none;
            color: #888;
            font-size: 12px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 4px;
            cursor: pointer;
            transition: color 0.3s;
        }
        
        .bottom-btn.active {
            color: #e94560;
        }
        
        .bottom-btn i {
            font-size: 24px;
        }
        
        /* Toast Notification */
        .toast {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            background: rgba(0, 0, 0, 0.9);
            color: white;
            padding: 20px 40px;
            border-radius: 16px;
            font-size: 18px;
            font-weight: bold;
            z-index: 2000;
            transition: transform 0.3s;
            border: 2px solid #e94560;
        }
        
        .toast.show {
            transform: translate(-50%, -50%) scale(1);
        }
        
        /* Inventory Section */
        .inventory-section {
            display: none;
        }
        
        .empty-inventory {
            text-align: center;
            padding: 60px 20px;
            color: #888;
        }
        
        .empty-icon {
            font-size: 64px;
            margin-bottom: 16px;
            opacity: 0.5;
        }
        
        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .floating {
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes shine {
            0% { background-position: -200% center; }
            100% { background-position: 200% center; }
        }
        
        .shiny {
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            background-size: 200% 100%;
            animation: shine 2s infinite;
        }
        
        /* Responsive */
        @media (max-width: 380px) {
            .shop-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="logo">🔥 KANEKI CS2 🔥</div>
            <div class="admin-badge" onclick="openAdmin()">👤 @kaneki_prime</div>
        </div>
        
        <!-- Ad Banner (Admin can edit) -->
        <div class="ad-banner" id="adBanner">
            <span class="ad-label">REKLAMA</span>
            <div class="ad-content" id="adText">🎁 Yangi skinlar qo'shildi! Tezroq tekshiring!</div>
        </div>
        
        <!-- Stats -->
        <div class="stats-bar">
            <div class="stat-card">
                <div class="stat-icon">🪙</div>
                <div class="stat-value" id="coinBalance">0</div>
                <div class="stat-label">Coinlar</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon">📦</div>
                <div class="stat-value" id="skinCount">0</div>
                <div class="stat-label">Skinlar</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon">🔥</div>
                <div class="stat-value" id="streakDays">0</div>
                <div class="stat-label">Kunlik</div>
            </div>
        </div>
        
        <!-- Daily Reward -->
        <div class="daily-reward" id="dailyReward">
            <h3>🎁 Kunlik Bonus</h3>
            <div class="reward-amount" id="rewardAmount">+50</div>
            <button class="claim-btn" id="claimBtn" onclick="claimDaily()">OLISH</button>
            <div class="streak-info" id="streakInfo">Ketma-ketlik: 1-kun | Hafta oxirigacha: 300 coin</div>
        </div>
        
        <!-- Navigation Tabs -->
        <div class="nav-tabs" id="categoryTabs">
            <button class="nav-tab active" onclick="filterSkins('all')">Barchasi</button>
            <button class="nav-tab" onclick="filterSkins('knife')">🔪 Pichoq</button>
            <button class="nav-tab" onclick="filterSkins('rifle')">🔫 Vintovka</button>
            <button class="nav-tab" onclick="filterSkins('pistol')">🔫 Pistolet</button>
            <button class="nav-tab" onclick="filterSkins('gloves')">🧤 Qo'lqop</button>
        </div>
        
        <!-- Shop Section -->
        <div class="shop-section" id="shopSection">
            <div class="shop-grid" id="shopGrid">
                <!-- Skins will be loaded here -->
            </div>
        </div>
        
        <!-- Buy Coins Section -->
        <div class="buy-coins-section" id="buyCoinsSection">
            <div class="coin-package">
                <div class="package-coins">25,000 🪙</div>
                <div class="package-price">100 ⭐ Telegram Stars</div>
                <button class="buy-package-btn" onclick="buyCoins()">SOTIB OLISH</button>
            </div>
            <p style="color: #888; margin-top: 20px; font-size: 14px;">
                💡 Coinlar orqali bepul skinlarni olishingiz mumkin!
            </p>
        </div>
        
        <!-- Inventory Section -->
        <div class="inventory-section" id="inventorySection">
            <div class="empty-inventory" id="emptyInventory">
                <div class="empty-icon">📭</div>
                <h3>Hali skin yo'q</h3>
                <p>Do'kondan skin sotib oling!</p>
            </div>
            <div class="shop-grid" id="inventoryGrid" style="display: none;"></div>
        </div>
    </div>
    
    <!-- Bottom Navigation -->
    <div class="bottom-nav">
        <button class="bottom-btn active" onclick="showSection('shop')">
            <span>🛒</span>
            <span>Do'kon</span>
        </button>
        <button class="bottom-btn" onclick="showSection('coins')">
            <span>💰</span>
            <span>Coin</span>
        </button>
        <button class="bottom-btn" onclick="showSection('inventory')">
            <span>🎒</span>
            <span>Inventar</span>
        </button>
    </div>
    
    <!-- Admin Panel -->
    <div class="admin-panel" id="adminPanel">
        <div class="admin-header">
    

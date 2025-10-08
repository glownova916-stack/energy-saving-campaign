
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Energy Saving Campaign - Rayat Shikshan Sanstha</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c5aa0;
            --secondary: #4CAF50;
            --accent: #FFC107;
            --light: #f8f9fa;
            --dark: #343a40;
            --danger: #dc3545;
            --success: #28a745;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary) 0%, #1e4080 100%);
            color: white;
            padding: 1rem;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        .floating-bulbs {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
        }
        
        .bulb {
            position: absolute;
            font-size: 1.5rem;
            opacity: 0.7;
            animation: float 6s infinite ease-in-out;
        }
        
        .bulb:nth-child(1) { top: 10%; left: 5%; animation-delay: 0s; }
        .bulb:nth-child(2) { top: 20%; left: 90%; animation-delay: 1s; }
        .bulb:nth-child(3) { top: 70%; left: 15%; animation-delay: 2s; }
        .bulb:nth-child(4) { top: 60%; left: 85%; animation-delay: 3s; }
        .bulb:nth-child(5) { top: 40%; left: 50%; animation-delay: 4s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
        }
        
        .logo {
            width: 80px;
            height: 80px;
            background-color: white;
            border-radius: 50%;
            margin-right: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: var(--primary);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .institution-name {
            font-size: 1.2rem;
            font-weight: bold;
        }
        
        .project-title {
            font-size: 2.2rem;
            margin: 1rem 0;
            color: var(--accent);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: glow 2s infinite alternate;
        }
        
        @keyframes glow {
            from { text-shadow: 0 0 10px rgba(255, 193, 7, 0.5); }
            to { text-shadow: 0 0 20px rgba(255, 193, 7, 0.8); }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .card {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            padding: 1.5rem;
            margin-bottom: 2rem;
            transition: transform 0.3s, box-shadow 0.3s;
            overflow: hidden;
            position: relative;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 20px rgba(0,0,0,0.15);
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: var(--secondary);
        }
        
        h2 {
            color: var(--primary);
            margin-bottom: 1rem;
            border-bottom: 2px solid var(--accent);
            padding-bottom: 0.5rem;
            display: flex;
            align-items: center;
        }
        
        h2 i {
            margin-right: 10px;
            color: var(--secondary);
        }
        
        h3 {
            color: var(--secondary);
            margin: 1rem 0 0.5rem;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
            position: relative;
        }
        
        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--primary);
        }
        
        input, select {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        input:focus, select:focus {
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.2);
            outline: none;
        }
        
        .input-icon {
            position: absolute;
            right: 15px;
            top: 40px;
            color: var(--primary);
        }
        
        button {
            background: linear-gradient(135deg, var(--secondary) 0%, #3d8b40 100%);
            color: white;
            border: none;
            padding: 0.9rem 1.8rem;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }
        
        button i {
            margin-right: 8px;
        }
        
        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }
        
        .btn-secondary {
            background: linear-gradient(135deg, var(--primary) 0%, #1e4080 100%);
        }
        
        .btn-secondary:hover {
            background: linear-gradient(135deg, #1e4080 0%, var(--primary) 100%);
        }
        
        .btn-danger {
            background: linear-gradient(135deg, var(--danger) 0%, #c82333 100%);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            border-radius: 8px;
            overflow: hidden;
        }
        
        th, td {
            padding: 0.75rem 1rem;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        th {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
        }
        
        tr:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        tr:hover {
            background-color: #e9f7e9;
        }
        
        .bulb-comparison {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin: 1.5rem 0;
            gap: 1rem;
        }
        
        .bulb-type {
            flex: 1;
            min-width: 200px;
            margin: 0.5rem;
            padding: 1.5rem 1rem;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .bulb-type:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }
        
        .bulb-type::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
        }
        
        .incandescent {
            background: linear-gradient(135deg, #ffebee 0%, #ffcdd2 100%);
            border-top: 4px solid #f44336;
        }
        
        .incandescent::after {
            background: #f44336;
        }
        
        .halogen {
            background: linear-gradient(135deg, #fff3e0 0%, #ffe0b2 100%);
            border-top: 4px solid #ff9800;
        }
        
        .halogen::after {
            background: #ff9800;
        }
        
        .cfl {
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%);
            border-top: 4px solid #4caf50;
        }
        
        .cfl::after {
            background: #4caf50;
        }
        
        .led {
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
            border-top: 4px solid #2196f3;
        }
        
        .led::after {
            background: #2196f3;
        }
        
        .bulb-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .energy-saving-tips {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .tip {
            background-color: white;
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-left: 5px solid var(--secondary);
            transition: all 0.3s;
            display: flex;
            align-items: flex-start;
        }
        
        .tip:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }
        
        .tip-icon {
            font-size: 1.8rem;
            color: var(--secondary);
            margin-right: 1rem;
            flex-shrink: 0;
        }
        
        .results {
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%);
            padding: 1.5rem;
            border-radius: 12px;
            margin-top: 1rem;
            border-left: 5px solid var(--success);
            animation: fadeIn 0.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .highlight {
            font-weight: bold;
            color: var(--primary);
            font-size: 1.1rem;
        }
        
        .data-section {
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
            padding: 1.5rem;
            border-radius: 12px;
            margin-top: 1rem;
            border-left: 5px solid var(--primary);
        }
        
        .data-table {
            max-height: 400px;
            overflow-y: auto;
            margin: 1rem 0;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        .savings-animation {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 1.5rem 0;
            height: 100px;
            position: relative;
        }
        
        .money-bag, .co2-cloud {
            font-size: 3rem;
            margin: 0 1rem;
            position: relative;
            z-index: 2;
        }
        
        .money-bag {
            color: #ffc107;
            animation: bounce 2s infinite;
        }
        
        .co2-cloud {
            color: #6c757d;
            animation: bounce 2s infinite 0.5s;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        .arrow {
            font-size: 2rem;
            color: var(--secondary);
            animation: pulse 1.5s infinite;
        }
        
        .progress-bar {
            height: 10px;
            background-color: #e9ecef;
            border-radius: 5px;
            margin: 1rem 0;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(90deg, var(--secondary) 0%, #8bc34a 100%);
            border-radius: 5px;
            transition: width 1s ease-in-out;
        }
        
        footer {
            background: linear-gradient(135deg, var(--dark) 0%, #23272b 100%);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }
        
        .counter {
            display: flex;
            justify-content: space-around;
            margin: 2rem 0;
            flex-wrap: wrap;
        }
        
        .counter-item {
            text-align: center;
            padding: 1rem;
        }
        
        .counter-value {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--secondary);
            display: block;
        }
        
        .counter-label {
            font-size: 1rem;
            color: var(--dark);
        }
        
        @media (max-width: 768px) {
            .bulb-comparison {
                flex-direction: column;
            }
            
            .bulb-type {
                min-width: 100%;
            }
            
            .project-title {
                font-size: 1.8rem;
            }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background-color: var(--accent);
            opacity: 0;
            z-index: 1000;
            pointer-events: none;
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 1001;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 2rem;
            border-radius: 12px;
            max-width: 500px;
            width: 90%;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            animation: modalFadeIn 0.3s;
        }
        
        @keyframes modalFadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
        
        .close-modal {
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark);
        }
    </style>
</head>
<body>
    <header>
        <div class="floating-bulbs">
            <div class="bulb">💡</div>
            <div class="bulb">💡</div>
            <div class="bulb">💡</div>
            <div class="bulb">💡</div>
            <div class="bulb">💡</div>
        </div>
        <div class="logo-container">
            <div class="logo">RSS</div>
            <div>
                <div class="institution-name">Rayat Shikshan Sanstha's</div>
                <div class="institution-name">R.B. Narayanrao Borawake College, Shrirampur (Autonomous)</div>
            </div>
        </div>
        <h1 class="project-title">Energy Saving Campaign</h1>
        <p>Field Project - S.Y.U.G | Academic Year (2025-26)</p>
    </header>

    <div class="container">
        <div class="card">
            <h2><i class="fas fa-lightbulb"></i> About the Project</h2>
            <p>This energy saving campaign aims to educate people about the benefits of switching to energy-efficient lighting solutions. By calculating your current energy consumption and comparing it with more efficient options, you can see how much energy and money you could save.</p>
            
            <div class="energy-saving-tips">
                <div class="tip">
                    <div class="tip-icon"><i class="fas fa-exchange-alt"></i></div>
                    <div>
                        <h3>Switch to Efficient Bulbs</h3>
                        <p>Replace incandescent bulbs with CFLs or LEDs to save up to 80% on lighting energy.</p>
                    </div>
                </div>
                <div class="tip">
                    <div class="tip-icon"><i class="fas fa-power-off"></i></div>
                    <div>
                        <h3>Turn Off Lights</h3>
                        <p>Always shut off lighting when exiting a room to save energy.</p>
                    </div>
                </div>
                <div class="tip">
                    <div class="tip-icon"><i class="fas fa-sun"></i></div>
                    <div>
                        <h3>Use Natural Light</h3>
                        <p>Open blinds or curtains during the day to utilize natural light whenever possible.</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="card">
            <h2><i class="fas fa-calculator"></i> Calculate Your Energy Usage</h2>
            <form id="energyForm">
                <div class="form-group">
                    <label for="userName"><i class="fas fa-user"></i> Name of User:</label>
                    <input type="text" id="userName" required placeholder="Enter your full name">
                    <div class="input-icon"><i class="fas fa-user-check"></i></div>
                </div>
                
                <div class="form-group">
                    <label for="userAddress"><i class="fas fa-home"></i> Address:</label>
                    <input type="text" id="userAddress" required placeholder="Enter your complete address">
                    <div class="input-icon"><i class="fas fa-map-marker-alt"></i></div>
                </div>
                
                <div class="form-group">
                    <label for="userMobile"><i class="fas fa-mobile-alt"></i> Mobile No:</label>
                    <input type="tel" id="userMobile" required placeholder="Enter your 10-digit mobile number">
                    <div class="input-icon"><i class="fas fa-phone"></i></div>
                </div>
                
                <h3><i class="fas fa-lightbulb"></i> Lighting Information</h3>
                
                <div class="form-group">
                    <label for="bulbType">Type of Bulb:</label>
                    <select id="bulbType" required>
                        <option value="">Select Bulb Type</option>
                        <option value="incandescent">Incandescent</option>
                        <option value="halogen">Halogen</option>
                        <option value="cfl">CFL</option>
                        <option value="led">LED</option>
                        <option value="tube">Tube Light</option>
                    </select>
                    <div class="input-icon"><i class="fas fa-chevron-down"></i></div>
                </div>
                
                <div class="form-group">
                    <label for="bulbCount">Number of Bulbs/Tube Lights:</label>
                    <input type="number" id="bulbCount" min="1" required placeholder="e.g., 5">
                    <div class="input-icon"><i class="fas fa-list-ol"></i></div>
                </div>
                
                <div class="form-group">
                    <label for="bulbWattage">Wattage of Bulb/Tube:</label>
                    <input type="number" id="bulbWattage" min="1" required placeholder="e.g., 60">
                    <div class="input-icon"><i class="fas fa-bolt"></i></div>
                </div>
                
                <div class="form-group">
                    <label for="hoursPerDay">Hours of Use per Day:</label>
                    <input type="number" id="hoursPerDay" min="0" max="24" step="0.5" required placeholder="e.g., 6.5">
                    <div class="input-icon"><i class="fas fa-clock"></i></div>
                </div>
                
                <button type="submit"><i class="fas fa-calculator"></i> Calculate Energy Usage</button>
                <button type="button" id="saveDataBtn" class="btn-secondary"><i class="fas fa-save"></i> Save User Data</button>
                <button type="button" id="resetFormBtn" class="btn-danger"><i class="fas fa-redo"></i> Reset Form</button>
            </form>
        </div>

        <div class="card">
            <h2><i class="fas fa-chart-line"></i> Energy Calculation Results</h2>
            <div id="resultsContainer" class="results">
                <p>Fill out the form above to see your energy usage and potential savings.</p>
            </div>
            
            <div class="savings-animation" id="savingsAnimation" style="display: none;">
                <div class="money-bag">💰</div>
                <div class="arrow">➡️</div>
                <div class="co2-cloud">☁️</div>
            </div>
            
            <h3><i class="fas fa-balance-scale"></i> Bulb Comparison</h3>
            <div class="bulb-comparison">
                <div class="bulb-type incandescent">
                    <div class="bulb-icon">💡</div>
                    <h4>Incandescent</h4>
                    <p>60W = 0.06 kW</p>
                    <p>Life: 1,000 hours</p>
                    <p>Efficiency: Low</p>
                </div>
                <div class="bulb-type halogen">
                    <div class="bulb-icon">💡</div>
                    <h4>Halogen</h4>
                    <p>43W = 0.043 kW</p>
                    <p>Life: 3,000 hours</p>
                    <p>Efficiency: Medium</p>
                </div>
                <div class="bulb-type cfl">
                    <div class="bulb-icon">💡</div>
                    <h4>CFL</h4>
                    <p>13W = 0.013 kW</p>
                    <p>Life: 10,000 hours</p>
                    <p>Efficiency: High</p>
                </div>
                <div class="bulb-type led">
                    <div class="bulb-icon">💡</div>
                    <h4>LED</h4>
                    <p>12W = 0.012 kW</p>
                    <p>Life: 25,000 hours</p>
                    <p>Efficiency: Very High</p>
                </div>
            </div>
            
            <h3><i class="fas fa-info-circle"></i> Did You Know?</h3>
            <p>Only 10% of the energy used by a traditional incandescent bulb produces light, the rest is given off as heat. This makes them highly inefficient compared to modern alternatives.</p>
            
            <div class="counter">
                <div class="counter-item">
                    <span class="counter-value" id="treesSaved">0</span>
                    <span class="counter-label">Trees Saved</span>
                </div>
                <div class="counter-item">
                    <span class="counter-value" id="moneySaved">0</span>
                    <span class="counter-label">Money Saved (₹)</span>
                </div>
                <div class="counter-item">
                    <span class="counter-value" id="co2Reduced">0</span>
                    <span class="counter-label">CO₂ Reduced (kg)</span>
                </div>
            </div>
        </div>

        <div class="card">
            <h2><i class="fas fa-database"></i> Access User Data</h2>
            <div class="data-section">
                <p>As an administrator, you can access user data in several ways:</p>
                
                <h3><i class="fas fa-eye"></i> 1. View All User Data</h3>
                <button id="viewDataBtn" class="btn-secondary"><i class="fas fa-table"></i> View All User Data</button>
                
                <h3><i class="fas fa-file-csv"></i> 2. Export Data to CSV</h3>
                <button id="exportCsvBtn" class="btn-secondary"><i class="fas fa-download"></i> Export to CSV</button>
                
                <h3><i class="fas fa-print"></i> 3. Print User Data</h3>
                <button id="printDataBtn" class="btn-secondary"><i class="fas fa-print"></i> Print Data</button>
                
                <div id="userDataContainer" class="data-table" style="display: none;">
                    <h3>Stored User Data</h3>
                    <table id="userDataTable">
                        <thead>
                            <tr>
                                <th>Name</th>
                                <th>Address</th>
                                <th>Mobile</th>
                                <th>Bulb Type</th>
                                <th>Bulb Count</th>
                                <th>Wattage</th>
                                <th>Hours/Day</th>
                                <th>Annual Cost</th>
                                <th>Date</th>
                            </tr>
                        </thead>
                        <tbody id="userDataBody">
                            <!-- User data will be populated here -->
                        </tbody>
                    </table>
                </div>
            </div>
        </div>

        <div class="card">
            <h2><i class="fas fa-money-bill-wave"></i> Electricity Rates</h2>
            <table>
                <thead>
                    <tr>
                        <th>Units (kWh)</th>
                        <th>Rate (in rupees)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>1 to 100</td>
                        <td>4.16</td>
                    </tr>
                    <tr>
                        <td>101 to 300</td>
                        <td>7.91</td>
                    </tr>
                    <tr>
                        <td>301 to 500</td>
                        <td>10.87</td>
                    </tr>
                    <tr>
                        <td>501 to 1000</td>
                        <td>12.35</td>
                    </tr>
                    <tr>
                        <td>1000 and above</td>
                        <td>13.63</td>
                    </tr>
                </tbody>
            </table>
            <p>Note: 1 Unit = 1 kWh</p>
        </div>
    </div>

    <div id="successModal" class="modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h2><i class="fas fa-check-circle" style="color: var(--success); font-size: 3rem;"></i></h2>
            <h3>Data Saved Successfully!</h3>
            <p>Your energy usage data has been saved to our database.</p>
            <p>Thank you for participating in our Energy Saving Campaign!</p>
            <button class="btn-secondary" id="closeModalBtn">OK</button>
        </div>
    </div>

    <footer>
        <p>Rayat Shikshan Sanstha's R.B. Narayanrao Borawake College, Shrirampur (Autonomous)</p>
        <p>Energy Saving Campaign - Field Project S.Y.U.G | Academic Year (2025-26)</p>
    </footer>

    <script>
        // Store user data in localStorage
        let userData = JSON.parse(localStorage.getItem('energyUserData')) || [];
        
        // Initialize counters
        let treesSaved = 0;
        let moneySaved = 0;
        let co2Reduced = 0;
        
        // Update counters based on saved data
        userData.forEach(data => {
            moneySaved += data.annualSavings || 0;
            co2Reduced += data.co2Reduction || 0;
        });
        
        // Calculate trees saved (approx 1 tree per 20kg CO2)
        treesSaved = Math.floor(co2Reduced / 20);
        
        // Update counter displays
        document.getElementById('treesSaved').textContent = treesSaved;
        document.getElementById('moneySaved').textContent = Math.round(moneySaved);
        document.getElementById('co2Reduced').textContent = Math.round(co2Reduced);
        
        // Animate counters
        animateCounter('treesSaved', 0, treesSaved, 1500);
        animateCounter('moneySaved', 0, Math.round(moneySaved), 1500);
        animateCounter('co2Reduced', 0, Math.round(co2Reduced), 1500);
        
        document.getElementById('energyForm').addEventListener('submit', function(e) {
            e.preventDefault();
            calculateEnergyUsage();
        });
        
        document.getElementById('saveDataBtn').addEventListener('click', function() {
            saveUserData();
        });
        
        document.getElementById('resetFormBtn').addEventListener('click', function() {
            document.getElementById('energyForm').reset();
            document.getElementById('resultsContainer').innerHTML = '<p>Fill out the form above to see your energy usage and potential savings.</p>';
            document.getElementById('savingsAnimation').style.display = 'none';
        });
        
        document.getElementById('viewDataBtn').addEventListener('click', function() {
            displayUserData();
        });
        
        document.getElementById('exportCsvBtn').addEventListener('click', function() {
            exportToCSV();
        });
        
        document.getElementById('printDataBtn').addEventListener('click', function() {
            printUserData();
        });
        
        document.querySelector('.close-modal').addEventListener('click', function() {
            document.getElementById('successModal').style.display = 'none';
        });
        
        document.getElementById('closeModalBtn').addEventListener('click', function() {
            document.getElementById('successModal').style.display = 'none';
        });
        
        // Close modal when clicking outside
        window.addEventListener('click', function(e) {
            if (e.target === document.getElementById('successModal')) {
                document.getElementById('successModal').style.display = 'none';
            }
        });
        
        function calculateEnergyUsage() {
            // Get form values
            const userName = document.getElementById('userName').value;
            const userAddress = document.getElementById('userAddress').value;
            const userMobile = document.getElementById('userMobile').value;
            const bulbType = document.getElementById('bulbType').value;
            const bulbCount = parseInt(document.getElementById('bulbCount').value);
            const bulbWattage = parseInt(document.getElementById('bulbWattage').value);
            const hoursPerDay = parseFloat(document.getElementById('hoursPerDay').value);
            
            // Calculate energy usage
            const wattHoursPerDay = bulbWattage * bulbCount * hoursPerDay;
            const kWhPerDay = wattHoursPerDay / 1000;
            const kWhPerMonth = kWhPerDay * 30;
            const kWhPerYear = kWhPerDay * 365;
            
            // Calculate cost based on electricity rates
            let costPerYear = calculateElectricityCost(kWhPerYear);
            
            // Calculate potential savings with LED
            const ledWattage = 12; // Average LED wattage for equivalent brightness
            const ledWattHoursPerDay = ledWattage * bulbCount * hoursPerDay;
            const ledKWhPerDay = ledWattHoursPerDay / 1000;
            const ledKWhPerYear = ledKWhPerDay * 365;
            
            const ledCostPerYear = calculateElectricityCost(ledKWhPerYear);
            const annualSavings = costPerYear - ledCostPerYear;
            const co2Reduction = (kWhPerYear - ledKWhPerYear) * 0.7; // Approx. 0.7 kg CO2 per kWh
            
            // Display results
            const resultsContainer = document.getElementById('resultsContainer');
            resultsContainer.innerHTML = `
                <h3>Your Current Energy Usage</h3>
                <p>Daily Energy Consumption: <span class="highlight">${kWhPerDay.toFixed(2)} kWh</span></p>
                <p>Monthly Energy Consumption: <span class="highlight">${kWhPerMonth.toFixed(2)} kWh</span></p>
                <p>Annual Energy Consumption: <span class="highlight">${kWhPerYear.toFixed(2)} kWh</span></p>
                <p>Annual Electricity Cost: <span class="highlight">₹${costPerYear.toFixed(2)}</span></p>
                
                <h3>Potential Savings with LED Bulbs</h3>
                <p>Annual Energy with LED: <span class="highlight">${ledKWhPerYear.toFixed(2)} kWh</span></p>
                <p>Annual Cost with LED: <span class="highlight">₹${ledCostPerYear.toFixed(2)}</span></p>
                <p>Annual Savings: <span class="highlight">₹${annualSavings.toFixed(2)}</span></p>
                <p>CO2 Reduction: <span class="highlight">${co2Reduction.toFixed(2)} kg per year</span></p>
                
                <div class="progress-bar">
                    <div class="progress" style="width: ${(annualSavings/costPerYear*100).toFixed(0)}%"></div>
                </div>
                <p>You could save <span class="highlight">${(annualSavings/costPerYear*100).toFixed(0)}%</span> on your lighting costs by switching to LED bulbs!</p>
                
                <p><strong>Recommendation:</strong> Consider switching to LED bulbs to save money and reduce your environmental impact.</p>
            `;
            
            // Show savings animation
            document.getElementById('savingsAnimation').style.display = 'flex';
            
            // Store current calculation for potential saving
            window.currentCalculation = {
                userName, userAddress, userMobile, bulbType, bulbCount, bulbWattage, hoursPerDay,
                kWhPerYear, costPerYear, ledKWhPerYear, ledCostPerYear, annualSavings, co2Reduction, 
                date: new Date().toLocaleString()
            };
        }
        
        function calculateElectricityCost(kWh) {
            let cost = 0;
            let remainingUnits = kWh;
            
            if (remainingUnits > 1000) {
                cost += (remainingUnits - 1000) * 13.63;
                remainingUnits = 1000;
            }
            if (remainingUnits > 500) {
                cost += (remainingUnits - 500) * 12.35;
                remainingUnits = 500;
            }
            if (remainingUnits > 300) {
                cost += (remainingUnits - 300) * 10.87;
                remainingUnits = 300;
            }
            if (remainingUnits > 100) {
                cost += (remainingUnits - 100) * 7.91;
                remainingUnits = 100;
            }
            cost += remainingUnits * 4.16;
            
            return cost;
        }
        
        function saveUserData() {
            if (!window.currentCalculation) {
                alert("Please calculate energy usage first before saving data.");
                return;
            }
            
            // Add current calculation to userData array
            userData.push(window.currentCalculation);
            
            // Save to localStorage
            localStorage.setItem('energyUserData', JSON.stringify(userData));
            
            // Update counters
            moneySaved += window.currentCalculation.annualSavings;
            co2Reduced += window.currentCalculation.co2Reduction;
            treesSaved = Math.floor(co2Reduced / 20);
            
            // Update counter displays with animation
            animateCounter('treesSaved', parseInt(document.getElementById('treesSaved').textContent), treesSaved, 1000);
            animateCounter('moneySaved', parseInt(document.getElementById('moneySaved').textContent), Math.round(moneySaved), 1000);
            animateCounter('co2Reduced', parseInt(document.getElementById('co2Reduced').textContent), Math.round(co2Reduced), 1000);
            
            // Show success modal
            document.getElementById('successModal').style.display = 'flex';
            
            // Create confetti effect
            createConfetti();
        }
        
        function animateCounter(elementId, start, end, duration) {
            const element = document.getElementById(elementId);
            let startTimestamp = null;
            const step = (timestamp) => {
                if (!startTimestamp) startTimestamp = timestamp;
                const progress = Math.min((timestamp - startTimestamp) / duration, 1);
                const value = Math.floor(progress * (end - start) + start);
                element.textContent = value;
                if (progress < 1) {
                    window.requestAnimationFrame(step);
                }
            };
            window.requestAnimationFrame(step);
        }
        
        function createConfetti() {
            const colors = ['#f44336', '#e91e63', '#9c27b0', '#673ab7', '#3f51b5', '#2196f3', '#03a9f4', '#00bcd4', '#009688', '#4CAF50', '#8BC34A', '#CDDC39', '#FFEB3B', '#FFC107', '#FF9800', '#FF5722'];
            
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.top = '-10px';
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                document.body.appendChild(confetti);
                
                // Animate confetti
                const animation = confetti.animate([
                    { transform: `translateY(0) rotate(0deg)`, opacity: 1 },
                    { transform: `translateY(${window.innerHeight}px) rotate(${Math.random() * 360}deg)`, opacity: 0 }
                ], {
                    duration: 1000 + Math.random() * 2000,
                    easing: 'cubic-bezier(0.1, 0.8, 0.2, 1)'
                });
                
                // Remove confetti after animation
                animation.onfinish = () => {
                    confetti.remove();
                };
            }
        }
        
        function displayUserData() {
            const userDataContainer = document.getElementById('userDataContainer');
            const userDataBody = document.getElementById('userDataBody');
            
            if (userData.length === 0) {
                userDataBody.innerHTML = '<tr><td colspan="9" style="text-align: center;">No user data available</td></tr>';
            } else {
                userDataBody.innerHTML = '';
                userData.forEach((data, index) => {
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td>${data.userName}</td>
                        <td>${data.userAddress}</td>
                        <td>${data.userMobile}</td>
                        <td>${data.bulbType}</td>
                        <td>${data.bulbCount}</td>
                        <td>${data.bulbWattage}W</td>
                        <td>${data.hoursPerDay}</td>
                        <td>₹${data.costPerYear.toFixed(2)}</td>
                        <td>${data.date}</td>
                    `;
                    userDataBody.appendChild(row);
                });
            }
            
            userDataContainer.style.display = 'block';
        }
        
        function exportToCSV() {
            if (userData.length === 0) {
                alert("No data available to export.");
                return;
            }
            
            // Create CSV content
            let csvContent = "Name,Address,Mobile,Bulb Type,Bulb Count,Wattage,Hours per Day,Annual Cost,Date\n";
            
            userData.forEach(data => {
                csvContent += `"${data.userName}","${data.userAddress}","${data.userMobile}","${data.bulbType}",${data.bulbCount},${data.bulbWattage},${data.hoursPerDay},${data.costPerYear.toFixed(2)},"${data.date}"\n`;
            });
            
            // Create download link
            const encodedUri = encodeURI('data:text/csv;charset=utf-8,' + csvContent);
            const link = document.createElement("a");
            link.setAttribute("href", encodedUri);
            link.setAttribute("download", "energy_user_data.csv");
            document.body.appendChild(link);
            
            // Trigger download
            link.click();
            document.body.removeChild(link);
        }
        
        function printUserData() {
            if (userData.length === 0) {
                alert("No data available to print.");
                return;
            }
            
            // Create printable content
            let printContent = `
                <html>
                <head>
                    <title>Energy Saving Campaign - User Data</title>
                    <style>
                        body { font-family: Arial, sans-serif; }
                        table { width: 100%; border-collapse: collapse; }
                        th, td { border: 1px solid #ddd; padding: 8px; text-align: left; }
                        th { background-color: #f2f2f2; }
                    </style>
                </head>
                <body>
                    <h1>Energy Saving Campaign - User Data</h1>
                    <p>Rayat Shikshan Sanstha's R.B. Narayanrao Borawake College, Shrirampur (Autonomous)</p>
                    <table>
                        <thead>
                            <tr>
                                <th>Name</th>
                                <th>Address</th>
                                <th>Mobile</th>
                                <th>Bulb Type</th>
                                <th>Bulb Count</th>
                                <th>Wattage</th>
                                <th>Hours/Day</th>
                                <th>Annual Cost</th>
                                <th>Date</th>
                            </tr>
                        </thead>
                        <tbody>
            `;
            
            userData.forEach(data => {
                printContent += `
                    <tr>
                        <td>${data.userName}</td>
                        <td>${data.userAddress}</td>
                        <td>${data.userMobile}</td>
                        <td>${data.bulbType}</td>
                        <td>${data.bulbCount}</td>
                        <td>${data.bulbWattage}W</td>
                        <td>${data.hoursPerDay}</td>
                        <td>₹${data.costPerYear.toFixed(2)}</td>
                        <td>${data.date}</td>
                    </tr>
                `;
            });
            
            printContent += `
                        </tbody>
                    </table>
                </body>
                </html>
            `;
            
            // Open print window
            const printWindow = window.open('', '_blank');
            printWindow.document.write(printContent);
            printWindow.document.close();
            printWindow.print();
        }
    </script>
</body>
</html>

\\

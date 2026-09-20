# Homi-Cargo-Travel-Tour-
Cargo<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Homi Cargo & Travel | Flights, Air Cargo & Car Rentals</title>
  <style>
    /* Reset & Base Styles */
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
    html { scroll-behavior: smooth; }
    body { background-color: #f8f9fa; color: #333; line-height: 1.6; }
    
    /* Top Bar */
    .top-bar { background-color: #002244; color: #ffcc00; padding: 0.6rem 1.5rem; font-size: 0.85rem; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 0.5rem; }
    .top-bar a { color: #ffffff; text-decoration: none; margin-left: 0.5rem; }
    .top-bar a:hover { text-decoration: underline; color: #ffcc00; }
    
    /* Language Selector */
    .lang-select { background: #003366; color: #ffcc00; border: 1px solid #ffcc00; padding: 0.25rem 0.5rem; border-radius: 4px; font-weight: bold; cursor: pointer; outline: none; }

    /* Header & Navigation Bar */
    header { background-color: #003366; color: white; padding: 1rem 1.5rem; position: sticky; top: 0; z-index: 1000; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; box-shadow: 0 2px 10px rgba(0,0,0,0.15); }
    .logo { font-size: 1.4rem; font-weight: bold; color: #ffcc00; text-decoration: none; display: flex; align-items: center; gap: 0.4rem; }
    nav { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 0.4rem; }
    nav a { color: white; text-decoration: none; font-weight: 500; font-size: 0.9rem; transition: color 0.2s; padding: 0.2rem 0; }
    nav a:hover { color: #ffcc00; }
    
    /* Hero Banner */
    .hero { background: linear-gradient(rgba(0, 51, 102, 0.8), rgba(0, 51, 102, 0.8)), url('https://images.unsplash.com/photo-1436491865332-7a61a109cc05?auto=format&fit=crop&w=1200&q=80') center/cover no-repeat; color: white; text-align: center; padding: 4.5rem 1rem; }
    .hero h1 { font-size: 2.5rem; margin-bottom: 0.8rem; }
    .hero p { font-size: 1.1rem; max-width: 650px; margin: 0 auto 1.8rem; color: #e2e8f0; }
    
    /* Layout Containers & Section Offsets */
    .container { max-width: 1100px; margin: 2rem auto; padding: 0 1rem; }
    .page-section { background: white; border-radius: 8px; padding: 2rem; margin-bottom: 2rem; box-shadow: 0 4px 12px rgba(0,0,0,0.05); scroll-margin-top: 90px; }
    h2 { color: #003366; margin-bottom: 1rem; font-size: 1.6rem; border-bottom: 2px solid #f0f0f0; padding-bottom: 0.5rem; }
    
    /* Grids & Cards */
    .grid-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.25rem; margin-top: 1.25rem; }
    .card { background: #f8f9fa; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1.5rem; text-align: center; display: flex; flex-direction: column; justify-content: space-between; }
    .card h3 { color: #003366; margin-bottom: 0.5rem; font-size: 1.2rem; }
    .price-tag { font-size: 1.3rem; font-weight: bold; color: #28a745; margin: 0.5rem 0; }
    .badge { background: #ffcc00; color: #003366; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; font-weight: bold; display: inline-block; }
    
    /* Form Styles */
    .form-group { margin-bottom: 1.2rem; text-align: left; }
    .form-group label { display: block; font-weight: 600; margin-bottom: 0.4rem; color: #003366; font-size: 0.95rem; }
    .form-group input, .form-group select, .form-group textarea { width: 100%; padding: 0.75rem; border: 1px solid #cbd5e1; border-radius: 5px; font-size: 0.95rem; background-color: #fff; }
    .form-group input:focus, .form-group select:focus, .form-group textarea:focus { outline: none; border-color: #003366; box-shadow: 0 0 0 2px rgba(0, 51, 102, 0.15); }
    
    /* Buttons */
    .btn { background-color: #003366; color: white; border: none; padding: 10px 20px; font-size: 0.95rem; border-radius: 5px; cursor: pointer; text-decoration: none; display: inline-block; transition: background 0.2s; text-align: center; }
    .btn:hover { background-color: #002244; }
    .btn-success { background-color: #28a745; }
    .btn-success:hover { background-color: #1e7e34; }
    
    /* Map Box */
    .map-box { background: #eef4f8; border-radius: 8px; padding: 1.25rem; text-align: center; margin-top: 1.5rem; }
    
    /* Footer */
    footer { background-color: #002244; color: white; text-align: center; padding: 2rem 1rem; margin-top: 3rem; }
    footer a { color: #ffcc00; text-decoration: none; }
    footer a:hover { text-decoration: underline; }

    /* Responsive Mobile Tweaks */
    @media (max-width: 600px) {
      header { flex-direction: column; align-items: flex-start; }
      nav { width: 100%; justify-content: space-between; }
      .hero h1 { font-size: 1.8rem; }
      .page-section { padding: 1.25rem; }
    }
  </style>
</head>
<body>

  <!-- Top Info Bar with Language Selector -->
  <div class="top-bar">
    <span>📍 Gaba Road, Kampala, Uganda</span>
    <div>
      <span>📞 <a href="tel:+256744458131">+256 744 458131</a></span>
      <span>✉️ <a href="mailto:homiwedi.nh@gmail.com">homiwedi.nh@gmail.com</a></span>
      <select id="languageSelect" class="lang-select" onchange="changeLanguage(this.value)">
        <option value="en">English</option>
        <option value="ti">ትግርኛ (Tigrigna)</option>
        <option value="fr">Français (French)</option>
      </select>
    </div>
  </div>

  <!-- Main Navigation Header -->
  <header>
    <a href="#home" class="logo">✈️ Homi Cargo & Travel</a>
    <nav>
      <a href="#home" data-i18n="nav_home">Home</a>
      <a href="#tickets" data-i18n="nav_tickets">Tickets</a>
      <a href="#cargo" data-i18n="nav_cargo">Cargo</a>
      <a href="#rentals" data-i18n="nav_rentals">Rentals</a>
      <a href="#tours" data-i18n="nav_tours">Tours</a>
      <a href="#appointment" data-i18n="nav_appointment">Appointment</a>
    </nav>
  </header>

  <!-- Hero Banner -->
  <section id="home" class="hero">
    <h1 data-i18n="hero_title">Homi Cargo & Travel</h1>
    <p data-i18n="hero_desc">Your one-stop destination for Express Air Cargo, Flight Bookings, Car Rentals, and Guided Tours in Kampala.</p>
    <a href="#appointment" class="btn btn-success" onclick="selectService('General Question')" data-i18n="btn_book_appointment">Book an Appointment</a>
  </section>

  <div class="container">

    <!-- HOME OVERVIEW -->
    <section class="page-section">
      <h2 data-i18n="welcome_title">Welcome to Homi Cargo & Travel</h2>
      <p data-i18n="welcome_desc">Based in Kampala, Uganda, we specialize in fast air logistics, flight ticketing services, vehicle hire, and tours connecting East Africa to Eritrea and international destinations.</p>
      
      <div class="grid-3">
        <div class="card">
          <h3 data-i18n="card_tickets_title">✈️ Flight Ticketing</h3>
          <p data-i18n="card_tickets_desc">Discounted airline ticket bookings with personalized itinerary assistance.</p>
        </div>
        <div class="card">
          <h3 data-i18n="card_cargo_title">📦 Air Freight Cargo</h3>
          <p data-i18n="card_cargo_desc">Express flight cargo services to Asmara and global destinations at competitive rates.</p>
        </div>
        <div class="card">
          <h3 data-i18n="card_rentals_title">🚘 Car Hire & Tours</h3>
          <p data-i18n="card_rentals_desc">Reliable vehicles for town runs, airport pickups, and full tour packages.</p>
        </div>
      </div>

      <!-- Map & Location -->
      <div class="map-box">
        <h3 data-i18n="map_title">📍 Our Office Location: Gaba Road, Kampala</h3>
        <p style="color: #555; margin-bottom: 1rem; font-size: 0.9rem;" data-i18n="map_desc">Visit us for in-person flight ticketing, cargo drop-off, and tour bookings.</p>
        <div style="border-radius: 8px; overflow: hidden; height: 260px;">
          <iframe 
            src="https://maps.google.com/maps?q=Gaba%20Road%20Kampala&t=&z=14&ie=UTF8&iwloc=&output=embed" 
            width="100%" 
            height="100%" 
            style="border:0;" 
            loading="lazy"
            allowfullscreen>
          </iframe>
        </div>
      </div>
    </section>

    <!-- PAGE 1: FLIGHT TICKETS -->
    <section id="tickets" class="page-section">
      <h2 data-i18n="tickets_section_title">✈️ Flight Ticket Booking</h2>
      <p data-i18n="tickets_section_desc">We check Google Flights rates and manage your full booking process for a smooth journey. (All listed prices include our $50 management fee).</p>
      
      <div class="grid-3">
        <div class="card">
          <div>
            <h3 data-i18n="route_asmara_title">Entebbe ↔ Asmara</h3>
            <p data-i18n="route_asmara_desc">Direct & Connecting Flight Management</p>
            <div class="price-tag">Est. $550 - $750*</div>
            <span class="badge" data-i18n="agency_fee_badge">Includes $50 Agency Fee</span>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Flight Ticketing', 'Entebbe to Asmara')" data-i18n="btn_book_route">Book This Route</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="route_dubai_title">Entebbe ↔ Dubai</h3>
            <p data-i18n="route_dubai_desc">Direct Flights & Express Baggage Handling</p>
            <div class="price-tag">Est. $450 - $600*</div>
            <span class="badge" data-i18n="agency_fee_badge">Includes $50 Agency Fee</span>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Flight Ticketing', 'Entebbe to Dubai')" data-i18n="btn_book_route">Book This Route</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="route_global_title">Entebbe ↔ Jeddah / Istanbul</h3>
            <p data-i18n="route_global_desc">International Connecting Routes</p>
            <div class="price-tag">Est. $600 - $850*</div>
            <span class="badge" data-i18n="agency_fee_badge">Includes $50 Agency Fee</span>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Flight Ticketing', 'Entebbe to Jeddah/Istanbul')" data-i18n="btn_book_route">Book This Route</a>
        </div>
      </div>
      <p style="font-size: 0.85rem; color: #666; margin-top: 1rem; text-align: center;" data-i18n="tickets_disclaimer">*Final prices subject to seasonal airline rate updates at time of confirmation.</p>
    </section>

    <!-- PAGE 2: AIR CARGO -->
    <section id="cargo" class="page-section">
      <h2 data-i18n="cargo_section_title">📦 Express Air Cargo Services</h2>
      <p data-i18n="cargo_section_desc">We send all cargo strictly by Flight Express for maximum speed, security, and real-time handling.</p>
      
      <div class="card" style="background: #e6f0fa; border: 2px solid #003366; text-align: center; padding: 2rem; margin-top: 1rem;">
        <h3 style="font-size: 1.6rem; color: #003366;" data-i18n="cargo_rate_title">Air Cargo Freight Rate</h3>
        <div class="price-tag" style="font-size: 2.2rem; color: #003366; margin: 0.5rem 0;">$7 USD / Kg</div>
        <p style="font-size: 1rem; margin-bottom: 1.5rem;" data-i18n="cargo_rate_desc">Fast air shipment connecting Kampala (Entebbe Airport) to Asmara and regional airports.</p>
        
        <div style="text-align: left; max-width: 450px; margin: 0 auto; line-height: 1.8;">
          <p>✓ <strong data-i18n="cargo_feature_1_title">Fast Delivery:</strong> <span data-i18n="cargo_feature_1_desc">Express flight logistics.</span></p>
          <p>✓ <strong data-i18n="cargo_feature_2_title">Accepted Goods:</strong> <span data-i18n="cargo_feature_2_desc">Personal items, garments, electronics, & documents.</span></p>
          <p>✓ <strong data-i18n="cargo_feature_3_title">Drop-off Point:</strong> <span data-i18n="cargo_feature_3_desc">Our office on Gaba Road, Kampala.</span></p>
        </div>
        <br>
        <a href="#appointment" class="btn btn-success" onclick="selectService('Air Cargo ($7/kg)')" data-i18n="btn_schedule_cargo">Schedule Cargo Drop-off</a>
      </div>
    </section>

    <!-- PAGE 3: CAR RENTALS -->
    <section id="rentals" class="page-section">
      <h2 data-i18n="rentals_section_title">🚘 Car Rental Services</h2>
      <p data-i18n="rentals_section_desc">Hire reliable vehicles for city navigation, airport transfers, or travel across Uganda.</p>
      
      <div class="grid-3">
        <div class="card">
          <div>
            <h3 data-i18n="car_compact_title">Compact & Town Cars</h3>
            <p data-i18n="car_compact_desc">Ideal for daily town travel across Kampala.</p>
            <div class="price-tag" data-i18n="price_compact">From $35 / Day</div>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Car Rental', 'Compact Town Car')" data-i18n="btn_reserve_car">Reserve Car</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="car_suv_title">4x4 SUVs & RAV4s</h3>
            <p data-i18n="car_suv_desc">Great for long distance, rough roads, and upcountry travel.</p>
            <div class="price-tag" data-i18n="price_suv">From $60 / Day</div>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Car Rental', '4x4 SUV / RAV4')" data-i18n="btn_reserve_suv">Reserve SUV</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="car_airport_title">Entebbe Airport Transfers</h3>
            <p data-i18n="car_airport_desc">Comfortable pickup & drop-off from Entebbe Airport to Kampala.</p>
            <div class="price-tag" data-i18n="price_airport">$30 - $40 / Trip</div>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Car Rental', 'Airport Transfer')" data-i18n="btn_book_transfer">Book Transfer</a>
        </div>
      </div>
    </section>

    <!-- PAGE 4: TOURS & TRAVEL -->
    <section id="tours" class="page-section">
      <h2 data-i18n="tours_section_title">🌴 Guided Tours & Safari Packages</h2>
      <p data-i18n="tours_section_desc">Explore top regional tourist attractions with our customized travel packages.</p>
      
      <div class="grid-3">
        <div class="card">
          <div>
            <h3 data-i18n="tour_safari_title">Uganda Safari Tours</h3>
            <p data-i18n="tour_safari_desc">National Parks, Wildlife Safaris, & River Nile trips.</p>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Tour Package', 'Uganda Safari Tours')" data-i18n="btn_inquire_package">Inquire Package</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="tour_city_title">Kampala City Experience</h3>
            <p data-i18n="tour_city_desc">Guided day trips around historical and cultural spots in Kampala.</p>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Tour Package', 'Kampala City Experience')" data-i18n="btn_inquire_package">Inquire Package</a>
        </div>

        <div class="card">
          <div>
            <h3 data-i18n="tour_group_title">Custom Group Vacations</h3>
            <p data-i18n="tour_group_desc">Tailored flight + hotel packages for families & groups.</p>
          </div>
          <a href="#appointment" class="btn" style="margin-top: 1rem;" onclick="selectService('Tour Package', 'Custom Group Vacation')" data-i18n="btn_inquire_package">Inquire Package</a>
        </div>
      </div>
    </section>

    <!-- PAGE 5: BOOK APPOINTMENT & INQUIRY FORM -->
    <section id="appointment" class="page-section">
      <h2 data-i18n="form_section_title">📅 Book an Appointment / Ask a Question</h2>
      <p data-i18n="form_section_desc">Fill out the form below to book a consultation at our Gaba Road office or request assistance with ticketing, cargo, or car rentals.</p>
      
      <form action="https://formspree.io/f/mbgldlvw" method="POST" style="margin-top: 1.5rem;">
        
        <div class="form-group">
          <label for="name" data-i18n="label_full_name">Full Name:</label>
          <input type="text" id="name" name="Client Name" placeholder="Your full name" required>
        </div>

        <div class="form-group">
          <label for="contact" data-i18n="label_phone">Phone Number / WhatsApp:</label>
          <input type="text" id="contact" name="Phone Number" placeholder="+256..." required>
        </div>

        <div class="form-group">
          <label for="service" data-i18n="label_service">Service Required:</label>
          <select id="service" name="Service Selected">
            <option value="Flight Ticketing" data-i18n="opt_flight">Flight Ticket Booking (+$50 Fee Plan)</option>
            <option value="Air Cargo ($7/kg)" data-i18n="opt_cargo">Air Cargo Shipment ($7 USD / kg)</option>
            <option value="Car Rental" data-i18n="opt_rental">Car Rental / Airport Transfer</option>
            <option value="Tour Package" data-i18n="opt_tour">Tour & Travel Package</option>
            <option value="General Question" data-i18n="opt_general">General Question / Office Appointment</option>
          </select>
        </div>

        <div class="form-group">
          <label for="message" data-i18n="label_message">Your Message or Appointment Request:</label>
          <textarea id="message" name="Message Detail" rows="4" placeholder="Tell us your travel dates, cargo weight estimate, or question..." required></textarea>
        </div>

        <button type="submit" class="btn btn-success" style="width: 100%; font-size: 1.05rem; padding: 14px;" data-i18n="btn_submit_form">Send Inquiry / Book Appointment</button>
      </form>
    </section>

  </div>

  <!-- Footer -->
  <footer>
    <p><strong>Homi Cargo & Travel</strong></p>
    <p>Gaba Road, Kampala, Uganda</p>
    <p style="margin-top: 0.3rem;">Phone: <a href="tel:+256744458131">+256 744 458131</a> | Email: <a href="mailto:homiwedi.nh@gmail.com">homiwedi.nh@gmail.com</a></p>
    <br>
    <p style="font-size: 0.85rem; color: #aaa;">© 2026 Homi Cargo & Travel. All Rights Reserved.</p>
  </footer>

  <!-- Translation & Interactive Scripts -->
  <script>
    const translations = {
      en: {
        nav_home: "Home",
        nav_tickets: "Tickets",
        nav_cargo: "Cargo",
        nav_rentals: "Rentals",
        nav_tours: "Tours",
        nav_appointment: "Appointment",
        hero_title: "Homi Cargo & Travel",
        hero_desc: "Your one-stop destination for Express Air Cargo, Flight Bookings, Car Rentals, and Guided Tours in Kampala.",
        btn_book_appointment: "Book an Appointment",
        welcome_title: "Welcome to Homi Cargo & Travel",
        welcome_desc: "Based in Kampala, Uganda, we specialize in fast air logistics, flight ticketing services, vehicle hire, and tours connecting East Africa to Eritrea and international destinations.",
        card_tickets_title: "✈️ Flight Ticketing",
        card_tickets_desc: "Discounted airline ticket bookings with personalized itinerary assistance.",
        card_cargo_title: "📦 Air Freight Cargo",
        card_cargo_desc: "Express flight cargo services to Asmara and global destinations at competitive rates.",
        card_rentals_title: "🚘 Car Hire & Tours",
        card_rentals_desc: "Reliable vehicles for town runs, airport pickups, and full tour packages.",
        map_title: "📍 Our Office Location: Gaba Road, Kampala",
        map_desc: "Visit us for in-person flight ticketing, cargo drop-off, and tour bookings.",
        tickets_section_title: "✈️ Flight Ticket Booking",
        tickets_section_desc: "We check Google Flights rates and manage your full booking process for a smooth journey. (All listed prices include our $50 management fee).",
        route_asmara_title: "Entebbe ↔ Asmara",
        route_asmara_desc: "Direct & Connecting Flight Management",
        route_dubai_title: "Entebbe ↔ Dubai",
        route_dubai_desc: "Direct Flights & Express Baggage Handling",
        route_global_title: "Entebbe ↔ Jeddah / Istanbul",
        route_global_desc: "International Connecting Routes",
        agency_fee_badge: "Includes $50 Agency Fee",
        btn_book_route: "Book This Route",
        tickets_disclaimer: "*Final prices subject to seasonal airline rate updates at time of confirmation.",
        cargo_section_title: "📦 Express Air Cargo Services",
        cargo_section_desc: "We send all cargo strictly by Flight Express for maximum speed, security, and real-time handling.",
        cargo_rate_title: "Air Cargo Freight Rate",
        cargo_rate_desc: "Fast air shipment connecting Kampala (Entebbe Airport) to Asmara and regional airports.",
        cargo_feature_1_title: "Fast Delivery:",
        cargo_feature_1_desc: "Express flight logistics.",
        cargo_feature_2_title: "Accepted Goods:",
        cargo_feature_2_desc: "Personal items, garments, electronics, & documents.",
        cargo_feature_3_title: "Drop-off Point:",
        cargo_feature_3_desc: "Our office on Gaba Road, Kampala.",
        btn_schedule_cargo: "Schedule Cargo Drop-off",
        rentals_section_title: "🚘 Car Rental Services",
        rentals_section_desc: "Hire reliable vehicles for city navigation, airport transfers, or travel across Uganda.",
        car_compact_title: "Compact & Town Cars",
        car_compact_desc: "Ideal for daily town travel across Kampala.",
        price_compact: "From $35 / Day",
        btn_reserve_car: "Reserve Car",
        car_suv_title: "4x4 SUVs & RAV4s",
        car_suv_desc: "Great for long distance, rough roads, and upcountry travel.",
        price_suv: "From $60 / Day",
        btn_reserve_suv: "Reserve SUV",
        car_airport_title: "Entebbe Airport Transfers",
        car_airport_desc: "Comfortable pickup & drop-off from Entebbe Airport to Kampala.",
        price_airport: "$30 - $40 / Trip",
        btn_book_transfer: "Book Transfer",
        tours_section_title: "🌴 Guided Tours & Safari Packages",
        tours_section_desc: "Explore top regional tourist attractions with our customized travel packages.",
        tour_safari_title: "Uganda Safari Tours",
        tour_safari_desc: "National Parks, Wildlife Safaris, & River Nile trips.",
        tour_city_title: "Kampala City Experience",
        tour_city_desc: "Guided day trips around historical and cultural spots in Kampala.",
        tour_group_title: "Custom Group Vacations",
        tour_group_desc: "Tailored flight + hotel packages for families & groups.",
        btn_inquire_package: "Inquire Package",
        form_section_title: "📅 Book an Appointment / Ask a Question",
        form_section_desc: "Fill out the form below to book a consultation at our Gaba Road office or request assistance with ticketing, cargo, or car rentals.",
        label_full_name: "Full Name:",
        label_phone: "Phone Number / WhatsApp:",
        label_service: "Service Required:",
        opt_flight: "Flight Ticket Booking (+$50 Fee Plan)",
        opt_cargo: "Air Cargo Shipment ($7 USD / kg)",
        opt_rental: "Car Rental / Airport Transfer",
        opt_tour: "Tour & Travel Package",
        opt_general: "General Question / Office Appointment",
        label_message: "Your Message or Appointment Request:",
        btn_submit_form: "Send Inquiry / Book Appointment"
      },
      ti: {
        nav_home: "መእተዊ",
        nav_tickets: "ትኬት",
        nav_cargo: "ካርጎ",
        nav_rentals: "ኪራይ መኪና",
        nav_tours: "ቱሪዝም",
        nav_appointment: "ቀጸራ",
        hero_title: "ሆሚ ካርጎን ጉዕዞን",
        hero_desc: "ንቕልጡፍ ናይ ኣየር ካርጎ፣ ምቁራጽ ትኬት ነፋሪት፣ ኪራይ መኪናን ናይ ቱሪዝም ኣገልግሎትን ኣብ ካምፓላ።",
        btn_book_appointment: "ቀጸራ ትሓዙ",
        welcome_title: "እንቛዕ ብደሓን መጻእኩም ናብ ሆሚ ካርጎን ጉዕዞን",
        welcome_desc: "ኣብ ካምፓላ ኡጋንዳ ዝመደበሩ ትካልና፡ ንምብራቕ ኣፍሪቃ ምስ ኣስመራን ካልኦት ዓለም ለኻዊ ቦታታትን ዘራኽብ ናይ ኣየር ካርጎ፣ ትኬት ነፋሪት፣ ኪራይ መኪናን ቱሪዝምን የገልግሎ።",
        card_tickets_title: "✈️ ምቁራጽ ትኬት ነፋሪት",
        card_tickets_desc: "ሕሱር ዋጋታት ትኬትን ናይ ጉዕዞ ሓበሬታን ምስ ምሉእ ሓገዝ።",
        card_cargo_title: "📦 ናይ ኣየር ካርጎ (ጽዕነት)",
        card_cargo_desc: "ቀልጣፍ ናይ ኣየር ጽዕነት ናብ ኣስመራን ዓለም ለኻዊ ቦታታትን ብተወዳዳሪ ዋጋ።",
        card_rentals_title: "🚘 ኪራይ መኪናን ቱሪዝምን",
        card_rentals_desc: "እሙናት መካይን ንከተማ፣ ምቕባል ካብ ኤርፖርት፣ ва ናይ ቱሪዝም ጉዕዞታት።",
        map_title: "📍 ኣድራሻ ቤት ጽሕፈትና: ጋባ ሮድ፣ ካምፓላ",
        map_desc: "ትኬት ንምቁራጽ፣ ካርጎ ንምርካብ ወይ ቀጸራ ንምሓዝ ናብ ቤት ጽሕፈትና ይምጽኡ።",
        tickets_section_title: "✈️ ምቁራጽ ትኬት ነፋሪት",
        tickets_section_desc: "ብሉጽ ዋጋታት ብምርካብ ናይ ምቁራጽ መስርሕኩም ነቃልጥ። (ኩሉ ዋጋታት $50 ናይ ኣገልግሎት ክፍሊት ዝሓዘ እዩ)።",
        route_asmara_title: "ኤንተበ ↔ ኣስመራ",
        route_asmara_desc: "ቀጥታን ተዛማድን ናይ ነፋሪት ጉዕዞ",
        route_dubai_title: "ኤንተበ ↔ ዱባይ",
        route_dubai_desc: "ቀጥታ ጉዕዞን ቀልጣፍ ናይ ቦርሳ ሓገዝን",
        route_global_title: "ኤንተበ ↔ ጅዳ / ኢስታንቡል",
        route_global_desc: "ዓለም ለኻዊ ተዛማዲ ጉዕዞታት",
        agency_fee_badge: "$50 ናይ ኣገልግሎት ክፍሊት ዝሓዘ",
        btn_book_route: "ትኬት ሕዙ",
        tickets_disclaimer: "*ናይ መወዳእታ ዋጋ ከም ግዜኡን ናይ ኣየር መንገዲታት ለውጥን ክቀያየር ይኽእል እዩ።",
        cargo_section_title: "📦 ቀልጣፍ ናይ ኣየር ካርጎ ኣገልግሎት",
        cargo_section_desc: "ኩሉ ካርጎ ብልዑል ቕልጣፈን ሓለዋን ብነፋሪት ጥራይ ይልኣኽ።",
        cargo_rate_title: "ናይ ኣየር ካርጎ ዋጋ",
        cargo_rate_desc: "ካብ ካምፓላ (ኤርፖርት ኤንተበ) ናብ ኣስመራን ከባቢኡን ዝልኣኽ ቀልጣፍ ናይ ኣየር ጽዕነት።",
        cargo_feature_1_title: "ቀልጣፍ ምብጻሕ:",
        cargo_feature_1_desc: "ብነፋሪት ዝግበር ቀልጣፍ ጽዕነት።",
        cargo_feature_2_title: "ዝልኣኹ ኣቑሑት:",
        cargo_feature_2_desc: "ብሕታዊ ኣቑሑት፣ ክዳውንቲ፣ ኤレクトሮኒክስ፣ ሰነዳት።",
        cargo_feature_3_title: "መቐበሊ ቦታ:",
        cargo_feature_3_desc: "ኣብ ጋባ ሮድ (ካምፓላ) ዘሎ ቤት ጽሕፈትና።",
        btn_schedule_cargo: "ካርጎ ንምልኣኽ ቀጸራ ሕዙ",
        rentals_section_title: "🚘 ኣገልግሎት ኪራይ መኪና",
        rentals_section_desc: "ንከተማ፣ ንኤርፖርት ወይ ንመላእ ኡጋንዳ ዝኾና እሙናት መካይን ተካርዩ።",
        car_compact_title: "ንከተማ ዝኾና መካይን",
        car_compact_desc: "ንመዓልታዊ ናይ ከተማ ጉዕዞ ኣብ ካምፓላ።",
        price_compact: "ካብ $35 / መዓልቲ",
        btn_reserve_car: "መኪና ሕዙ",
        car_suv_title: "4x4 SUVs & RAV4s",
        car_suv_desc: "ንነወሕ መንገዲ፣ ጽቡቕ ዘይኮነ ጎደናታትን ገጠራትን ዝኾና።",
        price_suv: "ካብ $60 / መዓልቲ",
        btn_reserve_suv: "SUV ሕዙ",
        car_airport_title: "ካብ/ናብ ኤርፖርት ኤንተበ",
        car_airport_desc: "ምቹእ ናይ ምቕባልን ምብጻሕን ኣገልግሎት ካብ ኤንተበ ናብ ካምፓላ።",
        price_airport: "$30 - $40 / ምብጻሕ",
        btn_book_transfer: "መጓዓዝያ ሕዙ",
        tours_section_title: "🌴 ናይ ቱሪዝምን ሳፋሪን ፓኬጃት",
        tours_section_desc: "ምስ ናይና ፍሉይ ናይ ቱሪዝም ፓኬጃት ንምብራቕ ኣፍሪቃ ይጎብኙ።",
        tour_safari_title: "ኡጋንዳ ሳፋሪ ቱር",
        tour_safari_desc: "ብሄራዊ ፓርክታት፣ ናይ ዘረባ እንስሳታት ሳፋሪን ፈለግ ናይልን።",
        tour_city_title: "ናይ ካምፓላ ከተማ ዑደት",
        tour_city_desc: "ኣብ ታሪኻውን ባህላውን ቦታታት ካምፓላ ዝግበር ዑደት።",
        tour_group_title: "ናይ ስድራቤትን ጕጅለን ዕረፍቲ",
        tour_group_desc: "ንስድራቤታትን ጉጅለታትን ዝተዳለወ ናይ ነፋሪትን ሆቴልን ፓኬጅ።",
        btn_inquire_package: "ሓበሬታ ሕተቱ",
        form_section_title: "📅 ቀጸራ ንምሓዝ / ሕቶ ንምሕታት",
        form_section_desc: "ኣብ ቤት ጽሕፈትና ቀጸራ ንምሓዝ ወይ ብዛዕባ ትኬት፣ ካርጎን ኪራይ መኪናን ንምሕታት ነዚ ፎርም መልኡ።",
        label_full_name: "ምሉእ ስም:",
        label_phone: "ቁጽሪ ስልኪ /  his ፡",
        label_service: "ዝደልይዎ ኣገልግሎት:",
        opt_flight: "ምቁራጽ ትኬት ነፋሪት (+$50 ኣገልግሎት)",
        opt_cargo: "ናይ ኣየር ካርጎ ($7 USD / kg)",
        opt_rental: "ኪራይ መኪና / መጓዓዝያ ኤርፖርት",
        opt_tour: "ናይ ቱሪዝም ፓኬጅ",
        opt_general: "ሓፈሻዊ ሕቶ / ናይ ቤት ጽሕፈት ቀጸራ",
        label_message: "መልእኽትኹም ወይ ናይ ቀጸራ ሕቶኹም:",
        btn_submit_form: "መልእኽቲ ስደዱ / ቀጸራ ሕዙ"
      },
      fr: {
        nav_home: "Accueil",
        nav_tickets: "Billets",
        nav_cargo: "Fret Aérien",
        nav_rentals: "Location",
        nav_tours: "Circuits",
        nav_appointment: "Rendez-vous",
        hero_title: "Homi Cargo & Travel",
        hero_desc: "Votre destination unique pour le fret aérien express, la réservation de vols, la location de voitures et les visites guidées à Kampala.",
        btn_book_appointment: "Prendre Rendez-vous",
        welcome_title: "Bienvenue chez Homi Cargo & Travel",
        welcome_desc: "Basés à Kampala, en Ouganda, nous sommes spécialisés dans la logistique aérienne rapide, les billets d'avion, la location de véhicules et les séjours reliant l'Afrique de l'Est à l'Érythrée et au monde.",
        card_tickets_title: "✈️ Billetterie Aérienne",
        card_tickets_desc: "Réservations de billets d'avion à prix réduits avec assistance personnalisée.",
        card_cargo_title: "📦 Fret Aérien Express",
        card_cargo_desc: "Services de fret aérien express vers Asmara et le monde entier à des tarifs compétitifs.",
        card_rentals_title: "🚘 Location & Tours",
        card_rentals_desc: "Véhicules fiables pour vos déplacements en ville, transferts aéroport et circuits touristiques.",
        map_title: "📍 Notre Bureau: Gaba Road, Kampala",
        map_desc: "Rendez-nous visite pour réserver vos billets, déposer vos colis ou planifier vos voyages.",
        tickets_section_title: "✈️ Réservation de Billets d'Avion",
        tickets_section_desc: "Nous vérifions les tarifs Google Flights et gérons votre réservation pour un voyage sans tracas. (Les prix incluent nos 50 $ de frais de gestion).",
        route_asmara_title: "Entebbe ↔ Asmara",
        route_asmara_desc: "Gestion de vols directs et avec escales",
        route_dubai_title: "Entebbe ↔ Dubaï",
        route_dubai_desc: "Vols directs & gestion express des bagages",
        route_global_title: "Entebbe ↔ Djeddah / Istanbul",
        route_global_desc: "Liaisons internationales avec escales",
        agency_fee_badge: "Frais d'agence de 50 $ inclus",
        btn_book_route: "Réserver ce Trajet",
        tickets_disclaimer: "*Les prix finaux sont sujets aux variations saisonnières des compagnies aériennes.",
        cargo_section_title: "📦 Fret Aérien Express",
        cargo_section_desc: "Nous expédions tout le fret exclusivement par vol express pour une rapidité et une sécurité maximales.",
        cargo_rate_title: "Tarif du Fret Aérien",
        cargo_rate_desc: "Expédition aérienne rapide reliant Kampala (Aéroport d'Entebbe) à Asmara et aux aéroports régionaux.",
        cargo_feature_1_title: "Livraison Rapide:",
        cargo_feature_1_desc: "Logistique de vol express.",
        cargo_feature_2_title: "Marchandises Acceptées:",
        cargo_feature_2_desc: "Effets personnels, vêtements, électronique et documents.",
        cargo_feature_3_title: "Point de Dépôt:",
        cargo_feature_3_desc: "Notre bureau situé sur Gaba Road, Kampala.",
        btn_schedule_cargo: "Planifier un Dépôt Cargo",
        rentals_section_title: "🚘 Service de Location de Voitures",
        rentals_section_desc: "Louez des véhicules fiables pour la ville, vos transferts aéroport ou vos déplacements en Ouganda.",
        car_compact_title: "Voitures Citadines",
        car_compact_desc: "Idéales pour les trajets quotidiens dans Kampala.",
        price_compact: "À partir de 35 $ / Jour",
        btn_reserve_car: "Réserver une Voiture",
        car_suv_title: "4x4 & RAV4",
        car_suv_desc: "Parfaits pour les longues distances et les routes de campagne.",
        price_suv: "À partir de 60 $ / Jour",
        btn_reserve_suv: "Réserver un SUV",
        car_airport_title: "Transfert Aéroport d'Entebbe",
        car_airport_desc: "Service de navette confortable entre l'aéroport d'Entebbe et Kampala.",
        price_airport: "30 $ - 40 $ / Trajet",
        btn_book_transfer: "Réserver un Transfert",
        tours_section_title: "🌴 Circuits & Safaris Guidés",
        tours_section_desc: "Découvrez les meilleures attractions touristiques grâce à nos forfaits sur mesure.",
        tour_safari_title: "Safaris en Ouganda",
        tour_safari_desc: "Parcs nationaux, observation de la faune et excursions sur le Nil.",
        tour_city_title: "Visite de Kampala",
        tour_city_desc: "Excursions d'une journée dans les lieux historiques et culturels de Kampala.",
        tour_group_title: "Séjours de Groupe Sur Mesure",
        tour_group_desc: "Offres vol + hôtel adaptées aux familles et aux groupes.",
        btn_inquire_package: "Demander des Infos",
        form_section_title: "📅 Prendre Rendez-vous / Poser une Question",
        form_section_desc: "Remplissez le formulaire ci-dessous pour réserver une consultation à notre bureau de Gaba Road ou demander de l'aide.",
        label_full_name: "Nom Complet:",
        label_phone: "Numéro de Téléphone / WhatsApp:",
        label_service: "Service Requis:",
        opt_flight: "Réservation de Vol (Frais de 50 $ inclus)",
        opt_cargo: "Expédition Cargo Aérien (7 USD / kg)",
        opt_rental: "Location de Voiture / Navette Aéroport",
        opt_tour: "Forfait Circuit & Voyage",
        opt_general: "Question Générale / RDV au Bureau",
        label_message: "Votre Message ou Demande de RDV:",
        btn_submit_form: "Envoyer / Prendre RDV"
      }
    };

    function changeLanguage(lang) {
      const elements = document.querySelectorAll('[data-i18n]');
      elements.forEach(element => {
        const key = element.getAttribute('data-i18n');
        if (translations[lang] && translations[lang][key]) {
          element.textContent = translations[lang][key];
        }
      });
      document.documentElement.lang = lang;
    }

    function selectService(serviceValue, details) {
      const selectElement = document.getElementById('service');
      const messageElement = document.getElementById('message');
      
      if (selectElement) {
        selectElement.value = serviceValue;
      }
      
      if (details && messageElement) {
        messageElement.value = "Interest/Details: " + details + ". ";
      }
    }
  </script>

</body>
</html>
 and travel tour Agency 

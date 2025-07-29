// Homepage.jsx
import React from "react";

export default function Homepage() {
  return (
    <div className="bg-gray-50 text-gray-800">
      {/* Header */}
      <header className="bg-white shadow-sm sticky top-0 z-50">
        <div className="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
          <div className="text-2xl font-bold text-[#9CAF88]">Eagle Sight</div>
          <nav className="space-x-6 text-sm md:text-base">
            <a href="#services" className="hover:text-[#D4AF37]">Services / Huduma</a>
            <a href="#about" className="hover:text-[#D4AF37]">About Us / Kuhusu Sisi</a>
            <a href="#contact" className="hover:text-[#D4AF37]">Contact / Mawasiliano</a>
            <a href="#booking" className="bg-[#A3BFD9] px-4 py-2 rounded text-white hover:bg-[#9CAF88]">Book Now / Weka Booking</a>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="text-center py-16 px-4 bg-[#A3BFD9] text-white">
        <h1 className="text-4xl font-bold mb-4">Professional Cleaning Services</h1>
        <p className="text-lg mb-6">Reliable, affordable, and personalized cleaning for homes and offices in Tanzania.</p>
        <a href="#booking" className="bg-[#D4AF37] text-white px-6 py-3 rounded hover:bg-[#9CAF88]">Book a Cleaning / Weka Booking</a>
      </section>

      {/* Services */}
      <section id="services" className="py-16 px-4 max-w-6xl mx-auto">
        <h2 className="text-3xl font-semibold text-center mb-12">Our Services / Huduma Zetu</h2>
        <div className="grid md:grid-cols-3 gap-8">
          {[
            { title: "Home Cleaning", sw: "Usafi wa Nyumbani" },
            { title: "Office Cleaning", sw: "Usafi wa Ofisi" },
            { title: "Deep Cleaning", sw: "Usafi wa Kina" },
            { title: "Sofa/Carpet Cleaning", sw: "Usafi wa Sofa/Carpet" },
            { title: "Pest Control", sw: "Udhibiti wa Wadudu" },
            { title: "Post-construction Cleaning", sw: "Usafi Baada ya Ujenzi" },
          ].map((s, index) => (
            <div key={index} className="bg-white shadow p-6 rounded hover:shadow-lg">
              <h3 className="text-xl font-bold text-[#9CAF88] mb-2">{s.title}</h3>
              <p className="text-gray-600">{s.sw}</p>
              <a href="#booking" className="mt-4 inline-block text-[#D4AF37] hover:underline">Book Now</a>
            </div>
          ))}
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="bg-[#E5E5E5] py-16 px-4 text-center">
        <h2 className="text-3xl font-semibold mb-6">About Us / Kuhusu Sisi</h2>
        <h3 className="text-xl font-medium text-[#9CAF88] mb-4">Our Story / Hadithi Yetu</h3>
        <p className="max-w-3xl mx-auto text-gray-700">
          Eagle Sight Cleaning Services is a family-owned company founded by Samwel and Edithlinda Machibya.
          We are passionate about providing reliable and professional cleaning services across Dar es Salaam. 
          Our vision is to become the most trusted cleaning brand in East Africa.
        </p>
        <h3 className="text-xl font-medium text-[#9CAF88] mt-8 mb-2">Our Mission / Dhamira Yetu</h3>
        <p className="max-w-3xl mx-auto text-gray-700">
          To deliver reliable and high-quality cleaning services with professionalism, trust, and consistency.
        </p>
        <h3 className="text-xl font-medium text-[#9CAF88] mt-8 mb-2">Our Vision / Maono Yetu</h3>
        <p className="max-w-3xl mx-auto text-gray-700">
          To become the most trusted cleaning service provider in East Africa, recognized for excellence and customer care.
        </p>
      </section>

      {/* Booking Section */}
      <section id="booking" className="py-16 px-4 max-w-2xl mx-auto">
        <h2 className="text-3xl font-semibold text-center mb-8">Book a Service / Weka Booking</h2>
        <form className="grid gap-6">
          <input type="text" placeholder="Full Name / Jina Kamili" className="p-3 border rounded" />
          <input type="tel" placeholder="Phone Number / Namba ya Simu" className="p-3 border rounded" />
          <input type="text" placeholder="Location / Mahali" className="p-3 border rounded" />
          <select className="p-3 border rounded">
            <option>Select Service / Chagua Huduma</option>
            <option>Home Cleaning</option>
            <option>Office Cleaning</option>
            <option>Deep Cleaning</option>
            <option>Sofa/Carpet Cleaning</option>
            <option>Pest Control</option>
            <option>Post-construction Cleaning</option>
          </select>
          <input type="date" className="p-3 border rounded" />
          <select className="p-3 border rounded">
            <option>Payment Option / Njia ya Malipo</option>
            <option>Pay Now / Lipa Sasa</option>
            <option>Pay After / Lipa Baadae</option>
          </select>
          <button className="bg-[#9CAF88] text-white py-3 rounded hover:bg-[#D4AF37]">Submit Booking / Tuma Booking</button>
        </form>
      </section>

      {/* Footer */}
      <footer id="contact" className="bg-white text-center text-sm py-8 border-t">
        <p>Call: +255783858019 | +255744894306</p>
        <p>Email: samedward865@gmail.com</p>
        <p>Location: Ubungo, Dar es Salaam</p>
        <p className="mt-4">© {new Date().getFullYear()} Eagle Sight Cleaning Services. All rights reserved.</p>
      </footer>
    </div>
  );
}

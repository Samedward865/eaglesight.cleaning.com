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
      <section className="text-center py-20 px-6 bg-[#A3BFD9] text-white">
        <h1 className="text-5xl font-extrabold mb-4">Eagle Sight Cleaning Services</h1>
        <p className="text-xl mb-6">Professional. Reliable. Affordable. Cleaning services tailored to your needs.</p>
        <a href="#booking" className="bg-[#D4AF37] text-white px-6 py-3 rounded hover:bg-[#9CAF88] font-semibold">Book a Cleaning / Weka Booking</a>
      </section>

      {/* Services */}
      <section id="services" className="py-20 px-6 max-w-6xl mx-auto">
        <h2 className="text-4xl font-bold text-center text-[#9CAF88] mb-12">Our Services / Huduma Zetu</h2>
        <div className="grid md:grid-cols-3 gap-10">
          {[
            { title: "Home Cleaning", sw: "Usafi wa Nyumbani" },
            { title: "Office Cleaning", sw: "Usafi wa Ofisi" },
            { title: "Deep Cleaning", sw: "Usafi wa Kina" },
            { title: "Sofa/Carpet Cleaning", sw: "Usafi wa Sofa/Carpet" },
            { title: "Pest Control", sw: "Udhibiti wa Wadudu" },
            { title: "Post-construction Cleaning", sw: "Usafi Baada ya Ujenzi" },
          ].map((s, index) => (
            <div key={index} className="bg-white shadow-lg p-6 rounded-lg hover:shadow-xl">
              <h3 className="text-2xl font-semibold text-[#9CAF88] mb-2">{s.title}</h3>
              <p className="text-gray-600 text-sm">{s.sw}</p>
              <a href="#booking" className="mt-4 inline-block text-[#D4AF37] hover:underline font-medium">Book Now</a>
            </div>
          ))}
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="bg-[#E5E5E5] py-20 px-6 text-center">
        <h2 className="text-4xl font-bold text-[#9CAF88] mb-10">About Us / Kuhusu Sisi</h2>
        <div className="max-w-3xl mx-auto text-left space-y-10">
          <div>
            <h3 className="text-2xl font-semibold text-[#D4AF37] mb-2">Our Story / Hadithi Yetu</h3>
            <p className="text-gray-700">
              Eagle Sight Cleaning Services is a family-owned company founded by Samwel and Edithlinda Machibya.
              We are passionate about providing reliable and professional cleaning services across Dar es Salaam.
              Our vision is to become the most trusted cleaning brand in East Africa.
            </p>
          </div>
          <div>
            <h3 className="text-2xl font-semibold text-[#D4AF37] mb-2">Our Mission / Dhamira Yetu</h3>
            <p className="text-gray-700">
              To deliver reliable and high-quality cleaning services with professionalism, trust, and consistency.
            </p>
          </div>
          <div>
            <h3 className="text-2xl font-semibold text-[#D4AF37] mb-2">Our Vision / Maono Yetu</h3>
            <p className="text-gray-700">
              To become the most trusted cleaning service provider in East Africa, recognized for excellence and customer care.
            </p>
          </div>
        </div>
      </section>

      {/* Booking Section */}
      <section id="booking" className="py-20 px-6 max-w-2xl mx-auto">
        <h2 className="text-4xl font-bold text-center text-[#9CAF88] mb-10">Book a Service / Weka Booking</h2>
        <form className="grid gap-6 bg-white p-6 rounded shadow">
          <input type="text" placeholder="Full Name / Jina Kamili" className="p-3 border border-gray-300 rounded" />
          <input type="tel" placeholder="Phone Number / Namba ya Simu" className="p-3 border border-gray-300 rounded" />
          <input type="text" placeholder="Location / Mahali" className="p-3 border border-gray-300 rounded" />
          <select className="p-3 border border-gray-300 rounded">
            <option>Select Service / Chagua Huduma</option>
            <option>Home Cleaning</option>
            <option>Office Cleaning</option>
            <option>Deep Cleaning</option>
            <option>Sofa/Carpet Cleaning</option>
            <option>Pest Control</option>
            <option>Post-construction Cleaning</option>
          </select>
          <input type="date" className="p-3 border border-gray-300 rounded" />
          <select className="p-3 border border-gray-300 rounded">
            <option>Payment Option / Njia ya Malipo</option>
            <option>Pay Now / Lipa Sasa</option>
            <option>Pay After / Lipa Baadae</option>
          </select>
          <button className="bg-[#9CAF88] text-white py-3 rounded hover:bg-[#D4AF37] font-semibold">Submit Booking / Tuma Booking</button>
        </form>
      </section>

      {/* Footer */}
      <footer id="contact" className="bg-white text-center text-sm py-10 border-t border-gray-200">
        <div className="space-y-1">
          <p>Call: +255783858019 | +255744894306</p>
          <p>Email: samedward865@gmail.com</p>
          <p>Location: Ubungo, Dar es Salaam</p>
        </div>
        <p className="mt-4 text-gray-500">© {new Date().getFullYear()} Eagle Sight Cleaning Services. All rights reserved.</p>
      </footer>
    </div>
  );
}

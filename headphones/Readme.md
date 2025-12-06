import { Facebook, Twitter, Instagram } from "lucide-react";

export function Footer() {
  return (
    <footer className="bg-[#071629] text-white pt-20 pb-8 border-t border-white/10">
      <div className="max-w-[1000px] mx-auto px-6">
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
          {/* Company Info */}
          <div>
            <img 
              src="data:image/svg+xml,%3Csvg width='32' height='32' viewBox='0 0 32 32' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Ccircle cx='16' cy='16' r='16' fill='white'/%3E%3C/svg%3E" 
              alt="Logo" 
              className="w-10 h-10 mb-6"
            />
            <p className="text-white/60 text-sm">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            </p>
          </div>

          {/* Links Column 1 */}
          <div>
            <h4 className="mb-6">Company</h4>
            <ul className="space-y-3">
              <li>
                <a href="#about" className="hover-link text-white/70 text-sm">
                  About
                </a>
              </li>
              <li>
                <a href="#careers" className="hover-link text-white/70 text-sm">
                  Careers
                </a>
              </li>
              <li>
                <a href="#press" className="hover-link text-white/70 text-sm">
                  Press
                </a>
              </li>
            </ul>
          </div>

          {/* Links Column 2 */}
          <div>
            <h4 className="mb-6">Resources</h4>
            <ul className="space-y-3">
              <li>
                <a href="#blog" className="hover-link text-white/70 text-sm">
                  Blog
                </a>
              </li>
              <li>
                <a href="#help" className="hover-link text-white/70 text-sm">
                  Help Center
                </a>
              </li>
              <li>
                <a href="#contact" className="hover-link text-white/70 text-sm">
                  Contact
                </a>
              </li>
            </ul>
          </div>

          {/* Social Media */}
          <div>
            <h4 className="mb-6">Follow Us</h4>
            <div className="flex gap-4">
              <a 
                href="#facebook" 
                className="hover-button w-10 h-10 bg-white/10 rounded-full flex items-center justify-center"
                aria-label="Facebook"
              >
                <Facebook className="w-5 h-5" />
              </a>
              <a 
                href="#twitter" 
                className="hover-button w-10 h-10 bg-white/10 rounded-full flex items-center justify-center"
                aria-label="Twitter"
              >
                <Twitter className="w-5 h-5" />
              </a>
              <a 
                href="#instagram" 
                className="hover-button w-10 h-10 bg-white/10 rounded-full flex items-center justify-center"
                aria-label="Instagram"
              >
                <Instagram className="w-5 h-5" />
              </a>
            </div>
          </div>
        </div>

        {/* Copyright */}
        <div className="border-t border-white/10 pt-8 text-center">
          <p className="text-white/50 text-sm">
            &copy; 2025 Headphones. All rights reserved.
          </p>
        </div>
      </div>
    </footer>
  );
}


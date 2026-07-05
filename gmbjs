/* =============================================
       SECURITY: Disable right-click and text selection
       on sensitive content
    ============================================= */
    document.addEventListener('contextmenu', function (e) {
      if (e.target.closest('.pinfo-hidden, .pmodal-info-locked, .protected')) {
        e.preventDefault();
      }
    });

    document.addEventListener('dragstart', function (e) {
      if (e.target.tagName === 'IMG') e.preventDefault();
    });

    /* =============================================
       PROFILES DATA (No real private data in source)
       Name/Contact replaced with placeholders only.
    ============================================= */
    const BUREAU_PHONE = '+919969188756';
    const BUREAU_WA = '919969188756';

    const profiles = [
      { id: 'GMB-2026-0001', gender: 'Groom', age: 28, religion: 'Hindu', caste: 'Patel', subCaste: 'Kadava Patel', height: "5'10\"", education: 'MBA', occupation: 'Business', income: '₹8–12 LPA', city: 'Mumbai', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Hindi, English', horoscope: 'Libra', lifestyle: 'Vegetarian, Non-Smoker', hobbies: 'Cricket, Reading, Travel', family: 'Upper Middle Class, Nuclear Family, Business Background', description: 'Ambitious and grounded young man from a well-respected Patel business family in Mumbai. Values family traditions while embracing modern values. Seeks a life partner who is educated, independent, and family-oriented.', expectations: 'Educated bride, 24–27 years, from Gujarat. Values tradition and family.' },
      { id: 'GMB-2026-0002', gender: 'Bride', age: 25, religion: 'Jain', caste: 'Shwetambar Jain', subCaste: 'Visa Oshwal', height: "5'4\"", education: 'Post Graduate', occupation: 'Teacher', income: '₹4–6 LPA', city: 'Surat', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Hindi, English', horoscope: 'Virgo', lifestyle: 'Strict Vegetarian, Non-Smoker', hobbies: 'Yoga, Cooking, Art', family: 'Conservative Jain Family, Joint Family', description: 'Simple, cultured, and well-educated Jain girl from Surat. Deeply rooted in Jain values and traditions. Passionate about education and family. Looking for a kind-hearted life partner.', expectations: 'Jain groom, educated, employed, family-oriented. Age 27–32.' },
      { id: 'GMB-2026-0003', gender: 'Groom', age: 32, religion: 'Hindu', caste: 'Brahmin', subCaste: 'Anavil Brahmin', height: "5'8\"", education: 'Doctor (MBBS, MD)', occupation: 'Doctor', income: '₹18–25 LPA', city: 'Vadodara', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Hindi, English', horoscope: 'Scorpio', lifestyle: 'Vegetarian, Non-Smoker', hobbies: 'Music, Reading, Fitness', family: 'Well-educated Brahmin Family. Father is a retired IAS Officer.', description: 'Highly accomplished doctor from a distinguished Brahmin family in Vadodara. Practicing as a physician at a leading hospital. Values education, family harmony, and personal growth.', expectations: 'Educated bride, preferably from medical or professional background. Age 27–30.' },
      { id: 'GMB-2026-0004', gender: 'Bride', age: 27, religion: 'Hindu', caste: 'Patel', subCaste: 'Leuva Patel', height: "5'5\"", education: 'Engineer (BE Computer)', occupation: 'Software Engineer', income: '₹10–14 LPA', city: 'USA', state: 'California', country: 'USA', marital: 'Never Married', languages: 'Gujarati, Hindi, English', horoscope: 'Gemini', lifestyle: 'Vegetarian, Non-Smoker', hobbies: 'Dance, Cooking, Travel', family: 'NRI Family settled in USA. Strong Gujarati cultural values.', description: 'Well-educated NRI Gujarati girl settled in California. Working with a top tech company. Strong Gujarati values, modern outlook. Looking to settle in USA or India.', expectations: 'NRI groom preferred, employed, family-oriented. Age 29–34.' },
      { id: 'GMB-2026-0005', gender: 'Groom', age: 30, religion: 'Jain', caste: 'Digambar Jain', subCaste: 'Khandelwal', height: "5'9\"", education: 'CA', occupation: 'Chartered Accountant', income: '₹15–20 LPA', city: 'Rajkot', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Hindi, English', horoscope: 'Taurus', lifestyle: 'Strict Vegetarian, Non-Smoker, Non-Drinker', hobbies: 'Finance, Music, Meditation', family: 'Business family. Father runs diamond trading business in Rajkot.', description: 'Disciplined and successful Jain Chartered Accountant from Rajkot. Coming from a respected diamond business family. Values spirituality, discipline, and family togetherness.', expectations: 'Jain bride, educated, simple and family-oriented. Age 25–29.' },
      { id: 'GMB-2026-0006', gender: 'Bride', age: 24, religion: 'Hindu', caste: 'Vaishnav', subCaste: 'Pushtimargi Vaishnav', height: "5'3\"", education: 'B.Com, CS', occupation: 'Company Secretary', income: '₹5–7 LPA', city: 'Mumbai', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Hindi', horoscope: 'Leo', lifestyle: 'Strict Vegetarian', hobbies: 'Bhakti, Cooking, Music', family: 'Religious Vaishnav family. Strong devotional background.', description: 'Devoted Vaishnav girl from Mumbai. Deep spiritual values, yet professionally accomplished. A Company Secretary who balances modern career with traditional values.', expectations: 'Vaishnav groom, religious, employed. Age 26–30.' },
      { id: 'GMB-2026-0007', gender: 'Groom', age: 35, religion: 'Sikh', caste: 'Punjabi Khatri', subCaste: 'Khatri', height: "5'11\"", education: 'MBA (IIM)', occupation: 'Senior Manager (MNC)', income: '₹30–40 LPA', city: 'Mumbai', state: 'Gujarat', country: 'India', marital: 'Divorced', languages: 'Punjabi, Hindi, English, Gujarati', horoscope: 'Capricorn', lifestyle: 'Non-Vegetarian, Non-Smoker', hobbies: 'Cricket, Gym, Travel', family: 'Well-established Sikh family based in Mumbai. Parents retired professionals.', description: 'Highly educated IIM graduate working in a senior position with a multinational company. Divorced amicably with no children. Family-oriented and ready to begin a new chapter.', expectations: 'Educated and understanding partner. Open to divorcees. Age 28–33.' },
      { id: 'GMB-2026-0008', gender: 'Bride', age: 29, religion: 'Muslim', caste: 'Sunni', subCaste: 'Bohra', height: "5'4\"", education: 'BDS (Dentist)', occupation: 'Dentist', income: '₹8–12 LPA', city: 'Surat', state: 'Gujarat', country: 'India', marital: 'Never Married', languages: 'Gujarati, Urdu, Hindi, English', horoscope: 'Pisces', lifestyle: 'Halal, Non-Smoker', hobbies: 'Reading, Baking, Travel', family: 'Respected Dawoodi Bohra family. Father is a businessman.', description: 'Accomplished Bohra dentist from Surat. Well-cultured, educated, and family-oriented. Seeks a life partner who is equally accomplished and shares family values.', expectations: 'Educated Bohra Muslim groom. Age 30–35.' },
    ];

    const faqs = [
      { q: 'How does Gujarati Marriage Bureau work?', a: 'We begin with a personal consultation to understand your family\'s requirements and expectations. Our expert counselors then shortlist verified profiles from our database. Upon mutual interest, we facilitate the introduction. Everything is handled personally and confidentially.' },
      { q: 'Is my personal information safe with Gujarati Marriage Bureau?', a: 'Absolutely. We follow a strict privacy policy. Your name, contact number, address, and photographs are never shared without your explicit consent. Profile details are only disclosed after mutual interest is confirmed from both families.' },
      { q: 'What communities does Gujarati Marriage Bureau serve?', a: 'We serve all Gujarati communities including Hindu (Patel, Brahmin, Vaishnav, Lohana, Kshatriya, Bania), Jain (Shwetambar, Digambar), Sikh, Muslim, and Christian families. We also have an extensive NRI Gujarati database.' },
      { q: 'Can I see NRI profiles?', a: 'Yes. We have NRI Gujarati profiles from USA, UK, Canada, Australia, and other countries. Gold and Diamond membership holders get priority access to NRI profiles.' },
      { q: 'How do I unlock a profile\'s contact details?', a: 'Simply call or WhatsApp us with the Profile ID. After verifying your identity and confirming your membership, our team will personally share the complete profile contact details with you. We do not process payments online for security reasons.' },
      { q: 'How long does the matchmaking process take?', a: 'It varies for each family and the candidate choice, mutual feelings and understanding, We do not give any type of Guarantee.' },
      { q: 'Is there an online payment option?', a: 'We process payments online to ensure maximum security. All membership fees are collected via after calls. We also accept payments via trusted bank transfer after registration.' }
    ];

    /* =============================================
       RENDER PROFILE CARDS
    ============================================= */
    function renderProfiles(data) {
      const grid = document.getElementById('profilesGrid');
      const count = document.getElementById('resultsCount');
      grid.innerHTML = '';
      count.textContent = data.length + ' profile' + (data.length !== 1 ? 's' : '') + ' found';
      if (data.length === 0) {
        grid.innerHTML = '<div class="no-profiles">No profiles match your search. Try adjusting your filters.</div>';
        return;
      }
      data.forEach(function (p) {
        const emoji = p.gender === 'Bride' ? '👰' : '🤵';
        const card = document.createElement('div');
        card.className = 'profile-card';
        card.setAttribute('role', 'listitem');
        card.innerHTML = `
      <div class="profile-card-header">
        <div class="profile-avatar" aria-hidden="true">${emoji}</div>
        <div class="profile-header-info">
          <div class="profile-id">${p.id}</div>
          <div style="font-weight:700;color:rgba(255,255,255,0.9);margin-top:4px;">${p.age} yrs • ${p.height}</div>
          <div class="profile-tag-row">
            <span class="ptag">${p.gender}</span>
            <span class="ptag">${p.religion}</span>
            <span class="ptag">${p.city}</span>
          </div>
        </div>
        <div class="profile-status-dot" aria-label="Active profile"></div>
      </div>
      <div class="profile-card-body">
        <div class="profile-info-row">
          <span class="pinfo-label">Education</span>
          <span class="pinfo-value">${p.education}</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Occupation</span>
          <span class="pinfo-value">${p.occupation}</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Income</span>
          <span class="pinfo-value">${p.income}</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Caste</span>
          <span class="pinfo-value">${p.caste}</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Marital Status</span>
          <span class="pinfo-value">${p.marital}</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Name</span>
          <span class="pinfo-hidden protected" aria-label="Hidden for privacy">Hidden for Privacy</span>
        </div>
        <div class="profile-info-row">
          <span class="pinfo-label">Contact</span>
          <span class="pinfo-hidden protected" aria-label="Available after approval">Available After Approval</span>
        </div>
      </div>
      <div class="profile-card-footer">
        <button class="btn-view-profile" onclick="openProfileModal('${p.id}')" aria-label="View full profile for ${p.id}">View Profile</button>
        <button class="btn-unlock" onclick="openUnlockModal('${p.id}')" aria-label="Unlock contact details for profile ${p.id}">🔓 Unlock</button>
      </div>
    `;
        grid.appendChild(card);
      });
    }

    document.addEventListener("DOMContentLoaded", function () {
      renderProfiles(profiles); // or whatever your profiles array is called
    });
    /* =============================================
       FILTERING
    ============================================= */
    function sanitize(str) {
      return String(str).trim().replace(/[<>\"']/g, '');
    }

    function applyFilters() {
      const id = sanitize(document.getElementById('f-id').value).toLowerCase();
      const gender = sanitize(document.getElementById('f-gender').value);
      const religion = sanitize(document.getElementById('f-religion').value);
      const ageMin = parseInt(document.getElementById('f-age-min').value) || 0;
      const ageMax = parseInt(document.getElementById('f-age-max').value) || 999;
      const education = sanitize(document.getElementById('f-education').value);
      const city = sanitize(document.getElementById('f-city').value);
      const marital = sanitize(document.getElementById('f-marital').value);

      const filtered = profiles.filter(function (p) {
        if (id && !p.id.toLowerCase().includes(id)) return false;
        if (gender && p.gender !== gender) return false;
        if (religion && p.religion !== religion) return false;
        if (p.age < ageMin || p.age > ageMax) return false;
        if (education && !p.education.toLowerCase().includes(education.toLowerCase())) return false;
        if (city && p.city !== city) return false;
        if (marital && p.marital !== marital) return false;
        return true;
      });
      renderProfiles(filtered);
    }

    function resetFilters() {
      ['f-id', 'f-gender', 'f-religion', 'f-age-min', 'f-age-max', 'f-education', 'f-city', 'f-marital'].forEach(function (id) {
        const el = document.getElementById(id);
        el.value = '';
      });
      renderProfiles(profiles);
    }

    function filterByTag(tag) {
      document.getElementById('f-religion').value = tag;
      document.getElementById('profiles').scrollIntoView({ behavior: 'smooth' });
      setTimeout(applyFilters, 400);
    }

    // Debounce search
    let debounceTimer;
    document.getElementById('f-id').addEventListener('input', function () {
      clearTimeout(debounceTimer);
      debounceTimer = setTimeout(applyFilters, 350);
    });

    document.getElementById('applyFilters').addEventListener('click', applyFilters);
    document.getElementById('resetFilters').addEventListener('click', resetFilters);

    /* =============================================
       MODALS
    ============================================= */
    function openModal(id) {
      const m = document.getElementById(id);
      m.classList.add('open');
      document.body.style.overflow = 'hidden';
      m.querySelector('[class*="modal-close"], .btn-cancel-modal') && null;
      // Focus trap - focus first focusable element
      const focusable = m.querySelectorAll('button, a, input, select, textarea, [tabindex]');
      if (focusable[0]) focusable[0].focus();
    }

    function closeModal(id) {
      document.getElementById(id).classList.remove('open');
      document.body.style.overflow = '';
    }

    // Close modal on overlay click
    document.querySelectorAll('.modal-overlay').forEach(function (overlay) {
      overlay.addEventListener('click', function (e) {
        if (e.target === overlay) closeModal(overlay.id);
      });
    });

    // Close on Escape key
    document.addEventListener('keydown', function (e) {
      if (e.key === 'Escape') {
        document.querySelectorAll('.modal-overlay.open').forEach(function (m) {
          closeModal(m.id);
        });
      }
    });

    function openUnlockModal(profileId) {
      document.getElementById('unlockProfileId').textContent = profileId;
      const waMsg = encodeURIComponent('Hello,\n\nI would like to unlock Profile ID: ' + profileId + '.\n\nPlease share the payment details and process.\n\nThank you.');
      document.getElementById('unlockWABtn').href = 'https://wa.me/' + BUREAU_WA + '?text=' + waMsg;
      openModal('unlockModal');
    }

    function openProfileModal(profileId) {
      const p = profiles.find(function (pr) { return pr.id === profileId; });
      if (!p) return;
      const emoji = p.gender === 'Bride' ? '👰' : '🤵';
      const content = document.getElementById('profileModalContent');
      content.innerHTML = `
    <div class="pmodal-hero">
      <div class="pmodal-avatar" aria-hidden="true">${emoji}</div>
      <div>
        <div class="pmodal-id">${p.id}</div>
        <div class="pmodal-name" style="font-size:1.1rem;font-weight:700;">${p.gender} • ${p.age} years • ${p.height}</div>
        <div style="font-size:0.85rem;opacity:0.8;">${p.city}, ${p.state}, ${p.country}</div>
        <div class="pmodal-tags">
          <span class="pmodal-tag">${p.religion}</span>
          <span class="pmodal-tag">${p.caste}</span>
          <span class="pmodal-tag">${p.occupation}</span>
          <span class="pmodal-tag">${p.marital}</span>
        </div>
      </div>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">Personal Information</div>
      <div class="pmodal-info-grid">
        <div class="pmodal-info-item"><div class="pmodal-info-label">Age</div><div class="pmodal-info-value">${p.age} years</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Height</div><div class="pmodal-info-value">${p.height}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Religion</div><div class="pmodal-info-value">${p.religion}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Caste</div><div class="pmodal-info-value">${p.caste}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Sub Caste</div><div class="pmodal-info-value">${p.subCaste}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Marital Status</div><div class="pmodal-info-value">${p.marital}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Horoscope</div><div class="pmodal-info-value">${p.horoscope}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Languages</div><div class="pmodal-info-value">${p.languages}</div></div>
      </div>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">Education & Career</div>
      <div class="pmodal-info-grid">
        <div class="pmodal-info-item"><div class="pmodal-info-label">Education</div><div class="pmodal-info-value">${p.education}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Occupation</div><div class="pmodal-info-value">${p.occupation}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Annual Income</div><div class="pmodal-info-value">${p.income}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">City</div><div class="pmodal-info-value">${p.city}, ${p.state}</div></div>
      </div>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">Lifestyle & Family</div>
      <div class="pmodal-info-grid">
        <div class="pmodal-info-item"><div class="pmodal-info-label">Lifestyle</div><div class="pmodal-info-value">${p.lifestyle}</div></div>
        <div class="pmodal-info-item"><div class="pmodal-info-label">Hobbies</div><div class="pmodal-info-value">${p.hobbies}</div></div>
      </div>
      <div style="margin-top:12px;padding:14px;background:var(--gray-100);border-radius:var(--radius-sm);">
        <div class="pmodal-info-label" style="margin-bottom:6px;">Family Background</div>
        <div style="font-size:0.875rem;color:var(--text-secondary);">${p.family}</div>
      </div>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">About This Profile</div>
      <p class="pmodal-desc">${p.description}</p>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">Partner Expectations</div>
      <p class="pmodal-desc">${p.expectations}</p>
    </div>

    <div class="pmodal-section">
      <div class="pmodal-section-title">Private Information (Locked)</div>
      <div class="pmodal-info-grid">
        <div class="pmodal-info-item">
          <div class="pmodal-info-label">Full Name</div>
          <div class="pmodal-locked-badge" aria-label="Name hidden for privacy">🔒 Hidden for Privacy</div>
        </div>
        <div class="pmodal-info-item">
          <div class="pmodal-info-label">Mobile Number</div>
          <div class="pmodal-locked-badge" aria-label="Contact available after approval">🔒 After Approval</div>
        </div>
        <div class="pmodal-info-item">
          <div class="pmodal-info-label">WhatsApp</div>
          <div class="pmodal-locked-badge" aria-label="WhatsApp available after approval">🔒 After Approval</div>
        </div>
        <div class="pmodal-info-item">
          <div class="pmodal-info-label">Email / Address</div>
          <div class="pmodal-locked-badge" aria-label="Email available after approval">🔒 After Approval</div>
        </div>
      </div>
    </div>

    <div class="pmodal-unlock-bar">
      <div class="pmodal-unlock-text">
        <strong>Want to connect with this profile?</strong><br>
        Contact our bureau with Profile ID <strong>${p.id}</strong>
      </div>
      <button class="btn-primary" onclick="closeModal('profileModal');openUnlockModal('${p.id}')">
        🔓 Unlock Details
      </button>
    </div>
  `;
      document.getElementById('profileModalTitle').textContent = 'Profile ' + p.id;
      openModal('profileModal');
    }

    /* =============================================
       FAQ ACCORDION
    ============================================= */
    function renderFAQs() {
      const list = document.getElementById("faqList");

      if (!list) {
        console.error("Element with id 'faqList' not found.");
        return;
      }

      list.innerHTML = "";

      faqs.forEach((faq, i) => {
        const item = document.createElement("div");
        item.className = "faq-item";
        item.setAttribute("role", "listitem");

        item.innerHTML = `
      <div
        class="faq-q"
        tabindex="0"
        role="button"
        aria-expanded="false"
        aria-controls="faq-a-${i}"
        id="faq-q-${i}"
      >
        <span>${faq.q}</span>
        <div class="faq-icon">+</div>
      </div>

      <div
        class="faq-a"
        id="faq-a-${i}"
        role="region"
        aria-labelledby="faq-q-${i}"
        style="max-height:0; overflow:hidden; transition:max-height .3s ease;"
      >
        <div class="faq-a-inner">
          ${faq.a}
        </div>
      </div>
    `;

        list.appendChild(item);

        const question = item.querySelector(".faq-q");
        const answer = item.querySelector(".faq-a");
        const answerInner = item.querySelector(".faq-a-inner");
        const icon = item.querySelector(".faq-icon");

        function toggleFAQ() {
          const isOpen = item.classList.contains("open");

          // Close all FAQs
          document.querySelectorAll(".faq-item.open").forEach(openItem => {
            openItem.classList.remove("open");

            const openAnswer = openItem.querySelector(".faq-a");
            const openQuestion = openItem.querySelector(".faq-q");
            const openIcon = openItem.querySelector(".faq-icon");

            openAnswer.style.maxHeight = "0";
            openQuestion.setAttribute("aria-expanded", "false");
            openIcon.textContent = "+";
          });

          // Open clicked FAQ
          if (!isOpen) {
            item.classList.add("open");
            answer.style.maxHeight = answerInner.scrollHeight + "px";
            question.setAttribute("aria-expanded", "true");
            icon.textContent = "−";
          }
        }

        question.addEventListener("click", toggleFAQ);

        question.addEventListener("keydown", (e) => {
          if (e.key === "Enter" || e.key === " ") {
            e.preventDefault();
            toggleFAQ();
          }
        });
      });
    }

    // Run after the page loads
    document.addEventListener("DOMContentLoaded", renderFAQs);

    /* =============================================
       NAVIGATION
    ============================================= */
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', function () {
      navbar.classList.toggle('scrolled', window.scrollY > 60);
      const btn = document.getElementById('back-to-top');
      btn.style.display = window.scrollY > 400 ? 'flex' : 'none';
    }, { passive: true });

    document.getElementById('menuBtn').addEventListener('click', function () {
      const nav = document.getElementById('mobileNav');
      const btn = document.getElementById('menuBtn');
      const isOpen = nav.classList.toggle('open');
      btn.setAttribute('aria-expanded', isOpen ? 'true' : 'false');
    });

    document.querySelectorAll('.mobile-nav a').forEach(function (a) {
      a.addEventListener('click', function () {
        document.getElementById('mobileNav').classList.remove('open');
        document.getElementById('menuBtn').setAttribute('aria-expanded', 'false');
      });
    });

    document.getElementById('back-to-top').addEventListener('click', function () {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    /* =============================================
       SCROLL REVEAL
    ============================================= */
    const revealObserver = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          revealObserver.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

    document.querySelectorAll('.reveal, .reveal-left, .reveal-right').forEach(function (el) {
      revealObserver.observe(el);
    });

    /* =============================================
       ANIMATED COUNTERS
    ============================================= */
    function animateCounter(el) {
      const target = parseInt(el.dataset.target);
      const suffix = el.dataset.suffix || '';
      const duration = 1800;
      const start = performance.now();
      function step(now) {
        const elapsed = now - start;
        const progress = Math.min(elapsed / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3);
        el.textContent = Math.floor(eased * target).toLocaleString('en-IN') + suffix;
        if (progress < 1) requestAnimationFrame(step);
      }
      requestAnimationFrame(step);
    }

    const counterObserver = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.querySelectorAll('[data-target]').forEach(animateCounter);
          counterObserver.unobserve(entry.target);
        }
      });
    }, { threshold: 0.3 });

    const statsSection = document.querySelector('.stats-grid');
    if (statsSection) counterObserver.observe(statsSection);

    /* =============================================
       CONTACT FORM
    ============================================= */
    function showToast(msg, type) {
      const container = document.getElementById('toastContainer');
      const toast = document.createElement('div');
      toast.className = 'toast ' + (type || '');
      toast.textContent = msg;
      container.appendChild(toast);
      setTimeout(function () {
        toast.style.opacity = '0';
        toast.style.transition = 'opacity 0.4s';
        setTimeout(function () { toast.remove(); }, 400);
      }, 3500);
    }

    document.getElementById('contactForm').addEventListener('submit', function (e) {
      e.preventDefault();
      const name = document.getElementById('cf-name').value.trim();
      const phone = document.getElementById('cf-phone').value.trim();
      if (!name) { showToast('Please enter your full name.', 'error'); return; }
      if (!phone || phone.length < 10) { showToast('Please enter a valid mobile number.', 'error'); return; }
      // Simulate form submission (UI only - would need backend in real scenario)
      showToast('✓ Thank you ' + name + '! We will contact you within 24 hours.', 'success');
      this.reset();
    });

    /* =============================================
       LAZY LOAD IMAGES (observer-based)
    ============================================= */
    if ('IntersectionObserver' in window) {
      const lazyImages = document.querySelectorAll('img[loading="lazy"]');
      const imageObserver = new IntersectionObserver(function (entries) {
        entries.forEach(function (entry) {
          if (entry.isIntersecting) {
            const img = entry.target;
            if (img.dataset.src) img.src = img.dataset.src;
            imageObserver.unobserve(img);
          }
        });
      });
      lazyImages.forEach(function (img) { imageObserver.observe(img); });
    }

    /* =============================================
       INIT
    ============================================= */
    renderProfiles(profiles);
    renderFAQs();

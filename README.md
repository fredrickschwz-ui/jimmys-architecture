<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JIMMY S. | Architecture & Development</title>
    <!-- Google Fonts: Inter & Cormorant Garamond for corporate editorial refinement -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        alabaster: '#F9F9F8',
                        stonewarm: '#E8E6E1',
                        obsidian: '#1A1A1A',
                        slate: '#5C5C5C',
                        bronze: '#9A7B56',
                        bronzedark: '#7D6242'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Cormorant Garamond', 'serif'],
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-alabaster text-obsidian font-sans antialiased selection:bg-bronze selection:text-white flex flex-col min-h-screen">

    <!-- Top Sticky Minimalist Navigation -->
    <header class="sticky top-0 z-40 bg-alabaster/95 backdrop-blur-md border-b border-obsidian/10">
        <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
            <div class="flex items-center justify-between h-20">
                <!-- Brand Mark -->
                <button onclick="navigateTo('main')" class="flex items-center gap-3 text-left group focus:outline-none">
                    <div class="w-8 h-8 border border-obsidian flex items-center justify-center transition-colors group-hover:bg-obsidian group-hover:text-alabaster">
                        <span class="font-serif text-lg font-semibold tracking-tighter">JS</span>
                    </div>
                    <div>
                        <span class="block text-xs sm:text-sm font-semibold tracking-[0.22em] uppercase text-obsidian">JIMMY S.</span>
                        <span class="block text-[10px] tracking-[0.18em] uppercase text-slate">Architecture & Development</span>
                    </div>
                </button>

                <!-- Desktop Navigation Links -->
                <nav class="hidden md:flex items-center space-x-10">
                    <button id="nav-main" onclick="navigateTo('main')" class="text-xs uppercase tracking-[0.18em] font-medium py-2 border-b-2 border-obsidian text-obsidian transition-all">
                        Overview &amp; Projects
                    </button>
                    <button id="nav-about" onclick="navigateTo('about')" class="text-xs uppercase tracking-[0.18em] font-medium py-2 border-b-2 border-transparent text-slate hover:text-obsidian transition-all">
                        About Jimmy S.
                    </button>
                    <button onclick="scrollToContact()" class="px-5 py-2.5 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronze transition-colors rounded-sm">
                        Inquire
                    </button>
                </nav>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" onclick="toggleMobileMenu()" aria-label="Toggle Menu" class="p-2 text-obsidian hover:text-bronze focus:outline-none">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="square" stroke-linejoin="miter" stroke-width="1.5" d="M4 7h16M4 12h16M4 17h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Dropdown Navigation -->
        <div id="mobile-menu" class="hidden md:hidden bg-alabaster border-b border-obsidian/10 px-6 py-6 space-y-4">
            <button id="mobile-nav-main" onclick="navigateTo('main'); toggleMobileMenu();" class="block w-full text-left text-xs uppercase tracking-[0.18em] font-semibold text-obsidian py-2">
                01 / Overview &amp; Projects
            </button>
            <button id="mobile-nav-about" onclick="navigateTo('about'); toggleMobileMenu();" class="block w-full text-left text-xs uppercase tracking-[0.18em] font-medium text-slate py-2">
                02 / About Jimmy S.
            </button>
            <div class="pt-2 border-t border-obsidian/10">
                <button onclick="toggleMobileMenu(); scrollToContact();" class="w-full py-3 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium text-center rounded-sm">
                    Direct Consultation
                </button>
            </div>
        </div>
    </header>

    <!-- ===================================================================== -->
    <!-- PAGE 1: MAIN PAGE (ARCHITECTURAL DESIGN & URBAN DEVELOPMENT)          -->
    <!-- ===================================================================== -->
    <main id="page-main" class="flex-grow transition-opacity duration-300">
        
        <!-- Hero Section -->
        <section class="border-b border-obsidian/10">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12 py-12 lg:py-20">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 lg:gap-12 items-center">
                    <!-- Left Editorial Column -->
                    <div class="lg:col-span-5 space-y-8">
                        <div class="inline-flex items-center gap-2.5 px-3 py-1 bg-stonewarm/70 border border-obsidian/10 rounded-sm">
                            <span class="w-1.5 h-1.5 rounded-full bg-bronze"></span>
                            <span class="text-[11px] uppercase tracking-[0.2em] text-slate font-medium">Principal-Led Practice</span>
                        </div>
                        
                        <h1 class="text-4xl sm:text-5xl lg:text-[54px] font-light tracking-tight leading-[1.08] text-obsidian">
                            Precision in <span class="font-serif italic font-normal text-bronze">Spatial Design</span> &amp; Urban Development.
                        </h1>
                        
                        <p class="text-base text-slate leading-relaxed font-light">
                            Directed by Principal Architect &amp; Developer <strong class="font-medium text-obsidian">Jimmy S.</strong>, our firm integrates architectural rigor with commercial development discipline—delivering enduring institutional, commercial, and residential landmarks.
                        </p>

                        <div class="pt-2 flex flex-col sm:flex-row gap-4">
                            <a href="#portfolio-section" class="px-7 py-3.5 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronze transition-colors text-center rounded-sm">
                                Explore Portfolio
                            </a>
                            <button onclick="scrollToContact()" class="px-7 py-3.5 border border-obsidian text-obsidian text-xs uppercase tracking-[0.18em] font-medium hover:bg-stonewarm transition-colors text-center rounded-sm">
                                Contact Jimmy S.
                            </button>
                        </div>

                        <!-- Key Metrics Strip -->
                        <div class="pt-8 border-t border-obsidian/10 grid grid-cols-3 gap-6">
                            <div>
                                <p class="text-2xl font-light text-obsidian">18+</p>
                                <p class="text-[11px] uppercase tracking-[0.14em] text-slate mt-1">Years Practice</p>
                            </div>
                            <div>
                                <p class="text-2xl font-light text-obsidian">$1.4B</p>
                                <p class="text-[11px] uppercase tracking-[0.14em] text-slate mt-1">Developed Value</p>
                            </div>
                            <div>
                                <p class="text-2xl font-light text-obsidian">42</p>
                                <p class="text-[11px] uppercase tracking-[0.14em] text-slate mt-1">Built Works</p>
                            </div>
                        </div>
                    </div>

                    <!-- Right Architectural Showcase Image -->
                    <div class="lg:col-span-7">
                        <div class="relative bg-stonewarm border border-obsidian/10 overflow-hidden rounded-sm group">
                            <img 
                                src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=1600&q=85" 
                                alt="Monolithic Glass and Concrete Corporate Tower" 
                                onerror="this.src='https://placehold.co/1200x800/E8E6E1/1A1A1A?text=JIMMY+S.+ARCHITECTURE'"
                                class="w-full h-[420px] sm:h-[540px] object-cover object-center transition-transform duration-700 group-hover:scale-[1.02]"
                            >
                            <div class="bg-alabaster/95 backdrop-blur-sm border-t border-obsidian/10 px-6 py-4 flex flex-wrap items-center justify-between gap-4">
                                <div>
                                    <span class="text-[10px] uppercase tracking-[0.2em] text-bronze font-semibold block">Featured Commission</span>
                                    <span class="text-sm font-medium text-obsidian">The Sterling Financial Pavilion — Chicago, IL</span>
                                </div>
                                <span class="text-xs uppercase tracking-[0.15em] text-slate">340,000 SQ FT / 2025</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Core Capabilities / Services Strip -->
        <section class="border-b border-obsidian/10 bg-stonewarm/40">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12 py-16 lg:py-24">
                <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
                    <div>
                        <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Core Disciplines</span>
                        <h2 class="text-2xl sm:text-3xl font-light tracking-tight text-obsidian">Integrated Architecture &amp; Capital Stewardship</h2>
                    </div>
                    <p class="text-sm text-slate max-w-md font-light">
                        Eliminating friction between visionary architectural form and financial feasibility through single-point principal accountability.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 border-t border-l border-obsidian/10 bg-alabaster">
                    <!-- Discipline 1 -->
                    <div class="p-8 lg:p-10 border-r border-b border-obsidian/10 flex flex-col justify-between hover:bg-stonewarm/25 transition-colors">
                        <div>
                            <span class="text-xs font-mono text-bronze tracking-widest block mb-6">01 / DESIGN</span>
                            <h3 class="text-xl font-medium text-obsidian mb-4">Architectural Design</h3>
                            <p class="text-sm text-slate leading-relaxed font-light">
                                Comprehensive architectural services from schematic concept through construction administration, emphasizing structural clarity, natural daylighting, and tactile longevity.
                            </p>
                        </div>
                        <div class="mt-8 pt-4 border-t border-obsidian/10 text-[11px] uppercase tracking-[0.16em] text-obsidian font-medium">
                            Commercial • Civic • Bespoke Residential
                        </div>
                    </div>

                    <!-- Discipline 2 -->
                    <div class="p-8 lg:p-10 border-r border-b border-obsidian/10 flex flex-col justify-between hover:bg-stonewarm/25 transition-colors">
                        <div>
                            <span class="text-xs font-mono text-bronze tracking-widest block mb-6">02 / DEVELOPMENT</span>
                            <h3 class="text-xl font-medium text-obsidian mb-4">Real Estate &amp; Urban Development</h3>
                            <p class="text-sm text-slate leading-relaxed font-light">
                                End-to-end development advisory, site acquisition underwriting, entitlement navigation, and capital structuring led directly by Jimmy S. to maximize long-term asset yield.
                            </p>
                        </div>
                        <div class="mt-8 pt-4 border-t border-obsidian/10 text-[11px] uppercase tracking-[0.16em] text-obsidian font-medium">
                            Feasibility • Entitlements • Joint Ventures
                        </div>
                    </div>

                    <!-- Discipline 3 -->
                    <div class="p-8 lg:p-10 border-r border-b border-obsidian/10 flex flex-col justify-between hover:bg-stonewarm/25 transition-colors">
                        <div>
                            <span class="text-xs font-mono text-bronze tracking-widest block mb-6">03 / EXECUTION</span>
                            <h3 class="text-xl font-medium text-obsidian mb-4">Master Planning &amp; Execution</h3>
                            <p class="text-sm text-slate leading-relaxed font-light">
                                Multi-phase campus frameworks, adaptive reuse strategies, and owner representation ensuring strict adherence to budget tolerances, schedules, and LEED Platinum standards.
                            </p>
                        </div>
                        <div class="mt-8 pt-4 border-t border-obsidian/10 text-[11px] uppercase tracking-[0.16em] text-obsidian font-medium">
                            Urban Infill • Adaptive Reuse • Sustainability
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Curated Architectural Image Gallery -->
        <section id="portfolio-section" class="border-b border-obsidian/10 py-16 lg:py-24">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
                <!-- Gallery Header & Filter Controls -->
                <div class="flex flex-col lg:flex-row lg:items-end justify-between mb-12 gap-8">
                    <div>
                        <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Selected Works &amp; Precedents</span>
                        <h2 class="text-3xl sm:text-4xl font-light tracking-tight text-obsidian">Architectural Portfolio Gallery</h2>
                    </div>

                    <!-- Filter Buttons -->
                    <div class="flex flex-wrap gap-2" role="tablist" aria-label="Filter architectural projects">
                        <button onclick="filterProjects('All')" data-filter="All" class="filter-btn px-4 py-2 text-xs uppercase tracking-[0.16em] font-medium bg-obsidian text-alabaster border border-obsidian transition-colors rounded-sm">
                            All Works
                        </button>
                        <button onclick="filterProjects('Commercial')" data-filter="Commercial" class="filter-btn px-4 py-2 text-xs uppercase tracking-[0.16em] font-medium bg-transparent text-slate border border-obsidian/20 hover:border-obsidian hover:text-obsidian transition-colors rounded-sm">
                            Commercial
                        </button>
                        <button onclick="filterProjects('Residential')" data-filter="Residential" class="filter-btn px-4 py-2 text-xs uppercase tracking-[0.16em] font-medium bg-transparent text-slate border border-obsidian/20 hover:border-obsidian hover:text-obsidian transition-colors rounded-sm">
                            Residential
                        </button>
                        <button onclick="filterProjects('Urban Development')" data-filter="Urban Development" class="filter-btn px-4 py-2 text-xs uppercase tracking-[0.16em] font-medium bg-transparent text-slate border border-obsidian/20 hover:border-obsidian hover:text-obsidian transition-colors rounded-sm">
                            Urban Development
                        </button>
                    </div>
                </div>

                <!-- Gallery Grid -->
                <div id="gallery-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Populated via JavaScript for clean state management and modal inspection -->
                </div>
            </div>
        </section>

        <!-- Direct Contact / Consultation Section -->
        <section id="contact-section" class="bg-stonewarm/50 py-16 lg:py-24">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
                    <!-- Left: Main Contact Details (Jimmy S.) -->
                    <div class="lg:col-span-5 space-y-8">
                        <div>
                            <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Direct Inquiries</span>
                            <h2 class="text-3xl sm:text-4xl font-light tracking-tight text-obsidian">Initiate a Development or Design Dialogue.</h2>
                        </div>

                        <p class="text-sm text-slate leading-relaxed font-light">
                            All prospective commissions, land development partnerships, and architectural consultations are reviewed directly by our founding principal.
                        </p>

                        <!-- Executive Contact Card -->
                        <div class="bg-alabaster border border-obsidian/15 p-8 rounded-sm space-y-6">
                            <div class="flex items-center justify-between border-b border-obsidian/10 pb-5">
                                <div>
                                    <span class="text-[10px] uppercase tracking-[0.2em] text-bronze font-semibold block">Main Contact</span>
                                    <h3 class="text-xl font-medium text-obsidian mt-0.5">Jimmy S., AIA, LEED AP</h3>
                                    <p class="text-xs text-slate mt-0.5">Principal Architect &amp; Managing Developer</p>
                                </div>
                                <button onclick="navigateTo('about')" class="text-xs uppercase tracking-[0.15em] text-bronze hover:text-obsidian underline underline-offset-4 font-medium">
                                    View Profile
                                </button>
                            </div>

                            <div class="space-y-4 text-sm">
                                <div class="flex items-start justify-between gap-4">
                                    <span class="text-xs uppercase tracking-[0.15em] text-slate">Direct Email</span>
                                    <div class="flex items-center gap-2">
                                        <span id="jimmy-email" class="font-medium text-obsidian">jimmy@jimmysarchitecture.com</span>
                                        <button onclick="copyEmail()" title="Copy Email" class="p-1.5 text-slate hover:text-obsidian border border-obsidian/15 rounded-sm text-[10px] uppercase tracking-wider">
                                            Copy
                                        </button>
                                    </div>
                                </div>
                                <div class="flex items-center justify-between gap-4">
                                    <span class="text-xs uppercase tracking-[0.15em] text-slate">Direct Line</span>
                                    <span class="font-medium text-obsidian">+1 (312) 555-0194</span>
                                </div>
                                <div class="flex items-start justify-between gap-4">
                                    <span class="text-xs uppercase tracking-[0.15em] text-slate">Headquarters</span>
                                    <span class="font-medium text-obsidian text-right">440 N. Wells Street, Suite 700<br>Chicago, IL 60654</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Right: Corporate Consultation Form -->
                    <div class="lg:col-span-7 bg-alabaster border border-obsidian/15 p-8 sm:p-10 rounded-sm">
                        <h3 class="text-lg font-medium text-obsidian mb-6 pb-4 border-b border-obsidian/10">Project &amp; Partnership Brief</h3>
                        
                        <form id="inquiry-form" onsubmit="handleInquirySubmit(event)" class="space-y-6">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label for="client-name" class="block text-xs uppercase tracking-[0.15em] text-slate mb-2">Full Name *</label>
                                    <input type="text" id="client-name" required placeholder="e.g., Elena Vance" class="w-full px-4 py-3 bg-alabaster border border-obsidian/20 text-sm text-obsidian focus:outline-none focus:border-obsidian rounded-sm">
                                </div>
                                <div>
                                    <label for="client-org" class="block text-xs uppercase tracking-[0.15em] text-slate mb-2">Organization / Firm</label>
                                    <input type="text" id="client-org" placeholder="e.g., Vance Capital Partners" class="w-full px-4 py-3 bg-alabaster border border-obsidian/20 text-sm text-obsidian focus:outline-none focus:border-obsidian rounded-sm">
                                </div>
                            </div>

                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label for="client-email" class="block text-xs uppercase tracking-[0.15em] text-slate mb-2">Corporate Email *</label>
                                    <input type="email" id="client-email" required placeholder="name@company.com" class="w-full px-4 py-3 bg-alabaster border border-obsidian/20 text-sm text-obsidian focus:outline-none focus:border-obsidian rounded-sm">
                                </div>
                                <div>
                                    <label for="project-scope" class="block text-xs uppercase tracking-[0.15em] text-slate mb-2">Inquiry Scope</label>
                                    <select id="project-scope" class="w-full px-4 py-3 bg-alabaster border border-obsidian/20 text-sm text-obsidian focus:outline-none focus:border-obsidian rounded-sm">
                                        <option value="Commercial Architecture">Commercial Architecture</option>
                                        <option value="Real Estate & Urban Development">Real Estate &amp; Urban Development</option>
                                        <option value="Private Residential Commission">Private Residential Commission</option>
                                        <option value="Joint Venture / Site Advisory">Joint Venture / Site Advisory</option>
                                    </select>
                                </div>
                            </div>

                            <div>
                                <label for="project-notes" class="block text-xs uppercase tracking-[0.15em] text-slate mb-2">Site Location, Timeline &amp; Objectives *</label>
                                <textarea id="project-notes" rows="4" required placeholder="Provide a brief summary of your site, estimated square footage, or development goals for Jimmy S.'s review..." class="w-full px-4 py-3 bg-alabaster border border-obsidian/20 text-sm text-obsidian focus:outline-none focus:border-obsidian rounded-sm"></textarea>
                            </div>

                            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 pt-2">
                                <span class="text-xs text-slate">Confidentiality assured under standard NDA protocol.</span>
                                <button type="submit" class="px-8 py-3.5 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronze transition-colors rounded-sm">
                                    Transmit to Jimmy S.
                                </button>
                            </div>
                        </form>

                        <!-- Submission Confirmation Banner (Hidden by default) -->
                        <div id="inquiry-confirmation" class="hidden mt-6 p-6 bg-stonewarm border-l-4 border-bronze rounded-sm">
                            <p class="text-xs uppercase tracking-[0.18em] text-bronze font-semibold mb-1">Brief Logged &amp; Routed</p>
                            <p class="text-sm text-obsidian font-medium">Thank you. Your project dossier has been transmitted directly to Jimmy S.'s desk.</p>
                            <p class="text-xs text-slate mt-1">Expect a direct response within one business day.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- ===================================================================== -->
    <!-- PAGE 2: ABOUT JIMMY S. (PRINCIPAL ARCHITECT & DEVELOPMENT DIRECTOR)   -->
    <!-- ===================================================================== -->
    <main id="page-about" class="hidden flex-grow transition-opacity duration-300">
        
        <!-- Editorial Profile Header -->
        <section class="border-b border-obsidian/10">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12 py-12 lg:py-20">
                <div class="mb-8">
                    <button onclick="navigateTo('main')" class="inline-flex items-center gap-2 text-xs uppercase tracking-[0.18em] text-slate hover:text-obsidian transition-colors">
                        <span>&larr;</span>
                        <span>Back to Overview &amp; Projects</span>
                    </button>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                    <!-- Portrait / Studio Frame -->
                    <div class="lg:col-span-5">
                        <div class="bg-stonewarm border border-obsidian/15 p-3 rounded-sm">
                            <div class="overflow-hidden bg-obsidian">
                                <img 
                                    src="https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=1000&q=85" 
                                    alt="Jimmy S. — Principal Architect & Development Director" 
                                    onerror="this.src='https://placehold.co/800x960/E8E6E1/1A1A1A?text=JIMMY+S.+PRINCIPAL'"
                                    class="w-full h-[460px] sm:h-[520px] object-cover object-top grayscale contrast-110"
                                >
                            </div>
                            <div class="pt-4 pb-1 px-2 flex items-center justify-between">
                                <div>
                                    <p class="text-sm font-semibold text-obsidian">Jimmy S.</p>
                                    <p class="text-xs text-slate">Principal Architect &amp; Founder</p>
                                </div>
                                <span class="text-[11px] uppercase tracking-[0.16em] text-bronze font-medium">AIA • NCARB • LEED AP</span>
                            </div>
                        </div>
                    </div>

                    <!-- Editorial Bio Header -->
                    <div class="lg:col-span-7 space-y-8">
                        <div class="inline-flex items-center gap-2.5 px-3 py-1 bg-stonewarm/70 border border-obsidian/10 rounded-sm">
                            <span class="w-1.5 h-1.5 rounded-full bg-bronze"></span>
                            <span class="text-[11px] uppercase tracking-[0.2em] text-slate font-medium">Leadership &amp; Practice Profile</span>
                        </div>

                        <h1 class="text-3xl sm:text-5xl font-light tracking-tight leading-[1.12] text-obsidian">
                            Jimmy S. — Principal Architect &amp; <span class="font-serif italic font-normal text-bronze">Development Director.</span>
                        </h1>

                        <blockquote class="border-l-2 border-bronze pl-6 py-1 text-lg sm:text-xl font-serif italic text-obsidian/90 leading-relaxed">
                            “Great architecture is never divorced from economic reality. When structural honesty meets disciplined capital stewardship, buildings endure for generations.”
                        </blockquote>

                        <p class="text-base text-slate leading-relaxed font-light">
                            With nearly two decades of dual-disciplinary leadership across commercial architecture and urban real estate development, Jimmy S. founded the firm to unite design excellence with rigorous financial execution. Serving as the primary point of contact on every commission, Jimmy guides institutional investors, private developers, and civic stakeholders from initial land underwriting through final occupancy.
                        </p>

                        <div class="pt-2 flex flex-wrap gap-4">
                            <button onclick="scrollToContact()" class="px-7 py-3.5 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronze transition-colors rounded-sm">
                                Schedule a Consultation with Jimmy S.
                            </button>
                            <button onclick="navigateTo('main')" class="px-7 py-3.5 border border-obsidian text-obsidian text-xs uppercase tracking-[0.18em] font-medium hover:bg-stonewarm transition-colors rounded-sm">
                                View Selected Works
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Biography & Architectural Philosophy (Two-Column Editorial Layout) -->
        <section class="border-b border-obsidian/10 bg-stonewarm/35 py-16 lg:py-24">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
                <div class="mb-12">
                    <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Background &amp; Methodology</span>
                    <h2 class="text-3xl font-light tracking-tight text-obsidian">Bridging Spatial Vision &amp; Development Feasibility</h2>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-12 lg:gap-16 text-sm sm:text-base text-slate leading-relaxed font-light">
                    <div class="space-y-6">
                        <h3 class="text-lg font-medium text-obsidian">Dual-Discipline Pedigree</h3>
                        <p>
                            Early in his career, Jimmy S. recognized a persistent divide in the built environment: visionary architectural studios frequently overlooked construction economics and zoning friction, while purely financial developers often sacrificed spatial quality for short-term margins.
                        </p>
                        <p>
                            To resolve this disconnect, Jimmy pursued advanced training in both architectural design and real estate finance. Prior to establishing his namesake practice, he directed major mixed-use urban infill developments across Chicago, New York, and Austin, overseeing more than 3.2 million square feet of Class-A commercial and high-density residential assets.
                        </p>
                    </div>

                    <div class="space-y-6">
                        <h3 class="text-lg font-medium text-obsidian">Tectonic Restraint &amp; Long-Term Asset Value</h3>
                        <p>
                            Under Jimmy S.’s direction, the studio favors honest, high-durability palettes—board-formed architectural concrete, anodized bronze, thermally broken curtain walls, and limestone—that age with dignity and reduce lifecycle maintenance costs for asset owners.
                        </p>
                        <p>
                            Every project is approached through an analytical lens: optimizing floor-plate efficiency, passive solar orientation, and municipal entitlement pathways before a single cubic yard of concrete is poured. Clients work directly with Jimmy at every milestone, ensuring transparent governance and decisive leadership.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Career Milestones & Credentials -->
        <section class="border-b border-obsidian/10 py-16 lg:py-24">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                    <!-- Left: Education & Licensure -->
                    <div class="lg:col-span-5 space-y-8">
                        <div>
                            <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Credentials</span>
                            <h2 class="text-2xl sm:text-3xl font-light tracking-tight text-obsidian">Education &amp; Licensure</h2>
                        </div>

                        <div class="space-y-6 border-t border-obsidian/10 pt-6">
                            <div>
                                <p class="text-xs uppercase tracking-[0.15em] text-bronze font-semibold">Academic Foundation</p>
                                <p class="text-base font-medium text-obsidian mt-1">Master of Architecture (M.Arch)</p>
                                <p class="text-sm text-slate">Harvard University Graduate School of Design</p>
                            </div>
                            <div>
                                <p class="text-base font-medium text-obsidian">M.S. in Real Estate Development</p>
                                <p class="text-sm text-slate">Massachusetts Institute of Technology (MIT)</p>
                            </div>
                            <div class="pt-4 border-t border-obsidian/10">
                                <p class="text-xs uppercase tracking-[0.15em] text-bronze font-semibold">Registrations &amp; Affiliations</p>
                                <ul class="mt-2 space-y-2 text-sm text-slate">
                                    <li>• Licensed Architect — Illinois, New York, Texas, California</li>
                                    <li>• NCARB Certified Principal</li>
                                    <li>• American Institute of Architects (AIA) Member</li>
                                    <li>• Urban Land Institute (ULI) — Urban Development Council</li>
                                    <li>• LEED Accredited Professional (LEED AP BD+C)</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!-- Right: Career Timeline -->
                    <div class="lg:col-span-7 space-y-8">
                        <div>
                            <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Track Record</span>
                            <h2 class="text-2xl sm:text-3xl font-light tracking-tight text-obsidian">Selected Career Milestones</h2>
                        </div>

                        <div class="border-t border-obsidian/10 divide-y divide-obsidian/10">
                            <div class="py-6 grid grid-cols-1 sm:grid-cols-4 gap-4">
                                <span class="text-xs font-mono uppercase tracking-widest text-bronze">2018 — Present</span>
                                <div class="sm:col-span-3">
                                    <h3 class="text-base font-medium text-obsidian">Founder &amp; Principal — Jimmy S. Architecture &amp; Development</h3>
                                    <p class="text-sm text-slate mt-1 font-light">Established integrated design-development firm delivering institutional headquarters, boutique hospitality, and urban master plans nationwide.</p>
                                </div>
                            </div>

                            <div class="py-6 grid grid-cols-1 sm:grid-cols-4 gap-4">
                                <span class="text-xs font-mono uppercase tracking-widest text-bronze">2023</span>
                                <div class="sm:col-span-3">
                                    <h3 class="text-base font-medium text-obsidian">AIA National Honor Award for Commercial Architecture</h3>
                                    <p class="text-sm text-slate mt-1 font-light">Recognized for the adaptive reuse and structural expansion of the Fulton Market Timber &amp; Glass Exchange.</p>
                                </div>
                            </div>

                            <div class="py-6 grid grid-cols-1 sm:grid-cols-4 gap-4">
                                <span class="text-xs font-mono uppercase tracking-widest text-bronze">2013 — 2018</span>
                                <div class="sm:col-span-3">
                                    <h3 class="text-base font-medium text-obsidian">Vice President of Design &amp; Development — Meridian Urban Group</h3>
                                    <p class="text-sm text-slate mt-1 font-light">Led architectural oversight and $650M in ground-up mixed-use acquisitions across major North American metropolitan corridors.</p>
                                </div>
                            </div>

                            <div class="py-6 grid grid-cols-1 sm:grid-cols-4 gap-4">
                                <span class="text-xs font-mono uppercase tracking-widest text-bronze">2008 — 2013</span>
                                <div class="sm:col-span-3">
                                    <h3 class="text-base font-medium text-obsidian">Senior Project Architect — Atelier Nord &amp; Partners</h3>
                                    <p class="text-sm text-slate mt-1 font-light">Directed facade engineering and civic cultural commissions in Zurich and New York.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Three Core Leadership Principles + Direct CTA -->
        <section class="bg-stonewarm/50 py-16 lg:py-24">
            <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
                <div class="text-center max-w-2xl mx-auto mb-14">
                    <span class="text-xs uppercase tracking-[0.22em] text-bronze font-semibold block mb-2">Practice Charter</span>
                    <h2 class="text-3xl font-light tracking-tight text-obsidian">Three Pillars of Jimmy S.’s Practice</h2>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
                    <div class="bg-alabaster border border-obsidian/10 p-8 rounded-sm">
                        <span class="text-xs font-mono text-bronze block mb-4">PILLAR I</span>
                        <h3 class="text-lg font-medium text-obsidian mb-3">Direct Principal Accountability</h3>
                        <p class="text-sm text-slate leading-relaxed font-light">
                            Clients never get handed off to junior tiers. Jimmy S. personally leads design charrettes, municipal presentations, and capital reviews from inception to completion.
                        </p>
                    </div>

                    <div class="bg-alabaster border border-obsidian/10 p-8 rounded-sm">
                        <span class="text-xs font-mono text-bronze block mb-4">PILLAR II</span>
                        <h3 class="text-lg font-medium text-obsidian mb-3">Capital &amp; Schedule Discipline</h3>
                        <p class="text-sm text-slate leading-relaxed font-light">
                            Architectural ambition is calibrated against real-time construction cost modeling and constructability reviews, protecting pro-forma returns without diluting design integrity.
                        </p>
                    </div>

                    <div class="bg-alabaster border border-obsidian/10 p-8 rounded-sm">
                        <span class="text-xs font-mono text-bronze block mb-4">PILLAR III</span>
                        <h3 class="text-lg font-medium text-obsidian mb-3">Enduring Civic Contribution</h3>
                        <p class="text-sm text-slate leading-relaxed font-light">
                            Every building shapes the public realm. We prioritize pedestrian-scale streetscapes, carbon-conscious structural systems, and timeless proportions.
                        </p>
                    </div>
                </div>

                <!-- Direct Executive CTA Banner -->
                <div class="bg-obsidian text-alabaster p-8 sm:p-12 rounded-sm flex flex-col lg:flex-row items-start lg:items-center justify-between gap-8">
                    <div class="space-y-2 max-w-2xl">
                        <span class="text-xs uppercase tracking-[0.2em] text-bronze font-semibold block">Direct Principal Access</span>
                        <h3 class="text-2xl sm:text-3xl font-light">Ready to discuss an architectural commission or development site?</h3>
                        <p class="text-sm text-alabaster/75 font-light">
                            Connect directly with Jimmy S. at <span class="text-white font-medium">jimmy@jimmysarchitecture.com</span> or initiate a confidential project brief.
                        </p>
                    </div>
                    <button onclick="scrollToContact()" class="px-8 py-4 bg-bronze text-white text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronzedark transition-colors whitespace-nowrap rounded-sm">
                        Schedule a Consultation
                    </button>
                </div>
            </div>
        </section>
    </main>

    <!-- ===================================================================== -->
    <!-- PROJECT INSPECTION LIGHTBOX MODAL                                     -->
    <!-- ===================================================================== -->
    <div id="project-modal" class="hidden fixed inset-0 z-50 bg-obsidian/80 backdrop-blur-sm flex items-center justify-center p-4 sm:p-6 overflow-y-auto" role="dialog" aria-modal="true" aria-labelledby="modal-title">
        <div class="bg-alabaster border border-obsidian/20 max-w-4xl w-full rounded-sm overflow-hidden shadow-2xl my-auto">
            <div class="flex items-center justify-between px-6 py-4 border-b border-obsidian/10 bg-stonewarm/50">
                <span id="modal-category" class="text-xs uppercase tracking-[0.2em] text-bronze font-semibold">Commercial</span>
                <button onclick="closeModal()" aria-label="Close modal" class="p-1.5 text-obsidian hover:text-bronze transition-colors text-xs uppercase tracking-widest font-medium flex items-center gap-1.5">
                    <span>Close</span>
                    <span class="text-lg leading-none">&times;</span>
                </button>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12">
                <div class="lg:col-span-7 bg-stonewarm">
                    <img id="modal-img" src="" alt="Project view" class="w-full h-72 sm:h-[420px] object-cover">
                </div>
                <div class="lg:col-span-5 p-6 sm:p-8 flex flex-col justify-between space-y-6">
                    <div>
                        <h3 id="modal-title" class="text-2xl font-light text-obsidian leading-snug">Project Title</h3>
                        <p id="modal-location" class="text-xs uppercase tracking-[0.16em] text-slate mt-1">Location</p>

                        <div class="grid grid-cols-2 gap-4 py-4 my-4 border-y border-obsidian/10 text-xs">
                            <div>
                                <span class="text-slate uppercase tracking-wider block">Area</span>
                                <span id="modal-area" class="font-medium text-obsidian text-sm mt-0.5 block">120,000 SQ FT</span>
                            </div>
                            <div>
                                <span class="text-slate uppercase tracking-wider block">Completion</span>
                                <span id="modal-year" class="font-medium text-obsidian text-sm mt-0.5 block">2024</span>
                            </div>
                        </div>

                        <p id="modal-desc" class="text-sm text-slate leading-relaxed font-light">
                            Architectural design and development notes.
                        </p>
                    </div>

                    <div class="pt-4 border-t border-obsidian/10 flex flex-col gap-3">
                        <div class="text-xs text-slate">
                            Principal in Charge: <strong class="text-obsidian font-medium">Jimmy S.</strong>
                        </div>
                        <button onclick="closeModal(); scrollToContact();" class="w-full py-3 bg-obsidian text-alabaster text-xs uppercase tracking-[0.18em] font-medium hover:bg-bronze transition-colors rounded-sm">
                            Inquire About Similar Scope
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- ===================================================================== -->
    <!-- CORPORATE MINIMALIST FOOTER (SHARED ACROSS BOTH PAGES)                -->
    <!-- ===================================================================== -->
    <footer class="bg-obsidian text-alabaster border-t border-obsidian/10">
        <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12 py-14">
            <div class="grid grid-cols-1 md:grid-cols-12 gap-10 pb-12 border-b border-alabaster/15">
                <div class="md:col-span-5 space-y-4">
                    <div class="flex items-center gap-3">
                        <div class="w-7 h-7 border border-alabaster/60 flex items-center justify-center">
                            <span class="font-serif text-sm font-semibold">JS</span>
                        </div>
                        <span class="text-xs font-semibold tracking-[0.22em] uppercase">JIMMY S. ARCHITECTURE &amp; DEVELOPMENT</span>
                    </div>
                    <p class="text-xs text-alabaster/70 leading-relaxed max-w-sm font-light">
                        Disciplined spatial architecture, commercial real estate development, and urban master planning led by Principal Jimmy S.
                    </p>
                </div>

                <div class="md:col-span-3 space-y-3">
                    <p class="text-[11px] uppercase tracking-[0.2em] text-bronze font-semibold">Navigation</p>
                    <ul class="space-y-2 text-xs text-alabaster/80">
                        <li><button onclick="navigateTo('main')" class="hover:text-white transition-colors">01. Overview &amp; Projects</button></li>
                        <li><button onclick="navigateTo('about')" class="hover:text-white transition-colors">02. About Jimmy S.</button></li>
                        <li><button onclick="scrollToContact()" class="hover:text-white transition-colors">03. Direct Inquiry</button></li>
                    </ul>
                </div>

                <div class="md:col-span-4 space-y-3">
                    <p class="text-[11px] uppercase tracking-[0.2em] text-bronze font-semibold">Main Contact</p>
                    <p class="text-xs text-alabaster font-medium">Jimmy S. — Principal Architect &amp; Developer</p>
                    <p class="text-xs text-alabaster/75">jimmy@jimmysarchitecture.com • +1 (312) 555-0194</p>
                    <p class="text-xs text-alabaster/60">440 N. Wells Street, Suite 700, Chicago, IL</p>
                </div>
            </div>

            <div class="pt-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-[11px] text-alabaster/50 tracking-wider uppercase">
                <p>&copy; 2026 JIMMY S. ARCHITECTURE &amp; DEVELOPMENT LLC. ALL RIGHTS RESERVED.</p>
                <p>CHICAGO • NEW YORK • AUSTIN</p>
            </div>
        </div>
    </footer>

    <!-- Toast Notification for Clipboard / Feedback -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 hidden bg-obsidian text-alabaster border border-bronze px-5 py-3 text-xs uppercase tracking-[0.16em] shadow-lg rounded-sm">
        Email Copied to Clipboard
    </div>

    <script>
        // Curated Architectural Projects Dataset (High-Resolution Architectural Photography)
        const architecturalProjects = [
            {
                id: 1,
                title: "The Sterling Financial Pavilion",
                category: "Commercial",
                location: "Chicago, IL",
                area: "340,000 SQ FT",
                year: "2025",
                image: "https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=1200&q=80",
                description: "A 28-story Class-A commercial headquarters featuring a triple-glazed unitized curtain wall, exposed structural steel diagrid bracing, and a double-height travertine public colonnade."
            },
            {
                id: 2,
                title: "Monolith Ridge Residence",
                category: "Residential",
                location: "Aspen, CO",
                area: "11,400 SQ FT",
                year: "2024",
                image: "https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=1200&q=80",
                description: "Cantilevered board-formed concrete and thermally modified cedar volumes anchored into an alpine granite slope, balancing dramatic mountain framing with passive solar efficiency."
            },
            {
                id: 3,
                title: "West Loop Riverfront Masterplan",
                category: "Urban Development",
                location: "Chicago, IL",
                area: "1.2M SQ FT",
                year: "2025",
                image: "https://images.unsplash.com/photo-1449844908441-8829872d2607?auto=format&fit=crop&w=1200&q=80",
                description: "Multi-phase transit-oriented urban infill development spearheaded by Jimmy S., integrating commercial office towers, 420 residential units, and a landscaped riverwalk esplanade."
            },
            {
                id: 4,
                title: "Vanguard Biotech & Research Hub",
                category: "Commercial",
                location: "Cambridge, MA",
                area: "215,000 SQ FT",
                year: "2024",
                image: "https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=1200&q=80",
                description: "Purpose-built life sciences and executive laboratory facility designed around modular structural bays, daylight-flooded atriums, and LEED Platinum energy recovery."
            },
            {
                id: 5,
                title: "Courtyard Limestone Villa",
                category: "Residential",
                location: "Austin, TX",
                area: "8,900 SQ FT",
                year: "2023",
                image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1200&q=80",
                description: "Minimalist private residence organized around a shaded limestone reflection court, utilizing deep bronze overhangs to mitigate solar heat gain while blurring indoor-outdoor living."
            },
            {
                id: 6,
                title: "Hudson Yards Cultural & Civic Plaza",
                category: "Urban Development",
                location: "New York, NY",
                area: "580,000 SQ FT",
                year: "2023",
                image: "https://images.unsplash.com/photo-1479839672679-a46483c0e7c8?auto=format&fit=crop&w=1200&q=80",
                description: "Adaptive redevelopment of an industrial rail corridor into a mixed-use commercial gallery, executive workspace, and public civic forum."
            }
        ];

        let currentPage = 'main';
        let activeFilter = 'All';

        // Initialize Gallery on Load
        document.addEventListener('DOMContentLoaded', () => {
            renderGallery('All');
        });

        // Two-Page Navigation Controller
        function navigateTo(page) {
            currentPage = page;
            const mainPage = document.getElementById('page-main');
            const aboutPage = document.getElementById('page-about');
            const navMain = document.getElementById('nav-main');
            const navAbout = document.getElementById('nav-about');
            const mobNavMain = document.getElementById('mobile-nav-main');
            const mobNavAbout = document.getElementById('mobile-nav-about');

            if (page === 'main') {
                mainPage.classList.remove('hidden');
                aboutPage.classList.add('hidden');

                // Update Desktop Nav Active State
                navMain.classList.add('border-obsidian', 'text-obsidian');
                navMain.classList.remove('border-transparent', 'text-slate');
                navAbout.classList.add('border-transparent', 'text-slate');
                navAbout.classList.remove('border-obsidian', 'text-obsidian');

                // Update Mobile Nav Active State
                mobNavMain.classList.add('font-semibold', 'text-obsidian');
                mobNavMain.classList.remove('font-medium', 'text-slate');
                mobNavAbout.classList.add('font-medium', 'text-slate');
                mobNavAbout.classList.remove('font-semibold', 'text-obsidian');
            } else {
                mainPage.classList.add('hidden');
                aboutPage.classList.remove('hidden');

                // Update Desktop Nav Active State
                navAbout.classList.add('border-obsidian', 'text-obsidian');
                navAbout.classList.remove('border-transparent', 'text-slate');
                navMain.classList.add('border-transparent', 'text-slate');
                navMain.classList.remove('border-obsidian', 'text-obsidian');

                // Update Mobile Nav Active State
                mobNavAbout.classList.add('font-semibold', 'text-obsidian');
                mobNavAbout.classList.remove('font-medium', 'text-slate');
                mobNavMain.classList.add('font-medium', 'text-slate');
                mobNavMain.classList.remove('font-semibold', 'text-obsidian');
            }

            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Scroll smoothly to Direct Contact section on Main Page
        function scrollToContact() {
            if (currentPage !== 'main') {
                navigateTo('main');
                setTimeout(() => {
                    const contactEl = document.getElementById('contact-section');
                    if (contactEl) contactEl.scrollIntoView({ behavior: 'smooth' });
                }, 120);
            } else {
                const contactEl = document.getElementById('contact-section');
                if (contactEl) contactEl.scrollIntoView({ behavior: 'smooth' });
            }
        }

        // Mobile Navigation Drawer Toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // Filter & Render Architectural Gallery
        function filterProjects(category) {
            activeFilter = category;
            
            // Update Filter Button Styles
            document.querySelectorAll('.filter-btn').forEach(btn => {
                if (btn.getAttribute('data-filter') === category) {
                    btn.classList.remove('bg-transparent', 'text-slate', 'border-obsidian/20');
                    btn.classList.add('bg-obsidian', 'text-alabaster', 'border-obsidian');
                } else {
                    btn.classList.add('bg-transparent', 'text-slate', 'border-obsidian/20');
                    btn.classList.remove('bg-obsidian', 'text-alabaster', 'border-obsidian');
                }
            });

            renderGallery(category);
        }

        function renderGallery(category) {
            const grid = document.getElementById('gallery-grid');
            const filtered = category === 'All' 
                ? architecturalProjects 
                : architecturalProjects.filter(p => p.category === category);

            grid.innerHTML = filtered.map(project => `
                <article onclick="openModal(${project.id})" class="group cursor-pointer bg-alabaster border border-obsidian/10 hover:border-obsidian/40 transition-all rounded-sm overflow-hidden flex flex-col">
                    <div class="relative h-64 sm:h-72 bg-stonewarm overflow-hidden">
                        <img 
                            src="${project.image}" 
                            alt="${project.title}" 
                            onerror="this.src='https://placehold.co/800x600/E8E6E1/1A1A1A?text=${encodeURIComponent(project.title)}'"
                            class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
                        >
                        <div class="absolute top-3 left-3 bg-alabaster/95 backdrop-blur-sm px-3 py-1 border border-obsidian/10 rounded-sm">
                            <span class="text-[10px] uppercase tracking-[0.18em] text-obsidian font-medium">${project.category}</span>
                        </div>
                    </div>
                    <div class="p-6 flex-grow flex flex-col justify-between">
                        <div>
                            <div class="flex items-center justify-between text-[11px] uppercase tracking-[0.15em] text-slate mb-2">
                                <span>${project.location}</span>
                                <span>${project.year}</span>
                            </div>
                            <h3 class="text-lg font-medium text-obsidian group-hover:text-bronze transition-colors">${project.title}</h3>
                        </div>
                        <div class="mt-6 pt-4 border-t border-obsidian/10 flex items-center justify-between text-xs">
                            <span class="text-slate font-mono">${project.area}</span>
                            <span class="uppercase tracking-[0.16em] text-obsidian font-medium group-hover:translate-x-1 transition-transform">Inspect &rarr;</span>
                        </div>
                    </div>
                </article>
            `).join('');
        }

        // Lightbox Modal Controls
        function openModal(projectId) {
            const project = architecturalProjects.find(p => p.id === projectId);
            if (!project) return;

            document.getElementById('modal-category').textContent = project.category;
            document.getElementById('modal-title').textContent = project.title;
            document.getElementById('modal-location').textContent = project.location;
            document.getElementById('modal-area').textContent = project.area;
            document.getElementById('modal-year').textContent = project.year;
            document.getElementById('modal-desc').textContent = project.description;
            
            const imgEl = document.getElementById('modal-img');
            imgEl.src = project.image;
            imgEl.alt = project.title;

            document.getElementById('project-modal').classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            document.getElementById('project-modal').classList.add('hidden');
            document.body.style.overflow = '';
        }

        // Close modal on Escape key or backdrop click
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') closeModal();
        });
        document.getElementById('project-modal').addEventListener('click', (e) => {
            if (e.target.id === 'project-modal') closeModal();
        });

        // Copy Jimmy S.'s Email using reliable execCommand fallback
        function copyEmail() {
            const emailText = document.getElementById('jimmy-email').textContent;
            const tempInput = document.createElement('input');
            tempInput.value = emailText;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);

            const toast = document.getElementById('toast');
            toast.classList.remove('hidden');
            setTimeout(() => {
                toast.classList.add('hidden');
            }, 2600);
        }

        // Handle Direct Project Inquiry Form Submission
        function handleInquirySubmit(event) {
            event.preventDefault();
            const form = document.getElementById('inquiry-form');
            const confirmation = document.getElementById('inquiry-confirmation');
            
            confirmation.classList.remove('hidden');
            form.reset();
        }
    </script>
</body>
</html>

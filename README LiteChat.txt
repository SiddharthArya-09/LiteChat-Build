<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LiteChat Privacy Policy</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals -->
    <!-- Application Structure Plan: The SPA transforms the dense privacy policy into an interactive, user-friendly experience. Instead of a linear document, it uses a thematic, single-page dashboard structure with a sticky top navigation for easy access to key areas. The core design uses interactive 'cards' and 'accordions' for major topics like 'What We Collect' and 'Your Rights'. This layered approach allows users to see a high-level overview first and then drill down into details by clicking on elements. This structure was chosen to reduce cognitive load, improve scannability, and empower users to find information quickly without being overwhelmed by legal text. -->
    <!-- Visualization & Content Choices: 1. Information Collected: Goal: Inform. Method: Interactive grid of cards (HTML/CSS) with icons. Interaction: Click to expand and show details. Justification: Breaks down data types into digestible chunks. 2. How Information is Used: Goal: Inform. Method: Similar interactive grid. Interaction: Click to expand. Justification: Creates consistent UI and clarifies the purpose of data collection. 3. Information Sharing: Goal: Inform. Method: Styled HTML list. Interaction: N/A. Justification: Simple and clear for the listed points. 4. Your Rights: Goal: Empower. Method: Accordion list (HTML/JS). Interaction: Click to expand each right. Justification: Makes rights feel actionable and easy to navigate. All text is from the source report, populated via JS. No complex data exists, so Chart.js is not used for visualization, which is a deliberate design choice to maintain clarity. Library/Method: Vanilla JS for interactions, Tailwind CSS for styling. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s cubic-bezier(0, 1, 0, 1);
        }
        .accordion-content.open {
            max-height: 1000px; 
            transition: max-height 1s ease-in-out;
        }
        .nav-link.active {
            color: #f59e0b; /* amber-500 */
            border-bottom-color: #f59e0b;
        }
        .chart-container { 
            position: relative; 
            width: 100%; 
            max-width: 600px; 
            margin-left: auto; 
            margin-right: auto; 
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) { .chart-container { height: 350px; } }
    </style>
</head>
<body class="bg-stone-50 text-stone-800">

    <header class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 border-b border-stone-200">
        <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-shrink-0">
                    <h1 class="text-2xl font-bold text-stone-900">LiteChat Privacy</h1>
                </div>
                <div class="hidden md:block">
                    <div id="nav-menu" class="ml-10 flex items-baseline space-x-4">
                        <a href="#introduction" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">Overview</a>
                        <a href="#collection" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">What We Collect</a>
                        <a href="#usage" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">How We Use It</a>
                        <a href="#sharing" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">Sharing</a>
                        <a href="#rights" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">Your Rights</a>
                        <a href="#security" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-stone-600 hover:text-amber-500 border-b-2 border-transparent">Security</a>
                    </div>
                </div>
                 <div class="md:hidden">
                    <select id="mobile-nav-menu" class="bg-stone-100 border border-stone-300 text-stone-900 text-sm rounded-lg focus:ring-amber-500 focus:border-amber-500 block w-full p-2.5">
                        <option value="#introduction">Overview</option>
                        <option value="#collection">What We Collect</option>
                        <option value="#usage">How We Use It</option>
                        <option value="#sharing">Sharing</option>
                        <option value="#rights">Your Rights</option>
                        <option value="#security">Security</option>
                    </select>
                </div>
            </div>
        </nav>
    </header>

    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-8 md:py-12">
        
        <section id="introduction" class="text-center py-12">
            <h2 class="text-3xl font-bold tracking-tight text-stone-900 sm:text-4xl">Your Privacy, Clarified.</h2>
            <p class="mt-4 max-w-2xl mx-auto text-lg text-stone-600">This policy explains how LiteChat Build collects, uses, and protects your information when you use our app, LiteChat. We believe in transparency and want you to feel secure. This interactive guide is here to help you understand our practices at a glance.</p>
            <p class="mt-2 text-xs text-stone-500">Last Updated: June 20, 2025</p>
        </section>

        <section id="collection" class="py-12 scroll-mt-20">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-stone-900">What Information We Collect</h2>
                <p class="mt-3 max-w-2xl mx-auto text-md text-stone-600">To make LiteChat work, we need to collect some information. We group this into two categories: information you give us directly, and information we collect automatically as you use the app. Click on each card to learn more.</p>
            </div>
            <div id="collection-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            </div>
        </section>
        
        <section id="usage" class="py-12 scroll-mt-20">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-stone-900">How We Use Your Information</h2>
                <p class="mt-3 max-w-2xl mx-auto text-md text-stone-600">We use the information we collect for specific purposes, all aimed at providing and improving your experience. Explore how your data helps power LiteChat's features and security.</p>
            </div>
            <div id="usage-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            </div>
        </section>

        <section id="sharing" class="py-12 scroll-mt-20">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-stone-900">How We Share Your Information</h2>
                <p class="mt-3 max-w-2xl mx-auto text-md text-stone-600">We don't sell your data. We only share it in specific situations to provide our service, comply with the law, or with your consent. Here’s a breakdown of when and why your information might be shared.</p>
            </div>
            <div id="sharing-list" class="max-w-3xl mx-auto space-y-4">
            </div>
        </section>

        <section id="rights" class="py-12 scroll-mt-20">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-stone-900">Your Choices and Rights</h2>
                <p class="mt-3 max-w-2xl mx-auto text-md text-stone-600">You are in control of your personal information. This section outlines the rights you have and the choices you can make regarding your data in LiteChat.</p>
            </div>
            <div id="rights-accordion" class="max-w-3xl mx-auto space-y-3">
            </div>
        </section>
        
        <section id="security" class="py-12 scroll-mt-20">
            <div class="text-center mb-10">
                 <h2 class="text-3xl font-bold text-stone-900">Security & Other Key Policies</h2>
                <p class="mt-3 max-w-2xl mx-auto text-md text-stone-600">We take your privacy and security seriously. Learn about our approach to data protection, retention, and other important policies.</p>
            </div>
            <div id="security-list" class="max-w-3xl mx-auto space-y-6">
            </div>
        </section>
        
    </main>

    <footer class="bg-stone-100 border-t border-stone-200">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-8 text-center">
            <h3 class="text-xl font-bold text-stone-900">Contact Us</h3>
            <p class="mt-2 text-stone-600">If you have any questions or concerns about this Privacy Policy or our data practices, please reach out.</p>
            <a href="mailto:anantgautam267@gmail.com" class="mt-4 inline-block bg-amber-400 text-amber-900 font-bold py-2 px-4 rounded-lg hover:bg-amber-500 transition-colors">anantgautam267@gmail.com</a>
        </div>
    </footer>

    <script>
        const privacyData = {
            collection: [
                {
                    type: 'Directly Provided',
                    title: 'Account Information',
                    icon: '👤',
                    content: 'When you create an account, we collect your username, email address and password.'
                },
                {
                    type: 'Directly Provided',
                    title: 'Messages',
                    icon: '💬',
                    content: 'We collect the content of your messages, including text, images, videos, and other files you send or receive. Messages are generally end-to-end encrypted, meaning we cannot access the content. However, data related to message delivery (e.g., sender, recipient, timestamp) may be collected.'
                },
                {
                    type: 'Directly Provided',
                    title: 'User Content',
                    icon: '📝',
                    content: 'Any other content you create, share, or upload to the App, such as status updates or shared media.'
                },
                {
                    type: 'Directly Provided',
                    title: 'Feedback/Support',
                    icon: '❤️',
                    content: 'If you contact us for support or provide feedback, we collect the information you provide in those communications.'
                },
                {
                    type: 'Automatically Collected',
                    title: 'Usage Information',
                    icon: '📊',
                    content: 'We collect information about how you use the App, such as the features you use, the time, frequency, and duration of your activities, and interactions with other users.'
                },
                {
                    type: 'Automatically Collected',
                    title: 'Device & Log Data',
                    icon: '📱',
                    content: 'We collect information from your device, including IP address, device identifiers, operating system, browser type, mobile network information, crash data, and log data like pages visited and search terms.'
                }
            ],
            usage: [
                {
                    title: 'Provide & Maintain',
                    icon: '⚙️',
                    content: "To operate, maintain, and improve the App's features and functionality."
                },
                {
                    title: 'Communicate With You',
                    icon: '📣',
                    content: 'To send you updates, security alerts, and support messages, and to respond to your comments and questions.'
                },
                {
                    title: 'Personalize Experience',
                    icon: '✨',
                    content: 'To customize your experience within the App, such as showing you relevant content or features.'
                },
                {
                    title: 'Improve Services',
                    icon: '🚀',
                    content: 'To understand and analyze how you use the App and to develop new products, services, features, and functionality.'
                },
                {
                    title: 'Ensure Safety & Security',
                    icon: '🛡️',
                    content: 'To detect and prevent fraud, abuse, and other harmful activity, and to enforce our terms of service.'
                },
                {
                    title: 'Comply with Legal Obligations',
                    icon: '⚖️',
                    content: 'To comply with applicable laws, regulations, and legal processes.'
                }
            ],
            sharing: [
                {
                    title: 'With Other Users',
                    icon: '👥',
                    content: 'Information you share publicly or send to other users (e.g., profile information, messages) will be accessible to those users.'
                },
                {
                    title: 'Service Providers',
                    icon: '🤝',
                    content: 'We may share your information with third-party service providers who perform services on our behalf, such as hosting and data analysis. They are obligated to protect your information.'
                },
                {
                    title: 'For Legal Reasons',
                    icon: '📜',
                    content: 'We may disclose your information if required by law or to protect our rights, property, or the safety of users.'
                },
                {
                    title: 'Business Transfers',
                    icon: '🏢',
                    content: 'If LiteChat is involved in a merger, acquisition, or sale of assets, your information may be transferred as part of that transaction.'
                },
                {
                    title: 'With Your Consent',
                    icon: '✅',
                    content: 'We may share your information with third parties when we have your explicit consent to do so.'
                }
            ],
            rights: [
                {
                    title: 'Review and Update Account Information',
                    content: "You can review and update your account information at any time through the App's settings."
                },
                {
                    title: 'Delete Your Account',
                    content: 'You may delete your account at any time. Upon deletion, your personal information will be removed from our active databases, though some information may persist for a limited time for backup, archival, or legal purposes.'
                },
                {
                    title: 'Opt-Out of Marketing Communications',
                    content: 'You may opt-out of receiving promotional communications from us by following the instructions in those communications or by adjusting your notification settings in the App.'
                },
                {
                    title: 'Access, Correction, Deletion Rights',
                    content: 'Depending on your jurisdiction, you may have the right to request access to, correction of, or deletion of your personal data. To exercise these rights, please contact us.'
                }
            ],
            security: [
                 {
                    title: 'Our Security Measures',
                    icon: '🔐',
                    content: 'We take reasonable measures, including administrative, technical, and physical safeguards, to protect your information from loss, theft, misuse, and unauthorized access. However, no security system is impenetrable, and we cannot guarantee absolute security.'
                },
                {
                    title: 'Data Retention',
                    icon: '⏳',
                    content: 'We retain your information for as long as necessary to provide our services, comply with legal obligations, resolve disputes, and enforce our policies. The retention period can vary based on the type of data.'
                },
                {
                    title: "Children's Privacy",
                    icon: '🧒',
                    content: 'The App is not intended for use by children under the age of 16. We do not knowingly collect personal information from children under 16. If we become aware that we have, we will take steps to remove that information.'
                },
                {
                    title: 'Changes to This Policy',
                    icon: '🔄',
                    content: 'We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new policy on this page and updating the "Last Updated" date. You are advised to review this policy periodically.'
                },
            ]
        };

        document.addEventListener('DOMContentLoaded', () => {
            const collectionGrid = document.getElementById('collection-grid');
            const usageGrid = document.getElementById('usage-grid');
            const sharingList = document.getElementById('sharing-list');
            const rightsAccordion = document.getElementById('rights-accordion');
            const securityList = document.getElementById('security-list');

            const createCard = (item, type) => {
                const card = document.createElement('div');
                card.className = 'accordion-toggle bg-white rounded-lg shadow-sm hover:shadow-md transition-shadow cursor-pointer border border-stone-200';
                
                let categoryHTML = '';
                if (type === 'collection' && item.type) {
                     categoryHTML = `<div class="text-xs font-semibold ${item.type === 'Directly Provided' ? 'text-blue-600' : 'text-purple-600'}">${item.type}</div>`
                }
                
                card.innerHTML = `
                    <div class="p-5 flex items-start space-x-4">
                        <div class="text-3xl">${item.icon}</div>
                        <div class="flex-1">
                            ${categoryHTML}
                            <h3 class="font-bold text-stone-900 mt-1">${item.title}</h3>
                        </div>
                         <div class="flex-shrink-0 transform transition-transform duration-300">
                            <span class="text-xl text-stone-400">&#x25BC;</span>
                        </div>
                    </div>
                    <div class="accordion-content px-5">
                        <p class="text-stone-600 pb-5">${item.content}</p>
                    </div>
                `;
                return card;
            };
            
            const createSharingItem = (item) => {
                const div = document.createElement('div');
                div.className = 'bg-white rounded-lg p-5 flex items-start space-x-4 border border-stone-200';
                div.innerHTML = `
                    <div class="text-3xl">${item.icon}</div>
                    <div>
                        <h4 class="font-bold text-stone-900">${item.title}</h4>
                        <p class="text-stone-600 mt-1">${item.content}</p>
                    </div>
                `;
                return div;
            };

            const createAccordionItem = (item) => {
                 const div = document.createElement('div');
                 div.className = 'bg-white rounded-lg shadow-sm border border-stone-200 overflow-hidden';
                 div.innerHTML = `
                    <button class="accordion-toggle w-full text-left p-5 flex justify-between items-center hover:bg-stone-50 transition-colors">
                        <h4 class="font-bold text-stone-900">${item.title}</h4>
                        <span class="transform transition-transform duration-300 text-xl text-stone-400">&#x25BC;</span>
                    </button>
                    <div class="accordion-content px-5">
                        <p class="text-stone-600 pb-5">${item.content}</p>
                    </div>
                 `;
                 return div;
            };

            privacyData.collection.forEach(item => collectionGrid.appendChild(createCard(item, 'collection')));
            privacyData.usage.forEach(item => usageGrid.appendChild(createCard(item, 'usage')));
            privacyData.sharing.forEach(item => sharingList.appendChild(createSharingItem(item)));
            privacyData.rights.forEach(item => rightsAccordion.appendChild(createAccordionItem(item)));
            privacyData.security.forEach(item => securityList.appendChild(createSharingItem(item)));

            document.querySelectorAll('.accordion-toggle').forEach(button => {
                button.addEventListener('click', () => {
                    const content = button.tagName === 'BUTTON' ? button.nextElementSibling : button.querySelector('.accordion-content');
                    const arrow = button.querySelector('span');
                    
                    if (content.classList.contains('open')) {
                        content.classList.remove('open');
                        if (arrow) arrow.style.transform = 'rotate(0deg)';
                    } else {
                        content.classList.add('open');
                        if (arrow) arrow.style.transform = 'rotate(180deg)';
                    }
                });
            });

            const navLinks = document.querySelectorAll('.nav-link');
            const sections = document.querySelectorAll('main section');

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        navLinks.forEach(link => {
                            link.classList.remove('active');
                            if (link.getAttribute('href').substring(1) === entry.target.id) {
                                link.classList.add('active');
                            }
                        });
                    }
                });
            }, { rootMargin: '-50% 0px -50% 0px', threshold: 0 });

            sections.forEach(section => observer.observe(section));
            
            const mobileNav = document.getElementById('mobile-nav-menu');
            mobileNav.addEventListener('change', (e) => {
                window.location.href = e.target.value;
            });
        });
    </script>
</body>
</html>

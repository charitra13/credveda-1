# CredVeda - Financial Transparency Platform

CredVeda is a financial awareness tool for the Indian loan payment ecosystem with smart EMI Reminders, loan comparison, and connection with trusted financial advisors.

## Features

- **Credit Profile Analysis**: AI-powered analysis using SHAP technology to reveal hidden credit strengths
- **Smart Payment Reminders**: WhatsApp and SMS alerts to never miss payment deadlines
- **Loan Comparison**: Side-by-side comparison of loan offers with transparent cost breakdown
- **Financial Advisor Network**: Connect with 500+ verified DSAs and NBFCs
- **Financial Transparency**: Empowering users with information rather than selling loans

## Tech Stack

- **Framework**: Next.js 14 with App Router
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Deployment**: Vercel

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Project Structure

```
src/
├── app/
│   ├── page.tsx          # Main landing page
│   ├── layout.tsx        # Root layout
│   └── globals.css       # Global styles
├── components/
│   ├── Header.tsx        # Site header with navigation
│   ├── Hero.tsx          # Hero section
│   ├── Features.tsx      # Features showcase
│   ├── Footer.tsx        # Site footer
│   └── ui/
│       ├── button.tsx    # Button component
│       └── card.tsx      # Card component
└── lib/
    └── utils.ts          # Utility functions
```

## Version History

### v1.8.0 - Vercel Deployment Fix & Supabase Integration
- **Fixed**: Resolved Vercel deployment build error related to missing Supabase server configuration
- **Added**: Created `src/utils/supabase/server.ts` with proper Next.js 15 cookie handling
- **Added**: Created `src/utils/supabase/client.ts` for client-side Supabase integration
- **Added**: Created `src/utils/supabase/database.types.ts` with proper TypeScript definitions
- **Fixed**: Updated cookieStore handling to use `await cookies()` for Next.js 15 compatibility
- **Fixed**: Resolved TypeScript errors by replacing `any` types with `Record<string, unknown>`
- **Fixed**: Removed unused imports from Features.tsx and floating-chat.tsx components
- **Enhanced**: Build now passes all TypeScript and ESLint checks successfully
- **Improved**: Proper error handling in cookie operations for server components
- **Added**: Complete Supabase SSR integration ready for authentication and database operations

### v1.7.0 - Features Breakpoint Optimization for 1024-1279px Viewport Range
- **Fixed**: Resolved column height alignment issues in Features.tsx component for 1024-1279px viewport range
- **Changed**: Updated all responsive breakpoints from `lg:` (1024px) to `xl:` (1280px) for two-column grid layout
- **Enhanced**: Single-column layout now extends through 1024-1279px maintaining the optimal 1023px design
- **Improved**: Two-column layout now only activates at 1280px+ where there's sufficient horizontal space
- **Fixed**: Bottom two cards in left column no longer appear below right column's bottom edge
- **Updated**: Grid layout breakpoint: `lg:grid-cols-5` → `xl:grid-cols-5`
- **Updated**: Column spans: `lg:col-span-2/3` → `xl:col-span-2/3`
- **Updated**: All height classes: `lg:min-h-[]` and `lg:h-[]` → `xl:min-h-[]` and `xl:h-[]`
- **Updated**: Spacing and layout: `lg:gap-8`, `lg:mb-8`, `lg:aspect-square` → `xl:gap-8`, `xl:mb-8`, `xl:aspect-square`
- **Enhanced**: Responsive design now provides consistent visual hierarchy across all viewport ranges
- **Improved**: Layout alignment ensures perfect column height matching when two-column layout is active

### v1.6.0 - Features Component Complete Responsiveness Overhaul
- **Fixed**: Complete responsiveness issues in Features.tsx component for 360x780px and all viewport sizes
- **Removed**: All fixed heights (`h-[510px]`, `h-[278px]`, `lg:h-[850px]`) that caused content overflow
- **Added**: Mobile-first responsive design with proper breakpoints (`sm:`, `lg:`) throughout component
- **Enhanced**: Image placeholders now resize properly with responsive aspect ratios and min-heights
- **Fixed**: Card content no longer flows outside card boundaries with proper `flex-shrink-0` and content organization
- **Improved**: Cards now reorder correctly on mobile (stack vertically) and desktop (complex grid layout)
- **Added**: Responsive typography with text sizes that scale appropriately across devices (`text-sm sm:text-base`)
- **Enhanced**: Flexible card heights using `min-h-[]` instead of fixed heights preventing content overflow
- **Improved**: Payment reminders card layout switches from horizontal (desktop) to vertical (mobile) stacking
- **Added**: Proper responsive spacing with adaptive gaps (`gap-6 sm:gap-8`) and padding (`p-4 sm:p-6`)
- **Fixed**: Icon sizes now scale responsively (`h-6 w-6 sm:h-8 sm:w-8`) for better mobile display
- **Enhanced**: Image placeholder aspect ratios (`aspect-square sm:aspect-[4/3] lg:aspect-square`) for optimal display
- **Improved**: Bottom card content alignment using `mt-auto` for consistent CTA button positioning
- **Added**: Minimum heights for image placeholders (`min-h-[200px] sm:min-h-[250px]`) ensuring visibility
- **Enhanced**: Grid system now properly adapts from single column mobile to complex desktop layout
- **Fixed**: All responsiveness issues ensuring perfect display on 360px width viewports and all screen sizes

### v1.5.0 - Floating Chat Theme & Responsive Design Enhancement
- **Enhanced**: Complete theme alignment of floating chat component with website design system
- **Updated**: Replaced generic blue colors with custom CSS variables (`--primary`, `--foreground`, `--gray-dark`)
- **Added**: Gradient-primary styling for chat trigger button matching site's button patterns
- **Enhanced**: Responsive design implementation across all viewports (mobile, tablet, desktop)
- **Improved**: Mobile-first approach with full-screen modal on small screens (`inset-4`)
- **Added**: Tablet optimization with adaptive sizing (`sm:h-[70vh]`) and proper margins
- **Enhanced**: Desktop floating behavior with optimal positioning (`lg:w-96 lg:h-[600px]`)
- **Updated**: Button styling to use established component variants (`primary`, `ghost`)
- **Enhanced**: Typography consistency with Plus Jakarta Sans font family inheritance
- **Improved**: Message bubble styling with rounded corners (`rounded-2xl`) and enhanced shadows
- **Added**: FAQ section responsive behavior with adaptive max-height (`lg:max-h-40`)
- **Enhanced**: Input focus states with proper primary color theming
- **Improved**: Speech bubble arrow colors matching theme (`#0066ff` for user, `#f8f9fa` for bot)
- **Added**: Smooth hover transitions and scale effects matching site's interaction patterns
- **Enhanced**: Touch-friendly design with proper 44px+ touch targets across all devices
- **Improved**: Accessibility with proper contrast ratios and keyboard navigation support

### v1.4.12 - Financial Transparency Section Height Optimization
- **Fixed**: Set Financial Transparency section to exactly 600px height as requested
- **Removed**: Responsive padding (`py-16 lg:py-24`) replaced with fixed height (`h-[600px]`)
- **Added**: Flexbox centering (`flex items-center justify-center`) for perfect vertical content alignment
- **Enhanced**: Content now perfectly centered within the 600px container height
- **Improved**: Eliminates extra white space when scrolled to bottom, creating seamless experience up to navigation bar

### v1.4.11 - Hero Section Body Text Enhancement
- **Enhanced**: Updated hero section body text to emphasize AI-powered credit profile analysis
- **Improved**: Changed opening from "CredVeda is a financial awareness tool" to "Analyze your credit profile with our AI"
- **Enhanced**: More direct and action-oriented messaging that highlights key AI capabilities upfront
- **Improved**: Better flow connecting AI analysis with payment reminders, loan comparison, and advisor connections

### v1.4.10 - Compare Loan Card Bottom Edge Alignment Fix
- **Fixed**: Increased "Compare Loan Offers Side by Side Instantly" card height by 4px (538px → 542px)
- **Improved**: Perfect bottom edge alignment between right column Compare Loan card and left column bottom two cards
- **Enhanced**: Visual consistency ensuring both column sections end at exactly the same vertical position
- **Optimized**: Precise height adjustments to eliminate any visual misalignment between card columns

### v1.4.9 - Column Height Alignment Optimization
- **Enhanced**: "Compare Loan Offers Side by Side" card height increased by 30px (508px → 538px)
- **Enhanced**: Bottom two cards in left column height increased by 30px (278px → 308px)
- **Improved**: Both columns now maintain equal height (850px) ensuring perfect bottom edge alignment
- **Fixed**: Visual alignment issue where column 2 card didn't reach the same bottom edge as column 1 cards

### v1.4.8 - AI Powered Insights Tag Update
- **Changed**: Updated top card tag from "Smart Analysis" to "AI Powered Insights" for better brand positioning
- **Enhanced**: More impactful messaging that emphasizes AI capabilities and actionable insights
- **Improved**: Tag now better aligns with the SHAP technology and credit analysis content

### v1.4.7 - Bottom Cards Content and Icons Enhancement
- **Added**: Users icon (Lucide React) to "Connect with Financial Advisors who Actually Care" card
- **Added**: Navigation icon (Lucide React) to "Navigate your Financial Journey Effortlessly" card
- **Enhanced**: Updated "Financial Advisors" card heading to emphasize advisors who "Actually Care"
- **Enhanced**: Updated body text to highlight competitive rates from DSAs and NBFCs network
- **Enhanced**: Updated "Financial Journey" heading to emphasize "Effortlessly" navigation
- **Enhanced**: Updated body text to emphasize intuitive interface designed for real people, not finance experts
- **Improved**: Visual hierarchy with prominent icons above each card heading
- **Added**: Consistent icon styling with primary color and proper spacing

### v1.4.6 - Smart Comparison Card Content Enhancement
- **Added**: "Smart Comparison" tag above "Compare Loan Offers Side by Side Instantly" heading for better categorization
- **Enhanced**: Updated body text to emphasize personalized profile matching and transparent cost breakdowns
- **Improved**: More specific content highlighting lender comparison benefits and transparency features
- **Clarified**: Content now explains profile-specific matching and comprehensive cost analysis

### v1.4.5 - Peace of Mind Card Content Enhancement
- **Added**: "Peace of Mind" tag above "Never Miss Another Payment Deadline" heading for better categorization
- **Enhanced**: Updated body text to emphasize WhatsApp and SMS alert features for loan reminders
- **Improved**: More specific content highlighting credit score health benefits and alert mechanisms
- **Clarified**: Content now clearly explains the dual notification system (WhatsApp + SMS)

### v1.4.4 - Smart Analysis Card Content Enhancement
- **Added**: "Smart Analysis" tag above "Know Your True Credit Worth" heading for better categorization
- **Enhanced**: Updated body text to highlight SHAP technology and credit strength analysis benefits
- **Fixed**: Corrected spelling to "Analyse My Profile" (British English) for consistency
- **Improved**: More descriptive and engaging content that emphasizes AI capabilities and user benefits

### v1.4.3 - Features Section Extended Height Optimization
- **Enhanced**: "Compare Loan Offers Side by Side" card height increased by additional 70px (now 508px total)
- **Enhanced**: Bottom two cards in left column increased by additional 70px each (now 278px each)
- **Improved**: Both columns now maintain equal height (820px) ensuring perfect visual alignment
- **Optimized**: Extended card heights provide better content spacing and improved visual hierarchy

### v1.4.2 - Features Section Height Balance Optimization
- **Enhanced**: "Know Your True Credit Worth" card height increased by 50px for better visual proportion
- **Enhanced**: Bottom two cards in left column increased by 50px each for improved content spacing
- **Enhanced**: "Compare Loan Offers Side by Side" card height increased by 100px for better content hierarchy
- **Improved**: Both columns now maintain equal height (750px) ensuring perfect visual alignment
- **Fixed**: Column height balance to create seamless visual flow and hierarchy across the Features section

### v1.4.1 - About Us Tag Removal
- **Removed**: "About Us" tag from the financial transparency section for cleaner design
- **Simplified**: Section now starts directly with the main headline without redundant label
- **Enhanced**: Improved visual hierarchy and reduced visual clutter

### v1.4.0 - Auth Card Modal Implementation
- **Added**: New AuthCard component with modal overlay functionality
- **Added**: Framer Motion animations for smooth card entrance/exit
- **Added**: Backdrop blur and click-to-close functionality
- **Changed**: Replaced standalone auth page with centered modal card
- **Enhanced**: Navigation buttons now trigger auth modal instead of page navigation
- **Removed**: Standalone auth page implementation for cleaner codebase
- **Added**: Close button (X) in auth card for better UX
- **Improved**: Responsive design with proper mobile padding and max-width constraints

### v1.3.0 - Global Floating Chat Integration
- **Added**: FloatingChat component integrated into root layout for global availability
- **Enhanced**: Chat interface now accessible from every page across the application
- **Added**: Interactive FAQ system with expandable quick access panel
- **Added**: Notification popup system with auto-hide functionality
- **Added**: Smooth animations and transitions using Framer Motion
- **Added**: Speech bubble styling with proper arrow indicators
- **Added**: Auto-scroll functionality for new messages
- **Added**: Keyboard support (ESC to close, Enter to send)
- **Enhanced**: User experience with responsive design and accessibility features

### v1.2.3 - Hero Section Shadow Fix for Mobile
- **Fixed**: Blue gradient shadow effect appearing around hero image placeholder on mobile viewports below 500px
- **Made Responsive**: Decorative blur elements now scale appropriately: 128px on mobile, 192px on tablets, 288px on desktop
- **Enhanced**: Shadow depth effect (`shadow-2xl`) now consistently visible across all viewport sizes
- **Improved**: Mobile positioning of decorative elements prevents interference with main image shadow
- **Maintained**: Original elegant desktop shadow appearance preserved

### v1.2.2 - Navigation Always Opaque
- **Removed**: Transparent navigation background feature when page is not scrolled
- **Changed**: Navigation bar now consistently uses opaque white background (`bg-white/90`) at all times
- **Simplified**: Removed scroll state tracking logic and useEffect hook for cleaner code
- **Enhanced**: Consistent visual appearance with backdrop blur and border always visible

### v1.2.1 - Mobile Navigation Background Fix
- **Fixed**: Hamburger menu background transparency issue at 360x780px viewport
- **Added**: Solid white background (`bg-white`) to mobile menu dropdown ensuring opacity at all scroll states
- **Enhanced**: Visual separation with top border (`border-t border-gray-200`) and shadow (`shadow-lg`)
- **Improved**: Mobile menu spacing with increased padding (`py-6 px-2`) for better touch targets
- **Added**: Rounded bottom corners (`rounded-b-lg`) for enhanced visual aesthetics
- **Fixed**: Mobile menu no longer overlaps with hero section content at small viewports

### v1.2 - UI Pattern Grid & Light Mode Only
- **Added**: Subtle diagonal fade grid pattern background visible across the entire site, inspired by PatternCraft
- **Fixed**: Removed all component background gradients so the pattern is visible everywhere
- **Changed**: Removed dark mode media query; site now always uses light mode colors
- **Fixed**: Features bento grid row/column span and stat card layout to match wireframe

### v1.1 - Bento Grid Layout Restructure
- **Major**: Restructured Features.tsx component with unified bento grid layout
- **Added**: New bentoItems array replacing separate features and stats arrays
- **Added**: Dynamic card types (feature, feature-with-image, stat, placeholder) for flexible grid layouts
- **Added**: Proper TypeScript definitions for bento grid items
- **Enhanced**: Grid layout with responsive column spanning (md:col-span-1, md:col-span-2)
- **Improved**: Component maintainability with single grid rendering instead of multiple sections

### v1.0.3 - Production Deployment
- **Fixed**: Resolved TypeScript errors with Framer Motion ease property
- **Deployed**: Successfully deployed to Vercel production environment
- **Live URL**: https://credveda-1-heawu0lhs-charitrajainofficial-gmailcoms-projects.vercel.app

### v1.0.2 - ESLint Fixes
- **Fixed**: Resolved ESLint errors with unescaped entities (quotes and apostrophes)
- **Fixed**: Removed unused imports from Features and Footer components

### v1.0.1 - Dependency Fix
- **Fixed**: Updated lucide-react to latest version for React 19 compatibility
- **Fixed**: Resolved npm install dependency conflicts for Vercel deployment

### v1.0.0 - Initial Release
- **Added**: Complete landing page with Hero, Features, and About Us sections
- **Added**: Responsive navigation with smooth scrolling
- **Added**: About Us section with financial transparency messaging
- **Added**: Features section showcasing key platform capabilities
- **Added**: Footer with social links and company information
- **Fixed**: Removed duplicate About Us sections
- **Fixed**: Updated About Us tag styling to match Features tag
- **Fixed**: Removed Contact Us navigation link (no corresponding section)

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

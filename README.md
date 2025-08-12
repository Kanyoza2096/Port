# KanyozaTech - Modern Developer Portfolio

A cutting-edge, high-performance developer portfolio built with Next.js 14, featuring advanced animations, real-time analytics, interactive components, and enterprise-grade CI/CD pipeline.

## 🚀 Features

### Core Features
- **Dynamic Hero Section** with animated particles and code snippets
- **Interactive Skills Matrix** with animated progress indicators
- **Project Showcase** with filtering, live demos, and GitHub integration
- **Blog System** with MDX support for technical articles
- **Contact Form** with email integration and auto-responses
- **Dark/Light Mode** with smooth transitions

### Advanced Features
- **Real-time Terminal** with animated command execution
- **Interactive Code Showcase** with syntax highlighting
- **Performance Metrics Dashboard** with live Core Web Vitals
- **Technology Radar** visualization
- **Analytics Dashboard** with charts and real-time data
- **Micro-interactions** using Framer Motion
- **Advanced Security** headers and rate limiting
- **Responsive Design** optimized for all devices
- **SEO Optimized** with OpenGraph and meta tags
- **Performance Focused** with lazy loading and optimizations
- **Enterprise CI/CD** with automated testing and deployment

## 🛠️ Tech Stack

- **Framework**: Next.js 14 with TypeScript
- **Styling**: TailwindCSS with custom design system
- **Animations**: Framer Motion
- **Charts**: Recharts
- **Email**: Nodemailer for contact form
- **UI Components**: Shadcn/ui with Radix UI
- **Icons**: Lucide React
- **Testing**: Jest + React Testing Library
- **Security**: Snyk + CodeQL
- **Performance**: Lighthouse CI
- **Deployment**: Vercel (recommended)

## 🔧 Development & Testing

### Scripts
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript checks
npm run test         # Run tests
npm run test:watch   # Run tests in watch mode
npm run test:coverage # Run tests with coverage
npm run analyze      # Analyze bundle size
```

### CI/CD Pipeline

The project includes a comprehensive CI/CD pipeline with:

#### Continuous Integration
- **Multi-Node Testing**: Tests on Node.js 18.x and 20.x
- **Code Quality**: ESLint, TypeScript checking, and formatting
- **Security Scanning**: npm audit, Snyk, and CodeQL analysis
- **Performance Testing**: Lighthouse CI with Core Web Vitals
- **Bundle Analysis**: Automated bundle size monitoring

#### Continuous Deployment
- **Preview Deployments**: Automatic preview deployments for PRs
- **Production Deployment**: Automated deployment to production on main branch
- **Release Management**: Automatic GitHub releases with versioning
- **Notifications**: Slack notifications for deployment status

#### Security Features
- **Dependency Scanning**: Daily security scans
- **Code Analysis**: Static code analysis with CodeQL
- **Vulnerability Monitoring**: Automated security alerts
- **SARIF Integration**: Security findings in GitHub Security tab

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/kanyoza/kanyozatech-portfolio.git
cd kanyozatech-portfolio
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

4. Configure your environment variables in `.env.local`:
```env
SMTP_HOST=smtp.gmail.com
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
SMTP_FROM=noreply@yoursite.com
CONTACT_EMAIL=your-contact@email.com
```

5. Start the development server:
```bash
npm run dev
```

## 🐳 Docker Deployment

### Local Development
```bash
docker-compose up --build
```

### Production Deployment
```bash
# Build the image
docker build -t kanyozatech-portfolio .

# Run the container
docker run -p 3000:3000 \
  -e SMTP_HOST=your-smtp-host \
  -e SMTP_USER=your-email \
  -e SMTP_PASS=your-password \
  kanyozatech-portfolio
```

## 🔒 Security Features

- **Security Headers**: X-Frame-Options, CSP, HSTS
- **Rate Limiting**: API endpoint protection
- **Input Validation**: Zod schema validation
- **HTTPS Enforcement**: SSL/TLS configuration
- **Dependency Scanning**: Automated vulnerability detection

## 🎨 Customization

### Personal Information
Update the personal information in:
- `lib/data/projects.ts` - Your projects
- `lib/data/skills.ts` - Your skills and expertise
- `lib/data/blog-posts.ts` - Your blog posts
- `components/sections/hero.tsx` - Personal introduction
- `components/sections/footer.tsx` - Contact information

### Advanced Components
- `components/advanced/terminal.tsx` - Interactive terminal
- `components/advanced/code-showcase.tsx` - Code examples
- `components/advanced/performance-metrics.tsx` - Performance dashboard
- `components/advanced/tech-radar.tsx` - Technology visualization
- `components/advanced/analytics-dashboard.tsx` - Analytics charts

### Styling
The design system uses CSS custom properties for easy theming:
- Colors: Defined in `app/globals.css`
- Components: Built with TailwindCSS classes
- Animations: Configured in Framer Motion components

### Content Management
For a headless CMS integration:
1. Choose your CMS (Sanity, Contentful, Strapi)
2. Replace static data files with API calls
3. Update TypeScript interfaces in `lib/types.ts`

## 📊 Monitoring & Analytics

### Performance Monitoring
- **Core Web Vitals**: FCP, LCP, CLS, TTI tracking
- **Bundle Analysis**: Automated bundle size monitoring
- **Lighthouse Scores**: Continuous performance testing

### Security Monitoring
- **Dependency Scanning**: Daily vulnerability scans
- **Code Quality**: Automated code analysis
- **Security Headers**: OWASP compliance

## 🚀 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Configure environment variables in Vercel dashboard
4. Deploy automatically on every push

### Other Platforms
The portfolio works on any platform supporting Next.js:
- Netlify
- Railway
- AWS Amplify
- Digital Ocean App Platform

### GitHub Actions Setup

Required secrets for CI/CD:
```
VERCEL_TOKEN          # Vercel deployment token
VERCEL_ORG_ID         # Vercel organization ID
VERCEL_PROJECT_ID     # Vercel project ID
SNYK_TOKEN           # Snyk security scanning token
SLACK_WEBHOOK_URL    # Slack notifications webhook
LHCI_GITHUB_APP_TOKEN # Lighthouse CI token
```

## 📊 Performance

- **Core Web Vitals**: Optimized for excellent scores
- **Lighthouse Score**: 95+ across all metrics
- **Image Optimization**: Next.js Image component with lazy loading
- **Code Splitting**: Automatic with Next.js
- **Caching**: Static generation with ISR support

### Performance Benchmarks
- **Lighthouse Score**: 95+ across all metrics
- **First Contentful Paint**: < 1.2s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1
- **Time to Interactive**: < 3.8s

## 🔧 Development

### Project Structure
```
├── app/                 # Next.js 13+ app directory
│   ├── api/            # API routes
│   ├── globals.css     # Global styles
│   ├── layout.tsx      # Root layout
│   └── page.tsx        # Home page
├── components/         # React components
│   ├── sections/       # Page sections
│   ├── advanced/       # Advanced interactive components
│   ├── ui/            # UI components
│   └── providers/     # Context providers
├── __tests__/         # Test files
├── .github/           # GitHub Actions workflows
├── lib/               # Utilities and data
│   ├── data/          # Static data
│   └── types.ts       # TypeScript definitions
├── public/            # Static assets
├── Dockerfile         # Docker configuration
└── docker-compose.yml # Docker Compose setup
```

## 🧪 Testing

### Test Coverage
- **Unit Tests**: Component and utility function testing
- **Integration Tests**: API route testing
- **E2E Tests**: User workflow testing
- **Performance Tests**: Lighthouse CI integration

### Running Tests
```bash
npm test                 # Run all tests
npm run test:watch      # Watch mode
npm run test:coverage   # Coverage report
```

## 📝 Content Guidelines

### Projects
- Use high-quality images (1200x600 recommended)
- Include comprehensive descriptions
- Add live demo and GitHub links
- Categorize projects appropriately

### Blog Posts
- Write in MDX format for rich content
- Include meta information (date, tags, reading time)
- Use descriptive titles and summaries
- Add featured images for better engagement

### Skills
- Rate skills honestly (0-100)
- Group by categories (frontend, backend, etc.)
- Include relevant icons and colors
- Update regularly as you learn

## 🔄 CI/CD Workflow

### Pull Request Workflow
1. **Code Quality Checks**: Linting, type checking, testing
2. **Security Scanning**: Dependency audit, code analysis
3. **Performance Testing**: Lighthouse CI, bundle analysis
4. **Preview Deployment**: Automatic Vercel preview
5. **Review Process**: Automated checks + manual review

### Production Deployment
1. **Merge to Main**: Triggers production pipeline
2. **Full Test Suite**: All quality and security checks
3. **Production Build**: Optimized build generation
4. **Deployment**: Automatic Vercel production deployment
5. **Release Creation**: Automated GitHub release
6. **Notifications**: Slack deployment notifications

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### Development Guidelines
- Follow TypeScript best practices
- Write tests for new features
- Maintain 70%+ test coverage
- Follow conventional commit messages
- Update documentation for new features

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing framework
- [TailwindCSS](https://tailwindcss.com/) for the utility-first CSS
- [Framer Motion](https://www.framer.com/motion/) for smooth animations
- [Shadcn/ui](https://ui.shadcn.com/) for beautiful components
- [Lucide](https://lucide.dev/) for the icon set
- [Recharts](https://recharts.org/) for data visualization
- [Jest](https://jestjs.io/) for testing framework

## 📞 Support

If you have questions or need help customizing the portfolio:
- Open an issue on GitHub
- Reach out via the contact form
- Connect on LinkedIn

---

Built with ❤️ by [Kanyoza Innocent](https://kanyozatech.com)# Port

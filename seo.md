---

## 📜 `seo.md` (SEO Best Practices)  

```md
# SEO Best Practices  

## 🔹 General SEO Strategy  
- Ensure **fast page load speeds** (use Lighthouse for performance audits).  
- Follow **mobile-first design** principles.  
- Use **semantic HTML5 elements** for better indexing.  
- Implement **structured data (Schema.org)** for rich search results.  

## 🔹 On-Page SEO  

### 1️⃣ **Title & Meta Tags**  
- Titles: **50-60 characters**, with primary keywords first.  
- Meta Descriptions: **120-160 characters**, including a CTA.  
- Use **React Helmet** or Django's `{% block meta %}` for dynamic metadata.  

### 2️⃣ **Keyword Optimization**  
- Identify primary and secondary keywords.  
- Use keywords in **H1-H3 headers, first 100 words, and alt attributes**.  

### 3️⃣ **Internal Linking & Navigation**  
- Maintain a **clear site structure** with breadcrumbs.  
- Link related articles to increase engagement.  

## 🔹 Technical SEO  

### 1️⃣ **Page Speed & Performance**  
- Use **lazy loading** for images (`loading="lazy"`).  
- Optimize images with **WebP** format.  
- Minimize **JavaScript blocking** by deferring scripts.  

### 2️⃣ **Crawlability & Indexing**  
- Ensure **robots.txt** and **sitemap.xml** are configured.  
- Use **canonical tags** to prevent duplicate content.  
- Avoid JavaScript-heavy content that isn’t SEO-friendly.  

### 3️⃣ **Accessibility & User Experience**  
- Ensure contrast ratios meet **WCAG 2.1 standards**.  
- Use **ARIA attributes** for screen readers.  
- Enable **keyboard navigation** for interactive elements.  

## 🔹 Off-Page SEO  
- Build **high-quality backlinks** from authoritative sources.  
- Encourage **social media shares** for organic traffic.  
- Monitor site rankings with **Google Search Console**.  

---
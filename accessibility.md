
# Accessibility Best Practices

## 🔹 Core Principles
1. **WCAG 2.2 Compliance**: Meet AA standard as minimum requirement
2. **Progressive Enhancement**: Ensure functionality without JavaScript
3. **Assistive Technology First**: Prioritize screen reader/screen magnifier compatibility
4. **Perceivable & Navigable**: Content accessible through multiple modalities

---

## 🔹 Semantic HTML Implementation

### 1. **Landmark Structure**
```html
<header role="banner">
  <nav aria-label="Main navigation">...</nav>
</header>
<main role="main">
  <article>...</article>
</main>
<aside role="complementary">...</aside>
<footer role="contentinfo">...</footer>
```

### 2. **ARIA Roles & Properties**
- Use `aria-label` for ambiguous controls
- Implement `aria-live` for dynamic content updates
- Apply `aria-expanded` for collapsible sections
- Use `role="alert"` for critical notifications

### 3. **Form Accessibility**
```html
<label for="email">Email address</label>
<input type="email" id="email" 
       aria-describedby="email-help"
       required>
<p id="email-help" class="sr-only">
  Must contain @ symbol
</p>
```

---

## 🔹 Keyboard Navigation Requirements

### **Essential Behaviors**
1. Logical tab order (follows visual flow)
2. Visible focus indicators
3. Skip navigation link (first interactive element)
4. No keyboard traps

### **Custom Component Requirements**
| Component      | Keyboard Support           |
|----------------|----------------------------|
| Dropdown       | Arrow keys, Esc            |
| Modal          | Trap focus, Esc close      |
| Carousel       | Arrow keys, Home/End       |
| Accordion      | Enter/Space to toggle      |

---

## 🔹 Visual Accessibility

### 1. **Color Contrast**
- Text: **4.5:1** minimum (AA)
- Large Text: **3:1** minimum
- Non-text Elements: **3:1** contrast

### 2. **Responsive Design**
- Support 200% zoom without breaking layout
- Maintain readability at 1280px width
- Ensure touch targets ≥48x48px

### 3. **Alternative Representations**
```markdown
- Images: `alt` text (descriptive for content, empty for decorative)
- Charts: Tabular data equivalent
- Audio/Video: Closed captions & transcripts
- Icons: Text labels or `aria-label`
```

---

## 🔹 Testing & Validation

### **Automated Tools**
```bash
# Run these in CI/CD pipeline
npm install axe-core --save-dev
npx playwright test --accessibility
lighthouse --accessibility <url>
```

### **Manual Checks**
1. Full navigation using screen reader (NVDA/JAWS)
2. Keyboard-only operation
3. Windows High Contrast Mode test
4. Mobile screen reader testing (VoiceOver/TalkBack)

---

## 🔹 Framework-Specific Guidelines

### **React**
```jsx
// Accessible modal component
function Modal({ children }) {
  useEffect(() => {
    const mainContent = document.getElementById('main');
    mainContent.setAttribute('aria-hidden', 'true');
    return () => mainContent.removeAttribute('aria-hidden');
  }, []);

  return (
    <div role="dialog" aria-modal="true">
      {children}
    </div>
  );
}
```

### **Django**
```python
# Accessible form errors
class SignUpForm(forms.ModelForm):
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        for field in self.fields:
            self.fields[field].widget.attrs.update({
                'aria-describedby': f'{field}-help'
            })
```

---

## 🔹 Accessibility Checklist
- [ ] All images have proper alt text
- [ ] Color contrast meets WCAG AA
- [ ] Full keyboard navigation support
- [ ] ARIA landmarks implemented
- [ ] Form fields have associated labels
- [ ] No autoplaying media
- [ ] Accessible error messages
- [ ] Screen reader testing completed
- [ ] Reduced motion support
- [ ] Language attribute set
- [ ] Heading hierarchy maintained

---

## 🔹 Legal Requirements
1. **ADA Title III** (US)
2. **Section 508** (US Government)
3. **EN 301 549** (EU)
4. **AODA** (Canada)
5. **DDA** (Australia)

*Last updated: [DATE] - Update frequency: Quarterly*
```

---

This document ensures your auto-coder:  
1. Generates accessible code by default  
2. Includes accessibility checks at every development phase  
3. Maintains compliance with international standards  
4. Provides clear testing protocols  

Would you like me to create a companion **accessibility-testing.md** file with detailed test cases? 🦮
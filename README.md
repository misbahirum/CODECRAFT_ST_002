# CODECRAFT_ST_002
# 🛠️ Cross-Browser Compatibility Testing Report  

**Project:** E-commerce Demo Website  
**URL:** [Shoplane by Lassie](https://shoplane-by-lassie.netlify.app/)  
**Browsers Tested:** Chrome, Edge, Firefox  
**Devices Tested:** Desktop, Tablet, Mobile  
**Tester:** QA Engineer  

---

## 📌 Test Summary  

| Browser   | Desktop | Tablet | Mobile |
|-----------|---------|--------|--------|
| Chrome    | Pass (except Clothing & Accessories links) | Pass (except Clothing & Accessories links) | **Fail (Homepage overlap + Clothing & Accessories links)** |
| Edge      | Pass (except Clothing & Accessories links) | Pass (except Clothing & Accessories links) | **Fail (Homepage overlap + Clothing & Accessories links)** |
| Firefox   | Pass (except Clothing & Accessories links) | Pass (except Clothing & Accessories links) | **Fail (Homepage overlap + Clothing & Accessories links)** |

---

## 🔍 Detailed Findings  

### 1. Page Load  
- Homepage loads correctly across all browsers.  
- **Clothing (`/clothing.html`) and Accessories (`/accessories.html`) pages FAIL (404 error)** on **all browsers and all devices**.  

### 2. Navigation  
- Navbar visible across browsers.  
- Clothing & Accessories links broken (404).  

### 3. Functionality  
- **Add to Cart:** ✅ Working in all browsers.  
- **Remove from Cart / Update Quantity:** ✅ Working correctly.  
- **Checkout:** ✅ Redirects correctly.  

### 4. Layout & Responsiveness  
- **Desktop:** Layout responsive and clean.  
- **Tablet:** Layout adjusts properly, no overlaps.  
- **Mobile:**  
  - ❌ Homepage overlap issue in **Chrome, Edge, Firefox**.  

---

## ❌ Issues Found  

| Issue | Browser | Device | Description | Severity | Suggested Fix |
|-------|---------|--------|-------------|----------|---------------|
| Broken Link: Clothing Page | Chrome, Edge, Firefox | Desktop, Tablet, Mobile | `/clothing.html` returns 404 error | High | Ensure file is deployed & navbar link updated. |
| Broken Link: Accessories Page | Chrome, Edge, Firefox | Desktop, Tablet, Mobile | `/accessories.html` returns 404 error | High | Ensure file is deployed & navbar link updated. |
| Layout Overlap (Homepage) | Chrome, Edge, Firefox | Mobile | Homepage elements overlap on small screens | High | Fix CSS breakpoints for mobile view across all browsers. |

---

## 💡 Recommendations  

1. Fix **Clothing & Accessories links** (currently broken on all devices & browsers).  
2. Fix **Homepage mobile overlap issue** (affecting Chrome, Edge, Firefox).  
   - Update CSS media queries for small screen widths.  
   - Test again across multiple device sizes (320px, 375px, 414px, etc.).  
3. Retest across all browsers after fixes.  
4. Optimize heavy images for better performance (optional).  

---

## ✅ Conclusion  

- **Chrome & Edge:** Functional and responsive except for Clothing & Accessories broken links and **homepage mobile overlap**.  
- **Firefox:** Same link issues + **homepage mobile overlap**.  
- Website requires **navigation fixes** and **responsive CSS adjustments** before production-ready release.  

---

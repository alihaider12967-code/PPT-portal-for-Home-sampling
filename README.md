# Home Sampling Portal (GitHub Pages version)

Yeh ek static web portal hai. Kisi server ya software ki zarurat nahi, aur claude.ai ya Google login nahi maanga jata.

## Files
- `index.html`  : poora portal (dashboard, upload, tables, PPT)
- `data.js`     : sara data (har mahine ka). Isi file ko update karna hota hai.
- `lib/`        : zaroori libraries (Excel parhna, PPT banana). Internet ke bagair bhi chalti hain.

## GitHub par lagane ka tareeqa
1. github.com par naya repository banayen (maslan `hs-portal`).
2. "Add file > Upload files" se `index.html`, `data.js` aur poora `lib` folder upload karein, phir Commit karein.
3. Repository mein Settings > Pages kholen. "Deploy from a branch" chunen, branch `main`, folder `/ (root)`, Save.
4. 1-2 minute baad aap ka link yeh hoga: `https://<aap-ka-username>.github.io/hs-portal/`
5. Yeh link kisi ko bhi bhej dein, koi login nahi chahiye.

## DHYAN: privacy
Free GitHub account par GitHub Pages ke liye repository **public** honi chahiye. Is ka matlab hai ke link jis ke paas ho wo data dekh sakta hai, aur `data.js` file repository mein sab ko nazar aa sakti hai. Agar data company ka private hai to:
- GitHub ka paid plan (private Pages) istemal karein, ya
- Netlify / Cloudflare Pages / company ka apna server jahan password laga sakein.

## Har mahine naya data kaise daalen
1. Portal kholen, **Upload** tab par jayen.
2. Year aur Month chunen, 3 files (KPI, Complaints, Pre-Analytical) upload karein, "Read files" dabayen.
3. Preview mein NOP (patients) bharein aur numbers check karein, phir "Save to portal".
4. **Tables** tab par "Download data.js (for GitHub)" dabayen.
5. GitHub repository mein purani `data.js` ko nayi `data.js` se replace karein (Add file > Upload files, wahi naam). Commit karein.
6. 1-2 minute baad sab ko naya data nazar aa jayega.

Note: Save karne ke baad data sirf aap ke browser mein hota hai jab tak aap `data.js` GitHub par replace na karein.

## Data kahan hai
Koi database server nahi hai. Data `data.js` file mein hai (jis ki copy GitHub par rehti hai). Browser mein jo naye changes hon wo us browser ke localStorage mein rehte hain jab tak aap unhein `data.js` mein export na karein.

## Shared database chahiye (sab live ek hi data mein likhein)?
GitHub Pages sirf static files dikhata hai, is liye wo mumkin nahi. Iske liye Firebase ya Supabase jaise free database service chahiye hogi (ek chhota sa setup).

# Chicken Runner - GitHub se APK banane ka tareeqa

Is folder me tumhari poori (customized) game already maujood hai — naam, sounds, speed,
score system, sab kuch. Bas GitHub par upload karo, aur GitHub ke apne servers par
free me asli, installable APK ban jayegi.

## Step 1: GitHub account banao (agar nahi hai)
https://github.com par jao aur free account bana lo.

## Step 2: Naya repository banao
1. GitHub par login karne ke baad, upar right corner me **"+"** icon dabao -> **"New repository"**
2. Naam do: `chicken-runner` (ya jo chaho)
3. **Public** ya **Private** — dono chalega
4. "Create repository" dabao (README/gitignore add karne ki zaroorat nahi)

## Step 3: Yeh saari files upload karo
Is poore folder (`github_apk_build`) ke andar jo bhi hai — `config.xml`, `www/` folder,
`res/` folder, aur `.github/workflows/build-apk.yml` — sab kuch apne naye repository
me upload karna hai.

**Sabse aasan tareeqa (website se, bina command line ke):**
1. Apni nayi repository ke page par jao
2. "uploading an existing file" wala link dabao (ya **Add file -> Upload files**)
3. Is poore folder ka content select karo aur drag-drop kar do
   - ⚠️ Zaroori: `.github` folder (jisme `workflows` hai) bhi zaroor upload karna hai —
     yeh chhupa hua (hidden) folder lagta hai, isliye dhyan se select karna
4. Neeche "Commit changes" dabao

## Step 4: Build apne aap shuru ho jayegi
Jaise hi files upload/commit hongi, GitHub Actions apne aap APK banana shuru kar dega.

Dekhne ke liye:
1. Apni repository ke upar **"Actions"** tab par jao
2. "Build Chicken Runner APK" wala workflow dikhega, usme click karo
3. Build chalte hue dekh sakte ho (takreeban 5-10 minute lagte hain)
4. Jab hara ✅ tick aa jaye (build complete), usi page ke neeche
   **"Artifacts"** section me `ChickenRunner-debug-apk` milega
5. Usay download karo — yeh ek `.zip` file hogi, usay extract karo,
   andar asli `.apk` file milegi

## Step 5: Phone par install karo
1. APK file apne Android phone par copy karo (USB, Google Drive, WhatsApp - kuch bhi)
2. Phone par "Unknown sources" / "Install unknown apps" allow karo (Settings me)
3. APK par tap karo -> Install

## Agar build fail ho jaye
Actions tab me us failed run par click karo, red ❌ wala step dikhega, uska error
message paste kar ke mujhe bhejo, main fix kar dunga.

## Note
Yeh **debug APK** hai — apne phone par test karne ke liye bilkul theek hai. Agar
Google Play Store par publish karni ho, to us waqt "release" build aur signing key
ki zaroorat hogi — woh alag step hai, tab bata dena.

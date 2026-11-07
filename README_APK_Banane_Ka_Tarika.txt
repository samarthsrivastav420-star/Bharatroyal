BHARAT ROYALE - APK / AAB BANANE KA TARIKA
===========================================
Is project mein game (index.html) pehle se andar hai. Aapko bas build karna hai.

TARIKA 1 (sabse aasaan, laptop ya phone ka browser kaafi hai) - GitHub se
1. github.com par free account banao -> New repository banao (naam: bharat-royale).
2. Is zip ko khol kar uske andar ki saari files repository mein upload karo
   (Add file -> Upload files). Agar ".github" folder upload na ho to:
   Add file -> Create new file -> naam likho:  .github/workflows/build.yml
   aur "build.yml.txt" ka poora text usme paste kar do.
3. Upar "Actions" tab -> "Build Bharat Royale APK and AAB" -> Run workflow.
4. 6-10 minute baad run ke andar "Artifacts" mein
      BharatRoyale-APK  (phone mein install karne ke liye)
      BharatRoyale-AAB  (Google Play ke liye)
   download karo. Dono ke andar zip hota hai - kholo.
5. APK ko phone mein bhej kar install karo (Unknown sources allow karna padega).

TARIKA 2 - Android Studio se
1. Android Studio install karo -> File -> Open -> ye BharatRoyale_Android folder.
2. Gradle sync hone do (internet chahiye). Gradle 8.7 maange to wahi chuno.
3. Offline chalane ke liye: https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js
   file download karke app/src/main/assets/ mein "three.min.js" naam se rakho, aur
   app/src/main/assets/index.html mein us link ki jagah sirf  three.min.js  likh do.
   (Ye na karo to game chalega, par pehli baar internet chahiye.)
4. Build -> Build Bundle(s) / APK(s) -> Build APK(s)  ya  Generate Signed Bundle (AAB).

TARIKA 3 - bina APK ke (PWA)
PWA_Install_Without_APK folder ko GitHub Pages ya Netlify par daalo, phir phone
ke Chrome mein kholo -> menu -> "Add to Home screen". App ki tarah chalega.

ZAROORI BAATEN
* Google Play par daalne ke liye: Play Console account (ek baar ~$25), aur apni
  KHUD ki signing key chahiye. GitHub mein Settings -> Secrets mein ye 3 daalo:
  KEYSTORE_BASE64, KEYSTORE_PASSWORD, KEY_ALIAS. Nahi daaloge to har build par
  nayi temporary key banti hai - us APK ko purane ke upar update nahi kar sakte.
* "Friends" (dost ke saath khelna) sirf claude.ai ke page par chalta tha,
  APK/PWA mein nahi chalega. Uske liye alag server banana padega.
* Game ke account/level/coins phone mein hi save hote hain.
* App landscape (leti hui screen) mein khulta hai, back button 2 baar dabane par band hota hai.
* Play Store icon: PlayStore_Icon_512.png.

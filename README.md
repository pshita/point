# לוח נקודות כיתה

אתר סטטי (HTML/CSS/JS פשוטים, ללא build step) ללוח ניקוד כיתתי, עם שמירה
משותפת בין כל המחשבים דרך Firebase (Firestore). אין תלות בחשבון קלוד.

## הגדרה חד-פעמית (Firebase)

1. נכנסים ל-[console.firebase.google.com](https://console.firebase.google.com/)
   ויוצרים **פרויקט חדש** (חינמי, לא דורש כרטיס אשראי).
2. **Build → Firestore Database → Create database** → מצב **Production**.
3. בלשונית **Rules** של Firestore, מדביקים את התוכן של `firestore.rules`
   מהריפו הזה ולוחצים **Publish**.
4. **Project settings → General → Your apps** → מוסיפים אפליקציית **Web**
   (`</>`), ומעתיקים את אובייקט ה-config שמופיע.
5. מדביקים את הערכים בקובץ `firebase-config.js` במקום ה-`PASTE_...`.

לאחר מכן האתר יעבוד אוטומטית — אין צורך בשינוי קוד נוסף.

## הרצה מקומית

```bash
python3 -m http.server 8000
# ואז נכנסים ל־http://localhost:8000
```

## GitHub Pages

תחת Settings → Pages בריפו, בוחרים Source: Deploy from branch, ענף `main`,
תיקייה `/ (root)`.

# Admin Panel Guide - How to Login and Add Content

Complete guide for using the admin panel to manage your portfolio website.

## 🔐 Step 1: Access Admin Login

### Your Admin Login URL:

```
https://your-vercel-site.vercel.app/admin/login
```

Replace `your-vercel-site` with your actual Vercel domain.

**Example:**
- If your site is `portfolio-website.vercel.app`, then:
- Admin login: `https://portfolio-website.vercel.app/admin/login`

---

## 👤 Step 2: Login Credentials

Use the **Supabase admin user** you created:

1. **Go to Supabase Dashboard:**
   - Visit: https://supabase.com/dashboard
   - Select your project
   - Go to **Authentication** → **Users**

2. **Find Your Admin User:**
   - You should see the user you created
   - Email: The email you used
   - Password: The password you set

3. **Login:**
   - Go to your admin login page
   - Enter the email and password
   - Click "Sign In"

---

## 🎯 Step 3: Using the Admin Dashboard

After logging in, you'll see the **Admin Dashboard** with these sections:

### Available Sections:

1. **Grants** - Manage funded grants
2. **Publications** - Manage research publications
3. **Administration** - Manage admin roles
4. **Patents** - Manage patents
5. **Awards** - Manage awards and recognition
6. **Events** - Manage organized events
7. **Gallery** - Upload and manage images
8. **Profile** - Update profile information

---

## 📝 Step 4: Adding Content

### Adding a Grant:

1. **Click "Grants"** in dashboard
2. **Click "Add Grant"** button
3. **Fill in the form:**
   - Title: "Optimal energy management system in shipboard power system with solar PV"
   - Funding Agency: "DST"
   - Amount: "Amount if available" (optional)
   - Period: "2020-2023"
   - Status: Select "completed" or "ongoing"
   - Description: Add details (optional)
4. **Click "Save"**
5. **Grant appears** on the Grants page immediately!

### Adding a Publication:

1. **Click "Publications"** in dashboard
2. **Click "Add Publication"** button
3. **Fill in the form:**
   - Title: Publication title
   - Authors: "J. Preetha Roselyn, et al."
   - Journal: Journal name
   - Year: 2024
   - DOI: If available (optional)
   - Link: URL to paper (optional)
4. **Click "Save"**
5. **Publication appears** on Publications page!

### Adding an Award:

1. **Click "Awards"** in dashboard
2. **Click "Add Award"** button
3. **Fill in:**
   - Title: "IEEE Publication Award"
   - Organization: "IEEE"
   - Year: 2019
   - Description: Award details (optional)
4. **Click "Save"**

### Adding an Event:

1. **Click "Events"** in dashboard
2. **Click "Add Event"** button
3. **Fill in:**
   - Title: Event name
   - Type: Select (conference, workshop, seminar, other)
   - Date: "2024-01-15"
   - Location: Event location (optional)
   - Description: Event details (optional)
4. **Click "Save"**

### Adding a Patent:

1. **Click "Patents"** in dashboard
2. **Click "Add Patent"** button
3. **Fill in:**
   - Title: Patent title
   - Patent Number: If available
   - Area: "Building automation"
   - Status: "filed" or "granted"
   - Year: Patent year
4. **Click "Save"**

### Adding an Admin Role:

1. **Click "Administration"** in dashboard
2. **Click "Add Admin Role"** button
3. **Fill in:**
   - Title: "Chairman"
   - Organization: "MTS India Section"
   - Period: "2020 - Present"
   - Description: Role details (optional)
4. **Click "Save"**

---

## 🖼️ Step 5: Uploading Gallery Images

1. **Click "Gallery"** in dashboard
2. **Click "Add Image"** button
3. **Upload Image:**
   - Click "Choose Image"
   - Select image file (JPG, PNG, GIF - max 5MB)
   - Image preview will show
4. **Add Details:**
   - Caption: Image description (optional)
   - Category: "Events", "Awards", etc. (optional)
5. **Click "Upload Image"**
6. **Wait for upload** (shows "Uploading...")
7. **Image appears** in gallery immediately!

**Note:** Images are stored in Supabase Storage and appear on the Gallery page.

---

## ✏️ Step 6: Editing Content

1. **Go to any section** (Grants, Publications, etc.)
2. **Find the item** you want to edit
3. **Click the "Edit" icon** (pencil icon)
4. **Modify the fields**
5. **Click "Save"**
6. **Changes appear** immediately on the website!

---

## 🗑️ Step 7: Deleting Content

1. **Go to any section**
2. **Find the item** you want to delete
3. **Click the "Delete" icon** (trash icon)
4. **Confirm deletion**
5. **Item is removed** from the website immediately!

---

## 🔄 Step 8: Updating Profile (Coming Soon)

The Profile section will allow you to update:
- Name, title, department
- Bio and qualifications
- Specialization areas
- Achievements
- Contact information

---

## ✅ Quick Checklist for Adding Your Content

Based on the information provided, here's what to add:

### Grants:
- [ ] DST funded project - "Optimal energy management system in shipboard power system with solar PV"
- [ ] MODROB funded project from AICTE (microgrid)
- [ ] Two MOES funded projects (Digital twin and Image processing)
- [ ] Co-PI of 4 SATU projects
- [ ] 3 internally funded projects

### Publications:
- [ ] Add all 55 international publications
- [ ] Include book: "GA based placement of FACTS devices for voltage stability Enhancement"

### Administration Roles:
- [ ] Chairman of MTS India Section
- [ ] Faculty mentor of SRM Marine Technology Society student chapter

### Patents:
- [ ] Building automation patents
- [ ] Underwater AUVs patents

### Awards:
- [ ] IEEE publication award
- [ ] John P Craven mentor international award
- [ ] Honorary Rosalind member of London Journals Press

### Events:
- [ ] Add all organized conferences, workshops, seminars

### Gallery:
- [ ] Upload photos from events
- [ ] Add award ceremony photos
- [ ] Add conference photos

---

## 🆘 Troubleshooting

### Can't Login:

1. **Check Credentials:**
   - Verify email/password in Supabase Dashboard
   - Make sure user is confirmed (Auto Confirm: Yes)

2. **Check Supabase Connection:**
   - Verify environment variables in Vercel
   - Check Supabase project is active

3. **Try Again:**
   - Clear browser cache
   - Try incognito mode
   - Check browser console for errors

### Content Not Saving:

1. **Check Database:**
   - Verify tables exist in Supabase
   - Check Row Level Security policies
   - Make sure you're logged in

2. **Check Browser Console:**
   - Open Developer Tools (F12)
   - Look for error messages
   - Check Network tab

### Images Not Uploading:

1. **Check Storage:**
   - Verify `gallery` bucket exists in Supabase
   - Check bucket is public
   - Verify Storage policies

2. **Check File Size:**
   - Max 5MB per image
   - Use JPG/PNG format

---

## 💡 Tips

1. **Save Often:** Content saves immediately, no need to worry
2. **Use Descriptions:** Add descriptions for better context
3. **Organize Gallery:** Use categories to organize images
4. **Test Public View:** Check how content looks on public pages
5. **Backup:** Your data is safe in Supabase!

---

## 🔗 Quick Links

- **Your Website:** `https://your-site.vercel.app`
- **Admin Login:** `https://your-site.vercel.app/admin/login`
- **Supabase Dashboard:** https://supabase.com/dashboard
- **Vercel Dashboard:** https://vercel.com/dashboard

---

**You're all set!** Start adding your content and your portfolio website will be complete! 🎉

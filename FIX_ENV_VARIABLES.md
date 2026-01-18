# Fix: Environment Variables Not Set in Vercel

## 🔴 The Problem

The error `placeholder.supabase.co` means Vercel is using placeholder values instead of your real Supabase credentials.

## ✅ Solution: Add Environment Variables in Vercel

### Step 1: Get Your Supabase Credentials

1. **Go to Supabase Dashboard:**
   - Visit: https://supabase.com/dashboard
   - Select your project

2. **Get API Keys:**
   - Click **Settings** (gear icon) → **API**
   - Copy these two values:
     - **Project URL** (looks like: `https://xxxxx.supabase.co`)
     - **anon public key** (long string starting with `eyJ...`)

### Step 2: Add to Vercel

1. **Go to Vercel Dashboard:**
   - Visit: https://vercel.com/dashboard
   - Select your project (`portfolio-website`)

2. **Go to Settings:**
   - Click **"Settings"** tab
   - Click **"Environment Variables"** in left sidebar

3. **Add First Variable:**
   - **Name:** `NEXT_PUBLIC_SUPABASE_URL`
   - **Value:** Paste your Supabase Project URL
   - **Environment:** Select all three:
     - ✅ Production
     - ✅ Preview  
     - ✅ Development
   - Click **"Save"**

4. **Add Second Variable:**
   - **Name:** `NEXT_PUBLIC_SUPABASE_ANON_KEY`
   - **Value:** Paste your Supabase anon/public key
   - **Environment:** Select all three:
     - ✅ Production
     - ✅ Preview
     - ✅ Development
   - Click **"Save"**

### Step 3: Redeploy

**IMPORTANT:** After adding environment variables, you MUST redeploy!

1. **Go to Deployments tab**
2. **Click the three dots** (⋯) on the latest deployment
3. **Click "Redeploy"**
4. **Wait 2-3 minutes** for rebuild

OR

1. **Make a small change** to trigger auto-deploy:
   ```bash
   # Make any small change, like adding a comment
   git commit --allow-empty -m "Trigger redeploy"
   git push origin main
   ```

### Step 4: Verify

1. **After redeploy completes:**
   - Visit your site
   - Try admin login again
   - Should work now!

---

## 🔍 How to Verify Variables Are Set

### Check in Vercel:

1. Go to Settings → Environment Variables
2. You should see:
   - `NEXT_PUBLIC_SUPABASE_URL` ✅
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY` ✅

### Check in Browser:

1. Open your site
2. Open Developer Tools (F12)
3. Go to Console tab
4. Type: `console.log(process.env.NEXT_PUBLIC_SUPABASE_URL)`
5. Should show your real Supabase URL (not placeholder)

---

## 🆘 Still Not Working?

### Check These:

1. **Variables are added:**
   - Settings → Environment Variables
   - Both variables exist

2. **Values are correct:**
   - Copy directly from Supabase Dashboard
   - No extra spaces
   - Full URL includes `https://`

3. **Redeployed after adding:**
   - Must redeploy for variables to take effect
   - Check deployment is complete

4. **Environment selected:**
   - Make sure Production is selected
   - Preview and Development too (for testing)

### Common Mistakes:

❌ **Wrong variable name:**
- Must be exactly: `NEXT_PUBLIC_SUPABASE_URL`
- Must be exactly: `NEXT_PUBLIC_SUPABASE_ANON_KEY`

❌ **Missing `NEXT_PUBLIC_` prefix:**
- Next.js requires this prefix for client-side variables

❌ **Not redeploying:**
- Variables only apply after redeploy

❌ **Wrong environment:**
- Make sure Production is checked

---

## 📝 Quick Checklist

- [ ] Got Supabase URL from Dashboard → Settings → API
- [ ] Got Supabase anon key from Dashboard → Settings → API
- [ ] Added `NEXT_PUBLIC_SUPABASE_URL` in Vercel
- [ ] Added `NEXT_PUBLIC_SUPABASE_ANON_KEY` in Vercel
- [ ] Selected all environments (Production, Preview, Development)
- [ ] Redeployed after adding variables
- [ ] Waited for deployment to complete
- [ ] Tested admin login again

---

## ✅ After Fixing

Once variables are set and redeployed:

1. **Visit admin login:**
   - `https://your-site.vercel.app/admin/login`

2. **Login with Supabase credentials:**
   - Email: Your Supabase user email
   - Password: Your Supabase user password

3. **Should work!** 🎉

---

**The error will be fixed once you add the environment variables and redeploy!**

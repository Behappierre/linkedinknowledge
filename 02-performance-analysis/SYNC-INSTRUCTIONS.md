# Repository Sync Instructions
## Fixing Outdated Project Files Issue

---

## 🚨 The Problem

**When Claude runs from mobile or browser:**
- Claude CANNOT access GitHub
- Claude falls back to reading `/mnt/project/` files
- These files are NEVER automatically synced with GitHub
- **Result: Claude gives you outdated information**

**When Claude runs from desktop/app:**
- Claude CAN access GitHub directly
- Claude reads current files
- **Result: Claude gives you correct information**

---

## ✅ Solutions

### Solution 1: Use Desktop/App (RECOMMENDED)

**Best practice:**
- Use Claude desktop or app version whenever possible
- This gives Claude direct GitHub access
- Always has latest data
- No sync issues

---

### Solution 2: Manual Sync Before Sessions

**If you must use mobile/browser:**

1. **Before starting analysis:**
   - Manually pull latest from GitHub
   - OR tell Claude: "Please pull latest from GitHub repository first"
   - Claude will fetch current data

2. **Check if data is current:**
   - Ask Claude: "What's the last update date in the rankings file?"
   - Compare with GitHub repository
   - If dates don't match, data is stale

---

### Solution 3: Manual Sync Script (FUTURE)

**Create this script on your system:**

```bash
#!/bin/bash
# sync-github-to-project.sh
# Syncs GitHub repository to project files

echo "🔄 Syncing GitHub → Project Files..."

# Navigate to repository
cd ~/linkedinknowledge

# Pull latest from GitHub
git pull origin main

# Copy to project directory
cp -r 02-performance-analysis/* /mnt/project/

echo "✅ Sync complete!"
echo "Last synced: $(date)"
```

**Usage:**
```bash
chmod +x sync-github-to-project.sh
./sync-github-to-project.sh
```

**Run this:**
- Before important analysis sessions
- After making significant GitHub updates
- Weekly to keep project files fresh

---

### Solution 4: Webhook Auto-Sync (IDEAL - Future)

**If you have server access:**

1. Set up GitHub webhook
2. Trigger on push events
3. Auto-pulls to `/mnt/project/`
4. Always in sync automatically

**This requires:**
- Server with webhook endpoint
- GitHub webhook configuration
- Auto-pull script

---

## 🎯 Best Practices

### Before Analysis Session

**Desktop/App:**
- ✅ Just start - Claude has GitHub access
- ✅ Data is always current

**Mobile/Browser:**
- ⚠️ Tell Claude: "Pull latest from GitHub first"
- ⚠️ OR accept data may be outdated
- ⚠️ Check last update date

---

### During Analysis

**If Claude gives outdated information:**
1. Stop the analysis
2. Tell Claude: "Please pull latest from GitHub"
3. Claude will fetch current data
4. Resume analysis

**Signs of outdated data:**
- Rankings don't match what you know
- Missing recent posts
- Old impression numbers
- Update dates are old

---

### After GitHub Updates

**If you update GitHub:**
1. Project files won't auto-update
2. Next mobile/browser session will be stale
3. Either: Use desktop/app next time
4. Or: Run manual sync script

---

## 📋 Quick Reference

| Scenario | Solution | Effort | Reliability |
|----------|----------|--------|-------------|
| Using desktop/app | Direct GitHub access | None | 100% |
| Using mobile/browser | Tell Claude to pull first | Low | 100% |
| Using mobile/browser | Accept outdated data | None | Variable |
| Regular sync needed | Manual sync script | Medium | High |
| Auto-sync | Webhook setup | High (one-time) | 100% |

---

## ⚠️ Important Notes

### GitHub is Always Source of Truth
- Repository: `https://github.com/Behappierre/linkedinknowledge`
- This is the canonical version
- All updates go here first
- Project files are secondary

### File Locations
- **GitHub:** `github.com/Behappierre/linkedinknowledge/02-performance-analysis/`
- **Project files:** `/mnt/project/`
- **NOT the same** - project files can be stale

### When Sync Matters
- **Critical:** Before important analysis or strategy sessions
- **Important:** After GitHub updates
- **Nice-to-have:** Weekly to stay current

### When Sync Doesn't Matter
- Quick conversational questions
- General strategy discussions
- Not relying on specific numbers

---

## 🔧 Troubleshooting

### "Claude gave me wrong impression numbers"
- **Cause:** Reading stale project files
- **Fix:** Tell Claude to pull from GitHub
- **Prevention:** Use desktop/app

### "Rankings don't match what I see on GitHub"
- **Cause:** Project files not synced
- **Fix:** Manual sync or pull latest
- **Prevention:** Use desktop/app or sync regularly

### "Claude says it can't access GitHub"
- **Cause:** Using mobile/browser
- **Options:** 
  1. Switch to desktop/app
  2. Accept limitations
  3. Set up manual sync

### "How do I know if data is current?"
- **Ask Claude:** "What's the last update date?"
- **Compare:** Check GitHub repository
- **Look for:** Recent commits, current dates

---

## 📝 Action Items

### Immediate (Choose One)
- [ ] **Option A:** Use desktop/app for analysis (EASIEST)
- [ ] **Option B:** Create manual sync script
- [ ] **Option C:** Accept occasional outdated data

### Short-Term
- [ ] Document which device you'll use for analysis
- [ ] Set up sync routine if using mobile/browser
- [ ] Test sync process works

### Long-Term (Optional)
- [ ] Investigate webhook auto-sync
- [ ] Fully automate if high-frequency usage

---

## 💡 Recommendation

**Best approach:**
1. **Primary:** Use Claude desktop/app for all LinkedIn analysis
2. **Backup:** If mobile/browser needed, tell Claude to pull first
3. **Future:** Set up manual sync script for convenience

**This ensures:**
- ✅ Always working with current data
- ✅ No confusion about rankings
- ✅ Correct strategic decisions
- ✅ Efficient analysis sessions

---

*Created: February 3, 2026*  
*For: Olivier Andre*  
*Status: ACTIVE - choose solution and implement*

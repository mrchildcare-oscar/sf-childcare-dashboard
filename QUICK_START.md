# SF Child Care Dashboard - Quick Start Guide

## 🚀 Resume Your Work

### Start Local Development Server
```bash
cd "/home/oscar/ECE SF Data"
python3 -m http.server 8000
```
Then open: **http://localhost:8000/index.html**

### Stop Local Server
```bash
pkill -f "python3 -m http.server 8000"
```

---

## 📁 Key Files

- **`index.html`** - Main dashboard (React app)
- **`childcare_all_coordinates.json`** - Facility data with coordinates
- **`add_cctr_info.py`** - Script to add CCTR contractor data
- **`add_sfusd_grades.py`** - Script to add PreK/TK data

---

## 🔧 Git Workflow

### Check Status
```bash
git status
git log --oneline -5
```

### Make Changes & Commit
```bash
git add .
git commit -m "Your descriptive message"
git push origin main
```

### View Branches
```bash
git branch -a
```

### Check Stashed Changes
```bash
git stash list
git stash show -p          # View stashed changes
git stash drop             # Delete if not needed
```

---

## 🌐 GitHub Repository

- **Repo:** https://github.com/mrchildcare-oscar/sf-childcare-dashboard
- **Main Branch:** https://github.com/mrchildcare-oscar/sf-childcare-dashboard/tree/main
- **JSON Data:** https://github.com/mrchildcare-oscar/sf-childcare-dashboard/blob/main/childcare_all_coordinates.json

---

## 📊 Dashboard Features

### Current Filters
- **Facility Type:** Day Care Center, Infant Center, etc.
- **License Status:** Licensed, Closed, etc.
- **ELFA Contracted:** Yes/No
- **Supervisor District:** 1-11 + No District Info
- **Capacity:** Min/Max range
- **Special Filters:**
  - SFUSD (39 facilities)
  - PreK (34 facilities)
  - TK (31 facilities)
  - Head Start (46 facilities)
  - CSPP (70 facilities)
  - CCTR (25 facilities)

### Default Filter
- **LICENSED** status is selected by default on page load

### Program Tags
- 🟣 **ELFA** - Early Learning for All
- 🟣 **SFUSD** - San Francisco Unified School District
- 🟣 **PreK** - Pre-Kindergarten
- 🟣 **TK** - Transitional Kindergarten
- 🟠 **HEAD START** - Federal Head Start
- 🟢 **CSPP** - California State Preschool Program
- 🟢 **CCTR** - CA Child Care & Development Services

---

## 🛠️ Common Tasks

### Update CCTR Contractor Data
```bash
python3 add_cctr_info.py
```

### Update SFUSD PreK/TK Data
```bash
python3 add_sfusd_grades.py
```

### Test Changes Locally
1. Start local server: `python3 -m http.server 8000`
2. Open: http://localhost:8000/index.html
3. Test your changes
4. Commit and push when ready

### Deploy to GitHub
```bash
git add .
git commit -m "Description of changes"
git push origin main
```

---

## 📝 Data Sources

- **ELFA:** https://sfdec.org/early-learning-for-all/early-learning-programs/
- **CCLD:** https://www.ccld.dss.ca.gov/carefacilitysearch/DownloadData
- **SFUSD:** https://www.sfusd.edu/schools/directory/table?field_school_type_target_id%5B317%5D=317
- **CCTR:** https://cdss.ca.gov/inforesources/child-care-and-development/contractor-resources/general-child-care-and-development-cctr-expansion/fy-24-25
- **CSPP:** https://www.cde.ca.gov/fg/fo/r2/cspp2425fundresults.asp

---

## 🎯 Quick Reference

### File Structure
```
/home/oscar/ECE SF Data/
├── index.html                          # Main dashboard
├── childcare_all_coordinates.json      # Facility data
├── add_cctr_info.py                    # CCTR data script
├── add_sfusd_grades.py                 # PreK/TK data script
├── QUICK_START.md                      # This file
└── .git/                               # Git repository
```

### Current Stats (as of last update)
- **Total Facilities:** 1,144
- **Licensed Facilities:** 892
- **Total Capacity:** 26,156 (licensed only)
- **SFUSD Sites:** 39 facilities across 37 schools
- **CCTR Contractors:** 3 (25 facilities)
- **Head Start Programs:** 46 facilities
- **CSPP Participants:** 70 facilities
- **PreK Programs:** 34 facilities
- **TK Programs:** 31 facilities

---

## 💡 Tips

1. **Always test locally** before pushing to GitHub
2. **Hard refresh** browser (Ctrl+Shift+R / Cmd+Shift+R) to see changes
3. **Commit frequently** with descriptive messages
4. **Check git status** before making changes
5. **Pull latest** if working from multiple locations: `git pull origin main`

---

## 🆘 Troubleshooting

### Server won't start
```bash
# Check if port 8000 is already in use
lsof -i :8000
# Kill existing server
pkill -f "python3 -m http.server 8000"
```

### Changes not showing
1. Hard refresh browser (Ctrl+Shift+R)
2. Clear browser cache
3. Check you're viewing the right file (index.html vs GitHub)

### Git push fails
```bash
# Check remote status
git remote -v
# Try push with credentials
git push origin main
```

---

**Last Updated:** December 13, 2025
**Dashboard Version:** Main (with CCTR, PreK/TK features)

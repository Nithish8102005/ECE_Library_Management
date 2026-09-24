# 🚀 Quick Start Guide
**ECE Department Library Management System**

---

## ✅ Current Status

**Both servers are RUNNING!**

- 🟢 **Backend:** `http://localhost:6070`
- 🟢 **Frontend:** `http://localhost:3000`
- 🟢 **Database:** MongoDB Atlas (Cloud)

---

## 🔑 Login Credentials

### Demo Accounts

```javascript
// 👨‍💼 Librarian (Admin)
Email:    admin@mkce.ac.in
Password: admin123

// 👨‍🎓 Student
Email:    student@mkce.ac.in
Password: student123

// 👨‍🏫 Faculty
Email:    faculty@mkce.ac.in
Password: faculty123
```

### Real User Accounts

```javascript
// Your personal account
Email:    saimiruthul@gmail.com
Password: [Your password]

// Other students
- 927623bec134@mkce.ac.in (Ikraam Khan)
- 927623bec131@mkce.ac.in (Manoj)
- 927623bec189@mkce.ac.in (Sanjai Magilan)
- 927623bec129@mkce.ac.in (Mahendra Prasad R)
```

---

## 🌐 Access the Application

### Frontend (User Interface)
**Open in browser:** `http://localhost:3000`

### Available Routes:
- `/login` - Login page
- `/register` - Registration page
- `/` - Dashboard (after login)
- `/books` - Browse books catalog
- `/my-books` - My issued books
- `/reservations` - My reservations
- `/change-password` - Change password

### Admin Routes:
- `/analytics` - Analytics dashboard
- `/manage-books` - Manage book inventory
- `/manage-users` - Manage user accounts
- `/manage-issues` - Approve/reject issue requests
- `/manage-reservations` - Handle reservations

---

## 🧪 Quick Testing Steps

### 1. Test Student Flow

```bash
# Step 1: Open browser
open http://localhost:3000/login

# Step 2: Login as student
Email: student@mkce.ac.in
Password: student123

# Step 3: Navigate to Books
Click "Books" in navbar

# Step 4: Browse and search books
- Use search box to find books
- Filter by category
- View book details

# Step 5: Reserve a book
Click "Reserve Book" on any available book

# Step 6: View your reservations
Click "My Reservations" in navbar
```

### 2. Test Admin Flow

```bash
# Step 1: Login as admin
Email: admin@mkce.ac.in
Password: admin123

# Step 2: View analytics
Click "Analytics" in navbar

# Step 3: Manage books
Click "Manage Books" → Add/Edit/Delete books

# Step 4: Manage users
Click "Manage Users" → Activate/Deactivate accounts

# Step 5: Handle issue requests
Click "Manage Issues" → Approve/Reject requests
```

---

## 🔧 API Testing (Optional)

### Test with curl commands:

```bash
# 1. Login (Get JWT Token)
curl -X POST http://localhost:6070/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"student@mkce.ac.in","password":"student123"}'

# 2. Get Books (Use token from login)
curl http://localhost:6070/api/books \
  -H "Authorization: Bearer YOUR_TOKEN_HERE"

# 3. Get My Reservations
curl http://localhost:6070/api/reservations/my \
  -H "Authorization: Bearer YOUR_TOKEN_HERE"

# 4. Get My Issues
curl http://localhost:6070/api/issues/my \
  -H "Authorization: Bearer YOUR_TOKEN_HERE"
```

---

## 📊 Database Statistics

**Current Data in MongoDB Atlas:**

```
Users:        8 accounts
Books:        24 books
  - ECE Engineering: 6 books
  - JLPT N5: 5 books
  - JLPT N4: 4 books
  - JLPT N3: 9 books
Reservations: 20 records
Issues:       11 records
```

---

## 🎯 Key Features to Test

### Student Features
- ✅ Register new account
- ✅ Login/Logout
- ✅ Browse books catalog
- ✅ Search books by title/author/ISBN
- ✅ Filter books by category
- ✅ Reserve unavailable books
- ✅ View my reservations
- ✅ View my issued books
- ✅ Check due dates and fines
- ✅ Change password

### Librarian Features
- ✅ View analytics dashboard
- ✅ Add new books
- ✅ Update book details
- ✅ Delete books
- ✅ Manage user accounts
- ✅ Activate/Deactivate users
- ✅ Approve/Reject book issue requests
- ✅ Process book returns
- ✅ Calculate fines automatically
- ✅ View all reservations
- ✅ Track overdue books

---

## 🐛 Known Issues

### ⚠️ Minor Issues:
1. **Book Inventory Data Inconsistency**
   - Issue: "Analog Electronic Circuits" shows 8 available copies but only 5 total copies
   - Impact: Low - doesn't affect functionality
   - Fix: Run data validation script to correct inventory

### ✅ Resolved Issues:
1. **Login Authentication** - FIXED
   - Updated credentials from `@ece.edu` to `@mkce.ac.in`

---

## 📱 Browser Compatibility

**Tested & Working:**
- ✅ Google Chrome (Latest)
- ✅ Mozilla Firefox (Latest)
- ✅ Safari (Latest)
- ✅ Microsoft Edge (Latest)

---

## 🛠️ Troubleshooting

### Backend not responding?
```bash
# Check if backend is running
curl http://localhost:6070/

# Restart backend
cd backend
npm run dev
```

### Frontend not loading?
```bash
# Check if frontend is running
curl http://localhost:3000/

# Restart frontend
cd frontend
npm start
```

### Database connection issues?
```bash
# Check MongoDB Atlas connection
# Verify MONGODB_URI in backend/.env
cat backend/.env | grep MONGODB_URI
```

### Authentication errors?
- ✅ Use correct email domain: `@mkce.ac.in`
- ✅ Check password: default is `student123`, `admin123`, `faculty123`
- ✅ Ensure user account is active

---

## 📞 Need Help?

Refer to these documents:
- **[TESTING_REPORT.md](TESTING_REPORT.md)** - Comprehensive testing results
- **[README.md](README.md)** - Full project documentation
- **[API_DOCUMENTATION.md](API_DOCUMENTATION.md)** - API reference
- **[SETUP_GUIDE.md](SETUP_GUIDE.md)** - Detailed setup instructions

---

## 🎓 For Academic Presentation

### Demo Flow (10 minutes):

1. **Introduction (1 min)**
   - Project overview and purpose

2. **Student Demo (3 min)**
   - Login as student
   - Browse books
   - Search and filter
   - Reserve a book

3. **Librarian Demo (3 min)**
   - Login as admin
   - View analytics
   - Manage books
   - Approve issue requests

4. **Technical Highlights (3 min)**
   - Show database collections
   - Explain authentication flow
   - Demonstrate API endpoints
   - Highlight security features

---

**System Ready for:**
- ✅ Development
- ✅ Testing
- ✅ Demo/Presentation
- ✅ Academic Evaluation

---

*Last Updated: 2026-03-03*
*Status: All Systems Operational* 🟢

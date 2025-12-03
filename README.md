Here’s the user roles hierarchy and functionality:

## USER ROLES HIERARCHY (Top to Bottom)

---

## LEVEL 1: Platform-Wide (SaaS Owner Side)

### 1. Super Admin
**Scope:** Entire platform (all organizations)

**Who:** Your team / platform owners

**Functionality:**
- Create/activate/suspend organizations (rescues)
- Access any organization's data for support/debugging
- Manage global platform settings and feature flags
- View billing across all organizations
- Handle customer support issues
- Monitor platform health and usage

**Example:** "Delhi Rescue is having payment issues" → Super Admin logs in and checks their billing, can fix payment problems

---

## LEVEL 2: Organization Level (Per Rescue)

### 2. Org Admin / Org Owner
**Scope:** Single organization (one rescue/shelter)

**Who:** Primary owner/manager of that rescue

**Functionality:**
- Complete control over their organization
- Manage organization profile (name, logo, contact info)
- Configure organization settings (timezone, currency, adoption fees)
- Set up integrations (Stripe, PayPal, Petfinder API keys)
- Manage billing for their organization
- Invite staff members and assign roles
- Remove/deactivate staff accounts
- See all data and reports for their organization
- Can switch between any role's view (for support)

**Example:** "I need to add Stripe payment" → Org Admin goes to Settings → Integrations → Adds Stripe API key

---

### 3. Coordinators (Functional Admins)

These roles manage specific areas. They have admin access within their domain, but cannot change organization settings or billing.

#### 3a. Adoption Coordinator
**Scope:** Adoption process for their organization

**Functionality:**
- View all adoption applications
- Approve/reject adoption applications
- Schedule and track home visits
- Check references (vet, personal)
- Generate adoption contracts
- Send contracts for e-signature
- Mark animals as "adopted" when contract signed
- Handle adoption returns (if adopter brings animal back)
- View adopter database
- Add adopter to "Do Not Adopt" list if needed
- See adoption reports (how many adopted this month, success rates)

**Example:** "John applied to adopt Max" → Adoption Coordinator reviews application → Approves → Sends contract → John signs → Coordinator marks Max as adopted

---

#### 3b. Foster Coordinator
**Scope:** Foster program for their organization

**Functionality:**
- View all foster applications
- Approve/reject foster applications
- Assign animals to foster homes
- Track which animals are in which foster home
- Monitor foster placements (start date, expected return)
- Communicate with foster parents
- View foster capacity (how many animals each foster can take)
- Manage foster availability (when fosters are available/unavailable)
- Handle foster returns (when animal comes back to shelter)
- See foster reports (how many in foster, average length of stay)

**Example:** "Sarah wants to foster" → Foster Coordinator reviews application → Approves → Assigns puppy "Bella" to Sarah → Tracks daily updates from Sarah

---

#### 3c. Volunteer Coordinator
**Scope:** Volunteer program for their organization

**Functionality:**
- View volunteer applications
- Approve volunteers
- Schedule volunteer shifts (cleaning, walking dogs, events)
- Assign tasks to volunteers
- Track volunteer hours
- Send volunteer reminders and communications
- Manage volunteer availability
- Generate volunteer reports (hours contributed, who's most active)
- Deactivate volunteers if needed

**Example:** "Raj wants to volunteer on weekends" → Volunteer Coordinator approves → Assigns Saturday morning dog-walking shift → Tracks his hours

---

#### 3d. Medical/Vet Coordinator
**Scope:** Medical records for their organization

**Functionality:**
- View all animals' medical records
- Add medical records (vaccinations, surgeries, checkups)
- Update vaccination schedules
- Flag animals needing medical attention
- Track medication schedules
- Record veterinarian information
- Upload medical documents (vaccine certificates, lab reports)
- See medical alerts (vaccinations due, surgeries scheduled)
- Generate medical reports (vaccination status, health statistics)
- Can mark animals as "medical hold" (not available for adoption due to health)

**Example:** "Max needs rabies vaccine" → Medical Coordinator adds vaccination record → System alerts when next vaccine due → Coordinator schedules follow-up

---

#### 3e. Finance/Donor Manager
**Scope:** Financial operations for their organization

**Functionality:**
- View all donations (one-time and recurring)
- Process donation refunds if needed
- Generate tax receipts for donors
- Manage donation campaigns
- View financial reports (monthly donations, trends)
- Track expenses per animal (vet costs, food, supplies)
- Reconcile payments (Stripe, PayPal)
- Export financial data for accounting
- See donor database
- Send thank-you emails to donors
- Cannot change organization billing (only Org Admin can)

**Example:** "Donor gave ₹5000" → Finance Manager sees donation → System auto-generates tax receipt → Manager sends receipt to donor

---

### 4. Staff (General Internal Users)

#### 4a. Shelter/Operations Staff
**Scope:** Day-to-day animal care and operations

**Functionality:**
- Create new animal records (when animal arrives at shelter)
- Update animal information (name, breed, photos)
- Add daily notes (fed, walked, behavior observed)
- Upload photos/videos of animals
- Update animal status (available, in foster, adopted)
- View animals they're assigned to
- Search for animals
- Print animal records for vet visits
- Cannot delete animals or change critical data
- Cannot access financial or donor information
- Cannot approve applications or contracts

**Example:** "New dog arrived today" → Staff member creates animal record → Adds intake info → Takes photos → Uploads to system

---

## LEVEL 3: External Users (Public-Facing)

These are people outside the rescue organization who interact with the platform.

### 5a. Adopter
**Scope:** Their own adoption application(s)

**Functionality:**
- Browse available animals (public listing)
- Submit adoption application for specific animal
- View application status (submitted, under review, approved, rejected)
- Upload requested documents (ID proof, residence proof)
- Receive email notifications about application status
- Sign adoption contract electronically
- View their adopted animals after adoption
- Submit post-adoption updates (optional)
- Cannot see other adopters' information
- Cannot see internal rescue notes

**Example:** "I want to adopt Max" → Adopter fills application form → Submits → Gets email "Application received" → Later gets email "Approved!" → Signs contract → Adoption complete

---

### 5b. Foster
**Scope:** Their foster application and assigned animals

**Functionality:**
- Submit foster application
- View application status
- See animals assigned to them (if approved)
- Submit daily care updates (fed, walked, health status)
- Upload photos/videos of fostered animals
- Communicate with foster coordinator
- View foster schedule (how long animal will be with them)
- Cannot see other fosters' information
- Cannot access shelter-wide data

**Example:** "I'm fostering Bella" → Foster logs in → Sees Bella's profile → Daily: uploads photo, adds note "Ate well, played in yard" → Coordinator sees updates

---

### 5c. Volunteer
**Scope:** Their volunteer profile and assigned tasks

**Functionality:**
- Submit volunteer application
- View application status
- See assigned shifts/tasks
- View schedule (what days/times they volunteered)
- Log volunteer hours (if enabled)
- Receive shift reminders
- View upcoming volunteer opportunities
- Cannot see other volunteers' schedules
- Cannot access animal/people records

**Example:** "I volunteer on Saturdays" → Volunteer logs in → Sees "This Saturday: Dog walking, 9am-12pm" → Can mark as completed → Hours tracked automatically

---

### 5d. Donor/Sponsor
**Scope:** Their donation history

**Functionality:**
- Browse donation campaigns
- Make one-time donation
- Set up recurring donation (monthly, etc.)
- View their donation history
- Download tax receipts
- See impact (their donations helped X animals)
- Cannot see other donors' information
- Cannot see shelter financial details

**Example:** "I want to donate ₹1000 monthly" → Donor selects recurring donation → Pays via Stripe → Each month charged automatically → Receives tax receipt

---

### 5e. External Vet/Partner (Optional)
**Scope:** Limited medical records for assigned animals

**Functionality:**
- View animals assigned to them (if rescue enables)
- Upload medical records (vaccination certificates, lab reports)
- Add medical notes
- Cannot see other animals
- Cannot change rescue settings
- Limited read-only access

**Example:** "Vet clinic needs to update Max's vaccination record" → External Vet logs in → Sees Max → Uploads vaccine certificate → Medical Coordinator receives notification

---

## VISUAL HIERARCHY

```
Super Admin (Platform-wide)
    │
    └── Org Admin (Per Rescue)
            │
            ├── Adoption Coordinator
            ├── Foster Coordinator
            ├── Volunteer Coordinator
            ├── Medical/Vet Coordinator
            ├── Finance/Donor Manager
            │
            ├── Staff (General)
            │
            └── External Users (Public)
                    ├── Adopter
                    ├── Foster
                    ├── Volunteer
                    ├── Donor
                    └── External Vet
```

---

## PERMISSION SUMMARY TABLE

| Role | Create Animals | Approve Applications | Manage Donations | Change Org Settings | Access All Data | External Access |
|------|----------------|----------------------|------------------|---------------------|-----------------|-----------------|
| Super Admin | ✅ All orgs | ✅ All orgs | ✅ All orgs | ✅ Platform-wide | ✅ All orgs | ❌ |
| Org Admin | ✅ Their org | ✅ Their org | ✅ Their org | ✅ Their org | ✅ Their org | ❌ |
| Adoption Coordinator | ✅ | ✅ (Adoption only) | ❌ | ❌ | ✅ (Adoption domain) | ❌ |
| Foster Coordinator | ✅ | ✅ (Foster only) | ❌ | ❌ | ✅ (Foster domain) | ❌ |
| Volunteer Coordinator | ❌ | ✅ (Volunteer only) | ❌ | ❌ | ✅ (Volunteer domain) | ❌ |
| Medical Coordinator | ✅ | ❌ | ❌ | ❌ | ✅ (Medical domain) | ❌ |
| Finance Manager | ❌ | ❌ | ✅ | ❌ | ✅ (Finance domain) | ❌ |
| Staff | ✅ (Limited) | ❌ | ❌ | ❌ | ❌ | ❌ |
| Adopter | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ (Own data) |
| Foster | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ (Own data) |
| Volunteer | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ (Own data) |
| Donor | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ (Own data) |

---

## REAL-WORLD EXAMPLES

**Scenario 1: New Dog Arrives**
1. Staff member creates animal record → "Max, Golden Retriever, arrived today"
2. Medical Coordinator adds vaccination → "Rabies given today"
3. Adoption Coordinator sees Max in system → Marks as "Available for adoption"
4. Max auto-syncs to Petfinder → Public can see him
5. Adopter applies → Adoption Coordinator reviews → Approves → Adoption complete

**Scenario 2: Donation Received**
1. Donor donates ₹5000 on website
2. Finance Manager sees donation → Verifies payment
3. System auto-generates tax receipt
4. Finance Manager emails receipt to donor
5. Donor can log in and see donation in their history

**Scenario 3: Foster Assignment**
1. Foster applies → Foster Coordinator reviews → Approves
2. Foster Coordinator assigns "Bella" (puppy) to Foster
3. Foster logs in → Sees Bella's profile
4. Daily: Foster uploads photos, adds notes "Fed at 8am, playing well"
5. Foster Coordinator monitors updates
6. When Bella is ready for adoption → Foster Coordinator marks "Return to shelter"

---

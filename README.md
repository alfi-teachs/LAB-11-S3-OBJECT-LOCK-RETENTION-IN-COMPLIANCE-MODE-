# LAB-11-S3-OBJECT-LOCK-RETENTION-IN-COMPLIANCE-MODE

https://www.youtube.com/watch?v=NqGb5YraA2Y

## S3 Object Lock (Retention in Compliance Mode)

### What you will learn
- Enable Object Lock in S3  
- Apply default retention  
- Understand Compliance mode (no delete allowed)  

---

### Step 1: Create S3 Bucket
- Go to AWS Console → S3  
- Click **Create bucket**  
- Enter bucket name (unique)  
- **Enable Versioning**
- **Enable Object Lock** (important: can only be enabled during creation)
- Create bucket  

---

### Step 2: Upload Object
- Open your bucket  
- Click **Upload → Add files**  
- Upload any file  
- Click **Upload**

---

### Step 3: Apply Default Retention
- Go to **Properties tab**
- Scroll to **Object Lock**
- Click **Edit**
- Enable:
  - Default retention  
  - Retention mode → **Compliance**
  - Retention period → **1 day**
- Click **Save changes**

---

### Step 4: Upload New Object
- Upload another file (or same file again)

---

### Step 5: Verify Retention
- Click the uploaded object  
- Go to **Properties**
- Scroll to **Object Lock**
- You will see:
  - Retention mode: Compliance  
  - Retain until date  

---

### Step 6: Test Delete
- Try to delete the object  

❌ You **cannot delete** the object  
❌ Even admin/root user cannot delete  
❌ Cannot modify retention  

---

### Important Concept

#### Compliance Mode
- Strongest protection  
- No user can delete object  
- No way to reduce retention period  
- Used for legal / audit requirements  

---

### Key Points
- Object Lock requires **Versioning enabled**
- Must be enabled at **bucket creation time**
- Works only on **new objects after retention is set**

---

### Final Result
- Bucket created with Object Lock  
- Retention policy applied  
- Object protected from deletion  

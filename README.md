# SSRpro Microservices Plan
---

## ✅ **1) API Gateway**

*(There is no controller here. This is just a reverse proxy and routing layer.)*

* All services' APIs will be routed through gateway.
* No controllers defined here.

---

## ✅ **2) Auth & User Service**

**Controllers included:**

* `auth-controller`

  * `/api/auth/signup`
  * `/api/auth/signin`
  * `/api/auth/forgot-password`
  * `/api/auth/update-user/{id}`
  * `/api/auth/update-password`
  * `/api/auth/user/{id}`
  * `/api/auth/isValidUser`
  * `/api/auth/all`

---

## ✅ **3) Master Data Service**

**Controllers included:**

### **Master SSR**

* `master-ssr-controller`

### **Master Chapters**

* `master-chapters-controller`

### **Master Detailed Items**

* `master-detailed-items-controller`

### **Master Materials**

* `master-materials-controller`

### **Master Material Rate (only master side, not txn)**

* `master-materials-rate-controller`

### **Master State**

* `master-state-controller`

### **Master Department**

* `master-department-controller`

### **Master C1 Lead**

* `master-c-1-lead-controller`

### **Master Subscriptions (metadata)**

* `master-subscription-controller`

### **Master Item Classification**

* `master-item-classification-controller`

### **Insurance Rates**

* `master-insurance-rate-controller`

### **Geo Specific Areas**

* `master-geo-specific-areas-controller`

### **Excavation Depth Adjustments**

* `master-excavation-depth-adjustments-controller`

### **Building Floor Adjustments**

* `master-building-floor-adjustments-controller`

### **Master Consumption Material & Road**

* `master-consumption-material-and-road-controller`

### **Construction Testing Master**

* `master-construction-testing-material-controller`

---

## ✅ **4) Payments Service**

**Controllers:**

* `payment-controller`

  * `/api/payments/create`
  * `/api/payments/verify`
* `webhook-controller`

  * `/api/webhooks/razorpay`

---

## ✅ **5) Subscription & Credits Service**

**User Subscription**

* `user-subscription-controller`

**User Payments**

* `user-payment-controller`

  * *Only business side; webhook belongs to Payment Service*

**User Credits**

* `user-total-credits-controller`

**Credit History**

* `credit-history-controller`

**Referral**

* `user-referral-controller`

---

## ✅ **6) File / PDF Service**

**Controllers included:**

* `file-upload-controller`

  * `/api/file/upload`
* `Generic File Upload`

  * `/api/file/upload-all`
* `file-download-controller`

  * `/api/file/download/{fileName}`
* `master-pdf-controller`

  * `/api/Master-pdfs`
* `master-pdf-report-controller`

  * `/api/pdf-report/sync`
* `txn-pdf-generated-controller`

  * `/api/pdf-generated`

---

## ✅ **7) Notification Service**

**Controllers included:**

* `email-notification-controller`
* `contact-form`

  * `/submit` (contact ticket + email)

---

## ✅ **8) Materials / Rates Service + Material Testing & Lab Service**

**Material Rate (Transactional side)**

* `txn-rate-analysis-controller`

**Material Testing**

* `txn-material-testing-controller`

**Material Testing Details**

* `txn-material-testing-detail-controller`

**Master Material Rate (master CRUD → belongs to Master Data)**
*Transactional rate analysis remains here — not master CRUD.*

---

## ✅ **9) Transition Records Service (TXN Domain)**

**All transactional controllers grouped:**

### **Workorder**

* `txn-workorder-controller`

### **Workorder Revision**

* `txn-workorder-revise-controller`

### **Subwork**

* `txn-subwork-controller`

### **Txn Items**

* `txn-items-controller`

### **Txn Item MTS**

* `txn-item-mts-controller`

### **Txn Item Properties**

* `txn-item-properties-controller`

### **Txn Leads**

* `txn-lead-controller`

### **Txn Lead Intrim**

* `txn-item-lead-intrim-controller`

### **Recap**

* `txn-recap-controller`

### **Client Info**

* `txn-client-info-controller`

### **Custom Items**

* `trx-custom-item-controller`

---

## ✅ **10) Auxiliary Services**

**Controllers:**

* `health-controller` (`/api/health`)

*(Future: logging, analytics, metrics, config-server, feature flags, etc.)*

---

# ⭐ **FINAL CLEAN SERVICE-WISE LIST**

---

## **Auth & User Service**

* auth-controller

## **Master Data Service**

* master-ssr-controller
* master-chapters-controller
* master-detailed-items-controller
* master-materials-controller
* master-materials-rate-controller
* master-state-controller
* master-department-controller
* master-c-1-lead-controller
* master-subscription-controller
* master-item-classification-controller
* master-insurance-rate-controller
* master-geo-specific-areas-controller
* master-excavation-depth-adjustments-controller
* master-building-floor-adjustments-controller
* master-consumption-material-and-road-controller
* master-construction-testing-material-controller

## **Payments Service**

* payment-controller
* webhook-controller

## **Subscription & Credits Service**

* user-subscription-controller
* user-payment-controller
* user-total-credits-controller
* credit-history-controller
* user-referral-controller

## **File / PDF Service**

* file-upload-controller
* file-download-controller
* master-pdf-controller
* master-pdf-report-controller
* txn-pdf-generated-controller
* Generic File Upload (`upload-all`)

## **Notification Service**

* email-notification-controller
* contact-form controller

## **Materials / Rates + Material Testing Service**

* txn-rate-analysis-controller
* txn-material-testing-controller
* txn-material-testing-detail-controller

## **Transaction (TXN) Service**

* txn-workorder-controller
* txn-workorder-revise-controller
* txn-subwork-controller
* txn-items-controller
* txn-item-mts-controller
* txn-item-properties-controller
* txn-lead-controller
* txn-item-lead-intrim-controller
* txn-recap-controller
* txn-client-info-controller
* trx-custom-item-controller

## **Auxiliary Service**

* health-controller

---

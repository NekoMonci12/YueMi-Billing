## 🔧 Phase 1: Core Foundations (Laravel Backend)
----------------------------------------

### 1. **Authentication System**
- ✅ **User Registration, Login, Logout** [#01e1153](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/01e115304f06ed33529d84816222fc2dd3b23591)
- ✅ **Role-based access** (Admin, Client) [#125ca7b](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/125ca7bafc6cb71dba819707533544b2e551491d)
- ✅ Use **Laravel Breeze** [#01e1153](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/01e115304f06ed33529d84816222fc2dd3b23591)
- ✅ Add **CSRF, CORS, and password encryption** [#7383b14](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/7383b14285ff477e297ec6e04de66c4600ed80dd)

### 2. **Client Management**
- ✅ Create database tables: `users` [#01e1153](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/01e115304f06ed33529d84816222fc2dd3b23591)
- ✅ Admin can view/add/edit/delete clients [#21d238f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/21d238fad2f4e68c5e3c17d2c2cbe070045842b3)
- ✅ Clients can view and edit their profile [#21d238f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/21d238fad2f4e68c5e3c17d2c2cbe070045842b3)

### 3. **Product & Service Management**
- ✅ Define products (e.g., Shared Hosting, VPS, Domains) [#69ee5ae](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/69ee5ae0e74cff1d40e8be2109041683fe0535dc)
- ✅ Database: `products`, `product_categories`, `services` [#69ee5ae](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/69ee5ae0e74cff1d40e8be2109041683fe0535dc)
- 🟨 Clients can buy/view/manage their services

### 4. **Invoice System (Billing)**
- 🟨 Generate invoices on product/service purchase
- ✅ Database: `invoices`, `invoice_items`, `payments` [#63c8f4f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/63c8f4f82ab28a8a82e5d5121f341861ed16cc66)
- ✅ Support for "Pending", "Paid", "Overdue" statuses [#63c8f4f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/63c8f4f82ab28a8a82e5d5121f341861ed16cc66)

### 5. **Basic UI/UX**
- ✅ Use **Bootstrap** for layout [#21d238f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/21d238fad2f4e68c5e3c17d2c2cbe070045842b3)
- Use **Core UI** for chart
- React for client dashboard interactions (optional at this stage)
- ✅ FontAwesome for icons [#21d238f](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/21d238fad2f4e68c5e3c17d2c2cbe070045842b3)

---

## 🛡️ Phase 2: Security & Reliability
----------------------------------

### 6. **Payment Integration**
- Start with **manual payment confirmation**
- Later integrate **payment gateways** like:
  - Midtrans / Xendit (for Indonesia)
  - Stripe / PayPal (international)

### 7. **Email Notifications**
- On registration, invoice creation, overdue notice, etc.
- Use Laravel's Mail system + Mailtrap for testing

### 8. **Service Provisioning (Manual at first)**
- Admin panel to mark services as active or expired
- Later integrate with APIs (cPanel, Plesk, VPS providers)

### 9. **Clients Inactivity System**
- When Registered set to `Pending`
- If Last Online more than 30d then set to `Inactive`
- After Verifying Emails set to `Active`
- If clients is `Inactive` they must verify their emails again.
---

## 🔁 Phase 3: Automation
--------------------------------

### 10. **Auto-Provisioning**
- Integrate APIs for:
  - Pterodactyl Panel
  - Tripay
  - Midtrans

### 11. **Cron Jobs & Expiry Handling**
- Auto suspend unpaid services
- Send reminders for due invoices
- Auto-renewal logic

## ⚛️ Phase 4: React Native (Frontend)
--------------------------------

### 12. **API System**
- ✅ API Key System [#798b7f6](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/798b7f6ea1fc95d49c732e06c9d3fdac49f3d103)
- ✅ Users Management [#6e982a34](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/6e982a3494106db5ceebab2954e73cd7a9a50636)
- ✅ Product Management [#04cbcac](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/04cbcaccde585a4bd3268dd92e2b7813d8b459e4)
- Invoice Management
  - Payment Gateway
- Service Management
  - Provisioning Hooks

### 13. **Frontend Pages**
- User Dashboard
- Admin Dashboard
- Checkout Pages

### 14. **Performance & Security**
- Cloudflare Turnstile
- CSRF Protection

### 15. **Documentation Sites**
- ✅ Laravel API Docs [#798b7f6](https://github.com/NekoMonci12/YueMi-Billing-Backend/commit/798b7f6ea1fc95d49c732e06c9d3fdac49f3d103)
- Frontend Demo Pictures

## 🎫 Customer Support
--------------------------------

### 16. **Ticket System**
- Laravel System
  - Create/Store/Delete Ticket
  - Encrypt Ticket Data
- React Pages
  - Show Ticket Data
  - Ticket UI

### 17. **AI Customer Service**
- Chat Bubble (Frontend)
  - Call AI on Backend
  - Show Chats

- API Data Access (Backend)
  - Determine which Data to Hooks
  - Generate Answer From Data
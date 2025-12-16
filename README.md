# Konekt  
### *Connect Anywhere. Anytime.*

Konekt is a hybrid messaging app designed to keep people connected even when traditional networks fail. It intelligently switches between **Internet**, **SMS**, and **Bluetooth Mesh** to ensure your messages are delivered — whether you're online, offline, out of data, or completely off the grid.

---

## 🚀 Features

### **1. Smart Messaging Routing**
Konekt automatically chooses the best available method to send your message:
- **Internet** (WiFi/Data) → Primary messaging channel  
- **SMS Fallback** → When internet is weak or unavailable  
- **Bluetooth Mesh** → Offline messaging between nearby devices  

### **2. Offline Bluetooth Mesh Network**
- Send messages without internet or cellular signal  
- Devices relay messages hop‑to‑hop  
- Works seamlessly in crowds, remote areas, and disaster zones  

### **3. End‑to‑End Encryption**
All communication — whether via Internet, SMS, or Bluetooth — is protected with strong encryption.

### **4. Always‑On Reliability**
- Automatic retries  
- Local caching  
- Background message delivery  
- Syncs when connection returns  

### **5. Android‑First Design**
Built to leverage Android’s advanced Bluetooth and background service capabilities for full mesh support.

---

## 📱 How It Works

Konekt uses an intelligent **Transport Router** that selects the best communication method:

```kotlin
if (internet_available) 
    use InternetService()
else if (sms_enabled && carrier_signal_available)
    use SmsFallback()
else
    use BluetoothMesh()

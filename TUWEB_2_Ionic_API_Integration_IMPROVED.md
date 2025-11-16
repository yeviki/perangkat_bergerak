# TUWEB 2: Integrasi Ionic Framework dengan API Eksternal

**Mata Kuliah:** Pemrograman Berbasis Perangkat Bergerak (MSIM4401)  
**Dosen:** Yeviki Maisyah Putra, S.Kom, M.Kom.  
**Universitas:** Universitas Putra Indonesia YPTK Padang - Universitas Terbuka  
**Durasi:** 120 menit (2 jam)

---

## 🎯 Tujuan Pembelajaran

Assalamualaikum, wr, wb, Semoga Kita Sehat Selalu, berikut adalah materi mandiri tentang Integrasi Ionic Framework dengan API Eksternal, selamat mengerjakan... ^_^
Setelah mengikuti sesi ini, mahasiswa diharapkan mampu:

### 📋 Level Pemahaman (Bloom's Taxonomy)

#### 🔵 **C1 - Mengingat (Remember)**
- Menyebutkan komponen utama Ionic Framework
- Mengidentifikasi HTTP methods untuk API
- Menjelaskan konsep async/await

#### 🔵 **C2 - Memahami (Understand)**  
- Menjelaskan arsitektur Ionic untuk hybrid apps
- Memahami flow RESTful API communication
- Mengartikan JSON data structure

#### 🔵 **C3 - Menerapkan (Apply)**
- Membuat project Ionic dengan Vue.js
- Mengintegrasikan external API ke aplikasi
- Membuat responsive mobile UI dengan Ionic components

---

## 🕐 Timeline Sesi

| Waktu | Aktivitas | Metode |
|-------|-----------|--------|
| 00:00-10:00 | **Pendahuluan & Demo App** | Live Demo |
| 10:00-25:00 | **Teori Ionic Framework** | Ceramah + Visual |
| 25:00-45:00 | **Setup Project Ionic** | Hands-on |
| 45:00-60:00 | **Teori RESTful API** | Ceramah + Diagram |
| 60:00-85:00 | **Praktikum API Integration** | Guided Practice |
| 85:00-105:00 | **Build Weather App** | Hands-on |
| 105:00-115:00 | **Testing & Debugging** | Practice |
| 115:00-120:00 | **Q&A & Next Steps** | Diskusi |

---

## 📚 Materi 1: Pengenalan Ionic Framework

### 1.1 Apa itu Ionic Framework? (Visual Understanding)

#### 🎯 **Konsep Visual**
Ionic adalah **framework untuk membuat aplikasi mobile hybrid**. Bayangkan:

```
📱 Aplikasi Native          🌐 Aplikasi Web              📱 Aplikasi Ionic
├── iOS Native Code        ├── HTML/CSS/JS              ├── HTML/CSS/JS
├── Android Native Code    ├── Browser Engine          ├── WebView Wrapper
├── Device APIs            ├── Limited Device Access   ├── Native Bridge
└── Platform Specific     └── Cross Platform          └── Cross Platform
```

#### 📊 **Perbandingan Platform Development**

| Aspek | Native iOS | Native Android | Ionic Hybrid |
|-------|------------|---------------|--------------|
| **Language** | Swift/Objective-C | Kotlin/Java | TypeScript/JS |
| **Code Base** | Terpisah | Terpisah | Satu codebase |
| **Development Cost** | Tinggi | Tinggi | Sedang |
| **Performance** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Development Speed** | Lambat | Lambat | Cepat |
| **UI Consistency** | Perfect | Perfect | Very Good |

#### 🏗️ **Arsitektur Ionic Framework**

```
┌─────────────────────────────────────────────────────────────┐
│                    📱 Aplikasi Anda                        │
│  ┌─────────────────────────────────────────────────────┐   │
│  │              Vue.js Components                       │   │
│  │  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐ │   │
│  │  │   Weather   │  │    Profile  │  │   Settings  │ │   │
│  │  │  Component  │  │ Component   │  │ Component   │ │   │
│  │  └─────────────┘  └─────────────┘  └─────────────┘ │   │
│  └─────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────┤
│                 🎨 Ionic UI Components                    │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐       │
│  │ IonHeader   │  │ IonCard     │  │ IonButton   │       │
│  │ IonToolbar  │  │ IonList     │  │ IonInput    │       │
│  │ IonContent  │  │ IonItem     │  │ IonIcon     │       │
│  └─────────────┘  └─────────────┘  └─────────────┘       │
├─────────────────────────────────────────────────────────────┤
│                🔌 Capacitor/Cordova Bridge                  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐       │
│  │   Camera    │  │  GPS/Location│  │  Push Notif │       │
│  │   Storage   │  │  Bluetooth   │  │  Biometrics │       │
│  │   Network   │  │   File Sys   │  │   Sensors   │       │
│  └─────────────┘  └─────────────┘  └─────────────┘       │
├─────────────────────────────────────────────────────────────┤
│                📱 Native Platform                          │
│  ┌─────────────────┐              ┌─────────────────┐     │
│  │   iOS Device    │              │ Android Device  │     │
│  │   (Swift/ObjC)  │              │ (Java/Kotlin)   │     │
│  └─────────────────┘              └─────────────────┘     │
└─────────────────────────────────────────────────────────────┘
```

### 1.2 Keunggulan Ionic Framework

#### 🚀 **Development Advantages**

1. **🔄 Single Codebase**
   ```
   Tulis sekali → Jalankan di mana saja
   ├── iOS App
   ├── Android App  
   └── Web App (PWA)
   ```

2. **🎨 Rich UI Components**
   - 100+ pre-built components
   - Native look & feel
   - Customizable themes

3. **⚡ Modern Development**
   - TypeScript support
   - Hot reload development
   - Rich debugging tools

4. **🔌 Native Access**
   - Camera, GPS, Storage
   - Push notifications
   - Biometric authentication

#### 💼 **Business Benefits**

| Benefit | Explanation | Impact |
|---------|-------------|--------|
| **Cost Reduction** | One team, multiple platforms | 💰 50-70% cost saving |
| **Faster Time-to-Market** | Rapid development cycle | ⚡ 2-3x faster |
| **Easier Maintenance** | Single codebase | 🔧 Simplified updates |
| **Wider Reach** | iOS + Android + Web | 🌍 More users |

### 1.3 Setup Environment Ionic (Step-by-Step Visual)

#### 🛠️ **Prerequisites Checklist**

```
✅ Node.js (v18+)
✅ npm atau yarn
✅ Git untuk version control
✅ Code Editor (VS Code recommended)
✅ Smartphone/Emulator untuk testing
```

#### 📱 **Step 1: Install Ionic CLI**

```bash
# Buka terminal/command prompt
# Install Ionic CLI globally
npm install -g @ionic/cli

# Verifikasi instalasi
ionic --version

# Expected output: Ionic CLI v7.x.x
```

**💡 Pro Tip:** Jika error, coba run as administrator (Windows) atau gunakan sudo (Mac/Linux).

#### 🏗️ **Step 2: Create New Ionic Project**

```bash
# Buat folder untuk project
mkdir ionic-weather-app
cd ionic-weather-app

# Create new project dengan Vue.js
ionic start . tabs --type=vue

# atau
ionic start . tabs

# Atau jika file folder belum di create seperti ini
ionic start ionic-weather-app tabs

# Pilihan yang akan muncul:
# ? Framework: Vue
# ? Starter template: Tabs (recommended for beginners)

# atau seperti dibawah ini, tidak perlu memilik framework vue karena sudah ditentukan
ionic start ionic-weather-app tabs --type vue
```

**📊 Project Structure yang akan dibuat:**

```
ionic-weather-app/
├── src/
│   ├── components/          # Reusable components
│   ├── views/              # Page components
│   │   ├── Tab1Page.vue   # Home tab
│   │   ├── Tab2Page.vue   # Weather tab  
│   │   └── Tab3Page.vue   # Settings tab
│   ├── router/             # Vue Router configuration
│   ├── theme/              # Styling dan themes
│   └── App.vue             # Main app component
├── public/                 # Static assets
├── capacitor.config.ts     # Native platform config
├── ionic.config.json      # Ionic configuration
└── package.json           # Dependencies
```

#### 🚀 **Step 3: Run Development Server**

```bash
# Install dependencies
npm install

# Run development server
ionic serve

# Atau
npm run dev
```

**🌐 What happens next:**
1. Browser akan otomatis membuka `http://localhost:8100`
2. Anda akan melihat aplikasi Ionic dengan 3 tabs
3. Hot reload aktif - perubahan akan langsung terlihat

#### 📱 **Step 4: Test on Mobile Device**

```bash
# Install Ionic DevApp (optional)
npm install -g @ionic/cli

# Run on device/emulator
ionic cap run android    # Untuk Android
ionic cap run ios        # Untuk iOS (Mac only)
```

---

## 📚 Materi 2: RESTful API Fundamentals

### 2.1 Apa itu RESTful API? (Konsep Visual)

#### 🌐 **API Communication Flow**

```
📱 Mobile App                    🌐 Server
├── Request → ──────────────────→ │
│   HTTP Method                  │
│   GET /weather                 │
│   Headers: {                  │
│     "Content-Type": "application/json" │
│   }                           │
│                                │
├── ← ────────────────── Response │
│   Status Code: 200 OK         │
│   Body: {                     │
│     "temperature": 28,         │
│     "humidity": 75            │
│   }                           │
└────────────────────────────────┘
```

#### 📋 **HTTP Methods Cheat Sheet**

| Method | Purpose | Example | Status Code |
|--------|---------|---------|-------------|
| **GET** | Retrieve data | `GET /weather` | 200 OK |
| **POST** | Create data | `POST /users` | 201 Created |
| **PUT** | Update entire data | `PUT /users/1` | 200 OK |
| **PATCH** | Update partial data | `PATCH /users/1` | 200 OK |
| **DELETE** | Delete data | `DELETE /users/1` | 204 No Content |

#### 📊 **HTTP Status Codes**

```
✅ 2xx Success
   200 OK - Request successful
   201 Created - Resource created
   204 No Content - Success but no content

⚠️ 4xx Client Error  
   400 Bad Request - Invalid request
   401 Unauthorized - Authentication required
   403 Forbidden - No permission
   404 Not Found - Resource not found

❌ 5xx Server Error
   500 Internal Server Error - Server problem
   502 Bad Gateway - Gateway issue
   503 Service Unavailable - Server down
```

### 2.2 JSON Data Structure (Visual Examples)

#### 📋 **Basic JSON Structure**

```json
{
  "status": "success",
  "data": {
    "location": {
      "name": "Jakarta",
      "country": "Indonesia",
      "coordinates": {
        "latitude": -6.2088,
        "longitude": 106.8456
      }
    },
    "current_weather": {
      "temperature": 28.5,
      "humidity": 75,
      "wind_speed": 15.2,
      "description": "Partly cloudy",
      "icon": "partly-cloudy"
    },
    "forecast": [
      {
        "date": "2024-01-15",
        "max_temp": 32,
        "min_temp": 24,
        "condition": "sunny"
      },
      {
        "date": "2024-01-16", 
        "max_temp": 30,
        "min_temp": 23,
        "condition": "rainy"
      }
    ]
  },
  "timestamp": "2024-01-15T10:30:00Z"
}
```

#### 🔍 **JSON Parsing di TypeScript**

```typescript
// Interface untuk type safety
interface WeatherData {
  status: string;
  data: {
    location: {
      name: string;
      country: string;
      coordinates: {
        latitude: number;
        longitude: number;
      };
    };
    current_weather: {
      temperature: number;
      humidity: number;
      wind_speed: number;
      description: string;
      icon: string;
    };
    forecast: Array<{
      date: string;
      max_temp: number;
      min_temp: number;
      condition: string;
    }>;
  };
  timestamp: string;
}

// Parsing JSON response
async function parseWeatherResponse(responseText: string): Promise<WeatherData> {
  try {
    const data: WeatherData = JSON.parse(responseText);
    return data;
  } catch (error) {
    throw new Error('Invalid JSON format');
  }
}
```

### 2.3 Async/Await Pattern (Step-by-Step)

#### ⚡ **Synchronous vs Asynchronous**

```
🔄 Synchronous (Blocking)
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ Step 1      │ │ Step 2      │ │ Step 3      │
│ (2 seconds) │ │ (3 seconds) │ │ (1 second)  │
└─────────────┘ └─────────────┘ └─────────────┘
Total: 6 seconds (blocking)

⚡ Asynchronous (Non-blocking)  
┌─────────────┐
│ Step 1      │
│ (2 seconds) │
└─────────────┘
┌─────────────┐
│ Step 2      │
│ (3 seconds) │
└─────────────┘
┌─────────────┐
│ Step 3      │
│ (1 second)  │
└─────────────┘
Total: ~3 seconds (parallel)
```

#### 🧩 **Async/Await Syntax**

```typescript
// ❌ Callback Hell (Old way)
function getData(callback: (data: any) => void) {
  fetch('/api/weather')
    .then(response => response.json())
    .then(data => callback(data))
    .catch(error => console.error(error));
}

// ✅ Async/Await (Modern way)
async function getWeatherData(): Promise<any> {
  try {
    const response = await fetch('/api/weather');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error fetching weather:', error);
    throw error;
  }
}

// 🎯 Using the async function
async function main() {
  try {
    const weather = await getWeatherData();
    console.log('Weather data:', weather);
  } catch (error) {
    console.error('Failed to get weather:', error);
  }
}
```

---

## 🛠️ Praktikum 1: Setup Ionic Weather Project

### 🎯 **Tujuan Praktikum**
Membuat project Ionic Vue.js untuk aplikasi cuaca dengan integrasi API.

### 📋 **Project Requirements**
- ✅ Ionic Framework dengan Vue.js
- ✅ TypeScript untuk type safety
- ✅ Open-Meteo Weather API integration
- ✅ Responsive mobile UI
- ✅ Error handling dan loading states

### 🏗️ **Step 1: Create Project**

```bash
# Create new project
ionic start weather-app tabs --type vue

# Navigate to project
cd weather-app

# Install additional dependencies
npm install axios

# Install Ionic icons
npm install ionicons
```

### 📁 **Step 2: Project Structure Setup**

```
weather-app/
├── src/
│   ├── components/          # Reusable components
│   │   ├── DailyForecast.vue
│   │   ├── HourlyForecast.vue
│   │   └── ErrorMessage.vue
│   │   └── LoadingSpinner.vue
│   │   └── WeatherCard.vue
│   │   └── WeatherChart.vue (Optional)
│   ├── views/              # Page components
│   │   ├── Tab1Page.vue    # → WeatherPage.vue
│   │   ├── Tab2Page.vue    
│   │   └── Tab3Page.vue    

```

### 📝 **Step 3: Create DailyForecast.vue**

```typescript
// src/components/DailyForecast.vue

<template>
  <ion-accordion-group>
    <ion-accordion v-for="(d, i) in data" :key="i">
      <ion-item slot="header">
        <ion-label>{{ d.date }} — rata-rata: {{ d.avg }}°C</ion-label>
      </ion-item>

      <div class="ion-padding" slot="content">
        Cuaca rata-rata hari ini adalah {{ d.avg }}°C
      </div>
    </ion-accordion>
  </ion-accordion-group>
</template>

<script setup>
import { IonAccordion, IonAccordionGroup, IonItem, IonLabel } from "@ionic/vue";
defineProps({ data: Array });
</script>

```

### 🔧 **Step 4: Create HourlyForecast.vue**

```typescript
// src/components/HourlyForecast.vue

<template>
  <ion-list>
    <ion-item v-for="(h, i) in data" :key="i">
      <ion-label>
        <h2>{{ h.time }}</h2>
        <p>{{ h.temp }} °C</p>
      </ion-label>
    </ion-item>
  </ion-list>
</template>

<script setup>
import { IonList, IonItem, IonLabel } from "@ionic/vue";
defineProps({ data: Array });
</script>

```

### 🔧 **Step 5: Create ErrorMessage.vue**

```typescript
// src/components/ErrorMessage.vue

<template>
  <ion-card color="danger">
    <ion-card-content>{{ message }}</ion-card-content>
  </ion-card>
</template>

<script setup>
import { IonCard, IonCardContent } from "@ionic/vue";
defineProps({ message: String });
</script>


```

### 🔧 **Step 6: Create LoadingSpinner.vue**

```typescript
// src/components/LoadingSpinner.vue

<template>
  <div class="center">
    <ion-spinner name="crescent"></ion-spinner>
    <p>Loading data...</p>
  </div>
</template>

<script setup>
import { IonSpinner } from "@ionic/vue";
</script>

<style scoped>
.center {
  text-align: center;
  margin-top: 30px;
}
</style>

```

### 🔧 **Step 7: Create WeatherCard.vue**

```typescript
// src/components/WeatherCard.vue

<template>
  <ion-card>
    <ion-card-header>
      <ion-card-title>{{ icon }} {{ temperature }}°C</ion-card-title>
      <ion-card-subtitle>Jakarta Hari Ini</ion-card-subtitle>
    </ion-card-header>
  </ion-card>
</template>

<script setup>
import { IonCard, IonCardHeader, IonCardTitle, IonCardSubtitle } from "@ionic/vue";
defineProps({
  temperature: Number,
  icon: String
});
</script>

```

### 🔧 **Step 8: Create WeatherChart.vue (Optional)**

```typescript
// src/components/WeatherChart.vue

<template>
  <ion-card>
    <ion-card-header>
      <ion-card-title>Grafik Suhu (24 Jam)</ion-card-title>
    </ion-card-header>

    <ion-card-content>
      <Line :data="chartData" :options="chartOptions" />
    </ion-card-content>
  </ion-card>
</template>

<script setup>
import { Line } from 'vue-chartjs'
import {
  Chart,
  LineElement,
  PointElement,
  LinearScale,
  CategoryScale,
  Filler,
  Tooltip,
  Legend
} from 'chart.js'

Chart.register(LineElement, PointElement, LinearScale, CategoryScale, Filler, Tooltip, Legend)

const props = defineProps({
  labels: Array,
  temps: Array
})

const chartData = {
  labels: props.labels,
  datasets: [
    {
      label: "Suhu",
      data: props.temps,
      fill: true,
      borderColor: "#3880ff",
      backgroundColor: "rgba(56,128,255,0.2)",
      tension: 0.3
    }
  ]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false
}
</script>

<style scoped>
ion-card { height: 1000px; }

.chart-container { height: 220px; }
</style>


```

### 🔧 **Step 9: Create Tab1Page.vue**

```typescript
// src/views/Tab1Page.vue

<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Cuaca Jakarta</ion-title>
        <ion-buttons slot="end">
          <ion-button @click="fetchWeather" :disabled="loading">
            <ion-icon :icon="refreshOutline" />
          </ion-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>

    <ion-content>

      <!-- Loading -->
      <LoadingSpinner v-if="loading" />

      <!-- Error -->
      <ErrorMessage v-if="error" :message="error" />

      <!-- Weather Summary -->
      <WeatherCard
        v-if="todayTemp"
        :temperature="todayTemp"
        :icon="weatherIcon"
      />

      <!-- Chart Suhu -->
      <WeatherChart
        v-if="hourly.length"
        :labels="hourly.map(h => h.time.split('T')[1])"
        :temps="hourly.map(h => h.temp)"
      />

      <!-- Segment -->
      <ion-segment v-model="segment">
        <ion-segment-button value="hourly">
          <ion-label>Hourly</ion-label>
        </ion-segment-button>

        <ion-segment-button value="daily">
          <ion-label>Daily</ion-label>
        </ion-segment-button>
      </ion-segment>

      <!-- Hourly Forecast -->
      <HourlyForecast
        v-if="segment === 'hourly'"
        :data="hourly"
      />

      <!-- Daily Forecast -->
      <DailyForecast
        v-if="segment === 'daily'"
        :data="daily"
      />

    </ion-content>
  </ion-page>
</template>

<script setup>
import { ref, onMounted } from "vue";
import axios from "axios";
import {
  IonPage, IonHeader, IonToolbar, IonTitle,
  IonContent, IonSegment, IonSegmentButton, IonLabel,
  IonButtons, IonButton, IonIcon
} from "@ionic/vue";
import { refreshOutline } from "ionicons/icons";

import LoadingSpinner from "@/components/LoadingSpinner.vue";
import ErrorMessage from "@/components/ErrorMessage.vue";
import WeatherCard from "@/components/WeatherCard.vue";
import HourlyForecast from "@/components/HourlyForecast.vue";
import DailyForecast from "@/components/DailyForecast.vue";
import WeatherChart from "@/components/WeatherChart.vue";


// state
const loading = ref(false);
const error = ref("");
const segment = ref("hourly");
const hourly = ref([]);
const daily = ref([]);
const todayTemp = ref(null);
const weatherIcon = ref("🌤️"); // default

// ambil data cuaca
async function fetchWeather() {
  loading.value = true;
  error.value = "";

  try {
    const url =
      "https://api.open-meteo.com/v1/forecast?latitude=-6.2&longitude=106.8&hourly=temperature_2m";

    const res = await axios.get(url);
    const t = res.data.hourly.temperature_2m;
    const times = res.data.hourly.time;

    // bentuk hourly list
    hourly.value = times.map((time, i) => ({
      time,
      temp: t[i]
    }));

    // ringkasan hari ini
    todayTemp.value = t[0];

    // icon simple
    if (todayTemp.value < 23) weatherIcon.value = "🌧️";
    else if (todayTemp.value < 28) weatherIcon.value = "⛅";
    else weatherIcon.value = "☀️";

    // bentuk daily data (group by date)
    const group = {};
    hourly.value.forEach((h) => {
      const date = h.time.split("T")[0];
      if (!group[date]) group[date] = [];
      group[date].push(h.temp);
    });

    daily.value = Object.keys(group).map((d) => ({
      date: d,
      avg: (group[d].reduce((a, b) => a + b, 0) / group[d].length).toFixed(1)
    }));

  } catch (err) {
    error.value = "Gagal memuat data cuaca!";
  } finally {
    loading.value = false;
  }
}

onMounted(fetchWeather);
</script>

<style scoped>
ion-segment {
  margin: 20px;
}
</style>

```

### 🔧 **Step 10: main.ts**

```dash
import { createApp } from 'vue'
import App from './App.vue'
import router from './router';

import { IonicVue } from '@ionic/vue';

/* Core CSS required for Ionic components to work properly */
import '@ionic/vue/css/core.css';

/* Basic CSS for apps built with Ionic */
import '@ionic/vue/css/normalize.css';
import '@ionic/vue/css/structure.css';
import '@ionic/vue/css/typography.css';

/* Optional CSS utils that can be commented out */
import '@ionic/vue/css/padding.css';
import '@ionic/vue/css/float-elements.css';
import '@ionic/vue/css/text-alignment.css';
import '@ionic/vue/css/text-transformation.css';
import '@ionic/vue/css/flex-utils.css';
import '@ionic/vue/css/display.css';

/**
 * Ionic Dark Mode
 * -----------------------------------------------------
 * For more info, please see:
 * https://ionicframework.com/docs/theming/dark-mode
 */

/* @import '@ionic/vue/css/palettes/dark.always.css'; */
/* @import '@ionic/vue/css/palettes/dark.class.css'; */
import '@ionic/vue/css/palettes/dark.system.css';

/* Theme variables */
import './theme/variables.css';

const app = createApp(App)
  .use(IonicVue)
  .use(router);

router.isReady().then(() => {
  app.mount('#app');
});

```

---

## 🎯 Latihan Mandiri (Progressive Difficulty)

### 📈 **Level 1: Basic Enhancement**

#### **Latihan 1.1: Add Search History**
Implementasikan fitur search history:
1. **Save searched cities** ke localStorage
2. **Display recent searches** dalam dropdown
3. **Quick access** untuk kota-kota favorit

#### **Latihan 1.2: Weather Animations**
Tambahkan animasi untuk weather conditions:
1. **Animated icons** untuk cuaca berbeda
2. **Background gradients** berdasarkan kondisi
3. **Transition effects** saat data berubah

### 📈 **Level 2: Intermediate Features**

#### **Latihan 2.1: Multiple Locations**
Buat sistem multi-location:
1. **Add multiple cities** ke dashboard
2. **Swipe between locations**
3. **Compare weather** antar kota

#### **Latihan 2.2: Advanced Weather Data**
Integrasikan additional weather data:
1. **Air quality index**
2. **Pollen count**
3. **Weather alerts dan warnings**

### 📈 **Level 3: Advanced Integration**

#### **Latihan 3.1: Offline Mode**
Implementasikan offline functionality:
1. **Cache weather data** untuk offline access
2. **Sync when online** kembali
3. **Offline indicators** di UI

#### **Latihan 3.2: Push Notifications**
Setup weather notifications:
1. **Daily weather summary**
2. **Severe weather alerts**
3. **Custom notification preferences**

---

## 📝 Evaluasi & Assessment

### 🎯 **Quick Quiz (10 menit)**

#### **Soal Pilihan Ganda**

1. **Apa keunggulan utama Ionic Framework?**
   - A) Native performance only
   - B) Cross-platform development dengan web technologies
   - C) Machine learning integration
   - D) Blockchain support

2. **HTTP method yang tepat untuk mengambil data cuaca:**
   - A) POST
   - B) PUT
   - C) GET
   - D) DELETE

3. **Apa fungsi utama dari async/await?**
   - A) Membuat kode synchronous
   - B) Handle asynchronous operations lebih readable
   - C) Optimize memory usage
   - D) Improve network speed

4. **Component Ionic untuk menampilkan list:**
   - A) IonGrid
   - B) IonList
   - C) IonCard
   - D) IonButton

5. **Status code untuk successful API request:**
   - A) 404
   - B) 500
   - C) 200
   - D) 301

#### **Jawaban:**
1. B, 2. C, 3. B, 4. B, 5. C

### 📊 **Rubrik Penilaian Praktikum**

| Kriteria | Sangat Baik (4) | Baik (3) | Cukup (2) | Kurang (1) |
|----------|-----------------|----------|-----------|------------|
| **API Integration** | ✅ Error handling complete | ✅ Basic integration | ⚠️ Limited functionality | ❌ Not working |
| **UI Components** | ✅ Rich & interactive | ✅ Good design | ⚠️ Basic UI | ❌ Poor UX |
| **Code Quality** | ✅ Clean & modular | ✅ Well structured | ⚠️ Needs refactoring | ❌ Messy code |
| **Features** | ✅ Extra features | ✅ All requirements | ⚠️ Missing some | ❌ Incomplete |
| **Responsive Design** | ✅ Perfect on all sizes | ✅ Good responsive | ⚠️ Some issues | ❌ Not responsive |

---

## 🔗 Resources Tambahan

### 📚 **Documentation & Learning**

#### **Official Documentation**
- [Ionic Documentation](https://ionicframework.com/docs) - Panduan lengkap Ionic
- [Capacitor Documentation](https://capacitorjs.com/docs) - Native bridge
- [Vue.js Documentation](https://vuejs.org/guide/) - Vue.js guide
- [REST API Design Guide](https://restfulapi.net/) - API design principles

#### **API Documentation**
- [Open-Meteo API](https://open-meteo.com/) - Free weather API
- [Nominatim API](https://nominatim.org/) - Geocoding service
- [Axios Documentation](https://axios-http.com/) - HTTP client library

### 🛠️ **Development Tools**

#### **Browser DevTools**
- **Vue DevTools** - Debug Vue applications
- **Network Tab** - Monitor API requests
- **Console** - Debug JavaScript errors
- **Application Tab** - Inspect localStorage

#### **Mobile Testing**
- **Ionic DevApp** - Test on real device
- **BrowserStack** - Cross-browser testing
- **Android Studio Emulator** - Android testing
- **Xcode Simulator** - iOS testing (Mac only)

### 🎮 **Practice Platforms**

#### **API Practice**
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) - Fake API for testing
- [Reqres.in](https://reqres.in/) - API for testing
- [Public APIs](https://github.com/public-apis/public-apis) - Collection of free APIs

#### **Ionic Examples**
- [Ionic Examples](https://ionicframework.com/examples/) - Official examples
- [CodePen Ionic](https://codepen.io/tag/ionic/) - Community examples
- [GitHub Ionic Projects](https://github.com/topics/ionic) - Open source projects

---

## 💡 Tips & Best Practices

### 🎯 **Untuk Mahasiswa Pemula**

#### **Learning Strategy**
1. **Start with UI** - Build interface first
2. **Add data later** - Integrate API after UI works
3. **Test frequently** - Run app after each change
4. **Use console.log** - Debug with logging
5. **Read documentation** - Check official docs first

#### **Common Mistakes to Avoid**
1. **Ignoring CORS issues** - API calls might fail
2. **Not handling errors** - Always catch API errors
3. **Blocking main thread** - Use async/await properly
4. **Forgetting responsive design** - Test on different screen sizes
5. **Not using TypeScript** - Lose type safety benefits

### 🚀 **Ionic Development Tips**

#### **Performance Optimization**
1. **Lazy load components** - Reduce initial bundle size
2. **Use virtual scrolling** - For long lists
3. **Optimize images** - Compress and resize
4. **Cache API responses** - Reduce network calls
5. **Use web workers** - For heavy computations

#### **UI/UX Best Practices**
1. **Follow platform guidelines** - iOS HIG, Android Material
2. **Use consistent spacing** - Follow Ionic design tokens
3. **Add loading states** - Improve perceived performance
4. **Handle edge cases** - No network, empty states
5. **Test on real devices** - Emulators aren't enough

---

## 🎉 Penutup Sesi

### 🏆 **Achievement Unlocked!**

Selamat! Anda telah menyelesaikan TUWEB 2 dan telah berhasil:

- ✅ **Membuat aplikasi Ionic** dengan Vue.js dan TypeScript
- ✅ **Mengintegrasikan RESTful API** untuk data cuaca real-time
- ✅ **Membangun responsive mobile UI** dengan Ionic components
- ✅ **Implementasikan best practices** untuk error handling dan loading states

### 🎯 **Key Takeaways**

1. **Ionic = Cross-Platform Power** - Satu kode untuk multiple platform
2. **API Integration = Real Data** - Connect apps to real-world services
3. **Async/Await = Modern JavaScript** - Handle async operations elegantly
4. **Component-Based = Modular Development** - Build reusable UI pieces

### 🚀 **Next Steps**

1. **Complete latihan mandiri** untuk reinforcement
2. **Explore additional Ionic components** (maps, charts, etc.)
3. **Prepare for TUWEB 3** - Advanced features dan deployment
4. **Start thinking about final project** yang menggabungkan semua materi
5. **Join Ionic communities** untuk support dan inspiration

### 📞 **Support & Contact**

**Jika ada pertanyaan:**
- **Email:** yeviki.maisyahputra@gmail.com / yeviki.maisyahputra@upiyptk.ac.id
- **WhatsApp Group:** [Link akan dibagikan]

**Remember:** "The best way to learn is by building. Keep creating, keep learning! 🚀"

---

**See you in TUWEB 3: Advanced Features & Deployment! 🌟**

---

*Dicetak oleh: Yeviki Maisyah Putra, S.Kom, M.Kom.*  
*Universitas Putra Indonesia YPTK Padang - Program Studi Sistem Informasi*  
*Universitas Terbuka - Pusat Belajar Jarak Jauh*  
*Tanggal: 30 Oktober 2025*

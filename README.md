# ARR Suite - The Absolute Best Configuration (Radarr & Sonarr)
## The Ultimate GOD SETUP by Roger para que las descargas estén es español de españa, priorice los codecs mas eficientes y rechace opciones menos interesantes.
![image](https://github.com/user-attachments/assets/4f91da37-679c-4989-a446-12f7b2fe1f74)

### ⚙️ Settings/IU 
**La interfaz tiene estar en ingés**, pero puedes opcionalmente (ya que es personal, pero no necesario) ajustar toda la configuración de UI como la imagen. 
**Tienes que habilitar Show Advanced (el engranaje en la parte superior)** para mostrar los ajustes avanzados.
![image](https://github.com/user-attachments/assets/757d9a65-f8fa-4ede-8524-838971bede2c)

### 🎯 Settings/Custom Formats
Así se importan los Custom Formats en formato json (en Sonarr es igual), si tienen ya Custom Formats construidos puedes borrarlos todos y ponerlos:
![Radarr Custom Formats Import](https://github.com/user-attachments/assets/f4b98753-e5a7-47dd-a310-0c4c1ef0e7ac)

#### 📌 420p
```json
{
  "name": "420p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "420p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 480
      }
    }
  ]
}
```

#### 📌 720p
```json
{
  "name": "720p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "720p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 720
      }
    }
  ]
}
```

#### 📌 1080p
```json
{
  "name": "1080p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "1080p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 1080
      }
    }
  ]
}
```

#### 📌 2160p
```json
{
  "name": "2160p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "2160p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 2160
      }
    }
  ]
}
```

#### 📌 Multi (Spanish)
```json
{
  "name": "Multi (Spanish)",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Spanish Language",
      "implementation": "LanguageSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": false
      }
    },
    {
      "name": "Multi-Language",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": "(?i)(multi-language|multi|lang)"
      }
    }
  ]
}
```

#### 📌 Only Spanish
```json
{
  "name": "Only Spanish",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Spanish Only",
      "implementation": "LanguageSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": false
      }
    },
    {
      "name": "Exclude Multi-Language",
      "implementation": "LanguageSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": true
      }
    }
  ]
}
```

#### 📌 Spanish (Latino) Reject
```json
{
  "name": "Spanish (Latino) Reject",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Latino/Mexican Spanish",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": false,
      "fields": {
        "value": "(?i)(latino|mexican|mex|arg|argentina|colombia|andes)"
      }
    }
  ]
}
```

#### 📌 x264
```json
{
  "name": "x264",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "x264/H264/AVC",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": false,
      "fields": {
        "value": "(?i)(x264|h264|avc)"
      }
    }
  ]
}
```

#### 📌 x265
```json
{
  "name": "x265",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "x265/H265/HEVC",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": false,
      "fields": {
        "value": "(?i)(x265|h265|hevc)"
      }
    }
  ]
}
```

---

### ⚙️ Settings/Quality
![image](https://github.com/user-attachments/assets/ab041763-906f-43df-b8ed-a5d2c0a68c09)

---
### ⚙️ Settings/Profiles
En este caso te recomiendo borrar las preset que tienes para comenzar de 0, hacer la primera preset completa y luego copiarla y editarle los valores como las imágenes , para de ese modo no tener que reorganizar los grupos por cada preset.

https://github.com/user-attachments/assets/345aad1e-410c-4d3b-98b7-fab7b9cea320

#### 📌 Full HD-1080p
![image](https://github.com/user-attachments/assets/b03dae65-e384-4f88-ae61-09f5dc593f4a)

#### 📌 HD-720p
![image](https://github.com/user-attachments/assets/f8a5dd17-48fd-4a8f-bae8-26620f6d05e5)

#### 📌 Ultra-HD
![image](https://github.com/user-attachments/assets/4acd5c95-a136-4199-91e5-6567a012a99c)

------
Ahora vamos a configurar a Sonarr, iré más al grano ya que hay que hacerle lo mismo que hicimos a Radarr: 

![image](https://github.com/user-attachments/assets/e137f1a5-7dd5-4622-b38a-a3921bf02cad)


### ⚙️ Settings/IU 
![image](https://github.com/user-attachments/assets/7b551afa-2f79-4387-a635-9696d65e4830)

### 🎯 Settings/Custom Formats

#### 📌 420p
```json
{
  "name": "420p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "420p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 480
      }
    }
  ]
}
```

#### 📌 720p
```json
{
  "name": "720p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "720p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 720
      }
    }
  ]
}
```

#### 📌 1080p
```json
{
  "name": "1080p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "1080p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 1080
      }
    }
  ]
}
```

#### 📌 2160p
```json
{
  "name": "2160p",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "2160p",
      "implementation": "ResolutionSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 2160
      }
    }
  ]
}
```

#### 📌 Multi (Spanish)
```json
{
  "name": "Multi (Spanish)",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Multi-Languages Required",
      "implementation": "LanguageSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": true
      }
    },
    {
      "name": "Spanish Required in Multi-Languages",
      "implementation": "LanguageSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": false
      }
    }
  ]
}
```

#### 📌 Only Spanish
```json
{
  "name": "Only Spanish",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Spanish Only",
      "implementation": "LanguageSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": false
      }
    },
    {
      "name": "Exclude Multi-Languages",
      "implementation": "LanguageSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": 3,
        "exceptLanguage": true
      }
    }
  ]
}
```

#### 📌 Spanish (Latino) Reject
```json
{
  "name": "Spanish (Latino) Reject",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "Latino/Mexican Spanish",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": "(?i)\\b(latino|mexican|mex|arg|argentina|colombia|andes)\\b"
      }
    }
  ]
}
```

### 📌 Códecs

#### 📌 x264
```json
{
  "name": "x264",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "x264/H264/AVC",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": false,
      "fields": {
        "value": "(?i)(x264|h264|avc)"
      }
    }
  ]
}
```

#### 📌 x265
```json
{
  "name": "x265",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "x265/H265/HEVC",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": false,
      "fields": {
        "value": "(?i)(x265|h265|hevc)"
      }
    }
  ]
}
```


---
✍️ **Autor:** Roger  
🚀 **Optimizado para:** Radarr, Sonarr y ARR Suite

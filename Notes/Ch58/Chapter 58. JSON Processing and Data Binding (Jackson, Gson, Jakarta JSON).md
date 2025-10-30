2025-10-22 21:49
Tags: #JSON #DataBinding #Jackson #Gson #Jakarta #toCheck 

## [[58.1. Introduction to JSON in Java (OK)]]


## [[58.2. Overview of JSON Libraries (to start)]]


## [[58.3. Jackson (FasterXML Jackson) (to format and check)]]


---

## **58.4. Gson**

### **58.4.1. Основные концепции**

- GsonBuilder и Gson
    
- JsonElement, JsonObject, JsonArray (Tree Model)
    
- Принципы Data Binding
    

### **58.4.2. Сериализация и десериализация**

- Автоматическое преобразование
    
- Custom TypeAdapter
    
- Exclusion Strategies (исключение полей)
    

### **58.4.3. Работа с Generic-типами**

- Использование `TypeToken`
    
- Runtime-рефлексия
    

### **58.4.4. Потоковая обработка (JsonReader/JsonWriter)**

---

## **58.5. Jakarta JSON Processing (JSON-P)**

### **58.5.1. Основные API**

- Streaming API (JsonParser, JsonGenerator)
    
- Object Model API (JsonObject, JsonArray)
    
- JSON-P vs Jackson/Gson
    

### **58.5.2. Работа с JSON Patch, JSON Pointer**

- Патчи (partial update)
    
- Работа с Pointer (указатели на элементы)
    

---

## **58.6. JSON Binding (Jakarta JSON-B)**

### **58.6.1. Общая концепция**

- Аналог Jackson, но стандарт Jakarta EE
    
- `Jsonb` интерфейс
    

### **58.6.2. Аннотации JSON-B**

- `@JsonbProperty`, `@JsonbTransient`
    
- Форматирование даты-времени
    
- Настройки null-полей
    

---

## **58.7. Streaming vs Tree Model vs Data Binding**

- 58.7.1. Когда использовать Streaming API (низкоуровневый, высокая производительность)
    
- 58.7.2. Tree Model API (гибкость)
    
- 58.7.3. Data Binding API (простота)
    
- 58.7.4. Сравнение по скорости и памяти
    

---

## **58.8. Common Use Cases**

- 58.8.1. Чтение JSON-файла из InputStream
    
- 58.8.2. Конвертация JSON-строки в объект
    
- 58.8.3. Запись JSON в файл, HTTP-ответ
    
- 58.8.4. Динамическое изменение JSON
    
- 58.8.5. Преобразование списков, вложенных структур
    

---

## **58.9. Integration with Frameworks**

- 58.9.1. Spring Boot и Jackson (auto-configuration)
    
- 58.9.2. Jakarta EE JSON-B Integration
    
- 58.9.3. RESTful сервисы (JAX-RS, Spring Web)
    
- 58.9.4. JSON и микросервисы (REST, gRPC, Kafka)
    

---

## **58.10. Performance and Benchmarking**

- 58.10.1. Сравнение сериализации Jackson vs Gson vs JSON-B
    
- 58.10.2. Memory Footprint
    
- 58.10.3. Lazy parsing и streaming для больших файлов
    

---

## **58.11. Security Considerations**

- 58.11.1. JSON Injection
    
- 58.11.2. Полиморфные атаки (Jackson vulnerabilities)
    
- 58.11.3. Safe configuration recommendations
    

---

## **58.12. Best Practices and Guidelines**

- 58.12.1. Стандартизация объектов (DTO)
    
- 58.12.2. Версионирование JSON API
    
- 58.12.3. Logging and Debugging JSON
    

---

## **58.13. Summary and Comparison Table**

- 58.13.1. Таблица сравнения Jackson, Gson, JSON-P, JSON-B
    
- 58.13.2. Рекомендации по применению в разных сценариях
    

---

### ✅ Готов продолжить:

**Хотите, чтобы я начал заполнять эти подразделы содержанием с примерами кода?**
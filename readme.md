# Proyekt adı : Global Travel Hub

## Açıqlama: Bu proyekt ilə, səyahət bələdçisi aplikasiyasının API-nı hazırlamaq lazım olacaq.

## Əsas özəllikləri:

### User CRUD:

1. `POST /users`: Yeni istifadəçi yaratmaq
2. `GET /users`: Bütün istifadəçilərə baxmaq(ancaq admin)
3. `GET /users/{userId}`: Id-yə görə spesifik user-i tapmaq
4. `PUT /users/{userId}`: User-in məlumatlarını dəyişmək
5. `DELETE /users/{userId}`: User-in məlumatlarını silmək

### Destination CRUD:

1. `POST /destinations`: Yeni istiqamət yaratmaq
2. `GET /destinations`: Bütün istiqamətləri gətirmək(login olmuş user-ə aid)
3. `GET /destinations/{destinationId}`: Seçilmiş istiqamətin detallarını gətirmək(login olmuş user-ə aid)
4. `PUT /destinations/{destinationId}`: Seçilən istiqaməti update etmək
5. `DELETE /destinations/{destinationId}`: İstiqaməti silmək

### Marşrut CRUD:

1. `POST /itineraries`: Yeni marşrut yaratmaq
2. `GET /itineraries`: Marşrutları gətirmək (login olmuş user-ə aid)
3. `GET /itineraries/{itineraryId}`: Seçilən marşrutun detallarını gətirmək
4. `PUT /itineraries/{itineraryId}`: Seçilən marşrutu dəyişmək
5. `DELETE /itineraries/{itineraryId}`: Marşrut silmək

### Yaşayış məntəqəsi CRUD:

1. `POST /accommodations`: Yeni məntəqə əlavə etmək
2. `GET /accommodations`: Bütün məntəqələri gətirmək
3. `GET /accommodations/{filter}`: Filterə uyğun məntəqələri gətirmək
4. `GET /accommodations/{accommodationId}`: Seçilən məntəqənin detallarını
5. `PUT /accommodations/{accommodationId}`: Məntəqəni detallarını dəyişmək
6. `DELETE /accommodations/{accommodationId}`: Məntəqəni ləvğ etmək

### Nəqliyyat CRUD:

1. `POST /transportations`: Yeni nəqliyyat əlavə etmək(admin spesifik)
2. `POST /transportations`: Yeni nəqliyyat əlavə etmək(admin spesifik)
3. `GET /transportations/{transportationId}`: Seçilən nəqliyyatın detallarını gətirmək
4. `PUT /transportations/{transportationId}`: Seçilən nəqliyyatın məlumatlarını dəyişmək
5. `DELETE /transportations/{transportationId}`: Nəqliyyatı silmək

### Content Management

1. `POST /{type}reviews`: Yuxarıda qeyd olunan: destination, marşrut, yaşayış məntəqəsi ayrılıqda rəy yarada bilmək
2. `GET /{type}reviews/`: Yazılan tipə görə bütün rəyləri gətirmək
3. `GET /{type}reviews/{filter}`: Yazılan tipə görə və filterə uyğun olan bütün rəyləri gətirmək
4. `GET /reviews/{reviewId}`: Seçilən rəyin detallarını gətirmək
5. `PUT /{type}reviews/{reviewId}`: Seçilən rəyin detallarını dəyişmək
6. `DELETE /reviews/{reviewId}`: Rəyi silmək

### Əlavə endpointlər

1. `GET /destinations/categories`: Destination tipinin kateqoriyalarını gətirmək(misal: şəhər, sahil, dağ və sair)
2. `GET /accommodation/types`: Yaşayış məntəqsi tipinin kateqoriyalarını gətirmək (misal: otellər, mənzillər, motellər və sair)
3. `GET /transportation/types`: Bütün nəqliyyat növlərini gətirmək (misal: təyyarə, qatar, avotbus)
4. `GET /itineraries/{itineraryId}/{transportationId}`: Səyahət üçün nəqliyyat seçmək
5. `GET /statistics`: Fərqli statiskilar gətirmək

### Əlavə challenge

> Edə bilsəniz, əlavə `GET /chat/{text}` kimi bir endpoint yazın və ChatGpt kimi suni zəkalardan birinə bağlayın.<br> `GET {eventApiUrl}/events/calendar`: Bundan əvvəl yazdığımız event API-dən hazırki gündə olan eventləri gətirmək🤠<br> `GET {eventApiUrl}/events/{destinationId}`: Bundan əvvəl yazdığımız event API-dən verilən destinationda olan eventləri gətirmək🤠

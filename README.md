# IT Help Desk

## English

A web application for recording and managing university technical support requests. Built with ASP.NET Core MVC and SQLite, it keeps tickets in a local database and provides an Azerbaijani user interface.

### Features

- Create tickets with a title, description, category, and priority.
- View all tickets, with the newest requests first.
- Open ticket details, including the creation date.
- Edit ticket information and update its status.
- Delete tickets after confirmation.
- View the total number of tickets on the home page.
- Identify high-priority tickets through color highlighting.
- Validate required fields before saving.

### Ticket options

| Field | Values |
| --- | --- |
| Category | Computer, Internet, Printer, Software |
| Priority | Low, Normal, High |
| Status | New, In Progress, Resolved, Closed |

New tickets receive the **New** status automatically.

### Technologies

- C# and .NET 8
- ASP.NET Core MVC and Razor Views
- Entity Framework Core 8
- SQLite
- HTML, CSS, and Bootstrap 5

### Run locally

Install the **.NET 8 SDK**, then extract or clone the project. Open a terminal in the folder containing `HelpDeskWeb.csproj` and run:

```bash
dotnet restore
dotnet run
```

Open the local address shown in the terminal. Keep the terminal open while using the application. Press **Ctrl+C** to stop it.

Alternatively, open `HelpDeskWeb.csproj` in Visual Studio with .NET 8 support and the **ASP.NET and web development** workload, then press **Ctrl+F5**.

### Database

The application uses a local SQLite file named `helpdesk.db`. The database and tables are created automatically if they do not exist. Tickets remain saved after restarting the application.

The connection string is defined in `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=helpdesk.db"
  }
}
```

### Project organization

| Path | Purpose |
| --- | --- |
| `Controllers/` | Handles page requests and ticket operations |
| `Models/` | Defines the ticket model and validation rules |
| `Views/` | Contains Razor pages |
| `Data/` | Contains the database context |
| `wwwroot/` | Stores static assets |
| `Program.cs` | Configures services, routing, and startup |

Bootstrap is loaded from a CDN and requires an internet connection. Local CSS is also included.

---

## Azərbaycanca

Universitetdə texniki dəstək müraciətlərinin qeydiyyatı və idarə edilməsi üçün hazırlanmış veb tətbiq. ASP.NET Core MVC və SQLite əsasında qurulub, müraciətləri lokal verilənlər bazasında saxlayır və Azərbaycan dilində interfeys təqdim edir.

### İmkanlar

- Başlıq, təsvir, kateqoriya və prioritet seçərək müraciət yaratmaq.
- Bütün müraciətləri ən yenisi əvvəl olmaqla siyahıda görmək.
- Müraciətin detallarına və yaradılma tarixinə baxmaq.
- Müraciət məlumatlarını redaktə etmək və statusunu dəyişmək.
- Təsdiqdən sonra müraciəti silmək.
- Ana səhifədə ümumi müraciət sayını görmək.
- Yüksək prioritetli müraciətləri rənglə fərqləndirmək.
- Məlumatları saxlamazdan əvvəl məcburi sahələri yoxlamaq.

### Müraciət seçimləri

| Sahə | Seçimlər |
| --- | --- |
| Kateqoriya | Kompüter, İnternet, Printer, Proqram təminatı |
| Prioritet | Aşağı, Normal, Yüksək |
| Status | New — Yeni; In Progress — İcra olunur; Resolved — Həll edilib; Closed — Bağlanıb |

Yeni müraciətlərə avtomatik **New** statusu verilir.

### İstifadə olunan texnologiyalar

- C# və .NET 8
- ASP.NET Core MVC və Razor Views
- Entity Framework Core 8
- SQLite
- HTML, CSS və Bootstrap 5

### İşə salmaq

**.NET 8 SDK** quraşdırın, sonra layihəni ZIP-dən çıxarın və ya repozitoriyanı klonlayın. `HelpDeskWeb.csproj` faylının yerləşdiyi qovluqda terminal açaraq bu əmrləri icra edin:

```bash
dotnet restore
dotnet run
```

Terminalda göstərilən lokal ünvanı brauzerdə açın. Tətbiqdən istifadə edərkən terminalı açıq saxlayın. Dayandırmaq üçün **Ctrl+C** basın.

Alternativ olaraq, `HelpDeskWeb.csproj` faylını .NET 8 dəstəyi və **ASP.NET and web development** komponenti olan Visual Studio-da açıb **Ctrl+F5** basın.

### Verilənlər bazası

Tətbiq `helpdesk.db` adlı lokal SQLite faylından istifadə edir. Baza və cədvəllər mövcud deyilsə, avtomatik yaradılır. Tətbiq yenidən başladıldıqda müraciətlər saxlanılır.

Bağlantı sətri `appsettings.json` faylında göstərilir:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=helpdesk.db"
  }
}
```

### Layihənin quruluşu

| Yol | Təyinat |
| --- | --- |
| `Controllers/` | Səhifə sorğularını və müraciət əməliyyatlarını idarə edir |
| `Models/` | Müraciət modelini və məlumat yoxlama qaydalarını saxlayır |
| `Views/` | Razor səhifələrini saxlayır |
| `Data/` | Verilənlər bazası kontekstini saxlayır |
| `wwwroot/` | Statik faylları saxlayır |
| `Program.cs` | Servisləri, marşrutları və tətbiqin başlanmasını tənzimləyir |

Bootstrap CDN vasitəsilə yükləndiyi üçün internet bağlantısı tələb olunur. Layihəyə lokal CSS də daxildir.


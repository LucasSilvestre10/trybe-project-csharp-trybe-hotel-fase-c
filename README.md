# Trybe Hotel - Fase C

#### Requisito 1 - Adição do Atributo State na Model City

Foi adicionado o atributo `State` na model `City`. As mudanças foram aplicadas no banco de dados utilizando migrations.

#### Requisito 2 - Refatoração do Endpoint POST /city

O endpoint POST /city foi refatorado, e a response da API agora segue o formato:
```json
{
    "cityId": 1,
    "name": "Rio de Janeiro",
    "state": "RJ"
}
```
A refatoração foi implementada no método `AddCity()` do arquivo `src/TrybeHotel/Repository/CityRepository.cs`.

#### Requisito 3 - Desenvolvimento do Endpoint PUT /city

Foi desenvolvido o endpoint PUT /city para atualizar os dados de uma cidade existente. A response da API agora segue o formato:
```json
{
    "cityId": 1,
    "name": "Rio de Janeiro",
    "state": "RJ"
}
```
A lógica foi implementada no método `PutCity()` da controller e no método `UpdateCity()` da repository.

#### Requisito 4 - Refatoração do Endpoint GET /city

O endpoint GET /city foi refatorado, e a response da API agora segue o formato:
```json
[
    {
        "cityId": 1,
        "name": "Rio de Janeiro",
        "state": "RJ"
    },
    /* ... */
]
```
A refatoração foi implementada no método `GetCities()` do arquivo `src/TrybeHotel/Repository/CityRepository.cs`.

#### Requisito 5 - Refatoração do Endpoint GET /hotel

O endpoint GET /hotel foi refatorado, e a response da API agora segue o formato:
```json
[
    {
        "hotelId": 1,
        "name": "Trybe Hotel SP",
        "address": "Avenida Paulista, 1400",
        "cityId": 1,
        "cityName": "São Paulo",
        "state": "SP"
    },
    /* ... */
]
```
A refatoração foi implementada no método `GetHotels()` do arquivo `src/TrybeHotel/Repository/HotelRepository.cs`.

#### Requisito 6 - Refatoração do Endpoint POST /hotel

O endpoint POST /hotel foi refatorado, e a response da API agora segue o formato:
```json
{
    "hotelId": 1,
    "name": "Trybe Hotel SP",
    "address": "Avenida Paulista, 1400",
    "cityId": 1,
    "cityName": "São Paulo",
    "state": "SP"
}
```
A refatoração foi implementada no método `AddHotel()` do arquivo `src/TrybeHotel/Repository/HotelRepository.cs`.

#### Requisito 7 - Refatoração do Endpoint GET /room

O endpoint GET /room foi refatorado, e a response da API agora segue o formato:
```json
[
    {
        "roomId": 1,
        "name": "Suite básica",
        "capacity": 2,
        "image": "image suite",
        "hotel": {
            "hotelId": 1,
            "name": "Trybe Hotel SP",
            "address": "Avenida Paulista, 1400",
            "cityId": 1,
            "cityName": "São Paulo",
            "state": "SP"
        }
    }
]
```
A refatoração foi implementada no método `GetRooms()` do arquivo `src/TrybeHotel/Repository/RoomRepository.cs`.

#### Requisito 8 - Refatoração do Endpoint POST /room

O endpoint POST /room foi refatorado, e a response da API agora segue o formato:
```json
{
    "roomId": 1,
    "name": "Suite básica",
    "capacity": 2,
    "image": "image suite",
    "hotel": {
        "hotelId": 1,
        "name": "Trybe Hotel SP",
        "address": "Avenida Paulista, 1400",
        "cityId": 1,
        "cityName": "São Paulo",
        "state": "SP"
    }
}
```
A refatoração foi implementada no método `AddRoom()` do arquivo `src/TrybeHotel/Repository/RoomRepository.cs`.

#### Requisito 9 - Refatoração do Endpoint POST /booking

O endpoint POST /booking foi refatorado, e a response da API agora segue o formato:
```json
{
    "bookingId": 1,
    "checkIn": "2030-08-27T00:00:00",
    "checkOut": "2030-08-28T00:00:00",
    "guestQuant": 1,
    "room": {
        "roomId": 1,
        "name": "Suite básica",
        "capacity": 2,
        "image": "image suite",
        "hotel": {
            "hotelId": 1,
            "name": "Trybe Hotel RJ",
            "address": "Avenida Atlântica, 1400",
            "cityId": 1,
            "cityName": "Rio de Janeiro",
            "state": "RJ"
        }
    }
}
```
A refatoração foi implementada no método `Add()` do arquivo `src/TrybeHotel/Repository/BookingRepository.cs`.

#### Requisito 10 - Refatoração do Endpoint GET /booking

O endpoint GET /booking foi refatorado, e a response da API agora segue o formato:
```json
{
    "bookingId": 1,
    "checkIn": "2030-08-27T00:00:00",
    "checkOut": "2030-08-28T00:00:00",
    "guestQuant": 1,
    "room": {
        "roomId": 1,
        "name": "Suite básica",
        "capacity": 2,
        "image": "image suite",
        "hotel": {
            "hotelId": 1,
            "name": "Trybe Hotel RJ",
            "address": "Avenida Atlântica, 1400",
            "cityId": 1,
            "cityName": "Rio de Janeiro",
            "state": "RJ"
        }
    }
}
```
A refatoração foi implementada no método `Add()` do arquivo `src/TrybeHotel/Repository/BookingRepository.cs`.

#### Requisito 11 - Desenvolvimento do Endpoint GET /geo/status

Foi desenvolvido o endpoint GET /geo/status para conferir o status da API externa responsável pela geolocalização. A response da API segue o padr

ão da API externa:
```json
{
    "status": 0,
    "message": "OK",
    "data_updated": "2020-05-04T14:47:00+00:00",
    "software_version": "3.6.0-0",
    "database_version": "3.6.0-0"
}
```
A lógica foi implementada no método `GetGeoStatus()` do arquivo `src/TrybeHotel/Services/GeoService.cs` e na controller no método `GetStatus()` do arquivo `src/TrybeHotel/Controllers/GeoController.cs`.

### Habilidades Técnicas

- **Linguagens:**
  - C#
  - ASP.NET
- **Tecnologias:**
  - LINQ
  - Entity Framework
  - REST API
  - JSON
- **Banco de Dados:**
  - SQL Server
  - Migrations
- **Outros:**
  - DTO (Data Transfer Object)
  - Geolocalização
  - Testes de Integração

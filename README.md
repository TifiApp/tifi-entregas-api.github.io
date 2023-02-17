# API TIFI

**URL** : https://tifivirgin-backend.herokuapp.com/

# Método [GET] - /api/requests/virgin

> **Descripción**: Este método me devuelve todas las solicitudes creadas en la API.
>
>  ### **URL**: https://tifivirgin-backend.herokuapp.com/api/requests/virgin
>

+ Response de ejemplo [200]

            [
              {
                "numEntrega": "6f990a10",
                "ciudad": {
                  "nameCity": "CALI",
                  "manager": "TIFI"
                },
                "direccion": "CLL 16 61 24",
                "localidad": "COMUNA 17",
                "barrio": "BARRIO LIMONAR",
                "nomCliente": "TEST TIFI",
                "numCelular": 3000000000,
                "numCedula": "1000000000",
                "tipo": "Portabilidad",
                "estado": "Pendiente por asignacion",
                "asesorId": {
                  "name": "virgin page"
                },
                "domiciliarioId": null,
                "cantidadSimCards": "1",
                "serialSimCards": [],
                "observaciones": "OBSERVACIONES OPCIONAL",
                "imagen": null,
                "nomReceptor": null,
                "valRecarga": null,
                "lineaVirgin": 3192839535,
                "nip": 63873,
                "assignmentAt": null,
                "deliveredAt": null,
                "createdAt": "2023-02-16T03:49:36.764Z",
                "updatedAt": "2023-02-16T03:49:36.764Z"
              },
              ...
            ]

# Método [POST] - /api/requests/virgin/create

> **Descripción**: Este método me permite crear una solicitud con los siguientes datos en la API.
**apikey: corresponde al apikey proporcionada por parte de tifi**
**ciudad: se debe enviar en nombre de la nameCity obtenido de "https://tifivirgin-backend.herokuapp.com/api/requests/virgin/cities/{nameDepartment}**
>
>  ### **URL**: https://tifivirgin-backend.herokuapp.com/api/requests/virgin/create
>


    + Body

            {
                "apikey": string,
                "ciudad": string,
                "direccion": string,
                "localidad": string,
                "barrio": string,
                "nomCliente": string,
                "numCelular": number,
                "numCedula": string,
                "tipo": string,
                "cantidadSimCards": string,
                "observaciones": string,
                "valRecarga": string,
                "lineaVirgin": number,
                "nip": number
            },


# Método [GET] - /api/requests/virgin/departments/{nameCountry}

> **Descripción**: Este método me devuelve todos los departamentos por un país que se envía como parámetro
>
> **nameCountry correspondiente al país debe ir en mayúsculas y es un string.**
>
>  ### **URL**: https://tifivirgin-backend.herokuapp.com/api/requests/virgin/deparments/{nameCountry}
>

+ Response de ejemplo [200]

            [
              {
                  "_id": "636c34c5480dd5e3821e95a7",
                  "nameDepartment": "NORTE DE SANTANDER",
                  "abbreviation": "N/STDER",
                  "countryId": "636bc30f53d92e88b08700b3",
                  "createdAt": "2022-11-09T23:16:21.317Z",
                  "updatedAt": "2022-11-09T23:16:21.317Z"
                },
                {
                  "_id": "636c33cb480dd5e3821e9589",
                  "nameDepartment": "CAUCA",
                  "abbreviation": "CAU",
                  "countryId": "636bc30f53d92e88b08700b3",
                  "createdAt": "2022-11-09T23:12:11.550Z",
                  "updatedAt": "2022-11-09T23:12:11.550Z"
                },
                {
                  "_id": "636c32f5480dd5e3821e956f",
                  "nameDepartment": "AMAZONAS",
                  "abbreviation": "AMAZ",
                  "countryId": "636bc30f53d92e88b08700b3",
                  "createdAt": "2022-11-09T23:08:37.112Z",
                  "updatedAt": "2022-11-09T23:08:37.112Z"
                },updatedAt": "2023-02-16T03:49:36.764Z"
              },
              ...
            ]


# Método [GET] - /api/requests/virgin/cities/{nameDepartment}

> **Descripción**: Este método me devuelve todos las ciudades por el departamento que se envía como parámetro
>
> **nameDepartment correspondiente al departamento debe ir en mayúsculas y es un string.**
>
>  ### **URL**: https://tifivirgin-backend.herokuapp.com/api/requests/virgin/cities/{nameDepartment}
>

+ Response de ejemplo [200]

            [
              {
                  "_id": "636ed7503c32658f9249bc60",
                  "nameCity": "APULO",
                  "deliveryTime": "7",
                  "departmentId": "636c340c480dd5e3821e9595",
                  "createdAt": "2022-11-11T23:14:24.655Z",
                  "updatedAt": "2022-11-11T23:14:24.655Z",
                  "manager": "LOGISTICA"
                },
                {
                  "_id": "636ed8f73c32658f9249bca5",
                  "nameCity": "CHINAUTA",
                  "deliveryTime": "9",
                  "departmentId": "636c340c480dd5e3821e9595",
                  "createdAt": "2022-11-11T23:21:27.668Z",
                  "updatedAt": "2022-11-11T23:21:27.668Z",
                  "manager": "LOGISTICA"
                },
                {
                  "_id": "63740d70fe6f2bfc99693869",
                  "nameCity": "GUACHIPAS",
                  "deliveryTime": "17",
                  "departmentId": "636c340c480dd5e3821e9595",
                  "createdAt": "2022-11-15T22:06:40.564Z",
                  "updatedAt": "2022-11-15T22:06:40.564Z",
                  "manager": "LOGISTICA"
                },
              ...
            ]



# Manejo-de-Versiones
graph TD
    subgraph Cliente
        A[Dispositivo del Usuario (PC o Smartphone)]
    end

    subgraph CDN
        B[CDN: Assets, Imágenes, Trailers]
    end

    subgraph Web
        C[Servidor Web (Frontend)]
    end

    subgraph App
        D[Servidor de Aplicaciones]
        D1[Módulo de Autenticación]
        D2[Módulo de Catálogo de Juegos]
        D3[Módulo de Pagos]
        D4[Módulo de Biblioteca de Usuario]
        D5[Módulo de Gestión de Descargas]
        D6[Módulo de Notificaciones]
    end

    subgraph DB
        E[Servidor de Base de Datos]
        E1[DB de Usuarios]
        E2[DB de Juegos]
        E3[DB de Transacciones]
    end

    subgraph Email
        F[Servidor de Correo (Verificación)]
    end

    A --> C
    A --> B
    C --> D
    D --> E
    D6 --> F
    D --> D1
    D --> D2
    D --> D3
    D --> D4
    D --> D5

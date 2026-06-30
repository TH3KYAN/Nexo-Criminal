# Plan de Commits

---

## Prerrequisitos (antes del Sprint 1)

### Setup del proyecto

| # | Autor | Archivos |
|---|-------|----------|
| 1 | **Manuel** | `backend/pom.xml`, `backend/src/main/java/com/nexocriminal/NexoCriminalApplication.java`, `backend/src/main/resources/application.properties` |
| 2 | **John** | `frontend/package.json`, `frontend/package-lock.json`, `frontend/index.html`, `frontend/vite.config.ts`, `frontend/tsconfig.json`, `frontend/src/main.tsx`, `frontend/src/styles.css`, `frontend/src/vite-env.d.ts`, `frontend/.env.development`, `frontend/public/thread.svg` |
| 3 | Isaac | `.gitignore`, `README.md`, `QUICKSTART.md`, `backend/README.md`, `frontend/README.md` |
| 4 | Santiago | `scripts/generar_datos.py`, `scripts/requirements.txt`, `scripts/README.md` |

### Base de datos

| # | Autor | Archivos |
|---|-------|----------|
| 5 | **Manuel** | `database/01-schema.sql`, `database/02-datos-ejemplo.sql` |

### Autenticación

| # | Autor | Archivos |
|---|-------|----------|
| 6 | **Manuel** | `backend/src/main/java/com/nexocriminal/security/SecurityConfig.java`, `backend/src/main/java/com/nexocriminal/security/JwtService.java`, `backend/src/main/java/com/nexocriminal/security/JwtAuthFilter.java` |
| 7 | **John** | `backend/src/main/java/com/nexocriminal/security/AuthController.java`, `backend/src/main/java/com/nexocriminal/security/Usuario.java`, `backend/src/main/java/com/nexocriminal/security/UsuarioRepository.java`, `backend/src/main/java/com/nexocriminal/security/BootstrapAdmin.java` |
| 8 | **John** | `backend/src/main/java/com/nexocriminal/middleware/CadenaMiddleware.java`, `backend/src/main/java/com/nexocriminal/middleware/ContextoPeticion.java`, `backend/src/main/java/com/nexocriminal/middleware/ManejadorPeticion.java`, `backend/src/main/java/com/nexocriminal/middleware/MiddlewareFilter.java`, `backend/src/main/java/com/nexocriminal/middleware/eslabones/ManejadorAutenticacion.java`, `backend/src/main/java/com/nexocriminal/middleware/eslabones/ManejadorAutorizacion.java` |
| 9 | **Manuel** | `backend/src/main/java/com/nexocriminal/common/GlobalExceptionHandler.java`, `backend/src/main/java/com/nexocriminal/config/ManejadorErroresValidacion.java` |
| 10 | **John** | `frontend/src/pages/Login.tsx`, `frontend/src/services/AuthContext.tsx` |
| 11 | **Manuel** | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` |
| 12 | Valeria | `frontend/src/App.tsx` |

### Personas CRUD

| # | Autor | Archivos |
|---|-------|----------|
| 13 | **Manuel** | `backend/src/main/java/com/nexocriminal/persona/application/CreatePersona.java`, `backend/src/main/java/com/nexocriminal/persona/application/UpdatePersona.java`, `backend/src/main/java/com/nexocriminal/persona/application/DeletePersona.java` |
| 14 | **Manuel** | `backend/src/main/java/com/nexocriminal/persona/application/ListPersonas.java`, `backend/src/main/java/com/nexocriminal/persona/application/GetPersona.java` |
| 15 | **John** | `backend/src/main/java/com/nexocriminal/persona/domain/model/Persona.java`, `backend/src/main/java/com/nexocriminal/persona/domain/port/PersonaRepositoryPort.java` |
| 16 | **John** | `backend/src/main/java/com/nexocriminal/persona/infrastructure/persistence/PersonaMapper.java`, `backend/src/main/java/com/nexocriminal/persona/infrastructure/persistence/PersonaRepositoryAdapter.java` |
| 17 | Isaac | `backend/src/main/java/com/nexocriminal/persona/infrastructure/web/PersonaController.java`, `backend/src/main/java/com/nexocriminal/persona/infrastructure/web/dto/PersonaRequest.java`, `backend/src/main/java/com/nexocriminal/persona/infrastructure/web/dto/PersonaResponse.java` |
| 18 | Santiago | `backend/src/main/java/com/nexocriminal/domain/persona/Persona.java`, `backend/src/main/java/com/nexocriminal/domain/persona/PersonaRepository.java`, `backend/src/main/java/com/nexocriminal/domain/persona/PersonaService.java`, `backend/src/main/java/com/nexocriminal/domain/persona/RolPersona.java` |
| 19 | **Manuel** | `backend/src/main/java/com/nexocriminal/validacion/ValidadorVenezolano.java`, `backend/src/main/java/com/nexocriminal/validacion/anotaciones/CedulaVenezolana.java`, `backend/src/main/java/com/nexocriminal/validacion/anotaciones/PlacaVenezolana.java`, `backend/src/main/java/com/nexocriminal/validacion/anotaciones/TelefonoVenezolano.java`, `backend/src/main/java/com/nexocriminal/validacion/validators/CedulaValidator.java`, `backend/src/main/java/com/nexocriminal/validacion/validators/PlacaValidator.java`, `backend/src/main/java/com/nexocriminal/validacion/validators/TelefonoValidator.java` |
| 20 | **John** | `frontend/src/pages/Personas.tsx`, `frontend/src/components/FormPersona.tsx` |
| 21 | **John** | `frontend/src/components/Sidebar.tsx`, `frontend/src/components/TopBar.tsx`, `frontend/src/components/FooterStatus.tsx` |
| 22 | Valeria | `frontend/src/components/Modal.tsx`, `frontend/src/components/ModalDetalle.tsx`, `frontend/src/components/ModalConfirmar.tsx`, `frontend/src/components/Paginacion.tsx` |
| 23 | Isaac | `frontend/src/services/PrefsContext.tsx`, `frontend/src/services/ToastContext.tsx`, `frontend/src/services/ConfirmContext.tsx` |

---

## Sprint 1

### Tarea 1: Registro de Vehículos

| # | Autor | Archivos |
|---|-------|----------|
| 24 | **Manuel** | `backend/src/main/java/com/nexocriminal/vehiculo/application/CreateVehiculo.java`, `backend/src/main/java/com/nexocriminal/vehiculo/application/UpdateVehiculo.java`, `backend/src/main/java/com/nexocriminal/vehiculo/application/DeleteVehiculo.java`, `backend/src/main/java/com/nexocriminal/vehiculo/application/GetVehiculo.java` |
| 25 | **John** | `backend/src/main/java/com/nexocriminal/vehiculo/domain/model/Vehiculo.java`, `backend/src/main/java/com/nexocriminal/vehiculo/domain/port/VehiculoRepositoryPort.java`, `backend/src/main/java/com/nexocriminal/vehiculo/domain/port/PersonaReaderPort.java` |
| 26 | **John** | `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/persistence/VehiculoMapper.java`, `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/persistence/VehiculoRepositoryAdapter.java`, `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/persistence/PersonaReaderAdapter.java` |
| 27 | **Manuel** | `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/VehiculoController.java`, `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/dto/VehiculoRequest.java`, `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/dto/VehiculoResponse.java`, `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/dto/PropietarioResumen.java` |
| 28 | Isaac | `backend/src/main/java/com/nexocriminal/domain/vehiculo/Vehiculo.java`, `backend/src/main/java/com/nexocriminal/domain/vehiculo/EstadoVehiculo.java`, `backend/src/main/java/com/nexocriminal/domain/vehiculo/VehiculoRepository.java`, `backend/src/main/java/com/nexocriminal/domain/vehiculo/VehiculoService.java` |
| 29 | **Manuel** | `frontend/src/pages/Vehiculos.tsx` |
| 30 | Santiago | `frontend/src/components/FormVehiculo.tsx` |
| 31 | Valeria | `frontend/src/services/files.ts` |

### Tarea 2: Marcado del estado del vehículo

| # | Autor | Archivos |
|---|-------|----------|
| 32 | **Manuel** | `backend/src/main/java/com/nexocriminal/vehiculo/application/ChangeVehiculoEstado.java` |
| 33 | **John** | `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/VehiculoController.java` (actualizar con PATCH /estado) |
| 34 | Isaac | `frontend/src/pages/Vehiculos.tsx` (agregar dropdown de estado) |

### Tarea 3: Listado de vehículos con filtro

| # | Autor | Archivos |
|---|-------|----------|
| 35 | **Manuel** | `backend/src/main/java/com/nexocriminal/vehiculo/application/ListVehiculos.java` |
| 36 | **John** | `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/VehiculoController.java` (actualizar GET con filtros) |
| 37 | **John** | `frontend/src/pages/Vehiculos.tsx` (agregar filtros + barra de búsqueda) |
| 38 | **Manuel** | `frontend/src/services/exportar.ts` |
| 39 | Santiago | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar) |

### Tarea 4: Registro de ubicaciones y geoposicionamiento

| # | Autor | Archivos |
|---|-------|----------|
| 40 | **John** | `backend/src/main/java/com/nexocriminal/ubicacion/application/CreateUbicacion.java`, `backend/src/main/java/com/nexocriminal/ubicacion/application/UpdateUbicacion.java`, `backend/src/main/java/com/nexocriminal/ubicacion/application/DeleteUbicacion.java` |
| 41 | **Manuel** | `backend/src/main/java/com/nexocriminal/ubicacion/application/GetUbicacion.java`, `backend/src/main/java/com/nexocriminal/ubicacion/application/ListUbicaciones.java`, `backend/src/main/java/com/nexocriminal/ubicacion/application/MarkSuspiciousNode.java` |
| 42 | **John** | `backend/src/main/java/com/nexocriminal/ubicacion/domain/model/Ubicacion.java`, `backend/src/main/java/com/nexocriminal/ubicacion/domain/port/UbicacionRepositoryPort.java` |
| 43 | **Manuel** | `backend/src/main/java/com/nexocriminal/ubicacion/infrastructure/persistence/UbicacionMapper.java`, `backend/src/main/java/com/nexocriminal/ubicacion/infrastructure/persistence/UbicacionRepositoryAdapter.java` |
| 44 | Isaac | `backend/src/main/java/com/nexocriminal/ubicacion/infrastructure/web/UbicacionController.java`, `backend/src/main/java/com/nexocriminal/ubicacion/infrastructure/web/dto/UbicacionRequest.java`, `backend/src/main/java/com/nexocriminal/ubicacion/infrastructure/web/dto/UbicacionResponse.java` |
| 45 | Valeria | `backend/src/main/java/com/nexocriminal/domain/ubicacion/Ubicacion.java`, `backend/src/main/java/com/nexocriminal/domain/ubicacion/TipoUbicacion.java`, `backend/src/main/java/com/nexocriminal/domain/ubicacion/UbicacionRepository.java`, `backend/src/main/java/com/nexocriminal/domain/ubicacion/UbicacionService.java` |
| 46 | **John** | `frontend/src/pages/Ubicaciones.tsx` |
| 47 | **Manuel** | `frontend/src/components/MapaTactical.tsx` |
| 48 | Santiago | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar) |

### Tarea 5: Registro de avistamiento de vehículos

| # | Autor | Archivos |
|---|-------|----------|
| 49 | **Manuel** | `backend/src/main/java/com/nexocriminal/domain/avistamiento/Avistamiento.java`, `backend/src/main/java/com/nexocriminal/domain/avistamiento/AvistamientoStack.java` |
| 50 | **John** | `backend/src/main/java/com/nexocriminal/vehiculo/infrastructure/web/VehiculoController.java` (actualizar con POST /avistamientos) |
| 51 | **Manuel** | `frontend/src/pages/Vehiculos.tsx` (agregar modal "Registrar avistamiento") |
| 52 | Isaac | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar) |

---

## Sprint 2

### Tarea 1: Registro de personas desaparecidas

| # | Autor | Archivos |
|---|-------|----------|
| 53 | **Manuel** | `backend/src/main/java/com/nexocriminal/desaparecida/application/CreateDesaparecida.java`, `backend/src/main/java/com/nexocriminal/desaparecida/application/UpdateDesaparecida.java`, `backend/src/main/java/com/nexocriminal/desaparecida/application/DeleteDesaparecida.java`, `backend/src/main/java/com/nexocriminal/desaparecida/application/GetDesaparecida.java` |
| 54 | **John** | `backend/src/main/java/com/nexocriminal/desaparecida/domain/model/Desaparecida.java`, `backend/src/main/java/com/nexocriminal/desaparecida/domain/port/DesaparecidaRepositoryPort.java`, `backend/src/main/java/com/nexocriminal/desaparecida/domain/port/UbicacionReaderPort.java` |
| 55 | **John** | `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/persistence/DesaparecidaMapper.java`, `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/persistence/DesaparecidaRepositoryAdapter.java`, `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/persistence/UbicacionReaderAdapter.java` |
| 56 | **Manuel** | `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/web/DesaparecidaController.java`, `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/web/dto/DesaparecidaRequest.java`, `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/web/dto/DesaparecidaResponse.java` |
| 57 | Isaac | `backend/src/main/java/com/nexocriminal/domain/desaparecida/PersonaDesaparecida.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/EstadoDesaparicion.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/PrioridadDesaparicion.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/PersonaDesaparecidaRepository.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/PersonaDesaparecidaService.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/FotoDesaparecida.java`, `backend/src/main/java/com/nexocriminal/domain/desaparecida/FotoDesaparecidaRepository.java` |
| 58 | **John** | `backend/src/main/java/com/nexocriminal/files/FileStorageService.java`, `backend/src/main/java/com/nexocriminal/files/FileStorageConfig.java` |
| 59 | **Manuel** | `frontend/src/pages/Desaparecidas.tsx`, `frontend/src/components/FormularioDesaparecida.tsx` |
| 60 | Valeria | `frontend/src/components/GaleriaFotos.tsx` |
| 61 | Santiago | `frontend/src/services/validaciones.ts` |

### Tarea 2: Listado de personas desaparecidas

| # | Autor | Archivos |
|---|-------|----------|
| 62 | **Manuel** | `backend/src/main/java/com/nexocriminal/desaparecida/application/ListDesaparecidas.java`, `backend/src/main/java/com/nexocriminal/desaparecida/application/BuscarCercanas.java`, `backend/src/main/java/com/nexocriminal/desaparecida/application/ChangeDesaparecidaEstado.java` |
| 63 | **John** | `backend/src/main/java/com/nexocriminal/desaparecida/infrastructure/web/DesaparecidaController.java` (actualizar GET endpoints) |
| 64 | **Manuel** | `frontend/src/pages/Desaparecidas.tsx` (galería + tabla + filtros) |
| 65 | Isaac | `frontend/src/components/ModalDesaparecida.tsx` |
| 66 | **John** | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de desaparecidas) |

### Tarea 3: Listado de sucesos con filtro

| # | Autor | Archivos |
|---|-------|----------|
| 67 | **Manuel** | `backend/src/main/java/com/nexocriminal/suceso/application/ListSucesos.java`, `backend/src/main/java/com/nexocriminal/suceso/application/GetSuceso.java` |
| 68 | **John** | `backend/src/main/java/com/nexocriminal/suceso/domain/model/Suceso.java`, `backend/src/main/java/com/nexocriminal/suceso/domain/port/SucesoRepositoryPort.java`, `backend/src/main/java/com/nexocriminal/suceso/domain/port/PersonaReaderPort.java`, `backend/src/main/java/com/nexocriminal/suceso/domain/port/VehiculoReaderPort.java`, `backend/src/main/java/com/nexocriminal/suceso/domain/port/UbicacionReaderPort.java` |
| 69 | **Manuel** | `backend/src/main/java/com/nexocriminal/suceso/infrastructure/persistence/SucesoMapper.java`, `backend/src/main/java/com/nexocriminal/suceso/infrastructure/persistence/SucesoRepositoryAdapter.java`, `backend/src/main/java/com/nexocriminal/suceso/infrastructure/persistence/PersonaReaderAdapter.java`, `backend/src/main/java/com/nexocriminal/suceso/infrastructure/persistence/VehiculoReaderAdapter.java`, `backend/src/main/java/com/nexocriminal/suceso/infrastructure/persistence/UbicacionReaderAdapter.java` |
| 70 | **John** | `backend/src/main/java/com/nexocriminal/suceso/infrastructure/web/SucesoController.java` (GET), `backend/src/main/java/com/nexocriminal/suceso/infrastructure/web/dto/SucesoResponse.java` |
| 71 | Isaac | `backend/src/main/java/com/nexocriminal/domain/suceso/Suceso.java`, `backend/src/main/java/com/nexocriminal/domain/suceso/TipoSuceso.java`, `backend/src/main/java/com/nexocriminal/domain/suceso/SucesoRepository.java`, `backend/src/main/java/com/nexocriminal/domain/suceso/SucesoService.java` |
| 72 | Valeria | `frontend/src/pages/Sucesos.tsx` (filtros + tabla) |
| 73 | Santiago | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de sucesos) |

### Tarea 4: Registro de sucesos delictivos

| # | Autor | Archivos |
|---|-------|----------|
| 74 | **Manuel** | `backend/src/main/java/com/nexocriminal/suceso/application/CreateSuceso.java`, `backend/src/main/java/com/nexocriminal/suceso/application/DeleteSuceso.java` |
| 75 | **John** | `backend/src/main/java/com/nexocriminal/suceso/infrastructure/web/dto/SucesoRequest.java` |
| 76 | **Manuel** | `backend/src/main/java/com/nexocriminal/suceso/infrastructure/web/SucesoController.java` (POST, DELETE) |
| 77 | **John** | `frontend/src/pages/Sucesos.tsx` (formulario de creación) |
| 78 | Isaac | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar) |

---

## Sprint 3

### Tarea 1: Detección automática de patrones delictivos por el motor de reglas

| # | Autor | Archivos |
|---|-------|----------|
| 79 | **Manuel** | `backend/src/main/java/com/nexocriminal/engine/ReglaVinculo.java`, `backend/src/main/java/com/nexocriminal/engine/RedThreadEngineService.java` |
| 80 | **Manuel** | `backend/src/main/java/com/nexocriminal/config/ConfiguracionMotor.java`, `backend/src/main/java/com/nexocriminal/config/ConfiguracionMotorRepository.java`, `backend/src/main/java/com/nexocriminal/config/ConfiguracionMotorService.java` |
| 81 | **John** | `backend/src/main/java/com/nexocriminal/engine/ReglaNodoLogistico.java` |
| 82 | **John** | `backend/src/main/java/com/nexocriminal/engine/ReglaEscoltaVehicular.java` |
| 83 | Isaac | `backend/src/main/java/com/nexocriminal/engine/ReglaCirculoConfianza.java` |
| 84 | Isaac | `backend/src/main/java/com/nexocriminal/engine/ReglaSimilitudModusOperandi.java` |
| 85 | **Manuel** | `backend/src/main/java/com/nexocriminal/engine/ReglaClusterDesapariciones.java` |

### Tarea 2: Clasificación automática del riesgo de cada alerta

| # | Autor | Archivos |
|---|-------|----------|
| 86 | **John** | `backend/src/main/java/com/nexocriminal/domain/alerta/TipoAlerta.java`, `backend/src/main/java/com/nexocriminal/domain/alerta/NivelRiesgo.java`, `backend/src/main/java/com/nexocriminal/domain/alerta/EstadoAlerta.java`, `backend/src/main/java/com/nexocriminal/domain/alerta/Alerta.java` |
| 87 | **John** | `backend/src/main/java/com/nexocriminal/domain/alerta/AlertaRepository.java`, `backend/src/main/java/com/nexocriminal/domain/alerta/AlertaService.java` |

### Tarea 3: Revisión y depuración de alertas por el analista

| # | Autor | Archivos |
|---|-------|----------|
| 88 | **John** | `backend/src/main/java/com/nexocriminal/alerta/domain/model/Alerta.java`, `backend/src/main/java/com/nexocriminal/alerta/domain/port/AlertaRepositoryPort.java` |
| 89 | **John** | `backend/src/main/java/com/nexocriminal/alerta/application/ListAlertas.java`, `backend/src/main/java/com/nexocriminal/alerta/application/ListAlertasPendientes.java`, `backend/src/main/java/com/nexocriminal/alerta/application/ChangeAlertaEstado.java` |
| 90 | **Manuel** | `backend/src/main/java/com/nexocriminal/alerta/infrastructure/persistence/AlertaMapper.java`, `backend/src/main/java/com/nexocriminal/alerta/infrastructure/persistence/AlertaRepositoryAdapter.java` |
| 91 | **Manuel** | `backend/src/main/java/com/nexocriminal/alerta/infrastructure/web/AlertaController.java`, `backend/src/main/java/com/nexocriminal/alerta/infrastructure/web/dto/AlertaResponse.java` |
| 92 | Santiago | `frontend/src/pages/Alertas.tsx` |

### Tarea 4: Visualización y exploración del grafo de relaciones

| # | Autor | Archivos |
|---|-------|----------|
| 93 | **Manuel** | `backend/src/main/java/com/nexocriminal/grafo/GrafoController.java` |
| 94 | **John** | `backend/src/main/java/com/nexocriminal/vinculo/domain/model/Vinculo.java`, `backend/src/main/java/com/nexocriminal/vinculo/domain/port/VinculoRepositoryPort.java` |
| 95 | **John** | `backend/src/main/java/com/nexocriminal/vinculo/application/ListVinculosActivos.java`, `backend/src/main/java/com/nexocriminal/vinculo/application/ListVinculosPorNodo.java` |
| 96 | **John** | `backend/src/main/java/com/nexocriminal/vinculo/infrastructure/persistence/VinculoMapper.java`, `backend/src/main/java/com/nexocriminal/vinculo/infrastructure/persistence/VinculoRepositoryAdapter.java` |
| 97 | **Manuel** | `backend/src/main/java/com/nexocriminal/vinculo/infrastructure/web/VinculoController.java`, `backend/src/main/java/com/nexocriminal/vinculo/infrastructure/web/dto/VinculoResponse.java` |

### Tarea 5: Filtros interactivos del grafo

| # | Autor | Archivos |
|---|-------|----------|
| 98 | **John** | `frontend/src/pages/Grafo.tsx` (implementar Cytoscape.js + layout) |
| 99 | Valeria | `frontend/src/pages/Grafo.tsx` (panel de filtros por tipo de nodo + toggle aristas) |

### Tarea 6: Identificación visual de nodos sospechosos

| # | Autor | Archivos |
|---|-------|----------|
| 100 | Santiago | `frontend/src/pages/Grafo.tsx` (estilo visual para nodos sospechosos + badges) |
| 101 | Valeria | `frontend/src/components/Modales.tsx` (panel de detalle al hacer clic en nodo) |

### Tarea 7: Ejecución del motor y actualización del grafo

| # | Autor | Archivos |
|---|-------|----------|
| 102 | **Manuel** | `backend/src/main/java/com/nexocriminal/engine/EngineController.java`, `backend/src/main/java/com/nexocriminal/config/ConfiguracionMotorController.java` |
| 103 | Isaac | `frontend/src/pages/Dashboard.tsx` (botón "Ejecutar Motor"), `frontend/src/pages/Grafo.tsx` (refrescar al ejecutar) |

### Tarea 8: Filtros de alertas por nivel de riesgo

| # | Autor | Archivos |
|---|-------|----------|
| 104 | **John** | `backend/src/main/java/com/nexocriminal/alerta/infrastructure/web/AlertaController.java` (GET con filtro por nivel de riesgo) |
| 105 | Santiago | `frontend/src/pages/Alertas.tsx` (filtros por nivel de riesgo en UI) |

### Tarea 9: Panel de resumen de alertas en el inicio

| # | Autor | Archivos |
|---|-------|----------|
| 106 | **Manuel** | `frontend/src/pages/Dashboard.tsx` (tarjetas de resumen de alertas pendientes) |
| 107 | **John** | `frontend/src/pages/Dashboard.tsx` (indicador de nivel de amenaza) |
| 108 | **Manuel** | `frontend/src/components/Modales.tsx` (modal de configuración del motor) |
| 109 | Valeria | `frontend/src/pages/Dashboard.tsx` (banner de ejecución del motor + última ejecución) |

---

## Sprint 4

### Tarea 1: Gestión de relaciones sociales

| # | Autor | Archivos |
|---|-------|----------|
| 110 | **Manuel** | `backend/src/main/java/com/nexocriminal/domain/relacion/TipoRelacion.java`, `backend/src/main/java/com/nexocriminal/domain/relacion/Relacion.java` |
| 111 | **Manuel** | `backend/src/main/java/com/nexocriminal/domain/relacion/RelacionRepository.java` |
| 112 | **John** | `backend/src/main/java/com/nexocriminal/domain/relacion/RelacionControllers.java` |
| 113 | **John** | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de relación) |
| 114 | **John** | `frontend/src/pages/Personas.tsx` (agregar panel de relaciones sociales en detalle) |

### Tarea 2: Módulo de modus operandi

| # | Autor | Archivos |
|---|-------|----------|
| 115 | **Manuel** | `backend/src/main/java/com/nexocriminal/modus/ModusOperandi.java`, `backend/src/main/java/com/nexocriminal/modus/ModusOperandiRepository.java` |
| 116 | **John** | `backend/src/main/java/com/nexocriminal/modus/ModusOperandiService.java`, `backend/src/main/java/com/nexocriminal/modus/ModusSeed.java` |
| 117 | **Manuel** | `backend/src/main/java/com/nexocriminal/modus/ModusOperandiController.java` |
| 118 | Isaac | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de modus operandi) |
| 119 | **John** | `frontend/src/pages/Sucesos.tsx` (agregar selector de modus operandi en formulario) |

### Tarea 3: Registro compuesto de robo completo

| # | Autor | Archivos |
|---|-------|----------|
| 120 | **Manuel** | `backend/src/main/java/com/nexocriminal/robo/RoboCompletoService.java` |
| 121 | **John** | `backend/src/main/java/com/nexocriminal/robo/RoboCompletoRequest.java`, `backend/src/main/java/com/nexocriminal/robo/RoboCompletoController.java` |
| 122 | **John** | `frontend/src/components/FormSucesoPorTipo.tsx` |
| 123 | Isaac | `frontend/src/components/BloqueRobo.tsx` |
| 124 | Santiago | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de robo) |

### Tarea 4: Gestión de testigos

| # | Autor | Archivos |
|---|-------|----------|
| 125 | **Manuel** | `backend/src/main/java/com/nexocriminal/testigo/SucesoTestigo.java`, `backend/src/main/java/com/nexocriminal/testigo/SucesoTestigoRepository.java` |
| 126 | **John** | `frontend/src/components/TestigosInput.tsx` |
| 127 | Isaac | `frontend/src/pages/Sucesos.tsx` (integrar testigos en formulario de creación) |
| 128 | Valeria | `frontend/src/components/BloqueSucesoSimple.tsx` |
| 129 | Valeria | `frontend/src/pages/Sucesos.tsx` (visualización de testigos en detalle del suceso) |

### Tarea 5: Búsqueda de intermediarios y refinamiento

| # | Autor | Archivos |
|---|-------|----------|
| 130 | **Manuel** | `backend/src/main/java/com/nexocriminal/persona/application/FindIntermediarios.java` |
| 131 | **John** | `backend/src/main/java/com/nexocriminal/persona/infrastructure/web/PersonaController.java` (agregar endpoint /intermediarios) |
| 132 | Santiago | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar), `frontend/src/pages/Personas.tsx` (panel de intermediarios) |
| 133 | Valeria | `frontend/src/components/BloqueDesaparicion.tsx` |

---

## Sprint 5

### Tarea 1: Búsqueda en fuentes externas (CNE y API Profesor)

| # | Autor | Archivos |
|---|-------|----------|
| 134 | **Manuel** | `backend/src/main/java/com/nexocriminal/fuentes/FuenteDatosPersona.java`, `backend/src/main/java/com/nexocriminal/fuentes/DatosPersonaExterna.java`, `backend/src/main/java/com/nexocriminal/fuentes/ModoFuente.java` |
| 135 | **John** | `backend/src/main/java/com/nexocriminal/fuentes/EstrategiaBusqueda.java`, `backend/src/main/java/com/nexocriminal/fuentes/adapter/CneScrapingAdapter.java` |
| 136 | **John** | `backend/src/main/java/com/nexocriminal/fuentes/adapter/ApiProfesorAdapter.java` |
| 137 | **Manuel** | `backend/src/main/java/com/nexocriminal/fuentes/config/FuentesDatosFactory.java` |
| 138 | **Manuel** | `backend/src/main/java/com/nexocriminal/fuentes/BuscadorPersonasService.java` |
| 139 | **John** | `backend/src/main/java/com/nexocriminal/fuentes/BuscadorPersonasController.java` |
| 140 | **Manuel** | `backend/src/main/java/com/nexocriminal/fuentes/strategy/AmbasStrategy.java`, `backend/src/main/java/com/nexocriminal/fuentes/strategy/SoloCneStrategy.java`, `backend/src/main/java/com/nexocriminal/fuentes/strategy/SoloApiStrategy.java` |
| 141 | Isaac | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con búsqueda externa) |
| 142 | Isaac | `frontend/src/pages/Personas.tsx` (agregar sección de búsqueda en fuentes externas) |
| 143 | **John** | `frontend/src/services/authMode.ts`, `frontend/src/services/ssoAuth.ts` |

### Tarea 2: Asistente IA con Claude

| # | Autor | Archivos |
|---|-------|----------|
| 144 | **John** | `backend/src/main/java/com/nexocriminal/ia/ClaudeClient.java`, `backend/src/main/java/com/nexocriminal/ia/MockClaudeClient.java` |
| 145 | **Manuel** | `backend/src/main/java/com/nexocriminal/ia/IAService.java` |
| 146 | **John** | `backend/src/main/java/com/nexocriminal/ia/dto/ChatRequest.java`, `backend/src/main/java/com/nexocriminal/ia/dto/MensajeChat.java`, `backend/src/main/java/com/nexocriminal/ia/dto/RespuestaIA.java` |
| 147 | **John** | `backend/src/main/java/com/nexocriminal/ia/IAController.java` |
| 148 | **Manuel** | `frontend/src/pages/AsistenteIA.tsx` |
| 149 | **John** | `frontend/src/components/BotonIA.tsx` |
| 150 | Santiago | `frontend/src/components/TextoIA.tsx` |
| 151 | Valeria | `frontend/src/pages/Alertas.tsx`, `frontend/src/pages/Desaparecidas.tsx` (integrar BotonIA en acciones) |
| 152 | Isaac | `frontend/src/services/api.ts`, `frontend/src/types/index.ts` (actualizar con tipos de IA) |

### Tarea 3: Integración y pulido final

| # | Autor | Archivos |
|---|-------|----------|
| 153 | **Manuel** | `frontend/src/services/usePaginacion.ts` |
| 154 | **John** | `frontend/src/components/TopBar.tsx` (agregar barra de búsqueda global) |
| 155 | Valeria | `frontend/src/components/Modales.tsx` (completar modales auxiliares restantes) |
| 156 | Santiago | `frontend/src/services/api.ts` (refactor final de servicios), `frontend/src/App.tsx` (rutas finales) |
| 157 | **Manuel** | `database/02-datos-ejemplo.sql` (actualizar con datos de ejemplo extendidos) |

---

## Resumen final

| Persona | Prerreqs | Sprint 1 | Sprint 2 | Sprint 3 | Sprint 4 | Sprint 5 | **Total** |
|---------|----------|----------|----------|----------|----------|----------|-----------|
| **Manuel** | 6 | 9 | 10 | 10 | 5 | 7 | **47** |
| **John** | 5 | 9 | 9 | 10 | 7 | 9 | **49** |
| Isaac | 3 | 4 | 5 | 4 | 3 | 4 | **23** |w
| Santiago | 3 | 2 | 3 | 3 | 2 | 3 | **16** |
| Valeria | 2 | 2 | 3 | 3 | 3 | 3 | **16** |

**Total commits: 157**

Manuel y John concentran ~61% de los commits, mientras que Isaac, Santiago y Valeria mantienen participaciones visibles. Esto simula un equipo donde Manuel (Tech Lead) y John (Senior Developer) cargan con la mayor parte del desarrollo, con contribuciones significativas de Isaac y participaciones menores pero constantes de Santiago y Valeria en componentes UI y tareas de integración.

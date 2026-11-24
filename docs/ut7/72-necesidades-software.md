# 7.2 Necesidades de software en entornos productivos

## Antes de elegir un software

En una empresa no se instala un programa "porque sí": hay que analizar varios aspectos antes de decidir.

| Área | Qué se revisa |
|---|---|
| Hardware | CPU, RAM, almacenamiento, GPU, red |
| Software y red | Compatibilidad con el SO, dependencias, acceso a internet |
| Organización y coste | Nº de usuarios, modelo de licencia, coste total de propiedad (TCO), formación, soporte, cumplimiento RGPD |

> [!NOTE]
> El **TCO (Total Cost of Ownership)** no es solo el precio de la licencia: incluye instalación, formación del personal, soporte técnico y mantenimiento a lo largo de los años.

También se distingue entre:

- **Requisitos funcionales**: qué debe hacer el programa.
- **Requisitos no funcionales**: cómo debe hacerlo (seguridad, usabilidad, compatibilidad, rendimiento, fiabilidad, mantenibilidad, portabilidad).

## "Primero estable, luego rápido"

En entornos de producción se prioriza la estabilidad sobre tener siempre la última versión:

- Se usan canales de soporte largo: **Ubuntu LTS**, **Debian Stable**, **Windows Enterprise LTSC**.
- Antes de actualizar en producción: probar el parche en un entorno de pruebas, hacer copia de seguridad, vigilar métricas tras el cambio, y tener un plan por si algo falla (backups, redundancia con RAID o réplicas, escalado).

## Software según tamaño de empresa y sector

| Tipo de organización | Software típico |
|---|---|
| Autónomo / microempresa | Aplicaciones SaaS |
| PYME | Sistemas modulares (facturación, inventario, CRM) |
| Gran empresa | ERP o software a medida |

Por sector cambia mucho la necesidad: una oficina necesita ofimática, un comercio necesita TPV y facturación electrónica, una fábrica necesita planificación de producción y CAD/CAM/SCADA, y un estudio de diseño necesita equipos con mucha GPU y RAM.

## Comprobar los requisitos desde la terminal

**En Linux:**

```bash
lscpu          # información de CPU
free -h        # memoria disponible
df -h          # espacio en disco
lsb_release -a # versión del sistema operativo
```

**En Windows (PowerShell):**

```powershell
Get-ComputerInfo | Select-Object OsName, OsVersion
Get-CimInstance Win32_Processor
Get-CimInstance Win32_LogicalDisk
```

> [!TIP]
> Antes de recomendar un programa, comprueba con estos comandos si el equipo cumple los requisitos mínimos **y** los recomendados. Instalar algo que solo cumple el mínimo suele dar problemas de rendimiento.

## Referencias

- Páginas oficiales de ciclo de vida de Ubuntu, Debian y Windows
- RGPD (Reglamento General de Protección de Datos)
- ISO/IEC/IEEE 29148, ISO/IEC 25010

# 7.1 Clasificación y licencias de software

## Objetivos del tema

Antes de instalar, recomendar o distribuir un programa en una empresa hay que saber dos cosas: **para qué sirve** y **qué se puede hacer legalmente con él**. Este tema repasa cómo se clasifica el software según su finalidad y qué tipos de licencia existen.

## 1. Clasificación según su propósito

El software se puede agrupar en tres grandes bloques:

- **Software de sistema**: gestiona el hardware y sirve de base para todo lo demás (sistemas operativos, controladores, firmware).
- **Software de programación**: herramientas para crear otro software (compiladores, IDEs, depuradores).
- **Software de aplicación**: programas pensados para que el usuario final resuelva una tarea concreta (ofimática, navegadores, editores de imagen...).

## 2. Licencias de software

Una **licencia** es el contrato que indica qué puede hacer el usuario con un programa: instalarlo, copiarlo, modificarlo, redistribuirlo, etc. Es importante no confundir **comprar una licencia de uso** con **ser propietario del software**: normalmente solo se adquiere el derecho de uso bajo unas condiciones (el típico **EULA**, *End User License Agreement*).

> [!WARNING]
> "Software libre" y "software gratis" (*freeware*) no son lo mismo. El software libre puede incluso venderse o tener soporte de pago; lo que lo define son las libertades que da al usuario, no el precio.

### 2.1 Las cuatro libertades del software libre

1. Libertad de **usar** el programa con cualquier propósito.
2. Libertad de **estudiarlo y modificarlo** (necesita acceso al código fuente).
3. Libertad de **redistribuir copias**.
4. Libertad de **distribuir versiones modificadas**.

A este conjunto de licencias también se le llama **FOSS/FLOSS** (*Free/Libre and Open Source Software*).

### 2.2 Espectro de licencias

No todo es "libre" o "privativo": existe un espectro con distintos niveles de restricción.

| Tipo de licencia | Acceso al código fuente | ¿Se puede modificar? | Ejemplo |
|---|---|---|---|
| Propietaria | No | No | Microsoft Office |
| Shareware | No (normalmente) | No | Versiones de prueba comerciales |
| Freeware | No | No | Adobe Acrobat Reader |
| Copyleft fuerte | Sí | Sí, pero las modificaciones deben compartirse igual | Linux (GPL) |
| Copyleft débil | Sí | Sí, con menos restricciones de redistribución | Firefox (MPL) |
| Permisiva | Sí | Sí, casi sin restricciones | Android (Apache) |
| Dominio público | Sí | Sí, sin ninguna restricción | SQLite |

### 2.3 Matices sobre modelos reales

- **Copyleft vs. permisivas**: el copyleft obliga a que las versiones derivadas mantengan la misma licencia; las permisivas no.
- **Doble licencia**: algunos proyectos se publican bajo dos licencias distintas según el uso que se le vaya a dar (por ejemplo, un producto como MySQL ofrece una vía libre y otra comercial; Android combina partes con licencias distintas).
- En España, los derechos de propiedad intelectual sobre un programa suelen proteger al autor durante toda su vida más un periodo adicional tras su fallecimiento, salvo que se ceda expresamente a un tercero (como la empresa para la que trabaja).

### 2.4 Licencias para documentación (Creative Commons)

Las licencias de software (GPL, MIT...) están pensadas para código fuente. Para documentos, imágenes o apuntes como los de este portfolio se usan licencias **Creative Commons (CC)**:

| Licencia CC | Uso comercial | Permite modificar | Obliga a compartir igual |
|---|---|---|---|
| CC BY | Sí | Sí | No |
| CC BY-SA | Sí | Sí | Sí |
| CC BY-NC | No | Sí | No |
| CC BY-ND | Sí | No | No |
| CC0 | Sí | Sí | No (dominio público) |

## 3. Comprobación práctica de licencias

Antes de usar un paquete en producción conviene comprobar su licencia desde la terminal.

**En Linux (Debian/Ubuntu):**

```bash
dpkg -s nombre-paquete
cat /usr/share/doc/nombre-paquete/copyright
```

**En Windows (PowerShell), con winget:**

```powershell
winget show nombre-paquete
```

> [!TIP]
> Si vas a recomendar un programa en un informe técnico, incluye siempre su licencia. Así quien lo lea sabe si puede instalarlo, modificarlo o redistribuirlo sin problemas legales.

## Referencias

- Free Software Foundation (FSF) / Proyecto GNU
- Open Source Initiative (OSI)
- SPDX License List
- Creative Commons
- Microsoft Learn (documentación de winget)

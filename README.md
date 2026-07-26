# Proyecto-Final-Control-Versiones
# Proyecto Final: Sistema Transaccional - Control de Versiones

## Descripción del Proyecto
Este proyecto documenta la evolución, control de versiones y gestión de incidencias en el desarrollo de la interfaz de inicio de sesión y validación de usuarios para el sistema transaccional. Se aborda la implementación de la autenticación en dos pasos (vía código SMS) y se documenta el flujo de recuperación frente a errores mediante la herramienta de reversión de versiones (`Revert`) de GitHub.

---

## Historial de Versiones del Proyecto

| Versión | Fecha | Autor | Descripción del cambio | Tipo de cambio | Aprobó |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **v1.0** | 15/07/2026 | Equipo | Creación de la estructura base de la interfaz de usuario `LoginView.java` | Inicial | Docente |
| **v1.9** | 20/07/2026 | Equipo | Ajustes de estilos y corrección de etiquetas de formulario | Mejora | Docente |
| **v2.0** | 26/07/2026 | Katy | Implementación del flujo de validación SMS y reversión de incidencias por error de digitación | Corrección / Nueva funcionalidad | Docente |

---

## Registro de Cambios (Detalle de Commits v2.0)

Para conservar la trazabilidad y la evidencia completa en el historial de Git, los cambios para la versión v2.0 se realizaron según el siguiente desglose:

| Código Versión | Fecha | Autor | Archivo | Cambio realizado | Motivo / Observación |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **v2.0a** | 26/07/2026 | Katy | `LoginView.java` | Agregar validación de formulario de login y redirección a vista de código SMS | Se introdujo un error de digitación que impidió la ejecución correcta del inicio de sesión. |
| **v2.0b** | 26/07/2026 | GitHub System / Katy | `LoginView.java` | *Revert* "Agregar validación de formulario de login" | Reversión automática mediante GitHub para restaurar la versión estable anterior sin alterar la historia. |
| **v2.0** | 26/07/2026 | Katy | `LoginView.java` | Reimplementación limpia de la validación del formulario y envío de código SMS | Restauración funcional y actualización completa de la documentación en el README.md. |

---

## Registro de Conflictos e Incidencias

| Fecha | Archivo | Descripción del conflicto / error | Solución aplicada | Responsable |
| :--- | :--- | :--- | :--- | :--- |
| **26/07/2026** | `LoginView.java` | Error de digitación en el commit *"Agregar validación de formulario de login"*, provocando que el inicio de sesión dejara de funcionar al probar la aplicación. | Se ejecutó la función **Revert** de GitHub sobre el commit conflictivo. Esto generó un nuevo commit de reversión que restauró el código anterior funcional y mantuvo la evidencia completa de la falla. | Katy |

---

## Registro de Recuperación de Versiones

| Versión recuperada | Fecha | Motivo de la recuperación |
| :--- | :--- | :--- |
| **v1.9** | 26/07/2026 | La versión v1.9 fue restaurada temporalmente mediante la opción *Revert* de GitHub tras el fallo generado por la sintaxis errónea en el commit de validación de formulario. |

---

## Estructura del Flujo de Autenticación (v2.0)

1. **Paso 1:** Validación de credenciales principales (`Login` y `Password`).
2. **Paso 2:** Solicitud e ingreso del código de seguridad enviado al teléfono móvil del usuario.
3. **Paso 3:** Acceso concedido al Dashboard del Sistema Transaccional.

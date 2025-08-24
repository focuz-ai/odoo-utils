# Odoo Utils - Módulos de Utilidades

## Descripción General

Esta colección contiene módulos de utilidades para Odoo 17.0 que añaden funcionalidades esenciales para mejorar la gestión de datos y la experiencia de usuario en Odoo.

## Módulos Disponibles

### 1. Partner VAT Unique
**Versión:** 17.0.1.0.0  
**Categoría:** Customer Relationship Management  
**Licencia:** AGPL-3  

#### Descripción
Módulo que garantiza la unicidad del número de identificación fiscal (VAT/RUC/NIT) para clientes y proveedores en el sistema. Los VATs vacíos no se consideran como duplicados.

#### Características Principales
- ✅ Validación automática de VAT único al crear o modificar contactos
- ✅ Prevención de duplicados de números fiscales
- ✅ Permite VATs vacíos sin restricciones
- ✅ Aplica tanto para clientes como proveedores

#### Casos de Uso
- Evitar la duplicación accidental de proveedores o clientes
- Garantizar la integridad de datos fiscales
- Cumplimiento de requisitos legales de identificación única
- Mejora en la calidad de datos maestros

#### Dependencias
- `base` (módulo base de Odoo)

---

### 2. Server Action Mass Edit (Mass Editing)
**Versión:** 17.0.1.0.2  
**Categoría:** Tools  
**Licencia:** AGPL-3  

#### Descripción
Este módulo permite editar múltiples registros simultáneamente en cualquier modelo de Odoo, proporcionando una herramienta poderosa para la actualización masiva de datos.

#### Características Principales
- ✅ Edición masiva de cualquier campo en cualquier modelo
- ✅ Interfaz intuitiva con popup de edición
- ✅ Acciones de establecer o eliminar valores
- ✅ Soporte para todos los tipos de campos de Odoo
- ✅ Configuración flexible por modelo
- ✅ Control de seguridad por grupos de usuarios

#### Funcionalidades
1. **Creación de Acciones Masivas**
   - Configurar acciones de edición masiva para modelos específicos
   - Seleccionar campos editables
   - Definir dominios para filtrar registros

2. **Tipos de Operaciones**
   - **Set**: Establecer un valor específico
   - **Remove**: Eliminar/limpiar el valor del campo

3. **Interfaz de Usuario**
   - Selección múltiple de registros desde vistas de lista
   - Popup de edición con campos configurados
   - Confirmación antes de aplicar cambios

#### Casos de Uso
- Actualización masiva de precios de productos
- Cambio de estado de múltiples documentos
- Asignación masiva de categorías o etiquetas
- Actualización de datos de contactos en lote
- Corrección de errores de datos históricos

#### Dependencias
- `base` (módulo base de Odoo)

#### Assets JavaScript
- Incluye componentes JavaScript personalizados para mejorar la experiencia de usuario en las vistas de lista y formularios

---

## Instalación

### Requisitos Previos
- Odoo 17.0 instalado y funcionando
- Acceso de administrador al sistema

### Pasos de Instalación

1. **Clonar o copiar los módulos**
   ```bash
   cd /path/to/odoo/addons
   git clone [repository-url] odoo-utils
   ```

2. **Actualizar la lista de módulos**
   - Ir a Aplicaciones en Odoo
   - Activar modo desarrollador
   - Actualizar lista de aplicaciones

3. **Instalar los módulos**
   - Buscar "Partner VAT Unique" o "Mass Editing"
   - Hacer clic en Instalar

## Configuración

### Partner VAT Unique
No requiere configuración adicional. El módulo funciona automáticamente después de la instalación.

### Server Action Mass Edit

1. **Crear una acción de edición masiva:**
   - Ir a Configuración → Técnico → Acciones → Acciones del servidor
   - Crear nueva acción
   - Tipo: "Mass Edit Records"
   - Seleccionar modelo objetivo
   - Configurar campos editables

2. **Asignar permisos:**
   - Configurar grupos de usuarios con acceso a las acciones masivas
   - Definir restricciones por modelo si es necesario

## Uso

### Partner VAT Unique
El módulo funciona de forma transparente:
- Al crear o editar un contacto con un VAT que ya existe, el sistema mostrará un error
- Los VATs vacíos están permitidos

### Server Action Mass Edit

1. Navegar a la vista de lista del modelo deseado
2. Seleccionar los registros a editar
3. Hacer clic en Acción → [Nombre de tu acción masiva]
4. En el popup, configurar los valores a establecer o eliminar
5. Confirmar los cambios

## Soporte Multi-idioma

Ambos módulos incluyen traducciones para múltiples idiomas:
- Español (es)
- Inglés (en)
- Francés (fr)
- Alemán (de)
- Italiano (it)
- Portugués (pt)
- Y muchos más...

## Contribuidores

### Partner VAT Unique
- Grant Thornton Spain - Ismael Calvo
- Manuel Calero - Tecnativa
- Odoo Community Association (OCA)

### Server Action Mass Edit
- Serpent Consulting Services Pvt. Ltd.
- Tecnativa
- GRAP
- Iván Todorovich
- Odoo Community Association (OCA)

## Licencia

Ambos módulos están licenciados bajo **AGPL-3.0** (GNU Affero General Public License v3.0)

## Enlaces de Interés

- **Partner VAT Unique**: https://github.com/OCA/partner-contact
- **Server Action Mass Edit**: https://github.com/OCA/server-ux

## Notas de Versión

### Partner VAT Unique v17.0.1.0.0
- Compatible con Odoo 17.0
- Estable para producción

### Server Action Mass Edit v17.0.1.0.2
- Compatible con Odoo 17.0
- Mejoras en la interfaz de usuario
- Correcciones de errores menores
- Assets JavaScript actualizados para Odoo 17

## Soporte y Contacto

Para reportar problemas o solicitar mejoras, por favor:
1. Abrir un issue en el repositorio correspondiente de GitHub
2. Contactar a los mantenedores a través de OCA

## Advertencias y Consideraciones

⚠️ **Importante para Server Action Mass Edit:**
- Las ediciones masivas no se pueden deshacer fácilmente
- Se recomienda hacer backup antes de operaciones masivas grandes
- Probar primero en entorno de desarrollo

⚠️ **Importante para Partner VAT Unique:**
- Si ya existen duplicados antes de instalar el módulo, deberán ser corregidos manualmente
- El módulo no valida el formato del VAT, solo su unicidad
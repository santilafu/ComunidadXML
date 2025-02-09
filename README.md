# ComunidadXML
Actividad Evaluacion Team 4 (Lenguaje de marcas) Aula Campus

# 📂 Sistema de Almacenamiento para Comunidad de Vecinos

Este proyecto consiste en la creación de un sistema de almacenamiento de usuarios para una comunidad de vecinos, utilizando **XML**, **DTD** y **XSD** para definir y validar la estructura de los datos.

Se han creado **dos archivos XML**:

1. **`comunidad.xml`** validado con **DTD (`comunidad.dtd`)**.
2. **`comunidad1.xml`** validado con **XSD (`comunidad.xsd`)** en **Notepad++**.

Cada archivo contiene información de los usuarios, incluyendo:

- **Nombre y apellidos**
- **Identificación** (DNI o NIF, permitiendo solo uno o ambos)
- **Teléfono** (formato internacional)
- **Correo electrónico**
- **Dirección** (portal, piso y letra)
- **Cuenta bancaria** (formato IBAN)
- **Cargo en la comunidad** (Presidente, Vicepresidente, Secretario, Vocal o Ninguno)

Para garantizar la correcta organización de los datos y el cumplimiento de las reglas establecidas, se han definido dos métodos de validación:

- **`comunidad.dtd`**: Define la estructura básica del documento XML.
- **`comunidad.xsd`**: Proporciona validaciones avanzadas, incluyendo restricciones en los valores y estructuras, validado en **Notepad++**.

---

## 📌 Validación del XML

### ✔️ Validación con DTD
Para verificar que el XML cumple con el **DTD**, puedes utilizar herramientas en línea como:

🔗 [XML Validation](https://www.xmlvalidation.com/)

O validar localmente con `xmllint` en Linux o macOS:
```bash
xmllint --noout --dtdvalid comunidad.dtd comunidad.xml
```

### ✔️ Validación con XSD en **Notepad++**
Para validar el **XSD** desde **Notepad++**, sigue estos pasos:

1. Asegúrate de tener instalados los complementos de **XML Tools**.
2. Abre `comunidad1.xml` en **Notepad++**.
3. Asegúrate de que el archivo contiene la referencia correcta al **XSD**:
   ```xml
   <comunidad xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="comunidad.xsd">
   ```
4. Ve a **Plugins** > **XML Tools** > **Validate Now** y selecciona `comunidad.xsd` como esquema.
5. Si el XML está bien estructurado, la validación confirmará que no hay errores.

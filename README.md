# ProcesoComprasSupermercadosMAXI

Archivos y evidencias de soporte para el proceso de compras de la empresa Supermercados MAXI, el cual, es un proyecto de automatización de procesos desarrollado mediante el software Bizagi Studio BPM.

Objetivo: automatizar el flujo de trabajo existente en el proceso de gestión de compras involucrando 4 áreas de negocio y entes externos a la compañía (proveedores)

Metodología: se desarrolla una aplicación de proceso BPM estructurada bajo los 6 pasos de automatización de procesos propuestos por el estándar BPM Bizagi. 

Funcionamiento: la solución consiste de 2 flujos de trabajo creados bajo la notación BPMN, 1 modelo de datos relacional alojado en SQL server 2017 con entidades transaccionales y de negocio, reglas de negocio desarrollados con el lenguaje Bizagi Expressions Language syntax, interfaz de usuario implementada mediante forms designer, servicios web SOA integrados mediante interfaces en tareas asíncronas, etc.

Alcance: el proceso gestiona las dinámicas e interacciones entre las áreas de gestión de compras, inventarios, adquisiciones y supervición. La solución no automatiza tareas manuales de revisión o actualización de inventarios ni contempla tareas realizadas por proveedores o agentes externos al modelo de datos estructurado.

Consideraciones:
-No se realiza configuración de notificaciones en los flujos dado que se trata de un proyecto local que no posee consola web. Por lo tanto, no hay configuración de notificaciones enviadas en ejecución.

-No se realiza configuración de asignación de tareas dado que es necesario poblar manualmente la entidad WFUSER para probar la lógica de asignación de usuarios. Se plantea la lógica de tener 4 roles/skills para cada area de negocio y manejar el método de asignación EVERYONE en las tareas de supervisión y validación.

-Es requerido poblar manualmente las entidades paramétricas pSucursal, pTipoCompra, pMonedaCompra, y WFUSER. Asimismo, las entidades de negocio: mInventarioProdsMAXI y mConvenioProveedores se deben poblar manualmente desde el proceso dado que su actualización no se encuentra automatizada en la solución propuesta. 

-Se encuentra pendiente revisar el mapeo del servicio encargado de generar la orden de compra. Se propone manejar la creación y mapeo de documentos mediante la funcionalidad "document templates" utilizando formatos predefinidos por la empresa. 

-La aplicación de proceso es creada en Bizagi Studio 11.2.51034 Non Portable proyecto local




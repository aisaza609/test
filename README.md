# Descripción del Proyecto
 
En Colombia, el sistema de salud enfrenta desafíos significativos en la continuidad de la atención médica, especialmente en zonas rurales donde la infraestructura y el personal son limitados. Los pacientes que requieren atención especializada suelen ser trasladados a hospitales de mayor nivel, ubicados en zonas urbanas, lo que incrementa los tiempos de espera y pone en riesgo su salud debido a la falta de interoperabilidad en la información clínica entre instituciones.

Nuestro proyecto propone una solución innovadora basada en tecnología blockchain para mejorar la interoperabilidad de Historias Clínicas Electrónicas (HCE) entre hospitales y clínicas en Colombia. Con esta red blockchain, se garantiza que la historia clínica de cada paciente esté disponible en tiempo real, accesible de forma segura y sin duplicación, independientemente de la ubicación geográfica de las instituciones de salud. La solución incluye un modelo predictivo que, a partir del análisis de datos en tiempo real, dirige a los pacientes al hospital más adecuado según su estado de salud y su EPS, asegurando así una atención continua y de calidad.

Esta plataforma no solo optimiza los traslados y la asignación de recursos médicos, sino que también reduce errores y mejora la seguridad en el manejo de información clínica, ofreciendo una solución escalable y adaptable a las necesidades del sistema de salud colombiano.

# Arquitectura de la Solución

La solución propuesta se basa en una red **blockchain** que permite la interoperabilidad entre diferentes hospitales y clínicas en Colombia, asegurando que la información clínica de los pacientes esté disponible en tiempo real y de manera segura. Esta red blockchain está diseñada para almacenar y compartir las Historias Clínicas Electrónicas (HCE) de los pacientes entre instituciones de salud de distintos niveles de atención.

Para validar la funcionalidad y efectividad de la solución, se ha implementado una **simulación** utilizando datos de **3 hospitales** con diferentes niveles de atención. La arquitectura de la solución incluye los siguientes componentes clave:

1. **Red Blockchain para Interoperabilidad**:
   - **Propósito**: Facilitar el intercambio de HCE entre hospitales y clínicas de forma segura y descentralizada.
   - **Funcionamiento**: Cada registro de paciente en la red es único y no puede ser alterado, garantizando la integridad de la información.
   - **Protocolos de Consenso**: La red utiliza protocolos de consenso para validar la autenticidad de los datos, asegurando que solo entidades autorizadas (IPS, EPS y otros actores del sistema de salud) puedan acceder y actualizar la información.

2. **Simulación de los 3 Hospitales**:
   - **Distribución por Niveles de Atención**: Los hospitales simulados representan distintos niveles de atención (niveles 1, 2 y 3), lo cual permite observar el flujo y manejo de pacientes de acuerdo con la gravedad de sus condiciones y la disponibilidad de recursos.
   - **Datos Utilizados**: La simulación emplea datos reales obtenidos de fuentes de datos abiertos y del **Registro Especial de Prestadores de Servicios de Salud (REPS)** de MinSalud, lo cual permite asignar correctamente el nivel hospitalario y evaluar la interoperabilidad de la red blockchain.
   - **Interacción en la Red**: A través de la simulación, los hospitales pueden intercambiar información sobre el estado de salud del paciente y su historia clínica. Si un hospital de nivel 1 recibe a un paciente en estado crítico, el modelo predictivo recomienda un traslado a un hospital de mayor nivel que cuente con los recursos necesarios.

3. **Modelos Predictivo y Descriptivo en Tiempo Real**:
   - **Modelo Descriptivo**: Se desarrolló un modelo descriptivo para evaluar la cantidad de pacientes que requerían traslados según su EPS y el nivel de atención necesario. Este análisis se llevó a cabo usando datos de dos hospitales específicos, permitiendo identificar patrones en la demanda de atención de mayor complejidad.
   - **Modelo Predictivo**: Analiza en tiempo real las necesidades de cada paciente, evaluando factores como su estado de salud actual, el tipo de atención requerida, y su EPS, para direccionarlo al hospital adecuado.
   - **Integración con Blockchain**: Los resultados de ambos modelos se registran en la blockchain, asegurando que los datos de traslado y atención estén disponibles y sean confiables para todos los actores del sistema.
   - **Optimización de Recursos**: Estos modelos permiten a los hospitales anticiparse a la recepción de pacientes, optimizando el uso de recursos médicos y reduciendo el tiempo de espera para los pacientes.


4. **Módulo de Seguridad y Autenticación**:
   - **Acceso Controlado**: La red blockchain emplea un sistema de autenticación robusto, donde solo instituciones verificadas pueden acceder a las HCE, esa informacion en sacada de datos de minsalu, encontada tambien en el github `Datasets externos/Prestadores_Reps.csv`
   - **Protección de Datos**: La blockchain protege los datos del paciente contra modificaciones no autorizadas, reduciendo el riesgo de pérdida de información durante los traslados.

# Modelos Descriptivo y Predictivo

Nuestra solución incorpora dos modelos clave para analizar y optimizar el flujo de pacientes en el sistema de salud, aunque sólo el modelo predictivo se integra en la red blockchain:

1. **Modelo Descriptivo**:
   - **Propósito**: Este modelo se desarrolló para evaluar la magnitud de la problemática, específicamente en cuanto a la cantidad de pacientes que requieren traslados según su EPS y el nivel de atención necesario. Se realizó un análisis de datos de dos hospitales, lo cual permite entender patrones en la demanda de atención de mayor complejidad y medir el impacto de la falta de recursos en la continuidad de la atención.
   - **Métodos y Métricas**: A través de un análisis estadístico de los datos históricos, el modelo descriptivo mide la frecuencia de traslados y la correlación entre la EPS del paciente y los niveles de atención requeridos. Las métricas clave incluyen el porcentaje de pacientes trasladados y las especialidades con mayor demanda de traslado, proporcionando una visión detallada del problema.
   - **Nota Importante**: Este modelo es solo para análisis y comprensión del contexto; **no se incorpora en la red blockchain**, ya que su propósito es explorar la magnitud de la situación actual.
   - **Repositorio**: Puedes encontrar el modelo descriptivo en el archivo de GitHub titulado `Analisis_Descriptivo_de_Traslados_en_los_Hospitales.ipynb`.

2. **Modelo Predictivo**:
   - **Propósito**: Basado en datos de tres hospitales, este modelo predictivo se integra en la red blockchain y analiza en tiempo real las necesidades de cada paciente. Su objetivo es sugerir el hospital adecuado para su traslado según su estado de salud, nivel de atención requerido y su EPS.
   - **Métodos y Métricas**: el modelo predictivo evalúa la probabilidad de que un paciente requiera traslado, priorizando aquellos en estado crítico, para ello tambien usamos el dataset de los codigos diagnosticos `` Las métricas clave incluyen precisión en la asignación del hospital adecuado y tiempos estimados de traslado, mejorando la eficacia en la respuesta de atención médica.
   - **Impacto**: Este modelo optimiza los traslados y reduce los tiempos de espera, asegurando que cada paciente reciba la atención correcta en el hospital que cuenta con los recursos necesarios para su condición, mejorando así la continuidad y calidad de la atención en el sistema de salud.






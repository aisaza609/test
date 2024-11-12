# Descripción del Proyecto

En Colombia, el sistema de salud enfrenta desafíos significativos en la continuidad de la atención médica, especialmente en zonas rurales donde la infraestructura y el personal son limitados. Los pacientes que requieren atención especializada suelen ser trasladados a hospitales de mayor nivel, ubicados en zonas urbanas, lo que incrementa los tiempos de espera y pone en riesgo su salud debido a la falta de interoperabilidad en la información clínica entre instituciones.

Nuestro proyecto propone una solución basada en tecnología blockchain para mejorar la interoperabilidad de Historias Clínicas Electrónicas (HCE) entre hospitales y clínicas en Colombia. Con esta red blockchain, se garantiza que la historia clínica de cada paciente esté disponible en tiempo real, accesible de forma segura y sin duplicación, independientemente de la ubicación geográfica de las instituciones de salud. La solución incluye un sistema de recomendación que, a partir del análisis de datos, sugiere el hospital más adecuado según el estado de salud del paciente y su EPS, asegurando una atención continua y de calidad.

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
   - **Interacción en la Red**: A través de la simulación, los hospitales pueden intercambiar información sobre el estado de salud del paciente y su historia clínica. Si un hospital de nivel 1 recibe a un paciente en estado crítico, el sistema de recomendación sugiere el traslado a un hospital de mayor nivel que cuente con los recursos necesarios.

3. **Sistema de Recomendación en Tiempo Real**:
   - **Propósito**: Evaluar en tiempo real el estado de cada paciente y sugerir el hospital más adecuado para su traslado, tomando en cuenta factores como su estado de salud, el tipo de atención requerida y su EPS.
   - **Métodos y Métricas**: Basado en reglas preestablecidas y datos históricos, el sistema de recomendación calcula el nivel de atención necesario y selecciona el hospital que cumple con esos requisitos, priorizando aquellos en estado crítico. Las métricas clave incluyen precisión en la asignación del hospital adecuado y tiempos estimados de traslado, mejorando la respuesta en la atención médica.
   - **Impacto**: Este sistema optimiza los traslados y reduce los tiempos de espera, asegurando que cada paciente reciba la atención correcta en el hospital que cuenta con los recursos necesarios para su condición, mejorando así la continuidad y calidad de la atención en el sistema de salud.

4. **Módulo de Seguridad y Autenticación**:
   - **Acceso Controlado**: La red blockchain emplea un sistema de autenticación robusto, donde solo instituciones verificadas pueden acceder a las HCE, con información sacada de datos de MinSalud y disponible en el archivo `Datasets externos/Prestadores_Reps.csv` en GitHub.
   - **Protección de Datos**: La blockchain protege los datos del paciente contra modificaciones no autorizadas, reduciendo el riesgo de pérdida de información durante los traslados.

# Sistema de Recomendación y Analisis Descritivo

Nuestra solución incorpora un sistema de recomendación para analizar y optimizar el flujo de pacientes en el sistema de salud:

1. **Sistema Descriptivo**:
   - **Propósito**: Evaluar la magnitud de la problemática en cuanto a la cantidad de pacientes que requieren traslados según su EPS y el nivel de atención necesario. Se realizó un análisis de datos de dos hospitales para entender patrones en la demanda de atención de mayor complejidad y medir el impacto de la falta de recursos en la continuidad de la atención.
   - **Métodos y Métricas**: A través de un análisis estadístico de los datos históricos, se mide la frecuencia de traslados y la correlación entre la EPS del paciente y los niveles de atención requeridos. Las métricas clave incluyen el porcentaje de pacientes trasladados y las especialidades con mayor demanda de traslado, proporcionando una visión detallada del problema.
   - **Nota Importante**: Este análisis es solo para entender el contexto; **no se incorpora en la red blockchain**, ya que su propósito es explorar la magnitud de la situación actual.
   - **Repositorio**: Puedes encontrar el análisis descriptivo en el archivo de GitHub titulado `Analisis_Descriptivo_de_Traslados_en_los_Hospitales.ipynb`.

2. **Sistema de Recomendación**:
   - **Propósito**: Basado en datos de tres hospitales, este sistema de recomendación se integra en la red blockchain y analiza en tiempo real las necesidades de cada paciente. Su objetivo es sugerir el hospital adecuado para su traslado según su estado de salud, nivel de atención requerido y su EPS.
   - **Métodos y Métricas**: El sistema evalúa la necesidad de traslado de cada paciente y selecciona el hospital que mejor cumpla con sus requerimientos. Las métricas clave incluyen precisión en la asignación del hospital adecuado y tiempos estimados de traslado.
   - **Impacto**: Este sistema optimiza los traslados y reduce los tiempos de espera, asegurando que cada paciente reciba la atención correcta en el hospital con los recursos necesarios, mejorando la continuidad y calidad de la atención.

# Dapp de Blockchain

# Datos Utilizados 

# Requisitos de Software y Herramientas

# Instrucciones de Instalación y Ejecución






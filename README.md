IA-HAR
as metodologías tradicionales de medición y conciliación volumétrica en tanques (estática), patines de medición e instalaciones de separación (dinámica) operan con desfases temporales (batching), dependencia de registros manuales y margen de error por variaciones termo-fisicoquímicas no capturadas a tiempo.

Además, que el sector de hidrocarburos en México a través del Servicio de Administración Tributaria (SAT) exige que las empresas de hidrocarburos cumplan con estrictos lineamientos de medición, registro, conciliación y trazabilidad de volúmenes en todas las etapas de la cadena: extracción, transporte, almacenamiento y comercialización.

Debido a que hay varias problemáticas que se requieren atender es posible proponer, más allá de una única solución, una plataforma digital integral constituida por módulos. En tal sentido se hablará del IA-HAR (Artifitial Intelligence to Hydrocarbon Accounting & Reconciliation).

AI HAR es una iniciativa estratégica diseñada para transformar la gestión volumétrica y la integridad fiscal en operaciones de hidrocarburos mediante el uso de Inteligencia Artificial Multimodal, cumpliendo de forma estricta los lineamientos del SAT (Anexo 30/31). El proyecto responde a una necesidad crítica del sector: garantizar mediciones confiables, trazabilidad completa y conciliaciones automáticas que eliminen riesgos fiscales, operativos y reputacionales


Nombre del proyecto: IA-HAR (Artifitial Intelligence to Hydrocarbon Accounting & Reconciliation).

Objetivo general: Desarrollar y evaluar modelos que permitan: Modelos de Machine Learning para detección de anomalías volumétricas (fugas, desviaciones, pérdidas no técnicas). IA generativa para conciliación automática de reportes SAT, generando explicaciones y trazabilidad de cada ajuste. Vision Computacional para validar lecturas de instrumentos (medidores, manómetros, indicadores analógicos).

Contexto general: Los instrumentos normativos clave son: • Anexo 30 – Estándares de medición y control volumétrico Establece cómo deben capturarse, transmitirse y resguardarse los datos de medición (caudal, presión, temperatura, densidad, factor de corrección, etc.). • Anexo 31 – Reportes electrónicos y trazabilidad fiscal Define los formatos XML, periodicidad, validaciones y auditorías para garantizar integridad fiscal y evitar pérdidas no técnicas.

Enfoque de Inteligencia Artificial:

Detección de Anomalías Volumétricas (distilbert-base-uncased) Criterio Técnico: Arquitectura basada en Transformers livianos (38% menos parámetros que BERT original) optimizada para inferencia ultrarrápida. Justificación Operativa: En el monitoreo de flujos y presiones en ductos o tanques, el volumen de datos de telemetría es masivo. Se priorizó una baja latencia en GPU para detectar desviaciones o fugas en tiempo real sin saturar los recursos de cómputo.

Conciliación y Auditoría Fiscal SAT (google/flan-t5-base) Criterio Técnico: Modelo Encoder-Decoder ajustado por instrucciones (Instruction-tuned LLM), especializado en razonamiento, síntesis y seguimiento de reglas complejas en texto. Justificación Operativa: La conciliación volumétrica requiere auditar discrepancias entre reportes contables y normativas del SAT. Se seleccionó por su capacidad para generar explicaciones legibles, trazables y clasificar inconformidades, sacrificando latencia en favor de interpretabilidad y precisión conceptual.

Validación Visual de Instrumentos (google/vit-base-patch16-224) Criterio Técnico: Modelo de Vision Transformer (ViT) de última generación que segmenta la imagen en parches de 16x16 píxeles, superando a las CNNs tradicionales en captura de contexto global. Justificación Operativa: En la validación de manómetros, medidores e indicadores analógicos en campo, se requiere alta robustez ante cambios de iluminación o textura. Se eligió por su alto desempeño (F1"-score" ) en tareas de clasificación y verificación visual con tiempos de procesamiento viables para inspecciones en borde.

Tecnologías utilizadas
Lenguaje de programación: • Python 3.12.12

Librerías principales: • Pandas 2.2.2, • Transformers (Hugging Face) • Scikit-learn • Datasets (Hugging Face)

Herramientas de desarrollo: • Google Colab • GPU NVIDIA T4 • Hugging Face Hub


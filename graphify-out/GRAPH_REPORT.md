# Graph Report - .  (2026-09-16)

## Corpus Check
- 75 files · ~437,512 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 441 nodes · 581 edges · 43 communities (26 shown, 17 thin omitted)
- Extraction: 81% EXTRACTED · 19% INFERRED · 1% AMBIGUOUS · INFERRED: 109 edges (avg confidence: 0.8)
- Token cost: 1,055,470 input · 186,256 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Bell & Weaver Farm Operations Chapters|Bell & Weaver: Farm Operations Chapters]]
- [[_COMMUNITY_NidoSmart Business Overview|NidoSmart Business Overview]]
- [[_COMMUNITY_Automation & Housing Design|Automation & Housing Design]]
- [[_COMMUNITY_Project Structure & Indexes|Project Structure & Indexes]]
- [[_COMMUNITY_Genetic Line Performance Standards|Genetic Line Performance Standards]]
- [[_COMMUNITY_Layer vs Broiler Decision & Vendors|Layer vs Broiler Decision & Vendors]]
- [[_COMMUNITY_Hot-Climate Housing Science|Hot-Climate Housing Science]]
- [[_COMMUNITY_FamTECH Cage Quotation Line Items|FamTECH Cage Quotation Line Items]]
- [[_COMMUNITY_640-Bird Scope Freeze & Investment|640-Bird Scope Freeze & Investment]]
- [[_COMMUNITY_Nave & Vehicle Open Specs|Nave & Vehicle Open Specs]]
- [[_COMMUNITY_Egg Safety Regulation (NOM-159)|Egg Safety Regulation (NOM-159)]]
- [[_COMMUNITY_Farm Financial Planning Methods|Farm Financial Planning Methods]]
- [[_COMMUNITY_Risk Management & AI Agents|Risk Management & AI Agents]]
- [[_COMMUNITY_Technology-First Investment Strategy|Technology-First Investment Strategy]]
- [[_COMMUNITY_Commercial Strategy & Pilot Economics|Commercial Strategy & Pilot Economics]]
- [[_COMMUNITY_Financial Plan Scale Economics|Financial Plan: Scale Economics]]
- [[_COMMUNITY_Growth Roadmap Phases|Growth Roadmap Phases]]
- [[_COMMUNITY_Pilot Validation Criteria|Pilot Validation Criteria]]
- [[_COMMUNITY_Biosecurity & Org Roles|Biosecurity & Org Roles]]
- [[_COMMUNITY_FamTECH Equipment Concepts|FamTECH Equipment Concepts]]
- [[_COMMUNITY_Installation Photo Cage Row Setup|Installation Photo: Cage Row Setup]]
- [[_COMMUNITY_Installation Photo Cage Interior|Installation Photo: Cage Interior]]
- [[_COMMUNITY_Installation Photo Egg Elevator|Installation Photo: Egg Elevator]]
- [[_COMMUNITY_Regulatory Bodies & Compliance|Regulatory Bodies & Compliance]]
- [[_COMMUNITY_Pilot-to-Expansion Criteria|Pilot-to-Expansion Criteria]]
- [[_COMMUNITY_ABC Machinery Branding|ABC Machinery Branding]]
- [[_COMMUNITY_Market & Location|Market & Location]]
- [[_COMMUNITY_Site Layout & Flow|Site Layout & Flow]]
- [[_COMMUNITY_Vehicle Fuel & Routes (Pending)|Vehicle Fuel & Routes (Pending)]]
- [[_COMMUNITY_Budget Cage Line Item|Budget: Cage Line Item]]
- [[_COMMUNITY_Email Thread Artifact|Email Thread Artifact]]
- [[_COMMUNITY_Egg Packaging Standard|Egg Packaging Standard]]
- [[_COMMUNITY_NOM-159 Reference|NOM-159 Reference]]
- [[_COMMUNITY_Immediate Next Steps|Immediate Next Steps]]
- [[_COMMUNITY_Environmental KPIs|Environmental KPIs]]
- [[_COMMUNITY_Commercial KPIs|Commercial KPIs]]
- [[_COMMUNITY_Technical KPIs|Technical KPIs]]
- [[_COMMUNITY_Operations Role|Operations Role]]
- [[_COMMUNITY_External Vet Role|External Vet Role]]
- [[_COMMUNITY_Project Naming Decision|Project Naming Decision]]
- [[_COMMUNITY_Modular Growth Decision|Modular Growth Decision]]
- [[_COMMUNITY_Automation Coverage Decision|Automation Coverage Decision]]
- [[_COMMUNITY_Optional Environmental Control Package|Optional Environmental Control Package]]

## God Nodes (most connected - your core abstractions)
1. `Fuentes técnicas de referencia` - 21 edges
2. `Chapter 52: Cage Management for Layers` - 18 edges
3. `Hermes Agent` - 17 edges
4. `Manual de Buenas Practicas Pecuarias en la Produccion de Huevo para Plato (SENASICA, 3a Ed. 2019)` - 17 edges
5. `Índice general del plan de negocios` - 14 edges
6. `Índice de Innovación e I+D` - 14 edges
7. `Knowledge Base` - 14 edges
8. `Chapter 5: Poultry Housing for Hot Climates` - 14 edges
9. `NOM-159-SSA1-2016 (Egg products, sanitary specifications)` - 11 edges
10. `FamTECH Quotation v1 (CIF Puebla, USD17,747)` - 10 edges

## Surprising Connections (you probably didn't know these)
- `Clasificación Adoptar / Adaptar / Investigar` --semantically_similar_to--> `Clasificación de fuentes por tipo de autoridad`  [INFERRED] [semantically similar]
  research/README.md → knowledge-base/README.md
- `docs/innovation contiene conclusiones propias, no es biblioteca de referencias` --semantically_similar_to--> `Separación entre conocimiento de terceros (knowledge-base) y producido por NidoSmart (docs)`  [INFERRED] [semantically similar]
  docs/innovation/README.md → knowledge-base/README.md
- `Separación entre datos crudos y su análisis derivado` --semantically_similar_to--> `Separación entre conocimiento de terceros (knowledge-base) y producido por NidoSmart (docs)`  [INFERRED] [semantically similar]
  data/README.md → knowledge-base/README.md
- `Nipple Drinking System (dosing pump, waterline, nipples; subtotal USD903.8)` --conceptually_related_to--> `Water for bird consumption (potability, tank/cistern cleaning program, section 4)`  [INFERRED]
  evidence/quotations/2026-07-21_FamTECH_v1_Jaula-Automatizacion_CIF-Puebla_USD17747.pdf → knowledge-base/regulations/buenas-practicas-huevo.pdf
- `Automatic Egg Collecting Machine (soft-shell separator, PP belt, drive unit; subtotal USD3,272.6)` --conceptually_related_to--> `Egg collection and selection (automatic belt vs manual collection, section 2.8)`  [INFERRED]
  evidence/quotations/2026-07-21_FamTECH_v1_Jaula-Automatizacion_CIF-Puebla_USD17747.pdf → knowledge-base/regulations/buenas-practicas-huevo.pdf

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Definición cotizada de la unidad productiva de 640 aves** — business_plan_07_diseno_fisico_modulo_inicial, business_plan_07_diseno_fisico_jaula_tipo_h, business_plan_07_diseno_fisico_famtech, quotations_readme [INFERRED 0.85]
- **Jerarquía tecnológica: control crítico local + capa de inteligencia** — business_plan_10_arquitectura_tecnologica_plc, business_plan_10_arquitectura_tecnologica_arquitectura_propuesta, business_plan_11_hermes_agent_y_paperclip_hermes_agent, business_plan_11_hermes_agent_y_paperclip_paperclip [EXTRACTED 1.00]
- **Requisito de conectividad permanente para la capa de datos e IA** — business_plan_09_arquitectura_electrica_hidraulica_comunicaciones_conectividad_internet, business_plan_09_arquitectura_electrica_hidraulica_comunicaciones_starlink, business_plan_11_hermes_agent_y_paperclip_hermes_agent, business_plan_11_hermes_agent_y_paperclip_paperclip [EXTRACTED 1.00]
- **Validación integral de la primera unidad de 640 aves (producción, finanzas, piloto)** — business_plan_16_produccion_y_capacidad_comercial_estimacion_produccion_640_aves, business_plan_17_plan_financiero_proyeccion_financiera_primera_unidad, business_plan_18_validacion_del_piloto_objetivo_financiero_validacion_piloto [INFERRED 0.85]
- **Secuencia de desarrollo tecnológico dentro de la Fase 1 de la hoja de ruta** — business_plan_22_desarrollo_tecnologico_secuencia_desarrollo_tecnologico, business_plan_23_hoja_de_ruta_fase_1_infraestructura_base, business_plan_22_desarrollo_tecnologico_nidosmart_core [EXTRACTED 1.00]
- **Decisiones estratégicas registradas que sustentan el enfoque del piloto y de la tecnología** — business_plan_18_validacion_del_piloto_objetivo_financiero_validacion_piloto, business_plan_22_desarrollo_tecnologico_enfoque_technology_first_business_validated, governance_registro_de_decisiones_registro [INFERRED 0.75]
- **Definición del alcance de inversión congelado en 640 aves** — governance_registro_de_decisiones_dec_012, investment_project_01_proyecto_de_inversion_unidad_640_aves, investment_project_05_ficha_tecnica_nave_doc, investment_project_07_presupuesto_consolidado_inversion_inicial_doc [INFERRED 0.85]
- **Decisiones de inversión diferidas hasta validación (vehículo, obra civil, control ambiental)** — investment_project_06_vehiculo_de_distribucion_forma_adquisicion, investment_project_05_ficha_tecnica_nave_estado_ficha, investment_project_01_proyecto_de_inversion_control_ambiental_opcional [INFERRED 0.75]
- **Jerarquía tecnológica: control crítico, IA asistente y elección de agente** — governance_registro_de_decisiones_dec_007, governance_registro_de_decisiones_dec_008, governance_registro_de_decisiones_dec_009 [INFERRED 0.85]
- **Cadena de trazabilidad: fuente → análisis → decisión → documento** — knowledge_base_readme, data_readme, evidence_dir, research_readme, models_dir, innovation_readme [EXTRACTED 1.00]
- **Flujo ejemplo: papers de anomalías → literature notes → estado del arte → línea de investigación** — knowledge_base_papers_anomaly_detection, research_literature_notes, state_of_the_art_05_anomaly_detection, innovation_03_lineas_de_investigacion [EXTRACTED 1.00]
- **Patrón: separar material crudo/externo del conocimiento derivado propio** — data_readme_raw_vs_analysis, knowledge_base_readme_raw_vs_produced, innovation_readme_conclusions_not_library [INFERRED 0.80]
- **FamTECH Quotation Version Family (v1/v2/v3)** — quotations_famtech_v1_document, quotations_famtech_v2_document, quotations_famtech_v3_document, quotations_famtech_v1_famtech [EXTRACTED 1.00]
- **Mexican Egg Production Regulatory Compliance Context** — regulations_nom_159_ssa1_2016_document, regulations_buenas_practicas_huevo_document, quotations_famtech_v1_layer_cage_system, quotations_famtech_v1_egg_collecting_system [INFERRED 0.75]
- **Layer Housing Density and Welfare Standards** — regulations_buenas_practicas_huevo_produccion_density, genetics_hy_line_w80_space_recommendations, quotations_famtech_v1_layer_cage_system, regulations_buenas_practicas_huevo_bienestar_calificacion_corporal [INFERRED 0.75]

## Communities (43 total, 17 thin omitted)

### Community 0 - "Bell & Weaver: Farm Operations Chapters"
Cohesion: 0.06
Nodes (48): Ahemeral 28-Hour Lighting Program (14 Hours Light, 14 Hours Dark) for Egg Strains, Chapter 10: Fundamentals of Managing Light for Poultry, Chapter 11: Waste Management, Chapter 12: External Parasites, Insects, and Rodents, Chapter 17: Feeding Egg-Type Replacement Pullets, Chapter 18: Feeding Commercial Egg-Type Layers, Chapter 20: Vitamins, Minerals, and Trace Ingredients, Chapter 22: Consumption and Quality of Water (+40 more)

### Community 1 - "NidoSmart Business Overview"
Cohesion: 0.05
Nodes (48): Automatización intensiva (>90%), Crecimiento modular, Escala objetivo de largo plazo (5,000 aves), Estrategia comercial (venta directa, suscripciones), Inversión preliminar ($723,300-$1,174,300 MXN), NidoSmart, Primera unidad productiva (640 aves), Segunda unidad (1,280 aves) (+40 more)

### Community 2 - "Automation & Housing Design"
Cohesion: 0.06
Nodes (47): Base de datos local de series de tiempo, Gateway industrial y Node-RED, Conectividad a internet permanente para datos e IA, Control crítico local sin internet, Aislamiento térmico de la nave (vs. calefacción auxiliar), Bell & Weaver - Commercial Chicken Meat and Egg Production, Condiciones climáticas del sitio (altiplano poblano), Automatización de agua (+39 more)

### Community 3 - "Project Structure & Indexes"
Cohesion: 0.07
Nodes (43): Índice del plan de negocios, data/experimental/, data/external/, Data, Separación entre datos crudos y su análisis derivado, docs/governance/, evidence/, Estrategia de I+D (+35 more)

### Community 4 - "Genetic Line Performance Standards"
Cohesion: 0.08
Nodes (31): Body weight curve (1212-1269g at 17wk; 1646-1783g at 100wk), Hy-Line W-80 Commercial Layers Performance Guide (April 2026), Egg size distribution (avg 64.9g at 100wk; 66.3% grande), Lighting program (ascending to 15-16h at peak, stimulate at 1180-1230g body weight), Nutritional recommendations (energy 2900-3100 kcal/kg initiation; calcium up to 4.60g/day at 86+wk), Performance standard summary (peak 94.4-98.2%; eggs 471.9-491.2 at 100wk; egg mass 30.3kg; FCR 1.94-2.01), Production space recommendations (490 cm2/bird, conventional cages, 20-80wk), Water quality standards (nitrate max 25ppm, pH 5-7, coliforms 0 CFU/mL) (+23 more)

### Community 5 - "Layer vs Broiler Decision & Vendors"
Cohesion: 0.07
Nodes (30): Comparación ponedoras vs pollo de engorda, Decisión: iniciar con gallinas ponedoras, Pollitas de prepostura (16-18 semanas), Registro de decisiones, Decisiones candidatas no confirmadas (broilers; muda/reciclaje de parvada), DEC-002: Inicio con gallinas ponedoras y no con pollo de engorda, Fuentes técnicas de referencia, Big Dutchman (+22 more)

### Community 6 - "Hot-Climate Housing Science"
Cohesion: 0.19
Nodes (19): Bird Heat Loss Mechanisms (Sensible vs Latent, Fig. 5.1), Poultry Production in Hot Climates (2nd Edition), Cage-to-Ceiling Clearance Threshold (Less Than 1 m Impairs Natural Ventilation), Minimum 1.2 m Centre Aisle Width for 3-4 Tier Cage Houses, Chapter 4: Behavioural, Physiological, Neuroendocrine and Molecular Responses to Heat Stress, Chapter 5: Poultry Housing for Hot Climates, Chapter 6: Nutrient Requirements of Poultry at High Temperatures, Circulation Fan Layout for Naturally Ventilated Houses (+11 more)

### Community 7 - "FamTECH Cage Quotation Line Items"
Cohesion: 0.22
Nodes (19): Chicken Coop Spec (17m x 4m x 4.2m, 640 birds, quoted x5 sets), FamTECH Quotation v1 (CIF Puebla, USD17,747), Automatic Egg Collecting Machine (soft-shell separator, PP belt, drive unit; subtotal USD3,272.6), FamTECH (supplier, via ABC Machinery / Anyang Best Complete Machinery), Layer Cage System (front/back end, 4-tier cages, manure belt, manger; subtotal USD4,253.16), NidoSmart (buyer, Mr. Miguel Hernandez), Nipple Drinking System (dosing pump, waterline, nipples; subtotal USD903.8), Quote v1 Commercial Terms (CIF Puebla; 40-day delivery; 30/70 payment; 13-month warranty) (+11 more)

### Community 8 - "640-Bird Scope Freeze & Investment"
Cohesion: 0.19
Nodes (18): DEC-003 — Inicio controlado con piloto de ~100 gallinas, DEC-010 — Servicios compartidos dimensionados para 300 aves desde el piloto, DEC-012 — Congelamiento del alcance de la inversión inicial en una unidad de 640 aves, DEC-013 — Presupuesto consolidado de inversión inicial, vehículo fuera del crédito, Registro de decisiones, Tabla de inversión inicial (CAPEX), Proyecto de inversión, FamTECH — cotización de jaula automatizada tipo H (+10 more)

### Community 9 - "Nave & Vehicle Open Specs"
Cohesion: 0.17
Nodes (12): Altura libre bajo estructura (pendiente), Estado de la ficha técnica de la nave, Materiales de muros y marco (pendiente), Tabla de 19 parámetros técnicos de la nave, Resistencia a viento y clima local (pendiente), Tipo estructural de la nave (pendiente), Forma de adquisición del vehículo: capital propio, sin compra dedicada, Tipo de vehículo recomendado (compacto, sin refrigeración) (+4 more)

### Community 10 - "Egg Safety Regulation (NOM-159)"
Cohesion: 0.21
Nodes (12): Alpha-amylase test method (Apendice A Normativo, verifies pasteurization adequacy), Total coliforms limit (<3 NMP/mL), NOM-159-SSA1-2016 (Egg products, sanitary specifications), Egg washing requirements (potable water 32-45C, sanitizer, no packaging reuse), Freezing requirement (freeze below -18C, store below -5C, no re-freezing), HACCP system requirement for egg product establishments (point 6.1.23), Dehydrated egg product humidity limit (<8%), Labeling requirements (lot, expiration/consume-preferably date, treatment applied) (+4 more)

### Community 11 - "Farm Financial Planning Methods"
Cohesion: 0.29
Nodes (10): Break-Even Price/Yield Analysis, Cash Flow Budgeting, Linear Programming (Farm Planning), Liquidity Analysis (Whole-Farm), Opportunity Cost in Budgeting, Partial Budgeting, Sensitivity Analysis, Shadow Prices and Reduced Costs (+2 more)

### Community 12 - "Risk Management & AI Agents"
Cohesion: 0.31
Nodes (9): Riesgo: error del agente de IA, Riesgo: falla de conectividad a internet, Riesgo: influenza aviar, Tabla de riesgos, impactos y mitigaciones, Hermes Agent, Paperclip, Conclusión general del plan, Decisión recomendada (doce condiciones) (+1 more)

### Community 13 - "Technology-First Investment Strategy"
Cohesion: 0.25
Nodes (8): Enfoque technology-first, business-validated, NidoSmart Core (MVP tecnológico), Secuencia de desarrollo tecnológico (5 etapas), Rol: Soporte técnico, Elementos que pueden aplazarse, Elementos que no deben sacrificarse, Estrategia de priorización de la automatización por riesgo, DEC-011 — Desarrollo tecnológico previo al ingreso de las aves

### Community 14 - "Commercial Strategy & Pilot Economics"
Cohesion: 0.29
Nodes (7): Modelo de venta, Planes de suscripción familiar, Política de precios, Posicionamiento de marca, Margen de contribución, Validación económica, Indicadores financieros

### Community 15 - "Financial Plan: Scale Economics"
Cohesion: 0.29
Nodes (7): Bell & Weaver, capítulo 18 (consumo de alimento y conversión alimenticia), Bell & Weaver, capítulo 50 (costo de capital, complejo de un millón de aves), FamTECH (cotización jaula automatizada tipo H), Flete final: almacén Puebla → sitio del proyecto (pendiente de cotizar), Interpretación: economía de escala de la automatización, Inversión inicial — primera unidad 640 aves, Proyección financiera preliminar — primera unidad (640 aves)

### Community 16 - "Growth Roadmap Phases"
Cohesion: 0.29
Nodes (7): Criterios de éxito antes de crecer, Fase 0. Prefactibilidad, Fase 1. Infraestructura base (640 aves), Fase 2. Validación productiva y comercial, Fase 3. Expansión a una segunda unidad (1,280 aves), Fase 4. Expansión a 1,920–2,560 aves, Fase 5. Expansión a 2,560–5,120 aves

### Community 17 - "Pilot Validation Criteria"
Cohesion: 0.33
Nodes (6): Punto estratégico: escenarios conservador/base/optimista, Objetivo financiero y de validación del piloto, Validación comercial, Validación productiva, Validación tecnológica, DEC-005 — Cubrir OPEX directo en el piloto, sin exigir recuperación del CAPEX

### Community 18 - "Biosecurity & Org Roles"
Cohesion: 0.33
Nodes (6): Medidas mínimas de bioseguridad, Respuesta ante anomalías, Indicadores productivos, Rol: Dirección, Índice general del plan de negocios, NidoSmart (proyecto)

### Community 19 - "FamTECH Equipment Concepts"
Cohesion: 0.40
Nodes (6): Automated Feed Trough (Layer Cage), FamTECH Battery Layer Cage System, Manure Removal Belt System, Multi-Tier Stacked Cage Configuration, FamTECH (Poultry Cage Equipment Supplier), Photo: FamTECH Layer Cage Row Interior

### Community 20 - "Installation Photo: Cage Row Setup"
Cohesion: 0.53
Nodes (6): Tiered Battery Cage Rack System, White Plastic Belt/Sheeting Roll, Photo: Installing Belt Roll on Layer Cage System, On-Site Installation Crew (Four Workers), "nbc Machinery" Branded Shirt, Poultry Shed / Barn Structure

### Community 21 - "Installation Photo: Cage Interior"
Cohesion: 0.60
Nodes (5): FamTECH (Supplier), Layer Cage House Interior Photo, Layer Cage Automation System (Equipment Shown), Manure Removal Trough/Belt System, Multi-Tier Battery Cage Rows

### Community 22 - "Installation Photo: Egg Elevator"
Cohesion: 0.60
Nodes (5): Multi-Tier Layer Battery Cage Row, Local Push-Button Control Panel on Elevator Tower, Vertical Egg Collection Elevator Tower, FamTECH (Poultry Cage Equipment Supplier), Photo: Battery Cage System with Egg Collection Elevator Tower

### Community 23 - "Regulatory Bodies & Compliance"
Cohesion: 0.50
Nodes (4): CONAGUA (aguas nacionales), Ley Federal de Sanidad Animal, SENASICA (registro de unidad de producción), Trámites específicos para San Francisco Acatepec, San Andrés Cholula, Puebla

### Community 24 - "Pilot-to-Expansion Criteria"
Cohesion: 0.67
Nodes (3): Cubrir OPEX y validar modelo sin exigir CAPEX en el piloto, Criterios para agregar un módulo, Validación del piloto (18)

### Community 25 - "ABC Machinery Branding"
Cohesion: 0.67
Nodes (3): ABC Machinery (brand), FamTECH Poultry Cage Quotation Thread, ABC Machinery Logo Image

## Ambiguous Edges - Review These
- `Table 22-8: Suggested Maximum Limits of Water Components for Chickens` → `Table 52-1: Recommended Minimum Space Allowances During Lay (Floor, Feeder, Waterer Space, 16 wk+)`  [AMBIGUOUS]
  knowledge-base/books/commercial-chicken-meat-and-egg-production.pdf · relation: conceptually_related_to
- `Table 50-1: Typical Egg Complex Investment Costs (US 1999, $/hen)` → `Table 52-2: Minimum Cage Floor Space Requirements for Laying Hens (Various Sources)`  [AMBIGUOUS]
  knowledge-base/books/commercial-chicken-meat-and-egg-production.pdf · relation: conceptually_related_to
- `ABC Machinery Logo Image` → `FamTECH Poultry Cage Quotation Thread`  [AMBIGUOUS]
  evidence/correspondence/mail_famtechpoultry.rtfd/4__#$!@%!#__unknown.jpg · relation: conceptually_related_to
- `Generic Download Icon Image` → `FamTECH Poultry Cage Quotation Email Thread`  [AMBIGUOUS]
  evidence/correspondence/mail_famtechpoultry.rtfd/unknown.png · relation: conceptually_related_to

## Knowledge Gaps
- **166 isolated node(s):** `Segunda unidad (1,280 aves)`, `Escala objetivo de largo plazo (5,000 aves)`, `Estrategia comercial (venta directa, suscripciones)`, `Productos secundarios`, `Mercado mexicano de huevo` (+161 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **17 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `Table 22-8: Suggested Maximum Limits of Water Components for Chickens` and `Table 52-1: Recommended Minimum Space Allowances During Lay (Floor, Feeder, Waterer Space, 16 wk+)`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **What is the exact relationship between `Table 50-1: Typical Egg Complex Investment Costs (US 1999, $/hen)` and `Table 52-2: Minimum Cage Floor Space Requirements for Laying Hens (Various Sources)`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **What is the exact relationship between `ABC Machinery Logo Image` and `FamTECH Poultry Cage Quotation Thread`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **What is the exact relationship between `Generic Download Icon Image` and `FamTECH Poultry Cage Quotation Email Thread`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **Why does `Índice general del plan de negocios` connect `Biosecurity & Org Roles` to `NidoSmart Business Overview`, `Risk Management & AI Agents`, `Technology-First Investment Strategy`, `Commercial Strategy & Pilot Economics`, `Financial Plan: Scale Economics`, `Growth Roadmap Phases`, `Pilot Validation Criteria`, `Regulatory Bodies & Compliance`?**
  _High betweenness centrality (0.143) - this node is a cross-community bridge._
- **Why does `Módulo inicial (640 aves, nave 17x4x4.2m)` connect `NidoSmart Business Overview` to `Financial Plan: Scale Economics`?**
  _High betweenness centrality (0.122) - this node is a cross-community bridge._
- **Are the 3 inferred relationships involving `Hermes Agent` (e.g. with `Base de datos local de series de tiempo` and `Acciones permitidas`) actually correct?**
  _`Hermes Agent` has 3 INFERRED edges - model-reasoned connections that need verification._
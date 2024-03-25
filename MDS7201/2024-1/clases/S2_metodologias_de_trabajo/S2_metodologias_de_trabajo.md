# S2 - Metodologías de trabajo

## Índice

- Por qué es importante tener una buena metodología de trabajo?
	- Reducir riesgo
	- Mejorar productividad
	- Mejorar el insight generado
- Diferencia con desarrollo de software tradicional
- Algunos riesgos
	- ![[Pasted image 20240310181304.png]]
- Algunas áreas en las que enfocar el trabajo
	- ![[Pasted image 20240310181537.png]]
- Tipos de metodologías de trabajo
	- Metodologías relacionadas con Data Science
		- KDD (década de los '90)
			1. Selection
			2. Pre-processing
			3. Transformation
			4. Data Mining
			5. Interpretation/Evaluation
		- CRISP-DM (1999)
			1. Business understanding – What does the business need?
			2. Data understanding – What data do we have / need? Is it clean?
			3. Data preparation – How do we organize the data for modeling?
			4. Modeling – What modeling techniques should we apply?
			5. Evaluation – Which model best meets the business objectives?
			6. Deployment – How do stakeholders access the results?
		- TDSP (Contemporáneo, editado en marzo 2024)
			- Etapas
				1. [Business understanding](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/lifecycle-business-understanding)
				2. [Data acquisition and understanding](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/lifecycle-data)
				3. [Modeling](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/lifecycle-modeling)
				4. [Deployment](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/lifecycle-deployment)
				5. [Customer acceptance](https://learn.microsoft.com/en-us/azure/architecture/data-science-process/lifecycle-acceptance)
			- Características
				- Coexistencia de fases
				- Distintos roles
		- Otros
			- SEMMA (2012)
			- Domino (2017)
		- MLOps (detalles para otro curso)
			- Automation
			- Continuous X
			- Versioning
			- Experiments Tracking
			- Testing
			- Monitoring
			- Reproducibility
			- Loosely Coupled Architecture (Modularity)
			- ML-based Software Delivery Metrics (4 metrics from “Accelerate”)
	- Metodologías de trabajo genéricas
		- Waterfall
		- Metodologías Ágiles != Manifiesto Ágil
			- El manifiesto ágil es básicamente cómo trabajar en equipo para ingenieros sin tantas habilidades sociales.
		- Manifiesto Ágil
			- Individuos e interacciones sobre procesos y herramientas  
			- Software funcionando sobre documentación extensiva  
			- Colaboración con el cliente sobre negociación contractual  
			- Respuesta ante el cambio sobre seguir un plan
		- Principios del manifiesto ágil
			- Nuestra mayor prioridad es satisfacer al cliente mediante la entrega temprana y continua de software con valor.
			- Aceptamos que los requisitos cambien, incluso en etapas tardías del desarrollo. Los procesos Ágiles aprovechan el cambio para proporcionar ventaja competitiva al cliente.
			- Entregamos software funcional frecuentemente, entre dos semanas y dos meses, con preferencia al periodo de tiempo más corto posible.
			- Los responsables de negocio y los desarrolladores trabajamos juntos de forma cotidiana durante todo el proyecto.
			- Los proyectos se desarrollan en torno a individuos motivados. Hay que darles el entorno y el apoyo que necesitan, y confiarles la ejecución del trabajo.  
			- El método más eficiente y efectivo de comunicar información al equipo de desarrollo y entre sus miembros es la conversación cara a cara.
			- El software funcionando es la medida principal de progreso.
			- Los procesos Ágiles promueven el desarrollo sostenible. Los promotores, desarrolladores y usuarios debemos ser capaces de mantener un ritmo constante de forma indefinida.
			- La atención continua a la excelencia técnica y al buen diseño mejora la Agilidad.
			- La simplicidad, o el arte de maximizar la cantidad de trabajo no realizado, es esencial.
			- Las mejores arquitecturas, requisitos y diseños emergen de equipos auto-organizados.
			- A intervalos regulares el equipo reflexiona sobre cómo ser más efectivo para a continuación ajustar y perfeccionar su comportamiento en consecuencia.
		- Scrum
			- Sprints
				- No sirve mucho para proyectos exploratorios ni inciertos
			- User Stories
			- Daily meeting
			- Retrospective
		- Kanban
			- Board
			- Backlog
		- Extreme Programming (XP)
			- Pair Programming
			- Unit test
		- Lean Development
			- Toyota
			- Remover lo innecesario
		- Crystal
			- División según cantidad de personas
			- Adaptativo
- Herramientas de manejo de proyectos
	- Carta Gantt (Waterfall)
	- Jira
	- Trello
	- Asana
	- Monday
	- ClickUp
	- Notion
	- Planner
	- Etc.
- Control de versiones
	- Git
	- Object Storage
	- Registry
		- Containers
		- Docker
		- Modelos
- Manifiesto de programación
	- Principios
		-  ![:mechanical_arm:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f9be.png) Un buen código es resiliente y robusto
		-  ![:track_next:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/23ed.png) Un buen código facilita el traspaso y la continuidad
		-  ![:athletic_shoe:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f45f.png) Un buen código es eficiente
		-  ![:tools:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f6e0.png) Un buen código permite ocupar distintas herramientas y lenguaje de programación
		-  ![:robot:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f916.png) Un buen código permite un sencillo paso a producción
		-  ![:classical_building:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f3db.png) Un buen código pertenece a una cultura en común
		-  ![:muscle:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f4aa.png) Un buen código sigue una estructura que, a la vez, es flexible
		-  ![:moneybag:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/1f4b0.png) Un buen código genera valor a la empresa
		-  ![:timer:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/standard/caa27a19-fc09-4452-b2b4-a301552fd69c/32x32/23f2.png) Un buen código toma tiempo
	- Técnicas Esenciales
		- Usar una estructura de carpetas y scripts
		- Usar nombres descriptivos para las variables
		- Comentar los códigos
		- Hacer buen uso de las funciones
		- Modularizar los proyectos
		- Saber cuándo ocupar scripts o notebooks
		- Conocer los distintos usos de los “Integrated development environment” (IDE)
	- Técnicas Básicas (detalles en otro curso)
	- Técnicas Avanzadas (detalles en otro curso)

## Links relevantes

- https://www.datascience-pm.com/data-science-methodologies/
- https://www.datascience-pm.com/kdd-and-data-mining/
- https://www.datascience-pm.com/crisp-dm-2/
- https://learn.microsoft.com/en-us/azure/architecture/data-science-process/overview
- https://www.turing.com/kb/understanding-the-workflow-of-mlops
- https://ml-ops.org/content/mlops-principles
- https://mlops-guide.github.io/
- https://rihab-feki.medium.com/mlops-01-an-introduction-to-mlops-levels-its-life-cycle-7e9eb9a1f296
- https://www.projectmanager.com/blog/project-management-methodology
- https://agilemanifesto.org/iso/es/manifesto.html
- https://agilemanifesto.org/iso/es/principles.html
- https://www.xpand-it.com/blog/top-5-agile-methodologies/
- https://monday.com/blog/project-management/agile-crystal/
- https://www.proofhub.com/articles/agile-project-management-tools-list
- https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F
- https://www.mirantis.com/cloud-native-concepts/understanding-containers/what-is-a-container-registry/
- https://neptune.ai/blog/ml-model-registry
- https://www.youtube.com/watch?v=C5JElgliTeE
- https://www.youtube.com/watch?v=7EmboKQH8lM&list=PLeKgk5El3zkShgXMvKQJF6SpslUNfFtqN&ab_channel=UnityCoin
- https://www.youtube.com/watch?v=62v251H96Dw
- https://www.youtube.com/watch?v=o80HGoCOlU8
- https://www.youtube.com/watch?v=bZ1JAHETKxY
- https://www.youtube.com/watch?v=MBPQpWudZhs

## Volver al inicio

[[resumenes_clases_MDS7201]]
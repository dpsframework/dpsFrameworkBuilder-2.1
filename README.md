# 1. Componentes de dpsFramework 
[English](https://github.com/dpsframework/dpsframework-components#1-dps-framework-components)



- Son los siguientes: 
1. Constructor de nodos de la infraestructura de aplicación distribuida (**dpsframework.Builder**)
1. Agentes JADE para gobierno de Sistemas de Producción (**dpsframework.PSAgents**)
1. Intérprete-compilador de Java para agentes PSAgents en tiempo de ejución (**BeanShell**)
1. Herramientas de construcción de Sistemas de Producción y sus librerías de comunicación con Java (**CLIPS**, **Jess**, etc.)
1. Framework Java para el Desarrollo de Sistemas Multi-Agente (**JADE**)
1. Herramientas de soporte al desarrollo y comprobación de la apalicación distribuida (**dpsframework.Utils**)
1. Framework Java para construir aplicaciones basadas en Ontología (**Apache-JENA**)



## 1.1. Contructor de los nodos de la infraestructura de aplicación: (**dpsframework.Builder**)

El constructor de nodos está disponible mediante: 


`java  -jar   dpsframework-application-builder-2.1.jar` (sólo para, Java JDK-11 o superior). 


- Descripción y funciones:
  - Cada nodo de la aplicación es generado por el objeto: **dpsframework.Builder**. 
  - Los nodo de una misma aplicación comparten: el mismo nombre y un mismo identificador único.


### 1.1.1. Objetivo del **constructor** de nodos: 
- Generar una estructura estándard: en cada Host (Hardware), máquina virtual (VMware/VirtualBOX) o contenedor (Docker), el constructor genera los Nodos de la aplicación distribuida.
- Migrar y desplegar de manera controlada: un Nodo es una estructura de directorios reconocida por los Agentes de una misma aplicación, hacia donde es posible migrar y desplegarse para obtener los recursos de la máquina (Host).
- Aportar seguridad y control: el constructor incorpora a todos los nodos de una misma aplicación distribuida, un mecanismo de verificación que se comprueba en cada comunicación entre Agentes.




### 1.1.2. Objetivo de la **aplicación distribuida**:
-  Gobernar un Sistema de Producción: la aplicación distribuida gestiona y gobierna mediante sus agenetes PSAgents, la ejecución, parada y coordinación de sistema de producción a distribuir.
-  Coordinar memorias de trabajo y hechos: la aplicación distribuida  ---mediante tecnología de los sistemas Multi-Agentes--- permite realizar el despligue y la interconexión de las memorias de trabajo, de las distintas activaciones de reglas en las agendas y, la re-alimentación de nuevos hechos desde los nodos hacias los agentes de la aplicación.













## 1.2. Agentes JADE para gobierno de Sistemas de Producción (**dpsframework.PSAgents**)

Librería de Java (artefacto): **dpsframework-agents-2.1.jar**. Permite crear nuevos Agentes de JADE con capacidad para desplegar sistemas de producción distribuidos. Esta librería utiliza además los componentes siguientes: 


- Descripción y funciones:
  - Los agentes de la aplicación: mantienen sus datos sobre directorios de los Nodos de aplicación. Cuando migran hacia otro Nodo, empaquetan y comprimen sus datos, se transmiten mediante la plataforma Multi-Agente y se despliegan de nuevo en el Nodo de destino.
  - Los tipos de agentes PSAgents: permiten generar y desplegar en la plataforma Multi-Agente, a los agentes de la aplicación distribuida. Existen cuatro modelos o tipos de estos agentes. Son el tipo-Agente de Monitorización, el tipo-Agente Sistema de Produccion, el tipo-Agente Pizarra y, el tipo-Agente Escenario-de-ensayo.

### 1.2.1. Objetivos de agentes tipo **PSAgents**: 
- Gobierno de la aplicación: 
- Facilitar la administración de la aplicación: 
- Desplegar el Sistema de Producción: 
- Facilitar las pruebas funcionales: 




## 1.3. Intérprete-compilador de Java para agentes PSAgents en tiempo de ejución (**BeanShell**)


## 1.4. Herramientas de construcción de Sistemas de Producción y sus librerías de comunicación con Java (**CLIPS**, **Jess**, etc.)


## 1.5. Framework Java para el Desarrollo de Sistemas Multi-Agente (**JADE**)


## 1.6. Herramientas de soporte al desarrollo y comprobación de la apalicación distribuida (**dpsframework.Utils**)


## 1.7. Framework Java para construir aplicaciones basadas en Ontología (**Apache-JENA**)

















---

# 1. dps-Framework components
[Castellano](https://github.com/dpsframework/dpsframework-components#1-componentes-de-dpsframework)


- They are the following:
1. Distributed Application Framework Node Builder (**dpsframework.Builder**)
1. JADE Agents for Production Systems governance (**dpsframework.PSAgents**)
1. Java interpreter-compiler for PSAgents at runtime (**BeanShell**)
1. Production Systems construction tools and their communication libraries with Java (**CLIPS**, **Jess**, etc.)
1. Java Framework for Multi-Agent Systems Development (**JADE**)
1. Distributed application development and testing tools (**dpsframework.Utils**)
1. Java framework to build ontology-based applications (**Apache-JENA**)











## 1.1. Application framework node builder: (**dpsframework.Builder**)

The node constructor is available via:


`java -jar dpsframework-application-builder-2.1.jar` (only for Java, JDK-11 or higher).


- Description and functions:
   - Each node belonging to the application is generated by the object: **dpsframework.Builder**.
   - The nodes of the same application share: the same name and the same unique identifier.
   
   
### 1.1.1. Objective of the **constructor** of nodes:
- Generate a standard structure: in each Host (Hardware), virtual machine (VMware/VirtualBOX) or container (Docker), the constructor generates the Nodes of the distributed application.
- Migrate and deploy PSAgents type agents: a Node is a directory structure recognized by the agents of the same application, where they can migrate and deploy to obtain the resources of the machine (Host).
- Provide security and control: the constructor incorporates, in all the nodes of the same application, mechanisms for verifying the communications between the agents.

### 1.1.2. Objective of the **distributed application**:
- Govern a Production System: the distributed application manages and governs, through its PSAgents, the execution, shutdown and coordination of the production system to be distributed.
- Coordinate work memories and facts: the distributed application ---through the use of Multi-Agent systems technology--- allows the deployment and interconnection of work memories, the different activations of rules in the agendas and the feedback of new facts from the nodes to the agents of the application.







## 1.2. JADE Agents for Production Systems governance (**dpsframework.PSAgents**)

Java library (artifact): **dpsframework-agents-2.1.jar**. It allows creating new JADE Agents with the capacity to deploy distributed production systems. This library also uses the following components:


- Description and functions:
   - The application agents: they keep their data on the directories of the application Nodes.
   - When PSAgents migrate to another Node, their data is packaged and compressed, transmitted through the Multi-Agent platform and deployed again on the destination Node.
   - The types of agents PSAgents: they allow to generate and deploy in the Multi-Agent platform, the agents of the distributed application. There are four models or types of these agents. 
   1. They are the Monitoring Agent-type
   2. The Production System Agent-type
   3. The Blackboard Agent-type and
   4. The Rehearsal Stage Agent-type
   
   

### 1.2.1. Objectives of agents type **PSAgents**:
- Application governance:
- Facilitate the administration of the application:
- Deploy the Production System:
- Facilitate functional tests:




## 1.3. Java interpreter-compiler for PSAgents at runtime (**BeanShell**)


## 1.4. Construction tools for Production Systems and their communication libraries with Java (**CLIPS**, **Jess**, etc.)


## 1.5. Java Framework for Multi-Agent Systems Development (**JADE**)


## 1.6. Distributed application development and testing support tools (**dpsframework.Utils**)


## 1.7. Java Framework to build applications based on Ontology (**Apache-JENA**)

## 1.2. JADE Agents for deployment and management of Production Systems: **dpsframework.PSAgent**

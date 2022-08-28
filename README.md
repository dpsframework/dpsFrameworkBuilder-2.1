# 1. dpsFramework-2.1
[**English**](https://github.com/dpsframework/dpsframework-components#1-dpsframework-21-1)


>  NOTA: La liberación de la versión 2.1 está prevista antes de finalizar el 2022.


- La versión 2.1 del proyecto aporta los siguientes artefactos: 

1. (**dpsFramework-installer-2.1.jar**) Creador de nodos de la aplicación para desplegar en (Host, Container o VBox).
1. (**dpsAgents-2.1.jar**) Agentes de JADE para gobierno de Sistemas de Producción. 
1. (**dpsDevelopment-2.1.jar**) Scripts para soporte al desarrollo, la depuración de agentes y la comprobación de los nodos de la aplicación. 

- La versión 2.1, del proyecto dpsFramework utiliza:

1. (**BeanShell-2.1**) Intérprete y compilador de Java en tiempo de ejecución para loas agentes tipo PSAgent.
1. (**CLIPS-6.40b**, **Jess-8.0b1**) Herramientas de construcción de Sistemas de Producción y sus librerías Java (actualizados a Java-11 a 18).
1. (**Plataforma JADE**) Framework Java para el Desarrollo de Sistemas Multi-Agente versión 4.5.4 r6868, Julio 2022.
1. (**Apache-JENA**) Framework Java para construir aplicaciones basadas en Ontologías 




## 1.1. Generador de nodos de la aplicación (**dpsFramework-installer-2.1.jar**)

El generador de los nodos de la aplicación debe ser utilizado desde la línea de comandos con la sentencia:  


`java  -jar   dpsFramework-installer-2.1.jar` (sólo para, Java-11 o superior). 


- **Descripción y funciones**:
  - Cada nodo de la aplicación es generado por la clase: **dpsframework.NodeBuilder** del artefacto **dpsFramework-installer-2.1.jar**. 
  - Los nodos de una misma aplicación comparten: el mismo nombre y un mismo identificador único. Eso les permite identificar a los agentes de la aplicación y permitir que los agentes de la aplicación puedan migrar hacia los servidores (Reales o Virtualizados) o los Contenedores (Docker) donde se ejecuta la plataforma JADE y, la aplicación, posee su nodo desplegado. 




### 1.1.1. Objetivo del **constructor de nodos**: 
- Generar una estructura estándard: en cada Host (Hardware), máquina virtual (VMware/VirtualBOX) o contenedor (Docker), el constructor genera los Nodos de la aplicación distribuida.
- Migrar y desplegar de manera controlada: un Nodo es una estructura de directorios reconocida por los Agentes de una misma aplicación, hacia donde es posible migrar y desplegarse para obtener los recursos de la máquina (Host).
- Aportar seguridad y control: el constructor incorpora a todos los nodos de una misma aplicación distribuida, un mecanismo de verificación que se comprueba en cada comunicación entre Agentes.




### 1.1.2. Objetivo de la **Aplicación de Sistema de Producción Multiagente**:
-  Gobernar un Sistema de Producción: la aplicación gestiona y gobierna mediante sus agenetes PSAgents, la ejecución, parada y coordinación de sistema de producción a distribuir.
-  Coordinar memorias de trabajo y hechos: la aplicación  ---mediante tecnología de los sistemas Multi-Agentes--- permite realizar el despligue y la interconexión de las memorias de trabajo, de las distintas activaciones de reglas en las agendas y, la re-alimentación de nuevos hechos desde los nodos hacias los agentes de la aplicación.













## 1.2. Agentes JADE para gobierno de Sistemas de Producción (**dpsframework.PSAgents**)

Librería de Java (artefacto): **dpsframework-agents-2.1.jar**. Permite crear nuevos Agentes de JADE con capacidad para desplegar sistemas de producción distribuidos. Esta librería utiliza además los componentes siguientes: 


- Descripción y funciones:
  - Los agentes de la aplicación: mantienen sus datos sobre directorios de los Nodos de aplicación. Cuando migran hacia otro Nodo, empaquetan y comprimen sus datos, se transmiten mediante la plataforma Multi-Agente y se despliegan de nuevo en el Nodo de destino.
  - Los tipos de agentes PSAgents: permiten generar y desplegar en la plataforma Multi-Agente, a los agentes de la aplicación distribuida. Existen cuatro modelos o tipos de estos agentes. Son:
  1. Agente-tipo Manager
  2. Agente-tipo Sistema de Produccion
  3. Agente-tipo Pizarra y
  4. Agente-tipo Escenario-de-ensayo

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

# 1. dpsFramework-2.1
[**Castellano**](https://github.com/dpsframework/dpsframework-components#1-dps-framework-21)



> NOTE: The release of version 2.1 is planned before the end of 2022.


- Version 2.1 of the project provides the following artifacts:

1. (**dpsFramework-installer-2.1.jar**) Application node builder to deploy to (Host, Container or VBox).
1. (**dpsAgents-2.1.jar**) JADE Agents for Production Systems governance.
1. (**dpsDevelopment-2.1.jar**) Scripts to support the development, agent debugging and testing of the application nodes.

- Version 2.1, of the dpsFramework project uses:

1. (**BeanShell-2.1**) Java runtime interpreter and compiler for PSAgent type agents.
1. (**CLIPS-6.40b**, **Jess-8.0b1**) Production Systems build tools and their Java libraries (updated to Java-11 to 18).
1. (**JADE Platform**) Java Framework for Multi-Agent Systems Development version 4.5.4 r6868, July 2022.
1. (**Apache-JENA**) Java Framework to build applications based on Ontologies



## 1.1. Application Node Builder (**dpsFramework-installer-2.1.jar**)

The generator of the application nodes must be used from the command line with the statement:


`java -jar dpsFramework-installer-2.1.jar` (only for Java-11 or higher).


- **Description and functions**:

  - Each application node is generated by calling the class: **dpsframework.NodeBuilder** of **dpsFramework-installer-2.1.jar** artifact.
  - The nodes of the same application share: the same name and the same unique identifier. This allows them to identify the application agents and allow the application agents to migrate to the servers (Real or Virtualized) or Containers (Docker) where the JADE platform is executed and the application has its node deployed.




### 1.1.1. Objective of the **constructor** of nodes:
- Generate a standard structure: in each Host (Hardware), virtual machine (VMware/VirtualBOX) or container (Docker), the constructor generates the Nodes of the distributed application.
- Migrate and deploy PSAgents type agents: a Node is a directory structure recognized by the agents of the same application, where they can migrate and deploy to obtain the resources of the machine (Host).
- Provide security and control: the constructor incorporates, in all the nodes of the same application, mechanisms for verifying the communications between the agents.




### 1.1.2. Objective of the **Multiagent Production System Application**:
- Govern a Production System: the application manages and governs, through its PSAgents, the execution, shutdown and coordination of the production system to be distributed.
- Coordinate work memories and facts: the application ---through the use of Multi-Agent systems technology--- allows the deployment and interconnection of work memories, the different activations of rules in the agendas and the feedback of new facts from the nodes to the agents of the application.







## 1.2. JADE Agents for Production Systems governance (**dpsAgents-2.1.jar**) artifact

Java library **dpsAgents-2.1.jar**: It allows creating new JADE Agents with the capacity to deploy distributed production systems. This library also uses the following components:


- Description and functions:
   - The application agents: they keep their data on the directories of the application Nodes.
   - When PSAgents migrate to another Node, their data is packaged and compressed, transmitted through the Multi-Agent platform and deployed again on the destination Node.
   - The types of agents PSAgents: they allow to generate and deploy in the Multi-Agent platform, the agents of the distributed application. There are four models or types of these agents. They are:
   1. The Manager Agent-type
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

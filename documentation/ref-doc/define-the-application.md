---
layout: article
title: Define the application
subtitle: Reference Documentation
relativePath: ..
---

The first questions John has to answer are :
What the application is supposed to be?
and
What the application is supposed to do?

What the application is supposed to be ?
----------------------------------------

First, John tries to get a feel for the bigger picture of its application. The purpose is to get an overall understanding of the system. He wants to catch the business process and checks if there is a precedent for this application.
To do so UML propose a very useful diagram : the **activity diagram**.
The activity diagram is part of the behavioral diagrams in UML Standard, it is used to represent workflows of stepwise activities.
![]({{page.relativePath}}/images/ActivityDiagram.png)

The activity diagram is a synchronized diagram which means that any elements existing under an activity in the UML model will be visible automatically in the activity diagram.

### <a name="activity-diagram"></a> Manage activities

It is possible to **create activity elements** by selecting the creation tools from the palette and then clicking on the diagram or an element.

![]({{page.relativePath}}/images/ActivityDiagramPalette.png)

A diagram is associated to a package and when the user click on the diagram background the element is created under the corresponding package in the UML model. If the user selects a container, the element will be created under the corresponding semantic element in the UML model.
Tooltip tools are also available to create any kind of elements :
![]({{page.relativePath}}/images/ActivityDiagramTooltips.png)

Creation tools are available in the activity diagram for the following types :

| Element               | Representation                                       | Comments                                           |
|-----------------------|------------------------------------------------------|----------------------------------------------------|
| Partition             | ![]({{page.relativePath}}/images/ActivityDiagramPartition.png)           | Organizes a flow by grouping elements              |
| Initial Node          | ![]({{page.relativePath}}/images/ActivityDiagramInitialNode.png)         | Start of a flow                                    |
| Activity Final Node   | ![]({{page.relativePath}}/images/ActivityDiagramActivityFinalNode.png)   | End of a flow                                      |
| Flow Final Node       | ![]({{page.relativePath}}/images/ActivityDiagramFlowFinalNode.png)       | Exit from the system                               |
| Decision Node         | ![]({{page.relativePath}}/images/ActivityDiagramDecisionNode.png)        | Point of conditional progression                   |
| Merge Node            | ![]({{page.relativePath}}/images/ActivityDiagramMergeNode.png)           | Brings together a number of alternative flow paths |
| Fork Node             | ![]({{page.relativePath}}/images/ActivityDiagramForkNode.png)            | Split the flow into concurrent flows               |
| Join Node             | ![]({{page.relativePath}}/images/ActivityDiagramJoinNode.png)            | Join the flow of concurrent flows                  |
| Opaque Action         | ![]({{page.relativePath}}/images/ActivityDiagramOpaqueAction.png)        | Describes a basic process                          |
| Activity state        | ![]({{page.relativePath}}/images/ActivityDiagramActivityState.png)       | Describes a sub activity                           |
| Call Operation action | ![]({{page.relativePath}}/images/ActivityDiagramCallOperationAction.png) | Describes a call to a defined operation            |
| Activity parameter    | ![]({{page.relativePath}}/images/ActivityDiagramActivityParameter.png)   | Defines parameters for the activity                |
| Data store            | ![]({{page.relativePath}}/images/ActivityDiagramDataStore.png)           | Define permanently stored data                     |
| Input pin             | ![]({{page.relativePath}}/images/ActivityDiagramInputPin.png)            | Activity input                                     |
| Output pin            | ![]({{page.relativePath}}/images/ActivityDiagramOutputPin.png)           | Activity output                                    |

When the *Call Operation action* tool is selected, a selection wizard is opened to ask the user to select an existing operation in the UML model :
![]({{page.relativePath}}/images/ActivityDiagramCallOperationActionWizard.png)

The user can also **delete an activity element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

### Manage flows

It is possible to **create a flow** by selecting the edge creation tool from the palette and then clicking on a source element and a target element.

The following edge creation tools exist in the palette :

| Element      | Representation                               | Comments                          |
|--------------|----------------------------------------------|-----------------------------------|
| Control flow | ![]({{page.relativePath}}/images/ActivityDiagramControlFlow.png) | Connect two nodes                 |
| Object flow  | ![]({{page.relativePath}}/images/ActivityDiagramObjectFlow.png)  | Connect two ports exchanging data |

The user can also **delete a flow** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect flows**. It is possible to reconnect the source and the target of any kind of edge in the activity diagram :

-   control flows
-   object flows

### Edit labels

In the use case diagram, it is possible to edit the elements labels (see [Diagram editor/Editor main graphical area/Direct edit]({{ page.relativePath }}/ref-doc/define-the-system.html#direct-edit)).
This actions allows to edit :

-   actor, subject (component, artifact, datatype, interface, collaboration, class), use case labels
-   relationships labels

### Manage bodies

It is possible to **define a body** to an Opaque Action by selecting the optional layer *Body* from the diagram toolbar. Then the Opaque actions contains there bodies which are editable thanks to the [direct edit]({{ page.relativePath }}/ref-doc/define-the-system.html#direct-edit)).

What the application is supposed to do ?
----------------------------------------

###  <a name="use-case-diagram"></a> Capture the use cases

The next step for John is to capture the different requirements. He knows what he wants, what the other stakeholders want and so he needs to document this. He has already started catching the requirements on post-it notes and pieces of paper during meetings, he has also used his whiteboard for some sketching.
When he recovered all his requirements, he starts to sort them by subject in order to see who is going to use the application. He needs now to capture the different users of the system. John creates a UML **Use Case diagram** to specify the different subjects and the roles played by users and other systems that interact.
The use case diagram is used to describe the interaction of the user and other applications with the specified system.
![]({{page.relativePath}}/images/UseCaseDiagram.png)

The use case diagram is an unsynchronized diagram which means that the user has to add existing elements manually on the diagram to see them.

#### Manage use cases

It is possible in the use case diagram to **create an element** by selecting the creation tool from the palette and then clicking on the diagram or an element. A diagram is associated to a package and in this case the element is created under the corresponding package in the UML model.

![]({{page.relativePath}}/images/UseCaseDiagramPalette.png)

Tooltip tools are also available to create any kind of elements.

The available elements in the use case diagram are :

| Element       | Representation                          | Comments                                       |
|---------------|-----------------------------------------|------------------------------------------------|
| Actor         | ![]({{page.relativePath}}/images/UseCaseDiagramActor.png)   | User of the system                             |
| UseCase       | ![]({{page.relativePath}}/images/UseCaseDiagramUseCase.png) | Describes how a user interacts with the system |
| Subject       | ![]({{page.relativePath}}/images/UseCaseDiagramSubject.png) | Group logically related elements               |

A subject could be a :

-   Component
-   Class
-   Artifact
-   DataType
-   Interface

The **Use Case Diagram** will display any `UseCase` not being affected to a subject on the canvas. If a subject is affected, then the use case
will be displayed directly within this subject.

The user can also **delete an element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Manage relationships

It is possible to **create a relationship** by selecting the edge creation tool from the palette and then clicking on a source element and a target element.
The following edge creation tools exist in the palette :

| Element        | Representation                                 | Comments                                                                           |
|----------------|------------------------------------------------|------------------------------------------------------------------------------------|
| Association    | ![]({{page.relativePath}}/images/UseCaseDiagramAssociation.png)    | General relationship type between elements                                         |
| Extend         | ![]({{page.relativePath}}/images/UseCaseDiagramExtend.png)         | Indicate that an element extends the behavior of another                           |
| Include        | ![]({{page.relativePath}}/images/UseCaseDiagramInclude.png)        | Indicates that the source element includes the functionality of the target element |
| Generalization | ![]({{page.relativePath}}/images/UseCaseDiagramGeneralization.png) | Indicate inheritance                                                               |

The user can also **delete a relationship** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect relationships**. It is possible to reconnect the source and the target of any kind of edge in the use case diagram :

-   association
-   extend
-   include
-   generalization

#### Manage existing elements

As the diagram is unsynchronized, the user needs to add manually the elements already existing in the semantic model that should appear on the representation.
It is possible to **add existing elements** in the use case diagram by :

-   selecting the add tool from the palette or the tooltip and then clicking on the diagram or an element. The add tool opens a selection wizard.
-   drag and droping an element from the model explorer.

Dragging a use case from a subject to the canvas (and the other way around) will set or unset the subject accordingly.

The following elements can be added on a use case diagram :

| Element                                                                  | Representation                                             |
|--------------------------------------------------------------------------|------------------------------------------------------------|
| Use case                                                                 | ![]({{page.relativePath}}/images/UseCaseDiagramUseCase.png)                    |
| Use case into a subject                                                  | ![]({{page.relativePath}}/images/UseCaseDiagramSubject.png)                    |
| Subject (component, artifact, datatype, interface, collaboration, class) | ![]({{page.relativePath}}/images/UseCaseDiagramSubject.png)                    |
| Actor                                                                    | ![]({{page.relativePath}}/images/UseCaseDiagramActor.png)                      |
| Package                                                                  | Add all the elements which could be visible on the diagram |

The user can see that an element is not coming from the current package :

-   the element border is lighter than the element border of elements defined in the current package
-   a tooltip shows the container package of the element if the element is not contained by the current package

And finally, he can **remove an existing element** from a diagram. In this case the element is only deleted from the representation but it is not removed from the UML model. This *Remove* tool exists in the *Existing elements* section in the palette (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Add related elements

In the use case diagram a contextual action is available to show on the diagram the element related to the selection.

The **Add related elements** action is available from :

-   a subject, a use case, an actor : shows all the elements that define a relationship (dependency, include, association...) with the selected element
-   a use case diagram : shows all the elements contained in the package associated to the diagram.

#### Edit labels

In the use case diagram, it is possible to edit the elements labels (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)). This actions allows to edit :

-   actor, collaboration, subject, use case labels
-   relationships labels

#### Use case cross table

Another representation allows the user to see which use cases are associated to which elements in the model. The **use case cross table** represents on lines all the model elements and in the columns the existing use cases. To associate a use case to an element just check the corresponding cell.

### <a name="package-diagram"></a> Define the package system structure

At this step, John knows who will use its application and what they are able todo with it. It is time to define the components, the interfaces and the relationships that would be seen and experienced by the application user. The purpose is to detail the available objects in the user's universe and how they can use them to accomplish certain tasks.
John defines the big structure of the system thanks to the **package diagram**.
The package diagram is used to describe the structure of the system by showing the packages and their dependencies.
![]({{page.relativePath}}/images/PackageDiagram.png)

The package diagram is an unsynchronized diagram which means that the user has to add existing elements manually on the diagram to see them.

#### Manage packages

![]({{page.relativePath}}/images/PackageDiagramPaletteTypes.png)

It is possible to **create activities elements** by selecting the creation tools from the palette and then clicking on the diagram or an element. A diagram is associated to a package and when the user click on the diagram background the element is created under the corresponding package in the UML model. If the user selects a container, the element will be created under the corresponding semantic element in the UML model.

A creation tool is available in the package diagram for the package : ![]({{page.relativePath}}/images/PackageDiagramPackage.png)

The user can also **delete an element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Manage relationships

It is possible to **create a relationship** by selecting the edge creation tool from the palette and then clicking on a source element and a target element.

![]({{page.relativePath}}/images/PackageDiagramPaletteRelationships.png)

The following edge creation tools exist in the palette :

| Element      | Representation                              | Comments                                                                       |
|--------------|---------------------------------------------|--------------------------------------------------------------------------------|
| Contained in | ![]({{page.relativePath}}/images/PackageDiagramContainedIn.png) | Defines that a package that is made up of smaller packages                     |
| Import       | ![]({{page.relativePath}}/images/PackageDiagramImport.png)      | Show that the package content is imported                                      |
| Usage        | ![]({{page.relativePath}}/images/PackageDiagramUsage.png)       | Shows that a package uses another package                                      |
| Dependency   | ![]({{page.relativePath}}/images/PackageDiagramDependency.png)  | Traces a dependency between packages                                           |
| Merge        | ![]({{page.relativePath}}/images/PackageDiagramMerge.png)       | The contents of the target package are merged with those of the source package |

The user can also **delete a relationship** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect relationships**. It is possible to reconnect the source and the target of any kind of edge in the use case diagram :

-   contained in
-   dependency
-   usage
-   import
-   merge

#### Manage existing elements

As the diagram is unsynchronized, the user needs to add manually the elements already existing in the semantic model that should appear on the representation.
It is possible to **add existing elements** by :

-   selecting the add tool from the palette and then clicking on the diagram or an element : 

![]({{page.relativePath}}/images/PackageDiagramPaletteExistingElements.png)
-   drag and droping a package from the model explorer : 

![]({{page.relativePath}}/images/PackageDiagramDragAndDropExistingElements.png)

The user can see that an element is not coming from the current package :

-   the element border is lighter than the element border of elements defined in the current package
-   a tooltip shows the container package of the element if the element is not contained by the current package

And finally, he can **remove an existing element** from a diagram. In this case the element is only deleted from the representation but it is not removed from the UML model. This *Remove* tool exists in the *Existing elements* section in the palette (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Add related elements

In the package diagram a contextual action is available to show on the diagram the element related to the selection.

![]({{page.relativePath}}/images/PackageDiagramAddRelatedElements.png)

The **add related elements** action is available from :

-   a package : shows all the packages that define a relationship (containment, dependency, usage..) with the selected package
-   a package diagram : shows all the elements contained in the package associated to the diagram.

#### Edit labels

In the package diagram, it is possible to edit the elements labels (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)). This actions allows to edit :

-   package labels
-   relationships labels

### <a name="component-diagram"></a> Define the components

It is the moment for John to split the system in multiple components and to describe how all these elements are linked together in a **component diagram**.
The component diagram is used to describe the structure of the system by showing the components and their connectors.
![]({{page.relativePath}}/images/ComponentDiagram.png)

The component diagram is an unsynchronized diagram which means that the user has to add existing elements manually on the diagram to see them.

#### Manage nodes

It is possible to **create nodes** by selecting the creation tools from the palette and then clicking on the diagram or an element. A diagram is associated to a package and when the user click on the diagram background the element is created under the corresponding package in the UML model.
If the user selects a container, the element will be created under the corresponding semantic element in the UML model.

![]({{page.relativePath}}/images/ComponentDiagramPalette.png)

Tooltip tools are also available to create any kind of elements.

Creation tools are available in the component diagram for the following types :

| Element                    | Representation                                          | Comments                                                       |
|----------------------------|---------------------------------------------------------|----------------------------------------------------------------|
| Component                  | ![]({{page.relativePath}}/images/ComponentDiagramComponent.png)             | A modular part of a system                                     |
| Component into a component | ![]({{page.relativePath}}/images/CompositeStructureDiagramSubComponent.png) | A sub part of a component                                      |
| Class                      | ![]({{page.relativePath}}/images/ComponentDiagramClass.png)                 | A representation of objects                                    |
| Class into a component     | ![]({{page.relativePath}}/images/CompositeStructureDiagramSubClass.png)     | A representation of objects                                    |
| Port on a component        | ![]({{page.relativePath}}/images/ComponentDiagramPort.png)                  | Define the interaction between a component and its environment |
| Port on a class            | ![]({{page.relativePath}}/images/CompositeStructureDiagramPort.png)         | Define the interaction between a class and its environment     |
| Interface                  | ![]({{page.relativePath}}/images/ComponentDiagramInterface.png)             | A contract that implementers agree to meet                     |

A class can be used as a component :
![]({{page.relativePath}}/images/features/component_pics/class_as_component.jpg)
or in a component :
![]({{page.relativePath}}/images/features/component_pics/implementation_classes_in_component.jpg)

Required and Provided Interfaces can be defined:

-   using ports :
    ![]({{page.relativePath}}/images/features/component_pics/exchange_through_ports.jpg)
-   or directly on the components :
    ![]({{page.relativePath}}/images/features/component_pics/exchange_through_component.jpg)

The user can also **delete an element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model).

#### Manage relationships

It is possible to **create a relationship** by selecting the edge creation tool from the palette and then clicking on a source element and a target element.
The following edge creation tools exist in the palette :

| Element               | Representation                                            | Comments                                      |
|-----------------------|-----------------------------------------------------------|-----------------------------------------------|
| Usage                 | ![]({{page.relativePath}}/images/ComponentDiagramUsage.png)                   | Source component uses target component        |
| Dependency            | ![]({{page.relativePath}}/images/ComponentDiagramDependency.png)              | Source component depends on target component  |
| Component Realization | ![]({{page.relativePath}}/images/ComponentDiagramComponentRealization.png)    | Source component realizes target component    |
| Generalization        | ![]({{page.relativePath}}/images/CompositeStructureDiagramGeneralization.png) | Source component generalizes target component |
| Interface Realization | ![]({{page.relativePath}}/images/ComponentDiagramInterfaceRealization.png)    | Component realizes interface                  |
| Redefined             | ![]({{page.relativePath}}/images/ComponentDiagramRedefined.png)               | Source port redefined target port             |
| Connector             | Represented by a solid link between two ports             | Source port is connected to target port       |

You can link two ports using assembly or delegation connectors.

Assembly Connector :

![]({{page.relativePath}}/images/features/component_pics/assembly_connector.jpg)

Delegation Connector :

![]({{page.relativePath}}/images/features/component_pics/delegation_connector.jpg)

The user can also **delete a relationship** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect relationships**. It is possible to reconnect the source and the target of any kind of edge in the use case diagram :

-   usage
-   dependency
-   component realization
-   interface realization
-   redefined
-   connector

#### Manage existing elements

As the diagram is unsynchronized, the user needs to add manually the elements already existing in the semantic model that should appear on the representation.
It is possible to **add existing elements** by :

-   selecting the add tool from the palette or the tooltip and then clicking on the diagram or an element. The add tool opens a selection wizard.
-   drag and droping an element from the model explorer.

The following elements can be added on a component diagram :

-   component
-   component into an existing component
-   class
-   class into an existing component
-   interface
-   package

The user can see that an element is not coming from the current package :

-   the element border is lighter than the element border of elements defined in the current package
-   a tooltip shows the container package of the element if the element is not contained by the current package

And finally, he can **remove an existing element** from a diagram. In this case the element is only deleted from the representation but it is not removed from the UML model. This *Remove* tool exists in the *Existing elements* section in the palette (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Add related elements

In the component diagram a contextual action is available to show on the diagram the element related to the selection.

The **add related elements** action is available from :

-   a component , a class, an interface, a port : shows all the elements that define a relationship (dependency, component realization, interface realization...) with the selected element
-   a component diagram : shows all the elements contained in the package associated to the diagram.

#### Edit labels

In the package diagram, it is possible to edit the elements labels (see [Diagram editor/Editor main graphical area/Direct edit]({{ page.relativePath }}/ref-doc/define-the-system.html#direct-edit)).
This actions allows to edit :

-   component, class, interface, port labels
-   relationships labels

### Define the information flow

By creating links between the components, John defines the flow followed by the data in the system.
To get details on how to manage the information flows (see [What the application is supposed to be?/Define components/Manage relationships]({{ page.relativePath }}/ref-doc/define-the-application.html#manage-relationships)).

### Diagram the organization of the information

He provides a detailed organization of the information by creating a new kind of activity diagram. This diagram shows how the information goes through the different components of the system. Previously in the process, John used an activity diagram to describe the global business process of the specified application, here the activity diagram is used again but for providing low level information.
To get details on activity diagram,[What the application is supposed to be ?]({{ page.relativePath }}/define-the-application.html).

### <a name="composite-structure-diagram"></a> Define the system interfaces

Then for each component, John details the internal structure of a component thanks to **Composite structure diagrams**.

The composite structure diagram is used to describe the structure of the system by showing the internal structure of classes and the interfaces they used to collaborate.

![]({{page.relativePath}}/images/CompositeStructureDiagram.png)

The composite structure diagram is an unsynchronized diagram which means that the user has to add existing elements manually on the diagram to see them.

#### Manage nodes

It is possible to **create a type** by selecting the type creation tool from the palette and then clicking on the diagram or an element.
A diagram is associated to a package and when the user click on the diagram background the element is created under the corresponding package in the UML model.
If the user selects a container, the element will be created under the corresponding semantic element in the UML model.

![]({{page.relativePath}}/images/CompositeStructureDiagramPalette.png)

Tooltip tools are also available to create any kind of elements.

Creation tools are available in the composite structure diagram for the following types :

| Element                    | Representation                                          | Comments                                            |
|----------------------------|---------------------------------------------------------|-----------------------------------------------------|
| Component                  | ![]({{page.relativePath}}/images/ComponentDiagramComponent.png)             | A modular part of a system                          |
| Component into a component | ![]({{page.relativePath}}/images/CompositeStructureDiagramSubComponent.png) | A sub part of a component                           |
| Class                      | ![]({{page.relativePath}}/images/ComponentDiagramClass.png)                 | A representation of objects                         |
| Class into a component     | ![]({{page.relativePath}}/images/CompositeStructureDiagramSubClass.png)     | A representation of objects                         |
| Part                       | ![]({{page.relativePath}}/images/CompositeStructurePart.png)                | Runtime instances of classes or interfaces          |
| Property                   | ![]({{page.relativePath}}/images/CompositeStructureProperty.png)            | Reference a property                                |
| Port on a component        | ![]({{page.relativePath}}/images/ComponentDiagramPort.png)                  | Interaction between a component and its environment |
| Port on a class            | ![]({{page.relativePath}}/images/CompositeStructureDiagramPort.png)         | Interaction between a class and its environment     |

The user can also **delete an element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Manage edges

It is possible to create a relationship by selecting the edge creation tool from the palette and then clicking on a source element and a target element.

The following edge creation tools exist in the palette :

| Element        | Representation                                            | Comments                                        |
|----------------|-----------------------------------------------------------|-------------------------------------------------|
| Connector      | ![]({{page.relativePath}}/images/CompositeStructureConnector.png)             | Illustrate communication links between elements |
| Usage          | ![]({{page.relativePath}}/images/ComponentDiagramUsage.png)                   | Element uses another element                    |
| Generalization | ![]({{page.relativePath}}/images/CompositeStructureDiagramGeneralization.png) | Indicates inheritance                           |
| Redefined      | ![]({{page.relativePath}}/images/ComponentDiagramRedefined.png)               | Indicates that a port redefined another port    |

The user can also **delete an activity element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect relationships**. It is possible to reconnect the source and the target of any kind of edge in the use case diagram :

-   usage
-   dependency
-   component realization
-   interface realization
-   redefined
-   connector

#### Manage existing elements

As the diagram is unsynchronized, the user needs to add manually the elements already existing in the semantic model that should appear on the representation.
It is possible to **add existing elements** by :

-   selecting the add tool from the palette or the tooltip and then clicking on the diagram or an element. The add tool opens a selection wizard.
-   drag and droping an element from the model explorer.

The following elements can be added on a component diagram :

-   component : the component and all its parts, properties and sub components will be visible
-   component into an existing component : the component and all its parts, properties and sub components will be visible
-   class : the class and all its ports will be visible
-   class into an existing component : the class and all its ports will be visible
-   part
-   property
-   interfaces
-   package : the package will not be visible on the diagram but all the sub elements will be added

The user can see that an element is not coming from the current package :

-   the element border is lighter than the element border of elements defined in the current package
-   a tooltip shows the container package of the element if the element is not contained by the current package

And finally, he can **remove an existing element** from a diagram. In this case the element is only deleted from the representation but it is not removed from the UML model. This *Remove* tool exists in the *Existing elements* section in the palette (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Add related elements

In the composite structure diagram a contextual action is available to show on the diagram the element related to the selection.

The **add related elements** action is available from :

-   a component , a class, an interface, a port : shows all the elements that define a relationship (dependency, component realization, interface realization...) with the selected element
-   a composite structure diagram : shows all the elements contained in the package associated to the diagram.

#### Edit labels

In the composite structure diagram, it is possible to edit the elements labels (see [Diagram editor/Editor main graphical area/Direct edit]({{ page.relativePath }}/ref-doc/define-the-system.html#direct-edit)). This actions allows to edit :

-   component, class, interface, port labels
-   relationships labels

### <a name="deployment-diagram"></a> Define the system environment

Then, John defines the system environment thanks to a **deployment diagram**, and how the software is deployed on the infrastructure. This diagram describes the current technological limitations and constraints.

The deployment diagram is used to describe the structure of the system by showing the physical deployment of artifacts on nodes.
![]({{page.relativePath}}/images/DeploymentDiagram.png)

The deployment diagram is an unsynchronized diagram which means that the user has to add existing elements manually on the diagram to see them.

#### Manage nodes

It is possible to create a type by selecting the type creation tool from the palette and then clicking on the diagram or an element.
A diagram is associated to a package and when the user click on the diagram background the element is created under the corresponding package in the UML model.
If the user selects a container, the element will be created under the corresponding semantic element in the UML model.

![]({{page.relativePath}}/images/DeploymentDiagramPalette.png)

Tooltip tools are also available to create any kind of elements. You have the ability to create elements in a contextual way related to the currently selected elements.
If your pointer is on the diagram background, after a few seconds you should see the following assistant :
![]({{page.relativePath}}/images/using_deployment_diagram/assistant.png)
If your pointer is **on a node** the assistant will be :
![]({{page.relativePath}}/images/using_deployment_diagram/assistant_node.png)

Indeed, a node is a composite element.

Creation tools are available in the deployment diagram for the following types :

| Element               | Representation                                          | Comments                                                   |
|-----------------------|---------------------------------------------------------|------------------------------------------------------------|
| Node                  | ![]({{page.relativePath}}/images/DeploymentDiagramNode.png)                 | Physical element on whic the system is deployed            |
| Device                | ![]({{page.relativePath}}/images/DeploymentDiagramDevice.png)               | Physical electronic resource with processing capability    |
| Execution environment | ![]({{page.relativePath}}/images/DeploymentDiagramExecutionEnvironment.png) | Specific node where artifacts are deployed                 |
| Artifact              | ![]({{page.relativePath}}/images/DeploymentDiagramArtifact.png)             | Physical piece of information used or produced by a system |

So, the user can create deployment diagram defining :

-   Device, Execution Environment, Node and links :

    ![]({{page.relativePath}}/images/features/deployment_pics/links_between_nodes.png)
-   Composite nodes :

    ![]({{page.relativePath}}/images/features/deployment_pics/composition.png)

The user can also **delete an activity element** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Manage relationships

It is possible to **create a relationship** by selecting the edge creation tool from the palette and then clicking on a source element and a target element.
The following edge creation tools exist in the palette :

| Element        | Representation                                    | Comments                                                     |
|----------------|---------------------------------------------------|--------------------------------------------------------------|
| Link           | ![]({{page.relativePath}}/images/DeploymentDiagramLink.png)           | General relationship                                         |
| Dependency     | ![]({{page.relativePath}}/images/DeploymentDiagramDependency.png)     | Dependency between elements                                  |
| Generalization | ![]({{page.relativePath}}/images/DeploymentDiagramGeneralization.png) | Indicates inheritance                                        |
| Deployment     | ![]({{page.relativePath}}/images/DeploymentDiagramDeployment.png)     | Indicates the deployment of an artifact on a node            |
| Manifestation  | ![]({{page.relativePath}}/images/DeploymentDiagramManifestation.png)  | An artifact embodies or manifests a number of model elements |

The user can create :

-   artifact dependencies and generalization:
    
    ![]({{page.relativePath}}/images/features/deployment_pics/artifact_dependency_generalization.png)
-   artifact manifestation of packageable elements:
    
    ![]({{page.relativePath}}/images/features/deployment_pics/artifact_manifestation_component_package.png)
-   artifact deployment :
    
    ![]({{page.relativePath}}/images/features/deployment_pics/artifact_deployment.png)
    We have two way to deploy an artifact:
-   Deployment could be shown as a deploy dependency that is drawn from the artifact to the deployment target.
-   Deployment could also be shown with deployed artifacts contained by a deployment target.

The user can also **delete a flow** (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

And finally, he can **reconnect flows**. It is possible to reconnect the source and the target of any kind of edge in the activity diagram :

-   link
-   dependency
-   generalization
-   deployment
-   manifestation

#### Manage existing elements

As the diagram is unsynchronized, the user needs to add manually the elements already existing in the semantic model that should appear on the representation.
It is possible to **add existing elements** by :

-   selecting the add tool from the palette or the tooltip and then clicking on the diagram or an element. The add tool opens a selection wizard.
-   drag and droping an element from the model explorer.

The following elements can be added on a component diagram :

-   node
-   node into a node
-   device
-   device into a node
-   execution environment
-   execution environment into a node
-   artifact
-   artifact into a node
-   component
-   package

The user can see that an element is not coming from the current package :

-   the element border is lighter than the element border of elements defined in the current package
-   a tooltip shows the container package of the element if the element is not contained by the current package

And finally, he can **remove an existing element** from a diagram. In this case the element is only deleted from the representation but it is not removed from the UML model. This *Remove* tool exists in the *Existing elements* section in the palette (see [Diagram editor/Editor tab-bar/Delete element/from model]({{ page.relativePath }}/ref-doc/define-the-system.html#delete-element-from-model)).

#### Add related elements

In the deployment diagram a contextual action is available to show on the diagram the element related to the selection.

The **add related elements** action is available from :

-   a component , a node, a device, an execution environment, an artifact : shows all the elements that define a relationship (dependency, deployment, manifestation...) with the selected element
-   a deployment diagram : shows all the elements contained in the package associated to the diagram.

#### Edit labels

In the package diagram, it is possible to edit the elements labels (see [Diagram editor/Editor main graphical area/Direct edit]({{ page.relativePath }}/ref-doc/define-the-system.html#direct-edit)). This actions allows to edit :

-   component, node, device, execution environment, artifact labels
-   relationships labels

We added a few accelerators so that you can quickly edit **labels** on elements or edges just by typing. Typing :

-   `aNewName` will update the label.

### Extend UML standard

#### Define extensions

Sometimes, the UML standard does not provide all the concepts expected by John. Thanks to the **profile diagram**, it is possible to extend the standard to add new concepts or to adapt existing ones. To use the profile diagram, the user must activate the `Extend` viewpoint.

The profile diagram operates at the metamodel level to provide new stereotypes and profiles.

![]({{page.relativePath}}/images/ProfileDiagram.png)

To create a new profile, the user creates a new UML model and selects as root element a **Profile** element.
Then on the newly created UML model, it is possible to create a **new Profile diagram**.

![]({{page.relativePath}}/images/using_profile_diagram/new_profile_diagram_model.png)

Another solution is to **right\_click** on a model element in the Model Explorer and select the menu `New Representation > Profile Diagram`.

![]({{page.relativePath}}/images/using_profile_diagram/new_profile_diagram_menu.png)

The main feature is to create and delete stereotypes in the profile diagram.
A stereotype can be created by selecting the stereotype creation tool from the palette and then clicking on the diagram. A diagram is associated to a package and in this case the element is created under the corresponding package in the UML model.
A tool is available in the palette to **create a stereotype**.

![]({{page.relativePath}}/images/using_profile_diagram/palette_stereotype.png)

![]({{page.relativePath}}/images/using_profile_diagram/stereotype.png)

By default, a stereotype does not extend any metaclass.

A tool is available in the palette to **reference a metaclass**.

![]({{page.relativePath}}/images/using_profile_diagram/palette_metaclass.png)

![]({{page.relativePath}}/images/using_profile_diagram/metaclass.png)

It opens a wizard which proposes all the available UML metaclass:

![]({{page.relativePath}}/images/using_profile_diagram/wizard_metaclass.png)

It is possible to filter the listed metaclass by :

-   Name
-   Only concrete metaclasses
-   Only sub classes of a selected metaclass

A tool is available in the palette to **create extensions** for a stereotype.

![]({{page.relativePath}}/images/using_profile_diagram/palette_extension.png)

![]({{page.relativePath}}/images/using_profile_diagram/extension.png)

According to the context, this tool will create an *Extension* edge linking *Stereotype* to an *Element Import* or a *Generalization* edge linking two *Stereotypes*. An *Element Import* is an UML reference to an imported metaclass in a profile.

![]({{page.relativePath}}/images/using_profile_diagram/wizard_metaclass.png)

Another tool allows the **creation of an UML “Association”** between two stereotypes.

![]({{page.relativePath}}/images/using_profile_diagram/extra_association.png)

Furthermore, this tool can suggest to reuse the existing relationship in the metamodel UML, if this relationship can link the metaclass referenced by the target and the source stereotype of the wanted association.
If the user selects an existing relationship of the UML metamodel, then the tool will import the metaclass of the selected relationship and create a new stereotype that extend this relationship. Besides, the tool link graphically the new created stereotype and the source and target stereotype of the association

![]({{page.relativePath}}/images/using_profile_diagram/wizard_extra_association.png)

Tooltip tools are also available to create any kind of elements.

The palette defines the following tools :

-   ***Stereotype*** : Create a new stereotype. The user selects the tool in the palette or the tooltip and selects the diagram background. A new stereotype looks like a UML class and contains in its label the keyword *stereotype*. By default a stereotype does not extend any metaclass. But when the user validates the UML profile, a warning is thrown when a stereotype does not extend, directly or indirectly, a metaclass.
-   ***MetaClass*** : Reference an existing metaclass. This tool opens a wizard which lists the UML metaclasses not already referenced in this profile. This wizard provides filters in order to show only the concretes classes or a sub part of the metamodel.
-   ***Attribute*** : Add a new property in a stereotype. After stereotype application, this property will be available in the property box.
-   ***Extension*** : Create an extension between a stereotype and a metaclass or create a generalization between to stereotypes, depending on the clicked elements. This tool also creates the base XXXX attributes which must not be visible on the diagram.
-   ***Association*** : Create an association between two stereotypes or a stereotype and a referenced metaclass. In the UML model, this tool creates a property in the stereotype and a navigable association to the target. This tool opens a wizard which also allows create a new association at UML level. This tool can also propose an existing directed relationship from UML, between these elements. If the user selects it, it will import the directed relationship into the profile and create a new stereotype extending it. The tool will display the association between source and target element, and link this new stereotype to it.
-   ***Enumeration*** : Create an enumeration within the profile. The user can also create enumeration literal in it afterwards.
-   ***Define*** : Generate complementary information within the profile in order to apply it dynamically in the current workspace. It mainly contains the UML annotation.
-   ***Undefine*** : Delete from the profile complementary information generated by the define command.
-   ***Export*** : Create or update an eclipse plugin in order to deploy the edited profile in an Eclipse installation. This plugin must contain the profile, all its generated code and populate extensions to register itself to the platform.

#### Defining a profile

The palette provides a tool to **define a profile** in order to be able to apply this one for other UML model in the workspace. This tool add information about the version to the profile as *Ecore Annotation*. Mainly, the information required for the versioning are:

-   Version number
-   Date
-   Author
-   Comment
-   Copyright
    
    ![]({{page.relativePath}}/images/using_profile_diagram/define_profile.png)

Another tool is available to **undefine a profile**, this tool removes all the *EPackage* representing the definition from the profile.

#### Exporting a profile

An *export profile* tool is available from the palette to export a profile as a jar file. This jar can be added to an eclipse platform to provide a profile as a registered package. The export operation creates an EMF project with an ecore file based on the profile model. Then an extension for the profile is added to the generated project (in “uml.generated\_package” and “ecore.uri\_mapping”). Finally, the tool builds and exports the created EMF project for the profile as a Deployable plug-in.
The tool requires some necessary information for the creation of the deployable plug-in:

-   Profile name, which is editable in the profile model.
-   Profile URI.
-   Profile plug-in name.
-   Version information
    
    ![]({{page.relativePath}}/images/using_profile_diagram/export_profile.png)

#### Manage profiles and stereotypes

In UML Designer, a *Profiles* layer is available on all the diagrams. To describe his application John opens the existing diagrams and activates the profiles layer.

![]({{page.relativePath}}/images/ProfileLayer.png)

This layer provides a new section in the palette.

![]({{page.relativePath}}/images/ProfileLayerPalette.png)

A new tool ***Stereotypes*** is available. Then, the user selects the *Stereotypes* tool in the palette and selects an element in the diagram, a wizards opens which shows the applicable and already applied stereotypes according to the available profiles. The stereotypes wizard lists all the stereotypes even if the profile was not applied before on the parent package. The tool will automatically applies the profiles before applying the selected stereotypes.

![]({{page.relativePath}}/images/ProfileLayerStereotypesWizard.png)

When a stereotype is applied on an element, a keyword representing the name of the stereotype is added before the label of the element :

![]({{page.relativePath}}/images/ClassWithStereotype.png)

It is also possible to manage from the property view :

-   the stereotypes in the **Stereotypes** tab. For example if the user selects a class, he will see:
    
    ![]({{page.relativePath}}/images/ManageStereotypesFromPropertyView.png)

-   the profiles in the **Profiles** tab available on *Package* elements. For example if the user selects a package (or the background of a class diagram as usually it is associated to a package) :
    
    ![]({{page.relativePath}}/images/ManageProfilesFromPropertyView.png)

If the profile defines some properties on the stereotypes, these properties are available in the property box, after canonical properties of the element. Here is a sample with a Stereotype adding a “tagged value” on a package:

![]({{page.relativePath}}/images/ProfileDiagramTaggedValue.png)

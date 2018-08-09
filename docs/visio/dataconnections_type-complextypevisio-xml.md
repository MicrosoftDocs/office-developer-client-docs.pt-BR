---
title: DataConnections_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771655"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="cee48-102">DataConnections_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cee48-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cee48-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="cee48-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cee48-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cee48-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cee48-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cee48-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cee48-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cee48-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cee48-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="cee48-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cee48-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cee48-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cee48-109">Definição</span><span class="sxs-lookup"><span data-stu-id="cee48-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cee48-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cee48-110">Elements and attributes</span></span>

<span data-ttu-id="cee48-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cee48-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cee48-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cee48-112">Child elements</span></span>

|<span data-ttu-id="cee48-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cee48-113">**Element**</span></span>|<span data-ttu-id="cee48-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cee48-114">**Type**</span></span>|<span data-ttu-id="cee48-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cee48-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cee48-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="cee48-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cee48-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="cee48-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cee48-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="cee48-118">Attributes</span></span>

|<span data-ttu-id="cee48-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cee48-119">**Attribute**</span></span>|<span data-ttu-id="cee48-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cee48-120">**Type**</span></span>|<span data-ttu-id="cee48-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cee48-121">**Required**</span></span>|<span data-ttu-id="cee48-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cee48-122">**Description**</span></span>|<span data-ttu-id="cee48-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cee48-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cee48-124">NextID</span><span class="sxs-lookup"><span data-stu-id="cee48-124">NextID</span></span>  <br/> |<span data-ttu-id="cee48-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cee48-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cee48-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cee48-126">required</span></span>  <br/> ||<span data-ttu-id="cee48-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cee48-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


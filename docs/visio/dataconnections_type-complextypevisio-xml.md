---
title: DataConnections_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542454"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="044e8-102">DataConnections_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="044e8-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="044e8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="044e8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="044e8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="044e8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="044e8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="044e8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="044e8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="044e8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="044e8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="044e8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="044e8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="044e8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="044e8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="044e8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="044e8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="044e8-110">Elements and attributes</span></span>

<span data-ttu-id="044e8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="044e8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="044e8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="044e8-112">Child elements</span></span>

|<span data-ttu-id="044e8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="044e8-113">**Element**</span></span>|<span data-ttu-id="044e8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="044e8-114">**Type**</span></span>|<span data-ttu-id="044e8-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="044e8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="044e8-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="044e8-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="044e8-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="044e8-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="044e8-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="044e8-118">Attributes</span></span>

|<span data-ttu-id="044e8-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="044e8-119">**Attribute**</span></span>|<span data-ttu-id="044e8-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="044e8-120">**Type**</span></span>|<span data-ttu-id="044e8-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="044e8-121">**Required**</span></span>|<span data-ttu-id="044e8-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="044e8-122">**Description**</span></span>|<span data-ttu-id="044e8-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="044e8-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="044e8-124">NextID</span><span class="sxs-lookup"><span data-stu-id="044e8-124">NextID</span></span>  <br/> |<span data-ttu-id="044e8-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="044e8-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="044e8-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="044e8-126">required</span></span>  <br/> ||<span data-ttu-id="044e8-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="044e8-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


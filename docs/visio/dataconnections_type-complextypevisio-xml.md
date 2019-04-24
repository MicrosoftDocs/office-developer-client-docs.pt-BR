---
title: DataConnections_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 2bbea48e1d5340c5a68bbafbef9a900a98357385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360372"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="f72e7-102">DataConnections_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f72e7-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f72e7-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f72e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f72e7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f72e7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f72e7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f72e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f72e7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f72e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f72e7-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f72e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f72e7-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f72e7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f72e7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f72e7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f72e7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f72e7-110">Elements and attributes</span></span>

<span data-ttu-id="f72e7-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f72e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f72e7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f72e7-112">Child elements</span></span>

|<span data-ttu-id="f72e7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f72e7-113">**Element**</span></span>|<span data-ttu-id="f72e7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f72e7-114">**Type**</span></span>|<span data-ttu-id="f72e7-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f72e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f72e7-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="f72e7-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f72e7-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="f72e7-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f72e7-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f72e7-118">Attributes</span></span>

|<span data-ttu-id="f72e7-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f72e7-119">**Attribute**</span></span>|<span data-ttu-id="f72e7-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f72e7-120">**Type**</span></span>|<span data-ttu-id="f72e7-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f72e7-121">**Required**</span></span>|<span data-ttu-id="f72e7-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f72e7-122">**Description**</span></span>|<span data-ttu-id="f72e7-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f72e7-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f72e7-124">NextID</span><span class="sxs-lookup"><span data-stu-id="f72e7-124">NextID</span></span>  <br/> |<span data-ttu-id="f72e7-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f72e7-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f72e7-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f72e7-126">required</span></span>  <br/> ||<span data-ttu-id="f72e7-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f72e7-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


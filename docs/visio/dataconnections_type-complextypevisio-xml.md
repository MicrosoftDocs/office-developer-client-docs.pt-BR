---
title: DataConnections_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 2bbea48e1d5340c5a68bbafbef9a900a98357385
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397384"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="68acc-102">DataConnections_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="68acc-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="68acc-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="68acc-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68acc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68acc-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="68acc-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="68acc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="68acc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="68acc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="68acc-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="68acc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="68acc-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68acc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68acc-109">Definição</span><span class="sxs-lookup"><span data-stu-id="68acc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="68acc-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="68acc-110">Elements and attributes</span></span>

<span data-ttu-id="68acc-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="68acc-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="68acc-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="68acc-112">Child elements</span></span>

|<span data-ttu-id="68acc-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="68acc-113">**Element**</span></span>|<span data-ttu-id="68acc-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="68acc-114">**Type**</span></span>|<span data-ttu-id="68acc-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68acc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68acc-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="68acc-116">DataConnection element</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68acc-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="68acc-117">DataConnection_Type complexType</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="68acc-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="68acc-118">Attributes</span></span>

|<span data-ttu-id="68acc-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="68acc-119">**Attribute**</span></span>|<span data-ttu-id="68acc-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="68acc-120">**Type**</span></span>|<span data-ttu-id="68acc-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="68acc-121">**Required**</span></span>|<span data-ttu-id="68acc-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68acc-122">**Description**</span></span>|<span data-ttu-id="68acc-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="68acc-123">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68acc-124">NextID</span><span class="sxs-lookup"><span data-stu-id="68acc-124">NextID</span></span>  <br/> |<span data-ttu-id="68acc-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68acc-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68acc-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="68acc-126">required</span></span>  <br/> ||<span data-ttu-id="68acc-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="68acc-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: Elemento DataConnections ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contém os elementos DataConnection para o documento.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395025"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="92b1f-103">Elemento DataConnections ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="92b1f-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="92b1f-104">Contém os elementos **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="92b1f-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="92b1f-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="92b1f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92b1f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="92b1f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="92b1f-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="92b1f-107">DataConnections_Type complexType</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="92b1f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92b1f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="92b1f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="92b1f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="92b1f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="92b1f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="92b1f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="92b1f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="92b1f-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="92b1f-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92b1f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="92b1f-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92b1f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="92b1f-114">Elements and attributes</span></span>

<span data-ttu-id="92b1f-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="92b1f-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="92b1f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="92b1f-116">Parent elements</span></span>

<span data-ttu-id="92b1f-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="92b1f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92b1f-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="92b1f-118">Child elements</span></span>

|<span data-ttu-id="92b1f-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="92b1f-119">**Element**</span></span>|<span data-ttu-id="92b1f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="92b1f-120">**Type**</span></span>|<span data-ttu-id="92b1f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="92b1f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92b1f-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="92b1f-122">DataConnection element</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92b1f-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="92b1f-123">DataConnection_Type complexType</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92b1f-124">Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não-XML.</span><span class="sxs-lookup"><span data-stu-id="92b1f-124">Abstracts communication between one or more DataRecordset objects and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="92b1f-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="92b1f-125">Attributes</span></span>

|<span data-ttu-id="92b1f-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="92b1f-126">**Attribute**</span></span>|<span data-ttu-id="92b1f-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="92b1f-127">**Type**</span></span>|<span data-ttu-id="92b1f-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="92b1f-128">**Required**</span></span>|<span data-ttu-id="92b1f-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="92b1f-129">**Description**</span></span>|<span data-ttu-id="92b1f-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="92b1f-130">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92b1f-131">NextID</span><span class="sxs-lookup"><span data-stu-id="92b1f-131">NextID</span></span>  <br/> |<span data-ttu-id="92b1f-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92b1f-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92b1f-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="92b1f-133">required</span></span>  <br/> |<span data-ttu-id="92b1f-134">A próxima ID disponível para novas conexões.</span><span class="sxs-lookup"><span data-stu-id="92b1f-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="92b1f-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="92b1f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: DataConnection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344601"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="2d711-102">DataConnection_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2d711-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2d711-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2d711-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d711-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2d711-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2d711-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d711-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2d711-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2d711-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2d711-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2d711-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2d711-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2d711-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2d711-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2d711-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2d711-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2d711-110">Elements and attributes</span></span>

<span data-ttu-id="2d711-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2d711-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2d711-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2d711-112">Child elements</span></span>

<span data-ttu-id="2d711-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2d711-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d711-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d711-114">Attributes</span></span>

|<span data-ttu-id="2d711-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2d711-115">**Attribute**</span></span>|<span data-ttu-id="2d711-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d711-116">**Type**</span></span>|<span data-ttu-id="2d711-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2d711-117">**Required**</span></span>|<span data-ttu-id="2d711-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d711-118">**Description**</span></span>|<span data-ttu-id="2d711-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2d711-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2d711-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="2d711-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="2d711-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2d711-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2d711-122">opcional</span><span class="sxs-lookup"><span data-stu-id="2d711-122">optional</span></span>  <br/> ||<span data-ttu-id="2d711-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2d711-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2d711-124">Comando</span><span class="sxs-lookup"><span data-stu-id="2d711-124">Command</span></span>  <br/> |<span data-ttu-id="2d711-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d711-125">xsd:string</span></span>  <br/> |<span data-ttu-id="2d711-126">opcional</span><span class="sxs-lookup"><span data-stu-id="2d711-126">optional</span></span>  <br/> ||<span data-ttu-id="2d711-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d711-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d711-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2d711-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="2d711-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d711-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2d711-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2d711-130">optional</span></span>  <br/> ||<span data-ttu-id="2d711-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d711-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d711-132">FileName</span><span class="sxs-lookup"><span data-stu-id="2d711-132">FileName</span></span>  <br/> |<span data-ttu-id="2d711-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d711-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2d711-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2d711-134">required</span></span>  <br/> ||<span data-ttu-id="2d711-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d711-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d711-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2d711-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="2d711-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2d711-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2d711-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2d711-138">optional</span></span>  <br/> ||<span data-ttu-id="2d711-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2d711-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2d711-140">ID</span><span class="sxs-lookup"><span data-stu-id="2d711-140">ID</span></span>  <br/> |<span data-ttu-id="2d711-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2d711-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2d711-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2d711-142">required</span></span>  <br/> ||<span data-ttu-id="2d711-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2d711-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2d711-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="2d711-144">Timeout</span></span>  <br/> |<span data-ttu-id="2d711-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2d711-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2d711-146">opcional</span><span class="sxs-lookup"><span data-stu-id="2d711-146">optional</span></span>  <br/> ||<span data-ttu-id="2d711-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2d711-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: DataConnection_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539646"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="53b5a-102">DataConnection_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="53b5a-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="53b5a-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="53b5a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53b5a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="53b5a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="53b5a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="53b5a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="53b5a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="53b5a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="53b5a-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="53b5a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="53b5a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="53b5a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53b5a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="53b5a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="53b5a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="53b5a-110">Elements and attributes</span></span>

<span data-ttu-id="53b5a-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="53b5a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="53b5a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="53b5a-112">Child elements</span></span>

<span data-ttu-id="53b5a-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="53b5a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53b5a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="53b5a-114">Attributes</span></span>

|<span data-ttu-id="53b5a-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="53b5a-115">**Attribute**</span></span>|<span data-ttu-id="53b5a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="53b5a-116">**Type**</span></span>|<span data-ttu-id="53b5a-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="53b5a-117">**Required**</span></span>|<span data-ttu-id="53b5a-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53b5a-118">**Description**</span></span>|<span data-ttu-id="53b5a-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="53b5a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53b5a-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="53b5a-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="53b5a-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="53b5a-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="53b5a-122">opcional</span><span class="sxs-lookup"><span data-stu-id="53b5a-122">optional</span></span>  <br/> ||<span data-ttu-id="53b5a-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="53b5a-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-124">Comando</span><span class="sxs-lookup"><span data-stu-id="53b5a-124">Command</span></span>  <br/> |<span data-ttu-id="53b5a-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="53b5a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="53b5a-126">opcional</span><span class="sxs-lookup"><span data-stu-id="53b5a-126">optional</span></span>  <br/> ||<span data-ttu-id="53b5a-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="53b5a-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="53b5a-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="53b5a-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="53b5a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="53b5a-130">opcional</span><span class="sxs-lookup"><span data-stu-id="53b5a-130">optional</span></span>  <br/> ||<span data-ttu-id="53b5a-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="53b5a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-132">FileName</span><span class="sxs-lookup"><span data-stu-id="53b5a-132">FileName</span></span>  <br/> |<span data-ttu-id="53b5a-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="53b5a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="53b5a-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="53b5a-134">required</span></span>  <br/> ||<span data-ttu-id="53b5a-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="53b5a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="53b5a-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="53b5a-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="53b5a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="53b5a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="53b5a-138">optional</span></span>  <br/> ||<span data-ttu-id="53b5a-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="53b5a-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-140">ID</span><span class="sxs-lookup"><span data-stu-id="53b5a-140">ID</span></span>  <br/> |<span data-ttu-id="53b5a-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="53b5a-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="53b5a-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="53b5a-142">required</span></span>  <br/> ||<span data-ttu-id="53b5a-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="53b5a-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="53b5a-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="53b5a-144">Timeout</span></span>  <br/> |<span data-ttu-id="53b5a-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="53b5a-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="53b5a-146">opcional</span><span class="sxs-lookup"><span data-stu-id="53b5a-146">optional</span></span>  <br/> ||<span data-ttu-id="53b5a-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="53b5a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


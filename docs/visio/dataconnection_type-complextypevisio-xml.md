---
title: DataConnection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389138"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="9a913-102">DataConnection_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9a913-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9a913-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="9a913-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a913-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a913-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a913-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9a913-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a913-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a913-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a913-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="9a913-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a913-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9a913-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a913-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9a913-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9a913-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9a913-110">Elements and attributes</span></span>

<span data-ttu-id="9a913-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9a913-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a913-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9a913-112">Child elements</span></span>

<span data-ttu-id="9a913-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9a913-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a913-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a913-114">Attributes</span></span>

|<span data-ttu-id="9a913-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9a913-115">**Attribute**</span></span>|<span data-ttu-id="9a913-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a913-116">**Type**</span></span>|<span data-ttu-id="9a913-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9a913-117">**Required**</span></span>|<span data-ttu-id="9a913-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a913-118">**Description**</span></span>|<span data-ttu-id="9a913-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9a913-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a913-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="9a913-120">AlwaysUseConnectionFile Property</span></span>  <br/> |<span data-ttu-id="9a913-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a913-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a913-122">opcional</span><span class="sxs-lookup"><span data-stu-id="9a913-122">optional</span></span>  <br/> ||<span data-ttu-id="9a913-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a913-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a913-124">Comando</span><span class="sxs-lookup"><span data-stu-id="9a913-124">Command</span></span>  <br/> |<span data-ttu-id="9a913-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a913-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9a913-126">opcional</span><span class="sxs-lookup"><span data-stu-id="9a913-126">optional</span></span>  <br/> ||<span data-ttu-id="9a913-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a913-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a913-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9a913-128">ConnectionString Property</span></span>  <br/> |<span data-ttu-id="9a913-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a913-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9a913-130">opcional</span><span class="sxs-lookup"><span data-stu-id="9a913-130">optional</span></span>  <br/> ||<span data-ttu-id="9a913-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a913-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a913-132">FileName</span><span class="sxs-lookup"><span data-stu-id="9a913-132">fileName</span></span>  <br/> |<span data-ttu-id="9a913-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a913-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9a913-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9a913-134">required</span></span>  <br/> ||<span data-ttu-id="9a913-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a913-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a913-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9a913-136">FriendlyName element</span></span>  <br/> |<span data-ttu-id="9a913-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a913-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9a913-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9a913-138">optional</span></span>  <br/> ||<span data-ttu-id="9a913-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a913-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a913-140">ID</span><span class="sxs-lookup"><span data-stu-id="9a913-140">ID</span></span>  <br/> |<span data-ttu-id="9a913-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a913-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a913-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9a913-142">required</span></span>  <br/> ||<span data-ttu-id="9a913-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a913-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a913-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="9a913-144">Timeout</span></span>  <br/> |<span data-ttu-id="9a913-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a913-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a913-146">opcional</span><span class="sxs-lookup"><span data-stu-id="9a913-146">optional</span></span>  <br/> ||<span data-ttu-id="9a913-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a913-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


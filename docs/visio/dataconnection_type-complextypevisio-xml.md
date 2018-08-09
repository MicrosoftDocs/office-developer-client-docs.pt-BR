---
title: DataConnection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 3a900e22fd36c936f689081149b484bd5e7460fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771667"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="8a27b-102">DataConnection_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8a27b-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8a27b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="8a27b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a27b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8a27b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8a27b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8a27b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8a27b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8a27b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8a27b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="8a27b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8a27b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8a27b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a27b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="8a27b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8a27b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8a27b-110">Elements and attributes</span></span>

<span data-ttu-id="8a27b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8a27b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8a27b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8a27b-112">Child elements</span></span>

<span data-ttu-id="8a27b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8a27b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a27b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="8a27b-114">Attributes</span></span>

|<span data-ttu-id="8a27b-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8a27b-115">**Attribute**</span></span>|<span data-ttu-id="8a27b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8a27b-116">**Type**</span></span>|<span data-ttu-id="8a27b-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8a27b-117">**Required**</span></span>|<span data-ttu-id="8a27b-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a27b-118">**Description**</span></span>|<span data-ttu-id="8a27b-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8a27b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8a27b-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="8a27b-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="8a27b-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8a27b-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8a27b-122">opcional</span><span class="sxs-lookup"><span data-stu-id="8a27b-122">optional</span></span>  <br/> ||<span data-ttu-id="8a27b-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8a27b-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-124">Command</span><span class="sxs-lookup"><span data-stu-id="8a27b-124">Command</span></span>  <br/> |<span data-ttu-id="8a27b-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8a27b-125">xsd:string</span></span>  <br/> |<span data-ttu-id="8a27b-126">opcional</span><span class="sxs-lookup"><span data-stu-id="8a27b-126">optional</span></span>  <br/> ||<span data-ttu-id="8a27b-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8a27b-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8a27b-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="8a27b-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8a27b-129">xsd:string</span></span>  <br/> |<span data-ttu-id="8a27b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="8a27b-130">optional</span></span>  <br/> ||<span data-ttu-id="8a27b-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8a27b-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-132">FileName</span><span class="sxs-lookup"><span data-stu-id="8a27b-132">FileName</span></span>  <br/> |<span data-ttu-id="8a27b-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8a27b-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8a27b-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8a27b-134">required</span></span>  <br/> ||<span data-ttu-id="8a27b-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8a27b-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8a27b-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="8a27b-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8a27b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8a27b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8a27b-138">optional</span></span>  <br/> ||<span data-ttu-id="8a27b-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8a27b-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-140">ID</span><span class="sxs-lookup"><span data-stu-id="8a27b-140">ID</span></span>  <br/> |<span data-ttu-id="8a27b-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a27b-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a27b-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8a27b-142">required</span></span>  <br/> ||<span data-ttu-id="8a27b-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a27b-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a27b-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="8a27b-144">Timeout</span></span>  <br/> |<span data-ttu-id="8a27b-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a27b-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a27b-146">opcional</span><span class="sxs-lookup"><span data-stu-id="8a27b-146">optional</span></span>  <br/> ||<span data-ttu-id="8a27b-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a27b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


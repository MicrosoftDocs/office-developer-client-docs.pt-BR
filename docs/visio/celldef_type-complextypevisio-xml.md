---
title: CellDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771469"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="10a0e-102">CellDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="10a0e-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="10a0e-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="10a0e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10a0e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10a0e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10a0e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="10a0e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10a0e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="10a0e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10a0e-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="10a0e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10a0e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10a0e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10a0e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="10a0e-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10a0e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="10a0e-110">Elements and attributes</span></span>

<span data-ttu-id="10a0e-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="10a0e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10a0e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="10a0e-112">Child elements</span></span>

<span data-ttu-id="10a0e-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="10a0e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10a0e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="10a0e-114">Attributes</span></span>

|<span data-ttu-id="10a0e-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="10a0e-115">**Attribute**</span></span>|<span data-ttu-id="10a0e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="10a0e-116">**Type**</span></span>|<span data-ttu-id="10a0e-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="10a0e-117">**Required**</span></span>|<span data-ttu-id="10a0e-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10a0e-118">**Description**</span></span>|<span data-ttu-id="10a0e-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="10a0e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10a0e-120">S</span><span class="sxs-lookup"><span data-stu-id="10a0e-120">F</span></span>  <br/> |<span data-ttu-id="10a0e-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="10a0e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="10a0e-122">opcional</span><span class="sxs-lookup"><span data-stu-id="10a0e-122">optional</span></span>  <br/> ||<span data-ttu-id="10a0e-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="10a0e-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10a0e-124">IX</span><span class="sxs-lookup"><span data-stu-id="10a0e-124">IX</span></span>  <br/> |<span data-ttu-id="10a0e-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="10a0e-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="10a0e-126">opcional</span><span class="sxs-lookup"><span data-stu-id="10a0e-126">optional</span></span>  <br/> ||<span data-ttu-id="10a0e-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="10a0e-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="10a0e-128">N</span><span class="sxs-lookup"><span data-stu-id="10a0e-128">N</span></span>  <br/> |<span data-ttu-id="10a0e-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="10a0e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="10a0e-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="10a0e-130">required</span></span>  <br/> ||<span data-ttu-id="10a0e-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="10a0e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10a0e-132">S</span><span class="sxs-lookup"><span data-stu-id="10a0e-132">S</span></span>  <br/> |<span data-ttu-id="10a0e-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="10a0e-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="10a0e-134">opcional</span><span class="sxs-lookup"><span data-stu-id="10a0e-134">optional</span></span>  <br/> ||<span data-ttu-id="10a0e-135">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="10a0e-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="10a0e-136">T</span><span class="sxs-lookup"><span data-stu-id="10a0e-136">T</span></span>  <br/> |<span data-ttu-id="10a0e-137">XSD:token</span><span class="sxs-lookup"><span data-stu-id="10a0e-137">xsd:token</span></span>  <br/> |<span data-ttu-id="10a0e-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="10a0e-138">required</span></span>  <br/> ||<span data-ttu-id="10a0e-139">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="10a0e-139">Values of the xsd:token type.</span></span>  <br/> |
   


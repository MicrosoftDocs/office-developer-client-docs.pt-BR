---
title: DocumentSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771755"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="4e537-102">DocumentSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4e537-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4e537-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4e537-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e537-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4e537-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4e537-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4e537-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4e537-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4e537-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4e537-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4e537-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4e537-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="4e537-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4e537-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4e537-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4e537-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4e537-110">Elements and attributes</span></span>

<span data-ttu-id="4e537-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4e537-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4e537-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4e537-112">Child elements</span></span>

<span data-ttu-id="4e537-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4e537-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e537-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e537-114">Attributes</span></span>

|<span data-ttu-id="4e537-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4e537-115">**Attribute**</span></span>|<span data-ttu-id="4e537-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4e537-116">**Type**</span></span>|<span data-ttu-id="4e537-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4e537-117">**Required**</span></span>|<span data-ttu-id="4e537-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e537-118">**Description**</span></span>|<span data-ttu-id="4e537-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4e537-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4e537-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="4e537-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="4e537-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="4e537-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4e537-122">opcional</span><span class="sxs-lookup"><span data-stu-id="4e537-122">optional</span></span>  <br/> ||<span data-ttu-id="4e537-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4e537-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4e537-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4e537-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4e537-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="4e537-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4e537-126">opcional</span><span class="sxs-lookup"><span data-stu-id="4e537-126">optional</span></span>  <br/> ||<span data-ttu-id="4e537-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4e537-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4e537-128">Nome</span><span class="sxs-lookup"><span data-stu-id="4e537-128">Name</span></span>  <br/> |<span data-ttu-id="4e537-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4e537-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4e537-130">opcional</span><span class="sxs-lookup"><span data-stu-id="4e537-130">optional</span></span>  <br/> ||<span data-ttu-id="4e537-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4e537-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4e537-132">NameU</span><span class="sxs-lookup"><span data-stu-id="4e537-132">NameU</span></span>  <br/> |<span data-ttu-id="4e537-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4e537-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4e537-134">opcional</span><span class="sxs-lookup"><span data-stu-id="4e537-134">optional</span></span>  <br/> ||<span data-ttu-id="4e537-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4e537-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4e537-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="4e537-136">UniqueID</span></span>  <br/> |<span data-ttu-id="4e537-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4e537-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4e537-138">opcional</span><span class="sxs-lookup"><span data-stu-id="4e537-138">optional</span></span>  <br/> ||<span data-ttu-id="4e537-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4e537-139">Values of the xsd:string type.</span></span>  <br/> |
   


---
title: ColorEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394906"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="935ae-102">ColorEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="935ae-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="935ae-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="935ae-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="935ae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="935ae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="935ae-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="935ae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="935ae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="935ae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="935ae-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="935ae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="935ae-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="935ae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="935ae-109">Definição</span><span class="sxs-lookup"><span data-stu-id="935ae-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="935ae-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="935ae-110">Elements and attributes</span></span>

<span data-ttu-id="935ae-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="935ae-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="935ae-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="935ae-112">Child elements</span></span>

<span data-ttu-id="935ae-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="935ae-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="935ae-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="935ae-114">Attributes</span></span>

|<span data-ttu-id="935ae-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="935ae-115">**Attribute**</span></span>|<span data-ttu-id="935ae-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="935ae-116">**Type**</span></span>|<span data-ttu-id="935ae-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="935ae-117">**Required**</span></span>|<span data-ttu-id="935ae-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="935ae-118">**Description**</span></span>|<span data-ttu-id="935ae-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="935ae-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="935ae-120">IX</span><span class="sxs-lookup"><span data-stu-id="935ae-120">IX</span></span>  <br/> |<span data-ttu-id="935ae-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935ae-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="935ae-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="935ae-122">required</span></span>  <br/> ||<span data-ttu-id="935ae-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="935ae-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="935ae-124">RGB</span><span class="sxs-lookup"><span data-stu-id="935ae-124">RGB</span></span>  <br/> |<span data-ttu-id="935ae-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="935ae-125">xsd:string</span></span>  <br/> |<span data-ttu-id="935ae-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="935ae-126">required</span></span>  <br/> ||<span data-ttu-id="935ae-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="935ae-127">Values of the xsd:string type.</span></span>  <br/> |
   


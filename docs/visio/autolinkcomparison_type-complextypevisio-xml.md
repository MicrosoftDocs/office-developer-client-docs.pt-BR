---
title: AutoLinkComparison_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389747"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="c736c-102">AutoLinkComparison_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c736c-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c736c-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c736c-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c736c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c736c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c736c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c736c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c736c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c736c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c736c-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c736c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c736c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c736c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c736c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c736c-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c736c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c736c-110">Elements and attributes</span></span>

<span data-ttu-id="c736c-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c736c-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c736c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c736c-112">Child elements</span></span>

<span data-ttu-id="c736c-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c736c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c736c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c736c-114">Attributes</span></span>

|<span data-ttu-id="c736c-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c736c-115">**Attribute**</span></span>|<span data-ttu-id="c736c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c736c-116">**Type**</span></span>|<span data-ttu-id="c736c-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c736c-117">**Required**</span></span>|<span data-ttu-id="c736c-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c736c-118">**Description**</span></span>|<span data-ttu-id="c736c-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c736c-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c736c-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="c736c-120">columnName</span></span>  <br/> |<span data-ttu-id="c736c-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c736c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="c736c-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c736c-122">required</span></span>  <br/> ||<span data-ttu-id="c736c-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c736c-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c736c-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="c736c-124">ContextType</span></span>  <br/> |<span data-ttu-id="c736c-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c736c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c736c-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c736c-126">required</span></span>  <br/> ||<span data-ttu-id="c736c-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c736c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c736c-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="c736c-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="c736c-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c736c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c736c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="c736c-130">optional</span></span>  <br/> ||<span data-ttu-id="c736c-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c736c-131">Values of the xsd:string type.</span></span>  <br/> |
   


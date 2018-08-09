---
title: AutoLinkComparison_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771280"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="ff52f-102">AutoLinkComparison_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ff52f-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff52f-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ff52f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff52f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff52f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff52f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff52f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff52f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff52f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff52f-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ff52f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff52f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff52f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff52f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ff52f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff52f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ff52f-110">Elements and attributes</span></span>

<span data-ttu-id="ff52f-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ff52f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff52f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff52f-112">Child elements</span></span>

<span data-ttu-id="ff52f-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ff52f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff52f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff52f-114">Attributes</span></span>

|<span data-ttu-id="ff52f-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ff52f-115">**Attribute**</span></span>|<span data-ttu-id="ff52f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff52f-116">**Type**</span></span>|<span data-ttu-id="ff52f-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ff52f-117">**Required**</span></span>|<span data-ttu-id="ff52f-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff52f-118">**Description**</span></span>|<span data-ttu-id="ff52f-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ff52f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff52f-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="ff52f-120">ColumnName</span></span>  <br/> |<span data-ttu-id="ff52f-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff52f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="ff52f-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff52f-122">required</span></span>  <br/> ||<span data-ttu-id="ff52f-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff52f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff52f-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="ff52f-124">ContextType</span></span>  <br/> |<span data-ttu-id="ff52f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff52f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff52f-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff52f-126">required</span></span>  <br/> ||<span data-ttu-id="ff52f-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff52f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff52f-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="ff52f-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="ff52f-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff52f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="ff52f-130">opcional</span><span class="sxs-lookup"><span data-stu-id="ff52f-130">optional</span></span>  <br/> ||<span data-ttu-id="ff52f-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff52f-131">Values of the xsd:string type.</span></span>  <br/> |
   

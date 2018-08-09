---
title: RowKeyValue_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: dcd4c972aac1e86fa7a66766a756ebef2cca7c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772794"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="54f9d-102">RowKeyValue_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="54f9d-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="54f9d-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="54f9d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54f9d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="54f9d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="54f9d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="54f9d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="54f9d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="54f9d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="54f9d-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="54f9d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="54f9d-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="54f9d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54f9d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="54f9d-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54f9d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="54f9d-110">Elements and attributes</span></span>

<span data-ttu-id="54f9d-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="54f9d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="54f9d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="54f9d-112">Child elements</span></span>

<span data-ttu-id="54f9d-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="54f9d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54f9d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="54f9d-114">Attributes</span></span>

|<span data-ttu-id="54f9d-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="54f9d-115">**Attribute**</span></span>|<span data-ttu-id="54f9d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="54f9d-116">**Type**</span></span>|<span data-ttu-id="54f9d-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="54f9d-117">**Required**</span></span>|<span data-ttu-id="54f9d-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54f9d-118">**Description**</span></span>|<span data-ttu-id="54f9d-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="54f9d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54f9d-120">RowID</span><span class="sxs-lookup"><span data-stu-id="54f9d-120">RowID</span></span>  <br/> |<span data-ttu-id="54f9d-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54f9d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54f9d-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="54f9d-122">required</span></span>  <br/> ||<span data-ttu-id="54f9d-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="54f9d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="54f9d-124">Value</span><span class="sxs-lookup"><span data-stu-id="54f9d-124">Value</span></span>  <br/> |<span data-ttu-id="54f9d-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="54f9d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="54f9d-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="54f9d-126">required</span></span>  <br/> ||<span data-ttu-id="54f9d-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="54f9d-127">Values of the xsd:string type.</span></span>  <br/> |
   


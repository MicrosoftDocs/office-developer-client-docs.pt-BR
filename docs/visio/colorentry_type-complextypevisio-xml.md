---
title: ColorEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771509"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="c0c61-102">ColorEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c0c61-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c0c61-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="c0c61-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0c61-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0c61-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c0c61-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c0c61-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c0c61-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c0c61-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c0c61-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="c0c61-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c0c61-108">None</span><span class="sxs-lookup"><span data-stu-id="c0c61-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0c61-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c0c61-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c0c61-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c0c61-110">Elements and attributes</span></span>

<span data-ttu-id="c0c61-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c0c61-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c0c61-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c0c61-112">Child elements</span></span>

<span data-ttu-id="c0c61-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c0c61-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0c61-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0c61-114">Attributes</span></span>

|<span data-ttu-id="c0c61-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c0c61-115">**Attribute**</span></span>|<span data-ttu-id="c0c61-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c0c61-116">**Type**</span></span>|<span data-ttu-id="c0c61-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c0c61-117">**Required**</span></span>|<span data-ttu-id="c0c61-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c0c61-118">**Description**</span></span>|<span data-ttu-id="c0c61-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c0c61-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c0c61-120">IX</span><span class="sxs-lookup"><span data-stu-id="c0c61-120">IX</span></span>  <br/> |<span data-ttu-id="c0c61-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0c61-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0c61-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c0c61-122">required</span></span>  <br/> ||<span data-ttu-id="c0c61-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0c61-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0c61-124">RGB</span><span class="sxs-lookup"><span data-stu-id="c0c61-124">RGB</span></span>  <br/> |<span data-ttu-id="c0c61-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c0c61-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c0c61-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c0c61-126">required</span></span>  <br/> ||<span data-ttu-id="c0c61-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c0c61-127">Values of the xsd:string type.</span></span>  <br/> |
   


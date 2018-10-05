---
title: RefBy_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383479"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="acd40-102">RefBy_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="acd40-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="acd40-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="acd40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acd40-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acd40-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="acd40-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="acd40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="acd40-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="acd40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="acd40-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="acd40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="acd40-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="acd40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acd40-109">Definição</span><span class="sxs-lookup"><span data-stu-id="acd40-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acd40-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="acd40-110">Elements and attributes</span></span>

<span data-ttu-id="acd40-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="acd40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="acd40-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="acd40-112">Child elements</span></span>

<span data-ttu-id="acd40-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="acd40-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acd40-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="acd40-114">Attributes</span></span>

|<span data-ttu-id="acd40-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="acd40-115">**Attribute**</span></span>|<span data-ttu-id="acd40-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acd40-116">**Type**</span></span>|<span data-ttu-id="acd40-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="acd40-117">**Required**</span></span>|<span data-ttu-id="acd40-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acd40-118">**Description**</span></span>|<span data-ttu-id="acd40-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="acd40-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="acd40-120">ID</span><span class="sxs-lookup"><span data-stu-id="acd40-120">ID</span></span>  <br/> |<span data-ttu-id="acd40-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="acd40-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="acd40-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="acd40-122">required</span></span>  <br/> ||<span data-ttu-id="acd40-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="acd40-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="acd40-124">T</span><span class="sxs-lookup"><span data-stu-id="acd40-124">T</span></span>  <br/> |<span data-ttu-id="acd40-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="acd40-125">xsd:string</span></span>  <br/> |<span data-ttu-id="acd40-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="acd40-126">required</span></span>  <br/> ||<span data-ttu-id="acd40-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="acd40-127">Values of the xsd:string type.</span></span>  <br/> |
   


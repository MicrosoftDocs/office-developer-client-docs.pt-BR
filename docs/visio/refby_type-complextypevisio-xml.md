---
title: RefBy_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 5042a618420a72284e0ef75c5d624c6f5464e162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772643"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="67418-102">RefBy_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="67418-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="67418-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="67418-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67418-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67418-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67418-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67418-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67418-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="67418-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67418-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="67418-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67418-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67418-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67418-109">Definição</span><span class="sxs-lookup"><span data-stu-id="67418-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="67418-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="67418-110">Elements and attributes</span></span>

<span data-ttu-id="67418-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="67418-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67418-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="67418-112">Child elements</span></span>

<span data-ttu-id="67418-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="67418-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67418-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="67418-114">Attributes</span></span>

|<span data-ttu-id="67418-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="67418-115">**Attribute**</span></span>|<span data-ttu-id="67418-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67418-116">**Type**</span></span>|<span data-ttu-id="67418-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="67418-117">**Required**</span></span>|<span data-ttu-id="67418-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67418-118">**Description**</span></span>|<span data-ttu-id="67418-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="67418-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67418-120">ID</span><span class="sxs-lookup"><span data-stu-id="67418-120">ID</span></span>  <br/> |<span data-ttu-id="67418-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67418-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67418-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="67418-122">required</span></span>  <br/> ||<span data-ttu-id="67418-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="67418-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67418-124">T</span><span class="sxs-lookup"><span data-stu-id="67418-124">T</span></span>  <br/> |<span data-ttu-id="67418-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="67418-125">xsd:string</span></span>  <br/> |<span data-ttu-id="67418-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="67418-126">required</span></span>  <br/> ||<span data-ttu-id="67418-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="67418-127">Values of the xsd:string type.</span></span>  <br/> |
   


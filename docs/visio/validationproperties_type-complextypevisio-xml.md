---
title: ValidationProperties_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: eb1373881b1584b77c6663dd4ec375c50a61efd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773237"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="bd2a5-102">ValidationProperties_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bd2a5-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bd2a5-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="bd2a5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd2a5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bd2a5-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bd2a5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bd2a5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bd2a5-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bd2a5-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bd2a5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd2a5-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bd2a5-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bd2a5-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bd2a5-110">Elements and attributes</span></span>

<span data-ttu-id="bd2a5-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bd2a5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bd2a5-112">Child elements</span></span>

<span data-ttu-id="bd2a5-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd2a5-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd2a5-114">Attributes</span></span>

|<span data-ttu-id="bd2a5-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-115">**Attribute**</span></span>|<span data-ttu-id="bd2a5-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-116">**Type**</span></span>|<span data-ttu-id="bd2a5-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-117">**Required**</span></span>|<span data-ttu-id="bd2a5-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-118">**Description**</span></span>|<span data-ttu-id="bd2a5-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd2a5-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="bd2a5-120">LastValidated</span></span>  <br/> |<span data-ttu-id="bd2a5-121">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="bd2a5-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="bd2a5-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd2a5-122">required</span></span>  <br/> ||<span data-ttu-id="bd2a5-123">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="bd2a5-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="bd2a5-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="bd2a5-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="bd2a5-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bd2a5-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd2a5-126">required</span></span>  <br/> ||<span data-ttu-id="bd2a5-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-127">Values of the xsd:boolean type.</span></span>  <br/> |
   


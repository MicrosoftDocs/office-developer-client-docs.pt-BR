---
title: IssueTarget_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393765"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="ff591-102">IssueTarget_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ff591-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff591-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ff591-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff591-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff591-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff591-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff591-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff591-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff591-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff591-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ff591-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff591-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff591-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff591-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ff591-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ff591-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ff591-110">Elements and attributes</span></span>

<span data-ttu-id="ff591-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ff591-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff591-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff591-112">Child elements</span></span>

<span data-ttu-id="ff591-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ff591-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff591-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff591-114">Attributes</span></span>

|<span data-ttu-id="ff591-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ff591-115">**Attribute**</span></span>|<span data-ttu-id="ff591-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff591-116">**Type**</span></span>|<span data-ttu-id="ff591-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ff591-117">**Required**</span></span>|<span data-ttu-id="ff591-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff591-118">**Description**</span></span>|<span data-ttu-id="ff591-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ff591-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff591-120">PageID</span><span class="sxs-lookup"><span data-stu-id="ff591-120">PageID</span></span>  <br/> |<span data-ttu-id="ff591-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff591-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff591-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff591-122">required</span></span>  <br/> ||<span data-ttu-id="ff591-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff591-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff591-124">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="ff591-124">ShapeID</span></span>  <br/> |<span data-ttu-id="ff591-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff591-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff591-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff591-126">required</span></span>  <br/> ||<span data-ttu-id="ff591-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff591-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: IssueTarget_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: b9e69edc5bd30ede969bc77d43501a4473e9f69e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772116"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="37b4a-102">IssueTarget_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="37b4a-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="37b4a-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="37b4a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37b4a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37b4a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="37b4a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="37b4a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="37b4a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="37b4a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="37b4a-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="37b4a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="37b4a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37b4a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37b4a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="37b4a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="37b4a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="37b4a-110">Elements and attributes</span></span>

<span data-ttu-id="37b4a-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="37b4a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="37b4a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="37b4a-112">Child elements</span></span>

<span data-ttu-id="37b4a-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="37b4a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37b4a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="37b4a-114">Attributes</span></span>

|<span data-ttu-id="37b4a-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="37b4a-115">**Attribute**</span></span>|<span data-ttu-id="37b4a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37b4a-116">**Type**</span></span>|<span data-ttu-id="37b4a-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="37b4a-117">**Required**</span></span>|<span data-ttu-id="37b4a-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37b4a-118">**Description**</span></span>|<span data-ttu-id="37b4a-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="37b4a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37b4a-120">PageID</span><span class="sxs-lookup"><span data-stu-id="37b4a-120">PageID</span></span>  <br/> |<span data-ttu-id="37b4a-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37b4a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37b4a-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="37b4a-122">required</span></span>  <br/> ||<span data-ttu-id="37b4a-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="37b4a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="37b4a-124">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="37b4a-124">ShapeID</span></span>  <br/> |<span data-ttu-id="37b4a-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37b4a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37b4a-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="37b4a-126">required</span></span>  <br/> ||<span data-ttu-id="37b4a-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="37b4a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: Elemento de mestres ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contém o mestre elementos do documento.
ms.openlocfilehash: d40071c64dc454eeb92f8518f89ef4de8b3b0cb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772315"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="45c1f-103">Elemento de mestres ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="45c1f-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="45c1f-104">Contém o mestre elementos do documento.</span><span class="sxs-lookup"><span data-stu-id="45c1f-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45c1f-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="45c1f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45c1f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="45c1f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="45c1f-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="45c1f-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="45c1f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="45c1f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="45c1f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="45c1f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="45c1f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="45c1f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="45c1f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="45c1f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="45c1f-112">Masters.XML</span><span class="sxs-lookup"><span data-stu-id="45c1f-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="45c1f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="45c1f-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="45c1f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="45c1f-114">Elements and attributes</span></span>

<span data-ttu-id="45c1f-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="45c1f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="45c1f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="45c1f-116">Parent elements</span></span>

<span data-ttu-id="45c1f-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="45c1f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45c1f-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="45c1f-118">Child elements</span></span>

|<span data-ttu-id="45c1f-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="45c1f-119">**Element**</span></span>|<span data-ttu-id="45c1f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="45c1f-120">**Type**</span></span>|<span data-ttu-id="45c1f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="45c1f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="45c1f-122">Master</span><span class="sxs-lookup"><span data-stu-id="45c1f-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45c1f-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="45c1f-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45c1f-124">Contém os elementos que definem um mestre para o documento.</span><span class="sxs-lookup"><span data-stu-id="45c1f-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="45c1f-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="45c1f-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45c1f-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="45c1f-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="45c1f-127">Especifica um atalho de mestre definido no documento.</span><span class="sxs-lookup"><span data-stu-id="45c1f-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="45c1f-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="45c1f-128">Attributes</span></span>

<span data-ttu-id="45c1f-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="45c1f-129">None.</span></span>
  


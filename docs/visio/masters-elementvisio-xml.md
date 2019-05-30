---
title: Elemento Masters (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contém os elementos mestres do documento.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538050"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="f9c68-103">Elemento Masters (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f9c68-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="f9c68-104">Contém os elementos mestres do documento.</span><span class="sxs-lookup"><span data-stu-id="f9c68-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9c68-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="f9c68-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9c68-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f9c68-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f9c68-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="f9c68-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f9c68-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9c68-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f9c68-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f9c68-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f9c68-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f9c68-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f9c68-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f9c68-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f9c68-112">Masters. xml</span><span class="sxs-lookup"><span data-stu-id="f9c68-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9c68-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f9c68-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9c68-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f9c68-114">Elements and attributes</span></span>

<span data-ttu-id="f9c68-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f9c68-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f9c68-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f9c68-116">Parent elements</span></span>

<span data-ttu-id="f9c68-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f9c68-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9c68-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9c68-118">Child elements</span></span>

|<span data-ttu-id="f9c68-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9c68-119">**Element**</span></span>|<span data-ttu-id="f9c68-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9c68-120">**Type**</span></span>|<span data-ttu-id="f9c68-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9c68-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9c68-122">Master</span><span class="sxs-lookup"><span data-stu-id="f9c68-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9c68-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="f9c68-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9c68-124">Contém elementos que definem um mestre para o documento.</span><span class="sxs-lookup"><span data-stu-id="f9c68-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="f9c68-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="f9c68-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9c68-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="f9c68-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9c68-127">Especifica um atalho mestre definido no documento.</span><span class="sxs-lookup"><span data-stu-id="f9c68-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f9c68-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9c68-128">Attributes</span></span>

<span data-ttu-id="f9c68-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f9c68-129">None.</span></span>
  


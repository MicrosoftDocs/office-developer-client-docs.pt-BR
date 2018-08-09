---
title: Elemento de cores (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contém a tabela de cores do documento.
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771521"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="2eba0-103">Elemento de cores (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2eba0-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2eba0-104">Contém a tabela de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="2eba0-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2eba0-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="2eba0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2eba0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2eba0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2eba0-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="2eba0-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2eba0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2eba0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2eba0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2eba0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2eba0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2eba0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2eba0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="2eba0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2eba0-112">Document</span><span class="sxs-lookup"><span data-stu-id="2eba0-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2eba0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="2eba0-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2eba0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2eba0-114">Elements and attributes</span></span>

<span data-ttu-id="2eba0-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2eba0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2eba0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2eba0-116">Parent elements</span></span>

|<span data-ttu-id="2eba0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2eba0-117">**Element**</span></span>|<span data-ttu-id="2eba0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2eba0-118">**Type**</span></span>|<span data-ttu-id="2eba0-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2eba0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2eba0-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="2eba0-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="2eba0-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="2eba0-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2eba0-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="2eba0-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2eba0-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2eba0-123">Child elements</span></span>

|<span data-ttu-id="2eba0-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2eba0-124">**Element**</span></span>|<span data-ttu-id="2eba0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2eba0-125">**Type**</span></span>|<span data-ttu-id="2eba0-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2eba0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2eba0-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="2eba0-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2eba0-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2eba0-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2eba0-129">Contém uma entrada da tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="2eba0-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2eba0-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="2eba0-130">Attributes</span></span>

<span data-ttu-id="2eba0-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2eba0-131">None.</span></span>
  


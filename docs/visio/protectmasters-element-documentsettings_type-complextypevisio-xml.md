---
title: Elemento ProtectMasters (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica se o usuário é impedido de criar, editar ou excluir formas mestras. O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314816"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="268aa-104">Elemento ProtectMasters (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="268aa-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="268aa-105">Especifica se o usuário é impedido de criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="268aa-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="268aa-106">O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração.</span><span class="sxs-lookup"><span data-stu-id="268aa-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="268aa-107">O intervalo de valores possíveis para esse elemento é ' 0 ' ou ' 1 '.</span><span class="sxs-lookup"><span data-stu-id="268aa-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="268aa-108">Um valor de ' 0 ' indica que os usuários podem criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="268aa-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="268aa-109">Um valor de ' 1 ' indica que os usuários não podem criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="268aa-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="268aa-110">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="268aa-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="268aa-111">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="268aa-111">**Element type**</span></span> <br/> |[<span data-ttu-id="268aa-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="268aa-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="268aa-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="268aa-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="268aa-114">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="268aa-114">**Schema file**</span></span> <br/> |<span data-ttu-id="268aa-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="268aa-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="268aa-116">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="268aa-116">**Document parts**</span></span> <br/> |<span data-ttu-id="268aa-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="268aa-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="268aa-118">Definição</span><span class="sxs-lookup"><span data-stu-id="268aa-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="268aa-119">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="268aa-119">Elements and attributes</span></span>

<span data-ttu-id="268aa-120">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="268aa-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="268aa-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="268aa-121">Parent elements</span></span>

|<span data-ttu-id="268aa-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="268aa-122">**Element**</span></span>|<span data-ttu-id="268aa-123">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="268aa-123">**Type**</span></span>|<span data-ttu-id="268aa-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="268aa-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="268aa-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="268aa-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="268aa-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="268aa-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="268aa-127">Contém elementos que especificam configurações de documentos.</span><span class="sxs-lookup"><span data-stu-id="268aa-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="268aa-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="268aa-128">Child elements</span></span>

<span data-ttu-id="268aa-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="268aa-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="268aa-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="268aa-130">Attributes</span></span>

<span data-ttu-id="268aa-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="268aa-131">None.</span></span>
  


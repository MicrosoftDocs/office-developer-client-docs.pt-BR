---
title: Elemento ProtectMasters (DocumentSettings_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica se o usuário é impedido de criar, editar ou excluir formas mestras. O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540690"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="b5d65-104">Elemento ProtectMasters (DocumentSettings_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="b5d65-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b5d65-105">Especifica se o usuário é impedido de criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="b5d65-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="b5d65-106">O usuário ainda pode criar novas formas a partir de uma forma mestra, independentemente dessa configuração.</span><span class="sxs-lookup"><span data-stu-id="b5d65-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="b5d65-107">O intervalo de valores possíveis para esse elemento é ' 0 ' ou ' 1 '.</span><span class="sxs-lookup"><span data-stu-id="b5d65-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="b5d65-108">Um valor de ' 0 ' indica que os usuários podem criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="b5d65-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="b5d65-109">Um valor de ' 1 ' indica que os usuários não podem criar, editar ou excluir formas mestras.</span><span class="sxs-lookup"><span data-stu-id="b5d65-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5d65-110">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="b5d65-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5d65-111">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5d65-111">**Element type**</span></span> <br/> |[<span data-ttu-id="b5d65-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="b5d65-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5d65-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5d65-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5d65-114">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5d65-114">**Schema file**</span></span> <br/> |<span data-ttu-id="b5d65-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5d65-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5d65-116">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="b5d65-116">**Document parts**</span></span> <br/> |<span data-ttu-id="b5d65-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="b5d65-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5d65-118">Definição</span><span class="sxs-lookup"><span data-stu-id="b5d65-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5d65-119">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b5d65-119">Elements and attributes</span></span>

<span data-ttu-id="b5d65-120">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b5d65-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5d65-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b5d65-121">Parent elements</span></span>

|<span data-ttu-id="b5d65-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5d65-122">**Element**</span></span>|<span data-ttu-id="b5d65-123">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5d65-123">**Type**</span></span>|<span data-ttu-id="b5d65-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5d65-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5d65-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="b5d65-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5d65-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b5d65-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5d65-127">Contém elementos que especificam configurações de documentos.</span><span class="sxs-lookup"><span data-stu-id="b5d65-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5d65-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b5d65-128">Child elements</span></span>

<span data-ttu-id="b5d65-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b5d65-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5d65-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5d65-130">Attributes</span></span>

<span data-ttu-id="b5d65-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b5d65-131">None.</span></span>
  


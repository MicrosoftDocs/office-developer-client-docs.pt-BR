---
title: weatherType complexType (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define os parâmetros sobre as condições de clima de um local.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771050"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="13f9d-103">weatherType complexType (esquema de local de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="13f9d-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="13f9d-104">Define os parâmetros sobre as condições de clima de um local.</span><span class="sxs-lookup"><span data-stu-id="13f9d-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="13f9d-105">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="13f9d-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13f9d-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13f9d-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="13f9d-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="13f9d-107">**Schema file**</span></span> <br/> |<span data-ttu-id="13f9d-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="13f9d-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="13f9d-109">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="13f9d-109">**Extension base**</span></span> <br/> |<span data-ttu-id="13f9d-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="13f9d-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13f9d-111">Definição</span><span class="sxs-lookup"><span data-stu-id="13f9d-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="13f9d-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="13f9d-112">Elements and attributes</span></span>

<span data-ttu-id="13f9d-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="13f9d-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="13f9d-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="13f9d-114">Child elements</span></span>

<span data-ttu-id="13f9d-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13f9d-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13f9d-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="13f9d-116">Attributes</span></span>

|<span data-ttu-id="13f9d-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="13f9d-117">**Attribute**</span></span>|<span data-ttu-id="13f9d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13f9d-118">**Type**</span></span>|<span data-ttu-id="13f9d-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="13f9d-119">**Required**</span></span>|<span data-ttu-id="13f9d-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13f9d-120">**Description**</span></span>|<span data-ttu-id="13f9d-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="13f9d-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13f9d-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="13f9d-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="13f9d-123">xs: String</span><span class="sxs-lookup"><span data-stu-id="13f9d-123">xs:string</span></span>  <br/> |<span data-ttu-id="13f9d-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="13f9d-124">required</span></span>  <br/> |<span data-ttu-id="13f9d-125">Especifica um código que está associado ao local para distinguir vários locais com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="13f9d-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="13f9d-126">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="13f9d-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="13f9d-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="13f9d-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="13f9d-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="13f9d-128">xs:string</span></span>  <br/> |<span data-ttu-id="13f9d-129">obrigatório</span><span class="sxs-lookup"><span data-stu-id="13f9d-129">required</span></span>  <br/> |<span data-ttu-id="13f9d-130">Especifica o nome do local.</span><span class="sxs-lookup"><span data-stu-id="13f9d-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="13f9d-131">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="13f9d-131">A value of the type xs:string</span></span>  <br/> |
   


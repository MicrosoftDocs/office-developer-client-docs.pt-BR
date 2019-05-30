---
title: Elemento weatherdata (Esquema de informações meteorológicas do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Define o elemento do clima.
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538981"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="d82c7-103">Elemento weatherdata (Esquema de informações meteorológicas do Outlook)</span><span class="sxs-lookup"><span data-stu-id="d82c7-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d82c7-104">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="d82c7-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d82c7-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="d82c7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d82c7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d82c7-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="d82c7-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d82c7-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d82c7-108">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d82c7-108">**Schema file**</span></span> <br/> |<span data-ttu-id="d82c7-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="d82c7-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d82c7-110">Definição</span><span class="sxs-lookup"><span data-stu-id="d82c7-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d82c7-111">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d82c7-111">Elements and attributes</span></span>

<span data-ttu-id="d82c7-112">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d82c7-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d82c7-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d82c7-113">Parent elements</span></span>

<span data-ttu-id="d82c7-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d82c7-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d82c7-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d82c7-115">Child elements</span></span>

|<span data-ttu-id="d82c7-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d82c7-116">**Element**</span></span>|<span data-ttu-id="d82c7-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d82c7-117">**Type**</span></span>|<span data-ttu-id="d82c7-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d82c7-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d82c7-119">clima</span><span class="sxs-lookup"><span data-stu-id="d82c7-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="d82c7-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="d82c7-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="d82c7-121">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="d82c7-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d82c7-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="d82c7-122">Attributes</span></span>

<span data-ttu-id="d82c7-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d82c7-123">None.</span></span>
  


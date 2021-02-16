---
title: Elemento weatherdata (Esquema de localização do clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define o elemento do clima.
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540928"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="cf0b6-103">Elemento weatherdata (Esquema de localização do clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="cf0b6-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="cf0b6-104">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="cf0b6-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf0b6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="cf0b6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf0b6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="cf0b6-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="cf0b6-108">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-108">**Schema file**</span></span> <br/> |<span data-ttu-id="cf0b6-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="cf0b6-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf0b6-110">Definição</span><span class="sxs-lookup"><span data-stu-id="cf0b6-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf0b6-111">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cf0b6-111">Elements and attributes</span></span>

<span data-ttu-id="cf0b6-112">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cf0b6-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf0b6-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cf0b6-113">Parent elements</span></span>

<span data-ttu-id="cf0b6-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cf0b6-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf0b6-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cf0b6-115">Child elements</span></span>

|<span data-ttu-id="cf0b6-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-116">**Element**</span></span>|<span data-ttu-id="cf0b6-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-117">**Type**</span></span>|<span data-ttu-id="cf0b6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cf0b6-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf0b6-119">clima</span><span class="sxs-lookup"><span data-stu-id="cf0b6-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="cf0b6-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="cf0b6-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="cf0b6-121">Especifica o local para o qual informar o clima.</span><span class="sxs-lookup"><span data-stu-id="cf0b6-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cf0b6-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf0b6-122">Attributes</span></span>

<span data-ttu-id="cf0b6-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cf0b6-123">None.</span></span>
  


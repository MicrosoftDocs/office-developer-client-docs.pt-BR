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
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388438"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="1a56d-103">Elemento weatherdata (Esquema de informações meteorológicas do Outlook)</span><span class="sxs-lookup"><span data-stu-id="1a56d-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="1a56d-104">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="1a56d-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a56d-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="1a56d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a56d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1a56d-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="1a56d-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1a56d-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="1a56d-108">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1a56d-108">**Schema file**</span></span> <br/> |<span data-ttu-id="1a56d-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="1a56d-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a56d-110">Definição</span><span class="sxs-lookup"><span data-stu-id="1a56d-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1a56d-111">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1a56d-111">Elements and attributes</span></span>

<span data-ttu-id="1a56d-112">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1a56d-112">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1a56d-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1a56d-113">Parent elements</span></span>

<span data-ttu-id="1a56d-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1a56d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a56d-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1a56d-115">Child elements</span></span>

|<span data-ttu-id="1a56d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a56d-116">**Element**</span></span>|<span data-ttu-id="1a56d-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1a56d-117">**Type**</span></span>|<span data-ttu-id="1a56d-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a56d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a56d-119">clima</span><span class="sxs-lookup"><span data-stu-id="1a56d-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="1a56d-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="1a56d-120">weatherType complexType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="1a56d-121">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="1a56d-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1a56d-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a56d-122">Attributes</span></span>

<span data-ttu-id="1a56d-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1a56d-123">None.</span></span>
  


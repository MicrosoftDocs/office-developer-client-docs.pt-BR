---
title: Connects_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: d9a3283e9ac16af8997d7e9d632e067ecec7423d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538694"
---
# <a name="connects_type-complextype-visio-xml"></a><span data-ttu-id="3d237-102">Connects_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3d237-102">Connects_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3d237-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3d237-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d237-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3d237-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3d237-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3d237-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3d237-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3d237-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3d237-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3d237-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3d237-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d237-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3d237-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3d237-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3d237-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3d237-110">Elements and attributes</span></span>

<span data-ttu-id="3d237-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3d237-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3d237-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3d237-112">Child elements</span></span>

|<span data-ttu-id="3d237-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3d237-113">**Element**</span></span>|<span data-ttu-id="3d237-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3d237-114">**Type**</span></span>|<span data-ttu-id="3d237-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3d237-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3d237-116">Connect</span><span class="sxs-lookup"><span data-stu-id="3d237-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3d237-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="3d237-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3d237-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d237-118">Attributes</span></span>

<span data-ttu-id="3d237-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d237-119">None.</span></span>
  


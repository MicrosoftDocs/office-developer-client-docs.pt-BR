---
title: PageSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400149"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="dc712-102">PageSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="dc712-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="dc712-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="dc712-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc712-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc712-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dc712-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dc712-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dc712-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dc712-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dc712-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="dc712-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dc712-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="dc712-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc712-109">Definição</span><span class="sxs-lookup"><span data-stu-id="dc712-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc712-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="dc712-110">Elements and attributes</span></span>

<span data-ttu-id="dc712-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="dc712-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dc712-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dc712-112">Child elements</span></span>

<span data-ttu-id="dc712-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="dc712-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc712-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc712-114">Attributes</span></span>

|<span data-ttu-id="dc712-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="dc712-115">**Attribute**</span></span>|<span data-ttu-id="dc712-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc712-116">**Type**</span></span>|<span data-ttu-id="dc712-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="dc712-117">**Required**</span></span>|<span data-ttu-id="dc712-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc712-118">**Description**</span></span>|<span data-ttu-id="dc712-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="dc712-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc712-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="dc712-120">UniqueID</span></span>  <br/> |<span data-ttu-id="dc712-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="dc712-121">xsd:string</span></span>  <br/> |<span data-ttu-id="dc712-122">opcional</span><span class="sxs-lookup"><span data-stu-id="dc712-122">optional</span></span>  <br/> ||<span data-ttu-id="dc712-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc712-123">Values of the xsd:string type.</span></span>  <br/> |
   


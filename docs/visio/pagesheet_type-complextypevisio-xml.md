---
title: PageSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334647"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="fa59e-102">PageSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="fa59e-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fa59e-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="fa59e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa59e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fa59e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fa59e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fa59e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fa59e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fa59e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fa59e-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="fa59e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fa59e-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="fa59e-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fa59e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="fa59e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fa59e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fa59e-110">Elements and attributes</span></span>

<span data-ttu-id="fa59e-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fa59e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fa59e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fa59e-112">Child elements</span></span>

<span data-ttu-id="fa59e-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fa59e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa59e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa59e-114">Attributes</span></span>

|<span data-ttu-id="fa59e-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fa59e-115">**Attribute**</span></span>|<span data-ttu-id="fa59e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fa59e-116">**Type**</span></span>|<span data-ttu-id="fa59e-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fa59e-117">**Required**</span></span>|<span data-ttu-id="fa59e-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa59e-118">**Description**</span></span>|<span data-ttu-id="fa59e-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fa59e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fa59e-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="fa59e-120">UniqueID</span></span>  <br/> |<span data-ttu-id="fa59e-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fa59e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="fa59e-122">opcional</span><span class="sxs-lookup"><span data-stu-id="fa59e-122">optional</span></span>  <br/> ||<span data-ttu-id="fa59e-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fa59e-123">Values of the xsd:string type.</span></span>  <br/> |
   


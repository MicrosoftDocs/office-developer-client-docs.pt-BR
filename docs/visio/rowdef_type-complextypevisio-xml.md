---
title: RowDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: e097e740b543661e5c49a81d75c047c8749ce1d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564252"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="0d08d-102">RowDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0d08d-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d08d-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="0d08d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d08d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d08d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d08d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0d08d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d08d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0d08d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d08d-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="0d08d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d08d-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0d08d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d08d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0d08d-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d08d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0d08d-110">Elements and attributes</span></span>

<span data-ttu-id="0d08d-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0d08d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d08d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0d08d-112">Child elements</span></span>

|<span data-ttu-id="0d08d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0d08d-113">**Element**</span></span>|<span data-ttu-id="0d08d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d08d-114">**Type**</span></span>|<span data-ttu-id="0d08d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0d08d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d08d-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="0d08d-116">CellDef</span></span> <br/> |[<span data-ttu-id="0d08d-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="0d08d-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d08d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d08d-118">Attributes</span></span>

<span data-ttu-id="0d08d-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0d08d-119">None.</span></span>
  


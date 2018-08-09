---
title: Função LISTSHEETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Retorna uma referência de planilha para a forma de contêiner da lista que contém a forma.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772242"
---
# <a name="listsheetref-function"></a><span data-ttu-id="7bd7f-103">Função LISTSHEETREF</span><span class="sxs-lookup"><span data-stu-id="7bd7f-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="7bd7f-104">Retorna uma referência de planilha para a forma de contêiner da lista que contém a forma.</span><span class="sxs-lookup"><span data-stu-id="7bd7f-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7bd7f-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="7bd7f-105">Version Information</span></span>

<span data-ttu-id="7bd7f-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="7bd7f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7bd7f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bd7f-107">Syntax</span></span>

<span data-ttu-id="7bd7f-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="7bd7f-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="7bd7f-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7bd7f-109">Return value</span></span>

<span data-ttu-id="7bd7f-110">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="7bd7f-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7bd7f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd7f-111">Remarks</span></span>

<span data-ttu-id="7bd7f-112">Se a forma não for um membro de lista, a função LISTSHEETREF retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="7bd7f-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="7bd7f-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7bd7f-113">Example</span></span>

<span data-ttu-id="7bd7f-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="7bd7f-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="7bd7f-115">Retorna o valor na célula Height da forma de contêiner da lista que contém a forma.</span><span class="sxs-lookup"><span data-stu-id="7bd7f-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  


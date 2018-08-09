---
title: Função LISTSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Retorna a cadeia de caracteres de separador de lista para a localidade do usuário atual.
ms.openlocfilehash: 77610b2cf3cc515fb5d3e8b4c6c48de98ab4acc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772215"
---
# <a name="listsep-function"></a><span data-ttu-id="75020-103">Função LISTSEP</span><span class="sxs-lookup"><span data-stu-id="75020-103">LISTSEP Function</span></span>

<span data-ttu-id="75020-104">Retorna a cadeia de caracteres de separador de lista para a localidade do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="75020-104">Returns the list-separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="75020-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75020-105">Syntax</span></span>

<span data-ttu-id="75020-106">LISTSEP ()</span><span class="sxs-lookup"><span data-stu-id="75020-106">LISTSEP ()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="75020-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="75020-107">Return value</span></span>

<span data-ttu-id="75020-108">String</span><span class="sxs-lookup"><span data-stu-id="75020-108">String</span></span>
  
## <a name="example"></a><span data-ttu-id="75020-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="75020-109">Example</span></span>

<span data-ttu-id="75020-110">SETF(GETREF(User.Extent), "MAX (largura" &amp; ListSep() &amp; "Altura)")</span><span class="sxs-lookup"><span data-stu-id="75020-110">SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)")</span></span> 
  


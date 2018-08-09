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
# <a name="listsep-function"></a>Função LISTSEP

Retorna a cadeia de caracteres de separador de lista para a localidade do usuário atual.
  
## <a name="syntax"></a>Sintaxe

LISTSEP ()
  
### <a name="return-value"></a>Valor retornado

String
  
## <a name="example"></a>Exemplo

SETF(GETREF(User.Extent), "MAX (largura" &amp; ListSep() &amp; "Altura)") 
  

